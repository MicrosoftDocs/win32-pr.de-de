---
title: MS-SQL-SQLServer-Klasse
description: Container zum Speichern von MS-SQL-SQLDatabase-, MS-SQL-SQLPublication- und MS-SQL-SQLRepository-Objekten.
ms.assetid: e83c93fa-b5d8-4941-af8c-b7a4c47c8e87
ms.tgt_platform: multiple
keywords:
- AD-Schema SQL MS-SQL-SQLServer-Klasse
- mS-SQL-SQLServer-Klasse AD Schema
topic_type:
- apiref
api_name:
- MS-SQL-SQLServer
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07cd5e3e8745b2adecb138ee4f523a568b9d9c34d8018ebce21577102b8113dc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119834620"
---
# <a name="ms-sql-sqlserver-class"></a>MS-SQL-SQLServer-Klasse

Container zum Speichern von [**MS-SQL-SQLDatabase-,**](c-ms-sql-sqldatabase.md) [**MS-SQL-SQLPublication-**](c-ms-sql-sqlpublication.md)und [**MS-SQL-SQLRepository-Objekten.**](c-ms-sql-sqlrepository.md)



| Eingabe | Wert |
|-------------------|--------------------------------------|
| CN                | MS-SQL-SQLServer                     |
| Ldap-Anzeigename | mS-SQL-SQLServer                     |
| Aktualisieren von Berechtigungen  | Dieser Wert wird vom System festgelegt.     |
| Updatehäufigkeit  | Beim Systemsetup.                     |
| Schema-ID-GUID    | 05f6c878-ccef-11d2-9993-0000f87a57d4 |



## <a name="implementations"></a>Implementierungen

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server

-   [Attribute](#windows-2000-server-attributes)



| Eingabe | Wert |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | False                                                                                        |
| Object-Category             | 1                                                                                            |
| Default-Object-Category     | \-                                                                                           |
| Governs-Id                  | 1.2.840.113556.1.5.184                                                                       |
| Default-Hiding-Value        | 1                                                                                            |
| Rdn-Att-Id                  | [**Common-Name**](a-cn.md)<br/>                                                       |
| Unterklasse von                 | [**Dienstverbindungspunkt**](c-serviceconnectionpoint.md)<br/>                      |
| Mögliche Vorgesetzte          | [**Dienstverbindungspunkt**](c-serviceconnectionpoint.md)                                 |
| Zusätzlich           | \-                                                                                           |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                 |
| Standardsicherheitsdeskriptor | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;;; AU) |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-2000-server-attributes"></a>Windows 2000-Serverattribute

Diese Klasse enthält die folgenden Attribute für Windows 2000-Server:



