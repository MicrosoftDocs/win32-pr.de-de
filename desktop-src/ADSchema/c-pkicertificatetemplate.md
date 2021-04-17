---
title: PKI-Certificate-Template-Klasse
description: Enthält Informationen für Zertifikate, die vom Zertifikat Server ausgestellt werden.
ms.assetid: 9b6ca989-058c-461b-ba3d-5b29ea15cbbc
ms.tgt_platform: multiple
keywords:
- PKI-Zertifikat-Vorlagen Klasse AD-Schema
- pkicertificatetemplate-Klasse, AD-Schema
topic_type:
- apiref
api_name:
- PKI-Certificate-Template
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c79f56b790b4bd6f4759891ec489e807c5e2a6cd
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104479514"
---
# <a name="pki-certificate-template-class"></a>PKI-Certificate-Template-Klasse

Enthält Informationen für Zertifikate, die vom Zertifikat Server ausgestellt werden.



| Eingabe | Wert |
|-------------------|--------------------------------------|
| CN                | PKI-Zertifikat-Vorlage             |
| LDAP-Display-Name | pkicertificatetemplate               |
| Berechtigung aktualisieren  | \-                                   |
| Aktualisierungshäufigkeit  | \-                                   |
| Schema-ID-GUID    | e5209ca2-3bba-11d2-90cc-00c04fd91ab1 |



## <a name="implementations"></a>Implementierungen

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server

