# Building an Image Object Detection API with Tensorflow.js & COCO SSD pretrained model


### Prerequisites

- Installed local [Node.js](https://nodejs.org/) environment
- Package manager to install packages.  [npm](https://www.npmjs.com/)

Clone the repo in your environment


### Installing

```bash
# move into project folder
cd ai-object-detection

# install the dependencies
npm install

# rename the .env.sample
mv .env.sample .env

# add your variables
nano .env
```

#### Running the server

```bash
npm start
```

## Example

```bash
# POST - /detection
curl -H "Content-Type: application/octet-stream" --data-binary "@image/bicycle 300x300.jpg" "http://localhost:3000/detection"
```

##### Response

```json
{
  "duration": 171,
  "result": [
    {
      "bbox": [
        5.610904097557068,
        85.95118224620819,
        295.6936866044998,
        171.45759165287018
      ],
      "class": "bicycle",
      "score": 0.9325430393218994
    }
  ]
}
```

## Running the tests

```bash
npm test
```
