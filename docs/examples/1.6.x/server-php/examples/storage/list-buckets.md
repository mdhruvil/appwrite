<?php

use Appwrite\Client;
use Appwrite\Services\Storage;

$client = (new Client())
    ->setEndpoint('https://<REGION>.cloud.appwrite.io/v1') // Your API Endpoint
    ->setProject('<YOUR_PROJECT_ID>') // Your project ID
    ->setKey('<YOUR_API_KEY>'); // Your secret API key

$storage = new Storage($client);

$result = $storage->listBuckets(
    queries: [], // optional
    search: '<SEARCH>' // optional
);