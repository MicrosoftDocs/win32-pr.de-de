---
title: NTDS-DSA-Klasse
description: Stellt den Active Directory DSA-Prozess auf dem Server dar.
ms.assetid: f4369122-d74a-45d2-9dc0-46894a9f99cc
ms.tgt_platform: multiple
keywords:
- AD-Schema der NTDS-DSA-Klasse
- AD-Schema der nTDSDSA-Klasse
topic_type:
- apiref
api_name:
- NTDS-DSA
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 284b04027b97be0a8808f45ff61707d6b56b054786272e8d46d32f92d43c5448
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119753440"
---
# <a name="ntds-dsa-class"></a>NTDS-DSA-Klasse

Stellt den Active Directory DSA-Prozess auf dem Server dar.



| Eingabe | Wert |
|-------------------|--------------------------------------|
| CN                | NTDS-DSA                             |
| Ldap-Anzeigename | nTDSDSA                              |
| Aktualisieren von Berechtigungen  | \-                                   |
| Updatehäufigkeit  | \-                                   |
| Schema-ID-GUID    | f0f8ffab-1191-11d0-a060-00aa006c33ed |



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
-   [Erweiterte Rechte](#windows-2000-server-extended-rights)



| Eingabe | Wert |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Richtig                                                                                         |
| Object-Category             | 1                                                                                            |
| Default-Object-Category     | \-                                                                                           |
| Governs-Id                  | 1.2.840.113556.1.5.7000.47                                                                   |
| Default-Hiding-Value        | 1                                                                                            |
| Rdn-Att-Id                  | [**Allgemeiner Name**](a-cn.md)<br/>                                                       |
| Unterklasse von                 | [**Anwendungs-Einstellungen**](c-applicationsettings.md)<br/>                             |
| Mögliche Übergeordnete          | [**Serverorganisation**](c-server.md)[](c-organization.md)                             |
| Zusätzlich           | \-                                                                                           |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                 |
| Standardsicherheitsdeskriptor | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;;; AU) |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-2000-server-attributes"></a>Windows 2000-Serverattribute

Diese Klasse enthält die folgenden Attribute für Windows 2000 Server:



| attribute                                                                 | Obligatorisch. | Abgeleitet von                                                     |
|---------------------------------------------------------------------------|-----------|------------------------------------------------------------------|
| [**Administratorbeschreibung**](a-admindescription.md)                           | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Admin-Display-Name**](a-admindisplayname.md)                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Allowed-Attributes**](a-allowedattributes.md)                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)      | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md) | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Anwendungsname**](a-applicationname.md)                             | Falsch     | [**Anwendungs-Einstellungen**](c-applicationsettings.md)<br/> |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)             | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Kanonischer Name**](a-canonicalname.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Allgemeiner Name**](a-cn.md)                                               | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Erstellen eines Zeitstempels**](a-createtimestamp.md)                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Beschreibung**](a-description.md)                                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Anzeigename**](a-displayname.md)                                     | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Anzeigename– druckbar**](a-displaynameprintable.md)                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**DMD-Location**](a-dmdlocation.md)                                     | Falsch     | **NTDS-DSA**                                                     |
| [**DSA-Signature**](a-dsasignature.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**DS-Core-Propagierungsdaten**](a-dscorepropagationdata.md)               | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Erweiterungsname**](a-extensionname.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Flaggen**](a-flags.md)                                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**From-Entry**](a-fromentry.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)             | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**FRS-Root-Path**](a-frsrootpath.md)                                    | Falsch     | **NTDS-DSA**                                                     |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Has-Master-NCs**](a-hasmasterncs.md)                                  | Falsch     | **NTDS-DSA**                                                     |
| [**Has-Partial-Replica-NCs**](a-haspartialreplicancs.md)                 | Falsch     | **NTDS-DSA**                                                     |
| [**Instanztyp**](a-instancetype.md)                                   | Richtig      | [**Nach oben**](c-top.md)<br/>                                  |
| [**Aufruf-ID**](a-invocationid.md)                                   | Falsch     | **NTDS-DSA**                                                     |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)             | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Is-Deleted**](a-isdeleted.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Is-Member-of-DL**](a-memberof.md)                                     | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Zeitpunkt der letzten Sicherung und Wiederherstellung**](a-lastbackuprestorationtime.md)       | Falsch     | **NTDS-DSA**                                                     |
| [**Last-Known-Parent**](a-lastknownparent.md)                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Verwaltet von**](a-managedby.md)                                         | Falsch     | **NTDS-DSA**                                                     |
| [**Verwaltete Objekte**](a-managedobjects.md)                               | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Mastered-By**](a-masteredby.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Modify-Time-Stamp**](a-modifytimestamp.md)                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)    | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Netzwerkadresse**](a-networkaddress.md)                               | Falsch     | **NTDS-DSA**                                                     |
| [**Non-Security-Member-BL**](a-nonsecuritymemberbl.md)                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Benachrichtigungsliste**](a-notificationlist.md)                           | Falsch     | [**Anwendungs-Einstellungen**](c-applicationsettings.md)<br/> |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                  | Richtig      | [**Nach oben**](c-top.md)<br/>                                  |
| [**Obj-Dist-Name**](a-distinguishedname.md)                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Objektkategorie**](a-objectcategory.md)                               | Richtig      | [**Nach oben**](c-top.md)<br/>                                  |
| [**Objektklasse**](a-objectclass.md)                                     | Richtig      | [**Nach oben**](c-top.md)<br/>                                  |
| [**Objekt-GUID**](a-objectguid.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Object-Version**](a-objectversion.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Optionen**](a-options.md)                                              | Falsch     | **NTDS-DSA**                                                     |
| [**Andere bekannte Objekte**](a-otherwellknownobjects.md)               | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md) | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Mögliche 100000000000**](a-possibleinferiors.md)                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Proxyadressen**](a-proxyaddresses.md)                               | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Query-Policy-BL**](a-querypolicybl.md)                                | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Query-Policy-Object**](a-querypolicyobject.md)                        | Falsch     | **NTDS-DSA**                                                     |
| [**Rdn**](a-name.md)                                                     | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Berichte**](a-directreports.md)                                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Reps-From**](a-repsfrom.md)                                           | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Reps-To**](a-repsto.md)                                               | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Retired-Repl-DSA-Signatures**](a-retiredrepldsasignatures.md)         | Falsch     | **NTDS-DSA**                                                     |
| [**Revision**](a-revision.md)                                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Serverreferenz**](a-serverreference.md)                             | Falsch     | **NTDS-DSA**                                                     |
| [**Server-Reference-BL**](a-serverreferencebl.md)                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)            | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Site-Object-BL**](a-siteobjectbl.md)                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Sub-Refs**](a-subrefs.md)                                             | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Systemflags**](a-systemflags.md)                                     | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**USN-Changed**](a-usnchanged.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**VON USN erstellt**](a-usncreated.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**USN-Intersite**](a-usnintersite.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                               | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**USN-Quelle**](a-usnsource.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Wbem-Path**](a-wbempath.md)                                           | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Bekannte Objekte**](a-wellknownobjects.md)                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Wenn geändert**](a-whenchanged.md)                                     | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Wenn erstellt**](a-whencreated.md)                                     | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**WWW-Homepage**](a-wwwhomepage.md)                                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**WWW-Page-Other**](a-url.md)                                           | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |



## <a name="windows-2000-server-extended-rights"></a>Windows 2000 Server Extended Rights

Diese Klasse enthält die folgenden erweiterten Rechte für Windows 2000-Server:



| Allgemeiner Name                                                                    |
|--------------------------------------------------------------------------------|
| [**Abbruchreplikation**](r-abandon-replication.md)                           |
| [**Do-Garbage Collection**](r-do-garbage-collection.md)                       |
| [**Neuberechnungshierarchie**](r-recalculate-hierarchy.md)                       |
| [**Allocate-Rids**](r-allocate-rids.md)                                       |
| [**Neuberechnung der Sicherheitsvererbung**](r-recalculate-security-inheritance.md) |
| [**DS-Check-Stale-Phantoms**](r-ds-check-stale-phantoms.md)                   |



## <a name="windows-server-2003"></a>Windows Server 2003

