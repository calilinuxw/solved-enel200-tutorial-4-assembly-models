Download Link: https://assignmentchef.com/product/solved-enel200-tutorial-4-assembly-models
<br>
<strong>   Assembly Models </strong>

Just as in real life situations, SolidWorks allows us to take parts and assemble them together. The assemblies follow certain rules, based on how we define the assembly, such that we are able to make parts move as a virtual mechanism.

Assembly models are of great practical importance as they can be used for checking fits and clearances between parts before anything is actually made. Dimensions of part models can be changed within the assembly modelling environment, enabling context sensitive design work to be done.

<strong>Goals </strong>

<ul>

 <li>Understand what assembly models are and how to create them</li>

 <li>Know how to insert parts into an assembly and apply assembly mates</li>

 <li>Be able to choose the best way to define assembly mates, and justify why your decision supports creating a robust assembly model</li>

</ul>

Exercise 1:          Engine Assembly

We’ve already modelled all of the major parts of the engine, so now we can assemble them to check how they fit together and see the mechanism working.

Before beginning this we’ll have a quick look at where we will end up. Assembly models are a different type of file to Part models, but they have many similarities. Shown below is a screenshot of the completed assembly model and the Feature Manager area. Just like a Part model there are three planes and an origin to define the space the model is in, but the big difference is that instead of having geometry features in the history tree, there are parts. At the bottom of the history tree is an item called Mates, which contains a list of all the part relationships that you have defined when building the assembly.










To begin the assembly select New from the File main menu to bring up the New SolidWorks Document popup window. Up until now you have been selecting UC Part Template whenever creating a new file, but this time select UC Assembly Template.







By default SolidWorks assumes you want to begin by inserting the first part immediately, so the Insert Component dialogue is invoked as soon as the new file opens. If you have any other parts open currently they will appear in the Open Documents list within this dialogue, otherwise the list will be blank. We want to insert the engine block into the assembly, so either select this from the list or click the Browse button below the list to search for the part. If you need to Browse for the file, make sure that the filter in the bottom right of the popup window is set to either <em>Part</em> or <em>All files</em> otherwise it will not ‘see’ your part files.

Once you have found your

Engine Block it will appear in the Graphics area as shown. Notice that there are two sets of planes, the one that belongs to the part and the bottom set that belong to the assembly. If we were to click the mouse button in the position shown the part would be inserted in this location, but to make things easier later we would prefer it if the part and assembly planes were all coincident (oriented the same and share the same origin). To make this happen easily, simply click on the green tick in the Insert Component dialogue and the part will automatically be moved to the position we want.          <sup> </sup>

Having the assembly planes aligned with at least the first part in the assembly is not essential, but it is very sensible. The assembly planes and assembly origin are the only things that we can rely on to never change in the assembly model – they will always be there and unchanged, no matter what parts are modified, added, or removed. This means that any positional references to these planes will be robust and reliable, which becomes a major consideration especially when dealing with assemblies of many parts.

By default the first part to be inserted into the assembly becomes fixed, or in other words is not able be dragged on the screen. Check next to the name of the part in the Feature Tree and you will see the letter f in brackets (f). We could right mouse button click on the part in the Feature Tree and select Float to allow the part to move, but this is not usually what you will want to do with the first part. The first part in an assembly is usually chosen because it will be stationary with respect to the whole assembly in a way that reflects reality. We could start by inserting the piston first and have that as the fixed part (SolidWorks wouldn’t care!), but it wouldn’t reflect reality.

Now we have our first part fixed in a known location, we can start to assemble other parts. There are two fundamental ways to position additional parts in the assembly, either by doing as we did with the first part by positioning with respect to the assembly planes, or by positioning with respect to existing part planes or part geometry.