| attribute                                                                 | Obligatorisch. | Abgeleitet von                                                                             |
|---------------------------------------------------------------------------|-----------|------------------------------------------------------------------------------------------|
| [**Admin-Description**](a-admindescription.md)                           | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Administratoranzeigename**](a-admindisplayname.md)                          | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Allowed-Attributes**](a-allowedattributes.md)                         | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)      | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                    | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md) | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)             | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Kanonischer Name**](a-canonicalname.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Common-Name**](a-cn.md)                                               | True      | [**Verbindungspunkt**](c-connectionpoint.md)<br/> [**Nach oben**](c-top.md)<br/> |
| [**Create-Time-Stamp**](a-createtimestamp.md)                            | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Beschreibung**](a-description.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Anzeigename**](a-displayname.md)                                     | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Display-Name-Printable**](a-displaynameprintable.md)                  | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**DSA-Signature**](a-dsasignature.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**DS-Core-Propagierungsdaten**](a-dscorepropagationdata.md)               | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Extension-Name**](a-extensionname.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Flaggen**](a-flags.md)                                                  | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**From-Entry**](a-fromentry.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)             | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                 | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Instanztyp**](a-instancetype.md)                                   | True      | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)             | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Is-Deleted**](a-isdeleted.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Is-Member-of-DL**](a-memberof.md)                                     | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                        | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Keywords**](a-keywords.md)                                            | False     | [**Verbindungspunkt**](c-connectionpoint.md)<br/>                                 |
| [**Letztes bekanntes übergeordnetes Element**](a-lastknownparent.md)                            | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Verwaltet von**](a-managedby.md)                                         | False     | [**Verbindungspunkt**](c-connectionpoint.md)<br/>                                 |
| [**Verwaltete Objekte**](a-managedobjects.md)                               | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Mastered By**](a-masteredby.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Modify-Time-Stamp**](a-modifytimestamp.md)                            | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)    | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                 | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**MS-SQL-AppleTalk**](a-ms-sql-appletalk.md)                            | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-Build**](a-ms-sql-build.md)                                    | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-CharacterSet**](a-ms-sql-characterset.md)                      | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-Clustered**](a-ms-sql-clustered.md)                            | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-Contact**](a-ms-sql-contact.md)                                | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-GPSHeight**](a-ms-sql-gpsheight.md)                            | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-GPSL übertragen**](a-ms-sql-gpslatitude.md)                        | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-GPSLongitude**](a-ms-sql-gpslongitude.md)                      | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-InformationURL**](a-ms-sql-informationurl.md)                  | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-Keywords**](a-ms-sql-keywords.md)                              | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-LastUpdatedDate**](a-ms-sql-lastupdateddate.md)                | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-Location**](a-ms-sql-location.md)                              | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-Memory**](a-ms-sql-memory.md)                                  | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-MultiProtocol**](a-ms-sql-multiprotocol.md)                    | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-Name**](a-ms-sql-name.md)                                      | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-NamedPipe**](a-ms-sql-namedpipe.md)                            | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-RegisteredOwner**](a-ms-sql-registeredowner.md)                | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-ServiceAccount**](a-ms-sql-serviceaccount.md)                  | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-SortOrder**](a-ms-sql-sortorder.md)                            | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-SPX**](a-ms-sql-spx.md)                                        | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-Status**](a-ms-sql-status.md)                                  | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-TCPIP**](a-ms-sql-tcpip.md)                                    | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-UnicodeSortOrder**](a-ms-sql-unicodesortorder.md)              | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-Vines**](a-ms-sql-vines.md)                                    | False     | **MS-SQL-SQLServer**                                                                     |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                  | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Non-Security-Member-BL**](a-nonsecuritymemberbl.md)                   | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                  | True      | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Obj-Dist-Name**](a-distinguishedname.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Objektkategorie**](a-objectcategory.md)                               | True      | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Objektklasse**](a-objectclass.md)                                     | True      | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Objekt-GUID**](a-objectguid.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Objektversion**](a-objectversion.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Andere bekannte Objekte**](a-otherwellknownobjects.md)               | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Teilattributlöschungsliste**](a-partialattributedeletionlist.md) | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Teilattributsatz**](a-partialattributeset.md)                    | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Mögliche Hindernisse**](a-possibleinferiors.md)                         | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                        | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Proxyadressen**](a-proxyaddresses.md)                               | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Query-Policy-BL**](a-querypolicybl.md)                                | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Rdn**](a-name.md)                                                     | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                 | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                      | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Berichte**](a-directreports.md)                                        | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Reps-From**](a-repsfrom.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Reps-To**](a-repsto.md)                                               | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Revision**](a-revision.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                        | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Server-Reference-BL**](a-serverreferencebl.md)                        | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Dienstbindungsinformationen**](a-servicebindinginformation.md)        | False     | [**Dienstverbindungspunkt**](c-serviceconnectionpoint.md)<br/>                  |
| [**Dienstklassenname**](a-serviceclassname.md)                          | False     | [**Dienstverbindungspunkt**](c-serviceconnectionpoint.md)<br/>                  |
| [**Dienst-DNS-Name**](a-servicednsname.md)                              | False     | [**Dienstverbindungspunkt**](c-serviceconnectionpoint.md)<br/>                  |
| [**Dienst-DNS-Name-Typ**](a-servicednsnametype.md)                     | False     | [**Dienstverbindungspunkt**](c-serviceconnectionpoint.md)<br/>                  |
| [**Nur in erweiterter Ansicht anzeigen**](a-showinadvancedviewonly.md)            | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Site-Object-BL**](a-siteobjectbl.md)                                  | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Sub-Refs**](a-subrefs.md)                                             | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                          | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Systemflags**](a-systemflags.md)                                     | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**USN geändert**](a-usnchanged.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**USN-erstellt**](a-usncreated.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**USN-DSA-last-obj-removed**](a-usndsalastobjremoved.md)                | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**USN-Intersite**](a-usnintersite.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                               | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**USN-Quelle**](a-usnsource.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Wbem-Pfad**](a-wbempath.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Bekannte Objekte**](a-wellknownobjects.md)                          | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Bei Änderung**](a-whenchanged.md)                                     | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Bei der Erstellung**](a-whencreated.md)                                     | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**WWW-Startseite**](a-wwwhomepage.md)                                    | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**WWW-Page-Other**](a-url.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                                                          |



## <a name="windows-server-2003"></a>Windows Server 2003

-   [Attribute](#windows-server-2003-attributes)



| Eingabe | Wert |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | False                                                                                        |
| Object-Category             | 1                                                                                            |
| Default-Object-Category     | \-                                                                                           |
| Governs-Id                  | 1.2.840.113556.1.5.184                                                                       |
| Default-Hiding-Value        | 1                                                                                            |
| Rdn-Att-Id                  | [**Allgemeiner Name**](a-cn.md)<br/>                                                       |
| Unterklasse von                 | [**Dienstverbindungspunkt**](c-serviceconnectionpoint.md)<br/>                      |
| Mögliche Übergeordnete          | [**Dienstverbindungspunkt**](c-serviceconnectionpoint.md)                                 |
| Zusätzlich           | \-                                                                                           |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                 |
| Standardsicherheitsdeskriptor | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;;; AU) |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2003-attributes"></a>Windows Server 2003-Attribute

Diese Klasse enthält die folgenden Attribute für Windows Server 2003:



| attribute                                                                   | Obligatorisch. | Abgeleitet von                                                                             |
|-----------------------------------------------------------------------------|-----------|------------------------------------------------------------------------------------------|
| [**Administratorbeschreibung**](a-admindescription.md)                             | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Administratoranzeigename**](a-admindisplayname.md)                            | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Allowed-Attributes**](a-allowedattributes.md)                           | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)        | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                      | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)   | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**App-Schema-Version**](a-appschemaversion.md)                            | False     | [**Dienstverbindungspunkt**](c-serviceconnectionpoint.md)<br/>                  |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)               | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Kanonischer Name**](a-canonicalname.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Common-Name**](a-cn.md)                                                 | True      | [**Verbindungspunkt**](c-connectionpoint.md)<br/> [**Nach oben**](c-top.md)<br/> |
| [**Create-Time-Stamp**](a-createtimestamp.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Beschreibung**](a-description.md)                                        | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Anzeigename**](a-displayname.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Display-Name-Printable**](a-displaynameprintable.md)                    | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**DSA-Signature**](a-dsasignature.md)                                     | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**DS-Core-Propagierungsdaten**](a-dscorepropagationdata.md)                 | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Extension-Name**](a-extensionname.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Flaggen**](a-flags.md)                                                    | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**From-Entry**](a-fromentry.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)               | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                   | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                  | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Instanztyp**](a-instancetype.md)                                     | True      | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)               | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Is-Deleted**](a-isdeleted.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Is-Member-of-DL**](a-memberof.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                          | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Keywords**](a-keywords.md)                                              | False     | [**Verbindungspunkt**](c-connectionpoint.md)<br/>                                 |
| [**Letztes bekanntes übergeordnetes Element**](a-lastknownparent.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Verwaltet von**](a-managedby.md)                                           | False     | [**Verbindungspunkt**](c-connectionpoint.md)<br/>                                 |
| [**Verwaltete Objekte**](a-managedobjects.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Mastered By**](a-masteredby.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Modify-Time-Stamp**](a-modifytimestamp.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                 | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md) | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)      | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Members-for-Az-Role-BL**](a-msds-membersforazrolebl.md)           | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                       | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)    | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)  | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                         | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)               | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Operations-for-Az-Role-BL**](a-msds-operationsforazrolebl.md)     | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Operations-for-Az-Task-BL**](a-msds-operationsforaztaskbl.md)     | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)      | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)              | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Einstellungen**](a-msds-settings.md)                                   | False     | [**Verbindungspunkt**](c-connectionpoint.md)<br/>                                 |
| [**ms-DS-Tasks-for-Az-Role-BL**](a-msds-tasksforazrolebl.md)               | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Tasks-for-Az-Task-BL**](a-msds-tasksforaztaskbl.md)               | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**MS-SQL-AppleTalk**](a-ms-sql-appletalk.md)                              | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-Build**](a-ms-sql-build.md)                                      | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-CharacterSet**](a-ms-sql-characterset.md)                        | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-Clustered**](a-ms-sql-clustered.md)                              | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-Contact**](a-ms-sql-contact.md)                                  | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-GPSHeight**](a-ms-sql-gpsheight.md)                              | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-GPSLatitude**](a-ms-sql-gpslatitude.md)                          | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-GPSLongitude**](a-ms-sql-gpslongitude.md)                        | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-InformationURL**](a-ms-sql-informationurl.md)                    | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-Keywords**](a-ms-sql-keywords.md)                                | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-LastUpdatedDate**](a-ms-sql-lastupdateddate.md)                  | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-Location**](a-ms-sql-location.md)                                | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-Memory**](a-ms-sql-memory.md)                                    | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-MultiProtocol**](a-ms-sql-multiprotocol.md)                      | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-Name**](a-ms-sql-name.md)                                        | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-NamedPipe**](a-ms-sql-namedpipe.md)                              | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-RegisteredOwner**](a-ms-sql-registeredowner.md)                  | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-ServiceAccount**](a-ms-sql-serviceaccount.md)                    | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-SortOrder**](a-ms-sql-sortorder.md)                              | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-SPX**](a-ms-sql-spx.md)                                          | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-Status**](a-ms-sql-status.md)                                    | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-TCPIP**](a-ms-sql-tcpip.md)                                      | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-UnicodeSortOrder**](a-ms-sql-unicodesortorder.md)                | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-Vines**](a-ms-sql-vines.md)                                      | False     | **MS-SQL-SQLServer**                                                                     |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                    | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Non-Security-Member-BL**](a-nonsecuritymemberbl.md)                     | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                    | True      | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Objektkategorie**](a-objectcategory.md)                                 | True      | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Objektklasse**](a-objectclass.md)                                       | True      | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Objekt-GUID**](a-objectguid.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Objektversion**](a-objectversion.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Andere bekannte Objekte**](a-otherwellknownobjects.md)                 | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Teilattributlöschungsliste**](a-partialattributedeletionlist.md)   | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Teilattributsatz**](a-partialattributeset.md)                      | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Mögliche Hindernisse**](a-possibleinferiors.md)                           | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                          | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Proxyadressen**](a-proxyaddresses.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Query-Policy-BL**](a-querypolicybl.md)                                  | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Rdn**](a-name.md)                                                       | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                   | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                        | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Berichte**](a-directreports.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Reps-From**](a-repsfrom.md)                                             | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Reps-To**](a-repsto.md)                                                 | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Revision**](a-revision.md)                                              | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                          | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Server-Reference-BL**](a-serverreferencebl.md)                          | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Dienstbindungsinformationen**](a-servicebindinginformation.md)          | False     | [**Dienstverbindungspunkt**](c-serviceconnectionpoint.md)<br/>                  |
| [**Service-Class-Name**](a-serviceclassname.md)                            | False     | [**Dienstverbindungspunkt**](c-serviceconnectionpoint.md)<br/>                  |
| [**Dienst-DNS-Name**](a-servicednsname.md)                                | False     | [**Dienstverbindungspunkt**](c-serviceconnectionpoint.md)<br/>                  |
| [**Service-DNS-Name-Type**](a-servicednsnametype.md)                       | False     | [**Dienstverbindungspunkt**](c-serviceconnectionpoint.md)<br/>                  |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)              | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                  | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Sub-Refs**](a-subrefs.md)                                               | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Systemflags**](a-systemflags.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**USN-Changed**](a-usnchanged.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**VON USN erstellt**](a-usncreated.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                  | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**USN-Intersite**](a-usnintersite.md)                                     | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**USN-Quelle**](a-usnsource.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Hersteller**](a-vendor.md)                                                  | False     | [**Dienstverbindungspunkt**](c-serviceconnectionpoint.md)<br/>                  |
| [**Versionsnummer**](a-versionnumber.md)                                   | False     | [**Dienstverbindungspunkt**](c-serviceconnectionpoint.md)<br/>                  |
| [**Versionsnummer-Hi**](a-versionnumberhi.md)                              | False     | [**Dienstverbindungspunkt**](c-serviceconnectionpoint.md)<br/>                  |
| [**Versionsnummer-Lo**](a-versionnumberlo.md)                              | False     | [**Dienstverbindungspunkt**](c-serviceconnectionpoint.md)<br/>                  |
| [**Wbem-Path**](a-wbempath.md)                                             | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Bekannte Objekte**](a-wellknownobjects.md)                            | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Wenn geändert**](a-whenchanged.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Wenn erstellt**](a-whencreated.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**WWW-Homepage**](a-wwwhomepage.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**WWW-Page-Other**](a-url.md)                                             | False     | [**Nach oben**](c-top.md)<br/>                                                          |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2

