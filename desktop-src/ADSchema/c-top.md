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
ms.openlocfilehash: 01cd6a72dfba6a80687081d503864c88fd1c5122
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104106731"
---
# <a name="top-class"></a>Top-Klasse

Die Klasse der obersten Ebene, von der alle Klassen abgeleitet werden.



| Eingabe | Wert |
|-------------------|--------------------------------------|
| CN                | Oben                                  |
| LDAP-Display-Name | top                                  |
| Berechtigung aktualisieren  | Schema Administrator                 |
| Aktualisierungshäufigkeit  | \-                                   |
| Schema-ID-GUID    | bf967ab7-0de6-11d0-a285-00aa003049e2 |



## <a name="implementations"></a>Implementierungen

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Adam**](#adam-attributes)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server

-   [Attribute](#windows-2000-server-attributes)



| Eingabe | Wert |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Richtig                                                                                         |
| Object-Category             | 2                                                                                            |
| Default-Object-Category     | \-                                                                                           |
| Governs-Id                  | 2.5.6.0                                                                                      |
| Standard-ausblenden-Wert        | 1                                                                                            |
| RDN-ATT-ID                  | [**Gemeinsamer Name**](a-cn.md)<br/>                                                       |
| Unterklasse von                 | **Top**<br/>                                                                           |
| Mögliche Vorgesetzten          | [**Verloren und gefunden**](c-lostandfound.md)                                                     |
| Zusätzlich           | \-                                                                                           |
| NT-Security-Descriptor      | o:Bag: schlecht: S:                                                                                 |
| Standard Sicherheits Beschreibung | D: (A;; rpwpcrccdclclorcwowdsddtsw;;;D a) (a;; Rpwpcrccdclclorcwowdsddtsw;;; SY) (A;; Rplclorc;;; Thaus |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-2000-server-attributes"></a>Windows 2000-Server Attribute

Diese Klasse enthält die folgenden Attribute für Windows 2000 Server:



| Attribut                                                                 | Obligatorisch. | Abgeleitet von |
|---------------------------------------------------------------------------|-----------|--------------|
| [**Administrator: Beschreibung**](a-admindescription.md)                           | False     | **Top**      |
| [**Administrator-Anzeige Name**](a-admindisplayname.md)                          | False     | **Top**      |
| [**Zulässige Attribute**](a-allowedattributes.md)                         | False     | **Top**      |
| [**Zulässige Attribute-gültig**](a-allowedattributeseffective.md)      | False     | **Top**      |
| [**Zulässige, untergeordnete Klassen**](a-allowedchildclasses.md)                    | False     | **Top**      |
| [**Zulässig-untergeordnete Klassen-gültig**](a-allowedchildclasseseffective.md) | False     | **Top**      |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)             | False     | **Top**      |
| [**Kanonischer Name**](a-canonicalname.md)                                 | False     | **Top**      |
| [**Gemeinsamer Name**](a-cn.md)                                               | False     | **Top**      |
| [**Create-Zeitstempel**](a-createtimestamp.md)                            | False     | **Top**      |
| [**Beschreibung**](a-description.md)                                      | False     | **Top**      |
| [**Anzeige Name**](a-displayname.md)                                     | False     | **Top**      |
| [**Anzeige Name-druckdruck**](a-displaynameprintable.md)                  | False     | **Top**      |
| [**DSA-Signatur**](a-dsasignature.md)                                   | False     | **Top**      |
| [**DS-Core-propagierungs Daten**](a-dscorepropagationdata.md)               | False     | **Top**      |
| [**Erweiterungs Name**](a-extensionname.md)                                 | False     | **Top**      |
| [**Fahren**](a-flags.md)                                                  | False     | **Top**      |
| [**Aus-Eintrag**](a-fromentry.md)                                         | False     | **Top**      |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)             | False     | **Top**      |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                 | False     | **Top**      |
| [**"F"-Rollen Besitzer**](a-fsmoroleowner.md)                                | False     | **Top**      |
| [**Instanztyp**](a-instancetype.md)                                   | Richtig      | **Top**      |
| [**Is-critical-System-Object**](a-iscriticalsystemobject.md)             | False     | **Top**      |
| [**Ist-gelöscht**](a-isdeleted.md)                                         | False     | **Top**      |
| [**Is-Member-of-DL**](a-memberof.md)                                     | False     | **Top**      |
| [**Is-Privilege-Inhaber**](a-isprivilegeholder.md)                        | False     | **Top**      |
| [**Letztes-bekannt/übergeordnetes Element**](a-lastknownparent.md)                            | False     | **Top**      |
| [**Verwaltete Objekte**](a-managedobjects.md)                               | False     | **Top**      |
| [**Verwaltet von**](a-masteredby.md)                                       | False     | **Top**      |
| [**Modify-Zeitstempel**](a-modifytimestamp.md)                            | False     | **Top**      |
| [**MS-DS-Konsistenz-untergeordnet-Anzahl**](a-ms-ds-consistencychildcount.md)    | False     | **Top**      |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                 | False     | **Top**      |
| [**NetBoot-SCP-BL**](a-netbootscpbl.md)                                  | False     | **Top**      |
| [**Nicht sicherheitsmitglied-BL**](a-nonsecuritymemberbl.md)                   | False     | **Top**      |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                  | Richtig      | **Top**      |
| [**Obj-Dist-Name**](a-distinguishedname.md)                              | False     | **Top**      |
| [**Objekt-Kategorie**](a-objectcategory.md)                               | Richtig      | **Top**      |
| [**Object-Klasse**](a-objectclass.md)                                     | Richtig      | **Top**      |
| [**Objekt-GUID**](a-objectguid.md)                                       | False     | **Top**      |
| [**Objekt-Version**](a-objectversion.md)                                 | False     | **Top**      |
| [**Andere-bekannte Objekte**](a-otherwellknownobjects.md)               | False     | **Top**      |
| [**Partial-Attribute-löschen-List**](a-partialattributedeletionlist.md) | False     | **Top**      |
| [**Partiell-Attribut Satz**](a-partialattributeset.md)                    | False     | **Top**      |
| [**Mögliche-minderwertig**](a-possibleinferiors.md)                         | False     | **Top**      |
| [**Proxy-Objekt Name**](a-proxiedobjectname.md)                        | False     | **Top**      |
| [**Proxy Adressen**](a-proxyaddresses.md)                               | False     | **Top**      |
| [**Abfrage-Richtlinie-BL**](a-querypolicybl.md)                                | False     | **Top**      |
| [**RDN**](a-name.md)                                                     | False     | **Top**      |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                 | False     | **Top**      |
| [**REPL-Update-Vector**](a-repluptodatevector.md)                      | False     | **Top**      |
| [**Berichte**](a-directreports.md)                                        | False     | **Top**      |
| [**Reps-from**](a-repsfrom.md)                                           | False     | **Top**      |
| [**Reps-to**](a-repsto.md)                                               | False     | **Top**      |
| [**Novel**](a-revision.md)                                            | False     | **Top**      |
| [**SD-Rechte**](a-sdrightseffective.md)                        | False     | **Top**      |
| [**Server-Reference-BL**](a-serverreferencebl.md)                        | False     | **Top**      |
| [**Anzeigen-in-Advanced-nur anzeigen**](a-showinadvancedviewonly.md)            | False     | **Top**      |
| [**Site-Object-BL**](a-siteobjectbl.md)                                  | False     | **Top**      |
| [**Sub-Refs**](a-subrefs.md)                                             | False     | **Top**      |
| [**Subschemasubentry**](a-subschemasubentry.md)                          | False     | **Top**      |
| [**SystemFlags**](a-systemflags.md)                                     | False     | **Top**      |
| [**Die Anwendung wurde geändert.**](a-usnchanged.md)                                       | False     | **Top**      |
| [**Von der Anwendung erstellte**](a-usncreated.md)                                       | False     | **Top**      |
| [**USA-DSA-letzte-obj-entfernt**](a-usndsalastobjremoved.md)                | False     | **Top**      |
| [**Standort-und standortübergreifende standortübergreifende**](a-usnintersite.md)                                   | False     | **Top**      |
| [**"An-Last-obj-REM"**](a-usnlastobjrem.md)                               | False     | **Top**      |
| [**Quell Code Quelle**](a-usnsource.md)                                         | False     | **Top**      |
| [**WBEM-Pfad**](a-wbempath.md)                                           | False     | **Top**      |
| [**Bekannte Objekte**](a-wellknownobjects.md)                          | False     | **Top**      |
| [**Bei Änderung**](a-whenchanged.md)                                     | False     | **Top**      |
| [**Bei Erstellung**](a-whencreated.md)                                     | False     | **Top**      |
| [**WWW-Homepage**](a-wwwhomepage.md)                                    | False     | **Top**      |
| [**WWW-Page-other**](a-url.md)                                           | False     | **Top**      |



## <a name="windows-server-2003"></a>Windows Server 2003

-   [Attribute](#windows-server-2003-attributes)



| Eingabe | Wert |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Richtig                                                                                         |
| Object-Category             | 2                                                                                            |
| Default-Object-Category     | \-                                                                                           |
| Governs-Id                  | 2.5.6.0                                                                                      |
| Standard-ausblenden-Wert        | 1                                                                                            |
| RDN-ATT-ID                  | [**Gemeinsamer Name**](a-cn.md)<br/>                                                       |
| Unterklasse von                 | **Top**<br/>                                                                           |
| Mögliche Vorgesetzten          | [**Verloren und gefunden**](c-lostandfound.md)                                                     |
| Zusätzlich           | \-                                                                                           |
| NT-Security-Descriptor      | o:Bag: schlecht: S:                                                                                 |
| Standard Sicherheits Beschreibung | D: (A;; rpwpcrccdclclorcwowdsddtsw;;;D a) (a;; Rpwpcrccdclclorcwowdsddtsw;;; SY) (A;; Rplclorc;;; Thaus |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2003-attributes"></a>Windows Server 2003-Attribute

Diese Klasse enthält die folgenden Attribute für Windows Server 2003:



| Attribut                                                                   | Obligatorisch. | Abgeleitet von |
|-----------------------------------------------------------------------------|-----------|--------------|
| [**Administrator: Beschreibung**](a-admindescription.md)                             | False     | **Top**      |
| [**Administrator-Anzeige Name**](a-admindisplayname.md)                            | False     | **Top**      |
| [**Zulässige Attribute**](a-allowedattributes.md)                           | False     | **Top**      |
| [**Zulässige Attribute-gültig**](a-allowedattributeseffective.md)        | False     | **Top**      |
| [**Zulässige, untergeordnete Klassen**](a-allowedchildclasses.md)                      | False     | **Top**      |
| [**Zulässig-untergeordnete Klassen-gültig**](a-allowedchildclasseseffective.md)   | False     | **Top**      |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)               | False     | **Top**      |
| [**Kanonischer Name**](a-canonicalname.md)                                   | False     | **Top**      |
| [**Gemeinsamer Name**](a-cn.md)                                                 | False     | **Top**      |
| [**Create-Zeitstempel**](a-createtimestamp.md)                              | False     | **Top**      |
| [**Beschreibung**](a-description.md)                                        | False     | **Top**      |
| [**Anzeige Name**](a-displayname.md)                                       | False     | **Top**      |
| [**Anzeige Name-druckdruck**](a-displaynameprintable.md)                    | False     | **Top**      |
| [**DSA-Signatur**](a-dsasignature.md)                                     | False     | **Top**      |
| [**DS-Core-propagierungs Daten**](a-dscorepropagationdata.md)                 | False     | **Top**      |
| [**Erweiterungs Name**](a-extensionname.md)                                   | False     | **Top**      |
| [**Fahren**](a-flags.md)                                                    | False     | **Top**      |
| [**Aus-Eintrag**](a-fromentry.md)                                           | False     | **Top**      |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)               | False     | **Top**      |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                   | False     | **Top**      |
| [**"F"-Rollen Besitzer**](a-fsmoroleowner.md)                                  | False     | **Top**      |
| [**Instanztyp**](a-instancetype.md)                                     | Richtig      | **Top**      |
| [**Is-critical-System-Object**](a-iscriticalsystemobject.md)               | False     | **Top**      |
| [**Ist-gelöscht**](a-isdeleted.md)                                           | False     | **Top**      |
| [**Is-Member-of-DL**](a-memberof.md)                                       | False     | **Top**      |
| [**Is-Privilege-Inhaber**](a-isprivilegeholder.md)                          | False     | **Top**      |
| [**Letztes-bekannt/übergeordnetes Element**](a-lastknownparent.md)                              | False     | **Top**      |
| [**Verwaltete Objekte**](a-managedobjects.md)                                 | False     | **Top**      |
| [**Verwaltet von**](a-masteredby.md)                                         | False     | **Top**      |
| [**Modify-Zeitstempel**](a-modifytimestamp.md)                              | False     | **Top**      |
| [**MS-com-partitionsetlink**](a-mscom-partitionsetlink.md)                 | False     | **Top**      |
| [**MS-com-userlink**](a-mscom-userlink.md)                                 | False     | **Top**      |
| [**ms-DS-ca-immed-untergeordnete Elemente**](a-msds-approx-immed-subordinates.md) | False     | **Top**      |
| [**MS-DS-Konsistenz-untergeordnet-Anzahl**](a-ms-ds-consistencychildcount.md)      | False     | **Top**      |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | False     | **Top**      |
| [**ms-DS-gemastert von**](a-msds-masteredby.md)                              | False     | **Top**      |
| [**ms-DS-Members-für-AZ-Role-BL**](a-msds-membersforazrolebl.md)           | False     | **Top**      |
| [**ms-DS-NC-repl-Cursor**](a-msds-ncreplcursors.md)                       | False     | **Top**      |
| [**ms-DS-NC-repl-Inbound-Nachbarn**](a-msds-ncreplinboundneighbors.md)    | False     | **Top**      |
| [**ms-DS-NC-repl-Outbound-Nachbarn**](a-msds-ncreploutboundneighbors.md)  | False     | **Top**      |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                         | False     | **Top**      |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)               | False     | **Top**      |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)     | False     | **Top**      |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)     | False     | **Top**      |
| [**ms-DS-repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)      | False     | **Top**      |
| [**ms-DS-repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)              | False     | **Top**      |
| [**ms-DS-Tasks-für-AZ-Role-BL**](a-msds-tasksforazrolebl.md)               | False     | **Top**      |
| [**ms-DS-Tasks-für-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)               | False     | **Top**      |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                       | False     | **Top**      |
| [**NetBoot-SCP-BL**](a-netbootscpbl.md)                                    | False     | **Top**      |
| [**Nicht sicherheitsmitglied-BL**](a-nonsecuritymemberbl.md)                     | False     | **Top**      |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                    | Richtig      | **Top**      |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                | False     | **Top**      |
| [**Objekt-Kategorie**](a-objectcategory.md)                                 | Richtig      | **Top**      |
| [**Object-Klasse**](a-objectclass.md)                                       | Richtig      | **Top**      |
| [**Objekt-GUID**](a-objectguid.md)                                         | False     | **Top**      |
| [**Objekt-Version**](a-objectversion.md)                                   | False     | **Top**      |
| [**Andere-bekannte Objekte**](a-otherwellknownobjects.md)                 | False     | **Top**      |
| [**Partial-Attribute-löschen-List**](a-partialattributedeletionlist.md)   | False     | **Top**      |
| [**Partiell-Attribut Satz**](a-partialattributeset.md)                      | False     | **Top**      |
| [**Mögliche-minderwertig**](a-possibleinferiors.md)                           | False     | **Top**      |
| [**Proxy-Objekt Name**](a-proxiedobjectname.md)                          | False     | **Top**      |
| [**Proxy Adressen**](a-proxyaddresses.md)                                 | False     | **Top**      |
| [**Abfrage-Richtlinie-BL**](a-querypolicybl.md)                                  | False     | **Top**      |
| [**RDN**](a-name.md)                                                       | False     | **Top**      |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                   | False     | **Top**      |
| [**REPL-Update-Vector**](a-repluptodatevector.md)                        | False     | **Top**      |
| [**Berichte**](a-directreports.md)                                          | False     | **Top**      |
| [**Reps-from**](a-repsfrom.md)                                             | False     | **Top**      |
| [**Reps-to**](a-repsto.md)                                                 | False     | **Top**      |
| [**Novel**](a-revision.md)                                              | False     | **Top**      |
| [**SD-Rechte**](a-sdrightseffective.md)                          | False     | **Top**      |
| [**Server-Reference-BL**](a-serverreferencebl.md)                          | False     | **Top**      |
| [**Anzeigen-in-Advanced-nur anzeigen**](a-showinadvancedviewonly.md)              | False     | **Top**      |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | False     | **Top**      |
| [**Struktur-Objekt-Klasse**](a-structuralobjectclass.md)                  | False     | **Top**      |
| [**Sub-Refs**](a-subrefs.md)                                               | False     | **Top**      |
| [**Subschemasubentry**](a-subschemasubentry.md)                            | False     | **Top**      |
| [**SystemFlags**](a-systemflags.md)                                       | False     | **Top**      |
| [**Die Anwendung wurde geändert.**](a-usnchanged.md)                                         | False     | **Top**      |
| [**Von der Anwendung erstellte**](a-usncreated.md)                                         | False     | **Top**      |
| [**USA-DSA-letzte-obj-entfernt**](a-usndsalastobjremoved.md)                  | False     | **Top**      |
| [**Standort-und standortübergreifende standortübergreifende**](a-usnintersite.md)                                     | False     | **Top**      |
| [**"An-Last-obj-REM"**](a-usnlastobjrem.md)                                 | False     | **Top**      |
| [**Quell Code Quelle**](a-usnsource.md)                                           | False     | **Top**      |
| [**WBEM-Pfad**](a-wbempath.md)                                             | False     | **Top**      |
| [**Bekannte Objekte**](a-wellknownobjects.md)                            | False     | **Top**      |
| [**Bei Änderung**](a-whenchanged.md)                                       | False     | **Top**      |
| [**Bei Erstellung**](a-whencreated.md)                                       | False     | **Top**      |
| [**WWW-Homepage**](a-wwwhomepage.md)                                      | False     | **Top**      |
| [**WWW-Page-other**](a-url.md)                                             | False     | **Top**      |