-   [Attribute](#windows-2000-server-attributes)
-   [Erweiterte Rechte](#windows-2000-server-extended-rights)



| Eingabe | Wert |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | False                                                                                        |
| Object-Category             | 1                                                                                            |
| Default-Object-Category     | \-                                                                                           |
| Governs-Id                  | 1.2.840.113556.1.5.177                                                                       |
| Standard-ausblenden-Wert        | 1                                                                                            |
| RDN-ATT-ID                  | [**Gemeinsamer Name**](a-cn.md)<br/>                                                       |
| Unterklasse von                 | [**Nach oben**](c-top.md)<br/>                                                              |
| Mögliche Vorgesetzten          | [**Container**](c-container.md)                                                             |
| Zusätzlich           | \-                                                                                           |
| NT-Security-Descriptor      | o:Bag: schlecht: S:                                                                                 |
| Standard Sicherheits Beschreibung | D: (A;; rpwpcrccdclclorcwowdsddtsw;;;D a) (a;; Rpwpcrccdclclorcwowdsddtsw;;; SY) (A;; Rplclorc;;; Thaus |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-2000-server-attributes"></a>Windows 2000-Server Attribute

Diese Klasse enthält die folgenden Attribute für Windows 2000 Server:



| Attribut                                                                 | Obligatorisch. | Abgeleitet von                                                 |
|---------------------------------------------------------------------------|-----------|--------------------------------------------------------------|
| [**Administrator: Beschreibung**](a-admindescription.md)                           | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Administrator-Anzeige Name**](a-admindisplayname.md)                          | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Zulässige Attribute**](a-allowedattributes.md)                         | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Zulässige Attribute-gültig**](a-allowedattributeseffective.md)      | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Zulässige, untergeordnete Klassen**](a-allowedchildclasses.md)                    | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Zulässig-untergeordnete Klassen-gültig**](a-allowedchildclasseseffective.md) | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)             | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Kanonischer Name**](a-canonicalname.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Gemeinsamer Name**](a-cn.md)                                               | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Create-Zeitstempel**](a-createtimestamp.md)                            | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Beschreibung**](a-description.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Anzeige Name**](a-displayname.md)                                     | False     | **PKI-Zertifikat-Vorlage** [ **oben**](c-top.md)<br/> |
| [**Anzeige Name-druckdruck**](a-displaynameprintable.md)                  | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**DSA-Signatur**](a-dsasignature.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**DS-Core-propagierungs Daten**](a-dscorepropagationdata.md)               | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Erweiterungs Name**](a-extensionname.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Fahren**](a-flags.md)                                                  | False     | **PKI-Zertifikat-Vorlage** [ **oben**](c-top.md)<br/> |
| [**Aus-Eintrag**](a-fromentry.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)             | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                 | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**"F"-Rollen Besitzer**](a-fsmoroleowner.md)                                | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Instanztyp**](a-instancetype.md)                                   | Richtig      | [**Nach oben**](c-top.md)<br/>                              |
| [**Is-critical-System-Object**](a-iscriticalsystemobject.md)             | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Ist-gelöscht**](a-isdeleted.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Is-Member-of-DL**](a-memberof.md)                                     | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Is-Privilege-Inhaber**](a-isprivilegeholder.md)                        | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Letztes-bekannt/übergeordnetes Element**](a-lastknownparent.md)                            | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Verwaltete Objekte**](a-managedobjects.md)                               | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Verwaltet von**](a-masteredby.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Modify-Zeitstempel**](a-modifytimestamp.md)                            | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**MS-DS-Konsistenz-untergeordnet-Anzahl**](a-ms-ds-consistencychildcount.md)    | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                 | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**NetBoot-SCP-BL**](a-netbootscpbl.md)                                  | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Nicht sicherheitsmitglied-BL**](a-nonsecuritymemberbl.md)                   | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                  | Richtig      | [**Nach oben**](c-top.md)<br/>                              |
| [**Obj-Dist-Name**](a-distinguishedname.md)                              | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Objekt-Kategorie**](a-objectcategory.md)                               | Richtig      | [**Nach oben**](c-top.md)<br/>                              |
| [**Object-Klasse**](a-objectclass.md)                                     | Richtig      | [**Nach oben**](c-top.md)<br/>                              |
| [**Objekt-GUID**](a-objectguid.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Objekt-Version**](a-objectversion.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Andere-bekannte Objekte**](a-otherwellknownobjects.md)               | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Partial-Attribute-löschen-List**](a-partialattributedeletionlist.md) | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Partiell-Attribut Satz**](a-partialattributeset.md)                    | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**PKI-Critical-Extensions**](a-pkicriticalextensions.md)                | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**PKI-default-CSPs**](a-pkidefaultcsps.md)                              | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**PKI-default-Key-spec**](a-pkidefaultkeyspec.md)                       | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**PKI-Registrierung-Zugriff**](a-pkienrollmentaccess.md)                    | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**PKI-Ablauf Zeitraum**](a-pkiexpirationperiod.md)                    | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**PKI-erweiterte Schlüssel Verwendung**](a-pkiextendedkeyusage.md)                   | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**PKI-Schlüssel-Verwendung**](a-pkikeyusage.md)                                    | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**PKI-Max-ausstellende Tiefe**](a-pkimaxissuingdepth.md)                     | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**PKI-Überlappung-Zeitraum**](a-pkioverlapperiod.md)                          | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**Mögliche-minderwertig**](a-possibleinferiors.md)                         | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Proxy-Objekt Name**](a-proxiedobjectname.md)                        | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Proxy Adressen**](a-proxyaddresses.md)                               | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Abfrage-Richtlinie-BL**](a-querypolicybl.md)                                | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**RDN**](a-name.md)                                                     | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                 | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**REPL-Update-Vector**](a-repluptodatevector.md)                      | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Berichte**](a-directreports.md)                                        | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Reps-from**](a-repsfrom.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Reps-to**](a-repsto.md)                                               | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Novel**](a-revision.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**SD-Rechte**](a-sdrightseffective.md)                        | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Server-Reference-BL**](a-serverreferencebl.md)                        | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Anzeigen-in-Advanced-nur anzeigen**](a-showinadvancedviewonly.md)            | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Site-Object-BL**](a-siteobjectbl.md)                                  | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Sub-Refs**](a-subrefs.md)                                             | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Subschemasubentry**](a-subschemasubentry.md)                          | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**SystemFlags**](a-systemflags.md)                                     | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Die Anwendung wurde geändert.**](a-usnchanged.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Von der Anwendung erstellte**](a-usncreated.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**USA-DSA-letzte-obj-entfernt**](a-usndsalastobjremoved.md)                | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Standort-und standortübergreifende standortübergreifende**](a-usnintersite.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**"An-Last-obj-REM"**](a-usnlastobjrem.md)                               | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Quell Code Quelle**](a-usnsource.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**WBEM-Pfad**](a-wbempath.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Bekannte Objekte**](a-wellknownobjects.md)                          | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Bei Änderung**](a-whenchanged.md)                                     | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Bei Erstellung**](a-whencreated.md)                                     | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**WWW-Homepage**](a-wwwhomepage.md)                                    | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**WWW-Page-other**](a-url.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                              |



## <a name="windows-2000-server-extended-rights"></a>Erweiterte Rechte für Windows 2000 Server

Diese Klasse enthält die folgenden erweiterten Rechte für Windows Server 2000-Server:



| Allgemeiner Name                                                |
|------------------------------------------------------------|
| [**Zertifikat-Registrierung**](r-certificate-enrollment.md) |



## <a name="windows-server-2003"></a>Windows Server 2003

-   [Attribute](#windows-server-2003-attributes)
-   [Erweiterte Rechte](#windows-server-2003-extended-rights)



| Eingabe | Wert |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | False                                                                                        |
| Object-Category             | 1                                                                                            |
| Default-Object-Category     | \-                                                                                           |
| Governs-Id                  | 1.2.840.113556.1.5.177                                                                       |
| Standard-ausblenden-Wert        | 1                                                                                            |
| RDN-ATT-ID                  | [**Gemeinsamer Name**](a-cn.md)<br/>                                                       |
| Unterklasse von                 | [**Nach oben**](c-top.md)<br/>                                                              |
| Mögliche Vorgesetzten          | [**Container**](c-container.md)                                                             |
| Zusätzlich           | \-                                                                                           |
| NT-Security-Descriptor      | o:Bag: schlecht: S:                                                                                 |
| Standard Sicherheits Beschreibung | D: (A;; rpwpcrccdclclorcwowdsddtsw;;;D a) (a;; Rpwpcrccdclclorcwowdsddtsw;;; SY) (A;; Rplclorc;;; Thaus |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2003-attributes"></a>Windows Server 2003-Attribute

Diese Klasse enthält die folgenden Attribute für Windows Server 2003:



| Attribut                                                                               | Obligatorisch. | Abgeleitet von                                                 |
|-----------------------------------------------------------------------------------------|-----------|--------------------------------------------------------------|
| [**Administrator: Beschreibung**](a-admindescription.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Administrator-Anzeige Name**](a-admindisplayname.md)                                        | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Zulässige Attribute**](a-allowedattributes.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Zulässige Attribute-gültig**](a-allowedattributeseffective.md)                    | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Zulässige, untergeordnete Klassen**](a-allowedchildclasses.md)                                  | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Zulässig-untergeordnete Klassen-gültig**](a-allowedchildclasseseffective.md)               | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                           | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Kanonischer Name**](a-canonicalname.md)                                               | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Gemeinsamer Name**](a-cn.md)                                                             | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Create-Zeitstempel**](a-createtimestamp.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Beschreibung**](a-description.md)                                                    | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Anzeige Name**](a-displayname.md)                                                   | False     | **PKI-Zertifikat-Vorlage** [ **oben**](c-top.md)<br/> |
| [**Anzeige Name-druckdruck**](a-displaynameprintable.md)                                | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**DSA-Signatur**](a-dsasignature.md)                                                 | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**DS-Core-propagierungs Daten**](a-dscorepropagationdata.md)                             | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Erweiterungs Name**](a-extensionname.md)                                               | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Fahren**](a-flags.md)                                                                | False     | **PKI-Zertifikat-Vorlage** [ **oben**](c-top.md)<br/> |
| [**Aus-Eintrag**](a-fromentry.md)                                                       | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                           | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                               | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**"F"-Rollen Besitzer**](a-fsmoroleowner.md)                                              | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Instanztyp**](a-instancetype.md)                                                 | Richtig      | [**Nach oben**](c-top.md)<br/>                              |
| [**Is-critical-System-Object**](a-iscriticalsystemobject.md)                           | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Ist-gelöscht**](a-isdeleted.md)                                                       | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Is-Member-of-DL**](a-memberof.md)                                                   | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Is-Privilege-Inhaber**](a-isprivilegeholder.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Letztes-bekannt/übergeordnetes Element**](a-lastknownparent.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Verwaltete Objekte**](a-managedobjects.md)                                             | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Verwaltet von**](a-masteredby.md)                                                     | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Modify-Zeitstempel**](a-modifytimestamp.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**MS-com-partitionsetlink**](a-mscom-partitionsetlink.md)                             | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**MS-com-userlink**](a-mscom-userlink.md)                                             | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-ca-immed-untergeordnete Elemente**](a-msds-approx-immed-subordinates.md)             | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**MS-DS-Konsistenz-untergeordnet-Anzahl**](a-ms-ds-consistencychildcount.md)                  | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                               | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-gemastert von**](a-msds-masteredby.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Members-für-AZ-Role-BL**](a-msds-membersforazrolebl.md)                       | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-NC-repl-Cursor**](a-msds-ncreplcursors.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-NC-repl-Inbound-Nachbarn**](a-msds-ncreplinboundneighbors.md)                | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-NC-repl-Outbound-Nachbarn**](a-msds-ncreploutboundneighbors.md)              | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                                     | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                           | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)                 | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)                 | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)                  | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                          | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Tasks-für-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                           | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Tasks-für-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                           | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                                   | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**MS-PKI-Certificate-Application-Policy**](a-mspki-certificate-application-policy.md) | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**MS-PKI-Certificate-Name-Flag**](a-mspki-certificate-name-flag.md)                   | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**MS-PKI-Certificate-Policy**](a-mspki-certificate-policy.md)                         | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**MS-PKI-CERT-Template-OID**](a-mspki-cert-template-oid.md)                           | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**MS-PKI-Registrierungsflag**](a-mspki-enrollment-flag.md)                               | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**MS-PKI-minimale Schlüsselgröße**](a-mspki-minimal-key-size.md)                             | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**MS-PKI-Private-Key-Flag**](a-mspki-private-key-flag.md)                             | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**MS-PKI-RA-Application-Policies**](a-mspki-ra-application-policies.md)               | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**MS-PKI-RA-Richtlinien**](a-mspki-ra-policies.md)                                       | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**MS-PKI-RA-Signature**](a-mspki-ra-signature.md)                                     | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**MS-PKI-abgelöst-Vorlagen**](a-mspki-supersede-templates.md)                       | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**MS-PKI-Template-Minor-Revision**](a-mspki-template-minor-revision.md)               | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**MS-PKI-Template-Schema-Version**](a-mspki-template-schema-version.md)               | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**NetBoot-SCP-BL**](a-netbootscpbl.md)                                                | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Nicht sicherheitsmitglied-BL**](a-nonsecuritymemberbl.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                                | Richtig      | [**Nach oben**](c-top.md)<br/>                              |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Objekt-Kategorie**](a-objectcategory.md)                                             | Richtig      | [**Nach oben**](c-top.md)<br/>                              |
| [**Object-Klasse**](a-objectclass.md)                                                   | Richtig      | [**Nach oben**](c-top.md)<br/>                              |
| [**Objekt-GUID**](a-objectguid.md)                                                     | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Objekt-Version**](a-objectversion.md)                                               | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Andere-bekannte Objekte**](a-otherwellknownobjects.md)                             | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Partial-Attribute-löschen-List**](a-partialattributedeletionlist.md)               | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Partiell-Attribut Satz**](a-partialattributeset.md)                                  | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**PKI-Critical-Extensions**](a-pkicriticalextensions.md)                              | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**PKI-default-CSPs**](a-pkidefaultcsps.md)                                            | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**PKI-default-Key-spec**](a-pkidefaultkeyspec.md)                                     | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**PKI-Registrierung-Zugriff**](a-pkienrollmentaccess.md)                                  | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**PKI-Ablauf Zeitraum**](a-pkiexpirationperiod.md)                                  | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**PKI-erweiterte Schlüssel Verwendung**](a-pkiextendedkeyusage.md)                                 | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**PKI-Schlüssel-Verwendung**](a-pkikeyusage.md)                                                  | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**PKI-Max-ausstellende Tiefe**](a-pkimaxissuingdepth.md)                                   | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**PKI-Überlappung-Zeitraum**](a-pkioverlapperiod.md)                                        | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**Mögliche-minderwertig**](a-possibleinferiors.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Proxy-Objekt Name**](a-proxiedobjectname.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Proxy Adressen**](a-proxyaddresses.md)                                             | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Abfrage-Richtlinie-BL**](a-querypolicybl.md)                                              | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**RDN**](a-name.md)                                                                   | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                               | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**REPL-Update-Vector**](a-repluptodatevector.md)                                    | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Berichte**](a-directreports.md)                                                      | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Reps-from**](a-repsfrom.md)                                                         | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Reps-to**](a-repsto.md)                                                             | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Novel**](a-revision.md)                                                          | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**SD-Rechte**](a-sdrightseffective.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Server-Reference-BL**](a-serverreferencebl.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Anzeigen-in-Advanced-nur anzeigen**](a-showinadvancedviewonly.md)                          | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Site-Object-BL**](a-siteobjectbl.md)                                                | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Struktur-Objekt-Klasse**](a-structuralobjectclass.md)                              | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Sub-Refs**](a-subrefs.md)                                                           | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Subschemasubentry**](a-subschemasubentry.md)                                        | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**SystemFlags**](a-systemflags.md)                                                   | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Die Anwendung wurde geändert.**](a-usnchanged.md)                                                     | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Von der Anwendung erstellte**](a-usncreated.md)                                                     | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**USA-DSA-letzte-obj-entfernt**](a-usndsalastobjremoved.md)                              | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Standort-und standortübergreifende standortübergreifende**](a-usnintersite.md)                                                 | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**"An-Last-obj-REM"**](a-usnlastobjrem.md)                                             | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Quell Code Quelle**](a-usnsource.md)                                                       | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**WBEM-Pfad**](a-wbempath.md)                                                         | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Bekannte Objekte**](a-wellknownobjects.md)                                        | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Bei Änderung**](a-whenchanged.md)                                                   | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Bei Erstellung**](a-whencreated.md)                                                   | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**WWW-Homepage**](a-wwwhomepage.md)                                                  | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**WWW-Page-other**](a-url.md)                                                         | False     | [**Nach oben**](c-top.md)<br/>                              |



