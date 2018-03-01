# ftelnotes-api-meteor

'api' folder of FTEL Notes Project split out here.

# How to deploy this?

## Deploy video
[![Watch the video](https://cdn1.iconfinder.com/data/icons/logotypes/32/youtube-256.png)](http://youtu.be/vt5fpE0bzSY)

## Deploy on Heroku

Full tutorial: [Here](https://medium.com/@pushplaybang/deploying-and-hosting-meteor-on-heroku-mongolab-for-free-37050a3ebd7e)

### Config Variables

`heroku config:set EMAIL_URL=smtp://USERNAME:PASSWORD@HOST:PORT/` (If your app sent email)

Example for gmail: `EMAIL_URL=smtps://abcd%40gmail.com:password@smtp.gmail.com:465/`

`heroku config:set MONGO_URL=mongodb://your-db-user-name:your-db-password@ds017231.mlab.com:17231/db-name`

`heroku config:set ROOT_URL=your-heroku-url`

### Buildpacks

Meteor Buildpack Horse: 
`https://github.com/AdmitHub/meteor-buildpack-horse.git`

### Some error

- To fix error: `at=error code=H14 desc="No web processes running" method=GET path="/sockjs/info?cb=2uma05ykoi`

Use command: `heroku ps:scale web=1 -a <app-name>`

- To fix error `No 'Access-Control-Allow-Origin' header is present on the requested resource`
![Fix erroer](https://lh6.googleusercontent.com/61wGCXNWCUVL344WZD0W8JrKHsAaZCv67F6wxYvCJr74L3OXnvZDNJJv5SAlBF6vZw1W5uOKiD87Jg=w1366-h647)

- To fix `Error: Invalid login` for Gmail account: [Click here](https://productforums.google.com/forum/#!topic/gmail/9KCgzXY4G_c)

## Deploy on Galaxy

Just one Command line:

`$ DEPLOY_HOSTNAME=us-east-1.galaxy-deploy.meteor.com meteor deploy [hostname] --settings settings.json`

Full tutorial: [Here](https://galaxy-guide.meteor.com/deploy-quickstart.html)

![](https://lh3.googleusercontent.com/nFELCaDjUl5dz5kU0wcS7g2AegNnRUyZXZtQBjAbawr_rsyLvVXYI_jwfYUFtl-Wv5_D77ZEzXIZbFi8Auqk=w1366-h647)