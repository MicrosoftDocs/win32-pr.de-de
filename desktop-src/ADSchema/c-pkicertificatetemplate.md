---
title: PKI-Certificate-Template-Klasse
description: Enthält Informationen zu Zertifikaten, die vom Zertifikatserver ausgestellt werden.
ms.assetid: 9b6ca989-058c-461b-ba3d-5b29ea15cbbc
ms.tgt_platform: multiple
keywords:
- PKI-Certificate-Template-Klasse AD Schema
- pKICertificateTemplate-Klasse AD-Schema
topic_type:
- apiref
api_name:
- PKI-Certificate-Template
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e45c19969a09770e8b37b5bf9a45c4ff4d87806fc8e77b02e1a7e109981110c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119753090"
---
# <a name="pki-certificate-template-class"></a>PKI-Certificate-Template-Klasse

Enthält Informationen zu Zertifikaten, die vom Zertifikatserver ausgestellt werden.



| Eingabe | Wert |
|-------------------|--------------------------------------|
| CN                | PKI-Certificate-Template             |
| Ldap-Anzeigename | pKICertificateTemplate               |
| Aktualisieren von Berechtigungen  | \-                                   |
| Updatehäufigkeit  | \-                                   |
| Schema-ID-GUID    | e5209ca2-3bba-11d2-90cc-00c04fd91ab1 |



## <a name="implementations"></a>Implementierungen

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server

-   [Attribute](#windows-2000-server-attributes)
-   [Erweiterte Rechte](#windows-2000-server-extended-rights)



| Eingabe | Wert |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Falsch                                                                                        |
| Object-Category             | 1                                                                                            |
| Default-Object-Category     | \-                                                                                           |
| Governs-Id                  | 1.2.840.113556.1.5.177                                                                       |
| Default-Hiding-Value        | 1                                                                                            |
| Rdn-Att-Id                  | [**Common-Name**](a-cn.md)<br/>                                                       |
| Unterklasse von                 | [**Nach oben**](c-top.md)<br/>                                                              |
| Mögliche Vorgesetzte          | [**Container**](c-container.md)                                                             |
| Zusätzlich           | \-                                                                                           |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                 |
| Standardsicherheitsdeskriptor | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;;; AU) |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-2000-server-attributes"></a>Windows 2000-Serverattribute

Diese Klasse enthält die folgenden Attribute für Windows 2000-Server:



| attribute                                                                 | Obligatorisch. | Abgeleitet von                                                 |
|---------------------------------------------------------------------------|-----------|--------------------------------------------------------------|
| [**Admin-Description**](a-admindescription.md)                           | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Administratoranzeigename**](a-admindisplayname.md)                          | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Allowed-Attributes**](a-allowedattributes.md)                         | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)      | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                    | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md) | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)             | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Kanonischer Name**](a-canonicalname.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Common-Name**](a-cn.md)                                               | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Create-Time-Stamp**](a-createtimestamp.md)                            | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Beschreibung**](a-description.md)                                      | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Anzeigename**](a-displayname.md)                                     | Falsch     | **PKI-Certificate-Template** [ **Top**](c-top.md)<br/> |
| [**Display-Name-Printable**](a-displaynameprintable.md)                  | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**DSA-Signature**](a-dsasignature.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**DS-Core-Propagierungsdaten**](a-dscorepropagationdata.md)               | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Extension-Name**](a-extensionname.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Flaggen**](a-flags.md)                                                  | Falsch     | **PKI-Certificate-Template** [ **Top**](c-top.md)<br/> |
| [**From-Entry**](a-fromentry.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)             | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                 | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Instanztyp**](a-instancetype.md)                                   | Richtig      | [**Nach oben**](c-top.md)<br/>                              |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)             | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Is-Deleted**](a-isdeleted.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Is-Member-of-DL**](a-memberof.md)                                     | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                        | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Letztes bekanntes übergeordnetes Element**](a-lastknownparent.md)                            | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Verwaltete Objekte**](a-managedobjects.md)                               | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Mastered By**](a-masteredby.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Modify-Time-Stamp**](a-modifytimestamp.md)                            | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)    | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                 | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Non-Security-Member-BL**](a-nonsecuritymemberbl.md)                   | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                  | Richtig      | [**Nach oben**](c-top.md)<br/>                              |
| [**Obj-Dist-Name**](a-distinguishedname.md)                              | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Objektkategorie**](a-objectcategory.md)                               | Richtig      | [**Nach oben**](c-top.md)<br/>                              |
| [**Object-Class**](a-objectclass.md)                                     | Richtig      | [**Nach oben**](c-top.md)<br/>                              |
| [**Objekt-GUID**](a-objectguid.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Object-Version**](a-objectversion.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Andere bekannte Objekte**](a-otherwellknownobjects.md)               | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md) | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                    | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**PKI-Critical-Extensions**](a-pkicriticalextensions.md)                | Falsch     | **PKI-Certificate-Template**                                 |
| [**PKI-Default-CSPs**](a-pkidefaultcsps.md)                              | Falsch     | **PKI-Certificate-Template**                                 |
| [**PKI-Default-Key-Spec**](a-pkidefaultkeyspec.md)                       | Falsch     | **PKI-Certificate-Template**                                 |
| [**PKI-Enrollment-Access**](a-pkienrollmentaccess.md)                    | Falsch     | **PKI-Certificate-Template**                                 |
| [**PKI-Ablaufzeitraum**](a-pkiexpirationperiod.md)                    | Falsch     | **PKI-Certificate-Template**                                 |
| [**PKI-Extended-Key-Usage**](a-pkiextendedkeyusage.md)                   | Falsch     | **PKI-Certificate-Template**                                 |
| [**PKI-Schlüsselverwendung**](a-pkikeyusage.md)                                    | Falsch     | **PKI-Certificate-Template**                                 |
| [**PKI-Max-Issuing-Depth**](a-pkimaxissuingdepth.md)                     | Falsch     | **PKI-Certificate-Template**                                 |
| [**PKI-Überlappungszeitraum**](a-pkioverlapperiod.md)                          | Falsch     | **PKI-Certificate-Template**                                 |
| [**Mögliche 100000000000**](a-possibleinferiors.md)                         | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                        | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Proxyadressen**](a-proxyaddresses.md)                               | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Query-Policy-BL**](a-querypolicybl.md)                                | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Rdn**](a-name.md)                                                     | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                 | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                      | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Berichte**](a-directreports.md)                                        | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Reps-From**](a-repsfrom.md)                                           | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Reps-To**](a-repsto.md)                                               | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Revision**](a-revision.md)                                            | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                        | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Server-Reference-BL**](a-serverreferencebl.md)                        | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)            | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Site-Object-BL**](a-siteobjectbl.md)                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Sub-Refs**](a-subrefs.md)                                             | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                          | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Systemflags**](a-systemflags.md)                                     | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**USN-Changed**](a-usnchanged.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**VON USN erstellt**](a-usncreated.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**USN-Intersite**](a-usnintersite.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                               | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**USN-Quelle**](a-usnsource.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Wbem-Path**](a-wbempath.md)                                           | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Bekannte Objekte**](a-wellknownobjects.md)                          | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Wenn geändert**](a-whenchanged.md)                                     | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Wenn erstellt**](a-whencreated.md)                                     | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**WWW-Homepage**](a-wwwhomepage.md)                                    | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**WWW-Page-Other**](a-url.md)                                           | Falsch     | [**Nach oben**](c-top.md)<br/>                              |