-   [Attribute](#windows-server-2003-r2-attributes)



| Eingabe | Wert |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | False                                                                                        |
| Object-Category             | 1                                                                                            |
| Default-Object-Category     | \-                                                                                           |
| Governs-Id                  | 1.2.840.113556.1.5.184                                                                       |
| Default-Hiding-Value        | 1                                                                                            |
| Rdn-Att-Id                  | [**Common-Name**](a-cn.md)<br/>                                                       |
| Unterklasse von                 | [**Dienstverbindungspunkt**](c-serviceconnectionpoint.md)<br/>                      |
| Mögliche Vorgesetzte          | [**Dienstverbindungspunkt**](c-serviceconnectionpoint.md)                                 |
| Zusätzlich           | \-                                                                                           |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                 |
| Standardsicherheitsdeskriptor | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;;; AU) |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2003-r2-attributes"></a>Windows Server 2003 R2-Attribute

Diese Klasse enthält die folgenden Attribute für Windows Server 2003 R2:



| attribute                                                                   | Obligatorisch. | Abgeleitet von                                                                             |
|-----------------------------------------------------------------------------|-----------|------------------------------------------------------------------------------------------|
| [**Admin-Description**](a-admindescription.md)                             | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Administratoranzeigename**](a-admindisplayname.md)                            | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Allowed-Attributes**](a-allowedattributes.md)                           | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)        | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                      | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)   | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**App-Schema-Version**](a-appschemaversion.md)                            | False     | [**Dienstverbindungspunkt**](c-serviceconnectionpoint.md)<br/>                  |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)               | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Kanonischer Name**](a-canonicalname.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Common-Name**](a-cn.md)                                                 | True      | [**Verbindungspunkt**](c-connectionpoint.md)<br/> [**Nach oben**](c-top.md)<br/> |
| [**Create-Time-Stamp**](a-createtimestamp.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Beschreibung**](a-description.md)                                        | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Anzeigename**](a-displayname.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Display-Name-Printable**](a-displaynameprintable.md)                    | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**DSA-Signature**](a-dsasignature.md)                                     | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**DS-Core-Propagierungsdaten**](a-dscorepropagationdata.md)                 | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Extension-Name**](a-extensionname.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Flaggen**](a-flags.md)                                                    | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**From-Entry**](a-fromentry.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)               | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                   | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                  | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Instanztyp**](a-instancetype.md)                                     | True      | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)               | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Is-Deleted**](a-isdeleted.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Is-Member-of-DL**](a-memberof.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                          | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Keywords**](a-keywords.md)                                              | False     | [**Verbindungspunkt**](c-connectionpoint.md)<br/>                                 |
| [**Letztes bekanntes übergeordnetes Element**](a-lastknownparent.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Verwaltet von**](a-managedby.md)                                           | False     | [**Verbindungspunkt**](c-connectionpoint.md)<br/>                                 |
| [**Verwaltete Objekte**](a-managedobjects.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Mastered By**](a-masteredby.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Modify-Time-Stamp**](a-modifytimestamp.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                 | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)         | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)             | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md) | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)      | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Members-For-Az-Role-BL**](a-msds-membersforazrolebl.md)           | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                       | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)    | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)  | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                         | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)               | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)     | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)     | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)      | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)              | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Einstellungen**](a-msds-settings.md)                                   | False     | [**Verbindungspunkt**](c-connectionpoint.md)<br/>                                 |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)               | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)               | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                  | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**MS-SQL-AppleTalk**](a-ms-sql-appletalk.md)                              | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-Build**](a-ms-sql-build.md)                                      | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-CharacterSet**](a-ms-sql-characterset.md)                        | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-Clustered**](a-ms-sql-clustered.md)                              | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-Contact**](a-ms-sql-contact.md)                                  | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-GPSHeight**](a-ms-sql-gpsheight.md)                              | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-GPSL übertragen**](a-ms-sql-gpslatitude.md)                          | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-GPSLongitude**](a-ms-sql-gpslongitude.md)                        | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-InformationURL**](a-ms-sql-informationurl.md)                    | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-Keywords**](a-ms-sql-keywords.md)                                | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-LastUpdatedDate**](a-ms-sql-lastupdateddate.md)                  | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-Location**](a-ms-sql-location.md)                                | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-Memory**](a-ms-sql-memory.md)                                    | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-MultiProtocol**](a-ms-sql-multiprotocol.md)                      | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-Name**](a-ms-sql-name.md)                                        | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-NamedPipe**](a-ms-sql-namedpipe.md)                              | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-RegisteredOwner**](a-ms-sql-registeredowner.md)                  | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-ServiceAccount**](a-ms-sql-serviceaccount.md)                    | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-SortOrder**](a-ms-sql-sortorder.md)                              | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-SPX**](a-ms-sql-spx.md)                                          | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-Status**](a-ms-sql-status.md)                                    | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-TCPIP**](a-ms-sql-tcpip.md)                                      | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-UnicodeSortOrder**](a-ms-sql-unicodesortorder.md)                | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-Vines**](a-ms-sql-vines.md)                                      | False     | **MS-SQL-SQLServer**                                                                     |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                    | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Non-Security-Member-BL**](a-nonsecuritymemberbl.md)                     | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                    | True      | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Objektkategorie**](a-objectcategory.md)                                 | True      | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Object-Class**](a-objectclass.md)                                       | True      | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Objekt-GUID**](a-objectguid.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Object-Version**](a-objectversion.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Andere bekannte Objekte**](a-otherwellknownobjects.md)                 | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)   | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                      | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Mögliche 100000000000**](a-possibleinferiors.md)                           | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                          | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Proxyadressen**](a-proxyaddresses.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Query-Policy-BL**](a-querypolicybl.md)                                  | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Rdn**](a-name.md)                                                       | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                   | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                        | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Berichte**](a-directreports.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Reps-From**](a-repsfrom.md)                                             | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Reps-To**](a-repsto.md)                                                 | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Revision**](a-revision.md)                                              | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                          | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Server-Reference-BL**](a-serverreferencebl.md)                          | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Dienstbindungsinformationen**](a-servicebindinginformation.md)          | False     | [**Dienstverbindungspunkt**](c-serviceconnectionpoint.md)<br/>                  |
| [**Service-Class-Name**](a-serviceclassname.md)                            | False     | [**Dienstverbindungspunkt**](c-serviceconnectionpoint.md)<br/>                  |
| [**Dienst-DNS-Name**](a-servicednsname.md)                                | False     | [**Dienstverbindungspunkt**](c-serviceconnectionpoint.md)<br/>                  |
| [**Service-DNS-Name-Type**](a-servicednsnametype.md)                       | False     | [**Dienstverbindungspunkt**](c-serviceconnectionpoint.md)<br/>                  |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)              | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                  | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Sub-Refs**](a-subrefs.md)                                               | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Systemflags**](a-systemflags.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**USN-Changed**](a-usnchanged.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**VON USN erstellt**](a-usncreated.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                  | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**USN-Intersite**](a-usnintersite.md)                                     | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**USN-Quelle**](a-usnsource.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Hersteller**](a-vendor.md)                                                  | False     | [**Dienstverbindungspunkt**](c-serviceconnectionpoint.md)<br/>                  |
| [**Versionsnummer**](a-versionnumber.md)                                   | False     | [**Dienstverbindungspunkt**](c-serviceconnectionpoint.md)<br/>                  |
| [**Versionsnummer-Hi**](a-versionnumberhi.md)                              | False     | [**Dienstverbindungspunkt**](c-serviceconnectionpoint.md)<br/>                  |
| [**Versionsnummer-Lo**](a-versionnumberlo.md)                              | False     | [**Dienstverbindungspunkt**](c-serviceconnectionpoint.md)<br/>                  |
| [**Wbem-Path**](a-wbempath.md)                                             | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Bekannte Objekte**](a-wellknownobjects.md)                            | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Wenn geändert**](a-whenchanged.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Wenn erstellt**](a-whencreated.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**WWW-Homepage**](a-wwwhomepage.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**WWW-Page-Other**](a-url.md)                                             | False     | [**Nach oben**](c-top.md)<br/>                                                          |



