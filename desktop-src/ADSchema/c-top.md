---
title: Top-Klasse
description: Die Klasse der obersten Ebene, von der alle Klassen abgeleitet werden.
ms.assetid: 025aff6c-1804-4141-accf-d50cfd50e90e
ms.tgt_platform: multiple
keywords:
- AD-Schema der obersten Klasse
- AD-Schema der obersten Klasse
topic_type:
- apiref
api_name:
- Top
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 248726d9fac9c0d39fae5759df08d4ea10f4f012ba1a1ce0cc2f4dbe55d76a6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119580590"
---
# <a name="top-class"></a>Top-Klasse

Die Klasse der obersten Ebene, von der alle Klassen abgeleitet werden.



| Eingabe | Wert |
|-------------------|--------------------------------------|
| CN                | Oben                                  |
| Ldap-Anzeigename | top                                  |
| Aktualisieren von Berechtigungen  | Schemaadministrator                 |
| Updatehäufigkeit  | \-                                   |
| Schema-ID-GUID    | bf967ab7-0de6-11d0-a285-00aa003049e2 |



## <a name="implementations"></a>Implementierungen

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Adam**](#adam-attributes)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server

-   [Attribute](#windows-2000-server-attributes)



| Eingabe | Wert |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | True                                                                                         |
| Object-Category             | 2                                                                                            |
| Default-Object-Category     | \-                                                                                           |
| Governs-Id                  | 2.5.6.0                                                                                      |
| Default-Hiding-Value        | 1                                                                                            |
| Rdn-Att-Id                  | [**Common-Name**](a-cn.md)<br/>                                                       |
| Unterklasse von                 | **Top**<br/>                                                                           |
| Mögliche Vorgesetzte          | [**Lost-and-Found**](c-lostandfound.md)                                                     |
| Zusätzlich           | \-                                                                                           |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                 |
| Standardsicherheitsdeskriptor | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;;; AU) |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-2000-server-attributes"></a>Windows 2000-Serverattribute

Diese Klasse enthält die folgenden Attribute für Windows 2000-Server:



| attribute                                                                 | Obligatorisch. | Abgeleitet von |
|---------------------------------------------------------------------------|-----------|--------------|
| [**Admin-Description**](a-admindescription.md)                           | False     | **Top**      |
| [**Administratoranzeigename**](a-admindisplayname.md)                          | False     | **Top**      |
| [**Allowed-Attributes**](a-allowedattributes.md)                         | False     | **Top**      |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)      | False     | **Top**      |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                    | False     | **Top**      |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md) | False     | **Top**      |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)             | False     | **Top**      |
| [**Kanonischer Name**](a-canonicalname.md)                                 | False     | **Top**      |
| [**Common-Name**](a-cn.md)                                               | False     | **Top**      |
| [**Create-Time-Stamp**](a-createtimestamp.md)                            | False     | **Top**      |
| [**Beschreibung**](a-description.md)                                      | False     | **Top**      |
| [**Anzeigename**](a-displayname.md)                                     | False     | **Top**      |
| [**Display-Name-Printable**](a-displaynameprintable.md)                  | False     | **Top**      |
| [**DSA-Signature**](a-dsasignature.md)                                   | False     | **Top**      |
| [**DS-Core-Propagierungsdaten**](a-dscorepropagationdata.md)               | False     | **Top**      |
| [**Erweiterungsname**](a-extensionname.md)                                 | False     | **Top**      |
| [**Flaggen**](a-flags.md)                                                  | False     | **Top**      |
| [**From-Entry**](a-fromentry.md)                                         | False     | **Top**      |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)             | False     | **Top**      |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                 | False     | **Top**      |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                | False     | **Top**      |
| [**Instanztyp**](a-instancetype.md)                                   | True      | **Top**      |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)             | False     | **Top**      |
| [**Is-Deleted**](a-isdeleted.md)                                         | False     | **Top**      |
| [**Is-Member-of-DL**](a-memberof.md)                                     | False     | **Top**      |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                        | False     | **Top**      |
| [**Last-Known-Parent**](a-lastknownparent.md)                            | False     | **Top**      |
| [**Verwaltete Objekte**](a-managedobjects.md)                               | False     | **Top**      |
| [**Mastered-By**](a-masteredby.md)                                       | False     | **Top**      |
| [**Modify-Time-Stamp**](a-modifytimestamp.md)                            | False     | **Top**      |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)    | False     | **Top**      |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                 | False     | **Top**      |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                  | False     | **Top**      |
| [**Non-Security-Member-BL**](a-nonsecuritymemberbl.md)                   | False     | **Top**      |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                  | True      | **Top**      |
| [**Obj-Dist-Name**](a-distinguishedname.md)                              | False     | **Top**      |
| [**Objektkategorie**](a-objectcategory.md)                               | True      | **Top**      |
| [**Objektklasse**](a-objectclass.md)                                     | True      | **Top**      |
| [**Objekt-GUID**](a-objectguid.md)                                       | False     | **Top**      |
| [**Objektversion**](a-objectversion.md)                                 | False     | **Top**      |
| [**Andere bekannte Objekte**](a-otherwellknownobjects.md)               | False     | **Top**      |
| [**Teilattributlöschungsliste**](a-partialattributedeletionlist.md) | False     | **Top**      |
| [**Teilattributsatz**](a-partialattributeset.md)                    | False     | **Top**      |
| [**Mögliche Hindernisse**](a-possibleinferiors.md)                         | False     | **Top**      |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                        | False     | **Top**      |
| [**Proxyadressen**](a-proxyaddresses.md)                               | False     | **Top**      |
| [**Query-Policy-BL**](a-querypolicybl.md)                                | False     | **Top**      |
| [**Rdn**](a-name.md)                                                     | False     | **Top**      |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                 | False     | **Top**      |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                      | False     | **Top**      |
| [**Berichte**](a-directreports.md)                                        | False     | **Top**      |
| [**Reps-From**](a-repsfrom.md)                                           | False     | **Top**      |
| [**Reps-To**](a-repsto.md)                                               | False     | **Top**      |
| [**Revision**](a-revision.md)                                            | False     | **Top**      |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                        | False     | **Top**      |
| [**Server-Reference-BL**](a-serverreferencebl.md)                        | False     | **Top**      |
| [**Nur in erweiterter Ansicht anzeigen**](a-showinadvancedviewonly.md)            | False     | **Top**      |
| [**Site-Object-BL**](a-siteobjectbl.md)                                  | False     | **Top**      |
| [**Sub-Refs**](a-subrefs.md)                                             | False     | **Top**      |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                          | False     | **Top**      |
| [**Systemflags**](a-systemflags.md)                                     | False     | **Top**      |
| [**USN geändert**](a-usnchanged.md)                                       | False     | **Top**      |
| [**USN-erstellt**](a-usncreated.md)                                       | False     | **Top**      |
| [**USN-DSA-last-obj-removed**](a-usndsalastobjremoved.md)                | False     | **Top**      |
| [**USN-Intersite**](a-usnintersite.md)                                   | False     | **Top**      |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                               | False     | **Top**      |
| [**USN-Quelle**](a-usnsource.md)                                         | False     | **Top**      |
| [**Wbem-Pfad**](a-wbempath.md)                                           | False     | **Top**      |
| [**Bekannte Objekte**](a-wellknownobjects.md)                          | False     | **Top**      |
| [**Bei Änderung**](a-whenchanged.md)                                     | False     | **Top**      |
| [**Bei der Erstellung**](a-whencreated.md)                                     | False     | **Top**      |
| [**WWW-Startseite**](a-wwwhomepage.md)                                    | False     | **Top**      |
| [**WWW-Page-Other**](a-url.md)                                           | False     | **Top**      |