## <a name="windows-2000-server-extended-rights"></a>erweiterte Rechte für Windows 2000-Server

Diese Klasse enthält die folgenden erweiterten Rechte für Windows 2000 Server:



| Allgemeiner Name                                                |
|------------------------------------------------------------|
| [**Zertifikatregistrierung**](r-certificate-enrollment.md) |



## <a name="windows-server-2003"></a>Windows Server 2003

-   [Attribute](#windows-server-2003-attributes)
-   [Erweiterte Rechte](#windows-server-2003-extended-rights)



| Eingabe | Wert |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Falsch                                                                                        |
| Object-Category             | 1                                                                                            |
| Default-Object-Category     | \-                                                                                           |
| Governs-Id                  | 1.2.840.113556.1.5.177                                                                       |
| Default-Hiding-Value        | 1                                                                                            |
| Rdn-Att-Id                  | [**Allgemeiner Name**](a-cn.md)<br/>                                                       |
| Unterklasse von                 | [**Nach oben**](c-top.md)<br/>                                                              |
| Mögliche Übergeordnete          | [**Container**](c-container.md)                                                             |
| Zusätzlich           | \-                                                                                           |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                 |
| Standardsicherheitsdeskriptor | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;;; AU) |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2003-attributes"></a>Windows Server 2003-Attribute

Diese Klasse enthält die folgenden Attribute für Windows Server 2003:



| attribute                                                                               | Obligatorisch. | Abgeleitet von                                                 |
|-----------------------------------------------------------------------------------------|-----------|--------------------------------------------------------------|
| [**Administratorbeschreibung**](a-admindescription.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Admin-Display-Name**](a-admindisplayname.md)                                        | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Allowed-Attributes**](a-allowedattributes.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)                    | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)               | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                           | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Kanonischer Name**](a-canonicalname.md)                                               | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Allgemeiner Name**](a-cn.md)                                                             | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Erstellen eines Zeitstempels**](a-createtimestamp.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Beschreibung**](a-description.md)                                                    | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Anzeigename**](a-displayname.md)                                                   | Falsch     | **PKI-Certificate-Template** [ **Top**](c-top.md)<br/> |
| [**Anzeigename– druckbar**](a-displaynameprintable.md)                                | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**DSA-Signature**](a-dsasignature.md)                                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**DS-Core-Propagierungsdaten**](a-dscorepropagationdata.md)                             | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Erweiterungsname**](a-extensionname.md)                                               | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Flaggen**](a-flags.md)                                                                | Falsch     | **PKI-Certificate-Template** [ **Top**](c-top.md)<br/> |
| [**From-Entry**](a-fromentry.md)                                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)                           | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                               | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                              | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Instanztyp**](a-instancetype.md)                                                 | Richtig      | [**Nach oben**](c-top.md)<br/>                              |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                           | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Is-Deleted**](a-isdeleted.md)                                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Is-Member-of-DL**](a-memberof.md)                                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                                      | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Last-Known-Parent**](a-lastknownparent.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Verwaltete Objekte**](a-managedobjects.md)                                             | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Mastered-By**](a-masteredby.md)                                                     | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Modify-Time-Stamp**](a-modifytimestamp.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                             | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                             | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md)             | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)                  | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                               | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Members-for-Az-Role-BL**](a-msds-membersforazrolebl.md)                       | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)                | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)              | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                                     | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                           | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Operations-for-Az-Role-BL**](a-msds-operationsforazrolebl.md)                 | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Operations-for-Az-Task-BL**](a-msds-operationsforaztaskbl.md)                 | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)                  | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                          | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Tasks-for-Az-Role-BL**](a-msds-tasksforazrolebl.md)                           | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Tasks-for-Az-Task-BL**](a-msds-tasksforaztaskbl.md)                           | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-PKI-Certificate-Application-Policy**](a-mspki-certificate-application-policy.md) | Falsch     | **PKI-Certificate-Template**                                 |
| [**ms-PKI-Certificate-Name-Flag**](a-mspki-certificate-name-flag.md)                   | Falsch     | **PKI-Certificate-Template**                                 |
| [**ms-PKI-Certificate-Policy**](a-mspki-certificate-policy.md)                         | Falsch     | **PKI-Certificate-Template**                                 |
| [**ms-PKI-Cert-Template-OID**](a-mspki-cert-template-oid.md)                           | Falsch     | **PKI-Certificate-Template**                                 |
| [**ms-PKI-Enrollment-Flag**](a-mspki-enrollment-flag.md)                               | Falsch     | **PKI-Certificate-Template**                                 |
| [**ms-PKI-Minimal-Key-Size**](a-mspki-minimal-key-size.md)                             | Falsch     | **PKI-Certificate-Template**                                 |
| [**ms-PKI-Private-Key-Flag**](a-mspki-private-key-flag.md)                             | Falsch     | **PKI-Certificate-Template**                                 |
| [**ms-PKI-RA-Application-Policies**](a-mspki-ra-application-policies.md)               | Falsch     | **PKI-Certificate-Template**                                 |
| [**ms-PKI-RA-Policies**](a-mspki-ra-policies.md)                                       | Falsch     | **PKI-Certificate-Template**                                 |
| [**ms-PKI-RA-Signature**](a-mspki-ra-signature.md)                                     | Falsch     | **PKI-Certificate-Template**                                 |
| [**ms-PKI-Supersede-Templates**](a-mspki-supersede-templates.md)                       | Falsch     | **PKI-Certificate-Template**                                 |
| [**ms-PKI-Template-Minor-Revision**](a-mspki-template-minor-revision.md)               | Falsch     | **PKI-Certificate-Template**                                 |
| [**ms-PKI-Template-Schema-Version**](a-mspki-template-schema-version.md)               | Falsch     | **PKI-Certificate-Template**                                 |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                                | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Non-Security-Member-BL**](a-nonsecuritymemberbl.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                                | Richtig      | [**Nach oben**](c-top.md)<br/>                              |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                            | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Objektkategorie**](a-objectcategory.md)                                             | Richtig      | [**Nach oben**](c-top.md)<br/>                              |
| [**Objektklasse**](a-objectclass.md)                                                   | Richtig      | [**Nach oben**](c-top.md)<br/>                              |
| [**Objekt-GUID**](a-objectguid.md)                                                     | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Objektversion**](a-objectversion.md)                                               | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Andere bekannte Objekte**](a-otherwellknownobjects.md)                             | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Teilattributlöschungsliste**](a-partialattributedeletionlist.md)               | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Teilattributsatz**](a-partialattributeset.md)                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**PKI-Critical-Extensions**](a-pkicriticalextensions.md)                              | Falsch     | **PKI-Certificate-Template**                                 |
| [**PKI-Default-CSPs**](a-pkidefaultcsps.md)                                            | Falsch     | **PKI-Certificate-Template**                                 |
| [**PKI-Default-Key-Spec**](a-pkidefaultkeyspec.md)                                     | Falsch     | **PKI-Certificate-Template**                                 |
| [**PKI-Enrollment-Access**](a-pkienrollmentaccess.md)                                  | Falsch     | **PKI-Certificate-Template**                                 |
| [**PKI-Ablaufzeitraum**](a-pkiexpirationperiod.md)                                  | Falsch     | **PKI-Certificate-Template**                                 |
| [**PKI-Extended-Key-Usage**](a-pkiextendedkeyusage.md)                                 | Falsch     | **PKI-Certificate-Template**                                 |
| [**PKI-Schlüsselverwendung**](a-pkikeyusage.md)                                                  | Falsch     | **PKI-Certificate-Template**                                 |
| [**PKI-Max-Issuing-Depth**](a-pkimaxissuingdepth.md)                                   | Falsch     | **PKI-Certificate-Template**                                 |
| [**PKI-Überlappungszeitraum**](a-pkioverlapperiod.md)                                        | Falsch     | **PKI-Certificate-Template**                                 |
| [**Mögliche Hindernisse**](a-possibleinferiors.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                                      | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Proxyadressen**](a-proxyaddresses.md)                                             | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Query-Policy-BL**](a-querypolicybl.md)                                              | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Rdn**](a-name.md)                                                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                               | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                                    | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Berichte**](a-directreports.md)                                                      | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Reps-From**](a-repsfrom.md)                                                         | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Reps-To**](a-repsto.md)                                                             | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Revision**](a-revision.md)                                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                                      | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Server-Reference-BL**](a-serverreferencebl.md)                                      | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Nur in erweiterter Ansicht anzeigen**](a-showinadvancedviewonly.md)                          | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Site-Object-BL**](a-siteobjectbl.md)                                                | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                              | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Sub-Refs**](a-subrefs.md)                                                           | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                        | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Systemflags**](a-systemflags.md)                                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**USN geändert**](a-usnchanged.md)                                                     | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**USN-erstellt**](a-usncreated.md)                                                     | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**USN-DSA-last-obj-removed**](a-usndsalastobjremoved.md)                              | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**USN-Intersite**](a-usnintersite.md)                                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                             | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**USN-Quelle**](a-usnsource.md)                                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Wbem-Pfad**](a-wbempath.md)                                                         | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Bekannte Objekte**](a-wellknownobjects.md)                                        | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Bei Änderung**](a-whenchanged.md)                                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Bei der Erstellung**](a-whencreated.md)                                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**WWW-Startseite**](a-wwwhomepage.md)                                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**WWW-Page-Other**](a-url.md)                                                         | Falsch     | [**Nach oben**](c-top.md)<br/>                              |