-   [Attribute](#windows-server-2003-attributes)
-   [Erweiterte Rechte](#windows-server-2003-extended-rights)



| Eingabe | Wert |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Richtig                                                                                         |
| Object-Category             | 1                                                                                            |
| Default-Object-Category     | \-                                                                                           |
| Governs-Id                  | 1.2.840.113556.1.5.7000.47                                                                   |
| Default-Hiding-Value        | 1                                                                                            |
| Rdn-Att-Id                  | [**Common-Name**](a-cn.md)<br/>                                                       |
| Unterklasse von                 | [**Anwendungs-Einstellungen**](c-applicationsettings.md)<br/>                             |
| Mögliche Vorgesetzte          | [**Serverorganisation**](c-server.md)[](c-organization.md)                             |
| Zusätzlich           | \-                                                                                           |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                 |
| Standardsicherheitsdeskriptor | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;;; AU) |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2003-attributes"></a>Windows Server 2003-Attribute

Diese Klasse enthält die folgenden Attribute für Windows Server 2003:



| attribute                                                                   | Obligatorisch. | Abgeleitet von                                                     |
|-----------------------------------------------------------------------------|-----------|------------------------------------------------------------------|
| [**Admin-Description**](a-admindescription.md)                             | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Administratoranzeigename**](a-admindisplayname.md)                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Allowed-Attributes**](a-allowedattributes.md)                           | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)        | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)   | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Anwendungsname**](a-applicationname.md)                               | Falsch     | [**Anwendungs-Einstellungen**](c-applicationsettings.md)<br/> |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)               | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Kanonischer Name**](a-canonicalname.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Common-Name**](a-cn.md)                                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Create-Time-Stamp**](a-createtimestamp.md)                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Beschreibung**](a-description.md)                                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Anzeigename**](a-displayname.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Display-Name-Printable**](a-displaynameprintable.md)                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**DMD-Location**](a-dmdlocation.md)                                       | Falsch     | **NTDS-DSA**                                                     |
| [**DSA-Signature**](a-dsasignature.md)                                     | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**DS-Core-Propagierungsdaten**](a-dscorepropagationdata.md)                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Erweiterungsname**](a-extensionname.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Flaggen**](a-flags.md)                                                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**From-Entry**](a-fromentry.md)                                           | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)               | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**FRS-Root-Path**](a-frsrootpath.md)                                      | Falsch     | **NTDS-DSA**                                                     |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Has-Master-NCs**](a-hasmasterncs.md)                                    | Falsch     | **NTDS-DSA**                                                     |
| [**Has-Partial-Replica-NCs**](a-haspartialreplicancs.md)                   | Falsch     | **NTDS-DSA**                                                     |
| [**Instanztyp**](a-instancetype.md)                                     | Richtig      | [**Nach oben**](c-top.md)<br/>                                  |
| [**Aufruf-ID**](a-invocationid.md)                                     | Falsch     | **NTDS-DSA**                                                     |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)               | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Is-Deleted**](a-isdeleted.md)                                           | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Is-Member-of-DL**](a-memberof.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Zeitpunkt der letzten Sicherung und Wiederherstellung**](a-lastbackuprestorationtime.md)         | Falsch     | **NTDS-DSA**                                                     |
| [**Last-Known-Parent**](a-lastknownparent.md)                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Verwaltet von**](a-managedby.md)                                           | Falsch     | **NTDS-DSA**                                                     |
| [**Verwaltete Objekte**](a-managedobjects.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Mastered-By**](a-masteredby.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Modify-Time-Stamp**](a-modifytimestamp.md)                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md) | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-Behavior-Version**](a-msds-behavior-version.md)                   | Falsch     | **NTDS-DSA**                                                     |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)      | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-Has-Domain-NCs**](a-msds-hasdomainncs.md)                         | Falsch     | **NTDS-DSA**                                                     |
| [**ms-DS-Has-Instantiated-NCs**](a-msds-hasinstantiatedncs.md)             | Falsch     | **NTDS-DSA**                                                     |
| [**ms-DS-Has-Master-NCs**](a-msds-hasmasterncs.md)                         | Falsch     | **NTDS-DSA**                                                     |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-Members-For-Az-Role-BL**](a-msds-membersforazrolebl.md)           | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)    | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)  | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)               | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)     | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)     | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)      | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-ReplicationEpoch**](a-msds-replicationepoch.md)                   | Falsch     | **NTDS-DSA**                                                     |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)              | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-Retired-Repl-NC-Signatures**](a-msds-retiredreplncsignatures.md)  | Falsch     | **NTDS-DSA**                                                     |
| [**ms-DS-Einstellungen**](a-msds-settings.md)                                   | Falsch     | [**Anwendungsbasierte Einstellungen**](c-applicationsettings.md)<br/> |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)               | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)               | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Netzwerkadresse**](a-networkaddress.md)                                 | Falsch     | **NTDS-DSA**                                                     |
| [**Non-Security-Member-BL**](a-nonsecuritymemberbl.md)                     | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Benachrichtigungsliste**](a-notificationlist.md)                             | Falsch     | [**Anwendungsbasierte Einstellungen**](c-applicationsettings.md)<br/> |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                    | Richtig      | [**Nach oben**](c-top.md)<br/>                                  |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Objektkategorie**](a-objectcategory.md)                                 | Richtig      | [**Nach oben**](c-top.md)<br/>                                  |
| [**Object-Class**](a-objectclass.md)                                       | Richtig      | [**Nach oben**](c-top.md)<br/>                                  |
| [**Objekt-GUID**](a-objectguid.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Object-Version**](a-objectversion.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Optionen**](a-options.md)                                                | Falsch     | **NTDS-DSA**                                                     |
| [**Andere bekannte Objekte**](a-otherwellknownobjects.md)                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)   | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Mögliche 100000000000**](a-possibleinferiors.md)                           | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Proxyadressen**](a-proxyaddresses.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Query-Policy-BL**](a-querypolicybl.md)                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Query-Policy-Object**](a-querypolicyobject.md)                          | Falsch     | **NTDS-DSA**                                                     |
| [**Rdn**](a-name.md)                                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Berichte**](a-directreports.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Reps-From**](a-repsfrom.md)                                             | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Reps-To**](a-repsto.md)                                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Retired-Repl-DSA-Signatures**](a-retiredrepldsasignatures.md)           | Falsch     | **NTDS-DSA**                                                     |
| [**Revision**](a-revision.md)                                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Serverreferenz**](a-serverreference.md)                               | Falsch     | **NTDS-DSA**                                                     |
| [**Server-Reference-BL**](a-serverreferencebl.md)                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Nur in erweiterter Ansicht anzeigen**](a-showinadvancedviewonly.md)              | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Sub-Refs**](a-subrefs.md)                                               | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Systemflags**](a-systemflags.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**USN geändert**](a-usnchanged.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**USN-erstellt**](a-usncreated.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**USN-DSA-last-obj-removed**](a-usndsalastobjremoved.md)                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**USN-Intersite**](a-usnintersite.md)                                     | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**USN-Quelle**](a-usnsource.md)                                           | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Wbem-Pfad**](a-wbempath.md)                                             | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Bekannte Objekte**](a-wellknownobjects.md)                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Bei Änderung**](a-whenchanged.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Bei der Erstellung**](a-whencreated.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**WWW-Startseite**](a-wwwhomepage.md)                                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**WWW-Page-Other**](a-url.md)                                             | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |



## <a name="windows-server-2003-extended-rights"></a>Windows Erweiterte Rechte für Server 2003

Diese Klasse enthält die folgenden erweiterten Rechte für Windows Server 2003:



| Allgemeiner Name                                                                    |
|--------------------------------------------------------------------------------|
| [**Do-Garbage Collection**](r-do-garbage-collection.md)                       |
| [**Neuberechnung der Hierarchie**](r-recalculate-hierarchy.md)                       |
| [**Allocate-Rids**](r-allocate-rids.md)                                       |
| [**Neuberechnung der Sicherheitsvererbung**](r-recalculate-security-inheritance.md) |
| [**DS-Check-Stale-Phantoms**](r-ds-check-stale-phantoms.md)                   |
| [**Refresh-Group-Cache**](r-refresh-group-cache.md)                           |



## <a name="adam"></a>Adam

