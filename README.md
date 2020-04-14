## Museum of Candy
 Museum of Candy project using Bootstrap 4

# Full Coding Script
*   Intro
    - Goal is to create a responsive design
    - Some components disappear in certain sizes
    - Stacking changes with different screen sizes
    - Navbar font-size - CSS supposed to be there at 13:17
    - Google Font Nunito, Custom CSS and general Bootstrap
*   Navbar
    - In app.css, add bg #f5d9d5
    - nav.navbar.navbar-dark and maybe.bg-dark to start
    - .navbar-expand-md and #mainNavbar
    - For brand a.navbar-brand - "Candy"
    - button.navbar-toggler, data-toggle = "collapse", data-target="" for now
    - button > span.navbar-toggler-icon
    - .collapse.navbar-collapse#navLinks
    - Data-target becomes #navLinks
    - navLinks > ul.navbar-nav > li.nav-item > a.nav-link, and replicate lis and change inner HTML
    - Inner HTML - Home, About and Tickets (all caps)
    - For Navbar button, need to be more accessible aria-label = "Toggle navigation"
    - In css file, change the font for the body - font-family: "Nunito", sans-serif;
    - #mainNavbar .navbar-brand - color: #ea1c2c; font-size to 1.5rem, font-weight: 100
    - Extend font-size and font-weight to the #mainNavbar
    - #mainNav.nav-link- color: white; on hover, it's #ea1c3c
    - Remove padding on top-botton with py-0 utility on main nav
    - Need to make it stay on top - Test out with some content
    - Set the main nav with class fixed-top. TODO: Need to handle the overlap piece
*   Top Section - Headings and image
    - After the nav, add section.container-fluid > .row > .col-6 > h2 for Museum of Candy (add a second col-6)
    - In second col-6, add img with hand2 PNG and add .img-fluid
    - Note that container-fluid has padding, so need to do px-0
    - For the row, align-items-center and in h2, .text-center
    - For cols, need to be 6 at lg (col-lg-6)
    - Duplicate Museum of Candy a few times and wrap them in div.text-white.text-center.d-none.d-lg-block (remove text-center from earlier blocks)
    - Start with one title for font size and slashes
    - Need span for each slash and select them in css (for div wrapping the h2s, add #headingGroup span - color: #EA1c2c)
    - For h2s, can add .display-2, however, can change them to h1s
    - In css, select heading group ID and change h1 font-weight to 100, font-size to 4rem and duplicate 7
    - In div wrapping the h1s, add mt-5 and need to shrink it down with a media query
    - @media (max-width: 1200px) {
        body{
            background-color: orange (for testing only!!)
        }
    }
    - Instead of body, select h1s in the heading group and change the font-size to 3rem
*   Bottom Sections
    - section.container-fluid.px-0 > .row > .col-md-6 (x2)
    - In first, add a img.img-fluid for milk, and in 2nd nest a row with col-8 and then col-10, but later
    - For now in 2nd, h2 - Title; img - lolli; p.lead with lorem40
    - In 2nd col-md-6, .text-center
    - In row, .align-items-center. Now to create spacing for the text!
    - In 2nd col-md-6, .row > .col-10 to start with the title, image and p.lead
    - To center horizontally  - in nested row, .justify-content-center
    - Nested .col-10 can also become .col-8-lg for breakpoint
    - In image of lolli, .d-none and the to make it appear on lg, .d-lg-inline
    - For ordering, in the cols, order-2, order-1. Then order-md-1, order-md-2
    - In app.css, select h2s and give the same c2c red color, font weight to 100, font size to 2.5rem
    - For image texts, give .blurb to col containing title, image and text
    - Select the .blurb p and give color #f498b8, font weight to 100, font size to 1.125, line-height is 2.0
    - Duplicate 1st order rows and give each .content with margin-top of 100px (note that it will need to be reversed)
*   Wrapping up
    - In second row, get rid of order and move the image after the text row and remove the ordering from both the text and image
    - Duplicate the first row and move it to the bottom
    - Change the images on both!
    - On the xs size, for the blurbs, add a mb-5 and mb-md-0 and copy to each of the others
    - For making the navbar cooler, define a CSS class which activates when you scroll
    - Before media queries, .navbar.scrolled - background - 222, 192, 222 RGB
    - After bootstrap scripts, add a new script:
        $(function() {
            $(document).scroll(function() {
                var $nav = $("#mainNavbar");
                $nav.toggleClass("scrolled", $(this).scrollTop() > $nav.height());
            })
        });
    - For animation, in .scrolled - transition: background 200ms;
    - Can add margin-bottom: 100px for the .content
    - Donut, milk, gumball and other for image order
