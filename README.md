# Dribbbble

## Filters with State

### Big Picture

You are the only React developer in the work (what a coincidence), and you have a mentor Mr. R. You’ve been learning React with him and so far you now understand how to create React components, how to pass data between components using ` props` and how to manage the state.

Mr. R has a cold, and he can’t work today. So, you have to cover your friend.

### The Assignment

Using `create-react-app` npm package, create a project and add the below code using modules (`files`).<br/>
You will need to create 4 components (one per file): `App`, `Container`, `Shots` and `Shot`. And a `data` file.

The markup code for each component:

#### `App.js`
```js
class App extends React.Component {
  render() {
    return (
      <div>
        <Container />
      </div>
    );
  }
}
```

#### `Container.js`
```js
class Container extends React.Component {
  render() {
    return (
      <header>
        <nav className='nav'>
          <ul className='nav__list'>
            <li>
              <a href='#'>All</a>
            </li>
            <li>
              <a href='#'>Popular</a>
            </li>
            <li>
              <a href='#'>Recent</a>
            </li>
            <li>
              <a href='#'>Debuts</a>
            </li>
          </ul>
        </nav>
        <Shots />
      </header>
    );
  }
}
```

#### `Shots.js`
```js
class Shots extends React.Component {  
  render() {
    return (
      <section>
        <div className='container'>
          <div className='shots'>
            return <Shot />
          </div>
        </div>
      </section>
    );
  }
}
```

#### `Shot.js`
```js
class Shot extends React.Component {
  render() {
    return (
      <article>
        <div>
          <div className='shot'>
            <picture>
              <img src='https://cdn.dribbble.com/users/23795/screenshots/2241261/open-uri20150912-3-14makg2_1x' />
            </picture>
            <section>
              <ul className='stats'>
                <li>
                  <i className='fa fa-eye'></i> 28,328
                </li>
                <li>
                  <i className='fa fa-comment'></i> 10
                </li>
                <li>
                  <i className='fa fa-heart'></i> 862
                </li>
              </ul>
            </section>
          </div>
          <footer className='author'>
            <a href='#'>
              <picture>
                <img src='https://cdn.dribbble.com/users/519846/avatars/mini/8010008dd2de026ecb0f23a48226b5f5.png?1413748190' />
              </picture>
              <span>Musixmatch</span>
            </a>
          </footer>
        </div>
      </article>
    );
  }
}
```

#### CSS, styles
```css
*,
*::before,
*::after {
  box-sizing: border-box;
}

body {
  font-family: 'Roboto';
  background-color: #F4F4F4;
}

.nav {
  color: #999;
  font-size: 14px;
  border-bottom: 1px solid #E5E5E5;
  background-color: white;
}

.nav__list {
  display: flex;
  height: 50px;
  justify-content: center;
  align-items: center;
  list-style-type: none;
  padding: 0;
  margin: 0;
}

.nav__list li {
  margin: 0 10px;
}

.shots {
  margin-top: 25px;
  font-size: 14px;
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
}

.shot {
  width: 220px;
  padding: 10px;
  background-color: white;
  box-shadow: 0 1px 2px rgba(0, 0, 0, 0.07);
}

.shot img {
  width: 100%;
  height: 150px;
}

.stats {
  color: #AAA;
  font-size: 12px;
  list-style-type: none;
  padding: 0;
  margin: 0;
  display: flex;
  justify-content: flex-end;
}

.stats li {
  margin: 0 5px;
}

.author {
  color: #3a8bbb;
  font-weight: bold;
  padding: 10px 0;
}

.author img {
  width: 16px;
  height: 16px;
  border-radius: 16px;
  margin-right: 5px;
}

.container {
  width: 85%;
  margin: 0 auto;
}

a {
  text-decoration: none;
  color: inherit;
}

article {
  margin: 10px;
}

.selected {
  font-weight: bold;
  color: #444;
}

```