## <a name="adam"></a>Adam

-   [Attribute](#adam-attributes)



| Eingabe | Wert |
|-----------------------------|------------------------------------------|
| System-Only                 | Richtig                                     |
| Object-Category             | 2                                        |
| Default-Object-Category     | \-                                       |
| Governs-Id                  | 2.5.6.0                                  |
| Standard-ausblenden-Wert        | 1                                        |
| RDN-ATT-ID                  | [**Gemeinsamer Name**](a-cn.md)<br/>   |
| Unterklasse von                 | **Top**<br/>                       |
| Mögliche Vorgesetzten          | [**Verloren und gefunden**](c-lostandfound.md) |
| Zusätzlich           | \-                                       |
| NT-Security-Descriptor      | o:Bag: schlecht: S:                             |
| Standard Sicherheits Beschreibung | d:s:                                     |
| System-Flags                | 0x00000010                               |



## <a name="adam-attributes"></a>Adam-Attribute

Diese Klasse enthält die folgenden Attribute für Adam:



| Attribut                                                                   | Obligatorisch. | Abgeleitet von |
|-----------------------------------------------------------------------------|-----------|--------------|
| [**Administrator: Beschreibung**](a-admindescription.md)                             | False     | **Top**      |
| [**Administrator-Anzeige Name**](a-admindisplayname.md)                            | False     | **Top**      |
| [**Zulässige Attribute**](a-allowedattributes.md)                           | False     | **Top**      |
| [**Zulässige Attribute-gültig**](a-allowedattributeseffective.md)        | False     | **Top**      |
| [**Zulässige, untergeordnete Klassen**](a-allowedchildclasses.md)                      | False     | **Top**      |
| [**Zulässig-untergeordnete Klassen-gültig**](a-allowedchildclasseseffective.md)   | False     | **Top**      |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)               | False     | **Top**      |
| [**Kanonischer Name**](a-canonicalname.md)                                   | False     | **Top**      |
| [**Gemeinsamer Name**](a-cn.md)                                                 | False     | **Top**      |
| [**Create-Zeitstempel**](a-createtimestamp.md)                              | False     | **Top**      |
| [**Beschreibung**](a-description.md)                                        | False     | **Top**      |
| [**Anzeige Name**](a-displayname.md)                                       | False     | **Top**      |
| [**DSA-Signatur**](a-dsasignature.md)                                     | False     | **Top**      |
| [**DS-Core-propagierungs Daten**](a-dscorepropagationdata.md)                 | False     | **Top**      |
| [**Aus-Eintrag**](a-fromentry.md)                                           | False     | **Top**      |
| [**"F"-Rollen Besitzer**](a-fsmoroleowner.md)                                  | False     | **Top**      |
| [**Instanztyp**](a-instancetype.md)                                     | Richtig      | **Top**      |
| [**Is-critical-System-Object**](a-iscriticalsystemobject.md)               | False     | **Top**      |
| [**Ist-gelöscht**](a-isdeleted.md)                                           | False     | **Top**      |
| [**Is-Member-of-DL**](a-memberof.md)                                       | False     | **Top**      |
| [**Letztes-bekannt/übergeordnetes Element**](a-lastknownparent.md)                              | False     | **Top**      |
| [**Verwaltete Objekte**](a-managedobjects.md)                                 | False     | **Top**      |
| [**Verwaltet von**](a-masteredby.md)                                         | False     | **Top**      |
| [**Modify-Zeitstempel**](a-modifytimestamp.md)                              | False     | **Top**      |
| [**ms-DS-ca-immed-untergeordnete Elemente**](a-msds-approx-immed-subordinates.md) | False     | **Top**      |
| [**MS-DS-Konsistenz-untergeordnet-Anzahl**](a-ms-ds-consistencychildcount.md)      | False     | **Top**      |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | False     | **Top**      |
| [**ms-DS-deaktivieren-für-Instanzen-BL**](a-msds-disableforinstancesbl.md)      | False     | **Top**      |
| [**ms-DS-gemastert von**](a-msds-masteredby.md)                              | False     | **Top**      |
| [**ms-DS-NC-repl-Cursor**](a-msds-ncreplcursors.md)                       | False     | **Top**      |
| [**ms-DS-NC-repl-Inbound-Nachbarn**](a-msds-ncreplinboundneighbors.md)    | False     | **Top**      |
| [**ms-DS-NC-repl-Outbound-Nachbarn**](a-msds-ncreploutboundneighbors.md)  | False     | **Top**      |
| [**ms-DS-repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)      | False     | **Top**      |
| [**ms-DS-repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)              | False     | **Top**      |
| [**ms-DS-Service-Account-BL**](a-msds-serviceaccountbl.md)                 | False     | **Top**      |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                    | Richtig      | **Top**      |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                | False     | **Top**      |
| [**Objekt-Kategorie**](a-objectcategory.md)                                 | Richtig      | **Top**      |
| [**Object-Klasse**](a-objectclass.md)                                       | Richtig      | **Top**      |
| [**Objekt-GUID**](a-objectguid.md)                                         | False     | **Top**      |
| [**Objekt-Version**](a-objectversion.md)                                   | False     | **Top**      |
| [**Andere-bekannte Objekte**](a-otherwellknownobjects.md)                 | False     | **Top**      |
| [**Partial-Attribute-löschen-List**](a-partialattributedeletionlist.md)   | False     | **Top**      |
| [**Partiell-Attribut Satz**](a-partialattributeset.md)                      | False     | **Top**      |
| [**Mögliche-minderwertig**](a-possibleinferiors.md)                           | False     | **Top**      |
| [**Proxy-Objekt Name**](a-proxiedobjectname.md)                          | False     | **Top**      |
| [**Proxy Adressen**](a-proxyaddresses.md)                                 | False     | **Top**      |
| [**Abfrage-Richtlinie-BL**](a-querypolicybl.md)                                  | False     | **Top**      |
| [**RDN**](a-name.md)                                                       | False     | **Top**      |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                   | False     | **Top**      |
| [**REPL-Update-Vector**](a-repluptodatevector.md)                        | False     | **Top**      |
| [**Reps-from**](a-repsfrom.md)                                             | False     | **Top**      |
| [**Reps-to**](a-repsto.md)                                                 | False     | **Top**      |
| [**Novel**](a-revision.md)                                              | False     | **Top**      |
| [**SD-Rechte**](a-sdrightseffective.md)                          | False     | **Top**      |
| [**Server-Reference-BL**](a-serverreferencebl.md)                          | False     | **Top**      |
| [**Anzeigen-in-Advanced-nur anzeigen**](a-showinadvancedviewonly.md)              | False     | **Top**      |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | False     | **Top**      |
| [**Struktur-Objekt-Klasse**](a-structuralobjectclass.md)                  | False     | **Top**      |
| [**Sub-Refs**](a-subrefs.md)                                               | False     | **Top**      |
| [**Subschemasubentry**](a-subschemasubentry.md)                            | False     | **Top**      |
| [**SystemFlags**](a-systemflags.md)                                       | False     | **Top**      |
| [**Die Anwendung wurde geändert.**](a-usnchanged.md)                                         | False     | **Top**      |
| [**Von der Anwendung erstellte**](a-usncreated.md)                                         | False     | **Top**      |
| [**USA-DSA-letzte-obj-entfernt**](a-usndsalastobjremoved.md)                  | False     | **Top**      |
| [**Standort-und standortübergreifende standortübergreifende**](a-usnintersite.md)                                     | False     | **Top**      |
| [**"An-Last-obj-REM"**](a-usnlastobjrem.md)                                 | False     | **Top**      |
| [**Quell Code Quelle**](a-usnsource.md)                                           | False     | **Top**      |
| [**WBEM-Pfad**](a-wbempath.md)                                             | False     | **Top**      |
| [**Bekannte Objekte**](a-wellknownobjects.md)                            | False     | **Top**      |
| [**Bei Änderung**](a-whenchanged.md)                                       | False     | **Top**      |
| [**Bei Erstellung**](a-whencreated.md)                                       | False     | **Top**      |
| [**WWW-Homepage**](a-wwwhomepage.md)                                      | False     | **Top**      |
| [**WWW-Page-other**](a-url.md)                                             | False     | **Top**      |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2

