

# Jukebox-TableViews

### Goals 

- Get even more familiar with Table View Controllers by making a customized one from its components.
- Use the `UITableView` delegate and datasource protocols to connect a table view to a view controller.

Let's take the first Jukebox-Views lab and use Table Views to provide a cleaner interface the user.    

## Instructions

A solution to the earlier Jukebox-Views lab is loaded into this lab upon startup. Use it (or your own solution) for reference when solving this new version. You'll need to switch the project's storyboard over from `OldLab.storyboard` to the standard `Main.storyboard` file. The data models for `FISSong` and `FISPlaylist` have been carried forward from the previous lab.

The new `Main.storyboard` file already contains a layout for you. The first `UITableViewController` meant for displaying the playlists embedded in a navigation controller. The new jukebox layout contains a few subviews including a tableview, but the class file will need to be set up as a subclass of `UIViewController` (**not** as a subclass of `UITableViewController`).

1. The first `FISPlaylistTableViewController` will display a list of playlists.  The title for each cell will display the name of the playlist (you'll have to add a name property to your Playlist object).  The subtitle will display the number of songs in the playlist.  

2. When clicking on a playlist, you'll show the new `FISJukeboxTableViewController` which has a tableview that will display the individual songs for the playlist that was tapped (one song in each cell). Make sure you set this view controller to conform to the `UITableViewDelegate` and `UITableViewDataSource` Protocols.  

3. All of the other functionality from the original jukebox should be translated into the new layout: 
	- Tapping a cell should play the song in that cell 
	- You should employ the services of a stop button to stop the current playing song. Can you reuse the same button that plays the track?
	- Use the `UISegmentedControl` in the navigation bar to sort the songs in the playlist and update the tableview's display.

4. You should also create an interface to show information about the current playing song. Be creative and if you have extra time, make it pretty. Use a `UIProgressView` to display the playback chronology of the current song.

### Extra Credit 

1. Create two modally presented view controllers, one which adds a new playlist to the list of playlists, and on which presents a lists all of the available songs and adds a selected song to the current playlist.  