<table width="616">

 <tbody>

  <tr>

   <td width="205"> </td>

   <td width="55"> </td>

   <td width="150"><strong>Advantages </strong></td>

   <td width="55"> </td>

   <td width="150"><strong>Disadvantages </strong></td>

  </tr>

  <tr>

   <td width="205"><strong>Position with respect to Assembly Planes </strong></td>

   <td width="55"></td>

   <td width="150">Robust because assembly planes never change</td>

   <td width="55"></td>

   <td width="150">Position of part will not automatically update to follow design intent</td>

  </tr>

  <tr>

   <td width="205"> </td>

   <td width="55"> </td>

   <td width="150"> </td>

   <td width="55"></td>

   <td width="150">Slower to create</td>

  </tr>

  <tr>

   <td width="205"><strong>Position with respect to Part Planes or part geometry </strong></td>

   <td width="55"></td>

   <td width="150">Fast and intuitive to create (can see where parts fit)Position of parts will update according to design intent</td>

   <td width="55"></td>

   <td width="150">Rebuild errors when planes or geometry that are being mated to are changed or deleted</td>

  </tr>

 </tbody>

</table>




Because there are pros and cons for either approach there is no right or wrong and you will use both in different situations. If the assembly model is simple and you are not expecting to make large modifications to the form of the parts, then it is better to position with respect to other parts. If it is a particularly large or complex model and you are expecting to make significant modifications to parts then you should consider positioning at least some of the parts with respect to the assembly planes.

In our case we are going to use a combination of these two approaches for positioning the first part to get a compromise between the benefits. We’ll go ahead and do this and then discuss further to justify our choice.




Select Insert Components from the Assembly tab of the

Command Manager and a dialogue will open in the Feature Manager area that is the same as when you first created the part. If the Assembly tab is not available in the Command Manger, right click on any of the existing tab names and toggle on the Assembly tab.




Browse to find the front cover part and open it. Just as with the engine block, you should see it appear in the Graphics Area and it will follow your mouse pointer around. This time we do not want to place it in the default location (aligned with the assembly planes) so just click on an approximate location next to the engine block.




Select Mate from the Assembly tab of the              Command Manager. Mates work in a similar way for assemblies as Sketch Relations do for sketches. They allow us to define geometric relationships which constrain where an entity is located and how (or if) it can move. As soon the dialogue opens in the Feature manager area you can select the two green faces as shown, and these selections will be recorded in the Mate Selections box. In the orientation shown in the example you would only be able to select the green face on the engine block, so you’ll need to rotate the view in the Graphics

Area to access the face on the front cover part.




You should note that when you select the second face the front cover part will move so that the two faces are coincident (on the same plane) with each other. SolidWorks has made a prediction that this is what you wanted so has created a coincident mate automatically. In this case the software is correct (and thus saved you an additional click), but there are other mates between these faces that are possible, for example Parallel, Perpendicular, or Tangent. Experiment by clicking on these to see the effect on in the Graphics Area, but then change it back to Coincident and click the green tick to accept the new mate.







After the mate has been accepted the dialogue box remains active so you can immediately begin creating another mate. This is another example of SolidWorks attempting to predict what you will do next and therefore saving extra clicks. Usually you will want to create a number of mates to define the position and possible movement of a part, so more often than not SolidWorks will be correct with this prediction.

Notice how the Coincident mate that has already been created is now listed in the Mates box at toward the bottom of the dialogue. If you wanted to make a change to it at this stage you could click on it in that list and it would become active for editing again.




Create another mate by selecting the Right plane of the front cover part and then the Right Plane of the assembly. Notice that the Right Plane of the assembly and the Right plane of the engine block are in the same plane, so be careful that the one you are selecting belongs to the assembly (see the popup description when you move the mouse over the edge of the plane).




Accept this mate and then create one more in a similar way for the Top Plane of the front cover part and the Top Plane of the assembly. The front cover should now be sitting correctly on the front of the engine block and be full constrained since we have defined its position in three orthogonal planes.

