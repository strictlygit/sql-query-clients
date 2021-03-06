Introduction
================================================

ibmcloudsql
------------------------

Working with structured data in IBM Cloud Object Storage using SQL language, involves multiple capabilities:

1. (A) `IBM Cloud access <https://cloud.ibm.com/docs/iam?topic=iam-manapikey>`_ which control access to all IBM catalogs/resources
2. (B) `IBM COS instance <https://www.ibm.com/cloud/object-storage>`_ where input and outpout data is stored.
3. (C) `IBM Cloud SQL Query instance <https://www.ibm.com/cloud/sql-query>`_ which offers the SQL-based data processing service
4. (D) Optionally: `IBM Watson Studio <https://www.ibm.com/cloud/watson-studio>`_: which provides notebook environment for running notebook, in that (Python) code and data asset are also stored, implicitly, in the Project's IBM COS instance.
5. (E) Visualization: can be done with Python code via IBM Watson Studio's notebook

..
    6. (F) Visualization: can be done via  ...
    7. (G) The back-end server may be running on `IBM Cloud Function <https://cloud.ibm.com/functions/>`_ 

This **ibmcloudsql** library provides these multiuple parts to Python applications. It comes with multiple submodules, each one links to another via subclass mechanism.

..  package extends the functionality of `ibmcloudsql <https://github.com/IBM-Cloud/sql-query-clients>`_

The submodules

* :ref:`utilities <utilities-label>` provides (A) - the IBM Cloud service connectivity-related functionality
* :ref:`cos <cos-label>` provides (A, B) - the COS-related functionality
* :ref:`SQLQuery <sql_query-label>` provides (A, B, C)
* (D, E) is done via notebook-based examples of user-specific code which also utilizes above submodules. For getting started use this `starter notebook <https://dataplatform.cloud.ibm.com/exchange/public/entry/view/4a9bb1c816fb1e0f31fec5d580e4e14d>`_.


To install your package in from source in this repository in editable mode:

.. code-block:: console

    cd sql-query-client/Python
    pip install -e .

To run the test on the package, run either

.. code-block:: console

    python -m pytest

    pytest

To install the published release of **ibmcloudsql** from `PyPi <https://pypi.org/project/ibmcloudsql/>`_:

 .. code-block:: console

     pip install ibmcloudsql
