---
layout: project
type: project
image: img/melemanoa/melemanoa-square.png
title: "Mele Manoa"
date: 2023
published: true
labels:
  - Software Engineering
  - JavaScript
  - HTML/CSS
  - React Bootstrap
  - Meteor
  - Web Development
summary: "A web application for the musicians of UH"
---

[GitHub Page](https://mele-manoa.github.io/)


<figure class="figure float-end ps-4">
  <img width="500px" src="../img/melemanoa/melemanoa-body.png" class="figure-img img-fluid rounded border">
</figure>

Mele Manoa is a web application project I worked on for ICS 314, Software Engineering I. The web application was created to aid musicians of the University of Hawai'i to be able to easily find one another and meet up for jam sessions, find new members for bands, or just make new friends. 


I worked on this project with [Yeeun Shin](https://github.com/YeeunS), [Kendal Oya](https://github.com/kendalo-tech), and [Tevin Takata](https://github.com/tevin-takata) through a four-week period. I took on the role of project manager and UI designer. To speed up the process, we used the [meteor-application-template-react](https://github.com/ics-software-engineering/meteor-application-template-react) as the basis for our project. Using what we learned in ICS 314 as well, we used React Bootstrap to style and build our web application, MongoDB to hold our data, and Meteor to run the application. It was then deployed using Digital Ocean.


Mele Manoa included a profile page, a discover page, and a groups page. The Discover and Groups pages allow musicians to find other musicians or musical groups of similar interests and musical tastes. The pages display all users registered to Mele Manoa and a sidebar allows the user to filter through which instrument, genre, or skill level they are looking for in a fellow musician.


My favorite part about Mele Manoa is that sidebar in the Discover and Groups pages. Ignoring the few hours that took me to create the interface that I wanted, it was a fun and interesting learning experience. React Bootstrap features a preset list group, accordions, and toggleable buttons. I used all three to create the accordion sidebar, and used the `active` class from toggleable buttons to indicate each list item's state. Toggling the active state was also a problem of its own. Finally, after it was finished, Kendal hooked it up to the filtering system where it became fully functional.

```
<h4>Filter By</h4>
<ListGroup>
  <ListGroup.Item className="p-0">
    <Accordion defaultActiveKey="0" flush>
      <Accordion.Item eventKey="0">
        <Accordion.Header>Genres</Accordion.Header>
        <Accordion.Body className="p-0">
          <ListGroup id="genre-group" variant="flush">
            {genres.map((genre, key) => (
              <ListGroup.Item
                action
                key={key}
                className="active"
                onClick={() => { changeGenreState(key); }}
              >
                {genre}
              </ListGroup.Item>
            ))}
          </ListGroup>
        </Accordion.Body>
      </Accordion.Item>
      <Accordion.Item eventKey="1">
        <Accordion.Header>Skill Level</Accordion.Header>
        <Accordion.Body className="p-0">
          <ListGroup id="skill-group" variant="flush">
            {skill.map((level, key) => (
              <ListGroup.Item
                action
                key={key}
                className="active"
                onClick={() => { changeSkillState(key); }}
              >
                {level}
              </ListGroup.Item>
            ))}
          </ListGroup>
        </Accordion.Body>
      </Accordion.Item>
    </Accordion>
  </ListGroup.Item>
  <ListGroup.Item
    id="seeking-item"
    action
    className="active"
    onClick={() => { changeSeekingState(); }}
  >
    Seeking Band Member
  </ListGroup.Item>
</ListGroup>
```

Through this project, I have learned much about how to use React Bootstrap when developing web applications. The project also allowed me to utilize Github more and practice working with a team of people. Towards the end, I also experienced working on a time crunch, as homework and projects from other classes increased in difficulty. Fortunately, I had my team members to rely on to accomplish tasks I could not. One of the 'rules' that we agreed on was to let other teammates know when we had trouble with a task that we were assigned. Throughout development, no one was afraid to admit they were having trouble with the task they were working on. Personally, I believe this is an important quality to have within a development team or any team in general. Developing a web application, working with frameworks, and creating a product with a team have all been valuable experiences for me for the future.