## <a name="windows-server-2008"></a>Windows Server 2008

-   [Attribute](#windows-server-2008-attributes)



| Eingabe | Wert |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | False                                                                                        |
| Object-Category             | 1                                                                                            |
| Default-Object-Category     | \-                                                                                           |
| Governs-Id                  | 1.2.840.113556.1.5.184                                                                       |
| Default-Hiding-Value        | 1                                                                                            |
| Rdn-Att-Id                  | [**Allgemeiner Name**](a-cn.md)<br/>                                                       |
| Unterklasse von                 | [**Dienstverbindungspunkt**](c-serviceconnectionpoint.md)<br/>                      |
| Mögliche Übergeordnete          | [**Dienstverbindungspunkt**](c-serviceconnectionpoint.md)                                 |
| Zusätzlich           | \-                                                                                           |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                 |
| Standardsicherheitsdeskriptor | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;;; AU) |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2008-attributes"></a>Windows Server 2008-Attribute

Diese Klasse enthält die folgenden Attribute für Windows Server 2008:



| attribute                                                                      | Obligatorisch. | Abgeleitet von                                                                             |
|--------------------------------------------------------------------------------|-----------|------------------------------------------------------------------------------------------|
| [**Administratorbeschreibung**](a-admindescription.md)                                | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Admin-Display-Name**](a-admindisplayname.md)                               | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Allowed-Attributes**](a-allowedattributes.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)           | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                         | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)      | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**App-Schema-Version**](a-appschemaversion.md)                               | False     | [**Dienstverbindungspunkt**](c-serviceconnectionpoint.md)<br/>                  |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                  | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Kanonischer Name**](a-canonicalname.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Allgemeiner Name**](a-cn.md)                                                    | True      | [**Verbindungspunkt**](c-connectionpoint.md)<br/> [**Nach oben**](c-top.md)<br/> |
| [**Erstellen eines Zeitstempels**](a-createtimestamp.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Beschreibung**](a-description.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Anzeigename**](a-displayname.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Anzeigename– druckbar**](a-displaynameprintable.md)                       | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**DSA-Signature**](a-dsasignature.md)                                        | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**DS-Core-Propagierungsdaten**](a-dscorepropagationdata.md)                    | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Erweiterungsname**](a-extensionname.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Flaggen**](a-flags.md)                                                       | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**From-Entry**](a-fromentry.md)                                              | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)                  | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                      | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                     | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Instanztyp**](a-instancetype.md)                                        | True      | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                  | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Is-Deleted**](a-isdeleted.md)                                              | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Is-Member-of-DL**](a-memberof.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                             | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Keywords**](a-keywords.md)                                                 | False     | [**Verbindungspunkt**](c-connectionpoint.md)<br/>                                 |
| [**Letztes bekanntes übergeordnetes Element**](a-lastknownparent.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Verwaltet von**](a-managedby.md)                                              | False     | [**Verbindungspunkt**](c-connectionpoint.md)<br/>                                 |
| [**Verwaltete Objekte**](a-managedobjects.md)                                    | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Mastered By**](a-masteredby.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Modify-Time-Stamp**](a-modifytimestamp.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                    | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                    | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)            | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md)    | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md) | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)         | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                      | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-is-Domain-for**](a-msds-isdomainfor.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-is-full-replica-for**](a-msds-isfullreplicafor.md)                   | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-is-partial-replica-for**](a-msds-ispartialreplicafor.md)             | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                            | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Members-For-Az-Role-BL**](a-msds-membersforazrolebl.md)              | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                          | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)       | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)     | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)  | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-Type**](a-msds-nctype.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                            | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                  | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)        | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)        | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                           | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-PSO-Applied**](a-msds-psoapplied.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)         | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                 | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Revealed-DSAs**](a-msds-revealeddsas.md)                             | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Revealed-List-BL**](a-msds-revealedlistbl.md)                        | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Einstellungen**](a-msds-settings.md)                                      | False     | [**Verbindungspunkt**](c-connectionpoint.md)<br/>                                 |
| [**ms-DS-Tasks-for-Az-Role-BL**](a-msds-tasksforazrolebl.md)                  | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Tasks-for-Az-Task-BL**](a-msds-tasksforaztaskbl.md)                  | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                     | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**MS-SQL-AppleTalk**](a-ms-sql-appletalk.md)                                 | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-Build**](a-ms-sql-build.md)                                         | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-CharacterSet**](a-ms-sql-characterset.md)                           | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-Clustered**](a-ms-sql-clustered.md)                                 | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-Contact**](a-ms-sql-contact.md)                                     | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-GPSHeight**](a-ms-sql-gpsheight.md)                                 | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-GPSLatitude**](a-ms-sql-gpslatitude.md)                             | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-GPSLongitude**](a-ms-sql-gpslongitude.md)                           | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-InformationURL**](a-ms-sql-informationurl.md)                       | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-Keywords**](a-ms-sql-keywords.md)                                   | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-LastUpdatedDate**](a-ms-sql-lastupdateddate.md)                     | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-Location**](a-ms-sql-location.md)                                   | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-Memory**](a-ms-sql-memory.md)                                       | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-MultiProtocol**](a-ms-sql-multiprotocol.md)                         | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-Name**](a-ms-sql-name.md)                                           | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-NamedPipe**](a-ms-sql-namedpipe.md)                                 | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-RegisteredOwner**](a-ms-sql-registeredowner.md)                     | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-ServiceAccount**](a-ms-sql-serviceaccount.md)                       | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-SortOrder**](a-ms-sql-sortorder.md)                                 | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-SPX**](a-ms-sql-spx.md)                                             | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-Status**](a-ms-sql-status.md)                                       | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-TCPIP**](a-ms-sql-tcpip.md)                                         | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-UnicodeSortOrder**](a-ms-sql-unicodesortorder.md)                   | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-Vines**](a-ms-sql-vines.md)                                         | False     | **MS-SQL-SQLServer**                                                                     |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Non-Security-Member-BL**](a-nonsecuritymemberbl.md)                        | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                       | True      | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Objektkategorie**](a-objectcategory.md)                                    | True      | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Object-Class**](a-objectclass.md)                                          | True      | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Objekt-GUID**](a-objectguid.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Object-Version**](a-objectversion.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Andere bekannte Objekte**](a-otherwellknownobjects.md)                    | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)      | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                         | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Mögliche 100000000000**](a-possibleinferiors.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                             | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Proxyadressen**](a-proxyaddresses.md)                                    | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Query-Policy-BL**](a-querypolicybl.md)                                     | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Rdn**](a-name.md)                                                          | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                      | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                           | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Berichte**](a-directreports.md)                                             | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Reps-From**](a-repsfrom.md)                                                | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Reps-To**](a-repsto.md)                                                    | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Revision**](a-revision.md)                                                 | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                             | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Server-Reference-BL**](a-serverreferencebl.md)                             | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Dienstbindungsinformationen**](a-servicebindinginformation.md)             | False     | [**Dienstverbindungspunkt**](c-serviceconnectionpoint.md)<br/>                  |
| [**Service-Class-Name**](a-serviceclassname.md)                               | False     | [**Dienstverbindungspunkt**](c-serviceconnectionpoint.md)<br/>                  |
| [**Dienst-DNS-Name**](a-servicednsname.md)                                   | False     | [**Dienstverbindungspunkt**](c-serviceconnectionpoint.md)<br/>                  |
| [**Service-DNS-Name-Type**](a-servicednsnametype.md)                          | False     | [**Dienstverbindungspunkt**](c-serviceconnectionpoint.md)<br/>                  |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)                 | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Site-Object-BL**](a-siteobjectbl.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                     | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Sub-Refs**](a-subrefs.md)                                                  | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                               | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Systemflags**](a-systemflags.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**USN-Changed**](a-usnchanged.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**VON USN erstellt**](a-usncreated.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                     | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**USN-Intersite**](a-usnintersite.md)                                        | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                    | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**USN-Quelle**](a-usnsource.md)                                              | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Hersteller**](a-vendor.md)                                                     | False     | [**Dienstverbindungspunkt**](c-serviceconnectionpoint.md)<br/>                  |
| [**Versionsnummer**](a-versionnumber.md)                                      | False     | [**Dienstverbindungspunkt**](c-serviceconnectionpoint.md)<br/>                  |
| [**Versionsnummer-Hi**](a-versionnumberhi.md)                                 | False     | [**Dienstverbindungspunkt**](c-serviceconnectionpoint.md)<br/>                  |
| [**Versionsnummer-Lo**](a-versionnumberlo.md)                                 | False     | [**Dienstverbindungspunkt**](c-serviceconnectionpoint.md)<br/>                  |
| [**Wbem-Path**](a-wbempath.md)                                                | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Bekannte Objekte**](a-wellknownobjects.md)                               | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Wenn geändert**](a-whenchanged.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Wenn erstellt**](a-whencreated.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**WWW-Homepage**](a-wwwhomepage.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**WWW-Page-Other**](a-url.md)                                                | False     | [**Nach oben**](c-top.md)<br/>                                                          |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2

