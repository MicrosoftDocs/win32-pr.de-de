---
title: ms-DS-Service-Connection-Point-Publication-Service-Klasse
description: Speichert Konfigurationsoptionen für den Dienstverbindungspunkt-Veröffentlichungsdienst in ADAM.
ms.assetid: 30b4df70-a03b-4d42-b200-75bfa6cf8273
ms.tgt_platform: multiple
keywords:
- ms-DS-Service-Connection-Point-Publication-Service-Klasse AD-Schema
- msDS-ServiceConnectionPointPublicationService-Klasse AD-Schema
topic_type:
- apiref
api_name:
- ms-DS-Service-Connection-Point-Publication-Service
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13b458a5d66d8d6fd90a58519ce57de03f625087be4123f2e51ca8c09534ed96
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119879840"
---
# <a name="ms-ds-service-connection-point-publication-service-class"></a>ms-DS-Service-Connection-Point-Publication-Service-Klasse

Speichert Konfigurationsoptionen für den Dienstverbindungspunkt-Veröffentlichungsdienst in ADAM.



| Eingabe | Wert |
|-------------------|----------------------------------------------------|
| CN                | ms-DS-Service-Connection-Point-Publication-Service |
| Ldap-Anzeigename | msDS-ServiceConnectionPointPublicationService      |
| Aktualisieren von Berechtigungen  | \-                                                 |
| Updatehäufigkeit  | \-                                                 |
| Schema-ID-GUID    | d33f5da6-b009-7e48-8268-b2305529e933               |



## <a name="implementations"></a>Implementierungen

