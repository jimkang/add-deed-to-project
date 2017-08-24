add-deed-to-project
==================

Given a deed object with a projectName, find that project in a collection, then add that deed to the project's `deeds` array.

Installation
------------

    npm install add-deed-to-project

Usage
-----

    var addDeedToProject = require('add-deed-to-project');
    var projectsByName = {
      project1: {},
      project2: {
        deeds: [
          {
            id: 'asdf',
            message: 'Got this started.',
            projectName: 'project2'
          }
        ]
      }
    };
    addDeedToProject(
      logError,
      projectsByName,
      {id: 'qwer', message: 'Update!', projectName: 'project2'}
    );

Resulting `projectsByName` collection:

    {
        project1: {},
        project2: {
          deeds: [
            {
              id: 'asdf',
              message: 'Got this started.',
              projectName: 'project2'
            },
            {
                id: 'qwer',
                message: 'Update!',
                projectName: 'project2'
              }
          ]
        }
      }

License
-------

The MIT License (MIT)

Copyright (c) 2017 Jim Kang

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.