Now to reflect on how we defined the mates for locating this first part. The first mate relies on a geometry mate with the engine block. This mate will fail if the engine block is ever deleted or the end face of the engine block is removed from the model. We consider that neither of these is likely, so for the convenience of having the front cover ‘glued’ to the front of the engine block, even if the <em>size</em> or position of the engine block front is changed, this approach is a good bet. For the other two mates we chose to mate the part with the assembly planes, which are the most stable entities (they can never be changed or removed) in the model. We could have assembly mated with two of the small holes that are in the block and the cover, or made the sides of the engine block and front cover coincident, and perhaps this seems more intuitive. In practise however, there is a fairly high probability that the position of these holes or sides of the engine block or front cover will be moved at some time in the development of the design. The result of this would be that either the mates would fail, or the front cover would move away from the central axis of the engine block, which is a primary design intent for the assembly. Having the mates aligning the part planes with the assembly planes makes sure that the design intent is embedded regardless of any part modifications.

In summary, <strong>pay close attention to how you form mates between parts</strong>. SolidWorks <em>will allow</em> you to do it in ways that can create a lot of work for you later on in the project! Wherever possible create mates with assembly planes and that embed your design intent for how parts should relate to each other.

Repeat this process again with the rear cover part. After inserting the part you may see that it’s orientated incorrectly (depending on the orientation that you modelled the part in). In the example the front cover and rear cover were modelled in the same orientation, so the rear one needs to be turned around to fit into the engine assembly. The part can be inserted in any place close to the engine, and then select Mate from the Assembly tab of the Command Manager. As before select the two faces we want to be coincident and the rear cover will move a little to obey the coincident mate that SolidWorks has correctly predicted that we want.




It will still be in the wrong orientation however, so to fix                 this click on the Mate Alignment button shown at the bottom of the example screen shot. This will flip the part around so it is facing the same way, but also tilt it onto an angle on the axis that it is still free to move on. This will be corrected when the plane mates are applied, so click the green tick to accept the first mate, and then create coincident mates between the Top and Right planes of the rear cover and the Top and Right assembly planes. Again, be careful that you are selecting the planes that belong to the assembly and not the front cover or the engine parts.







After creating these three mates

the dialogue in the Feature Manager area should look like the example shown, with the mates all listed in the Mates box at the bottom of the dialogue. Also the rear cover should be aligned sitting centrally on the rear of the engine block. Accept the mates just created by clicking on the green tick at the top of the dialogue once more. You can see that in assemblies the planes from all the parts can quickly make quite a mess in the graphics area, but at any time you can toggle planes on and off in the View menu from the Main Menu. Toggle them on and off as you need them.




So far we have only been using coincident mates, but there are many others that can be applied to define different relationships between parts. Our aim when applying mates is to lock down all of the three translational and three rotational freedoms that a part begins with, except the ones that we want to still be able to move in the assembly. The next part illustrates this point.

Insert the crankshaft part into the engine assembly and place it approximately close to the engine. Our design intent is that the shaft should be located concentrically with the hole in the front cover, the face of the crank web should be 1mm gap from the inner face of the front cover, and the crankshaft should be able to rotate about the shaft axis (and this is the only movement it is capable of)




Begin by applying a mate between the outer cylindrical surface of the long end of the crankshaft, and the large cylindrical hole in the front cover.




Now that we have selected cylindrical surfaces rather than planar surfaces, SolidWorks makes a different prediction about the mate that we likely want. This time it guesses, correctly, that we want a concentric mate. This type of mate makes the axis of two cylindrical parts coincident, but still allows the parts to rotate around these axis and also to move along the axis.