#### `data object`
```js
const data = [{
  key: 1,
  img: 'https://cdn.dribbble.com/users/23795/screenshots/2241261/open-uri20150912-3-14makg2_1x',
  stats: ['28,328', '10', '862'],
  author: {
    avatar: 'https://cdn.dribbble.com/users/519846/avatars/mini/8010008dd2de026ecb0f23a48226b5f5.png?1413748190',
    name: 'Musixmatch'
  },
  section: 'popular'
}, {
  key: 2,
  img: 'https://cdn.dribbble.com/users/207046/screenshots/1891233/discover_page_achoo_1x.png',
  stats: ['64,670', '15', '918'],
  author: {
    avatar: 'https://cdn.dribbble.com/users/207046/avatars/mini/d217b2a65dfa773771d1dae3139e06c1.png?1468930348',
    name: 'Balkan Brothers'
  },
  section: 'popular'
}, {
  key: 3,
  img: 'https://cdn.dribbble.com/users/692322/screenshots/3233887/overall-assets-dribbble-shot_1x.png',
  stats: ['37,213', '29', '684'],
  author: {
    avatar: 'https://cdn.dribbble.com/users/692322/avatars/mini/64cb1e3181907a25d69d09f1733f9679.jpg?1499508866',
    name: 'Divan Raj'
  },
  section: 'popular'
}, {
  key: 4,
  img: 'https://cdn.dribbble.com/users/692322/screenshots/3539286/mockup_copy_10_1x.png',
  stats: ['22,775', '33', '585'],
  author: {
    avatar: 'https://cdn.dribbble.com/users/692322/avatars/mini/64cb1e3181907a25d69d09f1733f9679.jpg?1499508866',
    name: 'Divan Raj'
  },
  section: 'popular'
}, {
  key: 5,
  img: 'https://cdn.dribbble.com/users/3816/screenshots/491138/____filters.png',
  stats: ['39,873', '34', '820'],
  author: {
    avatar: 'https://cdn.dribbble.com/users/559317/avatars/mini/rally_logo.png?1398641637',
    name: 'RALLY'
  },
  section: 'popular'
}, {
  key: 6,
  img: 'https://cdn.dribbble.com/users/412187/screenshots/3399291/dreamteam_1x.png',
  stats: ['22,003', '13', '606'],
  author: {
    avatar: 'https://cdn.dribbble.com/users/417228/avatars/mini/d00a5c1ac8265665dd54798a369e2e5d.png?1498286645',
    name: 'El Passion'
  },
  section: 'popular'
}, {
  key: 7,
  img: 'https://cdn.dribbble.com/users/2/screenshots/1460708/d2_1x.gif',
  stats: ['45,442', '43', '539'],
  author: {
    avatar: 'https://cdn.dribbble.com/users/39/avatars/mini/apple-flat-precomposed.png?1388523974',
    name: 'Dribbble'
  },
  section: 'popular'
}, {
  key: 8,
  img: 'https://cdn.dribbble.com/users/18730/screenshots/2356638/filters_new_1x.gif',
  stats: ['37,504', '14', '544'],
  author: {
    avatar: 'https://cdn.dribbble.com/users/104120/avatars/mini/5b424431efdceb03c6615b4db63445ed.png?1410310131',
    name: 'Handsome'
  },
  section: 'popular'
}, {
  key: 9,
  img: 'https://cdn.dribbble.com/users/411234/screenshots/4335041/dribbble-appointments2_1x.png',
  stats: ['165', '0', '18'],
  author: {
    avatar: 'https://cdn.dribbble.com/users/1888322/avatars/mini/87015ecbabfa678bdc90b1af81bf9c9f.png?1504552198',
    name: 'December Labs'
  },
  section: 'recent'
}, {
  key: 10,
  img: 'https://cdn.dribbble.com/users/67420/screenshots/4334413/table_gif1_1x.gif',
  stats: ['2,556', '0', '122'],
  author: {
    avatar: 'https://cdn.dribbble.com/users/598388/avatars/mini/c924c09762c62328de9f303ea705f0b9.png?1486660647',
    name: 'Oscar Health'
  },
  section: 'recent'
}, {
  key: 11,
  img: 'https://cdn.dribbble.com/users/411234/screenshots/4333620/dribbble-appointments_1x.png',
  stats: ['364', '0', '26'],
  author: {
    avatar: 'https://cdn.dribbble.com/users/1888322/avatars/mini/87015ecbabfa678bdc90b1af81bf9c9f.png?1504552198',
    name: 'December Labs'
  },
  section: 'recent'
}, {
  key: 12,
  img: 'https://cdn.dribbble.com/users/329836/screenshots/4319612/rba_phonecomps_1x.jpg',
  stats: ['167', '0', '14'],
  author: {
    avatar: 'https://cdn.dribbble.com/users/329836/avatars/mini/24d59405b12a1de9bd709f855788e48c.jpg?1518836727',
    name: 'Wattle & Daub'
  },
  section: 'recent'
}, {
  key: 13,
  img: 'https://cdn.dribbble.com/users/467044/screenshots/4310495/unit_details_1x.gif',
  stats: ['3,398', '4', '161'],
  author: {
    avatar: 'https://cdn.dribbble.com/users/467044/avatars/mini/7a40b944ae0be45e1f942258f56ac94b.jpg?1431106862',
    name: 'Yaroslav Zubko'
  },
  section: 'recent'
}, {
  key: 14,
  img: 'https://cdn.dribbble.com/users/467044/screenshots/4293522/uptop-filetrs_1x.gif',
  stats: ['6,508', '9', '273'],
  author: {
    avatar: 'https://cdn.dribbble.com/users/1946520/avatars/mini/9bc3447e7b146f321a3203f947d48d07.png?1508755865',
    name: 'Space~'
  },
  section: 'recent'
}, {
  key: 15,
  img: 'https://cdn.dribbble.com/users/52084/screenshots/4341505/cabin_design_1x.jpg',
  stats: ['4,365', '7', '556'],
  author: {
    avatar: 'https://cdn.dribbble.com/users/52084/avatars/mini/692992651656234d8bddb5823a090f98.jpg?1510596786',
    name: 'Steve Wolf'
  },
  section: 'debut'
}, {
  key: 16,
  img: 'https://cdn.dribbble.com/users/121405/screenshots/4331028/67_1x.png',
  stats: ['4,592', '14', '424'],
  author: {
    avatar: 'https://cdn.dribbble.com/users/707705/avatars/mini/2eb345c8eb7ff9672893dabc929c958c.png?1421237411',
    name: 'DuckDuckGo'
  },
  section: 'debut'
}, {
  key: 17,
  img: 'https://cdn.dribbble.com/users/46302/screenshots/4345319/too_1x.png',
  stats: ['3,680', '21', '354'],
  author: {
    avatar: 'https://cdn.dribbble.com/users/135634/avatars/mini/2278a1c672a9ed37f91ee6df158ec94e.png?1500409122',
    name: 'Norde'
  },
  section: 'debut'
}, {
  key: 18,
  img: 'https://cdn.dribbble.com/users/696837/screenshots/4343976/discared-bs_1x.png',
  stats: ['4,040', '7', '286'],
  author: {
    avatar: 'https://cdn.dribbble.com/users/414899/avatars/mini/8bd3ab4983c97f8f2b3a3d10a50fded6.png?1516738162',
    name: 'Focus Lab'
  },
  section: 'debut'
}, {
  key: 19,
  img: 'https://cdn.dribbble.com/users/56953/screenshots/4341020/intercom_pins_1x.jpg',
  stats: ['3,383', '12', '283'],
  author: {
    avatar: 'https://cdn.dribbble.com/users/463835/avatars/mini/1ad327f8642e7ac27d522436379615cd.jpg?1517200761',
    name: 'Hoodzpah'
  },
  section: 'debut'
}, {
  key: 20,
  img: 'https://cdn.dribbble.com/users/37385/screenshots/4339898/nloma_1x.jpg',
  stats: ['1,790', '9', '159'],
  author: {
    avatar: 'https://cdn.dribbble.com/users/37385/avatars/mini/4558725b673d62aa93badd9b976fda10.jpg?1482348855',
    name: 'Andrew Littman'
  },
  section: 'debut'
}, {
  key: 21,
  img: 'https://cdn.dribbble.com/users/60266/screenshots/4344697/gobragh_logo_shot_1x.jpg',
  stats: ['1,233', '1', '138'],
  author: {
    avatar: 'https://cdn.dribbble.com/users/60266/avatars/mini/c016783a9d4560a66b6c851c0b846f34.png?1479912139',
    name: 'Gustavo Zambelli'
  },
  section: 'debut'
}];
```

### Explorer Mode

Add the functionality to **Filters** section, and show the relative information with each option. Put attention in `data` object, there is a property called `section`, you may use that one to filter the data.

### Deliverables

A GitHub link repo with the solution.
