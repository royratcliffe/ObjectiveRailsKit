# Objective Rails Kit

[![Build Status](https://travis-ci.org/royratcliffe/ObjectiveRailsKit.png?branch=master)](https://travis-ci.org/royratcliffe/ObjectiveRailsKit)

ObjectiveRailsKit is an umbrella framework. Under the shadow of the umbrella
sit three Rails-like sub-frameworks:

1. ActiveResourceKit
2. ActiveModelKit
3. ActiveSupportKit

Import all three using the ObjectiveRailsKit.h monolithic header, as follows.

	#import <ObjectiveRailsKit/ObjectiveRailsKit.h>

Then link against `ObjectiveRailsKit.framework`.

## Linking Against ObjectiveRailsKit

1. Add the ObjectiveRailsKit project to your application project.
2. Add the ObjectiveRailsKit framework as a target dependency.
3. Link your application binary against `ObjectiveRailsKit.framework`.
4. Add a new Copy Files build phase.
   1. Make the destination equal to Frameworks.
   2. Add `ObjectiveRailsKit.framework` to the list of products to copy.

## Umbrella Framework

Apple say, “Don't do it!”

They prefer that third-party developers deploy single stand-alone frameworks.

## Sub-Modules

ObjectiveRailsKit comprises three Git sub-modules.

To build the kit, you need to check out those sub-frameworks from their Git
repositories. You do this using:

	git submodule update --init

You need to run this Git command even when incorporating ObjectiveRailsKit
itself as a submodule of another Git repository.

## iOS Support

ObjectiveRailsKit is an umbrella framework. iOS does not as yet conveniently
support frameworks. Nevertheless ObjectiveRailsKit does build an iOS target.

The iOS target combines all three Active kits (support, model and resource)
into a single static library, `libObjectiveRailsKit.a`.