-   [Attribute](#windows-server-2003-r2-attributes)



| Eingabe | Wert |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Richtig                                                                                         |
| Object-Category             | 2                                                                                            |
| Default-Object-Category     | \-                                                                                           |
| Governs-Id                  | 2.5.6.0                                                                                      |
| Standard-ausblenden-Wert        | 1                                                                                            |
| RDN-ATT-ID                  | [**Gemeinsamer Name**](a-cn.md)<br/>                                                       |
| Unterklasse von                 | **Top**<br/>                                                                           |
| Mögliche Vorgesetzten          | [**Verloren und gefunden**](c-lostandfound.md)                                                     |
| Zusätzlich           | \-                                                                                           |
| NT-Security-Descriptor      | o:Bag: schlecht: S:                                                                                 |
| Standard Sicherheits Beschreibung | D: (A;; rpwpcrccdclclorcwowdsddtsw;;;D a) (a;; Rpwpcrccdclclorcwowdsddtsw;;; SY) (A;; Rplclorc;;; Thaus |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2003-r2-attributes"></a>Windows Server 2003 R2-Attribute

Diese Klasse enthält die folgenden Attribute für Windows Server 2003 R2:



| Attribut                                                                   | Obligatorisch. | Abgeleitet von |
|-----------------------------------------------------------------------------|-----------|--------------|
| [**Administrator: Beschreibung**](a-admindescription.md)                             | False     | **Top**      |
| [**Administrator-Anzeige Name**](a-admindisplayname.md)                            | False     | **Top**      |
| [**Zulässige Attribute**](a-allowedattributes.md)                           | False     | **Top**      |
| [**Zulässige Attribute-gültig**](a-allowedattributeseffective.md)        | False     | **Top**      |
| [**Zulässige, untergeordnete Klassen**](a-allowedchildclasses.md)                      | False     | **Top**      |
| [**Zulässig-untergeordnete Klassen-gültig**](a-allowedchildclasseseffective.md)   | False     | **Top**      |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)               | False     | **Top**      |
| [**Kanonischer Name**](a-canonicalname.md)                                   | False     | **Top**      |
| [**Gemeinsamer Name**](a-cn.md)                                                 | False     | **Top**      |
| [**Create-Zeitstempel**](a-createtimestamp.md)                              | False     | **Top**      |
| [**Beschreibung**](a-description.md)                                        | False     | **Top**      |
| [**Anzeige Name**](a-displayname.md)                                       | False     | **Top**      |
| [**Anzeige Name-druckdruck**](a-displaynameprintable.md)                    | False     | **Top**      |
| [**DSA-Signatur**](a-dsasignature.md)                                     | False     | **Top**      |
| [**DS-Core-propagierungs Daten**](a-dscorepropagationdata.md)                 | False     | **Top**      |
| [**Erweiterungs Name**](a-extensionname.md)                                   | False     | **Top**      |
| [**Fahren**](a-flags.md)                                                    | False     | **Top**      |
| [**Aus-Eintrag**](a-fromentry.md)                                           | False     | **Top**      |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)               | False     | **Top**      |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                   | False     | **Top**      |
| [**"F"-Rollen Besitzer**](a-fsmoroleowner.md)                                  | False     | **Top**      |
| [**Instanztyp**](a-instancetype.md)                                     | Richtig      | **Top**      |
| [**Is-critical-System-Object**](a-iscriticalsystemobject.md)               | False     | **Top**      |
| [**Ist-gelöscht**](a-isdeleted.md)                                           | False     | **Top**      |
| [**Is-Member-of-DL**](a-memberof.md)                                       | False     | **Top**      |
| [**Is-Privilege-Inhaber**](a-isprivilegeholder.md)                          | False     | **Top**      |
| [**Letztes-bekannt/übergeordnetes Element**](a-lastknownparent.md)                              | False     | **Top**      |
| [**Verwaltete Objekte**](a-managedobjects.md)                                 | False     | **Top**      |
| [**Verwaltet von**](a-masteredby.md)                                         | False     | **Top**      |
| [**Modify-Zeitstempel**](a-modifytimestamp.md)                              | False     | **Top**      |
| [**MS-com-partitionsetlink**](a-mscom-partitionsetlink.md)                 | False     | **Top**      |
| [**MS-com-userlink**](a-mscom-userlink.md)                                 | False     | **Top**      |
| [**MS-DFSR-computerreferencebl**](a-msdfsr-computerreferencebl.md)         | False     | **Top**      |
| [**MS-DFSR-mitgliedreferencebl**](a-msdfsr-memberreferencebl.md)             | False     | **Top**      |
| [**ms-DS-ca-immed-untergeordnete Elemente**](a-msds-approx-immed-subordinates.md) | False     | **Top**      |
| [**MS-DS-Konsistenz-untergeordnet-Anzahl**](a-ms-ds-consistencychildcount.md)      | False     | **Top**      |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | False     | **Top**      |
| [**ms-DS-gemastert von**](a-msds-masteredby.md)                              | False     | **Top**      |
| [**ms-DS-Members-für-AZ-Role-BL**](a-msds-membersforazrolebl.md)           | False     | **Top**      |
| [**ms-DS-NC-repl-Cursor**](a-msds-ncreplcursors.md)                       | False     | **Top**      |
| [**ms-DS-NC-repl-Inbound-Nachbarn**](a-msds-ncreplinboundneighbors.md)    | False     | **Top**      |
| [**ms-DS-NC-repl-Outbound-Nachbarn**](a-msds-ncreploutboundneighbors.md)  | False     | **Top**      |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                         | False     | **Top**      |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)               | False     | **Top**      |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)     | False     | **Top**      |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)     | False     | **Top**      |
| [**ms-DS-repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)      | False     | **Top**      |
| [**ms-DS-repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)              | False     | **Top**      |
| [**ms-DS-Tasks-für-AZ-Role-BL**](a-msds-tasksforazrolebl.md)               | False     | **Top**      |
| [**ms-DS-Tasks-für-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)               | False     | **Top**      |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                       | False     | **Top**      |
| [**msSFU-30-POSIX-Member-of**](a-mssfu30posixmemberof.md)                  | False     | **Top**      |
| [**NetBoot-SCP-BL**](a-netbootscpbl.md)                                    | False     | **Top**      |
| [**Nicht sicherheitsmitglied-BL**](a-nonsecuritymemberbl.md)                     | False     | **Top**      |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                    | Richtig      | **Top**      |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                | False     | **Top**      |
| [**Objekt-Kategorie**](a-objectcategory.md)                                 | Richtig      | **Top**      |
| [**Object-Klasse**](a-objectclass.md)                                       | Richtig      | **Top**      |
| [**Objekt-GUID**](a-objectguid.md)                                         | False     | **Top**      |
| [**Objekt-Version**](a-objectversion.md)                                   | False     | **Top**      |
| [**Andere-bekannte Objekte**](a-otherwellknownobjects.md)                 | False     | **Top**      |
| [**Partial-Attribute-löschen-List**](a-partialattributedeletionlist.md)   | False     | **Top**      |
| [**Partiell-Attribut Satz**](a-partialattributeset.md)                      | False     | **Top**      |
| [**Mögliche-minderwertig**](a-possibleinferiors.md)                           | False     | **Top**      |
| [**Proxy-Objekt Name**](a-proxiedobjectname.md)                          | False     | **Top**      |
| [**Proxy Adressen**](a-proxyaddresses.md)                                 | False     | **Top**      |
| [**Abfrage-Richtlinie-BL**](a-querypolicybl.md)                                  | False     | **Top**      |
| [**RDN**](a-name.md)                                                       | False     | **Top**      |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                   | False     | **Top**      |
| [**REPL-Update-Vector**](a-repluptodatevector.md)                        | False     | **Top**      |
| [**Berichte**](a-directreports.md)                                          | False     | **Top**      |
| [**Reps-from**](a-repsfrom.md)                                             | False     | **Top**      |
| [**Reps-to**](a-repsto.md)                                                 | False     | **Top**      |
| [**Novel**](a-revision.md)                                              | False     | **Top**      |
| [**SD-Rechte**](a-sdrightseffective.md)                          | False     | **Top**      |
| [**Server-Reference-BL**](a-serverreferencebl.md)                          | False     | **Top**      |
| [**Anzeigen-in-Advanced-nur anzeigen**](a-showinadvancedviewonly.md)              | False     | **Top**      |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | False     | **Top**      |
| [**Struktur-Objekt-Klasse**](a-structuralobjectclass.md)                  | False     | **Top**      |
| [**Sub-Refs**](a-subrefs.md)                                               | False     | **Top**      |
| [**Subschemasubentry**](a-subschemasubentry.md)                            | False     | **Top**      |
| [**SystemFlags**](a-systemflags.md)                                       | False     | **Top**      |
| [**Die Anwendung wurde geändert.**](a-usnchanged.md)                                         | False     | **Top**      |
| [**Von der Anwendung erstellte**](a-usncreated.md)                                         | False     | **Top**      |
| [**USA-DSA-letzte-obj-entfernt**](a-usndsalastobjremoved.md)                  | False     | **Top**      |
| [**Standort-und standortübergreifende standortübergreifende**](a-usnintersite.md)                                     | False     | **Top**      |
| [**"An-Last-obj-REM"**](a-usnlastobjrem.md)                                 | False     | **Top**      |
| [**Quell Code Quelle**](a-usnsource.md)                                           | False     | **Top**      |
| [**WBEM-Pfad**](a-wbempath.md)                                             | False     | **Top**      |
| [**Bekannte Objekte**](a-wellknownobjects.md)                            | False     | **Top**      |
| [**Bei Änderung**](a-whenchanged.md)                                       | False     | **Top**      |
| [**Bei Erstellung**](a-whencreated.md)                                       | False     | **Top**      |
| [**WWW-Homepage**](a-wwwhomepage.md)                                      | False     | **Top**      |
| [**WWW-Page-other**](a-url.md)                                             | False     | **Top**      |



