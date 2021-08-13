---
title: ms-DS-Bindable-Object-Klasse
description: Hilfsklasse, die ein bindbares Objekt darstellen soll. Jede benutzerdefinierte Klasse, die eine Entität darstellt, die zum Binden an das Verzeichnis (d. h. ein Benutzer) verwendet werden kann, sollte diese Hilfsklasse enthalten.
ms.assetid: 181b3e2b-9442-4f11-9af7-4697491115f3
ms.tgt_platform: multiple
keywords:
- ms-DS-Bindable-Object-Klasse AD-Schema
- MSDS-BindableObject-Klasse AD-Schema
topic_type:
- apiref
api_name:
- ms-DS-Bindable-Object
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b702a26c61920f5a3868ccc479b1f8578a3075907b5dc5bc2eb9d070321c91d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118680780"
---
# <a name="ms-ds-bindable-object-class"></a>ms-DS-Bindable-Object-Klasse

Hilfsklasse, die ein bindbares Objekt darstellen soll. Jede benutzerdefinierte Klasse, die eine Entität darstellt, die zum Binden an das Verzeichnis (d. h. ein Benutzer) verwendet werden kann, sollte diese Hilfsklasse enthalten.



| Eingabe | Wert |
|-------------------|--------------------------------------|
| CN                | ms-DS-Bindable-Object                |
| Ldap-Anzeigename | msDS-BindableObject                  |
| Aktualisieren von Berechtigungen  | \-                                   |
| Updatehäufigkeit  | \-                                   |
| Schema-ID-GUID    | 89f4a69f-4416-6b49-821d-6e3c4a0ff802 |



## <a name="implementations"></a>Implementierungen