## <a name="windows-server-2003-extended-rights"></a>Windows Erweiterte Rechte für Server 2003

Diese Klasse enthält die folgenden erweiterten Rechte für Windows Server 2003:



| Allgemeiner Name                                                |
|------------------------------------------------------------|
| [**Zertifikatregistrierung**](r-certificate-enrollment.md) |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2

-   [Attribute](#windows-server-2003-r2-attributes)
-   [Erweiterte Rechte](#windows-server-2003-r2-extended-rights)



| Eingabe | Wert |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Falsch                                                                                        |
| Object-Category             | 1                                                                                            |
| Default-Object-Category     | \-                                                                                           |
| Governs-Id                  | 1.2.840.113556.1.5.177                                                                       |
| Default-Hiding-Value        | 1                                                                                            |
| Rdn-Att-Id                  | [**Allgemeiner Name**](a-cn.md)<br/>                                                       |
| Unterklasse von                 | [**Nach oben**](c-top.md)<br/>                                                              |
| Mögliche Übergeordnete          | [**Container**](c-container.md)                                                             |
| Zusätzlich           | \-                                                                                           |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                 |
| Standardsicherheitsdeskriptor | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;;; AU) |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2003-r2-attributes"></a>Windows Server 2003 R2-Attribute

Diese Klasse enthält die folgenden Attribute für Windows Server 2003 R2:



| attribute                                                                               | Obligatorisch. | Abgeleitet von                                                 |
|-----------------------------------------------------------------------------------------|-----------|--------------------------------------------------------------|
| [**Administratorbeschreibung**](a-admindescription.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Admin-Display-Name**](a-admindisplayname.md)                                        | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Allowed-Attributes**](a-allowedattributes.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)                    | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)               | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                           | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Kanonischer Name**](a-canonicalname.md)                                               | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Allgemeiner Name**](a-cn.md)                                                             | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Erstellen eines Zeitstempels**](a-createtimestamp.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Beschreibung**](a-description.md)                                                    | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Anzeigename**](a-displayname.md)                                                   | Falsch     | **PKI-Certificate-Template** [ **Top**](c-top.md)<br/> |
| [**Anzeigename– druckbar**](a-displaynameprintable.md)                                | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**DSA-Signature**](a-dsasignature.md)                                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**DS-Core-Propagierungsdaten**](a-dscorepropagationdata.md)                             | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Erweiterungsname**](a-extensionname.md)                                               | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Flaggen**](a-flags.md)                                                                | Falsch     | **PKI-Certificate-Template** [ **Top**](c-top.md)<br/> |
| [**From-Entry**](a-fromentry.md)                                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)                           | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                               | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                              | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Instanztyp**](a-instancetype.md)                                                 | Richtig      | [**Nach oben**](c-top.md)<br/>                              |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                           | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Is-Deleted**](a-isdeleted.md)                                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Is-Member-of-DL**](a-memberof.md)                                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                                      | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Last-Known-Parent**](a-lastknownparent.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Verwaltete Objekte**](a-managedobjects.md)                                             | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Mastered-By**](a-masteredby.md)                                                     | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Modify-Time-Stamp**](a-modifytimestamp.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                             | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                             | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)                     | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                         | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md)             | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)                  | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                               | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Members-for-Az-Role-BL**](a-msds-membersforazrolebl.md)                       | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)                | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)              | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                                     | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                           | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Operations-for-Az-Role-BL**](a-msds-operationsforazrolebl.md)                 | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Operations-for-Az-Task-BL**](a-msds-operationsforaztaskbl.md)                 | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)                  | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                          | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Tasks-for-Az-Role-BL**](a-msds-tasksforazrolebl.md)                           | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Tasks-for-Az-Task-BL**](a-msds-tasksforaztaskbl.md)                           | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-PKI-Certificate-Application-Policy**](a-mspki-certificate-application-policy.md) | Falsch     | **PKI-Certificate-Template**                                 |
| [**ms-PKI-Certificate-Name-Flag**](a-mspki-certificate-name-flag.md)                   | Falsch     | **PKI-Certificate-Template**                                 |
| [**ms-PKI-Certificate-Policy**](a-mspki-certificate-policy.md)                         | Falsch     | **PKI-Certificate-Template**                                 |
| [**ms-PKI-Cert-Template-OID**](a-mspki-cert-template-oid.md)                           | Falsch     | **PKI-Certificate-Template**                                 |
| [**ms-PKI-Enrollment-Flag**](a-mspki-enrollment-flag.md)                               | Falsch     | **PKI-Certificate-Template**                                 |
| [**ms-PKI-Minimal-Key-Size**](a-mspki-minimal-key-size.md)                             | Falsch     | **PKI-Certificate-Template**                                 |
| [**ms-PKI-Private-Key-Flag**](a-mspki-private-key-flag.md)                             | Falsch     | **PKI-Certificate-Template**                                 |
| [**ms-PKI-RA-Application-Policies**](a-mspki-ra-application-policies.md)               | Falsch     | **PKI-Certificate-Template**                                 |
| [**ms-PKI-RA-Policies**](a-mspki-ra-policies.md)                                       | Falsch     | **PKI-Certificate-Template**                                 |
| [**ms-PKI-RA-Signature**](a-mspki-ra-signature.md)                                     | Falsch     | **PKI-Certificate-Template**                                 |
| [**ms-PKI-Supersede-Templates**](a-mspki-supersede-templates.md)                       | Falsch     | **PKI-Certificate-Template**                                 |
| [**ms-PKI-Template-Minor-Revision**](a-mspki-template-minor-revision.md)               | Falsch     | **PKI-Certificate-Template**                                 |
| [**ms-PKI-Template-Schema-Version**](a-mspki-template-schema-version.md)               | Falsch     | **PKI-Certificate-Template**                                 |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                              | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                                | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Non-Security-Member-BL**](a-nonsecuritymemberbl.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                                | Richtig      | [**Nach oben**](c-top.md)<br/>                              |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                            | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Objektkategorie**](a-objectcategory.md)                                             | Richtig      | [**Nach oben**](c-top.md)<br/>                              |
| [**Objektklasse**](a-objectclass.md)                                                   | Richtig      | [**Nach oben**](c-top.md)<br/>                              |
| [**Objekt-GUID**](a-objectguid.md)                                                     | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Objektversion**](a-objectversion.md)                                               | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Andere bekannte Objekte**](a-otherwellknownobjects.md)                             | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Teilattributlöschungsliste**](a-partialattributedeletionlist.md)               | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Teilattributsatz**](a-partialattributeset.md)                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**PKI-Critical-Extensions**](a-pkicriticalextensions.md)                              | Falsch     | **PKI-Certificate-Template**                                 |
| [**PKI-Default-CSPs**](a-pkidefaultcsps.md)                                            | Falsch     | **PKI-Certificate-Template**                                 |
| [**PKI-Default-Key-Spec**](a-pkidefaultkeyspec.md)                                     | Falsch     | **PKI-Certificate-Template**                                 |
| [**PKI-Enrollment-Access**](a-pkienrollmentaccess.md)                                  | Falsch     | **PKI-Certificate-Template**                                 |
| [**PKI-Ablaufzeitraum**](a-pkiexpirationperiod.md)                                  | Falsch     | **PKI-Certificate-Template**                                 |
| [**PKI-Extended-Key-Usage**](a-pkiextendedkeyusage.md)                                 | Falsch     | **PKI-Certificate-Template**                                 |
| [**PKI-Schlüsselverwendung**](a-pkikeyusage.md)                                                  | Falsch     | **PKI-Certificate-Template**                                 |
| [**PKI-Max-Issuing-Depth**](a-pkimaxissuingdepth.md)                                   | Falsch     | **PKI-Certificate-Template**                                 |
| [**PKI-Überlappungszeitraum**](a-pkioverlapperiod.md)                                        | Falsch     | **PKI-Certificate-Template**                                 |
| [**Mögliche Hindernisse**](a-possibleinferiors.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                                      | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Proxyadressen**](a-proxyaddresses.md)                                             | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Query-Policy-BL**](a-querypolicybl.md)                                              | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Rdn**](a-name.md)                                                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                               | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                                    | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Berichte**](a-directreports.md)                                                      | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Reps-From**](a-repsfrom.md)                                                         | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Reps-To**](a-repsto.md)                                                             | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Revision**](a-revision.md)                                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                                      | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Server-Reference-BL**](a-serverreferencebl.md)                                      | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)                          | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Site-Object-BL**](a-siteobjectbl.md)                                                | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                              | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Sub-Refs**](a-subrefs.md)                                                           | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                        | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Systemflags**](a-systemflags.md)                                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**USN-Changed**](a-usnchanged.md)                                                     | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**VON USN erstellt**](a-usncreated.md)                                                     | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                              | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**USN-Intersite**](a-usnintersite.md)                                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                             | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**USN-Quelle**](a-usnsource.md)                                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Wbem-Path**](a-wbempath.md)                                                         | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Bekannte Objekte**](a-wellknownobjects.md)                                        | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Wenn geändert**](a-whenchanged.md)                                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Wenn erstellt**](a-whencreated.md)                                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**WWW-Homepage**](a-wwwhomepage.md)                                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**WWW-Page-Other**](a-url.md)                                                         | Falsch     | [**Nach oben**](c-top.md)<br/>                              |