## <a name="windows-server-2003"></a>Windows Server 2003

-   [Attribute](#windows-server-2003-attributes)



| Eingabe | Wert |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | True                                                                                         |
| Object-Category             | 2                                                                                            |
| Default-Object-Category     | \-                                                                                           |
| Governs-Id                  | 2.5.6.0                                                                                      |
| Default-Hiding-Value        | 1                                                                                            |
| Rdn-Att-Id                  | [**Allgemeiner Name**](a-cn.md)<br/>                                                       |
| Unterklasse von                 | **Top**<br/>                                                                           |
| Mögliche Übergeordnete          | [**Verloren gegangen und gefunden**](c-lostandfound.md)                                                     |
| Zusätzlich           | \-                                                                                           |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                 |
| Standardsicherheitsdeskriptor | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;;; AU) |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2003-attributes"></a>Windows Server 2003-Attribute

Diese Klasse enthält die folgenden Attribute für Windows Server 2003:



| attribute                                                                   | Obligatorisch. | Abgeleitet von |
|-----------------------------------------------------------------------------|-----------|--------------|
| [**Admin-Description**](a-admindescription.md)                             | False     | **Top**      |
| [**Administratoranzeigename**](a-admindisplayname.md)                            | False     | **Top**      |
| [**Allowed-Attributes**](a-allowedattributes.md)                           | False     | **Top**      |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)        | False     | **Top**      |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                      | False     | **Top**      |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)   | False     | **Top**      |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)               | False     | **Top**      |
| [**Kanonischer Name**](a-canonicalname.md)                                   | False     | **Top**      |
| [**Common-Name**](a-cn.md)                                                 | False     | **Top**      |
| [**Create-Time-Stamp**](a-createtimestamp.md)                              | False     | **Top**      |
| [**Beschreibung**](a-description.md)                                        | False     | **Top**      |
| [**Anzeigename**](a-displayname.md)                                       | False     | **Top**      |
| [**Display-Name-Printable**](a-displaynameprintable.md)                    | False     | **Top**      |
| [**DSA-Signature**](a-dsasignature.md)                                     | False     | **Top**      |
| [**DS-Core-Propagierungsdaten**](a-dscorepropagationdata.md)                 | False     | **Top**      |
| [**Extension-Name**](a-extensionname.md)                                   | False     | **Top**      |
| [**Flaggen**](a-flags.md)                                                    | False     | **Top**      |
| [**From-Entry**](a-fromentry.md)                                           | False     | **Top**      |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)               | False     | **Top**      |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                   | False     | **Top**      |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                  | False     | **Top**      |
| [**Instanztyp**](a-instancetype.md)                                     | True      | **Top**      |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)               | False     | **Top**      |
| [**Is-Deleted**](a-isdeleted.md)                                           | False     | **Top**      |
| [**Is-Member-of-DL**](a-memberof.md)                                       | False     | **Top**      |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                          | False     | **Top**      |
| [**Letztes bekanntes übergeordnetes Element**](a-lastknownparent.md)                              | False     | **Top**      |
| [**Verwaltete Objekte**](a-managedobjects.md)                                 | False     | **Top**      |
| [**Mastered By**](a-masteredby.md)                                         | False     | **Top**      |
| [**Modify-Time-Stamp**](a-modifytimestamp.md)                              | False     | **Top**      |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                 | False     | **Top**      |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                 | False     | **Top**      |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md) | False     | **Top**      |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)      | False     | **Top**      |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | False     | **Top**      |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                              | False     | **Top**      |
| [**ms-DS-Members-for-Az-Role-BL**](a-msds-membersforazrolebl.md)           | False     | **Top**      |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                       | False     | **Top**      |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)    | False     | **Top**      |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)  | False     | **Top**      |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                         | False     | **Top**      |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)               | False     | **Top**      |
| [**ms-DS-Operations-for-Az-Role-BL**](a-msds-operationsforazrolebl.md)     | False     | **Top**      |
| [**ms-DS-Operations-for-Az-Task-BL**](a-msds-operationsforaztaskbl.md)     | False     | **Top**      |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)      | False     | **Top**      |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)              | False     | **Top**      |
| [**ms-DS-Tasks-for-Az-Role-BL**](a-msds-tasksforazrolebl.md)               | False     | **Top**      |
| [**ms-DS-Tasks-for-Az-Task-BL**](a-msds-tasksforaztaskbl.md)               | False     | **Top**      |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                       | False     | **Top**      |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                    | False     | **Top**      |
| [**Non-Security-Member-BL**](a-nonsecuritymemberbl.md)                     | False     | **Top**      |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                    | True      | **Top**      |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                | False     | **Top**      |
| [**Objektkategorie**](a-objectcategory.md)                                 | True      | **Top**      |
| [**Objektklasse**](a-objectclass.md)                                       | True      | **Top**      |
| [**Objekt-GUID**](a-objectguid.md)                                         | False     | **Top**      |
| [**Objektversion**](a-objectversion.md)                                   | False     | **Top**      |
| [**Andere bekannte Objekte**](a-otherwellknownobjects.md)                 | False     | **Top**      |
| [**Teilattributlöschungsliste**](a-partialattributedeletionlist.md)   | False     | **Top**      |
| [**Teilattributsatz**](a-partialattributeset.md)                      | False     | **Top**      |
| [**Mögliche Hindernisse**](a-possibleinferiors.md)                           | False     | **Top**      |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                          | False     | **Top**      |
| [**Proxyadressen**](a-proxyaddresses.md)                                 | False     | **Top**      |
| [**Query-Policy-BL**](a-querypolicybl.md)                                  | False     | **Top**      |
| [**Rdn**](a-name.md)                                                       | False     | **Top**      |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                   | False     | **Top**      |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                        | False     | **Top**      |
| [**Berichte**](a-directreports.md)                                          | False     | **Top**      |
| [**Reps-From**](a-repsfrom.md)                                             | False     | **Top**      |
| [**Reps-To**](a-repsto.md)                                                 | False     | **Top**      |
| [**Revision**](a-revision.md)                                              | False     | **Top**      |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                          | False     | **Top**      |
| [**Server-Reference-BL**](a-serverreferencebl.md)                          | False     | **Top**      |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)              | False     | **Top**      |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | False     | **Top**      |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                  | False     | **Top**      |
| [**Sub-Refs**](a-subrefs.md)                                               | False     | **Top**      |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | False     | **Top**      |
| [**Systemflags**](a-systemflags.md)                                       | False     | **Top**      |
| [**USN-Changed**](a-usnchanged.md)                                         | False     | **Top**      |
| [**VON USN erstellt**](a-usncreated.md)                                         | False     | **Top**      |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                  | False     | **Top**      |
| [**USN-Intersite**](a-usnintersite.md)                                     | False     | **Top**      |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                 | False     | **Top**      |
| [**USN-Quelle**](a-usnsource.md)                                           | False     | **Top**      |
| [**Wbem-Path**](a-wbempath.md)                                             | False     | **Top**      |
| [**Bekannte Objekte**](a-wellknownobjects.md)                            | False     | **Top**      |
| [**Wenn geändert**](a-whenchanged.md)                                       | False     | **Top**      |
| [**Wenn erstellt**](a-whencreated.md)                                       | False     | **Top**      |
| [**WWW-Homepage**](a-wwwhomepage.md)                                      | False     | **Top**      |
| [**WWW-Page-Other**](a-url.md)                                             | False     | **Top**      |