-   [**Adam**](#adam-attributes)

## <a name="adam"></a>Adam

-   [Attribute](#adam-attributes)



| Eingabe | Wert |
|-----------------------------|----------------------------------------|
| System-Only                 | Richtig                                   |
| Object-Category             | 1                                      |
| Default-Object-Category     | \-                                     |
| Governs-Id                  | 1.2.840.113556.1.5.247                 |
| Default-Hiding-Value        | 1                                      |
| Rdn-Att-Id                  | [**Common-Name**](a-cn.md)<br/> |
| Unterklasse von                 | [**Nach oben**](c-top.md)<br/>        |
| Mögliche Vorgesetzte          | [**NTDS-Service**](c-ntdsservice.md)  |
| Zusätzlich           | \-                                     |
| NT-Security-Descriptor      | O:BAG:BAD:S:                           |
| Standardsicherheitsdeskriptor | D:S:                                   |
| System-Flags                | 0x00000000                             |



## <a name="adam-attributes"></a>ADAM-Attribute

Diese Klasse enthält die folgenden Attribute für ADAM:



| attribute                                                                   | Obligatorisch. | Abgeleitet von                                           |
|-----------------------------------------------------------------------------|-----------|--------------------------------------------------------|
| [**Admin-Description**](a-admindescription.md)                             | Falsch     | [**Nach oben**](c-top.md)<br/>                        |
| [**Administratoranzeigename**](a-admindisplayname.md)                            | Falsch     | [**Nach oben**](c-top.md)<br/>                        |
| [**Allowed-Attributes**](a-allowedattributes.md)                           | Falsch     | [**Nach oben**](c-top.md)<br/>                        |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)        | Falsch     | [**Nach oben**](c-top.md)<br/>                        |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                      | Falsch     | [**Nach oben**](c-top.md)<br/>                        |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)   | Falsch     | [**Nach oben**](c-top.md)<br/>                        |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)               | Falsch     | [**Nach oben**](c-top.md)<br/>                        |
| [**Kanonischer Name**](a-canonicalname.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                        |
| [**Common-Name**](a-cn.md)                                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                        |
| [**Create-Time-Stamp**](a-createtimestamp.md)                              | Falsch     | [**Nach oben**](c-top.md)<br/>                        |
| [**Beschreibung**](a-description.md)                                        | Falsch     | [**Nach oben**](c-top.md)<br/>                        |
| [**Anzeigename**](a-displayname.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                        |
| [**DSA-Signature**](a-dsasignature.md)                                     | Falsch     | [**Nach oben**](c-top.md)<br/>                        |
| [**DS-Core-Propagierungsdaten**](a-dscorepropagationdata.md)                 | Falsch     | [**Nach oben**](c-top.md)<br/>                        |
| [**Aktiviert**](a-enabled.md)                                                | Falsch     | **ms-DS-Service-Connection-Point-Publication-Service** |
| [**From-Entry**](a-fromentry.md)                                           | Falsch     | [**Nach oben**](c-top.md)<br/>                        |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                        |
| [**Instanztyp**](a-instancetype.md)                                     | Richtig      | [**Nach oben**](c-top.md)<br/>                        |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)               | Falsch     | [**Nach oben**](c-top.md)<br/>                        |
| [**Is-Deleted**](a-isdeleted.md)                                           | Falsch     | [**Nach oben**](c-top.md)<br/>                        |
| [**Is-Member-of-DL**](a-memberof.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                        |
| [**Keywords**](a-keywords.md)                                              | Falsch     | **ms-DS-Service-Connection-Point-Publication-Service** |
| [**Last-Known-Parent**](a-lastknownparent.md)                              | Falsch     | [**Nach oben**](c-top.md)<br/>                        |
| [**Verwaltete Objekte**](a-managedobjects.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                        |
| [**Mastered-By**](a-masteredby.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/>                        |
| [**Modify-Time-Stamp**](a-modifytimestamp.md)                              | Falsch     | [**Nach oben**](c-top.md)<br/>                        |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md) | Falsch     | [**Nach oben**](c-top.md)<br/>                        |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)      | Falsch     | [**Nach oben**](c-top.md)<br/>                        |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | Falsch     | [**Nach oben**](c-top.md)<br/>                        |
| [**ms-DS-Disable-For-Instances**](a-msds-disableforinstances.md)           | Falsch     | **ms-DS-Service-Connection-Point-Publication-Service** |
| [**ms-DS-Disable-For-Instances-BL**](a-msds-disableforinstancesbl.md)      | Falsch     | [**Nach oben**](c-top.md)<br/>                        |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                              | Falsch     | [**Nach oben**](c-top.md)<br/>                        |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                       | Falsch     | [**Nach oben**](c-top.md)<br/>                        |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)    | Falsch     | [**Nach oben**](c-top.md)<br/>                        |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)  | Falsch     | [**Nach oben**](c-top.md)<br/>                        |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)      | Falsch     | [**Nach oben**](c-top.md)<br/>                        |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)              | Falsch     | [**Nach oben**](c-top.md)<br/>                        |
| [**ms-DS-SCP-Container**](a-msds-scpcontainer.md)                          | Falsch     | **ms-DS-Service-Connection-Point-Publication-Service** |
| [**ms-DS-Service-Account-BL**](a-msds-serviceaccountbl.md)                 | Falsch     | [**Nach oben**](c-top.md)<br/>                        |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                    | Richtig      | [**Nach oben**](c-top.md)<br/>                        |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                | Falsch     | [**Nach oben**](c-top.md)<br/>                        |
| [**Objektkategorie**](a-objectcategory.md)                                 | Richtig      | [**Nach oben**](c-top.md)<br/>                        |
| [**Objektklasse**](a-objectclass.md)                                       | Richtig      | [**Nach oben**](c-top.md)<br/>                        |
| [**Objekt-GUID**](a-objectguid.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/>                        |
| [**Objektversion**](a-objectversion.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                        |
| [**Andere bekannte Objekte**](a-otherwellknownobjects.md)                 | Falsch     | [**Nach oben**](c-top.md)<br/>                        |
| [**Teilattributlöschungsliste**](a-partialattributedeletionlist.md)   | Falsch     | [**Nach oben**](c-top.md)<br/>                        |
| [**Teilattributsatz**](a-partialattributeset.md)                      | Falsch     | [**Nach oben**](c-top.md)<br/>                        |
| [**Mögliche Hindernisse**](a-possibleinferiors.md)                           | Falsch     | [**Nach oben**](c-top.md)<br/>                        |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                          | Falsch     | [**Nach oben**](c-top.md)<br/>                        |
| [**Proxyadressen**](a-proxyaddresses.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                        |
| [**Query-Policy-BL**](a-querypolicybl.md)                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                        |
| [**Rdn**](a-name.md)                                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                        |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                   | Falsch     | [**Nach oben**](c-top.md)<br/>                        |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                        | Falsch     | [**Nach oben**](c-top.md)<br/>                        |
| [**Reps-From**](a-repsfrom.md)                                             | Falsch     | [**Nach oben**](c-top.md)<br/>                        |
| [**Reps-To**](a-repsto.md)                                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                        |
| [**Revision**](a-revision.md)                                              | Falsch     | [**Nach oben**](c-top.md)<br/>                        |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                          | Falsch     | [**Nach oben**](c-top.md)<br/>                        |
| [**Server-Reference-BL**](a-serverreferencebl.md)                          | Falsch     | [**Nach oben**](c-top.md)<br/>                        |
| [**Nur in erweiterter Ansicht anzeigen**](a-showinadvancedviewonly.md)              | Falsch     | [**Nach oben**](c-top.md)<br/>                        |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | Falsch     | [**Nach oben**](c-top.md)<br/>                        |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                  | Falsch     | [**Nach oben**](c-top.md)<br/>                        |
| [**Sub-Refs**](a-subrefs.md)                                               | Falsch     | [**Nach oben**](c-top.md)<br/>                        |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | Falsch     | [**Nach oben**](c-top.md)<br/>                        |
| [**Systemflags**](a-systemflags.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                        |
| [**USN geändert**](a-usnchanged.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/>                        |
| [**USN-erstellt**](a-usncreated.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/>                        |
| [**USN-DSA-last-obj-removed**](a-usndsalastobjremoved.md)                  | Falsch     | [**Nach oben**](c-top.md)<br/>                        |
| [**USN-Intersite**](a-usnintersite.md)                                     | Falsch     | [**Nach oben**](c-top.md)<br/>                        |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                        |
| [**USN-Quelle**](a-usnsource.md)                                           | Falsch     | [**Nach oben**](c-top.md)<br/>                        |
| [**Wbem-Pfad**](a-wbempath.md)                                             | Falsch     | [**Nach oben**](c-top.md)<br/>                        |
| [**Bekannte Objekte**](a-wellknownobjects.md)                            | Falsch     | [**Nach oben**](c-top.md)<br/>                        |
| [**Bei Änderung**](a-whenchanged.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                        |
| [**Bei der Erstellung**](a-whencreated.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                        |
| [**WWW-Startseite**](a-wwwhomepage.md)                                      | Falsch     | [**Nach oben**](c-top.md)<br/>                        |
| [**WWW-Page-Other**](a-url.md)                                             | Falsch     | [**Nach oben**](c-top.md)<br/>                        |



 

 





