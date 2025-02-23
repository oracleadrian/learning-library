# Workshop with a single set of labs

## Instructions - Delete this file when finished

1. Open the sample-workshop template in Atom or Visual Studio Code
2. We pre-created 5 folders.  A workshop is created out of multiple labs.
3. Remove the comments like this one: *List objectives for this lab*
4. Make sure you use lower case folder and file name and dashes for spaces (setup-adb NOT Setup_ADB)
5. Your image names should have descriptive names. Not just adb1, adb2, adb3.  For handicap accessibility we need the image descriptions to explain what the image looks like.  Remember all lower case and dashes.
6. Make sure you watch this [video](https://otube.oracle.com/media/1_ucr6grc6) for how to do Self QA of a workshop.  These are the standards that need to be met before going to production.  (It's short don't worry!)
7. Download our [QA Feedback doc](https://confluence.oraclecorp.com/confluence/download/attachments/1966947336/LiveLabs-QA-Feedback-Form-v2.docx?version=2&modificationDate=1598913736000&api=v2) as well.  We find workshops get in production quicker when you know what's needed to move to production up front and you use the skeleton.

PS:  You do not need a Readme.md.  Readme's exist only at the top library levels. We direct all traffic to LiveLabs since we can't track usage on GitHub.  Do not create any direct links to GitHub, your workshop may be super popular but we can't track it so no one will know.

## Absolute Path for Oracle Cloud menu Navigation

**Lab 1: Provision an Instance -> Step 0: Use these Standardized Pictures for Oracle Cloud Navigation (Commonly for Provisioning)** - We've included a list of common screenshots for navigating the Oracle Cloud Menu. Please read this section and use the relevant absolute path images where appropriate.  This will future proof your workshop in case of Oracle Cloud user interface updates.

## Folder Structure

In this example, the goal is to create several "children" workshops from one longer "parent" workshop. The children are made up of parts from the parent.

- sample-workshop/
    - individual labs
        - prepare-setup/          -- contains the link to download the ORM/Terraform stack for the workshop
        - initialize-environment/ -- tasks to initialize the environment post Provisioning
        - provision/              -- first fictional lab
        - dataload/               -- second fictional lab
        - query/                  -- third fictional lab
        - introduction/
            - introduction.md     -- description of the everything workshop, note that it is a "lab" since there is only one
    - workshops/
      - desktop/                 -- *required* desktop version of the workshop (all labs)
          - index.html
          - manifest.json
      - desktop-advanced/        -- desktop version of the workshop (introduction, initialize-environment, dataload, query)
          - index.html
          - manifest.json
      - desktop-basics/          -- desktop version of the workshop (introduction, initialize-environment, provision)
          - index.html
          - manifest.json
      - freetier/                 -- *required* freetier version of the workshop (all labs)
          - index.html
          - manifest.json
      - freetier-advanced/        -- freetier version of the workshop (introduction, initialize-environment, dataload, query)
          - index.html
          - manifest.json
      - freetier-basics/          -- freetier version of the workshop (introduction, initialize-environment, provision)
          - index.html
          - manifest.json
      - livelabs/                 -- *required* livelabs version of the workshop (all labs)
         - index.html
         - manifest.json
      - livelabs-advanced/        -- livelabs version of the workshop (introduction, initialize-environment, dataload, query)
          - index.html
          - manifest.json
      - livelabs-basics/          -- livelabs version of the workshop (introduction, initialize-environment, provision)
           - index.html
           - manifest.json


### FreeTier vs LiveLabs vs desktop

* "Desktop"  - Workshop guide displayed inside the noVNC remote desktop session *required*
* "FreeTier" - Workshop provisioned using Free Trials, Paid Accounts and for some workshops, Always Free accounts (brown button) *required*
* "LiveLabs" - Workshop provisioned using "Reserve Workshop on LiveLabs" (green button) *required*
* "Desktop-xxxxxxx" - Subset or mini-workshop guide displayed inside the noVNC remote desktop session
* "FreeTier-xxxxxxx" - Subset or mini-workshop provisioned using Free Trials, Paid Accounts and for some workshops, Always Free accounts (brown button)
* "LiveLabs-xxxxxxx" - Subset or mini-workshop provisioned using "Reserve Workshop on LiveLabs" (green button)


### About the Workshop

The workshop includes all 6 of the individual labs in a single sequence.

The folder structure includes a Introduction "lab" that describes the workshop as a complete set of 6 labs. Note: you may not need to have a different introduction for each of the parent and child versions of the workshops, this is illustrative only.

Look at the product-name-workshop/freetier folder and look at the manifest.json file to see the structure.

> **Note:** The use "Lab n:" in the titles is optional

The Prerequisite "lab" is the first lab in a common folder on the oracle/learning-library repo. Because this lab already exists, we can use a RAW/absolute URL instead:

  ```
  "filename": "https://raw.githubusercontent.com/oracle/learning-library/master/common/labs/cloud-login/cloud-login-livelabs2.md"        },
  ```

The manifest.json file needs to know the location of each lab relative to where it exists in the hierarchy. In this structure, labs are located two levels up, for example:

  ```
  "filename": "../../provision/provision.md"
  ```

### For example:

This [APEX Workshop](https://oracle.github.io/learning-library/developer-library/apex/spreadsheet/workshops/freetier/) is a good example a workshop with a single set of labs: [https://github.com/oracle/learning-library/tree/master/developer-library/apex/spreadsheet](https://github.com/oracle/learning-library/tree/master/developer-library/apex/spreadsheet).


### More information

* [Creating the Structure of Markdown Labs](https://confluence.oraclecorp.com/confluence/display/DCS/Creating+the+Structure+of+Markdown+Labs)
* [See a working example on GitHub](https://github.com/oracle/learning-library/tree/master/data-management-library/autonomous-database/shared)
