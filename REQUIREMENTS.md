# Requirements for the exo-skeleton

Codename: **Exxxo Ito** (Exxxo v0.0)

Layered approach to building an Exo-skeleton, allowing it to be very **modular**, **customiseable**, **affordable** and opens up collaboration with several other industries that could create horizontal solutions around individual layers (or parts of it). After I complete my design, don't forget to **stress-test my design for pressure**.

## Physical Requirements

- One should be able to **push or pull up to 5kg** in any direction with it (each hand) (25Nm?)
- Exo-skeleton **could be counter-forced** by the human wearing it if needed. Motors should not break because of that (usable as breaks)
- Use **elastic bands** to **steer the motion, not control it**
- Maximum impact absorbable: ?

## Functional Requirements

Main movements to be supported at the start. Basically they revolve around 3 things - push, pull and holding balance:

- **Pushups** (burst-like repetitive push movements)
    - advanced: [breakdance] **One-hand top** (burst-like repetitive push movement with hard stops in a fixed body position inbetween)
        - very advanced: [breakdance] **Elbow-hand-elbow jumps** (balancing, explosive burst-like repetitive push movements)
        - very advanced: [breakdance] **Jackhammers** (explosive burst-like repetitive push movements with an elbow pressing against the abs)
        - very advanced: [breakdance] **Airchair hops** (explosive burst-like repetitive push movements with an elbow pressing against the lateral back muscles)
- **Elbowstand** (soft high-precision balancing, locking the elbow in a bent position)
    - advanced: **Handstand** (soft high-precision balancing, locking the elbow in a straight position)
    - advanced: [breakdance] **Elbow spin** (soft high-precision balancing, rotational movement, locking the elbow in a 90-degree position)
        - very advanced: [breakdance] **90s** (soft high-precision balancing, rotational movement, locking the elbow in a straight position)
- **Pullups** (high-torque pull movement)
    - advanced: **One-arm pullup** (very high-torque pull movement)
    - advanced: [parkour] **Muscle-up** (high-torque pull movement followed by a high-torque push movement, transition depending on catching enough momentum)

## Art direction:

"Spiral" design inspired by:

- **Japanese calligraphy**
- **Parametric architecture**

Color scheme inspired by:

- **Mirror's Edge** (lots of white combined with **bright and vivid colors**)

## Software

- Phone: webapp for the phone with NFC support
    - Run **HRNet** on my **phone** to do **real-time pose estimation** on videos
        - Alternative: **TwelveLabs** to recognize the movement
    - **movement editor** that can **smoothen / crop** parts of the moves and **checkpoints for sensors** to make the exo-skeleton act autonomously
        - Alternative: **NVidia Kimodo** via **Vultr** to generate trajectories (text-to-motion)
    - Write the move on an **NFC** sticker attached to a physical card
- Controller: NodeJS app with NFC support
    - Read **NFC**
    - Needs a **program correcting the pose** taht will run the exo-skeleton

## Hardware

### LAYER 0: Body

Layer zero is just **the body** itself. Probably just **skin** or the minimal amount of clothes that the user can carry before starting to put on the Exxxo, layer-by-layer.

### LAYER 1: Soft layer

Layer 1 is the **Base Layer**. It's clothes and fixtures that you could find in shops like Decathlon. It also includes all the **sensors** attached to or printed on soft materials.

- property: largely makes LAYER 2 **compliant with standards for wearables** as it has a lot of contact with the skin
- property: clothes are cheap and allow for **great fit**
- property: acts as a **protection layer**
- property: easily **washable and replaceable**

---

- [base] **9.99£ - Muai Thai gloves [red]** - perfect for printed pressure sensors
- [base] **7.49£ - Wrist compression** - perfect and controls (button/power)
- [base] **19.99£ - Shoulder support** - perfect base for the shoulder with the back support
- [armor] **4.29£ - Inner lower arm protection [black] (hard, bow)** - perfect protection for the lower arm
- [misc] **5.99£ - Anti-friction spray** could be useful for the interaction between the skeleton and clothes
- [misc] **4.99£ - Kinetic tape [blue/pink]** could be great preventive safety measure to test/use the suit. Good for **cable fixtures** against body or the prototype
- [misc] **3.99£ - Boxing wraps [black/blue/white]** - misc, I actually just need velcro patches

### LINK: LAYER 1 & LAYER 2

Layer 2 is mostly hard movable parts. In order to fit them more perfectly to the body and avoid leaving marks (basically making it more comfortable to wear), we need to use some kind of padding between Layer 1 and 2.

- **Velcro padding**
    - {buy}[red/black] **velcro padding** x 3 for the upper arm / shoulder part of the exo-skeleton
    - {buy}[red/black] **Velcro padding** x 2-3 for the shoulder support part of the exo-skeleton
    - {buy}[red/black] **velcro padding** x 2 for the forearm part of the exo-skeleton
    - {buy}[red] **Velcro padding (circular)** x 2 (one for each side of the joint)
    - _Note: Look into accessible helmet padding options on velcros_

### LAYER 2: Exo-skeleton

The core of the exo-skeleton, mostly **3D-printed parts**. Materials at our disposal: **PLA** (allows for perfect finish), **Carbon Fiber** (very hard, takes longer to print, low quantity), **Ninja** (very flexible, up to 600% until reaching a breaking point) and **Rubber-like fillament** (very dyrable, suitable for shoes). **Maximum dimensions**: 350x350x350mm (or more if you place it diagonally).

