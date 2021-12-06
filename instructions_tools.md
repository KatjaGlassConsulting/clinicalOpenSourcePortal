# Instructions to add Open-Source Tool (/tools)

To submit a new open source tool to be included into the portal, please provide information and ignore/delete those fields which are not applicable. If you have multiple links, please use an array.

The metadata is using the JSON format. Areas where there could be multiple information, e.g. multiple presentations, can simply be exchanged from one string value to an array of string values.

```json
    "areaUsers": "ANALYST"

    "areaUsers": [
        "PROG",
        "ANALYST",
        "STAT"
    ]
```

For vignettes it makes sense to provide also a label for a specific link. In this case please use the following syntax:

```json
"linkVignette": [
    {"Example 1": "https://cran.r-project.org/web/packages/.../xy.html"},
    {"Example 2": "https://cran.r-project.org/web/packages/.../yz.html"}
]
```

The following example shows all currently supported fields and is available under [/tools/reindeer.json](./tools/reindeer.json):

```json
"reindeer": {
        "id": "reindeer",
        "groupID": "",
        "name": "Reindeer - Result Render Tool",
        "openSource": true,
        "type": "Tool",
        "description": "Reindeer is a VBA tool to render SAS results in LISTING, RTF, TAGSETS.RTF and Figures into a Word template file. PDF can be generated as well. This easy to use and very intuitive open source tool is sponsored by ClinStat.",
        "language": [
            "Other",
            "SAS"
        ],
        "outstanding": "Sponsorship enabled this tool! We need more of this!",
        "commercialExtras":"",
        "thinkAbouts": "",
        "lastUpdateDate": "2021-03-05",
        "linkGithubNY": true,
        "linkSource": "https://github.com/KatjaGlassConsulting/reindeer",
        "linkDocumentation": "https://github.com/KatjaGlassConsulting/reindeer/blob/master/doc/Reindeer.docm",
        "linkHomepage": "",
        "linkCompany": "https://www.glacon.eu",
        "license": "MIT",
        "documentation": "The documentation is available in the Word file containing the tool itself.",
        "authorType": "company",
        "authors": "Katja Glass",
        "areaUsers": [
            "PROG",
            "ANALYST"
        ],
        "areaWorkfield": "Outputs",
        "size": "medium",
        "relevance": 5,
        "image": "reindeer_01.png",
        "images": [
            "reindeer_01.png",
            "reindeer_02.png",
            "reindeer_03.png"
        ],
        "logo": "glacon_logo.png",
        "linkPresentation": "",
        "linkPaper": "",
        "linkVideo": "",
        "linkLicense": "",
        "linkPoster": "",
        "linkDemonstration": "",
        "linkVignette": ""
    }
```

Most fields are self-explaining. Please find here further information for some keys:

Key | Description
-- | --
id | Please use a speaking short ID, use this as prefix for images related to your tool
groupid | Only needed when this open-source tool should be referenced by "Programs"
type | types: "Scripts", "Tool" or "Link" type <br/> Typically links are not provided as separate entries here, but some links are overly userful and for this included
language | types: "SAS", "R", "Web", "Java", "RShiny", "Python" or "Other"
lastUpdateDate | regularily updated automatically when in standard repositories (e.g. GitHub, GitLab, CRAN)
authorType | types: "individual" or "company"
areaUsers | types: "ANALYST", "STAT", "DM", "PROG" or just missing
areaWorkfield | types: "Outputs", "Statistics", "Programming", "Visualization", "Define", "CDISC" or missing
size | types: "small", "medium", "large" - this is a soft assumption
image | the image as displayed as preview
images | list of all images
relevance | number between 1 (high relevance) and 10 (not very important) - this is a soft assumption and not visible