After you create this first mate you may note that crankshaft is facing the wrong way, as in the example. To correct this press the Mate Alignment button in the mate dialogue and it will flip over to face the correct way. After flipping over the crankshaft may seem to disappear into the engine, at least partially. Rotate the model around a bit so you can see inside the end of the front cover and you will see the crankshaft is in there. It is best that the crankshaft is pulled out of the engine for easy access to it, so click on the end face of it, and with the mouse button held down, pull the crankshaft out by moving the mouse over. Let the mouse button go and it will stay in this position. Note that doing this does not create any new mates, it is simply moving the part in the graphics area in obedience to mates that are already there. If the concentric mate is working properly you should only be able to drag the crankshaft along and rotate it around its own axis.

All that remains now is to set the distance between the inner face of the front cover and the crank web (1mm) and the complete design intent will be met. This mate is achieved in a similar way to before, by selecting the two planes and defining the mate, but practically we have a problem this time in that we cannot see the inner face of the front cover to enable us to select it. The easiest way to solve this is to temporarily hide the engine block by left mouse button clicking while the pointer is over any surface belonging to the part, and then selecting Hide.




Now that you can see the faces, select both to generate a mate between them and, as expected, SolidWorks predicts that we want a coincident mate between them. This time the software has it wrong because we actually want a Distance mate. This is similar to a coincident mate in that the faces are parallel and able to slide against each other, but the Distance mate enforces a fixed separation between the faces. Select the Distance mate from the list, and type in a value of 1.5mm. You should now see the crankshaft move slightly along its axis so this distance between the two faces is established. There are two ways the Distance mate can be satisfied, either by having the faces separated by 1.5mm or overlapping each other by 1.5mm.




If your assembly has moved so that it is overlapping then click in the check box next to the words Flip Dimension (just below where you entered the dimension). Check that there is now a gap between the crankshaft and the front cover, and then click the green tick twice to accept this mate and exit the mate creation dialogue.




This raises an important point to note about SolidWorks assemblies; <strong>they will quite happily allow parts to overlap each other</strong>. Unlike physical space where solid parts cannot share the same volume, in the CAD model there is no such restriction. It is always up to the designer to check for any interference between parts, but SolidWorks does provide a tool to assist with this (see the <em>Interference Detection</em> tool from the Tools menu in the Main Menu bar).

While building an assembly model it is wise to check frequently that it is behaving as you expect it to.  The easiest way to do this is to check one part at a time by clicking on any surface belonging to it and, with the mouse button still held down, move the mouse to check what happens. If the part is able to move in some way then it will, otherwise it will remain stationary. In this case the front and rear covers should not be able to move, and the crankshaft should only be able to rotate around its own axis.

If any part of the assembly behaves in an unexpected way, either by allowing some movement you don’t want, or not allowing a movement you do want, then you need to check the mates you have applied or consider if any more need to be added. All of the mates created so far can be found and edited from the Feature Manager area. Click on the + symbol next to the Mates item in the Feature Tree and you will see a list of all the mates in the assembly. Left mouse clicking on any of them will open a popup graphical menu as shown in the example, the top left icon in which will open the Mate dialogue for that item so you can edit it.

Given that you are satisfied with how the engine assembly is working up until this state, we’ll continue by fitting the piston into the cylinder, and then connecting the piston to the crankshaft with the connecting rod. We could fit either of these parts first, and it will not make any difference to the end result, but arbitrarily we’ll do the piston first.




Insert the piston part into the assembly, placing it next to the engine as a starting point.

The cylinder block is still hidden, and since we want to mate the piston with the bore in this part it needs to be shown again. Select it in the Feature Tree and click on the Show Components icon in the popup graphical menu.




Open the mate dialogue by clicking on the Mate tool in the Assembly tab of the Command Manager, and then select the outer surface of the piston and the inner surface of the cylinder block bore. SolidWorks correctly predicts that we want a concentric mate between these parts, so click the green tick to accept this mate, and because this is the only mate required for this part, click it again to exit the mate dialogue.

Check the piston behaves as you expect by dragging it in the graphics area. It should move up and down in line with the cylinder bore, and also be able to rotate around its own axis. Once the connecting rod is fitted the rotation around its own axis will be prevented by the mate that will be formed with it, but for now it’s OK.