## <a name="windows-server-2008"></a>Windows Server 2008

-   [Attribute](#windows-server-2008-attributes)



| Eingabe | Wert |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Richtig                                                                                         |
| Object-Category             | 2                                                                                            |
| Default-Object-Category     | \-                                                                                           |
| Governs-Id                  | 2.5.6.0                                                                                      |
| Standard-ausblenden-Wert        | 1                                                                                            |
| RDN-ATT-ID                  | [**Gemeinsamer Name**](a-cn.md)<br/>                                                       |
| Unterklasse von                 | **Top**<br/>                                                                           |
| Mögliche Vorgesetzten          | [**Verloren und gefunden**](c-lostandfound.md)                                                     |
| Zusätzlich           | \-                                                                                           |
| NT-Security-Descriptor      | o:Bag: schlecht: S:                                                                                 |
| Standard Sicherheits Beschreibung | D: (A;; rpwpcrccdclclorcwowdsddtsw;;;D a) (a;; Rpwpcrccdclclorcwowdsddtsw;;; SY) (A;; Rplclorc;;; Thaus |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2008-attributes"></a>Windows Server 2008-Attribute

Diese Klasse enthält die folgenden Attribute für Windows Server 2008:



| Attribut                                                                      | Obligatorisch. | Abgeleitet von |
|--------------------------------------------------------------------------------|-----------|--------------|
| [**Administrator: Beschreibung**](a-admindescription.md)                                | False     | **Top**      |
| [**Administrator-Anzeige Name**](a-admindisplayname.md)                               | False     | **Top**      |
| [**Zulässige Attribute**](a-allowedattributes.md)                              | False     | **Top**      |
| [**Zulässige Attribute-gültig**](a-allowedattributeseffective.md)           | False     | **Top**      |
| [**Zulässige, untergeordnete Klassen**](a-allowedchildclasses.md)                         | False     | **Top**      |
| [**Zulässig-untergeordnete Klassen-gültig**](a-allowedchildclasseseffective.md)      | False     | **Top**      |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                  | False     | **Top**      |
| [**Kanonischer Name**](a-canonicalname.md)                                      | False     | **Top**      |
| [**Gemeinsamer Name**](a-cn.md)                                                    | False     | **Top**      |
| [**Create-Zeitstempel**](a-createtimestamp.md)                                 | False     | **Top**      |
| [**Beschreibung**](a-description.md)                                           | False     | **Top**      |
| [**Anzeige Name**](a-displayname.md)                                          | False     | **Top**      |
| [**Anzeige Name-druckdruck**](a-displaynameprintable.md)                       | False     | **Top**      |
| [**DSA-Signatur**](a-dsasignature.md)                                        | False     | **Top**      |
| [**DS-Core-propagierungs Daten**](a-dscorepropagationdata.md)                    | False     | **Top**      |
| [**Erweiterungs Name**](a-extensionname.md)                                      | False     | **Top**      |
| [**Fahren**](a-flags.md)                                                       | False     | **Top**      |
| [**Aus-Eintrag**](a-fromentry.md)                                              | False     | **Top**      |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                  | False     | **Top**      |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                      | False     | **Top**      |
| [**"F"-Rollen Besitzer**](a-fsmoroleowner.md)                                     | False     | **Top**      |
| [**Instanztyp**](a-instancetype.md)                                        | Richtig      | **Top**      |
| [**Is-critical-System-Object**](a-iscriticalsystemobject.md)                  | False     | **Top**      |
| [**Ist-gelöscht**](a-isdeleted.md)                                              | False     | **Top**      |
| [**Is-Member-of-DL**](a-memberof.md)                                          | False     | **Top**      |
| [**Is-Privilege-Inhaber**](a-isprivilegeholder.md)                             | False     | **Top**      |
| [**Letztes-bekannt/übergeordnetes Element**](a-lastknownparent.md)                                 | False     | **Top**      |
| [**Verwaltete Objekte**](a-managedobjects.md)                                    | False     | **Top**      |
| [**Verwaltet von**](a-masteredby.md)                                            | False     | **Top**      |
| [**Modify-Zeitstempel**](a-modifytimestamp.md)                                 | False     | **Top**      |
| [**MS-com-partitionsetlink**](a-mscom-partitionsetlink.md)                    | False     | **Top**      |
| [**MS-com-userlink**](a-mscom-userlink.md)                                    | False     | **Top**      |
| [**MS-DFSR-computerreferencebl**](a-msdfsr-computerreferencebl.md)            | False     | **Top**      |
| [**MS-DFSR-mitgliedreferencebl**](a-msdfsr-memberreferencebl.md)                | False     | **Top**      |
| [**ms-DS-ca-immed-untergeordnete Elemente**](a-msds-approx-immed-subordinates.md)    | False     | **Top**      |
| [**ms-DS-authentieredto-accountlist**](a-msds-authenticatedtoaccountlist.md) | False     | **Top**      |
| [**MS-DS-Konsistenz-untergeordnet-Anzahl**](a-ms-ds-consistencychildcount.md)         | False     | **Top**      |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                      | False     | **Top**      |
| [**ms-DS-is-Domain-for**](a-msds-isdomainfor.md)                              | False     | **Top**      |
| [**ms-DS-is-full-Replica-for**](a-msds-isfullreplicafor.md)                   | False     | **Top**      |
| [**ms-DS-is-Partial-Replica-for**](a-msds-ispartialreplicafor.md)             | False     | **Top**      |
| [**ms-DS-krbtgt-Link-BL**](a-msds-krbtgtlinkbl.md)                            | False     | **Top**      |
| [**ms-DS-gemastert von**](a-msds-masteredby.md)                                 | False     | **Top**      |
| [**ms-DS-Members-für-AZ-Role-BL**](a-msds-membersforazrolebl.md)              | False     | **Top**      |
| [**ms-DS-NC-repl-Cursor**](a-msds-ncreplcursors.md)                          | False     | **Top**      |
| [**ms-DS-NC-repl-Inbound-Nachbarn**](a-msds-ncreplinboundneighbors.md)       | False     | **Top**      |
| [**ms-DS-NC-repl-Outbound-Nachbarn**](a-msds-ncreploutboundneighbors.md)     | False     | **Top**      |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)  | False     | **Top**      |
| [**ms-DS-NC-Typ**](a-msds-nctype.md)                                         | False     | **Top**      |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                            | False     | **Top**      |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                  | False     | **Top**      |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)        | False     | **Top**      |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)        | False     | **Top**      |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                           | False     | **Top**      |
| [**ms-DS-PSO-angewendet**](a-msds-psoapplied.md)                                 | False     | **Top**      |
| [**ms-DS-repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)         | False     | **Top**      |
| [**ms-DS-repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                 | False     | **Top**      |
| [**ms-DS-offengelegt-DSAs**](a-msds-revealeddsas.md)                             | False     | **Top**      |
| [**ms-DS-enthüllt-List-BL**](a-msds-revealedlistbl.md)                        | False     | **Top**      |
| [**ms-DS-Tasks-für-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                  | False     | **Top**      |
| [**ms-DS-Tasks-für-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                  | False     | **Top**      |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                          | False     | **Top**      |
| [**msSFU-30-POSIX-Member-of**](a-mssfu30posixmemberof.md)                     | False     | **Top**      |
| [**NetBoot-SCP-BL**](a-netbootscpbl.md)                                       | False     | **Top**      |
| [**Nicht sicherheitsmitglied-BL**](a-nonsecuritymemberbl.md)                        | False     | **Top**      |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                       | Richtig      | **Top**      |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                   | False     | **Top**      |
| [**Objekt-Kategorie**](a-objectcategory.md)                                    | Richtig      | **Top**      |
| [**Object-Klasse**](a-objectclass.md)                                          | Richtig      | **Top**      |
| [**Objekt-GUID**](a-objectguid.md)                                            | False     | **Top**      |
| [**Objekt-Version**](a-objectversion.md)                                      | False     | **Top**      |
| [**Andere-bekannte Objekte**](a-otherwellknownobjects.md)                    | False     | **Top**      |
| [**Partial-Attribute-löschen-List**](a-partialattributedeletionlist.md)      | False     | **Top**      |
| [**Partiell-Attribut Satz**](a-partialattributeset.md)                         | False     | **Top**      |
| [**Mögliche-minderwertig**](a-possibleinferiors.md)                              | False     | **Top**      |
| [**Proxy-Objekt Name**](a-proxiedobjectname.md)                             | False     | **Top**      |
| [**Proxy Adressen**](a-proxyaddresses.md)                                    | False     | **Top**      |
| [**Abfrage-Richtlinie-BL**](a-querypolicybl.md)                                     | False     | **Top**      |
| [**RDN**](a-name.md)                                                          | False     | **Top**      |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                      | False     | **Top**      |
| [**REPL-Update-Vector**](a-repluptodatevector.md)                           | False     | **Top**      |
| [**Berichte**](a-directreports.md)                                             | False     | **Top**      |
| [**Reps-from**](a-repsfrom.md)                                                | False     | **Top**      |
| [**Reps-to**](a-repsto.md)                                                    | False     | **Top**      |
| [**Novel**](a-revision.md)                                                 | False     | **Top**      |
| [**SD-Rechte**](a-sdrightseffective.md)                             | False     | **Top**      |
| [**Server-Reference-BL**](a-serverreferencebl.md)                             | False     | **Top**      |
| [**Anzeigen-in-Advanced-nur anzeigen**](a-showinadvancedviewonly.md)                 | False     | **Top**      |
| [**Site-Object-BL**](a-siteobjectbl.md)                                       | False     | **Top**      |
| [**Struktur-Objekt-Klasse**](a-structuralobjectclass.md)                     | False     | **Top**      |
| [**Sub-Refs**](a-subrefs.md)                                                  | False     | **Top**      |
| [**Subschemasubentry**](a-subschemasubentry.md)                               | False     | **Top**      |
| [**SystemFlags**](a-systemflags.md)                                          | False     | **Top**      |
| [**Die Anwendung wurde geändert.**](a-usnchanged.md)                                            | False     | **Top**      |
| [**Von der Anwendung erstellte**](a-usncreated.md)                                            | False     | **Top**      |
| [**USA-DSA-letzte-obj-entfernt**](a-usndsalastobjremoved.md)                     | False     | **Top**      |
| [**Standort-und standortübergreifende standortübergreifende**](a-usnintersite.md)                                        | False     | **Top**      |
| [**"An-Last-obj-REM"**](a-usnlastobjrem.md)                                    | False     | **Top**      |
| [**Quell Code Quelle**](a-usnsource.md)                                              | False     | **Top**      |
| [**WBEM-Pfad**](a-wbempath.md)                                                | False     | **Top**      |
| [**Bekannte Objekte**](a-wellknownobjects.md)                               | False     | **Top**      |
| [**Bei Änderung**](a-whenchanged.md)                                          | False     | **Top**      |
| [**Bei Erstellung**](a-whencreated.md)                                          | False     | **Top**      |
| [**WWW-Homepage**](a-wwwhomepage.md)                                         | False     | **Top**      |
| [**WWW-Page-other**](a-url.md)                                                | False     | **Top**      |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2

-   [Attribute](#windows-server-2008-r2-attributes)



| Eingabe | Wert |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Richtig                                                                                         |
| Object-Category             | 2                                                                                            |
| Default-Object-Category     | \-                                                                                           |
| Governs-Id                  | 2.5.6.0                                                                                      |
| Standard-ausblenden-Wert        | 1                                                                                            |
| RDN-ATT-ID                  | [**Gemeinsamer Name**](a-cn.md)<br/>                                                       |
| Unterklasse von                 | **Top**<br/>                                                                           |
| Mögliche Vorgesetzten          | [**Verloren und gefunden**](c-lostandfound.md)                                                     |
| Zusätzlich           | \-                                                                                           |
| NT-Security-Descriptor      | o:Bag: schlecht: S:                                                                                 |
| Standard Sicherheits Beschreibung | D: (A;; rpwpcrccdclclorcwowdsddtsw;;;D a) (a;; Rpwpcrccdclclorcwowdsddtsw;;; SY) (A;; Rplclorc;;; Thaus |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2008-r2-attributes"></a>Windows Server 2008 R2-Attribute

Diese Klasse enthält die folgenden Attribute für Windows Server 2008 R2:



| Attribut                                                                        | Obligatorisch. | Abgeleitet von |
|----------------------------------------------------------------------------------|-----------|--------------|
| [**Administrator: Beschreibung**](a-admindescription.md)                                  | False     | **Top**      |
| [**Administrator-Anzeige Name**](a-admindisplayname.md)                                 | False     | **Top**      |
| [**Zulässige Attribute**](a-allowedattributes.md)                                | False     | **Top**      |
| [**Zulässige Attribute-gültig**](a-allowedattributeseffective.md)             | False     | **Top**      |
| [**Zulässige, untergeordnete Klassen**](a-allowedchildclasses.md)                           | False     | **Top**      |
| [**Zulässig-untergeordnete Klassen-gültig**](a-allowedchildclasseseffective.md)        | False     | **Top**      |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                    | False     | **Top**      |
| [**Kanonischer Name**](a-canonicalname.md)                                        | False     | **Top**      |
| [**Gemeinsamer Name**](a-cn.md)                                                      | False     | **Top**      |
| [**Create-Zeitstempel**](a-createtimestamp.md)                                   | False     | **Top**      |
| [**Beschreibung**](a-description.md)                                             | False     | **Top**      |
| [**Anzeige Name**](a-displayname.md)                                            | False     | **Top**      |
| [**Anzeige Name-druckdruck**](a-displaynameprintable.md)                         | False     | **Top**      |
| [**DSA-Signatur**](a-dsasignature.md)                                          | False     | **Top**      |
| [**DS-Core-propagierungs Daten**](a-dscorepropagationdata.md)                      | False     | **Top**      |
| [**Erweiterungs Name**](a-extensionname.md)                                        | False     | **Top**      |
| [**Fahren**](a-flags.md)                                                         | False     | **Top**      |
| [**Aus-Eintrag**](a-fromentry.md)                                                | False     | **Top**      |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                    | False     | **Top**      |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                        | False     | **Top**      |
| [**"F"-Rollen Besitzer**](a-fsmoroleowner.md)                                       | False     | **Top**      |
| [**Instanztyp**](a-instancetype.md)                                          | Richtig      | **Top**      |
| [**Is-critical-System-Object**](a-iscriticalsystemobject.md)                    | False     | **Top**      |
| [**Ist-gelöscht**](a-isdeleted.md)                                                | False     | **Top**      |
| [**Is-Member-of-DL**](a-memberof.md)                                            | False     | **Top**      |
| [**Is-Privilege-Inhaber**](a-isprivilegeholder.md)                               | False     | **Top**      |
| [**Ist-recycelt**](a-isrecycled.md)                                              | False     | **Top**      |
| [**Letztes-bekannt/übergeordnetes Element**](a-lastknownparent.md)                                   | False     | **Top**      |
| [**Verwaltete Objekte**](a-managedobjects.md)                                      | False     | **Top**      |
| [**Verwaltet von**](a-masteredby.md)                                              | False     | **Top**      |
| [**Modify-Zeitstempel**](a-modifytimestamp.md)                                   | False     | **Top**      |
| [**MS-com-partitionsetlink**](a-mscom-partitionsetlink.md)                      | False     | **Top**      |
| [**MS-com-userlink**](a-mscom-userlink.md)                                      | False     | **Top**      |
| [**MS-DFSR-computerreferencebl**](a-msdfsr-computerreferencebl.md)              | False     | **Top**      |
| [**MS-DFSR-mitgliedreferencebl**](a-msdfsr-memberreferencebl.md)                  | False     | **Top**      |
| [**ms-DS-ca-immed-untergeordnete Elemente**](a-msds-approx-immed-subordinates.md)      | False     | **Top**      |
| [**ms-DS-authentieredto-accountlist**](a-msds-authenticatedtoaccountlist.md)   | False     | **Top**      |
| [**MS-DS-Konsistenz-untergeordnet-Anzahl**](a-ms-ds-consistencychildcount.md)           | False     | **Top**      |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                        | False     | **Top**      |
| [**ms-DS-aktiviert-Feature-BL**](a-msds-enabledfeaturebl.md)                      | False     | **Top**      |
| [**ms-DS-Host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)             | False     | **Top**      |
| [**ms-DS-is-Domain-for**](a-msds-isdomainfor.md)                                | False     | **Top**      |
| [**ms-DS-is-full-Replica-for**](a-msds-isfullreplicafor.md)                     | False     | **Top**      |
| [**ms-DS-is-Partial-Replica-for**](a-msds-ispartialreplicafor.md)               | False     | **Top**      |
| [**ms-DS-krbtgt-Link-BL**](a-msds-krbtgtlinkbl.md)                              | False     | **Top**      |
| [**ms-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                              | False     | **Top**      |
| [**ms-DS-local-Effective-Lösch Zeit**](a-msds-localeffectivedeletiontime.md) | False     | **Top**      |
| [**ms-DS-local-Effective-Papier-Time**](a-msds-localeffectiverecycletime.md)   | False     | **Top**      |
| [**ms-DS-gemastert von**](a-msds-masteredby.md)                                   | False     | **Top**      |
| [**ms-DS-Members-für-AZ-Role-BL**](a-msds-membersforazrolebl.md)                | False     | **Top**      |
| [**ms-DS-NC-repl-Cursor**](a-msds-ncreplcursors.md)                            | False     | **Top**      |
| [**ms-DS-NC-repl-Inbound-Nachbarn**](a-msds-ncreplinboundneighbors.md)         | False     | **Top**      |
| [**ms-DS-NC-repl-Outbound-Nachbarn**](a-msds-ncreploutboundneighbors.md)       | False     | **Top**      |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)    | False     | **Top**      |
| [**ms-DS-NC-Typ**](a-msds-nctype.md)                                           | False     | **Top**      |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                              | False     | **Top**      |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                    | False     | **Top**      |
| [**ms-DS-oidtoidgruppe-Link-BL**](a-msds-oidtogrouplinkbl.md)                      | False     | **Top**      |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)          | False     | **Top**      |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)          | False     | **Top**      |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                             | False     | **Top**      |
| [**ms-DS-PSO-angewendet**](a-msds-psoapplied.md)                                   | False     | **Top**      |
| [**ms-DS-repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)           | False     | **Top**      |
| [**ms-DS-repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                   | False     | **Top**      |
| [**ms-DS-offengelegt-DSAs**](a-msds-revealeddsas.md)                               | False     | **Top**      |
| [**ms-DS-enthüllt-List-BL**](a-msds-revealedlistbl.md)                          | False     | **Top**      |
| [**ms-DS-Tasks-für-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                    | False     | **Top**      |
| [**ms-DS-Tasks-für-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                    | False     | **Top**      |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                            | False     | **Top**      |
| [**msSFU-30-POSIX-Member-of**](a-mssfu30posixmemberof.md)                       | False     | **Top**      |
| [**NetBoot-SCP-BL**](a-netbootscpbl.md)                                         | False     | **Top**      |
| [**Nicht sicherheitsmitglied-BL**](a-nonsecuritymemberbl.md)                          | False     | **Top**      |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                         | Richtig      | **Top**      |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                     | False     | **Top**      |
| [**Objekt-Kategorie**](a-objectcategory.md)                                      | Richtig      | **Top**      |
| [**Object-Klasse**](a-objectclass.md)                                            | Richtig      | **Top**      |
| [**Objekt-GUID**](a-objectguid.md)                                              | False     | **Top**      |
| [**Objekt-Version**](a-objectversion.md)                                        | False     | **Top**      |
| [**Andere-bekannte Objekte**](a-otherwellknownobjects.md)                      | False     | **Top**      |
| [**Partial-Attribute-löschen-List**](a-partialattributedeletionlist.md)        | False     | **Top**      |
| [**Partiell-Attribut Satz**](a-partialattributeset.md)                           | False     | **Top**      |
| [**Mögliche-minderwertig**](a-possibleinferiors.md)                                | False     | **Top**      |
| [**Proxy-Objekt Name**](a-proxiedobjectname.md)                               | False     | **Top**      |
| [**Proxy Adressen**](a-proxyaddresses.md)                                      | False     | **Top**      |
| [**Abfrage-Richtlinie-BL**](a-querypolicybl.md)                                       | False     | **Top**      |
| [**RDN**](a-name.md)                                                            | False     | **Top**      |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                        | False     | **Top**      |
| [**REPL-Update-Vector**](a-repluptodatevector.md)                             | False     | **Top**      |
| [**Berichte**](a-directreports.md)                                               | False     | **Top**      |
| [**Reps-from**](a-repsfrom.md)                                                  | False     | **Top**      |
| [**Reps-to**](a-repsto.md)                                                      | False     | **Top**      |
| [**Novel**](a-revision.md)                                                   | False     | **Top**      |
| [**SD-Rechte**](a-sdrightseffective.md)                               | False     | **Top**      |
| [**Server-Reference-BL**](a-serverreferencebl.md)                               | False     | **Top**      |
| [**Anzeigen-in-Advanced-nur anzeigen**](a-showinadvancedviewonly.md)                   | False     | **Top**      |
| [**Site-Object-BL**](a-siteobjectbl.md)                                         | False     | **Top**      |
| [**Struktur-Objekt-Klasse**](a-structuralobjectclass.md)                       | False     | **Top**      |
| [**Sub-Refs**](a-subrefs.md)                                                    | False     | **Top**      |
| [**Subschemasubentry**](a-subschemasubentry.md)                                 | False     | **Top**      |
| [**SystemFlags**](a-systemflags.md)                                            | False     | **Top**      |
| [**Die Anwendung wurde geändert.**](a-usnchanged.md)                                              | False     | **Top**      |
| [**Von der Anwendung erstellte**](a-usncreated.md)                                              | False     | **Top**      |
| [**USA-DSA-letzte-obj-entfernt**](a-usndsalastobjremoved.md)                       | False     | **Top**      |
| [**Standort-und standortübergreifende standortübergreifende**](a-usnintersite.md)                                          | False     | **Top**      |
| [**"An-Last-obj-REM"**](a-usnlastobjrem.md)                                      | False     | **Top**      |
| [**Quell Code Quelle**](a-usnsource.md)                                                | False     | **Top**      |
| [**WBEM-Pfad**](a-wbempath.md)                                                  | False     | **Top**      |
| [**Bekannte Objekte**](a-wellknownobjects.md)                                 | False     | **Top**      |
| [**Bei Änderung**](a-whenchanged.md)                                            | False     | **Top**      |
| [**Bei Erstellung**](a-whencreated.md)                                            | False     | **Top**      |
| [**WWW-Homepage**](a-wwwhomepage.md)                                           | False     | **Top**      |
| [**WWW-Page-other**](a-url.md)                                                  | False     | **Top**      |



## <a name="windows-server-2012"></a>Windows Server 2012

-   [Attribute](#windows-server-2012-attributes)



| Eingabe | Wert |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Richtig                                                                                         |
| Object-Category             | 2                                                                                            |
| Default-Object-Category     | \-                                                                                           |
| Governs-Id                  | 2.5.6.0                                                                                      |
| Standard-ausblenden-Wert        | 1                                                                                            |
| RDN-ATT-ID                  | [**Gemeinsamer Name**](a-cn.md)<br/>                                                       |
| Unterklasse von                 | **Top**<br/>                                                                           |
| Mögliche Vorgesetzten          | [**Verloren und gefunden**](c-lostandfound.md)                                                     |
| Zusätzlich           | \-                                                                                           |
| NT-Security-Descriptor      | o:Bag: schlecht: S:                                                                                 |
| Standard Sicherheits Beschreibung | D: (A;; rpwpcrccdclclorcwowdsddtsw;;;D a) (a;; Rpwpcrccdclclorcwowdsddtsw;;; SY) (A;; Rplclorc;;; Thaus |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2012-attributes"></a>Windows Server 2012-Attribute

Diese Klasse enthält die folgenden Attribute für Windows Server 2012:



| Attribut                                                                                    | Obligatorisch. | Abgeleitet von |
|----------------------------------------------------------------------------------------------|-----------|--------------|
| [**Administrator: Beschreibung**](a-admindescription.md)                                              | False     | **Top**      |
| [**Administrator-Anzeige Name**](a-admindisplayname.md)                                             | False     | **Top**      |
| [**Zulässige Attribute**](a-allowedattributes.md)                                            | False     | **Top**      |
| [**Zulässige Attribute-gültig**](a-allowedattributeseffective.md)                         | False     | **Top**      |
| [**Zulässige, untergeordnete Klassen**](a-allowedchildclasses.md)                                       | False     | **Top**      |
| [**Zulässig-untergeordnete Klassen-gültig**](a-allowedchildclasseseffective.md)                    | False     | **Top**      |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                                | False     | **Top**      |
| [**Kanonischer Name**](a-canonicalname.md)                                                    | False     | **Top**      |
| [**Gemeinsamer Name**](a-cn.md)                                                                  | False     | **Top**      |
| [**Create-Zeitstempel**](a-createtimestamp.md)                                               | False     | **Top**      |
| [**Beschreibung**](a-description.md)                                                         | False     | **Top**      |
| [**Anzeige Name**](a-displayname.md)                                                        | False     | **Top**      |
| [**Anzeige Name-druckdruck**](a-displaynameprintable.md)                                     | False     | **Top**      |
| [**DSA-Signatur**](a-dsasignature.md)                                                      | False     | **Top**      |
| [**DS-Core-propagierungs Daten**](a-dscorepropagationdata.md)                                  | False     | **Top**      |
| [**Erweiterungs Name**](a-extensionname.md)                                                    | False     | **Top**      |
| [**Fahren**](a-flags.md)                                                                     | False     | **Top**      |
| [**Aus-Eintrag**](a-fromentry.md)                                                            | False     | **Top**      |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                                | False     | **Top**      |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                                    | False     | **Top**      |
| [**"F"-Rollen Besitzer**](a-fsmoroleowner.md)                                                   | False     | **Top**      |
| [**Instanztyp**](a-instancetype.md)                                                      | Richtig      | **Top**      |
| [**Is-critical-System-Object**](a-iscriticalsystemobject.md)                                | False     | **Top**      |
| [**Ist-gelöscht**](a-isdeleted.md)                                                            | False     | **Top**      |
| [**Is-Member-of-DL**](a-memberof.md)                                                        | False     | **Top**      |
| [**Is-Privilege-Inhaber**](a-isprivilegeholder.md)                                           | False     | **Top**      |
| [**Ist-recycelt**](a-isrecycled.md)                                                          | False     | **Top**      |
| [**Letztes-bekannt/übergeordnetes Element**](a-lastknownparent.md)                                               | False     | **Top**      |
| [**Verwaltete Objekte**](a-managedobjects.md)                                                  | False     | **Top**      |
| [**Verwaltet von**](a-masteredby.md)                                                          | False     | **Top**      |
| [**Modify-Zeitstempel**](a-modifytimestamp.md)                                               | False     | **Top**      |
| [**MS-com-partitionsetlink**](a-mscom-partitionsetlink.md)                                  | False     | **Top**      |
| [**MS-com-userlink**](a-mscom-userlink.md)                                                  | False     | **Top**      |
| [**MS-DFSR-computerreferencebl**](a-msdfsr-computerreferencebl.md)                          | False     | **Top**      |
| [**MS-DFSR-mitgliedreferencebl**](a-msdfsr-memberreferencebl.md)                              | False     | **Top**      |
| [**ms-DS-ca-immed-untergeordnete Elemente**](a-msds-approx-immed-subordinates.md)                  | False     | **Top**      |
| [**ms-DS-authentieredto-accountlist**](a-msds-authenticatedtoaccountlist.md)               | False     | **Top**      |
| [**ms-DS-Claim-Shares-mögliche-values-with-BL**](a-msds-claimsharespossiblevalueswithbl.md) | False     | **Top**      |
| [**MS-DS-Konsistenz-untergeordnet-Anzahl**](a-ms-ds-consistencychildcount.md)                       | False     | **Top**      |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                                    | False     | **Top**      |
| [**ms-DS-aktiviert-Feature-BL**](a-msds-enabledfeaturebl.md)                                  | False     | **Top**      |
| [**ms-DS-Host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)                         | False     | **Top**      |
| [**ms-DS-is-Domain-for**](a-msds-isdomainfor.md)                                            | False     | **Top**      |
| [**ms-DS-is-full-Replica-for**](a-msds-isfullreplicafor.md)                                 | False     | **Top**      |
| [**ms-DS-is-Partial-Replica-for**](a-msds-ispartialreplicafor.md)                           | False     | **Top**      |
| [**ms-DS-is-Primary-Computer-für**](a-msds-isprimarycomputerfor.md)                         | False     | **Top**      |
| [**ms-DS-krbtgt-Link-BL**](a-msds-krbtgtlinkbl.md)                                          | False     | **Top**      |
| [**ms-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                                          | False     | **Top**      |
| [**ms-DS-local-Effective-Lösch Zeit**](a-msds-localeffectivedeletiontime.md)             | False     | **Top**      |
| [**ms-DS-local-Effective-Papier-Time**](a-msds-localeffectiverecycletime.md)               | False     | **Top**      |
| [**ms-DS-gemastert von**](a-msds-masteredby.md)                                               | False     | **Top**      |
| [**ms-DS-Members-für-AZ-Role-BL**](a-msds-membersforazrolebl.md)                            | False     | **Top**      |
| [**ms-DS-Members-of-Resource-Property-List-BL**](a-msds-membersofresourcepropertylistbl.md) | False     | **Top**      |
| [**ms-DS-NC-repl-Cursor**](a-msds-ncreplcursors.md)                                        | False     | **Top**      |
| [**ms-DS-NC-repl-Inbound-Nachbarn**](a-msds-ncreplinboundneighbors.md)                     | False     | **Top**      |
| [**ms-DS-NC-repl-Outbound-Nachbarn**](a-msds-ncreploutboundneighbors.md)                   | False     | **Top**      |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)                | False     | **Top**      |
| [**ms-DS-NC-Typ**](a-msds-nctype.md)                                                       | False     | **Top**      |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                                          | False     | **Top**      |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                                | False     | **Top**      |
| [**ms-DS-oidtoidgruppe-Link-BL**](a-msds-oidtogrouplinkbl.md)                                  | False     | **Top**      |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)                      | False     | **Top**      |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)                      | False     | **Top**      |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                                         | False     | **Top**      |
| [**ms-DS-PSO-angewendet**](a-msds-psoapplied.md)                                               | False     | **Top**      |
| [**ms-DS-repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)                       | False     | **Top**      |
| [**ms-DS-repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                               | False     | **Top**      |
| [**ms-DS-offengelegt-DSAs**](a-msds-revealeddsas.md)                                           | False     | **Top**      |
| [**ms-DS-enthüllt-List-BL**](a-msds-revealedlistbl.md)                                      | False     | **Top**      |
| [**ms-DS-Tasks-für-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                                | False     | **Top**      |
| [**ms-DS-Tasks-für-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                                | False     | **Top**      |
| [**ms-DS-TDO-Egress-BL**](a-msds-tdoegressbl.md)                                            | False     | **Top**      |
| [**ms-DS-TDO-Ingress-BL**](a-msds-tdoingressbl.md)                                          | False     | **Top**      |
| [**ms-DS-Value-Type-Reference-BL**](a-msds-valuetypereferencebl.md)                         | False     | **Top**      |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                                        | False     | **Top**      |
| [**msSFU-30-POSIX-Member-of**](a-mssfu30posixmemberof.md)                                   | False     | **Top**      |
| [**NetBoot-SCP-BL**](a-netbootscpbl.md)                                                     | False     | **Top**      |
| [**Nicht sicherheitsmitglied-BL**](a-nonsecuritymemberbl.md)                                      | False     | **Top**      |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                                     | Richtig      | **Top**      |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                                 | False     | **Top**      |
| [**Objekt-Kategorie**](a-objectcategory.md)                                                  | Richtig      | **Top**      |
| [**Object-Klasse**](a-objectclass.md)                                                        | Richtig      | **Top**      |
| [**Objekt-GUID**](a-objectguid.md)                                                          | False     | **Top**      |
| [**Objekt-Version**](a-objectversion.md)                                                    | False     | **Top**      |
| [**Andere-bekannte Objekte**](a-otherwellknownobjects.md)                                  | False     | **Top**      |
| [**Partial-Attribute-löschen-List**](a-partialattributedeletionlist.md)                    | False     | **Top**      |
| [**Partiell-Attribut Satz**](a-partialattributeset.md)                                       | False     | **Top**      |
| [**Mögliche-minderwertig**](a-possibleinferiors.md)                                            | False     | **Top**      |
| [**Proxy-Objekt Name**](a-proxiedobjectname.md)                                           | False     | **Top**      |
| [**Proxy Adressen**](a-proxyaddresses.md)                                                  | False     | **Top**      |
| [**Abfrage-Richtlinie-BL**](a-querypolicybl.md)                                                   | False     | **Top**      |
| [**RDN**](a-name.md)                                                                        | False     | **Top**      |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                                    | False     | **Top**      |
| [**REPL-Update-Vector**](a-repluptodatevector.md)                                         | False     | **Top**      |
| [**Berichte**](a-directreports.md)                                                           | False     | **Top**      |
| [**Reps-from**](a-repsfrom.md)                                                              | False     | **Top**      |
| [**Reps-to**](a-repsto.md)                                                                  | False     | **Top**      |
| [**Novel**](a-revision.md)                                                               | False     | **Top**      |
| [**SD-Rechte**](a-sdrightseffective.md)                                           | False     | **Top**      |
| [**Server-Reference-BL**](a-serverreferencebl.md)                                           | False     | **Top**      |
| [**Anzeigen-in-Advanced-nur anzeigen**](a-showinadvancedviewonly.md)                               | False     | **Top**      |
| [**Site-Object-BL**](a-siteobjectbl.md)                                                     | False     | **Top**      |
| [**Struktur-Objekt-Klasse**](a-structuralobjectclass.md)                                   | False     | **Top**      |
| [**Sub-Refs**](a-subrefs.md)                                                                | False     | **Top**      |
| [**Subschemasubentry**](a-subschemasubentry.md)                                             | False     | **Top**      |
| [**SystemFlags**](a-systemflags.md)                                                        | False     | **Top**      |
| [**Die Anwendung wurde geändert.**](a-usnchanged.md)                                                          | False     | **Top**      |
| [**Von der Anwendung erstellte**](a-usncreated.md)                                                          | False     | **Top**      |
| [**USA-DSA-letzte-obj-entfernt**](a-usndsalastobjremoved.md)                                   | False     | **Top**      |
| [**Standort-und standortübergreifende standortübergreifende**](a-usnintersite.md)                                                      | False     | **Top**      |
| [**"An-Last-obj-REM"**](a-usnlastobjrem.md)                                                  | False     | **Top**      |
| [**Quell Code Quelle**](a-usnsource.md)                                                            | False     | **Top**      |
| [**WBEM-Pfad**](a-wbempath.md)                                                              | False     | **Top**      |
| [**Bekannte Objekte**](a-wellknownobjects.md)                                             | False     | **Top**      |
| [**Bei Änderung**](a-whenchanged.md)                                                        | False     | **Top**      |
| [**Bei Erstellung**](a-whencreated.md)                                                        | False     | **Top**      |
| [**WWW-Homepage**](a-wwwhomepage.md)                                                       | False     | **Top**      |
| [**WWW-Page-other**](a-url.md)                                                              | False     | **Top**      |



 

 