## <a name="windows-server-2003-extended-rights"></a>Erweiterte Rechte für Windows Server 2003

Diese Klasse enthält die folgenden erweiterten Rechte für Windows Server 2003:



| Allgemeiner Name                                                |
|------------------------------------------------------------|
| [**Zertifikat-Registrierung**](r-certificate-enrollment.md) |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2

-   [Attribute](#windows-server-2003-r2-attributes)
-   [Erweiterte Rechte](#windows-server-2003-r2-extended-rights)



| Eingabe | Wert |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | False                                                                                        |
| Object-Category             | 1                                                                                            |
| Default-Object-Category     | \-                                                                                           |
| Governs-Id                  | 1.2.840.113556.1.5.177                                                                       |
| Standard-ausblenden-Wert        | 1                                                                                            |
| RDN-ATT-ID                  | [**Gemeinsamer Name**](a-cn.md)<br/>                                                       |
| Unterklasse von                 | [**Nach oben**](c-top.md)<br/>                                                              |
| Mögliche Vorgesetzten          | [**Container**](c-container.md)                                                             |
| Zusätzlich           | \-                                                                                           |
| NT-Security-Descriptor      | o:Bag: schlecht: S:                                                                                 |
| Standard Sicherheits Beschreibung | D: (A;; rpwpcrccdclclorcwowdsddtsw;;;D a) (a;; Rpwpcrccdclclorcwowdsddtsw;;; SY) (A;; Rplclorc;;; Thaus |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2003-r2-attributes"></a>Windows Server 2003 R2-Attribute

Diese Klasse enthält die folgenden Attribute für Windows Server 2003 R2:



| Attribut                                                                               | Obligatorisch. | Abgeleitet von                                                 |
|-----------------------------------------------------------------------------------------|-----------|--------------------------------------------------------------|
| [**Administrator: Beschreibung**](a-admindescription.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Administrator-Anzeige Name**](a-admindisplayname.md)                                        | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Zulässige Attribute**](a-allowedattributes.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Zulässige Attribute-gültig**](a-allowedattributeseffective.md)                    | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Zulässige, untergeordnete Klassen**](a-allowedchildclasses.md)                                  | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Zulässig-untergeordnete Klassen-gültig**](a-allowedchildclasseseffective.md)               | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                           | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Kanonischer Name**](a-canonicalname.md)                                               | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Gemeinsamer Name**](a-cn.md)                                                             | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Create-Zeitstempel**](a-createtimestamp.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Beschreibung**](a-description.md)                                                    | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Anzeige Name**](a-displayname.md)                                                   | False     | **PKI-Zertifikat-Vorlage** [ **oben**](c-top.md)<br/> |
| [**Anzeige Name-druckdruck**](a-displaynameprintable.md)                                | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**DSA-Signatur**](a-dsasignature.md)                                                 | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**DS-Core-propagierungs Daten**](a-dscorepropagationdata.md)                             | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Erweiterungs Name**](a-extensionname.md)                                               | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Fahren**](a-flags.md)                                                                | False     | **PKI-Zertifikat-Vorlage** [ **oben**](c-top.md)<br/> |
| [**Aus-Eintrag**](a-fromentry.md)                                                       | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                           | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                               | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**"F"-Rollen Besitzer**](a-fsmoroleowner.md)                                              | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Instanztyp**](a-instancetype.md)                                                 | Richtig      | [**Nach oben**](c-top.md)<br/>                              |
| [**Is-critical-System-Object**](a-iscriticalsystemobject.md)                           | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Ist-gelöscht**](a-isdeleted.md)                                                       | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Is-Member-of-DL**](a-memberof.md)                                                   | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Is-Privilege-Inhaber**](a-isprivilegeholder.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Letztes-bekannt/übergeordnetes Element**](a-lastknownparent.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Verwaltete Objekte**](a-managedobjects.md)                                             | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Verwaltet von**](a-masteredby.md)                                                     | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Modify-Zeitstempel**](a-modifytimestamp.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**MS-com-partitionsetlink**](a-mscom-partitionsetlink.md)                             | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**MS-com-userlink**](a-mscom-userlink.md)                                             | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**MS-DFSR-computerreferencebl**](a-msdfsr-computerreferencebl.md)                     | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**MS-DFSR-mitgliedreferencebl**](a-msdfsr-memberreferencebl.md)                         | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-ca-immed-untergeordnete Elemente**](a-msds-approx-immed-subordinates.md)             | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**MS-DS-Konsistenz-untergeordnet-Anzahl**](a-ms-ds-consistencychildcount.md)                  | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                               | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-gemastert von**](a-msds-masteredby.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Members-für-AZ-Role-BL**](a-msds-membersforazrolebl.md)                       | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-NC-repl-Cursor**](a-msds-ncreplcursors.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-NC-repl-Inbound-Nachbarn**](a-msds-ncreplinboundneighbors.md)                | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-NC-repl-Outbound-Nachbarn**](a-msds-ncreploutboundneighbors.md)              | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                                     | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                           | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)                 | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)                 | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)                  | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                          | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Tasks-für-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                           | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Tasks-für-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                           | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                                   | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**MS-PKI-Certificate-Application-Policy**](a-mspki-certificate-application-policy.md) | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**MS-PKI-Certificate-Name-Flag**](a-mspki-certificate-name-flag.md)                   | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**MS-PKI-Certificate-Policy**](a-mspki-certificate-policy.md)                         | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**MS-PKI-CERT-Template-OID**](a-mspki-cert-template-oid.md)                           | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**MS-PKI-Registrierungsflag**](a-mspki-enrollment-flag.md)                               | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**MS-PKI-minimale Schlüsselgröße**](a-mspki-minimal-key-size.md)                             | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**MS-PKI-Private-Key-Flag**](a-mspki-private-key-flag.md)                             | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**MS-PKI-RA-Application-Policies**](a-mspki-ra-application-policies.md)               | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**MS-PKI-RA-Richtlinien**](a-mspki-ra-policies.md)                                       | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**MS-PKI-RA-Signature**](a-mspki-ra-signature.md)                                     | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**MS-PKI-abgelöst-Vorlagen**](a-mspki-supersede-templates.md)                       | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**MS-PKI-Template-Minor-Revision**](a-mspki-template-minor-revision.md)               | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**MS-PKI-Template-Schema-Version**](a-mspki-template-schema-version.md)               | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**msSFU-30-POSIX-Member-of**](a-mssfu30posixmemberof.md)                              | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**NetBoot-SCP-BL**](a-netbootscpbl.md)                                                | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Nicht sicherheitsmitglied-BL**](a-nonsecuritymemberbl.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                                | Richtig      | [**Nach oben**](c-top.md)<br/>                              |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Objekt-Kategorie**](a-objectcategory.md)                                             | Richtig      | [**Nach oben**](c-top.md)<br/>                              |
| [**Object-Klasse**](a-objectclass.md)                                                   | Richtig      | [**Nach oben**](c-top.md)<br/>                              |
| [**Objekt-GUID**](a-objectguid.md)                                                     | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Objekt-Version**](a-objectversion.md)                                               | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Andere-bekannte Objekte**](a-otherwellknownobjects.md)                             | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Partial-Attribute-löschen-List**](a-partialattributedeletionlist.md)               | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Partiell-Attribut Satz**](a-partialattributeset.md)                                  | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**PKI-Critical-Extensions**](a-pkicriticalextensions.md)                              | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**PKI-default-CSPs**](a-pkidefaultcsps.md)                                            | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**PKI-default-Key-spec**](a-pkidefaultkeyspec.md)                                     | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**PKI-Registrierung-Zugriff**](a-pkienrollmentaccess.md)                                  | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**PKI-Ablauf Zeitraum**](a-pkiexpirationperiod.md)                                  | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**PKI-erweiterte Schlüssel Verwendung**](a-pkiextendedkeyusage.md)                                 | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**PKI-Schlüssel-Verwendung**](a-pkikeyusage.md)                                                  | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**PKI-Max-ausstellende Tiefe**](a-pkimaxissuingdepth.md)                                   | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**PKI-Überlappung-Zeitraum**](a-pkioverlapperiod.md)                                        | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**Mögliche-minderwertig**](a-possibleinferiors.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Proxy-Objekt Name**](a-proxiedobjectname.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Proxy Adressen**](a-proxyaddresses.md)                                             | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Abfrage-Richtlinie-BL**](a-querypolicybl.md)                                              | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**RDN**](a-name.md)                                                                   | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                               | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**REPL-Update-Vector**](a-repluptodatevector.md)                                    | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Berichte**](a-directreports.md)                                                      | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Reps-from**](a-repsfrom.md)                                                         | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Reps-to**](a-repsto.md)                                                             | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Novel**](a-revision.md)                                                          | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**SD-Rechte**](a-sdrightseffective.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Server-Reference-BL**](a-serverreferencebl.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Anzeigen-in-Advanced-nur anzeigen**](a-showinadvancedviewonly.md)                          | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Site-Object-BL**](a-siteobjectbl.md)                                                | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Struktur-Objekt-Klasse**](a-structuralobjectclass.md)                              | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Sub-Refs**](a-subrefs.md)                                                           | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Subschemasubentry**](a-subschemasubentry.md)                                        | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**SystemFlags**](a-systemflags.md)                                                   | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Die Anwendung wurde geändert.**](a-usnchanged.md)                                                     | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Von der Anwendung erstellte**](a-usncreated.md)                                                     | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**USA-DSA-letzte-obj-entfernt**](a-usndsalastobjremoved.md)                              | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Standort-und standortübergreifende standortübergreifende**](a-usnintersite.md)                                                 | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**"An-Last-obj-REM"**](a-usnlastobjrem.md)                                             | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Quell Code Quelle**](a-usnsource.md)                                                       | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**WBEM-Pfad**](a-wbempath.md)                                                         | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Bekannte Objekte**](a-wellknownobjects.md)                                        | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Bei Änderung**](a-whenchanged.md)                                                   | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Bei Erstellung**](a-whencreated.md)                                                   | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**WWW-Homepage**](a-wwwhomepage.md)                                                  | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**WWW-Page-other**](a-url.md)                                                         | False     | [**Nach oben**](c-top.md)<br/>                              |