Even though it might seem obvious at first, it’s important to reflect on why we chose the piston surface and the bore surface to make the assembly mate. Remember this is a geometry mate, so if either of these surfaces that we have selected to mate are deleted or fundamentally changed (not just a size change) during subsequent part modifications then the assembly mate will fail. We could have achieved the same result, and increased robustness, by mating the Right and Front planes of the piston part and the assembly. In this case however the decision to go with the geometry mate is reasonable because we are sure that the piston and they cylinder bore will never change from their basic cylindrical shape, and they will never be removed. Also the geometry mate gives the advantage that it is intuitive in that we know the piston fits into the bore, so the mate more closely follows the physical world than aligning to the assembly planes would. As assemblies become more complex, intuitiveness such as this becomes increasingly important when it inevitably comes time to make modifications and fix problems.

To complete the crank slider mechanism that is  fundamental to our engine, insert the Connecting rod part and place it near the other engine parts <sup> </sup>in the Graphics Area. Open the mate dialogue and  select the surfaces of the hole though the piston and the hole through the small end of the            connecting rod. SolidWorks predicts correctly that we want a concentric mate between these, so accept this first mate.




In a real engine we would have a pin (called a gudgeon pin) that fits through these holes to hold the piston onto the connecting rod, but in the CAD model we have omitted it for brevity and simplicity. This is an important capability of assembly models in that it allows us to take some shortcuts by omitting parts, but still have the assembly behave as if they are there.

For the second mate select the small cylindrical part on the crankshaft (called the crank pin) and the hole in the big end of the connecting rod, as shown by the green surfaces in the example. Accept the concentric mate that SolidWorks correctly predicts. This mate will rotate the connecting rod so that the hole through it is aligned with the crank pin, and because there is a mate between the piston and the crankshaft the piston will rotate also. As mentioned before, because of the combination of mates the piston will no longer be able to rotate about its own axis.




Check the behaviour of the model again, by dragging one part at a time. The crankshaft should still be able to rotate, and when it does the piston should move up and down with the connecting rod between it and the crankshaft.

Everything should be OK now, except when you try dragging the connecting rod you will notice that it is still free to move toward the front or rear of the engine. Try dragging the connecting rod right out the front of the engine and turning the crankshaft – the mechanism still works perfectly! This is another example of how assembly models allow us to do things that are not possible in the real world – sometimes this is an advantage because it enables us to put working models together quickly that are not perfect, but it does also put a responsibility on the designer to check everything very carefully before considering having parts manufactured to build the real thing.

To fix this problem with the connecting rod we need to add another assembly mate. The design intent is that the connecting rod should be located centrally within the piston (in the real part there would be some shoulder features inside the piston to hold the connecting rod centrally). To embed this intent into the model create a new coincident assembly mate between the Right Planes of the piston and the connecting rod (although if you have modelled these parts in a different orientation then your planes will be different).

Because the piston is mated into the cylinder bore, and the cylinder bore belongs to a fixed part (the cylinder block) then the only way to satisfy this new mate is for the connecting rod to move toward the piston. All being well you should see this happen, so accept the mate and exit the mate dialogue. Check the assembly by dragging parts in the Graphics Area again, just to be certain that all is as expected now.

To finish the part, insert the cylinder head part and apply assembly mates to meet the design intent that it fits on top of the cylinder block and is not able to move at all. There will be three mates required to complete this, and think about justifying why you have used geometry mates or mates to planes.




It’s often useful to be able to see through parts in an assembly to check the operation of a mechanism inside or behind a part, and in SolidWorks this is very easy to do. Click on any surface belonging to a part in Graphics Area and click on the Change Transparency icon in the popup graphical menu. In the example shown the cylinder block is changed to transparent so the crank slider mechanism can be observed operating within it.