## <a name="adam"></a>Adam

-   [Attribute](#adam-attributes)



| Eingabe | Wert |
|-----------------------------|------------------------------------------|
| System-Only                 | True                                     |
| Object-Category             | 2                                        |
| Default-Object-Category     | \-                                       |
| Governs-Id                  | 2.5.6.0                                  |
| Default-Hiding-Value        | 1                                        |
| Rdn-Att-Id                  | [**Common-Name**](a-cn.md)<br/>   |
| Unterklasse von                 | **Top**<br/>                       |
| Mögliche Vorgesetzte          | [**Lost-and-Found**](c-lostandfound.md) |
| Zusätzlich           | \-                                       |
| NT-Security-Descriptor      | O:BAG:BAD:S:                             |
| Standardsicherheitsdeskriptor | D:S:                                     |
| System-Flags                | 0x00000010                               |



## <a name="adam-attributes"></a>ADAM-Attribute

Diese Klasse enthält die folgenden Attribute für ADAM:



| attribute                                                                   | Obligatorisch. | Abgeleitet von |
|-----------------------------------------------------------------------------|-----------|--------------|
| [**Admin-Description**](a-admindescription.md)                             | False     | **Top**      |
| [**Administratoranzeigename**](a-admindisplayname.md)                            | False     | **Top**      |
| [**Allowed-Attributes**](a-allowedattributes.md)                           | False     | **Top**      |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)        | False     | **Top**      |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                      | False     | **Top**      |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)   | False     | **Top**      |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)               | False     | **Top**      |
| [**Kanonischer Name**](a-canonicalname.md)                                   | False     | **Top**      |
| [**Common-Name**](a-cn.md)                                                 | False     | **Top**      |
| [**Create-Time-Stamp**](a-createtimestamp.md)                              | False     | **Top**      |
| [**Beschreibung**](a-description.md)                                        | False     | **Top**      |
| [**Anzeigename**](a-displayname.md)                                       | False     | **Top**      |
| [**DSA-Signature**](a-dsasignature.md)                                     | False     | **Top**      |
| [**DS-Core-Propagierungsdaten**](a-dscorepropagationdata.md)                 | False     | **Top**      |
| [**From-Entry**](a-fromentry.md)                                           | False     | **Top**      |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                  | False     | **Top**      |
| [**Instanztyp**](a-instancetype.md)                                     | True      | **Top**      |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)               | False     | **Top**      |
| [**Is-Deleted**](a-isdeleted.md)                                           | False     | **Top**      |
| [**Is-Member-of-DL**](a-memberof.md)                                       | False     | **Top**      |
| [**Letztes bekanntes übergeordnetes Element**](a-lastknownparent.md)                              | False     | **Top**      |
| [**Verwaltete Objekte**](a-managedobjects.md)                                 | False     | **Top**      |
| [**Mastered By**](a-masteredby.md)                                         | False     | **Top**      |
| [**Modify-Time-Stamp**](a-modifytimestamp.md)                              | False     | **Top**      |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md) | False     | **Top**      |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)      | False     | **Top**      |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | False     | **Top**      |
| [**ms-DS-Disable-For-Instances-BL**](a-msds-disableforinstancesbl.md)      | False     | **Top**      |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                              | False     | **Top**      |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                       | False     | **Top**      |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)    | False     | **Top**      |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)  | False     | **Top**      |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)      | False     | **Top**      |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)              | False     | **Top**      |
| [**ms-DS-Service-Account-BL**](a-msds-serviceaccountbl.md)                 | False     | **Top**      |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                    | True      | **Top**      |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                | False     | **Top**      |
| [**Objektkategorie**](a-objectcategory.md)                                 | True      | **Top**      |
| [**Object-Class**](a-objectclass.md)                                       | True      | **Top**      |
| [**Objekt-GUID**](a-objectguid.md)                                         | False     | **Top**      |
| [**Object-Version**](a-objectversion.md)                                   | False     | **Top**      |
| [**Andere bekannte Objekte**](a-otherwellknownobjects.md)                 | False     | **Top**      |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)   | False     | **Top**      |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                      | False     | **Top**      |
| [**Mögliche 100000000000**](a-possibleinferiors.md)                           | False     | **Top**      |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                          | False     | **Top**      |
| [**Proxyadressen**](a-proxyaddresses.md)                                 | False     | **Top**      |
| [**Query-Policy-BL**](a-querypolicybl.md)                                  | False     | **Top**      |
| [**Rdn**](a-name.md)                                                       | False     | **Top**      |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                   | False     | **Top**      |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                        | False     | **Top**      |
| [**Reps-From**](a-repsfrom.md)                                             | False     | **Top**      |
| [**Reps-To**](a-repsto.md)                                                 | False     | **Top**      |
| [**Revision**](a-revision.md)                                              | False     | **Top**      |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                          | False     | **Top**      |
| [**Server-Reference-BL**](a-serverreferencebl.md)                          | False     | **Top**      |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)              | False     | **Top**      |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | False     | **Top**      |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                  | False     | **Top**      |
| [**Sub-Refs**](a-subrefs.md)                                               | False     | **Top**      |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | False     | **Top**      |
| [**Systemflags**](a-systemflags.md)                                       | False     | **Top**      |
| [**USN-Changed**](a-usnchanged.md)                                         | False     | **Top**      |
| [**VON USN erstellt**](a-usncreated.md)                                         | False     | **Top**      |
| [**USN-DSA-last-obj-removed**](a-usndsalastobjremoved.md)                  | False     | **Top**      |
| [**USN-Intersite**](a-usnintersite.md)                                     | False     | **Top**      |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                 | False     | **Top**      |
| [**USN-Quelle**](a-usnsource.md)                                           | False     | **Top**      |
| [**Wbem-Pfad**](a-wbempath.md)                                             | False     | **Top**      |
| [**Bekannte Objekte**](a-wellknownobjects.md)                            | False     | **Top**      |
| [**Bei Änderung**](a-whenchanged.md)                                       | False     | **Top**      |
| [**Bei der Erstellung**](a-whencreated.md)                                       | False     | **Top**      |
| [**WWW-Startseite**](a-wwwhomepage.md)                                      | False     | **Top**      |
| [**WWW-Page-Other**](a-url.md)                                             | False     | **Top**      |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2

