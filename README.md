# Go challenge

Edit `selectListings` in `challenge/main.go`. Leave the API unchanged, and do not call it from your program.

Start the API from the project root and leave that terminal open:

```bash
cd backend
npm install
npm run dev
```

The API listens on http://localhost:4000.

Run your result from the project root:

```bash
cd challenge
go run .
```

Compare it with:

```bash
curl.exe "http://localhost:4000/api/properties?type=Residential&minYield=6&sort=yieldPercent&order=desc"
```

task: "Read catalog.json and print the residential listings whose yield is at least 6, highest yield first. Each object must include modeledIncomeNote set to \"{yieldPercent}% modeled annual yield\". If two yields match, the lower id comes first. Array order matters. Field order does not."

pass if: "The parsed JSON is the same array, in the same order, as http://localhost:4000/api/properties?type=Residential&minYield=6&sort=yieldPercent&order=desc."