Exercise 2: Fuel Tank Assembly

The two fuel tank sheet metal parts will  be soldered together in the real assembly, but for out SolidWorks assembly we will just position them as they would be when soldered.

Sheet metal parts are not treated any differently to other part in an assembly, so can be assembled with each other or with other parts that are not sheet metal.

Begin by creating a new assembly and inserting the fuel tank bottom (shown in blue) into the default position. Remember this is done by just clicking on the green tick without clicking in the graphics area to define a position. The default position will align the part planes with the assembly planes and fix the position of the part.

<em>If the parts were modelled with the wrong dimensions they will not fit together perfectly, but the software doesn’t care. SW will let you assembly parts that overlap or have gaps. Don’t worry about this, just focus on the techniques for assembling parts. </em>

Insert the fuel tank upper and apply assembly mates to support the design intent that there should be a 1mm flange formed by the bottom fuel tank part all around the periphery of the top fuel tank part. This flange is there to make the soldering process easier; having a corner causes the molten solder to flow easily along the joint.

If you have modelled the two parts in the same orientation then the assembly operation becomes trivial, each part could just be ‘dropped’ into the model in the default position and fixed there. If not then you will need three assembly mates to position and constrain the upper fuel tank part in all directions.

Exercise 3:          Car Assembly

Members of an assembly are either parts, or they are sub-assemblies. The two assemblies we have created so far have only included parts, but these assemblies themselves are now going to become sub-assemblies in the overall car assembly. There can be as many layers of sub-assemblies as you want in your model, for example you can have an assembly that contains sub-assemblies, and that sub-assembly can contain parts and/or subassemblies etc. The final assembly, which is not used as a sub-assembly in any further assembly, is referred to as the top level assembly.

As with most aspects of CAD modelling, there is an element of design in how you go about constructing the assembly. For example we could use no sub-assemblies at all and just mate all of the parts into the top level assembly. This would work, but is often not the best strategy. Using subassemblies in certain instances gives us the following advantages:

<ol>

 <li>Sub-assemblies can be reused in as many assemblies as you want. We could design lots more model race cars and reuse the same fuel tank and engine as sub-assemblies without having to do any more work.</li>

 <li>Real sub-assemblies are often used in manufacture for reasons of efficiency and production management, so it makes sense to replicate these in the CAD assembly so that BOM (bill of materials) drawings can be done of these for use in the workshop or factory.</li>

 <li>CAD assemblies can become very difficult to manage when there are many parts to deal with, and in a worst case scenario if a large assembly has too many rebuild faults it can become practically impossible to fix. Sub-assemblies allow us to divide and conquer, for example it’s much easier to maintain 10 assemblies with 50 assembly mates in each, rather than 1 assembly with 500 assembly mates.</li>

</ol>

As a recap on where we are heading, the image below shows the parts and sub-assemblies we are going to put into our assembly. The engine (blue) and fuel tank (purple) are sub-assemblies and everything else in the assembly is a part.

We’ll start by creating another assembly file and inserting the car body into it in the default location. This gives a good starting point, but to proceed further we really need to do some geometry assembly mates with the body, so we need to model some features to assemble to.

<ul>

 <li>Holes for front and rear axles</li>

 <li>Boss for suspension sprint to locate on</li>

 <li>Engine mounts</li>

 <li>Pads for the fuel tank mount lugs to sit on</li>

</ul>

It is often the case that, while working in an assembly, we realise there is some more modelling that needs to be done at a part level. SolidWorks allows two workflows to deal with this situation.

The first is that we can click on any surface belonging to a part in the graphics area and then select the Open Part icon from the popup graphical menu. This will open the part so we can edit it just as if we just opened the part from file explorer.

The second option is that we can do the same thing, but instead of selecting the Open Part icon, select the Edit Part icon. The difference here is that the part becomes active for editing right where it is in the assembly modelling environment. This is particularly useful for making dimensional changes to make the part fit with other parts in the assembly because you can still see all of the other parts in the assembly, and how they relate to the part you are editing.

