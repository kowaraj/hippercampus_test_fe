For the test (React) Express (backend), see: https://github.com/kowaraj/hippercampus_test_be

# Test React client (frontend) for Express API

## Create

```
npx create-react-app hippercampus_test_fe
cd hippercampus_test_fe
npm start
```

## Add to fetch

```
constructor(props) {
    super(props);
    this.state = { apiResponse: "" };
}

callAPI() {
    fetch("http://localhost:9000/testAPI")
        .then(res => res.text())
        .then(res => this.setState({ apiResponse: res }));
}

componentWillMount() {
    this.callAPI();
}
```

## Observe the CORS problem!