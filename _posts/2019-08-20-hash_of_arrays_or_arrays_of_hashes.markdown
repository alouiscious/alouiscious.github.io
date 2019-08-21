---
layout: post
title:      "Hash of arrays or arrays of hashes"
date:       2019-08-21 02:30:55 +0000
permalink:  hash_of_arrays_or_arrays_of_hashes
---

labs are completing a bit faster, but i am referring to many resources all at once and have developed several go tos.

I can credit my most recent success to dotnetperls.com and ruby.org and AAQ.
below is a trascript of sorts from a recent AAQ

I have discovered ways to refactor code and plan for truthyness even better than before or else nil.

also, 

  def self.all
    @@all
  end

  def save
    self.class.all << self
  end

  def self.create
    song = self.new
    #@@all << song
    song
  end
  
  def self.new_by_name(name)
    song = self.new 
    song.name = name
    song
  end
	
Wicked stuck on what happend to initialize. then switched to tictactoe and because i'm no longer managing a library, initialize is set to a recurring empty array.

However, even though I'm stuck from time to time, I'm really glad to see green when i do. I'm happy green is getting easier.

	

on August 14
So I'm still stuck on filling the results I want to return to the terminal.

I worked with Issac...

Super patient. Very lead learn and made sure I owned the solution. 
The lab design gave me a chance to repeat the solution and lock down the lesson.



Hi Renee! How are you today?

I learned to understand the volumes or instance / class variables and their contents.
Using pry to test results is getting easier.

Also my typing is getting faster. Although, I still have to compensate for being so used to an ios tough key board.

I am investigating a UK map API with my pair partner. Jenny.
I thought about a list of the Blues and Jazz clubs and performance centers using a UK map.

We've started the first of four final labs.

I'm curoius about building an flatiron app that sorts cohort members by region of the time zone in which they reside.
Splits them across a chort teaching group. and arranges a pod meeting time based on closely located member and the closest teacher.


I"m still interested in creating ideas for teaching the skills im learning.

I'm wondering what my software specialty will be. I've always wanted to design music effect apps.

Here is a reminder of a AAQ session work flow.
Renee Sims 
[1] pry(Song)> !@@genre_count[genres].eql? genres
=> true
[2] pry(Song)> @@genre_count[genres] = genres
=> "rap"
[3] pry(Song)> @@genre_count[:genres] << 1
NoMethodError: undefined method `<<' for nil:NilClass
from (pry):3:in `block in genre_count'
[4] pry(Song)> @@genre_count[genres] << 1
=> "rap\u0001"
[5] pry(Song)> @@genre_count
=> {"rap"=>"rap\u0001"}
[6] pry(Song)> @@genre_count[genres] += 1
NoMethodError: undefined method `+' for nil:NilClass
from (pry):6:in `block in genre_count'
[7] pry(Song)>



Renee Sims 
this is my pry attempt.


Isaac Villicana
Hi Renee!

Isaac Villicana
can you run learn save so i can check your code?

require 'pry'

class Song
  
  attr_accessor :name, :artist, :genre
  
  @@count = 0
  @@genre_count = {}
  @@genres = []
  @@artists = []
  
  
  def initialize(name, artist, genre)
    @genre = genre
    @artist = artist
    @name = name
    @@count += 1
    @@genres << genre
    @@artists << artist
  end
  

  
  def genres
    @@genres.uniq!
  end
  
  def artists
    @@artists.uniq!
  end
  
  def self.count
    @@count
  end  
  
  def self.artists
    @@artists.uniq!
  end
  
  def self.genres
    @@genres.uniq!
  end
    
  
  def self.genre_count
    @@genres.each do |genres| 
# binding.pry      
      if !@@genre_count[genres] 
        @@genre_count[genres] = 1
      else
        @@genre_count[genres] += 1 
      end
    end
        @@genre_count

  end
  
  def self.artist_count
    
    @@artists.each do |artists|
      if !@@artist_count[artists]
        @@artist_count[artists] = 1 
      else 
        @@artist_count[artists] += 1 
      end
    end
    
    @@artist_count
  end
    
    
end