-   [Attribute](#windows-server-2003-r2-attributes)



| Eingabe | Wert |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | True                                                                                         |
| Object-Category             | 2                                                                                            |
| Default-Object-Category     | \-                                                                                           |
| Governs-Id                  | 2.5.6.0                                                                                      |
| Default-Hiding-Value        | 1                                                                                            |
| Rdn-Att-Id                  | [**Allgemeiner Name**](a-cn.md)<br/>                                                       |
| Unterklasse von                 | **Top**<br/>                                                                           |
| Mögliche Übergeordnete          | [**Verloren gegangen und gefunden**](c-lostandfound.md)                                                     |
| Zusätzlich           | \-                                                                                           |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                 |
| Standardsicherheitsdeskriptor | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;;; AU) |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2003-r2-attributes"></a>Windows Server 2003 R2-Attribute

Diese Klasse enthält die folgenden Attribute für Windows Server 2003 R2:



| attribute                                                                   | Obligatorisch. | Abgeleitet von |
|-----------------------------------------------------------------------------|-----------|--------------|
| [**Administratorbeschreibung**](a-admindescription.md)                             | False     | **Top**      |
| [**Admin-Display-Name**](a-admindisplayname.md)                            | False     | **Top**      |
| [**Allowed-Attributes**](a-allowedattributes.md)                           | False     | **Top**      |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)        | False     | **Top**      |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                      | False     | **Top**      |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)   | False     | **Top**      |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)               | False     | **Top**      |
| [**Kanonischer Name**](a-canonicalname.md)                                   | False     | **Top**      |
| [**Allgemeiner Name**](a-cn.md)                                                 | False     | **Top**      |
| [**Erstellen eines Zeitstempels**](a-createtimestamp.md)                              | False     | **Top**      |
| [**Beschreibung**](a-description.md)                                        | False     | **Top**      |
| [**Anzeigename**](a-displayname.md)                                       | False     | **Top**      |
| [**Anzeigename– druckbar**](a-displaynameprintable.md)                    | False     | **Top**      |
| [**DSA-Signature**](a-dsasignature.md)                                     | False     | **Top**      |
| [**DS-Core-Propagierungsdaten**](a-dscorepropagationdata.md)                 | False     | **Top**      |
| [**Erweiterungsname**](a-extensionname.md)                                   | False     | **Top**      |
| [**Flaggen**](a-flags.md)                                                    | False     | **Top**      |
| [**From-Entry**](a-fromentry.md)                                           | False     | **Top**      |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)               | False     | **Top**      |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                   | False     | **Top**      |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                  | False     | **Top**      |
| [**Instanztyp**](a-instancetype.md)                                     | True      | **Top**      |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)               | False     | **Top**      |
| [**Is-Deleted**](a-isdeleted.md)                                           | False     | **Top**      |
| [**Is-Member-of-DL**](a-memberof.md)                                       | False     | **Top**      |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                          | False     | **Top**      |
| [**Last-Known-Parent**](a-lastknownparent.md)                              | False     | **Top**      |
| [**Verwaltete Objekte**](a-managedobjects.md)                                 | False     | **Top**      |
| [**Mastered-By**](a-masteredby.md)                                         | False     | **Top**      |
| [**Modify-Time-Stamp**](a-modifytimestamp.md)                              | False     | **Top**      |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                 | False     | **Top**      |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                 | False     | **Top**      |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)         | False     | **Top**      |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)             | False     | **Top**      |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md) | False     | **Top**      |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)      | False     | **Top**      |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | False     | **Top**      |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                              | False     | **Top**      |
| [**ms-DS-Members-for-Az-Role-BL**](a-msds-membersforazrolebl.md)           | False     | **Top**      |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                       | False     | **Top**      |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)    | False     | **Top**      |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)  | False     | **Top**      |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                         | False     | **Top**      |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)               | False     | **Top**      |
| [**ms-DS-Operations-for-Az-Role-BL**](a-msds-operationsforazrolebl.md)     | False     | **Top**      |
| [**ms-DS-Operations-for-Az-Task-BL**](a-msds-operationsforaztaskbl.md)     | False     | **Top**      |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)      | False     | **Top**      |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)              | False     | **Top**      |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)               | False     | **Top**      |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)               | False     | **Top**      |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                       | False     | **Top**      |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                  | False     | **Top**      |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                    | False     | **Top**      |
| [**Non-Security-Member-BL**](a-nonsecuritymemberbl.md)                     | False     | **Top**      |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                    | True      | **Top**      |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                | False     | **Top**      |
| [**Objektkategorie**](a-objectcategory.md)                                 | True      | **Top**      |
| [**Object-Class**](a-objectclass.md)                                       | True      | **Top**      |
| [**Objekt-GUID**](a-objectguid.md)                                         | False     | **Top**      |
| [**Object-Version**](a-objectversion.md)                                   | False     | **Top**      |
| [**Andere bekannte Objekte**](a-otherwellknownobjects.md)                 | False     | **Top**      |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)   | False     | **Top**      |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                      | False     | **Top**      |
| [**Mögliche 100000000000**](a-possibleinferiors.md)                           | False     | **Top**      |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                          | False     | **Top**      |
| [**Proxyadressen**](a-proxyaddresses.md)                                 | False     | **Top**      |
| [**Query-Policy-BL**](a-querypolicybl.md)                                  | False     | **Top**      |
| [**Rdn**](a-name.md)                                                       | False     | **Top**      |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                   | False     | **Top**      |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                        | False     | **Top**      |
| [**Berichte**](a-directreports.md)                                          | False     | **Top**      |
| [**Reps-From**](a-repsfrom.md)                                             | False     | **Top**      |
| [**Reps-To**](a-repsto.md)                                                 | False     | **Top**      |
| [**Revision**](a-revision.md)                                              | False     | **Top**      |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                          | False     | **Top**      |
| [**Server-Reference-BL**](a-serverreferencebl.md)                          | False     | **Top**      |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)              | False     | **Top**      |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | False     | **Top**      |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                  | False     | **Top**      |
| [**Sub-Refs**](a-subrefs.md)                                               | False     | **Top**      |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | False     | **Top**      |
| [**Systemflags**](a-systemflags.md)                                       | False     | **Top**      |
| [**USN geändert**](a-usnchanged.md)                                         | False     | **Top**      |
| [**USN-erstellt**](a-usncreated.md)                                         | False     | **Top**      |
| [**USN-DSA-last-obj-removed**](a-usndsalastobjremoved.md)                  | False     | **Top**      |
| [**USN-Intersite**](a-usnintersite.md)                                     | False     | **Top**      |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                 | False     | **Top**      |
| [**USN-Quelle**](a-usnsource.md)                                           | False     | **Top**      |
| [**Wbem-Pfad**](a-wbempath.md)                                             | False     | **Top**      |
| [**Bekannte Objekte**](a-wellknownobjects.md)                            | False     | **Top**      |
| [**Bei Änderung**](a-whenchanged.md)                                       | False     | **Top**      |
| [**Bei der Erstellung**](a-whencreated.md)                                       | False     | **Top**      |
| [**WWW-Startseite**](a-wwwhomepage.md)                                      | False     | **Top**      |
| [**WWW-Page-Other**](a-url.md)                                             | False     | **Top**      |