## <a name="windows-server-2003-r2-extended-rights"></a>Windows Erweiterte Server 2003 R2-Rechte

Diese Klasse enthält die folgenden erweiterten Rechte für Windows Server 2003 R2:



| Allgemeiner Name                                                |
|------------------------------------------------------------|
| [**Zertifikatregistrierung**](r-certificate-enrollment.md) |



## <a name="windows-server-2008"></a>Windows Server 2008

-   [Attribute](#windows-server-2008-attributes)
-   [Erweiterte Rechte](#windows-server-2008-extended-rights)



| Eingabe | Wert |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Falsch                                                                                        |
| Object-Category             | 1                                                                                            |
| Default-Object-Category     | \-                                                                                           |
| Governs-Id                  | 1.2.840.113556.1.5.177                                                                       |
| Default-Hiding-Value        | 1                                                                                            |
| Rdn-Att-Id                  | [**Common-Name**](a-cn.md)<br/>                                                       |
| Unterklasse von                 | [**Nach oben**](c-top.md)<br/>                                                              |
| Mögliche Vorgesetzte          | [**Container**](c-container.md)                                                             |
| Zusätzlich           | \-                                                                                           |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                 |
| Standardsicherheitsdeskriptor | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;;; AU) |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2008-attributes"></a>Windows Server 2008-Attribute

Diese Klasse enthält die folgenden Attribute für Windows Server 2008:



| attribute                                                                               | Obligatorisch. | Abgeleitet von                                                 |
|-----------------------------------------------------------------------------------------|-----------|--------------------------------------------------------------|
| [**Admin-Description**](a-admindescription.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Administratoranzeigename**](a-admindisplayname.md)                                        | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Allowed-Attributes**](a-allowedattributes.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)                    | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)               | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                           | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Kanonischer Name**](a-canonicalname.md)                                               | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Common-Name**](a-cn.md)                                                             | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Create-Time-Stamp**](a-createtimestamp.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Beschreibung**](a-description.md)                                                    | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Anzeigename**](a-displayname.md)                                                   | Falsch     | **PKI-Certificate-Template** [ **Top**](c-top.md)<br/> |
| [**Display-Name-Printable**](a-displaynameprintable.md)                                | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**DSA-Signature**](a-dsasignature.md)                                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**DS-Core-Propagierungsdaten**](a-dscorepropagationdata.md)                             | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Extension-Name**](a-extensionname.md)                                               | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Flaggen**](a-flags.md)                                                                | Falsch     | **PKI-Certificate-Template** [ **Top**](c-top.md)<br/> |
| [**From-Entry**](a-fromentry.md)                                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)                           | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                               | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                              | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Instanztyp**](a-instancetype.md)                                                 | Richtig      | [**Nach oben**](c-top.md)<br/>                              |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                           | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Is-Deleted**](a-isdeleted.md)                                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Is-Member-of-DL**](a-memberof.md)                                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                                      | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Letztes bekanntes übergeordnetes Element**](a-lastknownparent.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Verwaltete Objekte**](a-managedobjects.md)                                             | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Mastered By**](a-masteredby.md)                                                     | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Modify-Time-Stamp**](a-modifytimestamp.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                             | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                             | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)                     | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                         | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md)             | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md)          | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)                  | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                               | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Is-Domain-For**](a-msds-isdomainfor.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-is-full-replica-for**](a-msds-isfullreplicafor.md)                            | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-is-partial-replica-for**](a-msds-ispartialreplicafor.md)                      | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                                     | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Members-for-Az-Role-BL**](a-msds-membersforazrolebl.md)                       | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)                | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)              | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)           | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-NC-Type**](a-msds-nctype.md)                                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                                     | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                           | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Operations-for-Az-Role-BL**](a-msds-operationsforazrolebl.md)                 | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Operations-for-Az-Task-BL**](a-msds-operationsforaztaskbl.md)                 | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                                    | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-PSO-Applied**](a-msds-psoapplied.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)                  | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                          | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Revealed-DSAs**](a-msds-revealeddsas.md)                                      | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Revealed-List-BL**](a-msds-revealedlistbl.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Tasks-for-Az-Role-BL**](a-msds-tasksforazrolebl.md)                           | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Tasks-for-Az-Task-BL**](a-msds-tasksforaztaskbl.md)                           | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-PKI-Certificate-Application-Policy**](a-mspki-certificate-application-policy.md) | Falsch     | **PKI-Certificate-Template**                                 |
| [**ms-PKI-Certificate-Name-Flag**](a-mspki-certificate-name-flag.md)                   | Falsch     | **PKI-Certificate-Template**                                 |
| [**ms-PKI-Certificate-Policy**](a-mspki-certificate-policy.md)                         | Falsch     | **PKI-Certificate-Template**                                 |
| [**ms-PKI-Cert-Template-OID**](a-mspki-cert-template-oid.md)                           | Falsch     | **PKI-Certificate-Template**                                 |
| [**ms-PKI-Enrollment-Flag**](a-mspki-enrollment-flag.md)                               | Falsch     | **PKI-Certificate-Template**                                 |
| [**ms-PKI-Minimal-Key-Size**](a-mspki-minimal-key-size.md)                             | Falsch     | **PKI-Certificate-Template**                                 |
| [**ms-PKI-Private-Key-Flag**](a-mspki-private-key-flag.md)                             | Falsch     | **PKI-Certificate-Template**                                 |
| [**ms-PKI-RA-Application-Policies**](a-mspki-ra-application-policies.md)               | Falsch     | **PKI-Certificate-Template**                                 |
| [**ms-PKI-RA-Policies**](a-mspki-ra-policies.md)                                       | Falsch     | **PKI-Certificate-Template**                                 |
| [**ms-PKI-RA-Signature**](a-mspki-ra-signature.md)                                     | Falsch     | **PKI-Certificate-Template**                                 |
| [**ms-PKI-Supersede-Templates**](a-mspki-supersede-templates.md)                       | Falsch     | **PKI-Certificate-Template**                                 |
| [**ms-PKI-Template-Minor-Revision**](a-mspki-template-minor-revision.md)               | Falsch     | **PKI-Certificate-Template**                                 |
| [**ms-PKI-Template-Schema-Version**](a-mspki-template-schema-version.md)               | Falsch     | **PKI-Certificate-Template**                                 |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                              | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                                | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Non-Security-Member-BL**](a-nonsecuritymemberbl.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                                | Richtig      | [**Nach oben**](c-top.md)<br/>                              |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                            | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Objektkategorie**](a-objectcategory.md)                                             | Richtig      | [**Nach oben**](c-top.md)<br/>                              |
| [**Object-Class**](a-objectclass.md)                                                   | Richtig      | [**Nach oben**](c-top.md)<br/>                              |
| [**Objekt-GUID**](a-objectguid.md)                                                     | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Object-Version**](a-objectversion.md)                                               | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Andere bekannte Objekte**](a-otherwellknownobjects.md)                             | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)               | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**PKI-Critical-Extensions**](a-pkicriticalextensions.md)                              | Falsch     | **PKI-Certificate-Template**                                 |
| [**PKI-Default-CSPs**](a-pkidefaultcsps.md)                                            | Falsch     | **PKI-Certificate-Template**                                 |
| [**PKI-Default-Key-Spec**](a-pkidefaultkeyspec.md)                                     | Falsch     | **PKI-Certificate-Template**                                 |
| [**PKI-Enrollment-Access**](a-pkienrollmentaccess.md)                                  | Falsch     | **PKI-Certificate-Template**                                 |
| [**PKI-Ablaufzeitraum**](a-pkiexpirationperiod.md)                                  | Falsch     | **PKI-Certificate-Template**                                 |
| [**PKI-Extended-Key-Usage**](a-pkiextendedkeyusage.md)                                 | Falsch     | **PKI-Certificate-Template**                                 |
| [**PKI-Schlüsselverwendung**](a-pkikeyusage.md)                                                  | Falsch     | **PKI-Certificate-Template**                                 |
| [**PKI-Max-Issuing-Depth**](a-pkimaxissuingdepth.md)                                   | Falsch     | **PKI-Certificate-Template**                                 |
| [**PKI-Überlappungszeitraum**](a-pkioverlapperiod.md)                                        | Falsch     | **PKI-Certificate-Template**                                 |
| [**Mögliche 100000000000**](a-possibleinferiors.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                                      | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Proxyadressen**](a-proxyaddresses.md)                                             | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Query-Policy-BL**](a-querypolicybl.md)                                              | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Rdn**](a-name.md)                                                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                               | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                                    | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Berichte**](a-directreports.md)                                                      | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Reps-From**](a-repsfrom.md)                                                         | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Reps-To**](a-repsto.md)                                                             | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Revision**](a-revision.md)                                                          | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Server-Reference-BL**](a-serverreferencebl.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Nur in erweiterter Ansicht anzeigen**](a-showinadvancedviewonly.md)                          | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Site-Object-BL**](a-siteobjectbl.md)                                                | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                              | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Sub-Refs**](a-subrefs.md)                                                           | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                        | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Systemflags**](a-systemflags.md)                                                   | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**USN geändert**](a-usnchanged.md)                                                     | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**USN-erstellt**](a-usncreated.md)                                                     | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**USN-DSA-last-obj-removed**](a-usndsalastobjremoved.md)                              | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**USN-Intersite**](a-usnintersite.md)                                                 | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                             | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**USN-Quelle**](a-usnsource.md)                                                       | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Wbem-Pfad**](a-wbempath.md)                                                         | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Bekannte Objekte**](a-wellknownobjects.md)                                        | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Bei Änderung**](a-whenchanged.md)                                                   | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Bei der Erstellung**](a-whencreated.md)                                                   | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**WWW-Startseite**](a-wwwhomepage.md)                                                  | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**WWW-Page-Other**](a-url.md)                                                         | False     | [**Nach oben**](c-top.md)<br/>                              |



