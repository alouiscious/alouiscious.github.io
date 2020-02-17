---
layout: post
title:      "Rails Projection"
date:       2020-02-17 07:08:53 -0500
permalink:  rails_projection
---


Well I finally feel more like writing a blog to demonstrate a project than ever before.
There are many moving parts to put this together.
One of the best discoveries is the real world modelled in an app is tricky!
But as with any model thesis, relationships and associtaions iron out the bumps of this real world to the point of finding out just how many details you could use to code yourself into a unending set of functional layers.

here are just some of the parts, and i was releived to have a true practice of writning about the projects for several days before writing a single once of code.

I wrote about it and read about it, and read about it again.
Until finally i could call evey method and helper by memory.

then i hit a serious block. a writers block - of sorts.
questioning everything, but especially losing track of where in the MVC of things would i beging to line in this code. where did it belong? while one class had to wait for another class to be written, another had to be written blindly to gain structure and understanding.

Song Design App

When a Song is created (song_id)
Has a user
title:string
genre:string
key:string
status:boolean active/dormant
instruments X7:string
can select or create instrument
Can be blank
musician.songnotes
auto-adds any
rehearsal assignment X2
can select or create rehearsal
rehearsal.songnotes
auto_adds any
cannot be blank

When a user is created (musician_id)
It belongs to a rehearsal
name:string
email:email
city:string
instrument:string
musician_note:note


When a rehearsal is created
It belongs to a user and a 
name:string
date:datetime
location:string

song:string X20
Can select or create song
Can add or create note for song notes
Can view existing notes
Can be blank
musician:string X7
Can select or create musician
Can add or create note for musician notes
Can view existing notes

Song_Notes
title:string
content:string
type:string
rehearsal, musician, song
belongs_to song

Some features are not even part of this project "assignment's scope".
Although they were not part of todays code, they still became a consideration regarding naming and scope and references.

Then there was time to think about the user. The inception of the project's app serves a purpose and has a result that makes other's work a little easier. However, writing feature just for the purpose was quickly managed by writing for the user and scalable intuitivity.

None the less, it is a good app and has been received well by my peers and mentors.
So here is it's introduction to you...

Introducing, Song Design.
The rehearsal creation app for the band leader or manager.
This app quickly brings together the information one needs to know to make the rehearsal.
It's goal is to assist with not repeating song perfomance instructions, to empower the performing musician to own their material, and keep track of the latest song design changes. 