## <a name="windows-server-2008"></a>Windows Server 2008

-   [Attribute](#windows-server-2008-attributes)



| Eingabe | Wert |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | True                                                                                         |
| Object-Category             | 2                                                                                            |
| Default-Object-Category     | \-                                                                                           |
| Governs-Id                  | 2.5.6.0                                                                                      |
| Default-Hiding-Value        | 1                                                                                            |
| Rdn-Att-Id                  | [**Allgemeiner Name**](a-cn.md)<br/>                                                       |
| Unterklasse von                 | **Top**<br/>                                                                           |
| Mögliche Übergeordnete          | [**Verloren gegangen und gefunden**](c-lostandfound.md)                                                     |
| Zusätzlich           | \-                                                                                           |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                 |
| Standardsicherheitsdeskriptor | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;;; AU) |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2008-attributes"></a>Windows Server 2008-Attribute

Diese Klasse enthält die folgenden Attribute für Windows Server 2008:



| attribute                                                                      | Obligatorisch. | Abgeleitet von |
|--------------------------------------------------------------------------------|-----------|--------------|
| [**Administratorbeschreibung**](a-admindescription.md)                                | False     | **Top**      |
| [**Admin-Display-Name**](a-admindisplayname.md)                               | False     | **Top**      |
| [**Allowed-Attributes**](a-allowedattributes.md)                              | False     | **Top**      |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)           | False     | **Top**      |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                         | False     | **Top**      |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)      | False     | **Top**      |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                  | False     | **Top**      |
| [**Kanonischer Name**](a-canonicalname.md)                                      | False     | **Top**      |
| [**Common-Name**](a-cn.md)                                                    | False     | **Top**      |
| [**Create-Time-Stamp**](a-createtimestamp.md)                                 | False     | **Top**      |
| [**Beschreibung**](a-description.md)                                           | False     | **Top**      |
| [**Anzeigename**](a-displayname.md)                                          | False     | **Top**      |
| [**Display-Name-Printable**](a-displaynameprintable.md)                       | False     | **Top**      |
| [**DSA-Signature**](a-dsasignature.md)                                        | False     | **Top**      |
| [**DS-Core-Propagierungsdaten**](a-dscorepropagationdata.md)                    | False     | **Top**      |
| [**Extension-Name**](a-extensionname.md)                                      | False     | **Top**      |
| [**Flaggen**](a-flags.md)                                                       | False     | **Top**      |
| [**From-Entry**](a-fromentry.md)                                              | False     | **Top**      |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)                  | False     | **Top**      |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                      | False     | **Top**      |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                     | False     | **Top**      |
| [**Instanztyp**](a-instancetype.md)                                        | True      | **Top**      |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                  | False     | **Top**      |
| [**Is-Deleted**](a-isdeleted.md)                                              | False     | **Top**      |
| [**Is-Member-of-DL**](a-memberof.md)                                          | False     | **Top**      |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                             | False     | **Top**      |
| [**Letztes bekanntes übergeordnetes Element**](a-lastknownparent.md)                                 | False     | **Top**      |
| [**Verwaltete Objekte**](a-managedobjects.md)                                    | False     | **Top**      |
| [**Mastered By**](a-masteredby.md)                                            | False     | **Top**      |
| [**Modify-Time-Stamp**](a-modifytimestamp.md)                                 | False     | **Top**      |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                    | False     | **Top**      |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                    | False     | **Top**      |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)            | False     | **Top**      |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                | False     | **Top**      |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md)    | False     | **Top**      |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md) | False     | **Top**      |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)         | False     | **Top**      |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                      | False     | **Top**      |
| [**ms-DS-is-Domain-for**](a-msds-isdomainfor.md)                              | False     | **Top**      |
| [**ms-DS-is-full-replica-for**](a-msds-isfullreplicafor.md)                   | False     | **Top**      |
| [**ms-DS-is-partial-replica-for**](a-msds-ispartialreplicafor.md)             | False     | **Top**      |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                            | False     | **Top**      |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                                 | False     | **Top**      |
| [**ms-DS-Members-For-Az-Role-BL**](a-msds-membersforazrolebl.md)              | False     | **Top**      |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                          | False     | **Top**      |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)       | False     | **Top**      |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)     | False     | **Top**      |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)  | False     | **Top**      |
| [**ms-DS-NC-Type**](a-msds-nctype.md)                                         | False     | **Top**      |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                            | False     | **Top**      |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                  | False     | **Top**      |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)        | False     | **Top**      |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)        | False     | **Top**      |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                           | False     | **Top**      |
| [**ms-DS-PSO-Applied**](a-msds-psoapplied.md)                                 | False     | **Top**      |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)         | False     | **Top**      |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                 | False     | **Top**      |
| [**ms-DS-Revealed-DSAs**](a-msds-revealeddsas.md)                             | False     | **Top**      |
| [**ms-DS-Revealed-List-BL**](a-msds-revealedlistbl.md)                        | False     | **Top**      |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)                  | False     | **Top**      |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)                  | False     | **Top**      |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                          | False     | **Top**      |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                     | False     | **Top**      |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                       | False     | **Top**      |
| [**Non-Security-Member-BL**](a-nonsecuritymemberbl.md)                        | False     | **Top**      |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                       | True      | **Top**      |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                   | False     | **Top**      |
| [**Objektkategorie**](a-objectcategory.md)                                    | True      | **Top**      |
| [**Object-Class**](a-objectclass.md)                                          | True      | **Top**      |
| [**Objekt-GUID**](a-objectguid.md)                                            | False     | **Top**      |
| [**Object-Version**](a-objectversion.md)                                      | False     | **Top**      |
| [**Andere bekannte Objekte**](a-otherwellknownobjects.md)                    | False     | **Top**      |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)      | False     | **Top**      |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                         | False     | **Top**      |
| [**Mögliche 100000000000**](a-possibleinferiors.md)                              | False     | **Top**      |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                             | False     | **Top**      |
| [**Proxyadressen**](a-proxyaddresses.md)                                    | False     | **Top**      |
| [**Query-Policy-BL**](a-querypolicybl.md)                                     | False     | **Top**      |
| [**Rdn**](a-name.md)                                                          | False     | **Top**      |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                      | False     | **Top**      |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                           | False     | **Top**      |
| [**Berichte**](a-directreports.md)                                             | False     | **Top**      |
| [**Reps-From**](a-repsfrom.md)                                                | False     | **Top**      |
| [**Reps-To**](a-repsto.md)                                                    | False     | **Top**      |
| [**Revision**](a-revision.md)                                                 | False     | **Top**      |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                             | False     | **Top**      |
| [**Server-Reference-BL**](a-serverreferencebl.md)                             | False     | **Top**      |
| [**Nur in erweiterter Ansicht anzeigen**](a-showinadvancedviewonly.md)                 | False     | **Top**      |
| [**Site-Object-BL**](a-siteobjectbl.md)                                       | False     | **Top**      |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                     | False     | **Top**      |
| [**Sub-Refs**](a-subrefs.md)                                                  | False     | **Top**      |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                               | False     | **Top**      |
| [**Systemflags**](a-systemflags.md)                                          | False     | **Top**      |
| [**USN geändert**](a-usnchanged.md)                                            | False     | **Top**      |
| [**USN-erstellt**](a-usncreated.md)                                            | False     | **Top**      |
| [**USN-DSA-last-obj-removed**](a-usndsalastobjremoved.md)                     | False     | **Top**      |
| [**USN-Intersite**](a-usnintersite.md)                                        | False     | **Top**      |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                    | False     | **Top**      |
| [**USN-Quelle**](a-usnsource.md)                                              | False     | **Top**      |
| [**Wbem-Pfad**](a-wbempath.md)                                                | False     | **Top**      |
| [**Bekannte Objekte**](a-wellknownobjects.md)                               | False     | **Top**      |
| [**Bei Änderung**](a-whenchanged.md)                                          | False     | **Top**      |
| [**Bei der Erstellung**](a-whencreated.md)                                          | False     | **Top**      |
| [**WWW-Startseite**](a-wwwhomepage.md)                                         | False     | **Top**      |
| [**WWW-Page-Other**](a-url.md)                                                | False     | **Top**      |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2