-   [**Adam**](#adam-attributes)

## <a name="adam"></a>Adam

-   [Attribute](#adam-attributes)



| Eingabe | Wert |
|-----------------------------|--------------------------------------------------------------|
| System-Only                 | Falsch                                                        |
| Object-Category             | 3                                                            |
| Default-Object-Category     | \-                                                           |
| Governs-Id                  | 1.2.840.113556.1.5.244                                       |
| Default-Hiding-Value        | 1                                                            |
| Rdn-Att-Id                  | \-                                                           |
| Unterklasse von                 | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/> |
| Mögliche Vorgesetzte          | \-                                                           |
| Zusätzlich           | \-                                                           |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                 |
| Standardsicherheitsdeskriptor | \-                                                           |
| System-Flags                | 0x00000010                                                   |



## <a name="adam-attributes"></a>ADAM-Attribute

Diese Klasse enthält die folgenden Attribute für ADAM:



| attribute                                                                                      | Obligatorisch. | Abgeleitet von                                                                                 |
|------------------------------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------|
| [**Konto läuft ab**](a-accountexpires.md)                                                    | Falsch     | **ms-DS-Bindable-Object**                                                                    |
| [**Admin-Description**](a-admindescription.md)                                                | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Administratoranzeigename**](a-admindisplayname.md)                                               | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Allowed-Attributes**](a-allowedattributes.md)                                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)                           | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Bad-Password-Time**](a-badpasswordtime.md)                                                 | Falsch     | **ms-DS-Bindable-Object**                                                                    |
| [**Bad-Pwd-Count**](a-badpwdcount.md)                                                         | Falsch     | **ms-DS-Bindable-Object**                                                                    |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Kanonischer Name**](a-canonicalname.md)                                                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Common-Name**](a-cn.md)                                                                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Create-Time-Stamp**](a-createtimestamp.md)                                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Beschreibung**](a-description.md)                                                           | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Anzeigename**](a-displayname.md)                                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**DSA-Signature**](a-dsasignature.md)                                                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**DS-Core-Propagierungsdaten**](a-dscorepropagationdata.md)                                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**From-Entry**](a-fromentry.md)                                                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                                     | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Instanztyp**](a-instancetype.md)                                                        | Richtig      | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Is-Deleted**](a-isdeleted.md)                                                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Is-Member-of-DL**](a-memberof.md)                                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Last-Known-Parent**](a-lastknownparent.md)                                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Letzter Anmeldezeitstempel**](a-lastlogontimestamp.md)                                           | Falsch     | **ms-DS-Bindable-Object**                                                                    |
| [**Sperrzeit**](a-lockouttime.md)                                                          | Falsch     | **ms-DS-Bindable-Object**                                                                    |
| [**Verwaltete Objekte**](a-managedobjects.md)                                                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Mastered-By**](a-masteredby.md)                                                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Modify-Time-Stamp**](a-modifytimestamp.md)                                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md)                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**ms-DS-Disable-For-Instances-BL**](a-msds-disableforinstancesbl.md)                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)                     | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**ms-DS-Service-Account-BL**](a-msds-serviceaccountbl.md)                                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**ms-DS-User-Account-Auto-Locked**](a-ms-ds-useraccountautolocked.md)                        | Falsch     | **ms-DS-Bindable-Object**                                                                    |
| [**ms-DS-User-Account-Control-Computed**](a-msds-user-account-control-computed.md)            | Falsch     | **ms-DS-Bindable-Object**                                                                    |
| [**ms-DS-User-Account-Disabled**](a-msds-useraccountdisabled.md)                              | Falsch     | **ms-DS-Bindable-Object**                                                                    |
| [**ms-DS-User-Dont-Expire-Password**](a-msds-userdontexpirepassword.md)                       | Falsch     | **ms-DS-Bindable-Object**                                                                    |
| [**ms-DS-User-Encrypted-Text-Password-Allowed**](a-ms-ds-userencryptedtextpasswordallowed.md) | Falsch     | **ms-DS-Bindable-Object**                                                                    |
| [**ms-DS-User-Password-Expired**](a-msds-userpasswordexpired.md)                              | Falsch     | **ms-DS-Bindable-Object**                                                                    |
| [**ms-DS-User-Password-Not-Required**](a-ms-ds-userpasswordnotrequired.md)                    | Falsch     | **ms-DS-Bindable-Object**                                                                    |
| [**Nt-Pwd-History**](a-ntpwdhistory.md)                                                       | Falsch     | **ms-DS-Bindable-Object**                                                                    |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                                       | Richtig      | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/> [**Nach oben**](c-top.md)<br/> |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Objektkategorie**](a-objectcategory.md)                                                    | Richtig      | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Object-Class**](a-objectclass.md)                                                          | Richtig      | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Objekt-GUID**](a-objectguid.md)                                                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Object-Sid**](a-objectsid.md)                                                              | Richtig      | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/>                                 |
| [**Object-Version**](a-objectversion.md)                                                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Andere bekannte Objekte**](a-otherwellknownobjects.md)                                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Mögliche 100000000000**](a-possibleinferiors.md)                                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                                             | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Proxyadressen**](a-proxyaddresses.md)                                                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Pwd-Last-Set**](a-pwdlastset.md)                                                           | Falsch     | **ms-DS-Bindable-Object**                                                                    |
| [**Query-Policy-BL**](a-querypolicybl.md)                                                     | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Rdn**](a-name.md)                                                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                                           | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Reps-From**](a-repsfrom.md)                                                                | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Reps-To**](a-repsto.md)                                                                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Revision**](a-revision.md)                                                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                                             | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Server-Reference-BL**](a-serverreferencebl.md)                                             | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Site-Object-BL**](a-siteobjectbl.md)                                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                                     | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Sub-Refs**](a-subrefs.md)                                                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                               | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Zusätzliche Anmeldeinformationen**](a-supplementalcredentials.md)                                  | Falsch     | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/>                                 |
| [**Systemflags**](a-systemflags.md)                                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Tokengruppen**](a-tokengroups.md)                                                          | Falsch     | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/>                                 |
| [**Unicode-Pwd**](a-unicodepwd.md)                                                            | Falsch     | **ms-DS-Bindable-Object**                                                                    |
| [**USN-Changed**](a-usnchanged.md)                                                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**VON USN erstellt**](a-usncreated.md)                                                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                                     | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**USN-Intersite**](a-usnintersite.md)                                                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**USN-Quelle**](a-usnsource.md)                                                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Wbem-Path**](a-wbempath.md)                                                                | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Bekannte Objekte**](a-wellknownobjects.md)                                               | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Wenn geändert**](a-whenchanged.md)                                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Wenn erstellt**](a-whencreated.md)                                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**WWW-Homepage**](a-wwwhomepage.md)                                                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**WWW-Page-Other**](a-url.md)                                                                | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |



 

 