-   [Attribute](#adam-attributes)
-   [Erweiterte Rechte](#adam-extended-rights)



| Eingabe | Wert |
|-----------------------------|------------------------------------------------------------------|
| System-Only                 | Richtig                                                             |
| Object-Category             | 1                                                                |
| Default-Object-Category     | \-                                                               |
| Governs-Id                  | 1.2.840.113556.1.5.7000.47                                       |
| Default-Hiding-Value        | 1                                                                |
| Rdn-Att-Id                  | [**Allgemeiner Name**](a-cn.md)<br/>                           |
| Unterklasse von                 | [**Anwendungs-Einstellungen**](c-applicationsettings.md)<br/> |
| Mögliche Übergeordnete          | [**Serverorganisation**](c-server.md)[](c-organization.md) |
| Zusätzlich           | \-                                                               |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                     |
| Standardsicherheitsdeskriptor | D:S:                                                             |
| System-Flags                | 0x00000010                                                       |



## <a name="adam-attributes"></a>ADAM-Attribute

Diese Klasse enthält die folgenden Attribute für ADAM:



| attribute                                                                   | Obligatorisch. | Abgeleitet von                                                     |
|-----------------------------------------------------------------------------|-----------|------------------------------------------------------------------|
| [**Administratorbeschreibung**](a-admindescription.md)                             | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Admin-Display-Name**](a-admindisplayname.md)                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Allowed-Attributes**](a-allowedattributes.md)                           | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)        | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)   | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)               | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Kanonischer Name**](a-canonicalname.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Allgemeiner Name**](a-cn.md)                                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Erstellen eines Zeitstempels**](a-createtimestamp.md)                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Beschreibung**](a-description.md)                                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Anzeigename**](a-displayname.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**DMD-Location**](a-dmdlocation.md)                                       | Falsch     | **NTDS-DSA**                                                     |
| [**DSA-Signature**](a-dsasignature.md)                                     | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**DS-Core-Propagierungsdaten**](a-dscorepropagationdata.md)                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**From-Entry**](a-fromentry.md)                                           | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Has-Master-NCs**](a-hasmasterncs.md)                                    | Falsch     | **NTDS-DSA**                                                     |
| [**Has-Partial-Replica-NCs**](a-haspartialreplicancs.md)                   | Falsch     | **NTDS-DSA**                                                     |
| [**Instanztyp**](a-instancetype.md)                                     | Richtig      | [**Nach oben**](c-top.md)<br/>                                  |
| [**Aufruf-ID**](a-invocationid.md)                                     | Falsch     | **NTDS-DSA**                                                     |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)               | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Is-Deleted**](a-isdeleted.md)                                           | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Is-Member-of-DL**](a-memberof.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Zeitpunkt der letzten Sicherung und Wiederherstellung**](a-lastbackuprestorationtime.md)         | Falsch     | **NTDS-DSA**                                                     |
| [**Last-Known-Parent**](a-lastknownparent.md)                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Verwaltet von**](a-managedby.md)                                           | Falsch     | **NTDS-DSA**                                                     |
| [**Verwaltete Objekte**](a-managedobjects.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Mastered-By**](a-masteredby.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Modify-Time-Stamp**](a-modifytimestamp.md)                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md) | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-Behavior-Version**](a-msds-behavior-version.md)                   | Falsch     | **NTDS-DSA**                                                     |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)      | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-Disable-For-Instances-BL**](a-msds-disableforinstancesbl.md)      | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-Has-Domain-NCs**](a-msds-hasdomainncs.md)                         | Falsch     | **NTDS-DSA**                                                     |
| [**ms-DS-Has-Instantiated-NCs**](a-msds-hasinstantiatedncs.md)             | Falsch     | **NTDS-DSA**                                                     |
| [**ms-DS-Has-Master-NCs**](a-msds-hasmasterncs.md)                         | Falsch     | **NTDS-DSA**                                                     |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)    | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)  | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-Port-LDAP**](a-msds-portldap.md)                                  | Falsch     | **NTDS-DSA**                                                     |
| [**ms-DS-Port-SSL**](a-msds-portssl.md)                                    | Falsch     | **NTDS-DSA**                                                     |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)      | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-ReplicationEpoch**](a-msds-replicationepoch.md)                   | Falsch     | **NTDS-DSA**                                                     |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)              | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-Retired-Repl-NC-Signatures**](a-msds-retiredreplncsignatures.md)  | Falsch     | **NTDS-DSA**                                                     |
| [**ms-DS-Service-Account**](a-msds-serviceaccount.md)                      | Falsch     | **NTDS-DSA**                                                     |
| [**ms-DS-Service-Account-BL**](a-msds-serviceaccountbl.md)                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-Service-Account-DNS-Domain**](a-msds-serviceaccountdnsdomain.md)  | Falsch     | **NTDS-DSA**                                                     |
| [**ms-DS-Einstellungen**](a-msds-settings.md)                                   | Falsch     | [**Anwendungs-Einstellungen**](c-applicationsettings.md)<br/> |
| [**Netzwerkadresse**](a-networkaddress.md)                                 | Falsch     | **NTDS-DSA**                                                     |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                    | Richtig      | [**Nach oben**](c-top.md)<br/>                                  |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Objektkategorie**](a-objectcategory.md)                                 | Richtig      | [**Nach oben**](c-top.md)<br/>                                  |
| [**Objektklasse**](a-objectclass.md)                                       | Richtig      | [**Nach oben**](c-top.md)<br/>                                  |
| [**Objekt-GUID**](a-objectguid.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Objektversion**](a-objectversion.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Optionen**](a-options.md)                                                | Falsch     | **NTDS-DSA**                                                     |
| [**Andere bekannte Objekte**](a-otherwellknownobjects.md)                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Teilattributlöschungsliste**](a-partialattributedeletionlist.md)   | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Teilattributsatz**](a-partialattributeset.md)                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Mögliche Hindernisse**](a-possibleinferiors.md)                           | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Proxyadressen**](a-proxyaddresses.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Query-Policy-BL**](a-querypolicybl.md)                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Query-Policy-Object**](a-querypolicyobject.md)                          | Falsch     | **NTDS-DSA**                                                     |
| [**Rdn**](a-name.md)                                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Reps-From**](a-repsfrom.md)                                             | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Reps-To**](a-repsto.md)                                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Retired-Repl-DSA-Signatures**](a-retiredrepldsasignatures.md)           | Falsch     | **NTDS-DSA**                                                     |
| [**Revision**](a-revision.md)                                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Serverreferenz**](a-serverreference.md)                               | Falsch     | **NTDS-DSA**                                                     |
| [**Server-Reference-BL**](a-serverreferencebl.md)                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Nur in erweiterter Ansicht anzeigen**](a-showinadvancedviewonly.md)              | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Sub-Refs**](a-subrefs.md)                                               | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Systemflags**](a-systemflags.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**USN geändert**](a-usnchanged.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**USN-erstellt**](a-usncreated.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**USN-DSA-last-obj-removed**](a-usndsalastobjremoved.md)                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**USN-Intersite**](a-usnintersite.md)                                     | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**USN-Quelle**](a-usnsource.md)                                           | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Wbem-Pfad**](a-wbempath.md)                                             | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Bekannte Objekte**](a-wellknownobjects.md)                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Bei Änderung**](a-whenchanged.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Bei der Erstellung**](a-whencreated.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**WWW-Startseite**](a-wwwhomepage.md)                                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**WWW-Page-Other**](a-url.md)                                             | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |



## <a name="adam-extended-rights"></a>ADAM Extended Rights

Diese Klasse enthält die folgenden erweiterten Rechte für ADAM:



| Allgemeiner Name                                                                    |
|--------------------------------------------------------------------------------|
| [**Do-Garbage Collection**](r-do-garbage-collection.md)                       |
| [**Neuberechnung der Sicherheitsvererbung**](r-recalculate-security-inheritance.md) |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2