-   [Attribute](#windows-server-2008-r2-attributes)



| Eingabe | Wert |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | True                                                                                         |
| Object-Category             | 2                                                                                            |
| Default-Object-Category     | \-                                                                                           |
| Governs-Id                  | 2.5.6.0                                                                                      |
| Default-Hiding-Value        | 1                                                                                            |
| Rdn-Att-Id                  | [**Common-Name**](a-cn.md)<br/>                                                       |
| Unterklasse von                 | **Top**<br/>                                                                           |
| Mögliche Vorgesetzte          | [**Lost-and-Found**](c-lostandfound.md)                                                     |
| Zusätzlich           | \-                                                                                           |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                 |
| Standardsicherheitsdeskriptor | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;;; AU) |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2008-r2-attributes"></a>Windows Server 2008 R2-Attribute

Diese Klasse enthält die folgenden Attribute für Windows Server 2008 R2:



| attribute                                                                        | Obligatorisch. | Abgeleitet von |
|----------------------------------------------------------------------------------|-----------|--------------|
| [**Admin-Description**](a-admindescription.md)                                  | False     | **Top**      |
| [**Administratoranzeigename**](a-admindisplayname.md)                                 | False     | **Top**      |
| [**Allowed-Attributes**](a-allowedattributes.md)                                | False     | **Top**      |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)             | False     | **Top**      |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                           | False     | **Top**      |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)        | False     | **Top**      |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                    | False     | **Top**      |
| [**Kanonischer Name**](a-canonicalname.md)                                        | False     | **Top**      |
| [**Common-Name**](a-cn.md)                                                      | False     | **Top**      |
| [**Create-Time-Stamp**](a-createtimestamp.md)                                   | False     | **Top**      |
| [**Beschreibung**](a-description.md)                                             | False     | **Top**      |
| [**Anzeigename**](a-displayname.md)                                            | False     | **Top**      |
| [**Display-Name-Printable**](a-displaynameprintable.md)                         | False     | **Top**      |
| [**DSA-Signature**](a-dsasignature.md)                                          | False     | **Top**      |
| [**DS-Core-Propagierungsdaten**](a-dscorepropagationdata.md)                      | False     | **Top**      |
| [**Extension-Name**](a-extensionname.md)                                        | False     | **Top**      |
| [**Flaggen**](a-flags.md)                                                         | False     | **Top**      |
| [**From-Entry**](a-fromentry.md)                                                | False     | **Top**      |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)                    | False     | **Top**      |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                        | False     | **Top**      |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                       | False     | **Top**      |
| [**Instanztyp**](a-instancetype.md)                                          | True      | **Top**      |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                    | False     | **Top**      |
| [**Is-Deleted**](a-isdeleted.md)                                                | False     | **Top**      |
| [**Is-Member-of-DL**](a-memberof.md)                                            | False     | **Top**      |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                               | False     | **Top**      |
| [**Wird wiederverwendet**](a-isrecycled.md)                                              | False     | **Top**      |
| [**Letztes bekanntes übergeordnetes Element**](a-lastknownparent.md)                                   | False     | **Top**      |
| [**Verwaltete Objekte**](a-managedobjects.md)                                      | False     | **Top**      |
| [**Mastered By**](a-masteredby.md)                                              | False     | **Top**      |
| [**Modify-Time-Stamp**](a-modifytimestamp.md)                                   | False     | **Top**      |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                      | False     | **Top**      |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                      | False     | **Top**      |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)              | False     | **Top**      |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                  | False     | **Top**      |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md)      | False     | **Top**      |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md)   | False     | **Top**      |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)           | False     | **Top**      |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                        | False     | **Top**      |
| [**ms-DS-Enabled-Feature-BL**](a-msds-enabledfeaturebl.md)                      | False     | **Top**      |
| [**ms-DS-Host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)             | False     | **Top**      |
| [**ms-DS-is-Domain-for**](a-msds-isdomainfor.md)                                | False     | **Top**      |
| [**ms-DS-is-full-replica-for**](a-msds-isfullreplicafor.md)                     | False     | **Top**      |
| [**ms-DS-is-partial-replica-for**](a-msds-ispartialreplicafor.md)               | False     | **Top**      |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                              | False     | **Top**      |
| [**ms-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                              | False     | **Top**      |
| [**ms-DS-local-Effective-Deletion-Time**](a-msds-localeffectivedeletiontime.md) | False     | **Top**      |
| [**ms-DS-local-Effective-Recycle-Time**](a-msds-localeffectiverecycletime.md)   | False     | **Top**      |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                                   | False     | **Top**      |
| [**ms-DS-Members-For-Az-Role-BL**](a-msds-membersforazrolebl.md)                | False     | **Top**      |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                            | False     | **Top**      |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)         | False     | **Top**      |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)       | False     | **Top**      |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)    | False     | **Top**      |
| [**ms-DS-NC-Type**](a-msds-nctype.md)                                           | False     | **Top**      |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                              | False     | **Top**      |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                    | False     | **Top**      |
| [**ms-DS-OIDToGroup-Link-BL**](a-msds-oidtogrouplinkbl.md)                      | False     | **Top**      |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)          | False     | **Top**      |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)          | False     | **Top**      |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                             | False     | **Top**      |
| [**ms-DS-PSO-Applied**](a-msds-psoapplied.md)                                   | False     | **Top**      |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)           | False     | **Top**      |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                   | False     | **Top**      |
| [**ms-DS-Revealed-DSAs**](a-msds-revealeddsas.md)                               | False     | **Top**      |
| [**ms-DS-Revealed-List-BL**](a-msds-revealedlistbl.md)                          | False     | **Top**      |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)                    | False     | **Top**      |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)                    | False     | **Top**      |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                            | False     | **Top**      |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                       | False     | **Top**      |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                         | False     | **Top**      |
| [**Non-Security-Member-BL**](a-nonsecuritymemberbl.md)                          | False     | **Top**      |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                         | True      | **Top**      |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                     | False     | **Top**      |
| [**Objektkategorie**](a-objectcategory.md)                                      | True      | **Top**      |
| [**Object-Class**](a-objectclass.md)                                            | True      | **Top**      |
| [**Objekt-GUID**](a-objectguid.md)                                              | False     | **Top**      |
| [**Object-Version**](a-objectversion.md)                                        | False     | **Top**      |
| [**Andere bekannte Objekte**](a-otherwellknownobjects.md)                      | False     | **Top**      |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)        | False     | **Top**      |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                           | False     | **Top**      |
| [**Mögliche 100000000000**](a-possibleinferiors.md)                                | False     | **Top**      |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                               | False     | **Top**      |
| [**Proxyadressen**](a-proxyaddresses.md)                                      | False     | **Top**      |
| [**Query-Policy-BL**](a-querypolicybl.md)                                       | False     | **Top**      |
| [**Rdn**](a-name.md)                                                            | False     | **Top**      |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                        | False     | **Top**      |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                             | False     | **Top**      |
| [**Berichte**](a-directreports.md)                                               | False     | **Top**      |
| [**Reps-From**](a-repsfrom.md)                                                  | False     | **Top**      |
| [**Reps-To**](a-repsto.md)                                                      | False     | **Top**      |
| [**Revision**](a-revision.md)                                                   | False     | **Top**      |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                               | False     | **Top**      |
| [**Server-Reference-BL**](a-serverreferencebl.md)                               | False     | **Top**      |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)                   | False     | **Top**      |
| [**Site-Object-BL**](a-siteobjectbl.md)                                         | False     | **Top**      |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                       | False     | **Top**      |
| [**Sub-Refs**](a-subrefs.md)                                                    | False     | **Top**      |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                 | False     | **Top**      |
| [**Systemflags**](a-systemflags.md)                                            | False     | **Top**      |
| [**USN-Changed**](a-usnchanged.md)                                              | False     | **Top**      |
| [**VON USN erstellt**](a-usncreated.md)                                              | False     | **Top**      |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                       | False     | **Top**      |
| [**USN-Intersite**](a-usnintersite.md)                                          | False     | **Top**      |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                      | False     | **Top**      |
| [**USN-Quelle**](a-usnsource.md)                                                | False     | **Top**      |
| [**Wbem-Path**](a-wbempath.md)                                                  | False     | **Top**      |
| [**Bekannte Objekte**](a-wellknownobjects.md)                                 | False     | **Top**      |
| [**Wenn geändert**](a-whenchanged.md)                                            | False     | **Top**      |
| [**Wenn erstellt**](a-whencreated.md)                                            | False     | **Top**      |
| [**WWW-Homepage**](a-wwwhomepage.md)                                           | False     | **Top**      |
| [**WWW-Page-Other**](a-url.md)                                                  | False     | **Top**      |