## <a name="windows-server-2003-r2-extended-rights"></a>Erweiterte Rechte für Windows Server 2003 R2

Diese Klasse enthält die folgenden erweiterten Rechte für Windows Server 2003 R2:



| Allgemeiner Name                                                |
|------------------------------------------------------------|
| [**Zertifikat-Registrierung**](r-certificate-enrollment.md) |



## <a name="windows-server-2008"></a>Windows Server 2008

-   [Attribute](#windows-server-2008-attributes)
-   [Erweiterte Rechte](#windows-server-2008-extended-rights)



| Eingabe | Wert |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | False                                                                                        |
| Object-Category             | 1                                                                                            |
| Default-Object-Category     | \-                                                                                           |
| Governs-Id                  | 1.2.840.113556.1.5.177                                                                       |
| Standard-ausblenden-Wert        | 1                                                                                            |
| RDN-ATT-ID                  | [**Gemeinsamer Name**](a-cn.md)<br/>                                                       |
| Unterklasse von                 | [**Nach oben**](c-top.md)<br/>                                                              |
| Mögliche Vorgesetzten          | [**Container**](c-container.md)                                                             |
| Zusätzlich           | \-                                                                                           |
| NT-Security-Descriptor      | o:Bag: schlecht: S:                                                                                 |
| Standard Sicherheits Beschreibung | D: (A;; rpwpcrccdclclorcwowdsddtsw;;;D a) (a;; Rpwpcrccdclclorcwowdsddtsw;;; SY) (A;; Rplclorc;;; Thaus |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2008-attributes"></a>Windows Server 2008-Attribute

Diese Klasse enthält die folgenden Attribute für Windows Server 2008:



| Attribut                                                                               | Obligatorisch. | Abgeleitet von                                                 |
|-----------------------------------------------------------------------------------------|-----------|--------------------------------------------------------------|
| [**Administrator: Beschreibung**](a-admindescription.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Administrator-Anzeige Name**](a-admindisplayname.md)                                        | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Zulässige Attribute**](a-allowedattributes.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Zulässige Attribute-gültig**](a-allowedattributeseffective.md)                    | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Zulässige, untergeordnete Klassen**](a-allowedchildclasses.md)                                  | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Zulässig-untergeordnete Klassen-gültig**](a-allowedchildclasseseffective.md)               | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                           | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Kanonischer Name**](a-canonicalname.md)                                               | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Gemeinsamer Name**](a-cn.md)                                                             | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Create-Zeitstempel**](a-createtimestamp.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Beschreibung**](a-description.md)                                                    | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Anzeige Name**](a-displayname.md)                                                   | False     | **PKI-Zertifikat-Vorlage** [ **oben**](c-top.md)<br/> |
| [**Anzeige Name-druckdruck**](a-displaynameprintable.md)                                | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**DSA-Signatur**](a-dsasignature.md)                                                 | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**DS-Core-propagierungs Daten**](a-dscorepropagationdata.md)                             | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Erweiterungs Name**](a-extensionname.md)                                               | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Fahren**](a-flags.md)                                                                | False     | **PKI-Zertifikat-Vorlage** [ **oben**](c-top.md)<br/> |
| [**Aus-Eintrag**](a-fromentry.md)                                                       | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                           | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                               | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**"F"-Rollen Besitzer**](a-fsmoroleowner.md)                                              | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Instanztyp**](a-instancetype.md)                                                 | Richtig      | [**Nach oben**](c-top.md)<br/>                              |
| [**Is-critical-System-Object**](a-iscriticalsystemobject.md)                           | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Ist-gelöscht**](a-isdeleted.md)                                                       | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Is-Member-of-DL**](a-memberof.md)                                                   | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Is-Privilege-Inhaber**](a-isprivilegeholder.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Letztes-bekannt/übergeordnetes Element**](a-lastknownparent.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Verwaltete Objekte**](a-managedobjects.md)                                             | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Verwaltet von**](a-masteredby.md)                                                     | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Modify-Zeitstempel**](a-modifytimestamp.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**MS-com-partitionsetlink**](a-mscom-partitionsetlink.md)                             | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**MS-com-userlink**](a-mscom-userlink.md)                                             | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**MS-DFSR-computerreferencebl**](a-msdfsr-computerreferencebl.md)                     | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**MS-DFSR-mitgliedreferencebl**](a-msdfsr-memberreferencebl.md)                         | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-ca-immed-untergeordnete Elemente**](a-msds-approx-immed-subordinates.md)             | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-authentieredto-accountlist**](a-msds-authenticatedtoaccountlist.md)          | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**MS-DS-Konsistenz-untergeordnet-Anzahl**](a-ms-ds-consistencychildcount.md)                  | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                               | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-is-Domain-for**](a-msds-isdomainfor.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-is-full-Replica-for**](a-msds-isfullreplicafor.md)                            | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-is-Partial-Replica-for**](a-msds-ispartialreplicafor.md)                      | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-krbtgt-Link-BL**](a-msds-krbtgtlinkbl.md)                                     | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-gemastert von**](a-msds-masteredby.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Members-für-AZ-Role-BL**](a-msds-membersforazrolebl.md)                       | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-NC-repl-Cursor**](a-msds-ncreplcursors.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-NC-repl-Inbound-Nachbarn**](a-msds-ncreplinboundneighbors.md)                | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-NC-repl-Outbound-Nachbarn**](a-msds-ncreploutboundneighbors.md)              | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)           | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-NC-Typ**](a-msds-nctype.md)                                                  | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                                     | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                           | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)                 | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)                 | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                                    | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-PSO-angewendet**](a-msds-psoapplied.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)                  | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                          | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-offengelegt-DSAs**](a-msds-revealeddsas.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-enthüllt-List-BL**](a-msds-revealedlistbl.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Tasks-für-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                           | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Tasks-für-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                           | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                                   | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**MS-PKI-Certificate-Application-Policy**](a-mspki-certificate-application-policy.md) | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**MS-PKI-Certificate-Name-Flag**](a-mspki-certificate-name-flag.md)                   | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**MS-PKI-Certificate-Policy**](a-mspki-certificate-policy.md)                         | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**MS-PKI-CERT-Template-OID**](a-mspki-cert-template-oid.md)                           | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**MS-PKI-Registrierungsflag**](a-mspki-enrollment-flag.md)                               | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**MS-PKI-minimale Schlüsselgröße**](a-mspki-minimal-key-size.md)                             | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**MS-PKI-Private-Key-Flag**](a-mspki-private-key-flag.md)                             | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**MS-PKI-RA-Application-Policies**](a-mspki-ra-application-policies.md)               | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**MS-PKI-RA-Richtlinien**](a-mspki-ra-policies.md)                                       | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**MS-PKI-RA-Signature**](a-mspki-ra-signature.md)                                     | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**MS-PKI-abgelöst-Vorlagen**](a-mspki-supersede-templates.md)                       | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**MS-PKI-Template-Minor-Revision**](a-mspki-template-minor-revision.md)               | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**MS-PKI-Template-Schema-Version**](a-mspki-template-schema-version.md)               | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**msSFU-30-POSIX-Member-of**](a-mssfu30posixmemberof.md)                              | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**NetBoot-SCP-BL**](a-netbootscpbl.md)                                                | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Nicht sicherheitsmitglied-BL**](a-nonsecuritymemberbl.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                                | Richtig      | [**Nach oben**](c-top.md)<br/>                              |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Objekt-Kategorie**](a-objectcategory.md)                                             | Richtig      | [**Nach oben**](c-top.md)<br/>                              |
| [**Object-Klasse**](a-objectclass.md)                                                   | Richtig      | [**Nach oben**](c-top.md)<br/>                              |
| [**Objekt-GUID**](a-objectguid.md)                                                     | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Objekt-Version**](a-objectversion.md)                                               | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Andere-bekannte Objekte**](a-otherwellknownobjects.md)                             | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Partial-Attribute-löschen-List**](a-partialattributedeletionlist.md)               | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Partiell-Attribut Satz**](a-partialattributeset.md)                                  | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**PKI-Critical-Extensions**](a-pkicriticalextensions.md)                              | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**PKI-default-CSPs**](a-pkidefaultcsps.md)                                            | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**PKI-default-Key-spec**](a-pkidefaultkeyspec.md)                                     | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**PKI-Registrierung-Zugriff**](a-pkienrollmentaccess.md)                                  | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**PKI-Ablauf Zeitraum**](a-pkiexpirationperiod.md)                                  | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**PKI-erweiterte Schlüssel Verwendung**](a-pkiextendedkeyusage.md)                                 | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**PKI-Schlüssel-Verwendung**](a-pkikeyusage.md)                                                  | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**PKI-Max-ausstellende Tiefe**](a-pkimaxissuingdepth.md)                                   | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**PKI-Überlappung-Zeitraum**](a-pkioverlapperiod.md)                                        | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**Mögliche-minderwertig**](a-possibleinferiors.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Proxy-Objekt Name**](a-proxiedobjectname.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Proxy Adressen**](a-proxyaddresses.md)                                             | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Abfrage-Richtlinie-BL**](a-querypolicybl.md)                                              | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**RDN**](a-name.md)                                                                   | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                               | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**REPL-Update-Vector**](a-repluptodatevector.md)                                    | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Berichte**](a-directreports.md)                                                      | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Reps-from**](a-repsfrom.md)                                                         | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Reps-to**](a-repsto.md)                                                             | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Novel**](a-revision.md)                                                          | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**SD-Rechte**](a-sdrightseffective.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Server-Reference-BL**](a-serverreferencebl.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Anzeigen-in-Advanced-nur anzeigen**](a-showinadvancedviewonly.md)                          | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Site-Object-BL**](a-siteobjectbl.md)                                                | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Struktur-Objekt-Klasse**](a-structuralobjectclass.md)                              | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Sub-Refs**](a-subrefs.md)                                                           | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Subschemasubentry**](a-subschemasubentry.md)                                        | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**SystemFlags**](a-systemflags.md)                                                   | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Die Anwendung wurde geändert.**](a-usnchanged.md)                                                     | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Von der Anwendung erstellte**](a-usncreated.md)                                                     | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**USA-DSA-letzte-obj-entfernt**](a-usndsalastobjremoved.md)                              | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Standort-und standortübergreifende standortübergreifende**](a-usnintersite.md)                                                 | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**"An-Last-obj-REM"**](a-usnlastobjrem.md)                                             | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Quell Code Quelle**](a-usnsource.md)                                                       | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**WBEM-Pfad**](a-wbempath.md)                                                         | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Bekannte Objekte**](a-wellknownobjects.md)                                        | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Bei Änderung**](a-whenchanged.md)                                                   | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Bei Erstellung**](a-whencreated.md)                                                   | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**WWW-Homepage**](a-wwwhomepage.md)                                                  | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**WWW-Page-other**](a-url.md)                                                         | False     | [**Nach oben**](c-top.md)<br/>                              |