-   [Attribute](#windows-server-2003-r2-attributes)
-   [Erweiterte Rechte](#windows-server-2003-r2-extended-rights)



| Eingabe | Wert |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Richtig                                                                                         |
| Object-Category             | 1                                                                                            |
| Default-Object-Category     | \-                                                                                           |
| Governs-Id                  | 1.2.840.113556.1.5.7000.47                                                                   |
| Default-Hiding-Value        | 1                                                                                            |
| Rdn-Att-Id                  | [**Allgemeiner Name**](a-cn.md)<br/>                                                       |
| Unterklasse von                 | [**Anwendungs-Einstellungen**](c-applicationsettings.md)<br/>                             |
| Mögliche Übergeordnete          | [**Serverorganisation**](c-server.md)[](c-organization.md)                             |
| Zusätzlich           | \-                                                                                           |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                 |
| Standardsicherheitsdeskriptor | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;;; AU) |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2003-r2-attributes"></a>Windows Server 2003 R2-Attribute

Diese Klasse enthält die folgenden Attribute für Windows Server 2003 R2:



| attribute                                                                   | Obligatorisch. | Abgeleitet von                                                     |
|-----------------------------------------------------------------------------|-----------|------------------------------------------------------------------|
| [**Administratorbeschreibung**](a-admindescription.md)                             | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Admin-Display-Name**](a-admindisplayname.md)                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Allowed-Attributes**](a-allowedattributes.md)                           | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)        | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)   | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Anwendungsname**](a-applicationname.md)                               | Falsch     | [**Anwendungs-Einstellungen**](c-applicationsettings.md)<br/> |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)               | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Kanonischer Name**](a-canonicalname.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Allgemeiner Name**](a-cn.md)                                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Erstellen eines Zeitstempels**](a-createtimestamp.md)                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Beschreibung**](a-description.md)                                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Anzeigename**](a-displayname.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Anzeigename– druckbar**](a-displaynameprintable.md)                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**DMD-Location**](a-dmdlocation.md)                                       | Falsch     | **NTDS-DSA**                                                     |
| [**DSA-Signature**](a-dsasignature.md)                                     | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**DS-Core-Propagierungsdaten**](a-dscorepropagationdata.md)                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Extension-Name**](a-extensionname.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Flaggen**](a-flags.md)                                                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**From-Entry**](a-fromentry.md)                                           | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)               | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**FRS-Root-Path**](a-frsrootpath.md)                                      | Falsch     | **NTDS-DSA**                                                     |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Has-Master-NCs**](a-hasmasterncs.md)                                    | Falsch     | **NTDS-DSA**                                                     |
| [**Has-Partial-Replica-NCs**](a-haspartialreplicancs.md)                   | Falsch     | **NTDS-DSA**                                                     |
| [**Instanztyp**](a-instancetype.md)                                     | Richtig      | [**Nach oben**](c-top.md)<br/>                                  |
| [**Aufruf-ID**](a-invocationid.md)                                     | Falsch     | **NTDS-DSA**                                                     |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)               | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Is-Deleted**](a-isdeleted.md)                                           | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Is-Member-of-DL**](a-memberof.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Zeitpunkt der letzten Sicherungswiederherstellung**](a-lastbackuprestorationtime.md)         | Falsch     | **NTDS-DSA**                                                     |
| [**Letztes bekanntes übergeordnetes Element**](a-lastknownparent.md)                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Verwaltet von**](a-managedby.md)                                           | Falsch     | **NTDS-DSA**                                                     |
| [**Verwaltete Objekte**](a-managedobjects.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Mastered By**](a-masteredby.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Modify-Time-Stamp**](a-modifytimestamp.md)                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)         | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)             | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md) | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-Behavior-Version**](a-msds-behavior-version.md)                   | Falsch     | **NTDS-DSA**                                                     |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)      | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-Has-Domain-NCs**](a-msds-hasdomainncs.md)                         | Falsch     | **NTDS-DSA**                                                     |
| [**ms-DS-Has-Instantiated-NCs**](a-msds-hasinstantiatedncs.md)             | Falsch     | **NTDS-DSA**                                                     |
| [**ms-DS-Has-Master-NCs**](a-msds-hasmasterncs.md)                         | Falsch     | **NTDS-DSA**                                                     |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-Members-For-Az-Role-BL**](a-msds-membersforazrolebl.md)           | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)    | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)  | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)               | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)     | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)     | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)      | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-ReplicationEpoch**](a-msds-replicationepoch.md)                   | Falsch     | **NTDS-DSA**                                                     |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)              | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-Retired-Repl-NC-Signatures**](a-msds-retiredreplncsignatures.md)  | Falsch     | **NTDS-DSA**                                                     |
| [**ms-DS-Einstellungen**](a-msds-settings.md)                                   | Falsch     | [**Anwendungsbasierte Einstellungen**](c-applicationsettings.md)<br/> |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)               | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)               | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Netzwerkadresse**](a-networkaddress.md)                                 | Falsch     | **NTDS-DSA**                                                     |
| [**Non-Security-Member-BL**](a-nonsecuritymemberbl.md)                     | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Benachrichtigungsliste**](a-notificationlist.md)                             | Falsch     | [**Anwendungsbasierte Einstellungen**](c-applicationsettings.md)<br/> |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                    | Richtig      | [**Nach oben**](c-top.md)<br/>                                  |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Objektkategorie**](a-objectcategory.md)                                 | Richtig      | [**Nach oben**](c-top.md)<br/>                                  |
| [**Object-Class**](a-objectclass.md)                                       | Richtig      | [**Nach oben**](c-top.md)<br/>                                  |
| [**Objekt-GUID**](a-objectguid.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Object-Version**](a-objectversion.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Optionen**](a-options.md)                                                | Falsch     | **NTDS-DSA**                                                     |
| [**Andere bekannte Objekte**](a-otherwellknownobjects.md)                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)   | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Mögliche 100000000000**](a-possibleinferiors.md)                           | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Proxyadressen**](a-proxyaddresses.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Query-Policy-BL**](a-querypolicybl.md)                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Query-Policy-Object**](a-querypolicyobject.md)                          | Falsch     | **NTDS-DSA**                                                     |
| [**Rdn**](a-name.md)                                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Berichte**](a-directreports.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Reps-From**](a-repsfrom.md)                                             | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Reps-To**](a-repsto.md)                                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Retired-Repl-DSA-Signatures**](a-retiredrepldsasignatures.md)           | Falsch     | **NTDS-DSA**                                                     |
| [**Revision**](a-revision.md)                                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Serverreferenz**](a-serverreference.md)                               | Falsch     | **NTDS-DSA**                                                     |
| [**Server-Reference-BL**](a-serverreferencebl.md)                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)              | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Sub-Refs**](a-subrefs.md)                                               | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Systemflags**](a-systemflags.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**USN-Changed**](a-usnchanged.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**VON USN erstellt**](a-usncreated.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**USN-Intersite**](a-usnintersite.md)                                     | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**USN-Quelle**](a-usnsource.md)                                           | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Wbem-Path**](a-wbempath.md)                                             | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Bekannte Objekte**](a-wellknownobjects.md)                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Wenn geändert**](a-whenchanged.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Wenn erstellt**](a-whencreated.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**WWW-Homepage**](a-wwwhomepage.md)                                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**WWW-Page-Other**](a-url.md)                                             | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |



## <a name="windows-server-2003-r2-extended-rights"></a>Windows Erweiterte Rechte für Server 2003 R2

Diese Klasse enthält die folgenden erweiterten Rechte für Windows Server 2003 R2:



| Allgemeiner Name                                                                    |
|--------------------------------------------------------------------------------|
| [**Do-Garbage Collection**](r-do-garbage-collection.md)                       |
| [**Neuberechnung der Hierarchie**](r-recalculate-hierarchy.md)                       |
| [**Allocate-Rids**](r-allocate-rids.md)                                       |
| [**Neuberechnung der Sicherheitsvererbung**](r-recalculate-security-inheritance.md) |
| [**DS-Check-Stale-Phantoms**](r-ds-check-stale-phantoms.md)                   |
| [**Refresh-Group-Cache**](r-refresh-group-cache.md)                           |



## <a name="windows-server-2008"></a>Windows Server 2008