-   [Attribute](#windows-server-2008-r2-attributes)



| Eingabe | Wert |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | False                                                                                        |
| Object-Category             | 1                                                                                            |
| Default-Object-Category     | \-                                                                                           |
| Governs-Id                  | 1.2.840.113556.1.5.184                                                                       |
| Default-Hiding-Value        | 1                                                                                            |
| Rdn-Att-Id                  | [**Common-Name**](a-cn.md)<br/>                                                       |
| Unterklasse von                 | [**Dienstverbindungspunkt**](c-serviceconnectionpoint.md)<br/>                      |
| Mögliche Vorgesetzte          | [**Dienstverbindungspunkt**](c-serviceconnectionpoint.md)                                 |
| Zusätzlich           | \-                                                                                           |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                 |
| Standardsicherheitsdeskriptor | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;;; AU) |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2008-r2-attributes"></a>Windows Server 2008 R2-Attribute

Diese Klasse enthält die folgenden Attribute für Windows Server 2008 R2:



| attribute                                                                        | Obligatorisch. | Abgeleitet von                                                                             |
|----------------------------------------------------------------------------------|-----------|------------------------------------------------------------------------------------------|
| [**Admin-Description**](a-admindescription.md)                                  | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Administratoranzeigename**](a-admindisplayname.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Allowed-Attributes**](a-allowedattributes.md)                                | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)             | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                           | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)        | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**App-Schema-Version**](a-appschemaversion.md)                                 | False     | [**Dienstverbindungspunkt**](c-serviceconnectionpoint.md)<br/>                  |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                    | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Kanonischer Name**](a-canonicalname.md)                                        | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Allgemeiner Name**](a-cn.md)                                                      | True      | [**Verbindungspunkt**](c-connectionpoint.md)<br/> [**Nach oben**](c-top.md)<br/> |
| [**Erstellen eines Zeitstempels**](a-createtimestamp.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Beschreibung**](a-description.md)                                             | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Anzeigename**](a-displayname.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Anzeigename– druckbar**](a-displaynameprintable.md)                         | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**DSA-Signature**](a-dsasignature.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**DS-Core-Propagierungsdaten**](a-dscorepropagationdata.md)                      | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Erweiterungsname**](a-extensionname.md)                                        | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Flaggen**](a-flags.md)                                                         | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**From-Entry**](a-fromentry.md)                                                | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)                    | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                        | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Instanztyp**](a-instancetype.md)                                          | True      | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                    | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Is-Deleted**](a-isdeleted.md)                                                | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Is-Member-of-DL**](a-memberof.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                               | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Wird wiederverwendet**](a-isrecycled.md)                                              | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Keywords**](a-keywords.md)                                                   | False     | [**Verbindungspunkt**](c-connectionpoint.md)<br/>                                 |
| [**Last-Known-Parent**](a-lastknownparent.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Verwaltet von**](a-managedby.md)                                                | False     | [**Verbindungspunkt**](c-connectionpoint.md)<br/>                                 |
| [**Verwaltete Objekte**](a-managedobjects.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Mastered-By**](a-masteredby.md)                                              | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Modify-Time-Stamp**](a-modifytimestamp.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                      | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)              | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                  | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md)      | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md)   | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)           | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                        | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Enabled-Feature-BL**](a-msds-enabledfeaturebl.md)                      | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)             | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-is-Domain-for**](a-msds-isdomainfor.md)                                | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-is-full-replica-for**](a-msds-isfullreplicafor.md)                     | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-is-partial-replica-for**](a-msds-ispartialreplicafor.md)               | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-local-Effective-Deletion-Time**](a-msds-localeffectivedeletiontime.md) | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-local-Effective-Recycle-Time**](a-msds-localeffectiverecycletime.md)   | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Members-For-Az-Role-BL**](a-msds-membersforazrolebl.md)                | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                            | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)         | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)       | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)    | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-Type**](a-msds-nctype.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                    | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-OIDToGroup-Link-BL**](a-msds-oidtogrouplinkbl.md)                      | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)          | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)          | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                             | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-PSO-Applied**](a-msds-psoapplied.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)           | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                   | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Revealed-DSAs**](a-msds-revealeddsas.md)                               | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Revealed-List-BL**](a-msds-revealedlistbl.md)                          | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Einstellungen**](a-msds-settings.md)                                        | False     | [**Verbindungspunkt**](c-connectionpoint.md)<br/>                                 |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)                    | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)                    | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                       | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**MS-SQL-AppleTalk**](a-ms-sql-appletalk.md)                                   | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-Build**](a-ms-sql-build.md)                                           | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-CharacterSet**](a-ms-sql-characterset.md)                             | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-Clustered**](a-ms-sql-clustered.md)                                   | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-Contact**](a-ms-sql-contact.md)                                       | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-GPSHeight**](a-ms-sql-gpsheight.md)                                   | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-GPSL übertragen**](a-ms-sql-gpslatitude.md)                               | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-GPSLongitude**](a-ms-sql-gpslongitude.md)                             | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-InformationURL**](a-ms-sql-informationurl.md)                         | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-Keywords**](a-ms-sql-keywords.md)                                     | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-LastUpdatedDate**](a-ms-sql-lastupdateddate.md)                       | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-Location**](a-ms-sql-location.md)                                     | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-Memory**](a-ms-sql-memory.md)                                         | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-MultiProtocol**](a-ms-sql-multiprotocol.md)                           | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-Name**](a-ms-sql-name.md)                                             | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-NamedPipe**](a-ms-sql-namedpipe.md)                                   | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-RegisteredOwner**](a-ms-sql-registeredowner.md)                       | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-ServiceAccount**](a-ms-sql-serviceaccount.md)                         | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-SortOrder**](a-ms-sql-sortorder.md)                                   | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-SPX**](a-ms-sql-spx.md)                                               | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-Status**](a-ms-sql-status.md)                                         | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-TCPIP**](a-ms-sql-tcpip.md)                                           | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-UnicodeSortOrder**](a-ms-sql-unicodesortorder.md)                     | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-Vines**](a-ms-sql-vines.md)                                           | False     | **MS-SQL-SQLServer**                                                                     |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Non-Security-Member-BL**](a-nonsecuritymemberbl.md)                          | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                         | True      | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                     | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Objektkategorie**](a-objectcategory.md)                                      | True      | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Object-Class**](a-objectclass.md)                                            | True      | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Objekt-GUID**](a-objectguid.md)                                              | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Objektversion**](a-objectversion.md)                                        | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Andere bekannte Objekte**](a-otherwellknownobjects.md)                      | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Teilattributlöschungsliste**](a-partialattributedeletionlist.md)        | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Teilattributsatz**](a-partialattributeset.md)                           | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Mögliche Hindernisse**](a-possibleinferiors.md)                                | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                               | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Proxyadressen**](a-proxyaddresses.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Query-Policy-BL**](a-querypolicybl.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Rdn**](a-name.md)                                                            | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                        | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                             | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Berichte**](a-directreports.md)                                               | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Reps-From**](a-repsfrom.md)                                                  | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Reps-To**](a-repsto.md)                                                      | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Revision**](a-revision.md)                                                   | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                               | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Server-Reference-BL**](a-serverreferencebl.md)                               | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Dienstbindungsinformationen**](a-servicebindinginformation.md)               | False     | [**Dienstverbindungspunkt**](c-serviceconnectionpoint.md)<br/>                  |
| [**Dienstklassenname**](a-serviceclassname.md)                                 | False     | [**Dienstverbindungspunkt**](c-serviceconnectionpoint.md)<br/>                  |
| [**Dienst-DNS-Name**](a-servicednsname.md)                                     | False     | [**Dienstverbindungspunkt**](c-serviceconnectionpoint.md)<br/>                  |
| [**Dienst-DNS-Name-Typ**](a-servicednsnametype.md)                            | False     | [**Dienstverbindungspunkt**](c-serviceconnectionpoint.md)<br/>                  |
| [**Nur in erweiterter Ansicht anzeigen**](a-showinadvancedviewonly.md)                   | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Site-Object-BL**](a-siteobjectbl.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                       | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Sub-Refs**](a-subrefs.md)                                                    | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Systemflags**](a-systemflags.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**USN geändert**](a-usnchanged.md)                                              | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**USN-erstellt**](a-usncreated.md)                                              | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**USN-DSA-last-obj-removed**](a-usndsalastobjremoved.md)                       | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**USN-Intersite**](a-usnintersite.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**USN-Quelle**](a-usnsource.md)                                                | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Hersteller**](a-vendor.md)                                                       | False     | [**Dienstverbindungspunkt**](c-serviceconnectionpoint.md)<br/>                  |
| [**Versionsnummer**](a-versionnumber.md)                                        | False     | [**Dienstverbindungspunkt**](c-serviceconnectionpoint.md)<br/>                  |
| [**Versionsnummer-Hi**](a-versionnumberhi.md)                                   | False     | [**Dienstverbindungspunkt**](c-serviceconnectionpoint.md)<br/>                  |
| [**Versionsnummer-Lo**](a-versionnumberlo.md)                                   | False     | [**Dienstverbindungspunkt**](c-serviceconnectionpoint.md)<br/>                  |
| [**Wbem-Pfad**](a-wbempath.md)                                                  | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Bekannte Objekte**](a-wellknownobjects.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Bei Änderung**](a-whenchanged.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Bei der Erstellung**](a-whencreated.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**WWW-Startseite**](a-wwwhomepage.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**WWW-Page-Other**](a-url.md)                                                  | False     | [**Nach oben**](c-top.md)<br/>                                                          |



