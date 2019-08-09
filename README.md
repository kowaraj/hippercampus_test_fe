# Test React client for Express API

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