## <a name="windows-server-2008-extended-rights"></a>Windows Erweiterte Rechte für Server 2008

Diese Klasse enthält die folgenden erweiterten Rechte für Windows Server 2008:



| Allgemeiner Name                                                |
|------------------------------------------------------------|
| [**Zertifikatregistrierung**](r-certificate-enrollment.md) |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2

-   [Attribute](#windows-server-2008-r2-attributes)
-   [Erweiterte Rechte](#windows-server-2008-r2-extended-rights)



| Eingabe | Wert |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | False                                                                                        |
| Object-Category             | 1                                                                                            |
| Default-Object-Category     | \-                                                                                           |
| Governs-Id                  | 1.2.840.113556.1.5.177                                                                       |
| Default-Hiding-Value        | 1                                                                                            |
| Rdn-Att-Id                  | [**Allgemeiner Name**](a-cn.md)<br/>                                                       |
| Unterklasse von                 | [**Nach oben**](c-top.md)<br/>                                                              |
| Mögliche Übergeordnete          | [**Container**](c-container.md)                                                             |
| Zusätzlich           | \-                                                                                           |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                 |
| Standardsicherheitsdeskriptor | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;;; AU) |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2008-r2-attributes"></a>Windows Server 2008 R2-Attribute

Diese Klasse enthält die folgenden Attribute für Windows Server 2008 R2:



| attribute                                                                               | Obligatorisch. | Abgeleitet von                                                 |
|-----------------------------------------------------------------------------------------|-----------|--------------------------------------------------------------|
| [**Administratorbeschreibung**](a-admindescription.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Admin-Display-Name**](a-admindisplayname.md)                                        | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Allowed-Attributes**](a-allowedattributes.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)                    | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)               | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                           | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Kanonischer Name**](a-canonicalname.md)                                               | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Allgemeiner Name**](a-cn.md)                                                             | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Erstellen eines Zeitstempels**](a-createtimestamp.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Beschreibung**](a-description.md)                                                    | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Anzeigename**](a-displayname.md)                                                   | Falsch     | **PKI-Certificate-Template** [ **Top**](c-top.md)<br/> |
| [**Anzeigename– druckbar**](a-displaynameprintable.md)                                | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**DSA-Signature**](a-dsasignature.md)                                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**DS-Core-Propagierungsdaten**](a-dscorepropagationdata.md)                             | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Erweiterungsname**](a-extensionname.md)                                               | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Flaggen**](a-flags.md)                                                                | Falsch     | **PKI-Certificate-Template** [ **Top**](c-top.md)<br/> |
| [**From-Entry**](a-fromentry.md)                                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)                           | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                               | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                              | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Instanztyp**](a-instancetype.md)                                                 | Richtig      | [**Nach oben**](c-top.md)<br/>                              |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                           | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Is-Deleted**](a-isdeleted.md)                                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Is-Member-of-DL**](a-memberof.md)                                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                                      | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Wird wiederverwendet**](a-isrecycled.md)                                                     | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Last-Known-Parent**](a-lastknownparent.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Verwaltete Objekte**](a-managedobjects.md)                                             | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Mastered By**](a-masteredby.md)                                                     | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Modify-Time-Stamp**](a-modifytimestamp.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                             | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                             | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)                     | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                         | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md)             | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md)          | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)                  | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                               | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Enabled-Feature-BL**](a-msds-enabledfeaturebl.md)                             | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)                    | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-is-Domain-for**](a-msds-isdomainfor.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-is-full-replica-for**](a-msds-isfullreplicafor.md)                            | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-is-partial-replica-for**](a-msds-ispartialreplicafor.md)                      | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                                     | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                                     | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-local-Effective-Deletion-Time**](a-msds-localeffectivedeletiontime.md)        | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-local-Effective-Recycle-Time**](a-msds-localeffectiverecycletime.md)          | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Members-For-Az-Role-BL**](a-msds-membersforazrolebl.md)                       | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)                | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)              | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)           | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-NC-Type**](a-msds-nctype.md)                                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                                     | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                           | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-OIDToGroup-Link-BL**](a-msds-oidtogrouplinkbl.md)                             | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)                 | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)                 | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                                    | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-PSO-Applied**](a-msds-psoapplied.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)                  | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                          | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Revealed-DSAs**](a-msds-revealeddsas.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Revealed-List-BL**](a-msds-revealedlistbl.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)                           | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)                           | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                                   | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-PKI-Certificate-Application-Policy**](a-mspki-certificate-application-policy.md) | False     | **PKI-Certificate-Template**                                 |
| [**ms-PKI-Certificate-Name-Flag**](a-mspki-certificate-name-flag.md)                   | False     | **PKI-Certificate-Template**                                 |
| [**ms-PKI-Certificate-Policy**](a-mspki-certificate-policy.md)                         | False     | **PKI-Certificate-Template**                                 |
| [**ms-PKI-Cert-Template-OID**](a-mspki-cert-template-oid.md)                           | False     | **PKI-Certificate-Template**                                 |
| [**ms-PKI-Enrollment-Flag**](a-mspki-enrollment-flag.md)                               | False     | **PKI-Certificate-Template**                                 |
| [**ms-PKI-Minimal-Key-Size**](a-mspki-minimal-key-size.md)                             | False     | **PKI-Certificate-Template**                                 |
| [**ms-PKI-Private-Key-Flag**](a-mspki-private-key-flag.md)                             | False     | **PKI-Certificate-Template**                                 |
| [**ms-PKI-RA-Application-Policies**](a-mspki-ra-application-policies.md)               | False     | **PKI-Certificate-Template**                                 |
| [**ms-PKI-RA-Policies**](a-mspki-ra-policies.md)                                       | False     | **PKI-Certificate-Template**                                 |
| [**ms-PKI-RA-Signature**](a-mspki-ra-signature.md)                                     | False     | **PKI-Certificate-Template**                                 |
| [**ms-PKI-Supersede-Templates**](a-mspki-supersede-templates.md)                       | False     | **PKI-Certificate-Template**                                 |
| [**ms-PKI-Template-Minor-Revision**](a-mspki-template-minor-revision.md)               | False     | **PKI-Certificate-Template**                                 |
| [**ms-PKI-Template-Schema-Version**](a-mspki-template-schema-version.md)               | False     | **PKI-Certificate-Template**                                 |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                              | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                                | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Non-Security-Member-BL**](a-nonsecuritymemberbl.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                                | True      | [**Nach oben**](c-top.md)<br/>                              |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Objektkategorie**](a-objectcategory.md)                                             | True      | [**Nach oben**](c-top.md)<br/>                              |
| [**Object-Class**](a-objectclass.md)                                                   | True      | [**Nach oben**](c-top.md)<br/>                              |
| [**Objekt-GUID**](a-objectguid.md)                                                     | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Object-Version**](a-objectversion.md)                                               | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Andere bekannte Objekte**](a-otherwellknownobjects.md)                             | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)               | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                                  | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**PKI-Critical-Extensions**](a-pkicriticalextensions.md)                              | False     | **PKI-Certificate-Template**                                 |
| [**PKI-Default-CSPs**](a-pkidefaultcsps.md)                                            | False     | **PKI-Certificate-Template**                                 |
| [**PKI-Default-Key-Spec**](a-pkidefaultkeyspec.md)                                     | Falsch     | **PKI-Certificate-Template**                                 |
| [**PKI-Enrollment-Access**](a-pkienrollmentaccess.md)                                  | Falsch     | **PKI-Certificate-Template**                                 |
| [**PKI-Ablaufzeitraum**](a-pkiexpirationperiod.md)                                  | Falsch     | **PKI-Certificate-Template**                                 |
| [**PKI-Extended-Key-Usage**](a-pkiextendedkeyusage.md)                                 | Falsch     | **PKI-Certificate-Template**                                 |
| [**PKI-Schlüsselverwendung**](a-pkikeyusage.md)                                                  | Falsch     | **PKI-Certificate-Template**                                 |
| [**PKI-Max-Issuing-Depth**](a-pkimaxissuingdepth.md)                                   | Falsch     | **PKI-Certificate-Template**                                 |
| [**PKI-Überlappungszeitraum**](a-pkioverlapperiod.md)                                        | Falsch     | **PKI-Certificate-Template**                                 |
| [**Mögliche Hindernisse**](a-possibleinferiors.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                                      | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Proxyadressen**](a-proxyaddresses.md)                                             | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Query-Policy-BL**](a-querypolicybl.md)                                              | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Rdn**](a-name.md)                                                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                               | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                                    | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Berichte**](a-directreports.md)                                                      | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Reps-From**](a-repsfrom.md)                                                         | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Reps-To**](a-repsto.md)                                                             | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Revision**](a-revision.md)                                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                                      | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Server-Reference-BL**](a-serverreferencebl.md)                                      | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Nur in erweiterter Ansicht anzeigen**](a-showinadvancedviewonly.md)                          | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Site-Object-BL**](a-siteobjectbl.md)                                                | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                              | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Sub-Refs**](a-subrefs.md)                                                           | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                        | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Systemflags**](a-systemflags.md)                                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**USN geändert**](a-usnchanged.md)                                                     | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**USN-erstellt**](a-usncreated.md)                                                     | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**USN-DSA-last-obj-removed**](a-usndsalastobjremoved.md)                              | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**USN-Intersite**](a-usnintersite.md)                                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                             | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**USN-Quelle**](a-usnsource.md)                                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Wbem-Pfad**](a-wbempath.md)                                                         | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Bekannte Objekte**](a-wellknownobjects.md)                                        | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Wenn geändert**](a-whenchanged.md)                                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Wenn erstellt**](a-whencreated.md)                                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**WWW-Homepage**](a-wwwhomepage.md)                                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**WWW-Page-Other**](a-url.md)                                                         | Falsch     | [**Nach oben**](c-top.md)<br/>                              |



