Contact App Template Made with React

---Features individual Card Components:
```javascript
const Card = ({ name, email, id }) => {
    return (
        <div className='tc bg-light-green dib br3 pa3 ma2 grow shadow-5'>
            <img alt='robo' src={`https://robohash.org/${id}?200x200`} />
            <div>
                <h2>{name}</h2>
                <p>{email}</p>
            </div>
        </div>
    );
}
```

---Card List Component to populate Cards with contacts from database. At the moment it is currently using a predisposed list of names:
```javascript
const CardList = ({ robots }) => {
    return (
    <div>
      {
        robots.map((user, i) => {
            return (
                <Card 
                  key={i} 
                  id={robots[i].id} 
                  name={robots[i].name} 
                  email={robots[i].email}
                />
            );
        })
      }
    </div>
    );
}
```

---Search Box for narrowing down contacts dynamically as letters are input(searches in no particular order. I.e. if you type 'A' any name with an 'A' will be present)
```javascript
const SearchBox = ({ searchfield, searchChange }) => {
    return (   
        <div className='pa2'>
            <input 
            className='pa3 ba ba--green bg-lightest-blue'
            type='search' 
            placeholder='Search Robots'
            onChange={searchChange}
            />
        </div>
    );
}
```

---Uses tachyons import for majority of CSS styling

---Uses a Robot image API that randomizes robot image

---Cards are inside scrollable box in middle of screen


Future Additions:

---Database connectivity

---User Registration & Authentication

---Customizable color schemes and fonts



 
