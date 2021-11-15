# Use inside 90POE

1. Generate proper access url for given channel [stream-tools](https://github.com/90poe/chat-monorepo/tree/master/stream-tools)

```bash
cd stream-tools
make build
ENV=local ./stream-tools token CHANNELID

d0170f81-78ff-4ef2-a5e6-6075487cbed: http://localhost:3000/?apikey=m7dwyc5hqjwf&user=d0170f81-78ff-4ef2-a5e6-6075487cbed3&user_token=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpYXQiOjE2MzY5NzYzNjAsInVzZXJfaWQiOiJkMDE3MGY4MS03OGZmLTRlZjItYTVlNi02MDc1NDg3Y2JlZDMifQ.CzS2EhQ-qvcp3blstRezyOTy-itRNpXufxpl-aflGLg&channelId=CHANNELID
```

2. Prepare UI for testing (development release)

```bash
cd team/
# check the filter(s) in `src/App.js:39`, defaults to `OnRadar` type
# use yarn or npm - both shall work
yarn && yarn start
# close http://localhost:3000 and open a generated URL above
```

# website-react-examples

## Apps

- [customer-support](https://getstream.github.io/website-react-examples/customer-support/)
- [social-messenger](https://getstream.github.io/website-react-examples/social-messenger/)
- [gaming-livestream](https://getstream.github.io/website-react-examples/gaming-livestream/)
- [team](https://getstream.github.io/website-react-examples/team/)
- [virtual-event](https://getstream.github.io/website-react-examples/virtual-event/)

## Important

- Use environment vars for apiKeys etc
- Make sure apiKey/userId/userToken can be set through queryParams