## <a name="windows-server-2012"></a>Windows Server 2012

-   [Attribute](#windows-server-2012-attributes)



| Eingabe | Wert |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | False                                                                                        |
| Object-Category             | 1                                                                                            |
| Default-Object-Category     | \-                                                                                           |
| Governs-Id                  | 1.2.840.113556.1.5.184                                                                       |
| Default-Hiding-Value        | 1                                                                                            |
| Rdn-Att-Id                  | [**Allgemeiner Name**](a-cn.md)<br/>                                                       |
| Unterklasse von                 | [**Dienstverbindungspunkt**](c-serviceconnectionpoint.md)<br/>                      |
| Mögliche Übergeordnete          | [**Dienstverbindungspunkt**](c-serviceconnectionpoint.md)                                 |
| Zusätzlich           | \-                                                                                           |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                 |
| Standardsicherheitsdeskriptor | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;;; AU) |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2012-attributes"></a>Windows Server 2012 Attribute

Diese Klasse enthält die folgenden Attribute für Windows Server 2012:



| attribute                                                                                    | Obligatorisch. | Abgeleitet von                                                                             |
|----------------------------------------------------------------------------------------------|-----------|------------------------------------------------------------------------------------------|
| [**Administratorbeschreibung**](a-admindescription.md)                                              | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Admin-Display-Name**](a-admindisplayname.md)                                             | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Allowed-Attributes**](a-allowedattributes.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)                         | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)                    | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**App-Schema-Version**](a-appschemaversion.md)                                             | False     | [**Dienstverbindungspunkt**](c-serviceconnectionpoint.md)<br/>                  |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                                | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Kanonischer Name**](a-canonicalname.md)                                                    | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Allgemeiner Name**](a-cn.md)                                                                  | True      | [**Verbindungspunkt**](c-connectionpoint.md)<br/> [**Nach oben**](c-top.md)<br/> |
| [**Erstellen eines Zeitstempels**](a-createtimestamp.md)                                               | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Beschreibung**](a-description.md)                                                         | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Anzeigename**](a-displayname.md)                                                        | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Display-Name-Printable**](a-displaynameprintable.md)                                     | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**DSA-Signature**](a-dsasignature.md)                                                      | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**DS-Core-Propagierungsdaten**](a-dscorepropagationdata.md)                                  | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Extension-Name**](a-extensionname.md)                                                    | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Flaggen**](a-flags.md)                                                                     | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**From-Entry**](a-fromentry.md)                                                            | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)                                | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                                    | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                                   | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Instanztyp**](a-instancetype.md)                                                      | True      | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                                | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Is-Deleted**](a-isdeleted.md)                                                            | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Is-Member-of-DL**](a-memberof.md)                                                        | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Wird wiederverwendet**](a-isrecycled.md)                                                          | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Keywords**](a-keywords.md)                                                               | False     | [**Verbindungspunkt**](c-connectionpoint.md)<br/>                                 |
| [**Letztes bekanntes übergeordnetes Element**](a-lastknownparent.md)                                               | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Verwaltet von**](a-managedby.md)                                                            | False     | [**Verbindungspunkt**](c-connectionpoint.md)<br/>                                 |
| [**Verwaltete Objekte**](a-managedobjects.md)                                                  | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Mastered By**](a-masteredby.md)                                                          | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Modify-Time-Stamp**](a-modifytimestamp.md)                                               | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                                  | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                                  | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)                          | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md)                  | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md)               | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Claim-Shares-Possible-Values-With-BL**](a-msds-claimsharespossiblevalueswithbl.md) | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)                       | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                                    | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Enabled-Feature-BL**](a-msds-enabledfeaturebl.md)                                  | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)                         | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-is-Domain-for**](a-msds-isdomainfor.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-is-full-replica-for**](a-msds-isfullreplicafor.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-is-partial-replica-for**](a-msds-ispartialreplicafor.md)                           | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Is-Primary-Computer-For**](a-msds-isprimarycomputerfor.md)                         | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-local-Effective-Deletion-Time**](a-msds-localeffectivedeletiontime.md)             | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-local-Effective-Recycle-Time**](a-msds-localeffectiverecycletime.md)               | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                                               | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Members-for-Az-Role-BL**](a-msds-membersforazrolebl.md)                            | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Members-of-Resource-Property-List-BL**](a-msds-membersofresourcepropertylistbl.md) | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                                        | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)                     | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)                   | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)                | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-Type**](a-msds-nctype.md)                                                       | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                                | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-OIDToGroup-Link-BL**](a-msds-oidtogrouplinkbl.md)                                  | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Operations-for-Az-Role-BL**](a-msds-operationsforazrolebl.md)                      | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Operations-for-Az-Task-BL**](a-msds-operationsforaztaskbl.md)                      | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-PSO-Applied**](a-msds-psoapplied.md)                                               | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)                       | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                               | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Revealed-DSAs**](a-msds-revealeddsas.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Revealed-List-BL**](a-msds-revealedlistbl.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Einstellungen**](a-msds-settings.md)                                                    | False     | [**Verbindungspunkt**](c-connectionpoint.md)<br/>                                 |
| [**ms-DS-Tasks-for-Az-Role-BL**](a-msds-tasksforazrolebl.md)                                | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Tasks-for-Az-Task-BL**](a-msds-tasksforaztaskbl.md)                                | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-TDO-Egress-BL**](a-msds-tdoegressbl.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-TDO-Ingress-BL**](a-msds-tdoingressbl.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Value-Type-Reference-BL**](a-msds-valuetypereferencebl.md)                         | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                                        | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**MS-SQL-AppleTalk**](a-ms-sql-appletalk.md)                                               | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-Build**](a-ms-sql-build.md)                                                       | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-CharacterSet**](a-ms-sql-characterset.md)                                         | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-Clustered**](a-ms-sql-clustered.md)                                               | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-Contact**](a-ms-sql-contact.md)                                                   | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-GPSHeight**](a-ms-sql-gpsheight.md)                                               | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-GPSLatitude**](a-ms-sql-gpslatitude.md)                                           | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-GPSLongitude**](a-ms-sql-gpslongitude.md)                                         | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-InformationURL**](a-ms-sql-informationurl.md)                                     | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-Keywords**](a-ms-sql-keywords.md)                                                 | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-LastUpdatedDate**](a-ms-sql-lastupdateddate.md)                                   | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-Location**](a-ms-sql-location.md)                                                 | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-Memory**](a-ms-sql-memory.md)                                                     | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-MultiProtocol**](a-ms-sql-multiprotocol.md)                                       | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-Name**](a-ms-sql-name.md)                                                         | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-NamedPipe**](a-ms-sql-namedpipe.md)                                               | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-RegisteredOwner**](a-ms-sql-registeredowner.md)                                   | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-ServiceAccount**](a-ms-sql-serviceaccount.md)                                     | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-SortOrder**](a-ms-sql-sortorder.md)                                               | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-SPX**](a-ms-sql-spx.md)                                                           | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-Status**](a-ms-sql-status.md)                                                     | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-TCPIP**](a-ms-sql-tcpip.md)                                                       | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-UnicodeSortOrder**](a-ms-sql-unicodesortorder.md)                                 | False     | **MS-SQL-SQLServer**                                                                     |
| [**MS-SQL-Vines**](a-ms-sql-vines.md)                                                       | False     | **MS-SQL-SQLServer**                                                                     |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                                     | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Non-Security-Member-BL**](a-nonsecuritymemberbl.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                                     | True      | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                                 | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Objektkategorie**](a-objectcategory.md)                                                  | True      | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Objektklasse**](a-objectclass.md)                                                        | True      | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Objekt-GUID**](a-objectguid.md)                                                          | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Objektversion**](a-objectversion.md)                                                    | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Andere bekannte Objekte**](a-otherwellknownobjects.md)                                  | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)                    | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Mögliche 100000000000**](a-possibleinferiors.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Proxyadressen**](a-proxyaddresses.md)                                                  | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Query-Policy-BL**](a-querypolicybl.md)                                                   | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Rdn**](a-name.md)                                                                        | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                                    | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Berichte**](a-directreports.md)                                                           | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Reps-From**](a-repsfrom.md)                                                              | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Reps-To**](a-repsto.md)                                                                  | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Revision**](a-revision.md)                                                               | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Server-Reference-BL**](a-serverreferencebl.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Dienstbindungsinformationen**](a-servicebindinginformation.md)                           | False     | [**Dienstverbindungspunkt**](c-serviceconnectionpoint.md)<br/>                  |
| [**Service-Class-Name**](a-serviceclassname.md)                                             | False     | [**Dienstverbindungspunkt**](c-serviceconnectionpoint.md)<br/>                  |
| [**Dienst-DNS-Name**](a-servicednsname.md)                                                 | False     | [**Dienstverbindungspunkt**](c-serviceconnectionpoint.md)<br/>                  |
| [**Service-DNS-Name-Type**](a-servicednsnametype.md)                                        | False     | [**Dienstverbindungspunkt**](c-serviceconnectionpoint.md)<br/>                  |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)                               | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Site-Object-BL**](a-siteobjectbl.md)                                                     | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Sub-Refs**](a-subrefs.md)                                                                | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                             | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Systemflags**](a-systemflags.md)                                                        | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**USN-Changed**](a-usnchanged.md)                                                          | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**VON USN erstellt**](a-usncreated.md)                                                          | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**USN-Intersite**](a-usnintersite.md)                                                      | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                                  | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**USN-Quelle**](a-usnsource.md)                                                            | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Hersteller**](a-vendor.md)                                                                   | False     | [**Dienstverbindungspunkt**](c-serviceconnectionpoint.md)<br/>                  |
| [**Versionsnummer**](a-versionnumber.md)                                                    | False     | [**Dienstverbindungspunkt**](c-serviceconnectionpoint.md)<br/>                  |
| [**Versionsnummer-Hi**](a-versionnumberhi.md)                                               | False     | [**Dienstverbindungspunkt**](c-serviceconnectionpoint.md)<br/>                  |
| [**Versionsnummer-Lo**](a-versionnumberlo.md)                                               | False     | [**Dienstverbindungspunkt**](c-serviceconnectionpoint.md)<br/>                  |
| [**Wbem-Pfad**](a-wbempath.md)                                                              | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Bekannte Objekte**](a-wellknownobjects.md)                                             | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Bei Änderung**](a-whenchanged.md)                                                        | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Bei der Erstellung**](a-whencreated.md)                                                        | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**WWW-Startseite**](a-wwwhomepage.md)                                                       | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**WWW-Page-Other**](a-url.md)                                                              | False     | [**Nach oben**](c-top.md)<br/>                                                          |



 

 





