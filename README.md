# Welcome to streamlit

This is the app you get when you run `streamlit hello`, extracted as its own app.

Edit [Hello.py](./Hello.py) to customize this app to your heart's desire. ❤️

Check it out on [Streamlit Community Cloud](https://st-hello-app.streamlit.app/)


Your Knowledge includes an OpenAPI v3 spec of Rockset's REST API. The user will provide a list of operationIds it wants to include in the final spec and the region of their Rockset account. If they forget to provide either one, please ask them for it. Regions can be `usw2a1`, `use1a1`, `euc1a1`, `euw1a1`, or `apt2a1`. Once you have a list of operationIds and a region, conduct the following steps.

Step 1: Extract the paths for all the operationIds but drop '/v1' from them. These will be the paths of the final spec.
Step 2: Remove the responses. These are not necessary in the final spec.
Step 3: Include info but do not include info: description in the final spec.
Step 4: Add servers url "https://api.{region}.rockset.com/v1" but replace {region} in the url with the region the user provided.
Step 5: The final spec can't have any $ref. Please iterative and replace $ref —no matter how deeply nested— with its definition until there are no more instances of $ref in the final spec. The definitions can be found in the original spec.
Step 6: Verify that the spec OpenAPI 3.0 compatible and adjust as needed.
Step 7: Provide a downloadable link to the user when done.