-   [Attribute](#windows-server-2008-attributes)
-   [Erweiterte Rechte](#windows-server-2008-extended-rights)



| Eingabe | Wert |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Richtig                                                                                         |
| Object-Category             | 1                                                                                            |
| Default-Object-Category     | \-                                                                                           |
| Governs-Id                  | 1.2.840.113556.1.5.7000.47                                                                   |
| Default-Hiding-Value        | 1                                                                                            |
| Rdn-Att-Id                  | [**Allgemeiner Name**](a-cn.md)<br/>                                                       |
| Unterklasse von                 | [**Anwendungs-Einstellungen**](c-applicationsettings.md)<br/>                             |
| Mögliche Übergeordnete          | [**Serverorganisation**](c-server.md)[](c-organization.md)                             |
| Zusätzlich           | \-                                                                                           |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                 |
| Standardsicherheitsdeskriptor | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;;; AU) |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2008-attributes"></a>Windows Server 2008-Attribute

Diese Klasse enthält die folgenden Attribute für Windows Server 2008:



| attribute                                                                      | Obligatorisch. | Abgeleitet von                                                     |
|--------------------------------------------------------------------------------|-----------|------------------------------------------------------------------|
| [**Administratorbeschreibung**](a-admindescription.md)                                | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Admin-Display-Name**](a-admindisplayname.md)                               | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Allowed-Attributes**](a-allowedattributes.md)                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)           | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)      | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Anwendungsname**](a-applicationname.md)                                  | Falsch     | [**Anwendungs-Einstellungen**](c-applicationsettings.md)<br/> |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Kanonischer Name**](a-canonicalname.md)                                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Allgemeiner Name**](a-cn.md)                                                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Erstellen eines Zeitstempels**](a-createtimestamp.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Beschreibung**](a-description.md)                                           | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Anzeigename**](a-displayname.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Anzeigename– druckbar**](a-displaynameprintable.md)                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**DMD-Location**](a-dmdlocation.md)                                          | Falsch     | **NTDS-DSA**                                                     |
| [**DSA-Signature**](a-dsasignature.md)                                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**DS-Core-Propagierungsdaten**](a-dscorepropagationdata.md)                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Erweiterungsname**](a-extensionname.md)                                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Flaggen**](a-flags.md)                                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**From-Entry**](a-fromentry.md)                                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**FRS-Root-Path**](a-frsrootpath.md)                                         | Falsch     | **NTDS-DSA**                                                     |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                     | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Has-Master-NCs**](a-hasmasterncs.md)                                       | Falsch     | **NTDS-DSA**                                                     |
| [**Has-Partial-Replica-NCs**](a-haspartialreplicancs.md)                      | Falsch     | **NTDS-DSA**                                                     |
| [**Instanztyp**](a-instancetype.md)                                        | Richtig      | [**Nach oben**](c-top.md)<br/>                                  |
| [**Aufruf-ID**](a-invocationid.md)                                        | Falsch     | **NTDS-DSA**                                                     |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Is-Deleted**](a-isdeleted.md)                                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Is-Member-of-DL**](a-memberof.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                             | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Zeitpunkt der letzten Sicherungswiederherstellung**](a-lastbackuprestorationtime.md)            | Falsch     | **NTDS-DSA**                                                     |
| [**Letztes bekanntes übergeordnetes Element**](a-lastknownparent.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Verwaltet von**](a-managedby.md)                                              | Falsch     | **NTDS-DSA**                                                     |
| [**Verwaltete Objekte**](a-managedobjects.md)                                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Mastered By**](a-masteredby.md)                                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Modify-Time-Stamp**](a-modifytimestamp.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)            | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md)    | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md) | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-Behavior-Version**](a-msds-behavior-version.md)                      | Falsch     | **NTDS-DSA**                                                     |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)         | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-Has-Domain-NCs**](a-msds-hasdomainncs.md)                            | Falsch     | **NTDS-DSA**                                                     |
| [**ms-DS-Has-Full-Replica-NCs**](a-msds-hasfullreplicancs.md)                 | Falsch     | **NTDS-DSA**                                                     |
| [**ms-DS-Has-Instantiated-NCs**](a-msds-hasinstantiatedncs.md)                | Falsch     | **NTDS-DSA**                                                     |
| [**ms-DS-Has-Master-NCs**](a-msds-hasmasterncs.md)                            | Falsch     | **NTDS-DSA**                                                     |
| [**ms-DS-is-Domain-for**](a-msds-isdomainfor.md)                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-is-full-replica-for**](a-msds-isfullreplicafor.md)                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-isGC**](a-msds-isgc.md)                                              | Falsch     | **NTDS-DSA**                                                     |
| [**ms-DS-is-partial-replica-for**](a-msds-ispartialreplicafor.md)             | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-isRODC**](a-msds-isrodc.md)                                          | Falsch     | **NTDS-DSA**                                                     |
| [**ms-DS-Is-User-Cachable-At-Rodc**](a-msds-isusercachableatrodc.md)          | Falsch     | **NTDS-DSA**                                                     |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-Members-for-Az-Role-BL**](a-msds-membersforazrolebl.md)              | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)       | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)     | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)  | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-NC-Type**](a-msds-nctype.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-Never-Reveal-Group**](a-msds-neverrevealgroup.md)                    | Falsch     | **NTDS-DSA**                                                     |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-Operations-for-Az-Role-BL**](a-msds-operationsforazrolebl.md)        | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-Operations-for-Az-Task-BL**](a-msds-operationsforaztaskbl.md)        | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                           | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-PSO-Applied**](a-msds-psoapplied.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)         | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-ReplicationEpoch**](a-msds-replicationepoch.md)                      | Falsch     | **NTDS-DSA**                                                     |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-Retired-Repl-NC-Signatures**](a-msds-retiredreplncsignatures.md)     | Falsch     | **NTDS-DSA**                                                     |
| [**ms-DS-Revealed-DSAs**](a-msds-revealeddsas.md)                             | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-Revealed-List-BL**](a-msds-revealedlistbl.md)                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-Revealed-Users**](a-msds-revealedusers.md)                           | Falsch     | **NTDS-DSA**                                                     |
| [**ms-DS-Reveal-OnDemand-Group**](a-msds-revealondemandgroup.md)              | Falsch     | **NTDS-DSA**                                                     |
| [**ms-DS-Einstellungen**](a-msds-settings.md)                                      | Falsch     | [**Anwendungs-Einstellungen**](c-applicationsettings.md)<br/> |
| [**ms-DS-SiteName**](a-msds-sitename.md)                                      | Falsch     | **NTDS-DSA**                                                     |
| [**ms-DS-Tasks-for-Az-Role-BL**](a-msds-tasksforazrolebl.md)                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-Tasks-for-Az-Task-BL**](a-msds-tasksforaztaskbl.md)                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                     | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Netzwerkadresse**](a-networkaddress.md)                                    | Falsch     | **NTDS-DSA**                                                     |
| [**Non-Security-Member-BL**](a-nonsecuritymemberbl.md)                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Benachrichtigungsliste**](a-notificationlist.md)                                | Falsch     | [**Anwendungs-Einstellungen**](c-applicationsettings.md)<br/> |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                       | Richtig      | [**Nach oben**](c-top.md)<br/>                                  |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Objektkategorie**](a-objectcategory.md)                                    | Richtig      | [**Nach oben**](c-top.md)<br/>                                  |
| [**Object-Class**](a-objectclass.md)                                          | Richtig      | [**Nach oben**](c-top.md)<br/>                                  |
| [**Objekt-GUID**](a-objectguid.md)                                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Object-Version**](a-objectversion.md)                                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Optionen**](a-options.md)                                                   | Falsch     | **NTDS-DSA**                                                     |
| [**Andere bekannte Objekte**](a-otherwellknownobjects.md)                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)      | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Mögliche 100000000000**](a-possibleinferiors.md)                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                             | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Proxyadressen**](a-proxyaddresses.md)                                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Query-Policy-BL**](a-querypolicybl.md)                                     | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Query-Policy-Object**](a-querypolicyobject.md)                             | Falsch     | **NTDS-DSA**                                                     |
| [**Rdn**](a-name.md)                                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                           | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Berichte**](a-directreports.md)                                             | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Reps-From**](a-repsfrom.md)                                                | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Reps-To**](a-repsto.md)                                                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Retired-Repl-DSA-Signatures**](a-retiredrepldsasignatures.md)              | Falsch     | **NTDS-DSA**                                                     |
| [**Revision**](a-revision.md)                                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                             | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Serverreferenz**](a-serverreference.md)                                  | Falsch     | **NTDS-DSA**                                                     |
| [**Server-Reference-BL**](a-serverreferencebl.md)                             | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Site-Object-BL**](a-siteobjectbl.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                     | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Sub-Refs**](a-subrefs.md)                                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                               | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Systemflags**](a-systemflags.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**USN-Changed**](a-usnchanged.md)                                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**VON USN erstellt**](a-usncreated.md)                                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                     | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**USN-Intersite**](a-usnintersite.md)                                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**USN-Quelle**](a-usnsource.md)                                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Wbem-Path**](a-wbempath.md)                                                | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Bekannte Objekte**](a-wellknownobjects.md)                               | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Wenn geändert**](a-whenchanged.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Wenn erstellt**](a-whencreated.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**WWW-Homepage**](a-wwwhomepage.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**WWW-Page-Other**](a-url.md)                                                | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |



## <a name="windows-server-2008-extended-rights"></a>Windows Erweiterte Server 2008-Rechte

Diese Klasse enthält die folgenden erweiterten Rechte für Windows Server 2008:



| Allgemeiner Name                                                                    |
|--------------------------------------------------------------------------------|
| [**Do-Garbage Collection**](r-do-garbage-collection.md)                       |
| [**Neuberechnungshierarchie**](r-recalculate-hierarchy.md)                       |
| [**Allocate-Rids**](r-allocate-rids.md)                                       |
| [**Neuberechnung der Sicherheitsvererbung**](r-recalculate-security-inheritance.md) |
| [**DS-Check-Stale-Phantoms**](r-ds-check-stale-phantoms.md)                   |
| [**Refresh-Group-Cache**](r-refresh-group-cache.md)                           |
| [**Reload-SSL-Certificate**](r-reload-ssl-certificate.md)                     |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2

-   [Attribute](#windows-server-2008-r2-attributes)
-   [Erweiterte Rechte](#windows-server-2008-r2-extended-rights)



| Eingabe | Wert |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Richtig                                                                                         |
| Object-Category             | 1                                                                                            |
| Default-Object-Category     | \-                                                                                           |
| Governs-Id                  | 1.2.840.113556.1.5.7000.47                                                                   |
| Default-Hiding-Value        | 1                                                                                            |
| Rdn-Att-Id                  | [**Common-Name**](a-cn.md)<br/>                                                       |
| Unterklasse von                 | [**Anwendungs-Einstellungen**](c-applicationsettings.md)<br/>                             |
| Mögliche Vorgesetzte          | [**Serverorganisation**](c-server.md)[](c-organization.md)                             |
| Zusätzlich           | \-                                                                                           |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                 |
| Standardsicherheitsdeskriptor | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;;; AU) |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2008-r2-attributes"></a>Windows Server 2008 R2-Attribute

Diese Klasse enthält die folgenden Attribute für Windows Server 2008 R2:



| attribute                                                                        | Obligatorisch. | Abgeleitet von                                                     |
|----------------------------------------------------------------------------------|-----------|------------------------------------------------------------------|
| [**Admin-Description**](a-admindescription.md)                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Administratoranzeigename**](a-admindisplayname.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Allowed-Attributes**](a-allowedattributes.md)                                | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)             | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                           | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)        | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Anwendungsname**](a-applicationname.md)                                    | Falsch     | [**Anwendungsbasierte Einstellungen**](c-applicationsettings.md)<br/> |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Kanonischer Name**](a-canonicalname.md)                                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Common-Name**](a-cn.md)                                                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Create-Time-Stamp**](a-createtimestamp.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Beschreibung**](a-description.md)                                             | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Anzeigename**](a-displayname.md)                                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Display-Name-Printable**](a-displaynameprintable.md)                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**DMD-Location**](a-dmdlocation.md)                                            | Falsch     | **NTDS-DSA**                                                     |
| [**DSA-Signature**](a-dsasignature.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**DS-Core-Propagierungsdaten**](a-dscorepropagationdata.md)                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Extension-Name**](a-extensionname.md)                                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Flaggen**](a-flags.md)                                                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**From-Entry**](a-fromentry.md)                                                | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**FRS-Root-Path**](a-frsrootpath.md)                                           | Falsch     | **NTDS-DSA**                                                     |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Has-Master-NCs**](a-hasmasterncs.md)                                         | Falsch     | **NTDS-DSA**                                                     |
| [**Has-Partial-Replica-NCs**](a-haspartialreplicancs.md)                        | Falsch     | **NTDS-DSA**                                                     |
| [**Instanztyp**](a-instancetype.md)                                          | Richtig      | [**Nach oben**](c-top.md)<br/>                                  |
| [**Aufruf-ID**](a-invocationid.md)                                          | Falsch     | **NTDS-DSA**                                                     |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Is-Deleted**](a-isdeleted.md)                                                | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Is-Member-of-DL**](a-memberof.md)                                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                               | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Wird wiederverwendet**](a-isrecycled.md)                                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Zeitpunkt der letzten Sicherungswiederherstellung**](a-lastbackuprestorationtime.md)              | Falsch     | **NTDS-DSA**                                                     |
| [**Letztes bekanntes übergeordnetes Element**](a-lastknownparent.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Verwaltet von**](a-managedby.md)                                                | Falsch     | **NTDS-DSA**                                                     |
| [**Verwaltete Objekte**](a-managedobjects.md)                                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Mastered-By**](a-masteredby.md)                                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Modify-Time-Stamp**](a-modifytimestamp.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)              | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md)      | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md)   | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-Behavior-Version**](a-msds-behavior-version.md)                        | Falsch     | **NTDS-DSA**                                                     |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)           | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-Enabled-Feature**](a-msds-enabledfeature.md)                           | Falsch     | **NTDS-DSA**                                                     |
| [**ms-DS-Enabled-Feature-BL**](a-msds-enabledfeaturebl.md)                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-Has-Domain-NCs**](a-msds-hasdomainncs.md)                              | Falsch     | **NTDS-DSA**                                                     |
| [**ms-DS-Has-Full-Replica-NCs**](a-msds-hasfullreplicancs.md)                   | Falsch     | **NTDS-DSA**                                                     |
| [**ms-DS-Has-Instantiated-NCs**](a-msds-hasinstantiatedncs.md)                  | Falsch     | **NTDS-DSA**                                                     |
| [**ms-DS-Has-Master-NCs**](a-msds-hasmasterncs.md)                              | Falsch     | **NTDS-DSA**                                                     |
| [**ms-DS-Host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)             | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-Is-Domain-For**](a-msds-isdomainfor.md)                                | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-is-full-replica-for**](a-msds-isfullreplicafor.md)                     | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-isGC**](a-msds-isgc.md)                                                | Falsch     | **NTDS-DSA**                                                     |
| [**ms-DS-is-partial-replica-for**](a-msds-ispartialreplicafor.md)               | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-isRODC**](a-msds-isrodc.md)                                            | Falsch     | **NTDS-DSA**                                                     |
| [**ms-DS-Is-User-Cachable-At-Rodc**](a-msds-isusercachableatrodc.md)            | Falsch     | **NTDS-DSA**                                                     |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-local-Effective-Deletion-Time**](a-msds-localeffectivedeletiontime.md) | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-local-Effective-Recycle-Time**](a-msds-localeffectiverecycletime.md)   | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-Members-for-Az-Role-BL**](a-msds-membersforazrolebl.md)                | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)         | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)       | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)    | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-NC-Type**](a-msds-nctype.md)                                           | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-Never-Reveal-Group**](a-msds-neverrevealgroup.md)                      | Falsch     | **NTDS-DSA**                                                     |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-OIDToGroup-Link-BL**](a-msds-oidtogrouplinkbl.md)                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-Operations-for-Az-Role-BL**](a-msds-operationsforazrolebl.md)          | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-Operations-for-Az-Task-BL**](a-msds-operationsforaztaskbl.md)          | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                             | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-PSO-Applied**](a-msds-psoapplied.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)           | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-ReplicationEpoch**](a-msds-replicationepoch.md)                        | Falsch     | **NTDS-DSA**                                                     |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-Retired-Repl-NC-Signatures**](a-msds-retiredreplncsignatures.md)       | Falsch     | **NTDS-DSA**                                                     |
| [**ms-DS-Revealed-DSAs**](a-msds-revealeddsas.md)                               | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-Revealed-List-BL**](a-msds-revealedlistbl.md)                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-Revealed-Users**](a-msds-revealedusers.md)                             | Falsch     | **NTDS-DSA**                                                     |
| [**ms-DS-Reveal-OnDemand-Group**](a-msds-revealondemandgroup.md)                | Falsch     | **NTDS-DSA**                                                     |
| [**ms-DS-Einstellungen**](a-msds-settings.md)                                        | Falsch     | [**Anwendungs-Einstellungen**](c-applicationsettings.md)<br/> |
| [**ms-DS-SiteName**](a-msds-sitename.md)                                        | Falsch     | **NTDS-DSA**                                                     |
| [**ms-DS-Tasks-for-Az-Role-BL**](a-msds-tasksforazrolebl.md)                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-Tasks-for-Az-Task-BL**](a-msds-tasksforaztaskbl.md)                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Netzwerkadresse**](a-networkaddress.md)                                      | Falsch     | **NTDS-DSA**                                                     |
| [**Non-Security-Member-BL**](a-nonsecuritymemberbl.md)                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Benachrichtigungsliste**](a-notificationlist.md)                                  | Falsch     | [**Anwendungs-Einstellungen**](c-applicationsettings.md)<br/> |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                         | Richtig      | [**Nach oben**](c-top.md)<br/>                                  |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                     | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Objektkategorie**](a-objectcategory.md)                                      | Richtig      | [**Nach oben**](c-top.md)<br/>                                  |
| [**Objektklasse**](a-objectclass.md)                                            | Richtig      | [**Nach oben**](c-top.md)<br/>                                  |
| [**Objekt-GUID**](a-objectguid.md)                                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Objektversion**](a-objectversion.md)                                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Optionen**](a-options.md)                                                     | Falsch     | **NTDS-DSA**                                                     |
| [**Andere bekannte Objekte**](a-otherwellknownobjects.md)                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Teilattributlöschungsliste**](a-partialattributedeletionlist.md)        | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Teilattributsatz**](a-partialattributeset.md)                           | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Mögliche Hindernisse**](a-possibleinferiors.md)                                | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                               | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Proxyadressen**](a-proxyaddresses.md)                                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Query-Policy-BL**](a-querypolicybl.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Query-Policy-Object**](a-querypolicyobject.md)                               | Falsch     | **NTDS-DSA**                                                     |
| [**Rdn**](a-name.md)                                                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                             | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Berichte**](a-directreports.md)                                               | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Reps-From**](a-repsfrom.md)                                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Reps-To**](a-repsto.md)                                                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Retired-Repl-DSA-Signatures**](a-retiredrepldsasignatures.md)                | Falsch     | **NTDS-DSA**                                                     |
| [**Revision**](a-revision.md)                                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                               | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Serverreferenz**](a-serverreference.md)                                    | Falsch     | **NTDS-DSA**                                                     |
| [**Server-Reference-BL**](a-serverreferencebl.md)                               | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Nur in erweiterter Ansicht anzeigen**](a-showinadvancedviewonly.md)                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Site-Object-BL**](a-siteobjectbl.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Sub-Refs**](a-subrefs.md)                                                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Systemflags**](a-systemflags.md)                                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**USN geändert**](a-usnchanged.md)                                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**USN-erstellt**](a-usncreated.md)                                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**USN-DSA-last-obj-removed**](a-usndsalastobjremoved.md)                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**USN-Intersite**](a-usnintersite.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**USN-Quelle**](a-usnsource.md)                                                | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Wbem-Pfad**](a-wbempath.md)                                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Bekannte Objekte**](a-wellknownobjects.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Bei Änderung**](a-whenchanged.md)                                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Bei der Erstellung**](a-whencreated.md)                                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**WWW-Startseite**](a-wwwhomepage.md)                                           | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**WWW-Page-Other**](a-url.md)                                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |



