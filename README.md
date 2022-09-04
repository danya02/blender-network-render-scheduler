# blender-network-render-scheduler
Scripts to make Blender render projects cooperatively over a network

This is designed for environments where you only have access to a Blender GUI, and otherwise limited access to the computer.
Examples of such environments include school computer classes, internet cafes and gaming centers.

To use this, a control server is required.
This must be a computer that has a publicly addressable IP address.
Various VPS providers will do.

Design goals: 
- should not require any interaction after typing in a bootstrap script
- should handle worker computers connecting and disconnecting at any time
- should not use any libraries other than the ones built into Blender
- should use the hard drive as little as possible, and delete all created files as soon as we can
- should support switching between different projects at runtime, without resetting the worker computers
- should leave the GUI interactive
