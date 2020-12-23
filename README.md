Contact App Template Made with React

Features individual Card Components
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

Card List Component to populate Cards with contacts from database. At the moment it is currently using a predisposed list of names
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


 
