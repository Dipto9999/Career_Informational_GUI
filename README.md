# Career Informational GUI

## Contents

* [Overview](#Overview)
* [Pages](#Pages)
    * [Home Page](#Home-Page)
    * [Career Page](#Career-Page)
        * [Job Titles](#Job-Titles)
        * [Job Duties](#Job-Duties)
    * [Education Page](#Education-Page)
        * [Post-Secondary Programs](#Post-Secondary-Programs)
    * [References Page](#References-Page)
* [Implementation](#Implementation)
    * [Content Files](#Content-Files)
* [Credit](#Credit)

## Overview

Create <b>GUI</b> driven program in <b>UofT</b>'s <b>Turing</b> language to display career and educational information for web designers and developers (<b>NOC 2175</b>).</br>

The [(`main.t`)](main.t) <b>Turing</b> file must be run to launch the application.

## Pages

The application consists of a multi-page <b>GUI</b> with a navigation bar providing access to the main sections. Each section may expose additional sub-pages through contextual buttons.

The navigation bar contains the following buttons available on every page :

<ul>
    <li><b>Home</b></li>
    <li><b>Career</b></li>
    <li><b>Education</b></li>
    <li><b>References</b></li>
    <li><b>Quit Program</b></li>
</ul>

### Home Page

The home page greets the user with a title (<em>NOC 2175: Web designers and developers</em>) and a representative image.

### Career Page

The career page displays a general overview of the web designer and developer profession read from [`Career.txt`](Career.txt), distinguishing between the roles of a <b>Web Designer</b> and a <b>Web Developer</b>.

#### Job Titles

A contextual button on the career page navigates to the job titles sub-page, which lists common job titles for the field read from [`Job_Titles.txt`](Job_Titles.txt).

#### Job Duties

A contextual button on the job titles sub-page navigates further to the job duties sub-page, which outlines the typical responsibilities read from [`Job_Duties.txt`](Job_Duties.txt). From here, users can navigate to the market sub-page.

### Education Page

The education page presents three post-secondary programs relevant to the field. Contextual buttons navigate to each individual program detail page.

#### Post-Secondary Programs

<table>
  <tr>
    <th>Button Label</th>
    <th>Program</th>
    <th>Institution</th>
    <th>Content File</th>
  </tr>
  <tr>
    <td>Website Development: Strategy & Execution</td>
    <td>Website Development: Strategy & Execution</td>
    <td>University of Toronto</td>
    <td><a href="Education_1.txt"><code>Education_1.txt</code></a></td>
  </tr>
  <tr>
    <td>Web Design, Development and Maintenance</td>
    <td>Web Design, Development and Maintenance</td>
    <td>University of Toronto</td>
    <td><a href="Education_2.txt"><code>Education_2.txt</code></a></td>
  </tr>
  <tr>
    <td>Web Design - LCA.C0</td>
    <td>Web Design - LCA.C0</td>
    <td>University of Toronto</td>
    <td><a href="Education_3.txt"><code>Education_3.txt</code></a></td>
  </tr>
</table>

### References Page

The references page displays photo credits and works cited from [`Photo_Credit_And_Works_Cited.txt`](Photo_Credit_And_Works_Cited.txt). Additional pages of references are accessible through contextual <b>Page 2</b>, <b>Page 3</b>, <b>Page 4</b>, and <b>Page 5</b> buttons, reading from [`Works_Cited_1.txt`](Works_Cited_1.txt), [`Works_Cited_2.txt`](Works_Cited_2.txt), [`Works_Cited_3.txt`](Works_Cited_3.txt), and [`Works_Cited_4.txt`](Works_Cited_4.txt) respectively.

## Implementation

The program is implemented as a single <b>Turing</b> source file. All procedures are pre-declared using the `forward` keyword and defined as `body` procedures. Navigation is handled by creating and hiding <b>GUI</b> buttons based on the active page context, while the main event loop delegates control to the <b>GUI</b> framework via `GUI.ProcessEvent`.

<ul>
    <li>Window dimensions are fixed at <b>840 × 550</b> pixels with a gray background.</li>
    <li>A <b>Comic Sans 30pt</b> font is used for the home page title.</li>
    <li>A header image (<a href="website-designer.jpg"><code>website-designer.jpg</code></a>) is rendered on the home page.</li>
</ul>

### Content Files

All page content is stored in plain-text <b>.txt</b> files and read line-by-line at runtime.

<table>
  <tr>
    <th>File</th>
    <th>Page</th>
  </tr>
  <tr>
    <td><a href="Career.txt"><code>Career.txt</code></a></td>
    <td>Career</td>
  </tr>
  <tr>
    <td><a href="Job_Titles.txt"><code>Job_Titles.txt</code></a></td>
    <td>Job Titles</td>
  </tr>
  <tr>
    <td><a href="Job_Duties.txt"><code>Job_Duties.txt</code></a></td>
    <td>Job Duties</td>
  </tr>
  <tr>
    <td><a href="Market.txt"><code>Market.txt</code></a></td>
    <td>The Market</td>
  </tr>
  <tr>
    <td><a href="Requirements.txt"><code>Requirements.txt</code></a></td>
    <td>Requirements</td>
  </tr>
  <tr>
    <td><a href="Employers.txt"><code>Employers.txt</code></a></td>
    <td>Employers</td>
  </tr>
  <tr>
    <td><a href="Education_1.txt"><code>Education_1.txt</code></a></td>
    <td>Education – Program 1</td>
  </tr>
  <tr>
    <td><a href="Education_2.txt"><code>Education_2.txt</code></a></td>
    <td>Education – Program 2</td>
  </tr>
  <tr>
    <td><a href="Education_3.txt"><code>Education_3.txt</code></a></td>
    <td>Education – Program 3</td>
  </tr>
  <tr>
    <td><a href="Photo_Credit_And_Works_Cited.txt"><code>Photo_Credit_And_Works_Cited.txt</code></a></td>
    <td>References – Page 1</td>
  </tr>
  <tr>
    <td><a href="Works_Cited_1.txt"><code>Works_Cited_1.txt</code></a></td>
    <td>References – Page 2</td>
  </tr>
  <tr>
    <td><a href="Works_Cited_2.txt"><code>Works_Cited_2.txt</code></a></td>
    <td>References – Page 3</td>
  </tr>
  <tr>
    <td><a href="Works_Cited_3.txt"><code>Works_Cited_3.txt</code></a></td>
    <td>References – Page 4</td>
  </tr>
  <tr>
    <td><a href="Works_Cited_4.txt"><code>Works_Cited_4.txt</code></a></td>
    <td>References – Page 5</td>
  </tr>
</table>

## Credit

The following sources were consulted as reference for the career information presented in this program.

* [Government of Canada – Job Bank : Web designers and developers](https://www.jobbank.gc.ca/marketreport/summary-occupation/22523/ca)
* [University of Toronto School of Continuing Studies](https://learn.utoronto.ca/)
