---
title: "Activities"
parent: "application-logic"
menu_order: 30
tags: ["studio pro", "microflows", "nanoflows", "activity"]
---

## 1 Introduction

Activities represent the actions that are executed in a microflow or a nanoflow.

The following types of activities are available:

## 2 Object Activities

Object activities can be used to create and manipulate objects. The [domain model](domain-model) defines the object types ([entities](entities)) that can be used.

| Graphic | Name | Description |
| --- | --- | --- |
| [![](attachments/819203/918013.png)](cast-object) | [Cast object](cast-object) | Cast object can be used in combination with an [object type decision](object-type-decision) to use the [specialized](entities) members of the object. |
| [![](attachments/819203/917661.png)](change-object) | [Change object](change-object) | Change object can be used to change the members of an object. This can be done with or without committing and with or without events. |
| [![](attachments/819203/17661961.png)](committing-objects) | [Commit object(s)](committing-objects) | Commit object(s) can be used to commit the changes to one or more objects. |
| [![](attachments/819203/917756.png)](create-object) | [Create object](create-object) | Create object can be used to create an object. |
| [![](attachments/819203/918191.png)](deleting-objects) | [Delete object(s)](deleting-objects) | Delete object can be used to delete an object. |
| [![](attachments/819203/917866.png)](retrieve) | [Retrieve](retrieve) | Retrieve can be used to get one (or more) associated objects of another object. Furthermore the activity can also get one (or more) objects directly from the database. |
| [![](attachments/819203/918119.png)](rollback-object) | [Rollback object](rollback-object) | Rollback object can be used to undo changes (that have not been committed) that were made to the object in the part of the microflow preceding the activity. Furthermore it deletes objects that have been created but have never been committed. |

## 3 List Activities

List activities can be used to create and manipulate lists of objects.

| Graphic | Name | Description |
| --- | --- | --- |
| [![](attachments/819203/918028.png)](aggregate-list) | [Aggregate list](aggregate-list) | Aggregate list can be used to calculate aggregated values such as the maximum, minimum, sum, average and total amount of objects over a list of objects. |
| [![](attachments/819203/918007.png)](change-list) | [Change list](change-list) | Change list can be used to change the content of a list of objects. |
| [![](attachments/819203/918009.png)](create-list) | [Create list](create-list) | Create list can be used to create a (empty) list of objects. |
| [![](attachments/819203/917792.png)](list-operation) | [List operation](list-operation) | List operation can be used to combine or compare two list with objects of the same entity. |

## 4 Action Call Activities

Action call activities can be used to call another microflow or to call a Java action.

| Graphic | Name | Description |
| --- | --- | --- |
| [![](attachments/819203/918018.png)](java-action-call) | [Java Action call](java-action-call) | Java Action call can be used to call a Java action. Arguments can be passed to the action and the result can be returned as an object, list, enumeration, or variable. |
| [![](attachments/819203/918001.png)](microflow-call) | [Microflow call](microflow-call) | Microflow call can be used to call another microflow. Arguments can be passed to the microflow and the result can be returned as an object, list, enumeration, or variable. |

## 5 Variable Activities

Variable activities can be used to create or change a variable within a microflow.

| Graphic | Name | Description |
| --- | --- | --- |
| [![](attachments/819203/918011.png)](change-variable) | [Change variable](change-variable) | Change variable can be used to change the value of a variable. |
| [![](attachments/819203/918110.png)](create-variable) | [Create variable](create-variable) | Create variable can be used to create a new variable. |

## 6 Client Activities

Client activities can be used to have the web client of your application perform an action, such as showing a different page or downloading a file.

| Graphic | Name | Description |
| --- | --- | --- |
| [![](attachments/819203/918114.png)](close-page) | [Close page](close-page) | Close page closes the page that is opened last by the user that calls the microflow where this activity is used in. |
| [![](attachments/819203/918108.png)](download-file) | [Download file](download-file) | Download file can be used to enable the browser to download a specific file. The user, that calls the microflow where this activity is used in, gets a download popup or the file is shown directly in the browser. |
| [![](attachments/819203/918099.png)](show-message) | [Show message](show-message) | Show message can be used to show a blocking or non-blocking message to the user that calls the microflow where this activity is used in. |
| [![](attachments/819203/917544.png)](show-page) | [Show page](show-page) | Show page can be used to show a page to the user that calls the microflow where this activity is used in. |
| [![](attachments/819203/918097.png)](validation-feedback) | [Validation feedback](validation-feedback) | Validation feedback can be used to display a red text below a widget that displays an attribute or association. |
| ![](attachments/819203/17661963.png) | [Show home page](show-home-page) | Show home Page can be used to navigate to the home page for the current user. |

## 7 Integration Activities

Integration activities can be used to integrate with other systems, for example by calling a web service.

| Graphic                              | Name                                         | Description                                                  |
| ------------------------------------ | -------------------------------------------- | ------------------------------------------------------------ |
| ![](attachments/819203/19399144.png) | [Call REST service](call-rest-action)         | Call rest action can be used to call a REST endpoint. You can use mappings to map results to entities or entities to requests. You can also store the result in a string variable, HTTP response, or File Document. |
| ![](attachments/819203/19398967.png) | [Call web service](call-web-service-action)  | Call web service action can be used to call one of the [imported web services](consumed-web-services). The content of the request can be edited. Furthermore the response of the webservice can be mapped to entities, stored or be ignored. |
| ![](attachments/819203/19398968.png) | [Import with mapping](import-mapping-action) | Import with mapping can be used to parse the data in a string variable or data stored in a file document, and store them in entity objects defined in the [domain model](domain-model) of the database. An [Import Mapping](import-mappings) is used to map the incoming XML or JSON to entities. |
| ![](attachments/819203/19398969.png) | [Export with mapping](export-mapping-action) | Export with mapping can be used to export the data stored in [domain model](domain-model) entities into an XML or JSON string. It can also be stored in a file document. An [Export Mapping](export-mappings) is used to map domain model entities into XML or JSON. |

## 8 Document Generation Activities

| Graphic | Name | Description |
| --- | --- | --- |
| [![](attachments/819203/918124.png)](generate-document) | [Generate document](generate-document) | Generate document can be used to create a document of a certain type based on a [template](document-templates). |
