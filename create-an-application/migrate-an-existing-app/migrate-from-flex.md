---
# Licensed to the Apache Software Foundation (ASF) under one or more
# contributor license agreements.  See the NOTICE file distributed with
# this work for additional information regarding copyright ownership.
# The ASF licenses this file to You under the Apache License, Version 2.0
# (the "License"); you may not use this file except in compliance with
# the License.  You may obtain a copy of the License at
# 
# http://www.apache.org/licenses/LICENSE-2.0
# 
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.

layout: docpage
title: Migrate from Flex
---
<!-- This is from material created by Peter Ent and modified by Tom Chiverton: https://cwiki.apache.org/confluence/pages/viewpage.action?pageId=34013930 -->
<!-- I have not added links to other pages, or to other sites, yet -->
# Migrate from Flex
If you have developed applications using <a href="http://flex.apache.org" target="_blank">Apache Flex</a>, or Adobe Flex before it, your applications probably combine MXML and ActionScript files along with resources like images and audio files, and some of the MXML files have <fx:Script> tags with ActionScript snippets inside them. If that is the case, you will find yourself at home working with Apache Royale. The big difference is not so much the code you use, but the output and what it needs to run properly.

It is not yet possible to just import an existing Flex application into Apache Royale and then produce output in JavaScript that will run almost anywhere. However, you may need to do less hands-on conversion than you think to get to where you can produce your application, transpiled to JavaScript, through Royale.

ActionScript syntax is the same for Royale as it was in Flex. Functions, loops, classes, and properties will work as they worked before.
Your "business logic", which you built all or mainly in ActionScript, probably does not need to change. 
Components and their functions that do not rely on Apache Flex or Adobe Flash features will probably work with minor tweaks.

Where the changes need to happen is in the MXML files. You built your user interface using Spark and MX components--containers, controls, and so on. All those components will need to migrate to their Royale equivalents. You will find some differences between the components you used and the ones you now have available, and not all Flex components have equivalents in Royale yet.

One big change you will notice right away is that the default Royale UI components come with a basic set of functions, but not with the full range of behaviors that was loaded into every single Flex UI component whether it needed it or not. To get exactly the behavior your application needs from a data display or an input field, you may need to add "beads" to the basic Royale component. For example, to provide a field where the user can enter a password, you need to take the basic Royale *TextInput* component and add a [bead](Welcome/Features/Strands%20and%20Beads.html) like *PasswordInputBead* to it. This makes your Royale application much more lightweight than its Flex ancestor was, and learning about Strands and Beads is not too hard.

*link to Development tools page goes here...*