## <a name="windows-server-2008-r2-extended-rights"></a>Windows Erweiterte Rechte für Server 2008 R2

Diese Klasse enthält die folgenden erweiterten Rechte für Windows Server 2008 R2:



| Allgemeiner Name                                                                    |
|--------------------------------------------------------------------------------|
| [**Do-Garbage Collection**](r-do-garbage-collection.md)                       |
| [**Neuberechnung der Hierarchie**](r-recalculate-hierarchy.md)                       |
| [**Allocate-Rids**](r-allocate-rids.md)                                       |
| [**Neuberechnung der Sicherheitsvererbung**](r-recalculate-security-inheritance.md) |
| [**DS-Check-Stale-Phantoms**](r-ds-check-stale-phantoms.md)                   |
| [**Refresh-Group-Cache**](r-refresh-group-cache.md)                           |
| [**Erneutes Laden von SSL-Zertifikaten**](r-reload-ssl-certificate.md)                     |



## <a name="windows-server-2012"></a>Windows Server 2012

-   [Attribute](#windows-server-2012-attributes)
-   [Erweiterte Rechte](#windows-server-2012-extended-rights)
-   [Überprüfte Schreibvorgänge](#windows-server-2012-validated-writes)



| Eingabe | Wert |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Richtig                                                                                         |
| Object-Category             | 1                                                                                            |
| Default-Object-Category     | \-                                                                                           |
| Governs-Id                  | 1.2.840.113556.1.5.7000.47                                                                   |
| Default-Hiding-Value        | 1                                                                                            |
| Rdn-Att-Id                  | [**Allgemeiner Name**](a-cn.md)<br/>                                                       |
| Unterklasse von                 | [**Anwendungs-Einstellungen**](c-applicationsettings.md)<br/>                             |
| Mögliche Übergeordnete          | [**Serverorganisation**](c-server.md)[](c-organization.md)                             |
| Zusätzlich           | \-                                                                                           |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                 |
| Standardsicherheitsdeskriptor | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;;; AU) |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2012-attributes"></a>Windows Server 2012 Attribute

Diese Klasse enthält die folgenden Attribute für Windows Server 2012:



| attribute                                                                                    | Obligatorisch. | Abgeleitet von                                                     |
|----------------------------------------------------------------------------------------------|-----------|------------------------------------------------------------------|
| [**Administratorbeschreibung**](a-admindescription.md)                                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Admin-Display-Name**](a-admindisplayname.md)                                             | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Allowed-Attributes**](a-allowedattributes.md)                                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Anwendungsname**](a-applicationname.md)                                                | Falsch     | [**Anwendungs-Einstellungen**](c-applicationsettings.md)<br/> |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                                | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Kanonischer Name**](a-canonicalname.md)                                                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Allgemeiner Name**](a-cn.md)                                                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Erstellen eines Zeitstempels**](a-createtimestamp.md)                                               | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Beschreibung**](a-description.md)                                                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Anzeigename**](a-displayname.md)                                                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Anzeigename– druckbar**](a-displaynameprintable.md)                                     | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**DMD-Location**](a-dmdlocation.md)                                                        | Falsch     | **NTDS-DSA**                                                     |
| [**DSA-Signature**](a-dsasignature.md)                                                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**DS-Core-Propagierungsdaten**](a-dscorepropagationdata.md)                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Erweiterungsname**](a-extensionname.md)                                                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Flaggen**](a-flags.md)                                                                     | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**From-Entry**](a-fromentry.md)                                                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)                                | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**FRS-Root-Path**](a-frsrootpath.md)                                                       | Falsch     | **NTDS-DSA**                                                     |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Has-Master-NCs**](a-hasmasterncs.md)                                                     | Falsch     | **NTDS-DSA**                                                     |
| [**Has-Partial-Replica-NCs**](a-haspartialreplicancs.md)                                    | Falsch     | **NTDS-DSA**                                                     |
| [**Instanztyp**](a-instancetype.md)                                                      | Richtig      | [**Nach oben**](c-top.md)<br/>                                  |
| [**Aufruf-ID**](a-invocationid.md)                                                      | Falsch     | **NTDS-DSA**                                                     |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                                | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Is-Deleted**](a-isdeleted.md)                                                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Is-Member-of-DL**](a-memberof.md)                                                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                                           | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Wird wiederverwendet**](a-isrecycled.md)                                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Zeitpunkt der letzten Sicherung und Wiederherstellung**](a-lastbackuprestorationtime.md)                          | Falsch     | **NTDS-DSA**                                                     |
| [**Last-Known-Parent**](a-lastknownparent.md)                                               | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Verwaltet von**](a-managedby.md)                                                            | Falsch     | **NTDS-DSA**                                                     |
| [**Verwaltete Objekte**](a-managedobjects.md)                                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Mastered-By**](a-masteredby.md)                                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Modify-Time-Stamp**](a-modifytimestamp.md)                                               | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md)                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md)               | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-Behavior-Version**](a-msds-behavior-version.md)                                    | Falsch     | **NTDS-DSA**                                                     |
| [**ms-DS-Claim-Shares-Possible-Values-with-BL**](a-msds-claimsharespossiblevalueswithbl.md) | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-Enabled-Feature**](a-msds-enabledfeature.md)                                       | Falsch     | **NTDS-DSA**                                                     |
| [**ms-DS-Enabled-Feature-BL**](a-msds-enabledfeaturebl.md)                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-Has-Domain-NCs**](a-msds-hasdomainncs.md)                                          | Falsch     | **NTDS-DSA**                                                     |
| [**ms-DS-Has-Full-Replica-NCs**](a-msds-hasfullreplicancs.md)                               | Falsch     | **NTDS-DSA**                                                     |
| [**ms-DS-Has-Instantiated-NCs**](a-msds-hasinstantiatedncs.md)                              | Falsch     | **NTDS-DSA**                                                     |
| [**ms-DS-Has-Master-NCs**](a-msds-hasmasterncs.md)                                          | Falsch     | **NTDS-DSA**                                                     |
| [**ms-DS-Host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-Is-Domain-For**](a-msds-isdomainfor.md)                                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-is-full-replica-for**](a-msds-isfullreplicafor.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-isGC**](a-msds-isgc.md)                                                            | Falsch     | **NTDS-DSA**                                                     |
| [**ms-DS-is-partial-replica-for**](a-msds-ispartialreplicafor.md)                           | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-Is-Primary-Computer-For**](a-msds-isprimarycomputerfor.md)                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-isRODC**](a-msds-isrodc.md)                                                        | Falsch     | **NTDS-DSA**                                                     |
| [**ms-DS-Is-User-Cachable-At-Rodc**](a-msds-isusercachableatrodc.md)                        | Falsch     | **NTDS-DSA**                                                     |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-local-Effective-Deletion-Time**](a-msds-localeffectivedeletiontime.md)             | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-local-Effective-Recycle-Time**](a-msds-localeffectiverecycletime.md)               | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                                               | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-Members-for-Az-Role-BL**](a-msds-membersforazrolebl.md)                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-Members-of-Resource-Property-List-BL**](a-msds-membersofresourcepropertylistbl.md) | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)                     | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)                | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-NC-Type**](a-msds-nctype.md)                                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-Never-Reveal-Group**](a-msds-neverrevealgroup.md)                                  | Falsch     | **NTDS-DSA**                                                     |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                                | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-OIDToGroup-Link-BL**](a-msds-oidtogrouplinkbl.md)                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-Operations-for-Az-Role-BL**](a-msds-operationsforazrolebl.md)                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-Operations-for-Az-Task-BL**](a-msds-operationsforaztaskbl.md)                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-PSO-Applied**](a-msds-psoapplied.md)                                               | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-ReplicationEpoch**](a-msds-replicationepoch.md)                                    | Falsch     | **NTDS-DSA**                                                     |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                               | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-Retired-Repl-NC-Signatures**](a-msds-retiredreplncsignatures.md)                   | Falsch     | **NTDS-DSA**                                                     |
| [**ms-DS-Revealed-DSAs**](a-msds-revealeddsas.md)                                           | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-Revealed-List-BL**](a-msds-revealedlistbl.md)                                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-Revealed-Users**](a-msds-revealedusers.md)                                         | Falsch     | **NTDS-DSA**                                                     |
| [**ms-DS-Reveal-OnDemand-Group**](a-msds-revealondemandgroup.md)                            | Falsch     | **NTDS-DSA**                                                     |
| [**ms-DS-Einstellungen**](a-msds-settings.md)                                                    | Falsch     | [**Anwendungs-Einstellungen**](c-applicationsettings.md)<br/> |
| [**ms-DS-SiteName**](a-msds-sitename.md)                                                    | Falsch     | **NTDS-DSA**                                                     |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)                                | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)                                | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-TDO-Egress-BL**](a-msds-tdoegressbl.md)                                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-TDO-Ingress-BL**](a-msds-tdoingressbl.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-DS-Value-Type-Reference-BL**](a-msds-valuetypereferencebl.md)                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                                     | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Netzwerkadresse**](a-networkaddress.md)                                                  | Falsch     | **NTDS-DSA**                                                     |
| [**Non-Security-Member-BL**](a-nonsecuritymemberbl.md)                                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Benachrichtigungsliste**](a-notificationlist.md)                                              | Falsch     | [**Anwendungs-Einstellungen**](c-applicationsettings.md)<br/> |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                                     | Richtig      | [**Nach oben**](c-top.md)<br/>                                  |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Objektkategorie**](a-objectcategory.md)                                                  | Richtig      | [**Nach oben**](c-top.md)<br/>                                  |
| [**Object-Class**](a-objectclass.md)                                                        | Richtig      | [**Nach oben**](c-top.md)<br/>                                  |
| [**Objekt-GUID**](a-objectguid.md)                                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Object-Version**](a-objectversion.md)                                                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Optionen**](a-options.md)                                                                 | Falsch     | **NTDS-DSA**                                                     |
| [**Andere bekannte Objekte**](a-otherwellknownobjects.md)                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Mögliche 100000000000**](a-possibleinferiors.md)                                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                                           | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Proxyadressen**](a-proxyaddresses.md)                                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Query-Policy-BL**](a-querypolicybl.md)                                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Query-Policy-Object**](a-querypolicyobject.md)                                           | Falsch     | **NTDS-DSA**                                                     |
| [**Rdn**](a-name.md)                                                                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Berichte**](a-directreports.md)                                                           | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Reps-From**](a-repsfrom.md)                                                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Reps-To**](a-repsto.md)                                                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Retired-Repl-DSA-Signatures**](a-retiredrepldsasignatures.md)                            | Falsch     | **NTDS-DSA**                                                     |
| [**Revision**](a-revision.md)                                                               | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                                           | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Serverreferenz**](a-serverreference.md)                                                | Falsch     | **NTDS-DSA**                                                     |
| [**Server-Reference-BL**](a-serverreferencebl.md)                                           | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)                               | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Site-Object-BL**](a-siteobjectbl.md)                                                     | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Sub-Refs**](a-subrefs.md)                                                                | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                             | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Systemflags**](a-systemflags.md)                                                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**USN-Changed**](a-usnchanged.md)                                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**VON USN erstellt**](a-usncreated.md)                                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**USN-Intersite**](a-usnintersite.md)                                                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**USN-Quelle**](a-usnsource.md)                                                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Wbem-Path**](a-wbempath.md)                                                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Bekannte Objekte**](a-wellknownobjects.md)                                             | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Wenn geändert**](a-whenchanged.md)                                                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**Wenn erstellt**](a-whencreated.md)                                                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**WWW-Homepage**](a-wwwhomepage.md)                                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |
| [**WWW-Page-Other**](a-url.md)                                                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                  |