## <a name="windows-server-2008-extended-rights"></a>Erweiterte Rechte für Windows Server 2008

Diese Klasse enthält die folgenden erweiterten Rechte für Windows Server 2008:



| Allgemeiner Name                                                |
|------------------------------------------------------------|
| [**Zertifikat-Registrierung**](r-certificate-enrollment.md) |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2

-   [Attribute](#windows-server-2008-r2-attributes)
-   [Erweiterte Rechte](#windows-server-2008-r2-extended-rights)



| Eingabe | Wert |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | False                                                                                        |
| Object-Category             | 1                                                                                            |
| Default-Object-Category     | \-                                                                                           |
| Governs-Id                  | 1.2.840.113556.1.5.177                                                                       |
| Standard-ausblenden-Wert        | 1                                                                                            |
| RDN-ATT-ID                  | [**Gemeinsamer Name**](a-cn.md)<br/>                                                       |
| Unterklasse von                 | [**Nach oben**](c-top.md)<br/>                                                              |
| Mögliche Vorgesetzten          | [**Container**](c-container.md)                                                             |
| Zusätzlich           | \-                                                                                           |
| NT-Security-Descriptor      | o:Bag: schlecht: S:                                                                                 |
| Standard Sicherheits Beschreibung | D: (A;; rpwpcrccdclclorcwowdsddtsw;;;D a) (a;; Rpwpcrccdclclorcwowdsddtsw;;; SY) (A;; Rplclorc;;; Thaus |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2008-r2-attributes"></a>Windows Server 2008 R2-Attribute

Diese Klasse enthält die folgenden Attribute für Windows Server 2008 R2:



| Attribut                                                                               | Obligatorisch. | Abgeleitet von                                                 |
|-----------------------------------------------------------------------------------------|-----------|--------------------------------------------------------------|
| [**Administrator: Beschreibung**](a-admindescription.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Administrator-Anzeige Name**](a-admindisplayname.md)                                        | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Zulässige Attribute**](a-allowedattributes.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Zulässige Attribute-gültig**](a-allowedattributeseffective.md)                    | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Zulässige, untergeordnete Klassen**](a-allowedchildclasses.md)                                  | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Zulässig-untergeordnete Klassen-gültig**](a-allowedchildclasseseffective.md)               | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                           | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Kanonischer Name**](a-canonicalname.md)                                               | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Gemeinsamer Name**](a-cn.md)                                                             | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Create-Zeitstempel**](a-createtimestamp.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Beschreibung**](a-description.md)                                                    | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Anzeige Name**](a-displayname.md)                                                   | False     | **PKI-Zertifikat-Vorlage** [ **oben**](c-top.md)<br/> |
| [**Anzeige Name-druckdruck**](a-displaynameprintable.md)                                | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**DSA-Signatur**](a-dsasignature.md)                                                 | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**DS-Core-propagierungs Daten**](a-dscorepropagationdata.md)                             | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Erweiterungs Name**](a-extensionname.md)                                               | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Fahren**](a-flags.md)                                                                | False     | **PKI-Zertifikat-Vorlage** [ **oben**](c-top.md)<br/> |
| [**Aus-Eintrag**](a-fromentry.md)                                                       | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                           | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                               | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**"F"-Rollen Besitzer**](a-fsmoroleowner.md)                                              | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Instanztyp**](a-instancetype.md)                                                 | Richtig      | [**Nach oben**](c-top.md)<br/>                              |
| [**Is-critical-System-Object**](a-iscriticalsystemobject.md)                           | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Ist-gelöscht**](a-isdeleted.md)                                                       | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Is-Member-of-DL**](a-memberof.md)                                                   | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Is-Privilege-Inhaber**](a-isprivilegeholder.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Ist-recycelt**](a-isrecycled.md)                                                     | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Letztes-bekannt/übergeordnetes Element**](a-lastknownparent.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Verwaltete Objekte**](a-managedobjects.md)                                             | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Verwaltet von**](a-masteredby.md)                                                     | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Modify-Zeitstempel**](a-modifytimestamp.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**MS-com-partitionsetlink**](a-mscom-partitionsetlink.md)                             | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**MS-com-userlink**](a-mscom-userlink.md)                                             | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**MS-DFSR-computerreferencebl**](a-msdfsr-computerreferencebl.md)                     | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**MS-DFSR-mitgliedreferencebl**](a-msdfsr-memberreferencebl.md)                         | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-ca-immed-untergeordnete Elemente**](a-msds-approx-immed-subordinates.md)             | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-authentieredto-accountlist**](a-msds-authenticatedtoaccountlist.md)          | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**MS-DS-Konsistenz-untergeordnet-Anzahl**](a-ms-ds-consistencychildcount.md)                  | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                               | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-aktiviert-Feature-BL**](a-msds-enabledfeaturebl.md)                             | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)                    | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-is-Domain-for**](a-msds-isdomainfor.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-is-full-Replica-for**](a-msds-isfullreplicafor.md)                            | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-is-Partial-Replica-for**](a-msds-ispartialreplicafor.md)                      | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-krbtgt-Link-BL**](a-msds-krbtgtlinkbl.md)                                     | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                                     | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-local-Effective-Lösch Zeit**](a-msds-localeffectivedeletiontime.md)        | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-local-Effective-Papier-Time**](a-msds-localeffectiverecycletime.md)          | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-gemastert von**](a-msds-masteredby.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Members-für-AZ-Role-BL**](a-msds-membersforazrolebl.md)                       | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-NC-repl-Cursor**](a-msds-ncreplcursors.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-NC-repl-Inbound-Nachbarn**](a-msds-ncreplinboundneighbors.md)                | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-NC-repl-Outbound-Nachbarn**](a-msds-ncreploutboundneighbors.md)              | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)           | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-NC-Typ**](a-msds-nctype.md)                                                  | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                                     | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                           | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-oidtoidgruppe-Link-BL**](a-msds-oidtogrouplinkbl.md)                             | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)                 | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)                 | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                                    | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-PSO-angewendet**](a-msds-psoapplied.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)                  | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                          | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-offengelegt-DSAs**](a-msds-revealeddsas.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-enthüllt-List-BL**](a-msds-revealedlistbl.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Tasks-für-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                           | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Tasks-für-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                           | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                                   | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**MS-PKI-Certificate-Application-Policy**](a-mspki-certificate-application-policy.md) | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**MS-PKI-Certificate-Name-Flag**](a-mspki-certificate-name-flag.md)                   | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**MS-PKI-Certificate-Policy**](a-mspki-certificate-policy.md)                         | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**MS-PKI-CERT-Template-OID**](a-mspki-cert-template-oid.md)                           | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**MS-PKI-Registrierungsflag**](a-mspki-enrollment-flag.md)                               | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**MS-PKI-minimale Schlüsselgröße**](a-mspki-minimal-key-size.md)                             | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**MS-PKI-Private-Key-Flag**](a-mspki-private-key-flag.md)                             | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**MS-PKI-RA-Application-Policies**](a-mspki-ra-application-policies.md)               | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**MS-PKI-RA-Richtlinien**](a-mspki-ra-policies.md)                                       | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**MS-PKI-RA-Signature**](a-mspki-ra-signature.md)                                     | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**MS-PKI-abgelöst-Vorlagen**](a-mspki-supersede-templates.md)                       | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**MS-PKI-Template-Minor-Revision**](a-mspki-template-minor-revision.md)               | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**MS-PKI-Template-Schema-Version**](a-mspki-template-schema-version.md)               | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**msSFU-30-POSIX-Member-of**](a-mssfu30posixmemberof.md)                              | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**NetBoot-SCP-BL**](a-netbootscpbl.md)                                                | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Nicht sicherheitsmitglied-BL**](a-nonsecuritymemberbl.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                                | Richtig      | [**Nach oben**](c-top.md)<br/>                              |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Objekt-Kategorie**](a-objectcategory.md)                                             | Richtig      | [**Nach oben**](c-top.md)<br/>                              |
| [**Object-Klasse**](a-objectclass.md)                                                   | Richtig      | [**Nach oben**](c-top.md)<br/>                              |
| [**Objekt-GUID**](a-objectguid.md)                                                     | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Objekt-Version**](a-objectversion.md)                                               | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Andere-bekannte Objekte**](a-otherwellknownobjects.md)                             | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Partial-Attribute-löschen-List**](a-partialattributedeletionlist.md)               | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Partiell-Attribut Satz**](a-partialattributeset.md)                                  | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**PKI-Critical-Extensions**](a-pkicriticalextensions.md)                              | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**PKI-default-CSPs**](a-pkidefaultcsps.md)                                            | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**PKI-default-Key-spec**](a-pkidefaultkeyspec.md)                                     | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**PKI-Registrierung-Zugriff**](a-pkienrollmentaccess.md)                                  | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**PKI-Ablauf Zeitraum**](a-pkiexpirationperiod.md)                                  | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**PKI-erweiterte Schlüssel Verwendung**](a-pkiextendedkeyusage.md)                                 | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**PKI-Schlüssel-Verwendung**](a-pkikeyusage.md)                                                  | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**PKI-Max-ausstellende Tiefe**](a-pkimaxissuingdepth.md)                                   | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**PKI-Überlappung-Zeitraum**](a-pkioverlapperiod.md)                                        | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**Mögliche-minderwertig**](a-possibleinferiors.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Proxy-Objekt Name**](a-proxiedobjectname.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Proxy Adressen**](a-proxyaddresses.md)                                             | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Abfrage-Richtlinie-BL**](a-querypolicybl.md)                                              | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**RDN**](a-name.md)                                                                   | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                               | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**REPL-Update-Vector**](a-repluptodatevector.md)                                    | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Berichte**](a-directreports.md)                                                      | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Reps-from**](a-repsfrom.md)                                                         | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Reps-to**](a-repsto.md)                                                             | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Novel**](a-revision.md)                                                          | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**SD-Rechte**](a-sdrightseffective.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Server-Reference-BL**](a-serverreferencebl.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Anzeigen-in-Advanced-nur anzeigen**](a-showinadvancedviewonly.md)                          | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Site-Object-BL**](a-siteobjectbl.md)                                                | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Struktur-Objekt-Klasse**](a-structuralobjectclass.md)                              | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Sub-Refs**](a-subrefs.md)                                                           | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Subschemasubentry**](a-subschemasubentry.md)                                        | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**SystemFlags**](a-systemflags.md)                                                   | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Die Anwendung wurde geändert.**](a-usnchanged.md)                                                     | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Von der Anwendung erstellte**](a-usncreated.md)                                                     | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**USA-DSA-letzte-obj-entfernt**](a-usndsalastobjremoved.md)                              | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Standort-und standortübergreifende standortübergreifende**](a-usnintersite.md)                                                 | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**"An-Last-obj-REM"**](a-usnlastobjrem.md)                                             | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Quell Code Quelle**](a-usnsource.md)                                                       | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**WBEM-Pfad**](a-wbempath.md)                                                         | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Bekannte Objekte**](a-wellknownobjects.md)                                        | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Bei Änderung**](a-whenchanged.md)                                                   | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Bei Erstellung**](a-whencreated.md)                                                   | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**WWW-Homepage**](a-wwwhomepage.md)                                                  | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**WWW-Page-other**](a-url.md)                                                         | False     | [**Nach oben**](c-top.md)<br/>                              |