## <a name="windows-server-2012"></a>Windows Server 2012

-   [Attribute](#windows-server-2012-attributes)



| Eingabe | Wert |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | True                                                                                         |
| Object-Category             | 2                                                                                            |
| Default-Object-Category     | \-                                                                                           |
| Governs-Id                  | 2.5.6.0                                                                                      |
| Default-Hiding-Value        | 1                                                                                            |
| Rdn-Att-Id                  | [**Common-Name**](a-cn.md)<br/>                                                       |
| Unterklasse von                 | **Top**<br/>                                                                           |
| Mögliche Vorgesetzte          | [**Lost-and-Found**](c-lostandfound.md)                                                     |
| Zusätzlich           | \-                                                                                           |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                 |
| Standardsicherheitsdeskriptor | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;;; AU) |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2012-attributes"></a>Windows Server 2012 Attribute

Diese Klasse enthält die folgenden Attribute für Windows Server 2012:



| attribute                                                                                    | Obligatorisch. | Abgeleitet von |
|----------------------------------------------------------------------------------------------|-----------|--------------|
| [**Admin-Description**](a-admindescription.md)                                              | False     | **Top**      |
| [**Administratoranzeigename**](a-admindisplayname.md)                                             | False     | **Top**      |
| [**Allowed-Attributes**](a-allowedattributes.md)                                            | False     | **Top**      |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)                         | False     | **Top**      |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                                       | False     | **Top**      |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)                    | False     | **Top**      |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                                | False     | **Top**      |
| [**Kanonischer Name**](a-canonicalname.md)                                                    | False     | **Top**      |
| [**Common-Name**](a-cn.md)                                                                  | False     | **Top**      |
| [**Create-Time-Stamp**](a-createtimestamp.md)                                               | False     | **Top**      |
| [**Beschreibung**](a-description.md)                                                         | False     | **Top**      |
| [**Anzeigename**](a-displayname.md)                                                        | False     | **Top**      |
| [**Display-Name-Printable**](a-displaynameprintable.md)                                     | False     | **Top**      |
| [**DSA-Signature**](a-dsasignature.md)                                                      | False     | **Top**      |
| [**DS-Core-Propagierungsdaten**](a-dscorepropagationdata.md)                                  | False     | **Top**      |
| [**Extension-Name**](a-extensionname.md)                                                    | False     | **Top**      |
| [**Flaggen**](a-flags.md)                                                                     | False     | **Top**      |
| [**From-Entry**](a-fromentry.md)                                                            | False     | **Top**      |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)                                | False     | **Top**      |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                                    | False     | **Top**      |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                                   | False     | **Top**      |
| [**Instanztyp**](a-instancetype.md)                                                      | True      | **Top**      |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                                | False     | **Top**      |
| [**Is-Deleted**](a-isdeleted.md)                                                            | False     | **Top**      |
| [**Is-Member-of-DL**](a-memberof.md)                                                        | False     | **Top**      |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                                           | False     | **Top**      |
| [**Wird wiederverwendet**](a-isrecycled.md)                                                          | False     | **Top**      |
| [**Letztes bekanntes übergeordnetes Element**](a-lastknownparent.md)                                               | False     | **Top**      |
| [**Verwaltete Objekte**](a-managedobjects.md)                                                  | False     | **Top**      |
| [**Mastered By**](a-masteredby.md)                                                          | False     | **Top**      |
| [**Modify-Time-Stamp**](a-modifytimestamp.md)                                               | False     | **Top**      |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                                  | False     | **Top**      |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                                  | False     | **Top**      |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)                          | False     | **Top**      |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                              | False     | **Top**      |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md)                  | False     | **Top**      |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md)               | False     | **Top**      |
| [**ms-DS-Claim-Shares-Possible-Values-with-BL**](a-msds-claimsharespossiblevalueswithbl.md) | False     | **Top**      |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)                       | False     | **Top**      |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                                    | False     | **Top**      |
| [**ms-DS-Enabled-Feature-BL**](a-msds-enabledfeaturebl.md)                                  | False     | **Top**      |
| [**ms-DS-Host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)                         | False     | **Top**      |
| [**ms-DS-Is-Domain-For**](a-msds-isdomainfor.md)                                            | False     | **Top**      |
| [**ms-DS-is-full-replica-for**](a-msds-isfullreplicafor.md)                                 | False     | **Top**      |
| [**ms-DS-is-partial-replica-for**](a-msds-ispartialreplicafor.md)                           | False     | **Top**      |
| [**ms-DS-Is-Primary-Computer-For**](a-msds-isprimarycomputerfor.md)                         | False     | **Top**      |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                                          | False     | **Top**      |
| [**ms-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                                          | False     | **Top**      |
| [**ms-DS-local-Effective-Deletion-Time**](a-msds-localeffectivedeletiontime.md)             | False     | **Top**      |
| [**ms-DS-local-Effective-Recycle-Time**](a-msds-localeffectiverecycletime.md)               | False     | **Top**      |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                                               | False     | **Top**      |
| [**ms-DS-Members-for-Az-Role-BL**](a-msds-membersforazrolebl.md)                            | False     | **Top**      |
| [**ms-DS-Members-of-Resource-Property-List-BL**](a-msds-membersofresourcepropertylistbl.md) | False     | **Top**      |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                                        | False     | **Top**      |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)                     | False     | **Top**      |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)                   | False     | **Top**      |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)                | False     | **Top**      |
| [**ms-DS-NC-Type**](a-msds-nctype.md)                                                       | False     | **Top**      |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                                          | False     | **Top**      |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                                | False     | **Top**      |
| [**ms-DS-OIDToGroup-Link-BL**](a-msds-oidtogrouplinkbl.md)                                  | False     | **Top**      |
| [**ms-DS-Operations-for-Az-Role-BL**](a-msds-operationsforazrolebl.md)                      | False     | **Top**      |
| [**ms-DS-Operations-for-Az-Task-BL**](a-msds-operationsforaztaskbl.md)                      | False     | **Top**      |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                                         | False     | **Top**      |
| [**ms-DS-PSO-Applied**](a-msds-psoapplied.md)                                               | False     | **Top**      |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)                       | False     | **Top**      |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                               | False     | **Top**      |
| [**ms-DS-Revealed-DSAs**](a-msds-revealeddsas.md)                                           | False     | **Top**      |
| [**ms-DS-Revealed-List-BL**](a-msds-revealedlistbl.md)                                      | False     | **Top**      |
| [**ms-DS-Tasks-for-Az-Role-BL**](a-msds-tasksforazrolebl.md)                                | False     | **Top**      |
| [**ms-DS-Tasks-for-Az-Task-BL**](a-msds-tasksforaztaskbl.md)                                | False     | **Top**      |
| [**ms-DS-TDO-Egress-BL**](a-msds-tdoegressbl.md)                                            | False     | **Top**      |
| [**ms-DS-TDO-Ingress-BL**](a-msds-tdoingressbl.md)                                          | False     | **Top**      |
| [**ms-DS-Value-Type-Reference-BL**](a-msds-valuetypereferencebl.md)                         | False     | **Top**      |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                                        | False     | **Top**      |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                                   | False     | **Top**      |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                                     | False     | **Top**      |
| [**Non-Security-Member-BL**](a-nonsecuritymemberbl.md)                                      | False     | **Top**      |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                                     | True      | **Top**      |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                                 | False     | **Top**      |
| [**Objektkategorie**](a-objectcategory.md)                                                  | True      | **Top**      |
| [**Objektklasse**](a-objectclass.md)                                                        | True      | **Top**      |
| [**Objekt-GUID**](a-objectguid.md)                                                          | False     | **Top**      |
| [**Objektversion**](a-objectversion.md)                                                    | False     | **Top**      |
| [**Andere bekannte Objekte**](a-otherwellknownobjects.md)                                  | False     | **Top**      |
| [**Teilattributlöschungsliste**](a-partialattributedeletionlist.md)                    | False     | **Top**      |
| [**Teilattributsatz**](a-partialattributeset.md)                                       | False     | **Top**      |
| [**Mögliche Hindernisse**](a-possibleinferiors.md)                                            | False     | **Top**      |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                                           | False     | **Top**      |
| [**Proxyadressen**](a-proxyaddresses.md)                                                  | False     | **Top**      |
| [**Query-Policy-BL**](a-querypolicybl.md)                                                   | False     | **Top**      |
| [**Rdn**](a-name.md)                                                                        | False     | **Top**      |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                                    | False     | **Top**      |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                                         | False     | **Top**      |
| [**Berichte**](a-directreports.md)                                                           | False     | **Top**      |
| [**Reps-From**](a-repsfrom.md)                                                              | False     | **Top**      |
| [**Reps-To**](a-repsto.md)                                                                  | False     | **Top**      |
| [**Revision**](a-revision.md)                                                               | False     | **Top**      |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                                           | False     | **Top**      |
| [**Server-Reference-BL**](a-serverreferencebl.md)                                           | False     | **Top**      |
| [**Nur in erweiterter Ansicht anzeigen**](a-showinadvancedviewonly.md)                               | False     | **Top**      |
| [**Site-Object-BL**](a-siteobjectbl.md)                                                     | False     | **Top**      |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                                   | False     | **Top**      |
| [**Sub-Refs**](a-subrefs.md)                                                                | False     | **Top**      |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                             | False     | **Top**      |
| [**Systemflags**](a-systemflags.md)                                                        | False     | **Top**      |
| [**USN-Changed**](a-usnchanged.md)                                                          | False     | **Top**      |
| [**VON USN erstellt**](a-usncreated.md)                                                          | False     | **Top**      |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                                   | False     | **Top**      |
| [**USN-Intersite**](a-usnintersite.md)                                                      | False     | **Top**      |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                                  | False     | **Top**      |
| [**USN-Quelle**](a-usnsource.md)                                                            | False     | **Top**      |
| [**Wbem-Path**](a-wbempath.md)                                                              | False     | **Top**      |
| [**Bekannte Objekte**](a-wellknownobjects.md)                                             | False     | **Top**      |
| [**Wenn geändert**](a-whenchanged.md)                                                        | False     | **Top**      |
| [**Wenn erstellt**](a-whencreated.md)                                                        | False     | **Top**      |
| [**WWW-Homepage**](a-wwwhomepage.md)                                                       | False     | **Top**      |
| [**WWW-Page-Other**](a-url.md)                                                              | False     | **Top**      |



 

 