## <a name="windows-server-2012-extended-rights"></a>Windows Server 2012 Erweiterte Rechte

Diese Klasse enthält die folgenden erweiterten Rechte für Windows Server 2012:



| Allgemeiner Name                                                                    |
|--------------------------------------------------------------------------------|
| [**Do-Garbage Collection**](r-do-garbage-collection.md)                       |
| [**Neuberechnungshierarchie**](r-recalculate-hierarchy.md)                       |
| [**Allocate-Rids**](r-allocate-rids.md)                                       |
| [**Neuberechnung der Sicherheitsvererbung**](r-recalculate-security-inheritance.md) |
| [**DS-Check-Stale-Phantoms**](r-ds-check-stale-phantoms.md)                   |
| [**Refresh-Group-Cache**](r-refresh-group-cache.md)                           |
| [**Reload-SSL-Certificate**](r-reload-ssl-certificate.md)                     |



## <a name="windows-server-2012-validated-writes"></a>Windows Server 2012 Überprüfte Schreibvorgänge

Diese Klasse enthält die folgenden überprüften Schreibvorgänge für Windows Server 2012:



| Allgemeiner Name                                                                    |
|--------------------------------------------------------------------------------|
| [**Validated-MS-DS-Behavior-Version**](r-validated-ms-ds-behavior-version.md) |



 

 





