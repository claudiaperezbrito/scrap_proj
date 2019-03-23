# scrap_proj
### ReadMe

This is the files for a Adv. Web Apps scraping project where I scraped Alachua jail inmate list.
  http://oldweb.circuit8.org/inmatelist.php
  
 The purpose of this project is to practice scraping with Beautiful Soup and Selenium (if it was necessary) 
 as well as scrape content that would be useful for journalists in a newsroom.
 
 The content I scraped was:
      >>> In bookings.csv: the inmate name, booking date, mni, pod, mugshot link, inmate detail link.
      >>> In charges.csv: the inmates charges, statute, description of the statute, level, degree.
 
 
 ## The Process:
  
  1. First I had to scrape the table of inmates that contained their mni, booking date, etc.
    In order to do that I created a for loop and made variables for each of the values.
    I also had to grab the hrefs from the inmate's name and mugshot to make into column for when I would write into my csv.
    
  2. I had to grab the inmate's booking number (which was after the = in the inmate's url) and add it into a empty list.
  This would work to later coordinate the inmate bookings with charges.
  
  3.  I had to create another for loop to iterate inside each of the inmate's detail urls to scrape the charges they had.
  
  
  ##Problems Encountered:
  
  1. The html had no classes or ids, so I had to deal with scraping the table by specifiying which 'td' I needed.
  
  2. During the scraping chrome crashed repeatedly, and I realized I had to take the driver outside of the for 
  loop or everytime it iterated through the pages it would open a new browser window.