For our example here there is no advantage of editing in the assembly environment as we don’t have the other parts in the assembly yet, so we’ll just use the first method to quickly open the part and do some part modelling.




Create an extruded cut through the body using the sketch as shown, which will allow us to position the front and rear axles.










To mount the suspension spring, create a plane 30mm up from the Top plane and draw a sketch as shown (<em>Features tab, </em>

<em>Reference Geometry, Plane)</em>. Extrude this downwards with the end condition set as Up To Next so that the boss will extend to the bottom of the inside of the car.

To mount the fuel tank draw a sketch as shown on a plane 13mm up from the Top plane and extrude it

downwards with the Up To Next end condition.




Finally, for the engine mount, sketch as shown on a plane 36mm up from the Top plane and then extrude this the same as you did for the fuel tank mounting pads.







Insert the engine and fuel tank subassemblies and position them into the assembly using a combination of geometry and assembly plane mates. The height of them should be set by placing them on the geometry features we have just created, but the longitudinal and transverse position should be set with assembly mates to the assembly planes.

Similarly, insert the front axle, applying a mate to position it concentrically through the holes in the body, but using a assembly plane mate to hold it centrally on the body. The design intent is that it should only be able to rotate around the axis through the holes in the body.

The suspension spring is the next part to be fitted, but this presents us with a little difficulty. After inserting it you will notice that there is no convenient way to mate it onto the cylindrical boss that we created. The answer here is that we can create assembly mates of axis in parts and features, so if we can find or create an axis for the spring and the cylindrical boss then we can simply make them coincident.

All axisymmetric (anything that can be created with a revolve around an axis) features that are created automatically have a type of axis created for them which SolidWorks calls a Temporary Axis. From the View menu in the Main Menu bar select the Temporary Axis item and you can see all of them in the graphics area, including for the cylindrical boss that the spring will be located on.






















With the axis tool dialogue open, select the two planes (Right and Front in the example) and you will see that a yellow preview axis appears. There are a number of ways to define and axis, as you can see from the list in the dialogue, but SolidWorks will make a selection for you based on what geometry you select for the definition.

Click the green tick to accept this axis and then return to the assembly model. Make sure that both Axis and Temporary Axis are turned on in the View menu, and you should see your new axis on the spring as well as the existing Temporary Axis in the mounting boss. Create a coincident mate between them and the spring will move so that it is aligned over the boss.

To set the height of the spring, apply a Distance assembly mate between the Top plane of the spring and the end surface of the location boss.

Insert one of the front wheels and one of the rear wheels and create assembly mates to position them on the left side of the car. The design intent is that the front wheel should be mounted on the suspended axle, and the wheel should locate against the shoulder on the axle. The wheel should be free to turn about its axis.

The rear wheel doesn’t have an axle detailed yet in our incomplete model of the race car, but the design intent is that it is concentric with the holes we created through the body, and the centre plane of the wheel is 75mm from the centre line of the body. The wheel should be free to turn about its axis.

We could do the same operation for the wheels on the other side of the model, but it is more convenient to use the Mirror Components feature to create the other instances of the wheels in the assembly. This is found in under the Pattern dropdown menu within the Assembly tab of the Command Manager.




Select the Right plane from the Graphics Area as the mirror plane, and then select the front and rear wheel as the Components to Mirror.




Click the green tick and the new instances of the wheels will be created on the other side of the car. Look in the Feature Manager Tree and you will see that a Mirror Component feature has been added below the Mates. Click on the + next to this and you will see the new part instances that have just been created.




The mirrored component positions are updated whenever the parent (original) part is moved, so there is no need to recreate the mirror if a part is moved. Test this by moving the front left wheel. When it moves up and down with the suspension, or rotates, the wheel on the right side will do exactly the same.





