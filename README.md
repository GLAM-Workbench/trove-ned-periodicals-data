# trove-ned-periodicals-data

This dataset contains details of periodical titles and issues submitted to the Trove through the NLA's National edeposit scheme. It includes CSV-formatted lists of titles and issues, and an SQLite database created for use with Datasette-Lite.

These datasets were generated using notebooks in the [trove-journals](https://github.com/GLAM-Workbench/trove-journals/) repository.

For more information and documentation see the [Details of periodicals submitted to Trove through the National edeposit scheme (NED)](https://glam-workbench.net/trove-journals/trove-ned-periodicals-data/) section of the [GLAM Workbench](https://glam-workbench.net).

## Dataset summary
- [ned-periodicals.csv](https://github.com/GLAM-Workbench/trove-ned-periodicals-data/raw/main/ned-periodicals.csv) (4.9 MB, text/csv)
- [ned-periodical-issues.csv](https://github.com/GLAM-Workbench/trove-ned-periodicals-data/raw/main/ned-periodical-issues.csv) (40.1 MB, text/csv)
- [ned-periodicals.db](https://github.com/GLAM-Workbench/trove-ned-periodicals-data/raw/main/ned-periodicals.db) (57.7 MB, db)


## Dataset details

### [ned-periodicals.csv](https://github.com/GLAM-Workbench/trove-ned-periodicals-data/raw/main/ned-periodicals.csv)

|                |                                                                                                                                                                                                                                                                                             |
|:---------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| date harvested | 2024-04-10                                                                                                                                                                                                                                                                                  |
| file size      | 4.9 MB                                                                                                                                                                                                                                                                                      |
| format         | text/csv                                                                                                                                                                                                                                                                                    |
| created by     | <a href='https://github.com/GLAM-Workbench/trove-journals/blob/master/harvest-ned-periodicals.ipynb'>Harvest details of periodicals submitted to Trove through the National edeposit scheme (NED)</a> ([documentation](https://glam-workbench.net/trove-journals/harvest-ned-periodicals/)) |
| number of rows | 7974                                                                                                                                                                                                                                                                                        |

#### Columns

| name            | type   | description                                                                              |
|:----------------|:-------|:-----------------------------------------------------------------------------------------|
| `id`            | string | digital object identifier                                                                |
| `title`         | string | title of the periodical; multiple values separated by | symbol                           |
| `contributor`   | string | multiple values separated by | symbol                                                    |
| `publisher`     | string | multiple values separated by | symbol                                                    |
| `date`          | string | multiple values separated by | symbol                                                    |
| `fulltext_url`  | string | link to digitised viewer                                                                 |
| `work_url`      | string | link to work record in Trove; multiple values separated by | symbol                      |
| `work_type`     | string | Trove work format, eg: 'Periodical'; multiple values separated by | symbol               |
| `type`          | string | eg: 'text'; multiple values separated by | symbol                                        |
| `format`        | string | eg: 'volume'; multiple values separated by | symbol                                      |
| `extent`        | string | size or physical dimensions; multiple values separated by | symbol                       |
| `language`      | string | publication language; multiple values separated by | symbol                              |
| `subject`       | string | associated subject headings; multiple values separated by | symbol                       |
| `spatial`       | string | related places; multiple values separated by | symbol                                    |
| `is_part_of`    | string | collections or series this publication is part of; multiple values separated by | symbol |
| `identifier`    | string | library identifiers; multiple values separated by | symbol                               |
| `rights`        | string | copyright and licensing information; multiple values separated by | symbol               |
| `catalogue_url` | any    | link to NLA catalogue; multiple values separated by | symbol                             |

### [ned-periodical-issues.csv](https://github.com/GLAM-Workbench/trove-ned-periodicals-data/raw/main/ned-periodical-issues.csv)

|                |                                                                                                                                                                                                                                                                                             |
|:---------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| date harvested | 2024-04-10                                                                                                                                                                                                                                                                                  |
| file size      | 40.1 MB                                                                                                                                                                                                                                                                                     |
| format         | text/csv                                                                                                                                                                                                                                                                                    |
| created by     | <a href='https://github.com/GLAM-Workbench/trove-journals/blob/master/harvest-ned-periodicals.ipynb'>Harvest details of periodicals submitted to Trove through the National edeposit scheme (NED)</a> ([documentation](https://glam-workbench.net/trove-journals/harvest-ned-periodicals/)) |
| number of rows | 156153                                                                                                                                                                                                                                                                                      |

#### Columns

| name                | type    | description                                                                        |
|:--------------------|:--------|:-----------------------------------------------------------------------------------|
| `id`                | string  | issue's digital object identifier                                                  |
| `title_id`          | string  | parent title's digital object identifier                                           |
| `title`             | string  | parent title's name                                                                |
| `description`       | string  | usually contains additional publication information, eg 'Issue 66 (2019)'          |
| `date`              | integer | year of publication                                                                |
| `url`               | string  | link to digitised viewer                                                           |
| `ebook_type`        | string  | publication mimetype, eg: 'application/pdf', or 'application/epub+zip'             |
| `access_conditions` | string  | indicates level of online access, eg 'Unrestricted', 'View only', or 'Onsite only' |
| `copyright_policy`  | string  | copyright status, eg 'In copyright'                                                |
| `download_link`     | string  | link to download this issue from Trove                                             |

### [ned-periodicals.db](https://github.com/GLAM-Workbench/trove-ned-periodicals-data/raw/main/ned-periodicals.db)

|                |                                                                                                                                                                                                                                                                                                                                             |
|:---------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| date harvested | 2024-04-10                                                                                                                                                                                                                                                                                                                                  |
| file size      | 57.7 MB                                                                                                                                                                                                                                                                                                                                     |
| format         | db                                                                                                                                                                                                                                                                                                                                          |
| created by     | <a href='https://github.com/GLAM-Workbench/trove-journals/blob/master/harvest-ned-periodicals.ipynb'>Harvest details of periodicals submitted to Trove through the National edeposit scheme (NED)</a> ([documentation](https://glam-workbench.net/trove-journals/harvest-ned-periodicals/))                                                 |
| description    | This SQLite database contains data relating to digitised periodical titles and issues from Trove. It was created for use with Datasette-Lite. There is a foreign key link between the issues and the titles, making it easy to find the issues from any title. Some extra columns have been added to include thumbnails and download links. |

## Examples of use

- [Explore in Datasette](https://glam-workbench.net/datasette-lite/?url=https://github.com/GLAM-Workbench/trove-ned-periodicals-data/blob/main/ned-periodicals.db&install=datasette-json-html&install=datasette-template-sql&metadata=https://github.com/GLAM-Workbench/trove-ned-periodicals-data/blob/main/metadata.json)


----
Created by [Tim Sherratt](https://timsherratt.au) for the [GLAM Workbench](https://glam-workbench.net)