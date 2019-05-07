# ![LOGO](logo.png) BC Data Catalogue **flow**ground Connector

## Description

A generated **flow**ground connector for the BC Data Catalogue API (version 3.0.1).

Generated from: https://api.apis.guru/v2/specs/gov.bc.ca/bcdc/3.0.1/openapi.json<br/>
Generated at: 2019-05-07T17:42:10+03:00

## API Description

This API provides live access to the BC Data Catalogue. Further documentation on the API is available from http://docs.ckan.org/en/latest/ Confirm the version of the API available from the catalogue by requesting https://catalogue.data.gov.bc.ca/api/3/action/status_show. 

Please note that you may experience issues when submitting requests to the delivery or test environment if using this [OpenAPI specification](https://github.com/bcgov/api-specs) in other API console viewers.

## Authorization

Supported authorization schemes:
- OAuth2
- API Key
For OAuth 2.0 you need to specify OAuth Client credentials as environment variables in the connector repository:
* `OAUTH_CLIENT_ID` - your OAuth client id
* `OAUTH_CLIENT_SECRET` - your OAuth client secret

## Actions

### Get the activity stream of an organization

> Return an organization's activity stream

*Tags:* `action`

#### Input Parameters
* `id` - _optional_ - The id or name of the organization

### Get the activity stream of an organization, HTML format

> Return an organization's activity stream as HTML

*Tags:* `action`

#### Input Parameters
* `id` - _optional_ - The id or name of the organization

### Get names of organizations that match a query string

> Return a list of organization names that contain a string

*Tags:* `action`

#### Input Parameters
* `q` - _optional_ - The string to search for
* `limit` - _optional_ - The maximum number of organizations to return (optional)

### Get number of followers of an organization

> Return the number of followers of an organization

*Tags:* `action`

#### Input Parameters
* `id` - _optional_ - The id or name of the organization

### Get users following an organization

> Return a list of users that are following a given organization

*Tags:* `action`

#### Input Parameters
* `id` - _optional_ - The id or name of the organization

### Get names of all organizations

> Returns the names of all indexed organizations

*Tags:* `action`

#### Input Parameters
* `offset` - _optional_ - The offset (index) of the first organizations to return
* `limit` - _optional_ - The number of organizations to be returned per page

### Get organizations that a user has a given permission for

> Return the organizations that the user has a given permission for

*Tags:* `action`

#### Input Parameters
* `permission` - _optional_ - The permission the user has against the returned organization

### Get organization revisions

> Return an organization's revisions

*Tags:* `action`

#### Input Parameters
* `id` - _optional_ - The name or id of the organization

### Get details of a specific organization

> Return the details of an organization

*Tags:* `action`

#### Input Parameters
* `id` - _optional_ - The id or name of the organization
* `include_datasets` - _optional_ - include a list of the organization's datasets

### Get the activity stream of a package (dataset)

> Returns a package's activity stream

*Tags:* `action`

#### Input Parameters
* `id` - _optional_ - The id or name of the package
* `offset` - _optional_ - Where to start getting activity items from
* `limit` - _optional_ - The maximum number of activities to return

### Get the activity stream of a package (dataset), HTML format

> The activity stream is rendered as a snippet of HTML meant to be included in an HTML pag, i.e it doesn't have any header or footer.

*Tags:* `action`

#### Input Parameters
* `id` - _optional_ - The id or name of the package
* `offset` - _optional_ - Where to start getting activity items from
* `limit` - _optional_ - The maximum number of activities to return

### Find packages (datasets) matching a query

> Return a list of datasets that match a string

*Tags:* `action`

#### Input Parameters
* `q` - _optional_ - The string to query
* `limit` - _optional_ - The maximum number of resource formats to return

### Get a list of all packages (datasets)

> Returns the names of all indexed packages (datasets)

*Tags:* `action`

#### Input Parameters
* `offset` - _optional_ - The offset (index) of the first package to return
* `limit` - _optional_ - The number of packages to be returned per page

### Get package (dataset) relationships

> Return a dataset's relationships

*Tags:* `action`

#### Input Parameters
* `id` - _optional_ - The id or name of the first package
* `id2` - _optional_ - The id or name of the second package
* `rel` - _optional_ - relationship as string

### Get list of revisions for a package (dataset)

> Return a dataset's revision as a list of dictionaries

*Tags:* `action`

#### Input Parameters
* `id` - _optional_ - The id or name of the dataset

### Find packages (datasets) matching query terms

> Searches for packages (datasets) matching the specified query terms

*Tags:* `action`

#### Input Parameters
* `q` - _optional_ - A query string

### Get metadata about one specific package (dataset)

> Returns metadata about the package (dataset) corresponding to the specified unique name

*Tags:* `action`

#### Input Parameters
* `id` - _optional_ - The package name

### Gets items related to a package (dataset)

> Returns a dataset's related items.

*Tags:* `action`

#### Input Parameters
* `id` - _optional_ - id or name of the dataset (optional)
* `dataset` - _optional_ - Dataset dictionary of the dataset (optional)
* `type_filter` - _optional_ - The type of related item to show (optional)
* `sort` - _optional_ - The order to sort the related items in
* `featured` - _optional_ - whether or not to restrict the results to only featured items

### Find resources

> Returns a dictionary with two fields ``count`` and ``results``.             The ``count`` field contains the total number of Resources                found without the limit or query parameters having an effect.             The ``results`` field is a list of dictized Resource objects.             The query parameter is a required field. It is a string in                the form ``{field}:{term}`` or a list of strings, each of the             same form. Within each string, ``{field}`` is a field or extra             field on the Resource domain object.

*Tags:* `action`

#### Input Parameters
* `query` - _optional_ - The search criteria string or list of strings of the form ``{field}:{term1}``
* `fields` - _optional_ - Depreciated
* `order_by` - _optional_ - A field on the resource model that orders the results
* `offset` - _optional_ - Apply an offset to the query
* `limit` - _optional_ - Apply a limit to the query

### Get metadata for a specific resource

> Return the metadata of a resource

*Tags:* `action`

#### Input Parameters
* `id` - _optional_ - The id of the resource
* `include_tracking` - _optional_ - Add tracking information to dataset

### Get the site status

> Returns the site status

*Tags:* `action`

### Get a list of tags

> Returns the names of all indexed tags

*Tags:* `action`

#### Input Parameters
* `offset` - _optional_ - The offset (index) of the first tag to return
* `limit` - _optional_ - The number of tags to be returned per page

## License

**flow**ground :- Telekom iPaaS / gov-bc-ca-bcdc-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
