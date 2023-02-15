.. _synchronization_sample:

Synchronization Sample
######################

Overview
********

A simple application that demonstrates basic sanity of the kernel.
Three threads (A, B and C) take turns printing a greeting message to the console,
and use sleep requests and semaphores to control the rate at which messages
are generated. This demonstrates that kernel scheduling, communication,
and timing are operating correctly.

Building and Running
********************

This project outputs to the console.  It can be built and executed
on QEMU as follows:

.. zephyr-app-commands::
   :zephyr-app: synchronization3
   :host-os: unix
   :board: qemu_cortex_m3
   :goals: run
   :compact:

Sample Output
=============

.. code-block:: console

   threadA: Hello World!
   threadB: Hello World!
   threadC: Hello World!
   threadA: Hello World!
   threadB: Hello World!
   threadC: Hello World!
   threadA: Hello World!
   threadB: Hello World!
   threadC: Hello World!
   threadA: Hello World!
   threadB: Hello World!
   threadC: Hello World!
   threadA: Hello World!
   threadB: Hello World!
   threadC: Hello World!

   <repeats endlessly>

Exit QEMU by pressing :kbd:`CTRL+A` :kbd:`x`.
