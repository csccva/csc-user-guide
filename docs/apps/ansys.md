## ANSYS
ANSYS offers a comprehensive software suite that spans the entire range of physics, providing access to virtually any field of engineering simulation that a design process requires ([ANSYS - Products](https://www.ansys.com/products)). *ANSYS Academic engineering simulation software*  (hereinafter **AAESS**) is used by thousands of universities globally for undergraduate students to learn physics principles, for researchers to solve complex engineering problems and for postgraduate students to produce data for their master’s theses or doctoral dissertations ([ANSYS - Academic](https://www.ansys.com/academic)).

## License

AAESS products are proprietary software. CSC - IT Center for Science Ltd. has these licences available on CSC's server platforms. The licenses are only for academic use.  See about use limitations from link given below (Ansys Academic - Terms and Conditions), and there, LICENSING AND TERM OF USE.

## Available

CSC's AAESS product licenses are available on CSC's computing platforms [Taito and Puhti](https://research.csc.fi/csc-s-servers).  Latest AAESS products will be available on the servers, and earlier versions installation is also possible.  All installed versions are maintained on the servers.

Notice that Taito server will be decommisioned in the end of December 2019.

## Usage

After login on the server, give command

    module available

and check lines *ansys/(version number)*. For example to load Ansys version 19.2., give command

    module load ansys/19.2

There are examples of **batch job files** available on Puhti server:

    Ansys CFX:        /appl/soft/eng/ansys_inc/example_batch_job_files/parjob_puhti_cfx

    Ansys Fluent:     /appl/soft/eng/ansys_inc/example_batch_job_files/parjob_puhti_fluent

    Ansys Structural: /appl/soft/eng/ansys_inc/example_batch_job_files/parjob_puhti_struct

Copy those files and modify them for your own use. Further instructions are given in the files.

Ansys Fluent input files for the example batch job are in the folder:
 
    /appl/soft/eng/ansys_inc/example_case_files/aircraft_wing/
    

## Support

In problem situation, send an email to servicedesk@csc.fi.

## More information

* [Ansys Inc.](https://www.ansys.com/)
* [Ansys Academic - Terms and Conditions](https://www.ansys.com/academic/terms-and-conditions)
* [Ansys Academic products feature table (2019)](https://www.ansys.com/-/media/ansys/corporate/files/pdf/product/academic/academic-products-features-table-2019-v2.pdf)


