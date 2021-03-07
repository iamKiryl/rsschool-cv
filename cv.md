# Kiryl Matusevich
***Logistics specialist / Junior front-end developer***

### Contact
- location: *Warsaw, Poland*
- tel: *+48 533 202 798*
- email: *iamkirylm@gmail.com*
- linkedin: *[Matusevich Kiryl](https://www.linkedin.com/in/matusevich-kiryl/)*

### Skills

- HTML5
- CSS3
- JavaScript
- RWD
- AJAX
- jQuery
- SCSS
- SASS
- Git
- Gulp
- Webpack
- React.js 
- Python (*basic*)
- C++ (*basic*)

### Profesional Experience

#### Beloil Polska
**Specialist of Sales Support Department** *(10/2018 - 07/2019)*
- Invoicing operations related to oil and gas products in SAP;
- Transferring purchase documents into SAP;
- Transferring logistics documents (e.g. truck and train aviso) into SAP
- Cooperation with refineries in Poland and Belarus;

#### Beloil Poslka
**Marketing Specialist** *(01/2016 - 10/2018)*
- Ordering train logistics;
- Cooperation with truck hauliers;
- Preparation of tenders for oil products;
- Updating the company website;
- Preparation of tenders for oil products;

#### OOO Beltopgroup 
**Sales Specialist** *(06/2015 - 10/2015)*
- Selling products in Belarus;
- Preparation of Sales and Technical Offers;
- Updating the company website;

#### ODO Belautozapchast

**Sales Specialist** *(10/2014 - 11/2014)*

- Selling car service parts in Belarus;
- Preparation of Sales and Technical Offers;

### Education

**WSB Universities** *(02/2020 - in progress)*

**Major:** *Informatics*<br/>
**Level:** *Engineer*

**Akademia Finansów i Biznesu Vistula** *(10/2014 - 11/2014)*

**Major:** *Management*<br/>
**Level:** *BA*

### Workshops, Courses, Certificates

**CSS Fundamentals course** *(2019)*

**HTML Fundamentals course** *(2019)*

**Akademia 108** *(2019)*

*Additional Information: HTML5, CSS3, JavaScript, ReactJS, jQuery, RWD, Bootstrap,
AJAX, GIT, WordPress*

- 1 month work on preworks
- 2 months of practical workshops
- 3 months of distant work within the frameworks of the Academy 108 Course

### Languages

**EN:** *Intermediate*<br/>
**PL:** *Advanced*<br/>
**RU:** *Native*

### My code:

``` 
	function timer() {

    const deadline = '2021-03-23'; /*some date*/

    function getTimeRemaining(endtime) {
        const t = Date.parse(endtime) - Date.parse(new Date()),
            days = Math.floor( (t/(1000*60*60*24)) ),
            seconds = Math.floor( (t/1000) % 60 ),
            minutes = Math.floor( (t/1000/60) % 60 ),
            hours = Math.floor( (t/(1000*60*60) % 24) );

        return {
            'total': t,
            'days': days,
            'hours': hours,
            'minutes': minutes,
            'seconds': seconds
        };
    }

    function getZero(num){
        if (num >= 0 && num < 10) { 
            return '0' + num;
        } else {
            return num;
        }
    }

    function setClock(selector, endtime) {

        const timer = document.querySelector(selector),
            days = timer.querySelector("#days"),
            hours = timer.querySelector('#hours'),
            minutes = timer.querySelector('#minutes'),
            seconds = timer.querySelector('#seconds'),
            timeInterval = setInterval(updateClock, 1000);

        updateClock();

        function updateClock() {
            const t = getTimeRemaining(endtime);

            days.innerHTML = getZero(t.days);
            hours.innerHTML = getZero(t.hours);
            minutes.innerHTML = getZero(t.minutes);
            seconds.innerHTML = getZero(t.seconds);

            if (t.total <= 0) {
                clearInterval(timeInterval);
            }
        }
    }

    setClock('.timer', deadline);
}

module.exports = timer;
```
