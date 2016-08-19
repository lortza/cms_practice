== README

CMS App

Here is the outline for a simple CMS app we can build for fun/learning. I don't expect this to be beautiful or portfolio-worthy. It's just for learning. However, you can always fork it and turn it into something fancy.

Overview:
This app will be a simple CMS where a user can create posts, pages, and events. All posts, pages, and events can be seen by the public, but it will require sign-in to add/edit/delete them -- a very simple admin user situation.

=== App Info:
* Ruby 2.2.1
* Rails 4.2.3
* Postgres
* Github repo: {https://github.com/lortza/cms_practice}[https://github.com/lortza/cms_practice]

=== Design Assets:
* {Twitter bootstrap cdn}[http://getbootstrap.com/getting-started/]
* {Google fonts}[https://fonts.google.com/?authuser=1]
* {fontawesome icons}[http://fontawesome.io/get-started/]
* {ipsum}[http://www.dummytextgenerator.com/]

=== Database:

Resource :: User :: Post :: Page :: Event
fields :: 1::2::3::4


<table width="100%" border="0" cellspacing="0" cellpadding="10">
  <tr>
    <th scope="col">Resource</th>
    <th scope="col">User</th>
    <th scope="col">Post</th>
    <th scope="col">Page</th>
    <th scope="col">Event</th>
  </tr>
  <tr>
    <td valign="top">fields</td>
    <td valign="top"><ul>
      <li>email (string) </li>
      <li>username (string)</li>
      <li> password (digest)</li>
    </ul>    </td>
    <td valign="top"><ul>
      <li>headline (string)</li>
      <li>content (text)</li>
      <li>      is_published (boolean, default false)</li>
    </ul>    </td>
    <td valign="top"><ul>
      <li>name (string)</li>
      <li>content (text)</li>
      <li>      is_published (boolean, default false)</li>
    </ul>    </td>
    <td valign="top"><ul>
      <li>name (string)</li>
      <li>starts_at (datetime)</li>
      <li>ends_at (datetime)</li>
      <li>description (text)</li>
      <li>location (string)</li>
      <li>price (decimal)</li>
      <li>        is_published (boolean, default false)</li>
    </ul>    </td>
  </tr>
  <tr>
    <td valign="top">views and scopes</td>
    <td valign="top">index (private)<br/>
      add/edit/form (private)<br/>
    show (private)</span></td>
    <td valign="top">index (private)<br/>
      add/edit/form (private)<br/>
      show (public)<br/>
    blog (public)</span></td>
    <td valign="top">index (private)<br/>
      add/edit/form (private)<br/>
    show (public)</span></td>
    <td valign="top">index (private)<br/>
      add/edit/form (private)<br/>
      show (public)<br/>
    list (public)</span></td>
  </tr>
  <tr>
    <td valign="top">content</td>
    <td valign="top">>Let&#39;s create a user called &quot;admin&quot;</td>
    <td valign="top">Create 3 posts</td>
    <td valign="top">Home<br/>
      About<br/>
    Contact</td>
    <td valign="top">Create 1 past event and 2 future events</td>
  </tr>
  <tr>
    <td valign="top">misc</td>
    <td valign="top">we'll need to create sessions for signin/out</td>
    <td valign="top">&nbsp;</td>
    <td valign="top">&nbsp;</td>
    <td valign="top">&nbsp;</td>
  </tr>
</table>


Post
Page
Event
fields
email (string)
username (string)
password (digest)
headline (string)
content (text)
is_published (boolean, default false)
name (string)
content (text)
is_published (boolean, default false)




name (string)
starts_at (datetime)
ends_at (datetime)
description (text)
location (string)
price (decimal)
is_published (boolean, default false)



views & scopes
index (private)
add/edit/form (private)
show (private)


index (private)
add/edit/form (private)
show (public)
blog (public)


index (private)
add/edit/form (private)
show (public)
index (private)
add/edit/form (private)
show (public)
list (public)
Misc stuff
We'll need sessions for sign in/out






Content
Let's create a user called "admin"
Create 3 posts
Home
About
Contact
Create 1 past event and 2 future events


Getting Started
I'm assuming you have postgres installed on your machine. I've created the base app (it's totally empty) and pushed it to {github here}[https://github.com/lortza/cms_practice]. After you clone it locally, here's how to set it up:

1. fire up postgres
2. ```cd cms_practice```
3. ```bundle```
4. ```rake db:create```
5. fire up the ```rails s```
6. navigate to http://localhost:3000/