![](img/sketch-red.png)

- **It has to be foldable** (or "embeddable" like chairs when you put them on top of eachother) so that it doesn't take too much space when packaged
    - property: **portable**
- **Some areas have to be open** to allow full range of movement and contact
- **Think about the printing process** as the structures are much stronger along a single horizontal dimension!
- property: **wearable** under clothes **assuming the hard exo-skeleton parts are static** (no moving parts that are independant the user's original body movements)
    - property: **beautiful** so much more socially acceptable
- **Support structures (Latticeal core)** inside the exo-skeleton: **Voronoi** or even better patterns - to dampen impact and energy
- [white] Exo-skeleton: hard carcass around **forearm**
    - property: **make sure id doesn't exceed maximum ROM**
    - property: **band linkage parts should be parallel if possible**
    - **triple-claw to attach rubber**
    - idea: add **metal rod** to increace toughness?
    - **Rubber-material cushions** to **absorb the impact** around elbows (**Re-entrant (Auxetic) Tessellations**)
    - **cable extrusions**
    - [black] Exo-skeleton: **joint connector** (under the forearm), connecting the joint ends of the forearm part
        - [red] Exo-skeleton: **joint screw - inner elbow** (with a **movable head** for the **motor**)
        - [red] Exo-skeleton: **joint screw - external elbow** (with a **movable head** for the **motor**)
- [white] Exo-skeleton: hard carcass around **upper arm / shoulder**
    - property: **band linkage parts should be parallel if possible**
    - property: **leave 2-part canal for the motor x 2**
        - {buy} **metal inclusion?**
    - **cable extrusions**
    - **handstand full ROM extrusion** (top edge of the shoulder)
    - ? **disc for additional DOF**
    - [red] **Mock engines in a good shape**
- [white] Exo-skeleton: hard carcass for **shoulder support** from the back (might need 2 for them to work as support)
    - ? do we **extend the support to the belt / hips** to improve the back support?
    - {buy} ? do we just **use a backpack with metal plating** to use as a shoulder support?
    - {buy} ? **battery**

### LINK: LAYER 2 & LAYER 3

- {buy} **frictionless** tape to put on top of the rubber band or the exo-skeleton parts where the resistance band rubs against

### LAYER 3: Movement activation
- property: there is **only one mechanism I can use: pull** to assist both push and pull movements as the exo-skeleton is based on using the resistance bands
- property: **hybrid** exo-skeleton. Not really passive, not really active
- property: **resistance bands** are **easily replaceable**
- property: **resistance bands** are **easily configurable** (just pick a different resistance and put it on)
- property: **resistance bands** allow **for much more flexible design**
    - Decathlon: **14.99-19.99£ bands 5-60kg [black/blue/red/orange/yellow]**
- [red] **Resistance band** with **Voronoi extrusions** for pull
    - {buy} **spring**
    - ? Print it in acid green with **Ninja** fillament?
    - {buy}[red] **Motor for pull** movements
        - Stepper motors like **Nema17** might work for me. Also explore **Hoverboard motors**, **bungie cords + gimbal motors**, QDD (**Quasi Direct Drive** actuators), **brushless motors**
- [red] **Resistance band** with **Voronoi extrusions** (for kicks) for push
    - {buy} **spring**
    - ? Print it in acid green with **Ninja** fillament?
    - {buy}[red] **Motor for push** movements
- Controller: **Raspberry Pi Zero** with the following add-ons:
    - {buy} Powerbank or a **battery**
        - property: **powerbank-connectable** (even better: **self-sustainable**)
        - property: place it on a **belt** to make it easily **switchable** like ammo magazines
    - **2.54-inch screen** (visual feedback)
    - **NFC reader** ("install" the movement on the controller)
        - {buy} **Cables**
    - **Physical card** with an AI-generated image of the move
    - {buy} **NFC sticker** for the card (external memory)
    - {buy} **Analog dialer** (power regulator)
        - {buy} **Cables**
    - {buy}[optional] **Fingerprint scanner / button** (controller + privacy)
        - {buy} **Cables**
    - {buy}[optional] **Pressure sensors** (for movement checkpoints) ingrained into soft materials
        - property: allows to **trigger movement checkpoints**, making some of the movements more **autonomous** rather than **"controlled environment only"** (where the exo-skeleton is oblivious about the positioning and the intent of the end-user as it doesn't get any external feedback from sensors)
        - {buy} **Cables**
    - {buy}[optional] **Gyroscopes** (for relational positioning of the parts, could be done via resistance measurements instead)
        - {buy} **Cables**
    - **Local models only**, something like Gemma4 or custom **RL models**
    - **2FA lock** like **Ubi-key**

### LINK: LAYER 3 & LAYER 4

- {buy} **Friction-reducing spray or material** to be put over the bands (exo-skeleton parts are fine as there are no moving parts, they are all static, mirroring user's movement)
- property: **wearable** under clothes

### LAYER 4: Clothes

### LAYER 5: Machine

Any other more powerful machine could be integrated at this level (**self-driving cars** or **much bigger exo-skeletons**, perhaps?)