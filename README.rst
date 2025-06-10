.. Copyright 2016 The Cartographer Authors

.. Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

..      http://www.apache.org/licenses/LICENSE-2.0

.. Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.

============================
Cartographer ROS Integration
============================

|build| |docs| |license|

Note
=======

**This repository contains a minor modification to the original Cartographer_ros code.**
At `node.cc`_ and `node.h`_ , there are some additional lines for publish pose data at 'base_link' frame.
There should be no translation between ``tracking_frame`` and the IMU frame. 
Therefore, if there is any translation between them, 
although it is possible to create a new node to obtain the pose of base_link, it was instead implemented internally.


.. _node.cc: https://github.com/jsryu118/cartographer_ros/blob/master/cartographer_ros/cartographer_ros/node.cc
.. _node.h: https://github.com/jsryu118/cartographer_ros/blob/master/cartographer_ros/cartographer_ros/node.h




Purpose
=======

`Cartographer`_ is a system that provides real-time simultaneous localization
and mapping (`SLAM`_) in 2D and 3D across multiple platforms and sensor
configurations. This project provides Cartographer's ROS integration.

.. _Cartographer: https://github.com/cartographer-project/cartographer
.. _SLAM: https://en.wikipedia.org/wiki/Simultaneous_localization_and_mapping

Getting started
===============

* Learn to use Cartographer with ROS at `our Read the Docs site`_.
* You can ask a question by `creating an issue`_.

.. _our Read the Docs site: https://google-cartographer-ros.readthedocs.io
.. _creating an issue: https://github.com/cartographer-project/cartographer_ros/issues/new?labels=question

Contributing
============

You can find information about contributing to Cartographer's ROS integration
at `our Contribution page`_.

.. _our Contribution page: https://github.com/cartographer-project/cartographer_ros/blob/master/CONTRIBUTING.md

.. |build| image:: https://app.travis-ci.com/cartographer-project/cartographer_ros.svg?branch=master
    :alt: Build Status
    :scale: 100%
    :target: https://app.travis-ci.com/cartographer-project/cartographer_ros
.. |docs| image:: https://readthedocs.org/projects/google-cartographer-ros/badge/?version=latest
    :alt: Documentation Status
    :scale: 100%
    :target: https://google-cartographer-ros.readthedocs.io/en/latest/?badge=latest
.. |license| image:: https://img.shields.io/badge/License-Apache%202.0-blue.svg
     :alt: Apache 2 license.
     :scale: 100%
     :target: https://github.com/cartographer-project/cartographer_ros/blob/master/LICENSE