## <a name="windows-server-2008-r2-extended-rights"></a>Erweiterte Rechte für Windows Server 2008 R2

Diese Klasse enthält die folgenden erweiterten Rechte für Windows Server 2008 R2:



| Allgemeiner Name                                                |
|------------------------------------------------------------|
| [**Zertifikat-Registrierung**](r-certificate-enrollment.md) |



## <a name="windows-server-2012"></a>Windows Server 2012

-   [Attribute](#windows-server-2012-attributes)
-   [Erweiterte Rechte](#windows-server-2012-extended-rights)



| Eingabe | Wert |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | False                                                                                        |
| Object-Category             | 1                                                                                            |
| Default-Object-Category     | \-                                                                                           |
| Governs-Id                  | 1.2.840.113556.1.5.177                                                                       |
| Standard-ausblenden-Wert        | 1                                                                                            |
| RDN-ATT-ID                  | [**Gemeinsamer Name**](a-cn.md)<br/>                                                       |
| Unterklasse von                 | [**Nach oben**](c-top.md)<br/>                                                              |
| Mögliche Vorgesetzten          | [**Container**](c-container.md)                                                             |
| Zusätzlich           | \-                                                                                           |
| NT-Security-Descriptor      | o:Bag: schlecht: S:                                                                                 |
| Standard Sicherheits Beschreibung | D: (A;; rpwpcrccdclclorcwowdsddtsw;;;D a) (a;; Rpwpcrccdclclorcwowdsddtsw;;; SY) (A;; Rplclorc;;; Thaus |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2012-attributes"></a>Windows Server 2012-Attribute

Diese Klasse enthält die folgenden Attribute für Windows Server 2012:



| Attribut                                                                                    | Obligatorisch. | Abgeleitet von                                                 |
|----------------------------------------------------------------------------------------------|-----------|--------------------------------------------------------------|
| [**Administrator: Beschreibung**](a-admindescription.md)                                              | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Administrator-Anzeige Name**](a-admindisplayname.md)                                             | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Zulässige Attribute**](a-allowedattributes.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Zulässige Attribute-gültig**](a-allowedattributeseffective.md)                         | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Zulässige, untergeordnete Klassen**](a-allowedchildclasses.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Zulässig-untergeordnete Klassen-gültig**](a-allowedchildclasseseffective.md)                    | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                                | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Kanonischer Name**](a-canonicalname.md)                                                    | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Gemeinsamer Name**](a-cn.md)                                                                  | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Create-Zeitstempel**](a-createtimestamp.md)                                               | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Beschreibung**](a-description.md)                                                         | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Anzeige Name**](a-displayname.md)                                                        | False     | **PKI-Zertifikat-Vorlage** [ **oben**](c-top.md)<br/> |
| [**Anzeige Name-druckdruck**](a-displaynameprintable.md)                                     | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**DSA-Signatur**](a-dsasignature.md)                                                      | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**DS-Core-propagierungs Daten**](a-dscorepropagationdata.md)                                  | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Erweiterungs Name**](a-extensionname.md)                                                    | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Fahren**](a-flags.md)                                                                     | False     | **PKI-Zertifikat-Vorlage** [ **oben**](c-top.md)<br/> |
| [**Aus-Eintrag**](a-fromentry.md)                                                            | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                                | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                                    | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**"F"-Rollen Besitzer**](a-fsmoroleowner.md)                                                   | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Instanztyp**](a-instancetype.md)                                                      | Richtig      | [**Nach oben**](c-top.md)<br/>                              |
| [**Is-critical-System-Object**](a-iscriticalsystemobject.md)                                | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Ist-gelöscht**](a-isdeleted.md)                                                            | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Is-Member-of-DL**](a-memberof.md)                                                        | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Is-Privilege-Inhaber**](a-isprivilegeholder.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Ist-recycelt**](a-isrecycled.md)                                                          | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Letztes-bekannt/übergeordnetes Element**](a-lastknownparent.md)                                               | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Verwaltete Objekte**](a-managedobjects.md)                                                  | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Verwaltet von**](a-masteredby.md)                                                          | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Modify-Zeitstempel**](a-modifytimestamp.md)                                               | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**MS-com-partitionsetlink**](a-mscom-partitionsetlink.md)                                  | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**MS-com-userlink**](a-mscom-userlink.md)                                                  | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**MS-DFSR-computerreferencebl**](a-msdfsr-computerreferencebl.md)                          | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**MS-DFSR-mitgliedreferencebl**](a-msdfsr-memberreferencebl.md)                              | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-ca-immed-untergeordnete Elemente**](a-msds-approx-immed-subordinates.md)                  | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-authentieredto-accountlist**](a-msds-authenticatedtoaccountlist.md)               | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Claim-Shares-mögliche-values-with-BL**](a-msds-claimsharespossiblevalueswithbl.md) | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**MS-DS-Konsistenz-untergeordnet-Anzahl**](a-ms-ds-consistencychildcount.md)                       | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                                    | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-aktiviert-Feature-BL**](a-msds-enabledfeaturebl.md)                                  | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)                         | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-is-Domain-for**](a-msds-isdomainfor.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-is-full-Replica-for**](a-msds-isfullreplicafor.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-is-Partial-Replica-for**](a-msds-ispartialreplicafor.md)                           | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-is-Primary-Computer-für**](a-msds-isprimarycomputerfor.md)                         | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-krbtgt-Link-BL**](a-msds-krbtgtlinkbl.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-local-Effective-Lösch Zeit**](a-msds-localeffectivedeletiontime.md)             | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-local-Effective-Papier-Time**](a-msds-localeffectiverecycletime.md)               | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-gemastert von**](a-msds-masteredby.md)                                               | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Members-für-AZ-Role-BL**](a-msds-membersforazrolebl.md)                            | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Members-of-Resource-Property-List-BL**](a-msds-membersofresourcepropertylistbl.md) | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-NC-repl-Cursor**](a-msds-ncreplcursors.md)                                        | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-NC-repl-Inbound-Nachbarn**](a-msds-ncreplinboundneighbors.md)                     | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-NC-repl-Outbound-Nachbarn**](a-msds-ncreploutboundneighbors.md)                   | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)                | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-NC-Typ**](a-msds-nctype.md)                                                       | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                                | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-oidtoidgruppe-Link-BL**](a-msds-oidtogrouplinkbl.md)                                  | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)                      | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)                      | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-PSO-angewendet**](a-msds-psoapplied.md)                                               | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)                       | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                               | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-offengelegt-DSAs**](a-msds-revealeddsas.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-enthüllt-List-BL**](a-msds-revealedlistbl.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Tasks-für-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                                | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Tasks-für-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                                | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-TDO-Egress-BL**](a-msds-tdoegressbl.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-TDO-Ingress-BL**](a-msds-tdoingressbl.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-DS-Value-Type-Reference-BL**](a-msds-valuetypereferencebl.md)                         | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                                        | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**MS-PKI-Certificate-Application-Policy**](a-mspki-certificate-application-policy.md)      | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**MS-PKI-Certificate-Name-Flag**](a-mspki-certificate-name-flag.md)                        | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**MS-PKI-Certificate-Policy**](a-mspki-certificate-policy.md)                              | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**MS-PKI-CERT-Template-OID**](a-mspki-cert-template-oid.md)                                | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**MS-PKI-Registrierungsflag**](a-mspki-enrollment-flag.md)                                    | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**MS-PKI-minimale Schlüsselgröße**](a-mspki-minimal-key-size.md)                                  | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**MS-PKI-Private-Key-Flag**](a-mspki-private-key-flag.md)                                  | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**MS-PKI-RA-Application-Policies**](a-mspki-ra-application-policies.md)                    | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**MS-PKI-RA-Richtlinien**](a-mspki-ra-policies.md)                                            | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**MS-PKI-RA-Signature**](a-mspki-ra-signature.md)                                          | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**MS-PKI-abgelöst-Vorlagen**](a-mspki-supersede-templates.md)                            | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**MS-PKI-Template-Minor-Revision**](a-mspki-template-minor-revision.md)                    | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**MS-PKI-Template-Schema-Version**](a-mspki-template-schema-version.md)                    | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**msSFU-30-POSIX-Member-of**](a-mssfu30posixmemberof.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**NetBoot-SCP-BL**](a-netbootscpbl.md)                                                     | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Nicht sicherheitsmitglied-BL**](a-nonsecuritymemberbl.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                                     | Richtig      | [**Nach oben**](c-top.md)<br/>                              |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                                 | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Objekt-Kategorie**](a-objectcategory.md)                                                  | Richtig      | [**Nach oben**](c-top.md)<br/>                              |
| [**Object-Klasse**](a-objectclass.md)                                                        | Richtig      | [**Nach oben**](c-top.md)<br/>                              |
| [**Objekt-GUID**](a-objectguid.md)                                                          | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Objekt-Version**](a-objectversion.md)                                                    | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Andere-bekannte Objekte**](a-otherwellknownobjects.md)                                  | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Partial-Attribute-löschen-List**](a-partialattributedeletionlist.md)                    | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Partiell-Attribut Satz**](a-partialattributeset.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**PKI-Critical-Extensions**](a-pkicriticalextensions.md)                                   | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**PKI-default-CSPs**](a-pkidefaultcsps.md)                                                 | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**PKI-default-Key-spec**](a-pkidefaultkeyspec.md)                                          | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**PKI-Registrierung-Zugriff**](a-pkienrollmentaccess.md)                                       | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**PKI-Ablauf Zeitraum**](a-pkiexpirationperiod.md)                                       | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**PKI-erweiterte Schlüssel Verwendung**](a-pkiextendedkeyusage.md)                                      | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**PKI-Schlüssel-Verwendung**](a-pkikeyusage.md)                                                       | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**PKI-Max-ausstellende Tiefe**](a-pkimaxissuingdepth.md)                                        | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**PKI-Überlappung-Zeitraum**](a-pkioverlapperiod.md)                                             | False     | **PKI-Zertifikat-Vorlage**                                 |
| [**Mögliche-minderwertig**](a-possibleinferiors.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Proxy-Objekt Name**](a-proxiedobjectname.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Proxy Adressen**](a-proxyaddresses.md)                                                  | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Abfrage-Richtlinie-BL**](a-querypolicybl.md)                                                   | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**RDN**](a-name.md)                                                                        | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                                    | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**REPL-Update-Vector**](a-repluptodatevector.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Berichte**](a-directreports.md)                                                           | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Reps-from**](a-repsfrom.md)                                                              | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Reps-to**](a-repsto.md)                                                                  | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Novel**](a-revision.md)                                                               | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**SD-Rechte**](a-sdrightseffective.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Server-Reference-BL**](a-serverreferencebl.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Anzeigen-in-Advanced-nur anzeigen**](a-showinadvancedviewonly.md)                               | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Site-Object-BL**](a-siteobjectbl.md)                                                     | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Struktur-Objekt-Klasse**](a-structuralobjectclass.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Sub-Refs**](a-subrefs.md)                                                                | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Subschemasubentry**](a-subschemasubentry.md)                                             | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**SystemFlags**](a-systemflags.md)                                                        | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Die Anwendung wurde geändert.**](a-usnchanged.md)                                                          | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Von der Anwendung erstellte**](a-usncreated.md)                                                          | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**USA-DSA-letzte-obj-entfernt**](a-usndsalastobjremoved.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Standort-und standortübergreifende standortübergreifende**](a-usnintersite.md)                                                      | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**"An-Last-obj-REM"**](a-usnlastobjrem.md)                                                  | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Quell Code Quelle**](a-usnsource.md)                                                            | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**WBEM-Pfad**](a-wbempath.md)                                                              | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Bekannte Objekte**](a-wellknownobjects.md)                                             | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Bei Änderung**](a-whenchanged.md)                                                        | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**Bei Erstellung**](a-whencreated.md)                                                        | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**WWW-Homepage**](a-wwwhomepage.md)                                                       | False     | [**Nach oben**](c-top.md)<br/>                              |
| [**WWW-Page-other**](a-url.md)                                                              | False     | [**Nach oben**](c-top.md)<br/>                              |



## <a name="windows-server-2012-extended-rights"></a>Erweiterte Rechte für Windows Server 2012

Diese Klasse enthält die folgenden erweiterten Rechte für Windows Server 2012:



| Allgemeiner Name                                                |
|------------------------------------------------------------|
| [**Zertifikat-Registrierung**](r-certificate-enrollment.md) |



 

 