## <a name="windows-server-2008-r2-extended-rights"></a>Windows Erweiterte Server 2008 R2-Rechte

Diese Klasse enthält die folgenden erweiterten Rechte für Windows Server 2008 R2:



| Allgemeiner Name                                                |
|------------------------------------------------------------|
| [**Zertifikatregistrierung**](r-certificate-enrollment.md) |



## <a name="windows-server-2012"></a>Windows Server 2012

-   [Attribute](#windows-server-2012-attributes)
-   [Erweiterte Rechte](#windows-server-2012-extended-rights)



| Eingabe | Wert |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Falsch                                                                                        |
| Object-Category             | 1                                                                                            |
| Default-Object-Category     | \-                                                                                           |
| Governs-Id                  | 1.2.840.113556.1.5.177                                                                       |
| Default-Hiding-Value        | 1                                                                                            |
| Rdn-Att-Id                  | [**Common-Name**](a-cn.md)<br/>                                                       |
| Unterklasse von                 | [**Nach oben**](c-top.md)<br/>                                                              |
| Mögliche Vorgesetzte          | [**Container**](c-container.md)                                                             |
| Zusätzlich           | \-                                                                                           |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                 |
| Standardsicherheitsdeskriptor | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;;; AU) |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2012-attributes"></a>Windows Server 2012 Attribute

Diese Klasse enthält die folgenden Attribute für Windows Server 2012:



| attribute                                                                                    | Obligatorisch. | Abgeleitet von                                                 |
|----------------------------------------------------------------------------------------------|-----------|--------------------------------------------------------------|
| [**Admin-Description**](a-admindescription.md)                                              | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Administratoranzeigename**](a-admindisplayname.md)                                             | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Allowed-Attributes**](a-allowedattributes.md)                                            | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)                         | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)                    | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                                | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Kanonischer Name**](a-canonicalname.md)                                                    | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Common-Name**](a-cn.md)                                                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Create-Time-Stamp**](a-createtimestamp.md)                                               | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Beschreibung**](a-description.md)                                                         | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Anzeigename**](a-displayname.md)                                                        | Falsch     | **PKI-Certificate-Template** [ **Top**](c-top.md)<br/> |
| [**Display-Name-Printable**](a-displaynameprintable.md)                                     | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**DSA-Signature**](a-dsasignature.md)                                                      | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**DS-Core-Propagierungsdaten**](a-dscorepropagationdata.md)                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Extension-Name**](a-extensionname.md)                                                    | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Flaggen**](a-flags.md)                                                                     | Falsch     | **PKI-Certificate-Template** [ **Top**](c-top.md)<br/> |
| [**From-Entry**](a-fromentry.md)                                                            | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)                                | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                                    | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Instanztyp**](a-instancetype.md)                                                      | Richtig      | [**Nach oben**](c-top.md)<br/>                              |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                                | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Is-Deleted**](a-isdeleted.md)                                                            | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Is-Member-of-DL**](a-memberof.md)                                                        | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                                           | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Wird wiederverwendet**](a-isrecycled.md)                                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Last-Known-Parent**](a-lastknownparent.md)                                               | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Verwaltete Objekte**](a-managedobjects.md)                                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Mastered-By**](a-masteredby.md)                                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Modify-Time-Stamp**](a-modifytimestamp.md)                                               | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)                          | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                              | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md)                  | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md)               | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Claim-Shares-Possible-Values-with-BL**](a-msds-claimsharespossiblevalueswithbl.md) | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)                       | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                                    | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Enabled-Feature-BL**](a-msds-enabledfeaturebl.md)                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)                         | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Is-Domain-For**](a-msds-isdomainfor.md)                                            | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-is-full-replica-for**](a-msds-isfullreplicafor.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-is-partial-replica-for**](a-msds-ispartialreplicafor.md)                           | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Is-Primary-Computer-For**](a-msds-isprimarycomputerfor.md)                         | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-local-Effective-Deletion-Time**](a-msds-localeffectivedeletiontime.md)             | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-local-Effective-Recycle-Time**](a-msds-localeffectiverecycletime.md)               | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                                               | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Members-for-Az-Role-BL**](a-msds-membersforazrolebl.md)                            | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Members-of-Resource-Property-List-BL**](a-msds-membersofresourcepropertylistbl.md) | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                                        | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)                     | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)                   | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)                | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-NC-Type**](a-msds-nctype.md)                                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                                | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-OIDToGroup-Link-BL**](a-msds-oidtogrouplinkbl.md)                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Operations-for-Az-Role-BL**](a-msds-operationsforazrolebl.md)                      | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Operations-for-Az-Task-BL**](a-msds-operationsforaztaskbl.md)                      | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-PSO-Applied**](a-msds-psoapplied.md)                                               | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)                       | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                               | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Revealed-DSAs**](a-msds-revealeddsas.md)                                           | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Revealed-List-BL**](a-msds-revealedlistbl.md)                                      | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Tasks-for-Az-Role-BL**](a-msds-tasksforazrolebl.md)                                | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Tasks-for-Az-Task-BL**](a-msds-tasksforaztaskbl.md)                                | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-TDO-Egress-BL**](a-msds-tdoegressbl.md)                                            | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-TDO-Ingress-BL**](a-msds-tdoingressbl.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Value-Type-Reference-BL**](a-msds-valuetypereferencebl.md)                         | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                                        | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-PKI-Certificate-Application-Policy**](a-mspki-certificate-application-policy.md)      | Falsch     | **PKI-Certificate-Template**                                 |
| [**ms-PKI-Certificate-Name-Flag**](a-mspki-certificate-name-flag.md)                        | Falsch     | **PKI-Certificate-Template**                                 |
| [**ms-PKI-Certificate-Policy**](a-mspki-certificate-policy.md)                              | Falsch     | **PKI-Certificate-Template**                                 |
| [**ms-PKI-Cert-Template-OID**](a-mspki-cert-template-oid.md)                                | Falsch     | **PKI-Certificate-Template**                                 |
| [**ms-PKI-Enrollment-Flag**](a-mspki-enrollment-flag.md)                                    | Falsch     | **PKI-Certificate-Template**                                 |
| [**ms-PKI-Minimal-Key-Size**](a-mspki-minimal-key-size.md)                                  | Falsch     | **PKI-Certificate-Template**                                 |
| [**ms-PKI-Private-Key-Flag**](a-mspki-private-key-flag.md)                                  | Falsch     | **PKI-Certificate-Template**                                 |
| [**ms-PKI-RA-Application-Policies**](a-mspki-ra-application-policies.md)                    | Falsch     | **PKI-Certificate-Template**                                 |
| [**ms-PKI-RA-Policies**](a-mspki-ra-policies.md)                                            | Falsch     | **PKI-Certificate-Template**                                 |
| [**ms-PKI-RA-Signature**](a-mspki-ra-signature.md)                                          | Falsch     | **PKI-Certificate-Template**                                 |
| [**ms-PKI-Supersede-Templates**](a-mspki-supersede-templates.md)                            | Falsch     | **PKI-Certificate-Template**                                 |
| [**ms-PKI-Template-Minor-Revision**](a-mspki-template-minor-revision.md)                    | Falsch     | **PKI-Certificate-Template**                                 |
| [**ms-PKI-Template-Schema-Version**](a-mspki-template-schema-version.md)                    | Falsch     | **PKI-Certificate-Template**                                 |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                                     | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Non-Security-Member-BL**](a-nonsecuritymemberbl.md)                                      | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                                     | Richtig      | [**Nach oben**](c-top.md)<br/>                              |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Objektkategorie**](a-objectcategory.md)                                                  | Richtig      | [**Nach oben**](c-top.md)<br/>                              |
| [**Object-Class**](a-objectclass.md)                                                        | Richtig      | [**Nach oben**](c-top.md)<br/>                              |
| [**Objekt-GUID**](a-objectguid.md)                                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Object-Version**](a-objectversion.md)                                                    | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Andere bekannte Objekte**](a-otherwellknownobjects.md)                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)                    | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**PKI-Critical-Extensions**](a-pkicriticalextensions.md)                                   | Falsch     | **PKI-Certificate-Template**                                 |
| [**PKI-Default-CSPs**](a-pkidefaultcsps.md)                                                 | Falsch     | **PKI-Certificate-Template**                                 |
| [**PKI-Default-Key-Spec**](a-pkidefaultkeyspec.md)                                          | Falsch     | **PKI-Certificate-Template**                                 |
| [**PKI-Enrollment-Access**](a-pkienrollmentaccess.md)                                       | Falsch     | **PKI-Certificate-Template**                                 |
| [**PKI-Ablaufzeitraum**](a-pkiexpirationperiod.md)                                       | Falsch     | **PKI-Certificate-Template**                                 |
| [**PKI-Extended-Key-Usage**](a-pkiextendedkeyusage.md)                                      | Falsch     | **PKI-Certificate-Template**                                 |
| [**PKI-Schlüsselverwendung**](a-pkikeyusage.md)                                                       | Falsch     | **PKI-Certificate-Template**                                 |
| [**PKI-Max-Issuing-Depth**](a-pkimaxissuingdepth.md)                                        | Falsch     | **PKI-Certificate-Template**                                 |
| [**PKI-Überlappungszeitraum**](a-pkioverlapperiod.md)                                             | Falsch     | **PKI-Certificate-Template**                                 |
| [**Mögliche 100000000000**](a-possibleinferiors.md)                                            | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                                           | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Proxyadressen**](a-proxyaddresses.md)                                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Query-Policy-BL**](a-querypolicybl.md)                                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Rdn**](a-name.md)                                                                        | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                                    | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Berichte**](a-directreports.md)                                                           | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Reps-From**](a-repsfrom.md)                                                              | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Reps-To**](a-repsto.md)                                                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Revision**](a-revision.md)                                                               | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                                           | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Server-Reference-BL**](a-serverreferencebl.md)                                           | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Nur in erweiterter Ansicht anzeigen**](a-showinadvancedviewonly.md)                               | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Site-Object-BL**](a-siteobjectbl.md)                                                     | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Sub-Refs**](a-subrefs.md)                                                                | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                             | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Systemflags**](a-systemflags.md)                                                        | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**USN geändert**](a-usnchanged.md)                                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**USN-erstellt**](a-usncreated.md)                                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**USN-DSA-last-obj-removed**](a-usndsalastobjremoved.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**USN-Intersite**](a-usnintersite.md)                                                      | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**USN-Quelle**](a-usnsource.md)                                                            | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Wbem-Pfad**](a-wbempath.md)                                                              | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Bekannte Objekte**](a-wellknownobjects.md)                                             | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Bei Änderung**](a-whenchanged.md)                                                        | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**Bei der Erstellung**](a-whencreated.md)                                                        | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**WWW-Startseite**](a-wwwhomepage.md)                                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                              |
| [**WWW-Page-Other**](a-url.md)                                                              | Falsch     | [**Nach oben**](c-top.md)<br/>                              |



## <a name="windows-server-2012-extended-rights"></a>Windows Server 2012 Erweiterte Rechte

Diese Klasse enthält die folgenden erweiterten Rechte für Windows Server 2012:



| Allgemeiner Name                                                |
|------------------------------------------------------------|
| [**Zertifikatregistrierung**](r-certificate-enrollment.md) |



 

 





