---
title: Print-Queue-Klasse
description: Enthält Informationen über eine Druck Warteschlange.
ms.assetid: 779eb37c-f94e-472a-9551-8a0f72fe0e2b
ms.tgt_platform: multiple
keywords:
- AD-Schema der Print-Queue-Klasse
- PrintQueue-Klasse, AD-Schema
topic_type:
- apiref
api_name:
- Print-Queue
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7995598603af4cab7b4b9d6f150e92964f0ee616
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104479511"
---
# <a name="print-queue-class"></a>Print-Queue-Klasse

Enthält Informationen über eine Druck Warteschlange.



| Eingabe | Wert |
|-------------------|--------------------------------------|
| CN                | Print-Queue                          |
| LDAP-Display-Name | Print Queue                           |
| Berechtigung aktualisieren  | Jeder kann dieses Objekt aktualisieren.       |
| Aktualisierungshäufigkeit  | \-                                   |
| Schema-ID-GUID    | bf967aa8-0de6-11d0-a285-00aa003049e2 |



## <a name="implementations"></a>Implementierungen

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server

-   [Attribute](#windows-2000-server-attributes)



| Eingabe | Wert |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | False                                                                                                                                                                |
| Object-Category             | 1                                                                                                                                                                    |
| Default-Object-Category     | \-                                                                                                                                                                   |
| Governs-Id                  | 1.2.840.113556.1.5.23                                                                                                                                                |
| Standard-ausblenden-Wert        | 0                                                                                                                                                                    |
| RDN-ATT-ID                  | [**Gemeinsamer Name**](a-cn.md)<br/>                                                                                                                               |
| Unterklasse von                 | [**Verbindungspunkt**](c-connectionpoint.md)<br/>                                                                                                             |
| Mögliche Vorgesetzten          | [**Computer**](c-computer.md)[**Container**](c-container.md)[**Domäne-DNS**](c-domaindns.md)-[**Organisationseinheit**](c-organizationalunit.md)                   |
| Zusätzlich           | \-                                                                                                                                                                   |
| NT-Security-Descriptor      | o:Bag: schlecht: S:                                                                                                                                                         |
| Standard Sicherheits Beschreibung | D: (A;; rpwpcrccdclclorcwowdsddtsw;;;D a) (a;; Rpwpcrccdclclorcwowdsddtsw;;; SY) (A;; Rpwpcrccdclclorcwowdsddtsw;;; PO) (A;; Rpwpcrccdclclorcwowdsddtsw;;; Co) (A;; Rplclorc;;; Thaus |
| System-Flags                | 0x00000010                                                                                                                                                           |



## <a name="windows-2000-server-attributes"></a>Windows 2000-Server Attribute

Diese Klasse enthält die folgenden Attribute für Windows 2000 Server:



| Attribut                                                                 | Obligatorisch. | Abgeleitet von                                                                             |
|---------------------------------------------------------------------------|-----------|------------------------------------------------------------------------------------------|
| [**Administrator: Beschreibung**](a-admindescription.md)                           | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Administrator-Anzeige Name**](a-admindisplayname.md)                          | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Zulässige Attribute**](a-allowedattributes.md)                         | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Zulässige Attribute-gültig**](a-allowedattributeseffective.md)      | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Zulässige, untergeordnete Klassen**](a-allowedchildclasses.md)                    | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Zulässig-untergeordnete Klassen-gültig**](a-allowedchildclasseseffective.md) | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Assetnummer**](a-assetnumber.md)                                     | False     | **Druck Warteschlange**                                                                          |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)             | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Bytes pro Minute**](a-bytesperminute.md)                              | False     | **Druck Warteschlange**                                                                          |
| [**Kanonischer Name**](a-canonicalname.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Gemeinsamer Name**](a-cn.md)                                               | Richtig      | [**Verbindungspunkt**](c-connectionpoint.md)<br/> [**Nach oben**](c-top.md)<br/> |
| [**Create-Zeitstempel**](a-createtimestamp.md)                            | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Standard-Priorität**](a-defaultpriority.md)                             | False     | **Druck Warteschlange**                                                                          |
| [**Beschreibung**](a-description.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Anzeige Name**](a-displayname.md)                                     | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Anzeige Name-druckdruck**](a-displaynameprintable.md)                  | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Treiber Name**](a-drivername.md)                                       | False     | **Druck Warteschlange**                                                                          |
| [**Treiber Version**](a-driverversion.md)                                 | False     | **Druck Warteschlange**                                                                          |
| [**DSA-Signatur**](a-dsasignature.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**DS-Core-propagierungs Daten**](a-dscorepropagationdata.md)               | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Erweiterungs Name**](a-extensionname.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Fahren**](a-flags.md)                                                  | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Aus-Eintrag**](a-fromentry.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)             | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                 | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**"F"-Rollen Besitzer**](a-fsmoroleowner.md)                                | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Instanztyp**](a-instancetype.md)                                   | Richtig      | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Is-critical-System-Object**](a-iscriticalsystemobject.md)             | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Ist-gelöscht**](a-isdeleted.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Is-Member-of-DL**](a-memberof.md)                                     | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Is-Privilege-Inhaber**](a-isprivilegeholder.md)                        | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Keywords**](a-keywords.md)                                            | False     | [**Verbindungspunkt**](c-connectionpoint.md)<br/>                                 |
| [**Letztes-bekannt/übergeordnetes Element**](a-lastknownparent.md)                            | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Hotels**](a-location.md)                                            | False     | **Druck Warteschlange**                                                                          |
| [**Verwaltet von**](a-managedby.md)                                         | False     | [**Verbindungspunkt**](c-connectionpoint.md)<br/>                                 |
| [**Verwaltete Objekte**](a-managedobjects.md)                               | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Verwaltet von**](a-masteredby.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Modify-Zeitstempel**](a-modifytimestamp.md)                            | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**MS-DS-Konsistenz-untergeordnet-Anzahl**](a-ms-ds-consistencychildcount.md)    | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                 | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**NetBoot-SCP-BL**](a-netbootscpbl.md)                                  | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Nicht sicherheitsmitglied-BL**](a-nonsecuritymemberbl.md)                   | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                  | Richtig      | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Obj-Dist-Name**](a-distinguishedname.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Objekt-Kategorie**](a-objectcategory.md)                               | Richtig      | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Object-Klasse**](a-objectclass.md)                                     | Richtig      | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Objekt-GUID**](a-objectguid.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Objekt-Version**](a-objectversion.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Betriebs System**](a-operatingsystem.md)                             | False     | **Druck Warteschlange**                                                                          |
| [**Betriebs System-Hotfix**](a-operatingsystemhotfix.md)                | False     | **Druck Warteschlange**                                                                          |
| [**Betriebs System-Service Pack**](a-operatingsystemservicepack.md)     | False     | **Druck Warteschlange**                                                                          |
| [**Betriebs System Version**](a-operatingsystemversion.md)              | False     | **Druck Warteschlange**                                                                          |
| [**Andere-bekannte Objekte**](a-otherwellknownobjects.md)               | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Partial-Attribute-löschen-List**](a-partialattributedeletionlist.md) | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Partiell-Attribut Satz**](a-partialattributeset.md)                    | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Physical-Location-Object**](a-physicallocationobject.md)              | False     | **Druck Warteschlange**                                                                          |
| [**Portname**](a-portname.md)                                           | False     | **Druck Warteschlange**                                                                          |
| [**Mögliche-minderwertig**](a-possibleinferiors.md)                         | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Print-Attribute**](a-printattributes.md)                             | False     | **Druck Warteschlange**                                                                          |
| [**Print-bin-Names**](a-printbinnames.md)                                | False     | **Druck Warteschlange**                                                                          |
| [**Drucken-COLLATE**](a-printcollate.md)                                   | False     | **Druck Warteschlange**                                                                          |
| [**Druckfarbe**](a-printcolor.md)                                       | False     | **Druck Warteschlange**                                                                          |
| [**Print-Duplex-unterstützt**](a-printduplexsupported.md)                  | False     | **Druck Warteschlange**                                                                          |
| [**Druck-Endzeit**](a-printendtime.md)                                  | False     | **Druck Warteschlange**                                                                          |
| [**Drucker Name**](a-printername.md)                                     | Richtig      | **Druck Warteschlange**                                                                          |
| [**Print-Formular Name**](a-printformname.md)                                | False     | **Druck Warteschlange**                                                                          |
| [**Print-Keep-Print-Jobs**](a-printkeepprintedjobs.md)                 | False     | **Druck Warteschlange**                                                                          |
| [**Druck Sprache**](a-printlanguage.md)                                 | False     | **Druck Warteschlange**                                                                          |
| [**Print-Mac-Adresse**](a-printmacaddress.md)                            | False     | **Druck Warteschlange**                                                                          |
| [**Print-Max-Kopien**](a-printmaxcopies.md)                              | False     | **Druck Warteschlange**                                                                          |
| [**Print-Max-Resolution wird unterstützt**](a-printmaxresolutionsupported.md)   | False     | **Druck Warteschlange**                                                                          |
| [**Print-Max-X-Block**](a-printmaxxextent.md)                           | False     | **Druck Warteschlange**                                                                          |
| [**Print-Max-Y-Block**](a-printmaxyextent.md)                           | False     | **Druck Warteschlange**                                                                          |
| [**Druck Medien-bereit**](a-printmediaready.md)                            | False     | **Druck Warteschlange**                                                                          |
| [**Print-Media-supported**](a-printmediasupported.md)                    | False     | **Druck Warteschlange**                                                                          |
| [**Druck-Arbeitsspeicher**](a-printmemory.md)                                     | False     | **Druck Warteschlange**                                                                          |
| [**Print-min-X-Block**](a-printminxextent.md)                           | False     | **Druck Warteschlange**                                                                          |
| [**Druck-min-Y-Block**](a-printminyextent.md)                           | False     | **Druck Warteschlange**                                                                          |
| [**Print-Network-Address**](a-printnetworkaddress.md)                    | False     | **Druck Warteschlange**                                                                          |
| [**Druck Benachrichtigung**](a-printnotify.md)                                     | False     | **Druck Warteschlange**                                                                          |
| [**Print-Number-up**](a-printnumberup.md)                                | False     | **Druck Warteschlange**                                                                          |
| [**Print-Ausrichtungen-unterstützt**](a-printorientationssupported.md)      | False     | **Druck Warteschlange**                                                                          |
| [**Druck Besitzer**](a-printowner.md)                                       | False     | **Druck Warteschlange**                                                                          |
| [**Druckseiten pro Minute**](a-printpagesperminute.md)                   | False     | **Druck Warteschlange**                                                                          |
| [**Druck Rate**](a-printrate.md)                                         | False     | **Druck Warteschlange**                                                                          |
| [**Druck Raten Einheit**](a-printrateunit.md)                                | False     | **Druck Warteschlange**                                                                          |
| [**Druck Trennzeichen-Datei**](a-printseparatorfile.md)                      | False     | **Druck Warteschlange**                                                                          |
| [**Druckfreigabe Name**](a-printsharename.md)                              | False     | **Druck Warteschlange**                                                                          |
| [**Druck Spoolvorgang**](a-printspooling.md)                                 | False     | **Druck Warteschlange**                                                                          |
| [**Print-Stapling-supported**](a-printstaplingsupported.md)              | False     | **Druck Warteschlange**                                                                          |
| [**Druck-Startzeit**](a-printstarttime.md)                              | False     | **Druck Warteschlange**                                                                          |
| [**Druck Status**](a-printstatus.md)                                     | False     | **Druck Warteschlange**                                                                          |
| [**Priorität**](a-priority.md)                                            | False     | **Druck Warteschlange**                                                                          |
| [**Proxy-Objekt Name**](a-proxiedobjectname.md)                        | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Proxy Adressen**](a-proxyaddresses.md)                               | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Abfrage-Richtlinie-BL**](a-querypolicybl.md)                                | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**RDN**](a-name.md)                                                     | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                 | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**REPL-Update-Vector**](a-repluptodatevector.md)                      | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Berichte**](a-directreports.md)                                        | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Reps-from**](a-repsfrom.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Reps-to**](a-repsto.md)                                               | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Novel**](a-revision.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**SD-Rechte**](a-sdrightseffective.md)                        | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Server Name**](a-servername.md)                                       | Richtig      | **Druck Warteschlange**                                                                          |
| [**Server-Reference-BL**](a-serverreferencebl.md)                        | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Short-Server-Name**](a-shortservername.md)                            | Richtig      | **Druck Warteschlange**                                                                          |
| [**Anzeigen-in-Advanced-nur anzeigen**](a-showinadvancedviewonly.md)            | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Site-Object-BL**](a-siteobjectbl.md)                                  | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Sub-Refs**](a-subrefs.md)                                             | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Subschemasubentry**](a-subschemasubentry.md)                          | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**SystemFlags**](a-systemflags.md)                                     | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**UNC-Name**](a-uncname.md)                                             | Richtig      | **Druck Warteschlange**                                                                          |
| [**Die Anwendung wurde geändert.**](a-usnchanged.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Von der Anwendung erstellte**](a-usncreated.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**USA-DSA-letzte-obj-entfernt**](a-usndsalastobjremoved.md)                | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Standort-und standortübergreifende standortübergreifende**](a-usnintersite.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**"An-Last-obj-REM"**](a-usnlastobjrem.md)                               | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Quell Code Quelle**](a-usnsource.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Versionsnummer**](a-versionnumber.md)                                 | Richtig      | **Druck Warteschlange**                                                                          |
| [**WBEM-Pfad**](a-wbempath.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Bekannte Objekte**](a-wellknownobjects.md)                          | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Bei Änderung**](a-whenchanged.md)                                     | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Bei Erstellung**](a-whencreated.md)                                     | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**WWW-Homepage**](a-wwwhomepage.md)                                    | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**WWW-Page-other**](a-url.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                                                          |



## <a name="windows-server-2003"></a>Windows Server 2003

-   [Attribute](#windows-server-2003-attributes)



| Eingabe | Wert |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | False                                                                                                                                                                |
| Object-Category             | 1                                                                                                                                                                    |
| Default-Object-Category     | \-                                                                                                                                                                   |
| Governs-Id                  | 1.2.840.113556.1.5.23                                                                                                                                                |
| Standard-ausblenden-Wert        | 0                                                                                                                                                                    |
| RDN-ATT-ID                  | [**Gemeinsamer Name**](a-cn.md)<br/>                                                                                                                               |
| Unterklasse von                 | [**Verbindungspunkt**](c-connectionpoint.md)<br/>                                                                                                             |
| Mögliche Vorgesetzten          | [**Computer**](c-computer.md)[**Container**](c-container.md)[**Domäne-DNS**](c-domaindns.md)-[**Organisationseinheit**](c-organizationalunit.md)                   |
| Zusätzlich           | \-                                                                                                                                                                   |
| NT-Security-Descriptor      | o:Bag: schlecht: S:                                                                                                                                                         |
| Standard Sicherheits Beschreibung | D: (A;; rpwpcrccdclclorcwowdsddtsw;;;D a) (a;; Rpwpcrccdclclorcwowdsddtsw;;; SY) (A;; Rpwpcrccdclclorcwowdsddtsw;;; PO) (A;; Rpwpcrccdclclorcwowdsddtsw;;; Co) (A;; Rplclorc;;; Thaus |
| System-Flags                | 0x00000010                                                                                                                                                           |



## <a name="windows-server-2003-attributes"></a>Windows Server 2003-Attribute

Diese Klasse enthält die folgenden Attribute für Windows Server 2003:



| Attribut                                                                   | Obligatorisch. | Abgeleitet von                                                                             |
|-----------------------------------------------------------------------------|-----------|------------------------------------------------------------------------------------------|
| [**Administrator: Beschreibung**](a-admindescription.md)                             | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Administrator-Anzeige Name**](a-admindisplayname.md)                            | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Zulässige Attribute**](a-allowedattributes.md)                           | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Zulässige Attribute-gültig**](a-allowedattributeseffective.md)        | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Zulässige, untergeordnete Klassen**](a-allowedchildclasses.md)                      | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Zulässig-untergeordnete Klassen-gültig**](a-allowedchildclasseseffective.md)   | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Assetnummer**](a-assetnumber.md)                                       | False     | **Druck Warteschlange**                                                                          |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)               | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Bytes pro Minute**](a-bytesperminute.md)                                | False     | **Druck Warteschlange**                                                                          |
| [**Kanonischer Name**](a-canonicalname.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Gemeinsamer Name**](a-cn.md)                                                 | Richtig      | [**Verbindungspunkt**](c-connectionpoint.md)<br/> [**Nach oben**](c-top.md)<br/> |
| [**Create-Zeitstempel**](a-createtimestamp.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Standard-Priorität**](a-defaultpriority.md)                               | False     | **Druck Warteschlange**                                                                          |
| [**Beschreibung**](a-description.md)                                        | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Anzeige Name**](a-displayname.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Anzeige Name-druckdruck**](a-displaynameprintable.md)                    | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Treiber Name**](a-drivername.md)                                         | False     | **Druck Warteschlange**                                                                          |
| [**Treiber Version**](a-driverversion.md)                                   | False     | **Druck Warteschlange**                                                                          |
| [**DSA-Signatur**](a-dsasignature.md)                                     | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**DS-Core-propagierungs Daten**](a-dscorepropagationdata.md)                 | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Erweiterungs Name**](a-extensionname.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Fahren**](a-flags.md)                                                    | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Aus-Eintrag**](a-fromentry.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)               | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                   | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**"F"-Rollen Besitzer**](a-fsmoroleowner.md)                                  | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Instanztyp**](a-instancetype.md)                                     | Richtig      | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Is-critical-System-Object**](a-iscriticalsystemobject.md)               | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Ist-gelöscht**](a-isdeleted.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Is-Member-of-DL**](a-memberof.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Is-Privilege-Inhaber**](a-isprivilegeholder.md)                          | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Keywords**](a-keywords.md)                                              | False     | [**Verbindungspunkt**](c-connectionpoint.md)<br/>                                 |
| [**Letztes-bekannt/übergeordnetes Element**](a-lastknownparent.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Hotels**](a-location.md)                                              | False     | **Druck Warteschlange**                                                                          |
| [**Verwaltet von**](a-managedby.md)                                           | False     | [**Verbindungspunkt**](c-connectionpoint.md)<br/>                                 |
| [**Verwaltete Objekte**](a-managedobjects.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Verwaltet von**](a-masteredby.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Modify-Zeitstempel**](a-modifytimestamp.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**MS-com-partitionsetlink**](a-mscom-partitionsetlink.md)                 | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**MS-com-userlink**](a-mscom-userlink.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-ca-immed-untergeordnete Elemente**](a-msds-approx-immed-subordinates.md) | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**MS-DS-Konsistenz-untergeordnet-Anzahl**](a-ms-ds-consistencychildcount.md)      | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-gemastert von**](a-msds-masteredby.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Members-für-AZ-Role-BL**](a-msds-membersforazrolebl.md)           | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-repl-Cursor**](a-msds-ncreplcursors.md)                       | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-repl-Inbound-Nachbarn**](a-msds-ncreplinboundneighbors.md)    | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-repl-Outbound-Nachbarn**](a-msds-ncreploutboundneighbors.md)  | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                         | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)               | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)     | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)     | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)      | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)              | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Settings**](a-msds-settings.md)                                   | False     | [**Verbindungspunkt**](c-connectionpoint.md)<br/>                                 |
| [**ms-DS-Tasks-für-AZ-Role-BL**](a-msds-tasksforazrolebl.md)               | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Tasks-für-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)               | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**NetBoot-SCP-BL**](a-netbootscpbl.md)                                    | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Nicht sicherheitsmitglied-BL**](a-nonsecuritymemberbl.md)                     | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                    | Richtig      | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Objekt-Kategorie**](a-objectcategory.md)                                 | Richtig      | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Object-Klasse**](a-objectclass.md)                                       | Richtig      | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Objekt-GUID**](a-objectguid.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Objekt-Version**](a-objectversion.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Betriebs System**](a-operatingsystem.md)                               | False     | **Druck Warteschlange**                                                                          |
| [**Betriebs System-Hotfix**](a-operatingsystemhotfix.md)                  | False     | **Druck Warteschlange**                                                                          |
| [**Betriebs System-Service Pack**](a-operatingsystemservicepack.md)       | False     | **Druck Warteschlange**                                                                          |
| [**Betriebs System Version**](a-operatingsystemversion.md)                | False     | **Druck Warteschlange**                                                                          |
| [**Andere-bekannte Objekte**](a-otherwellknownobjects.md)                 | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Partial-Attribute-löschen-List**](a-partialattributedeletionlist.md)   | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Partiell-Attribut Satz**](a-partialattributeset.md)                      | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Physical-Location-Object**](a-physicallocationobject.md)                | False     | **Druck Warteschlange**                                                                          |
| [**Portname**](a-portname.md)                                             | False     | **Druck Warteschlange**                                                                          |
| [**Mögliche-minderwertig**](a-possibleinferiors.md)                           | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Print-Attribute**](a-printattributes.md)                               | False     | **Druck Warteschlange**                                                                          |
| [**Print-bin-Names**](a-printbinnames.md)                                  | False     | **Druck Warteschlange**                                                                          |
| [**Drucken-COLLATE**](a-printcollate.md)                                     | False     | **Druck Warteschlange**                                                                          |
| [**Druckfarbe**](a-printcolor.md)                                         | False     | **Druck Warteschlange**                                                                          |
| [**Print-Duplex-unterstützt**](a-printduplexsupported.md)                    | False     | **Druck Warteschlange**                                                                          |
| [**Druck-Endzeit**](a-printendtime.md)                                    | False     | **Druck Warteschlange**                                                                          |
| [**Drucker Name**](a-printername.md)                                       | Richtig      | **Druck Warteschlange**                                                                          |
| [**Print-Formular Name**](a-printformname.md)                                  | False     | **Druck Warteschlange**                                                                          |
| [**Print-Keep-Print-Jobs**](a-printkeepprintedjobs.md)                   | False     | **Druck Warteschlange**                                                                          |
| [**Druck Sprache**](a-printlanguage.md)                                   | False     | **Druck Warteschlange**                                                                          |
| [**Print-Mac-Adresse**](a-printmacaddress.md)                              | False     | **Druck Warteschlange**                                                                          |
| [**Print-Max-Kopien**](a-printmaxcopies.md)                                | False     | **Druck Warteschlange**                                                                          |
| [**Print-Max-Resolution wird unterstützt**](a-printmaxresolutionsupported.md)     | False     | **Druck Warteschlange**                                                                          |
| [**Print-Max-X-Block**](a-printmaxxextent.md)                             | False     | **Druck Warteschlange**                                                                          |
| [**Print-Max-Y-Block**](a-printmaxyextent.md)                             | False     | **Druck Warteschlange**                                                                          |
| [**Druck Medien-bereit**](a-printmediaready.md)                              | False     | **Druck Warteschlange**                                                                          |
| [**Print-Media-supported**](a-printmediasupported.md)                      | False     | **Druck Warteschlange**                                                                          |
| [**Druck-Arbeitsspeicher**](a-printmemory.md)                                       | False     | **Druck Warteschlange**                                                                          |
| [**Print-min-X-Block**](a-printminxextent.md)                             | False     | **Druck Warteschlange**                                                                          |
| [**Druck-min-Y-Block**](a-printminyextent.md)                             | False     | **Druck Warteschlange**                                                                          |
| [**Print-Network-Address**](a-printnetworkaddress.md)                      | False     | **Druck Warteschlange**                                                                          |
| [**Druck Benachrichtigung**](a-printnotify.md)                                       | False     | **Druck Warteschlange**                                                                          |
| [**Print-Number-up**](a-printnumberup.md)                                  | False     | **Druck Warteschlange**                                                                          |
| [**Print-Ausrichtungen-unterstützt**](a-printorientationssupported.md)        | False     | **Druck Warteschlange**                                                                          |
| [**Druck Besitzer**](a-printowner.md)                                         | False     | **Druck Warteschlange**                                                                          |
| [**Druckseiten pro Minute**](a-printpagesperminute.md)                     | False     | **Druck Warteschlange**                                                                          |
| [**Druck Rate**](a-printrate.md)                                           | False     | **Druck Warteschlange**                                                                          |
| [**Druck Raten Einheit**](a-printrateunit.md)                                  | False     | **Druck Warteschlange**                                                                          |
| [**Druck Trennzeichen-Datei**](a-printseparatorfile.md)                        | False     | **Druck Warteschlange**                                                                          |
| [**Druckfreigabe Name**](a-printsharename.md)                                | False     | **Druck Warteschlange**                                                                          |
| [**Druck Spoolvorgang**](a-printspooling.md)                                   | False     | **Druck Warteschlange**                                                                          |
| [**Print-Stapling-supported**](a-printstaplingsupported.md)                | False     | **Druck Warteschlange**                                                                          |
| [**Druck-Startzeit**](a-printstarttime.md)                                | False     | **Druck Warteschlange**                                                                          |
| [**Druck Status**](a-printstatus.md)                                       | False     | **Druck Warteschlange**                                                                          |
| [**Priorität**](a-priority.md)                                              | False     | **Druck Warteschlange**                                                                          |
| [**Proxy-Objekt Name**](a-proxiedobjectname.md)                          | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Proxy Adressen**](a-proxyaddresses.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Abfrage-Richtlinie-BL**](a-querypolicybl.md)                                  | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**RDN**](a-name.md)                                                       | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                   | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**REPL-Update-Vector**](a-repluptodatevector.md)                        | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Berichte**](a-directreports.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Reps-from**](a-repsfrom.md)                                             | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Reps-to**](a-repsto.md)                                                 | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Novel**](a-revision.md)                                              | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**SD-Rechte**](a-sdrightseffective.md)                          | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Server Name**](a-servername.md)                                         | Richtig      | **Druck Warteschlange**                                                                          |
| [**Server-Reference-BL**](a-serverreferencebl.md)                          | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Short-Server-Name**](a-shortservername.md)                              | Richtig      | **Druck Warteschlange**                                                                          |
| [**Anzeigen-in-Advanced-nur anzeigen**](a-showinadvancedviewonly.md)              | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Struktur-Objekt-Klasse**](a-structuralobjectclass.md)                  | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Sub-Refs**](a-subrefs.md)                                               | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Subschemasubentry**](a-subschemasubentry.md)                            | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**SystemFlags**](a-systemflags.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**UNC-Name**](a-uncname.md)                                               | Richtig      | **Druck Warteschlange**                                                                          |
| [**Die Anwendung wurde geändert.**](a-usnchanged.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Von der Anwendung erstellte**](a-usncreated.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**USA-DSA-letzte-obj-entfernt**](a-usndsalastobjremoved.md)                  | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Standort-und standortübergreifende standortübergreifende**](a-usnintersite.md)                                     | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**"An-Last-obj-REM"**](a-usnlastobjrem.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Quell Code Quelle**](a-usnsource.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Versionsnummer**](a-versionnumber.md)                                   | Richtig      | **Druck Warteschlange**                                                                          |
| [**WBEM-Pfad**](a-wbempath.md)                                             | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Bekannte Objekte**](a-wellknownobjects.md)                            | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Bei Änderung**](a-whenchanged.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Bei Erstellung**](a-whencreated.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**WWW-Homepage**](a-wwwhomepage.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**WWW-Page-other**](a-url.md)                                             | False     | [**Nach oben**](c-top.md)<br/>                                                          |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2

-   [Attribute](#windows-server-2003-r2-attributes)



| Eingabe | Wert |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | False                                                                                                                                                                |
| Object-Category             | 1                                                                                                                                                                    |
| Default-Object-Category     | \-                                                                                                                                                                   |
| Governs-Id                  | 1.2.840.113556.1.5.23                                                                                                                                                |
| Standard-ausblenden-Wert        | 0                                                                                                                                                                    |
| RDN-ATT-ID                  | [**Gemeinsamer Name**](a-cn.md)<br/>                                                                                                                               |
| Unterklasse von                 | [**Verbindungspunkt**](c-connectionpoint.md)<br/>                                                                                                             |
| Mögliche Vorgesetzten          | [**Computer**](c-computer.md)[**Container**](c-container.md)[**Domäne-DNS**](c-domaindns.md)-[**Organisationseinheit**](c-organizationalunit.md)                   |
| Zusätzlich           | \-                                                                                                                                                                   |
| NT-Security-Descriptor      | o:Bag: schlecht: S:                                                                                                                                                         |
| Standard Sicherheits Beschreibung | D: (A;; rpwpcrccdclclorcwowdsddtsw;;;D a) (a;; Rpwpcrccdclclorcwowdsddtsw;;; SY) (A;; Rpwpcrccdclclorcwowdsddtsw;;; PO) (A;; Rpwpcrccdclclorcwowdsddtsw;;; Co) (A;; Rplclorc;;; Thaus |
| System-Flags                | 0x00000010                                                                                                                                                           |



## <a name="windows-server-2003-r2-attributes"></a>Windows Server 2003 R2-Attribute

Diese Klasse enthält die folgenden Attribute für Windows Server 2003 R2:



| Attribut                                                                   | Obligatorisch. | Abgeleitet von                                                                             |
|-----------------------------------------------------------------------------|-----------|------------------------------------------------------------------------------------------|
| [**Administrator: Beschreibung**](a-admindescription.md)                             | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Administrator-Anzeige Name**](a-admindisplayname.md)                            | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Zulässige Attribute**](a-allowedattributes.md)                           | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Zulässige Attribute-gültig**](a-allowedattributeseffective.md)        | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Zulässige, untergeordnete Klassen**](a-allowedchildclasses.md)                      | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Zulässig-untergeordnete Klassen-gültig**](a-allowedchildclasseseffective.md)   | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Assetnummer**](a-assetnumber.md)                                       | False     | **Druck Warteschlange**                                                                          |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)               | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Bytes pro Minute**](a-bytesperminute.md)                                | False     | **Druck Warteschlange**                                                                          |
| [**Kanonischer Name**](a-canonicalname.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Gemeinsamer Name**](a-cn.md)                                                 | Richtig      | [**Verbindungspunkt**](c-connectionpoint.md)<br/> [**Nach oben**](c-top.md)<br/> |
| [**Create-Zeitstempel**](a-createtimestamp.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Standard-Priorität**](a-defaultpriority.md)                               | False     | **Druck Warteschlange**                                                                          |
| [**Beschreibung**](a-description.md)                                        | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Anzeige Name**](a-displayname.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Anzeige Name-druckdruck**](a-displaynameprintable.md)                    | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Treiber Name**](a-drivername.md)                                         | False     | **Druck Warteschlange**                                                                          |
| [**Treiber Version**](a-driverversion.md)                                   | False     | **Druck Warteschlange**                                                                          |
| [**DSA-Signatur**](a-dsasignature.md)                                     | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**DS-Core-propagierungs Daten**](a-dscorepropagationdata.md)                 | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Erweiterungs Name**](a-extensionname.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Fahren**](a-flags.md)                                                    | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Aus-Eintrag**](a-fromentry.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)               | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                   | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**"F"-Rollen Besitzer**](a-fsmoroleowner.md)                                  | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Instanztyp**](a-instancetype.md)                                     | Richtig      | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Is-critical-System-Object**](a-iscriticalsystemobject.md)               | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Ist-gelöscht**](a-isdeleted.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Is-Member-of-DL**](a-memberof.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Is-Privilege-Inhaber**](a-isprivilegeholder.md)                          | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Keywords**](a-keywords.md)                                              | False     | [**Verbindungspunkt**](c-connectionpoint.md)<br/>                                 |
| [**Letztes-bekannt/übergeordnetes Element**](a-lastknownparent.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Hotels**](a-location.md)                                              | False     | **Druck Warteschlange**                                                                          |
| [**Verwaltet von**](a-managedby.md)                                           | False     | [**Verbindungspunkt**](c-connectionpoint.md)<br/>                                 |
| [**Verwaltete Objekte**](a-managedobjects.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Verwaltet von**](a-masteredby.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Modify-Zeitstempel**](a-modifytimestamp.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**MS-com-partitionsetlink**](a-mscom-partitionsetlink.md)                 | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**MS-com-userlink**](a-mscom-userlink.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**MS-DFSR-computerreferencebl**](a-msdfsr-computerreferencebl.md)         | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**MS-DFSR-mitgliedreferencebl**](a-msdfsr-memberreferencebl.md)             | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-ca-immed-untergeordnete Elemente**](a-msds-approx-immed-subordinates.md) | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**MS-DS-Konsistenz-untergeordnet-Anzahl**](a-ms-ds-consistencychildcount.md)      | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-gemastert von**](a-msds-masteredby.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Members-für-AZ-Role-BL**](a-msds-membersforazrolebl.md)           | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-repl-Cursor**](a-msds-ncreplcursors.md)                       | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-repl-Inbound-Nachbarn**](a-msds-ncreplinboundneighbors.md)    | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-repl-Outbound-Nachbarn**](a-msds-ncreploutboundneighbors.md)  | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                         | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)               | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)     | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)     | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)      | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)              | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Settings**](a-msds-settings.md)                                   | False     | [**Verbindungspunkt**](c-connectionpoint.md)<br/>                                 |
| [**ms-DS-Tasks-für-AZ-Role-BL**](a-msds-tasksforazrolebl.md)               | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Tasks-für-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)               | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**msSFU-30-POSIX-Member-of**](a-mssfu30posixmemberof.md)                  | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**NetBoot-SCP-BL**](a-netbootscpbl.md)                                    | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Nicht sicherheitsmitglied-BL**](a-nonsecuritymemberbl.md)                     | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                    | Richtig      | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Objekt-Kategorie**](a-objectcategory.md)                                 | Richtig      | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Object-Klasse**](a-objectclass.md)                                       | Richtig      | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Objekt-GUID**](a-objectguid.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Objekt-Version**](a-objectversion.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Betriebs System**](a-operatingsystem.md)                               | False     | **Druck Warteschlange**                                                                          |
| [**Betriebs System-Hotfix**](a-operatingsystemhotfix.md)                  | False     | **Druck Warteschlange**                                                                          |
| [**Betriebs System-Service Pack**](a-operatingsystemservicepack.md)       | False     | **Druck Warteschlange**                                                                          |
| [**Betriebs System Version**](a-operatingsystemversion.md)                | False     | **Druck Warteschlange**                                                                          |
| [**Andere-bekannte Objekte**](a-otherwellknownobjects.md)                 | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Partial-Attribute-löschen-List**](a-partialattributedeletionlist.md)   | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Partiell-Attribut Satz**](a-partialattributeset.md)                      | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Physical-Location-Object**](a-physicallocationobject.md)                | False     | **Druck Warteschlange**                                                                          |
| [**Portname**](a-portname.md)                                             | False     | **Druck Warteschlange**                                                                          |
| [**Mögliche-minderwertig**](a-possibleinferiors.md)                           | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Print-Attribute**](a-printattributes.md)                               | False     | **Druck Warteschlange**                                                                          |
| [**Print-bin-Names**](a-printbinnames.md)                                  | False     | **Druck Warteschlange**                                                                          |
| [**Drucken-COLLATE**](a-printcollate.md)                                     | False     | **Druck Warteschlange**                                                                          |
| [**Druckfarbe**](a-printcolor.md)                                         | False     | **Druck Warteschlange**                                                                          |
| [**Print-Duplex-unterstützt**](a-printduplexsupported.md)                    | False     | **Druck Warteschlange**                                                                          |
| [**Druck-Endzeit**](a-printendtime.md)                                    | False     | **Druck Warteschlange**                                                                          |
| [**Drucker Name**](a-printername.md)                                       | Richtig      | **Druck Warteschlange**                                                                          |
| [**Print-Formular Name**](a-printformname.md)                                  | False     | **Druck Warteschlange**                                                                          |
| [**Print-Keep-Print-Jobs**](a-printkeepprintedjobs.md)                   | False     | **Druck Warteschlange**                                                                          |
| [**Druck Sprache**](a-printlanguage.md)                                   | False     | **Druck Warteschlange**                                                                          |
| [**Print-Mac-Adresse**](a-printmacaddress.md)                              | False     | **Druck Warteschlange**                                                                          |
| [**Print-Max-Kopien**](a-printmaxcopies.md)                                | False     | **Druck Warteschlange**                                                                          |
| [**Print-Max-Resolution wird unterstützt**](a-printmaxresolutionsupported.md)     | False     | **Druck Warteschlange**                                                                          |
| [**Print-Max-X-Block**](a-printmaxxextent.md)                             | False     | **Druck Warteschlange**                                                                          |
| [**Print-Max-Y-Block**](a-printmaxyextent.md)                             | False     | **Druck Warteschlange**                                                                          |
| [**Druck Medien-bereit**](a-printmediaready.md)                              | False     | **Druck Warteschlange**                                                                          |
| [**Print-Media-supported**](a-printmediasupported.md)                      | False     | **Druck Warteschlange**                                                                          |
| [**Druck-Arbeitsspeicher**](a-printmemory.md)                                       | False     | **Druck Warteschlange**                                                                          |
| [**Print-min-X-Block**](a-printminxextent.md)                             | False     | **Druck Warteschlange**                                                                          |
| [**Druck-min-Y-Block**](a-printminyextent.md)                             | False     | **Druck Warteschlange**                                                                          |
| [**Print-Network-Address**](a-printnetworkaddress.md)                      | False     | **Druck Warteschlange**                                                                          |
| [**Druck Benachrichtigung**](a-printnotify.md)                                       | False     | **Druck Warteschlange**                                                                          |
| [**Print-Number-up**](a-printnumberup.md)                                  | False     | **Druck Warteschlange**                                                                          |
| [**Print-Ausrichtungen-unterstützt**](a-printorientationssupported.md)        | False     | **Druck Warteschlange**                                                                          |
| [**Druck Besitzer**](a-printowner.md)                                         | False     | **Druck Warteschlange**                                                                          |
| [**Druckseiten pro Minute**](a-printpagesperminute.md)                     | False     | **Druck Warteschlange**                                                                          |
| [**Druck Rate**](a-printrate.md)                                           | False     | **Druck Warteschlange**                                                                          |
| [**Druck Raten Einheit**](a-printrateunit.md)                                  | False     | **Druck Warteschlange**                                                                          |
| [**Druck Trennzeichen-Datei**](a-printseparatorfile.md)                        | False     | **Druck Warteschlange**                                                                          |
| [**Druckfreigabe Name**](a-printsharename.md)                                | False     | **Druck Warteschlange**                                                                          |
| [**Druck Spoolvorgang**](a-printspooling.md)                                   | False     | **Druck Warteschlange**                                                                          |
| [**Print-Stapling-supported**](a-printstaplingsupported.md)                | False     | **Druck Warteschlange**                                                                          |
| [**Druck-Startzeit**](a-printstarttime.md)                                | False     | **Druck Warteschlange**                                                                          |
| [**Druck Status**](a-printstatus.md)                                       | False     | **Druck Warteschlange**                                                                          |
| [**Priorität**](a-priority.md)                                              | False     | **Druck Warteschlange**                                                                          |
| [**Proxy-Objekt Name**](a-proxiedobjectname.md)                          | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Proxy Adressen**](a-proxyaddresses.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Abfrage-Richtlinie-BL**](a-querypolicybl.md)                                  | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**RDN**](a-name.md)                                                       | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                   | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**REPL-Update-Vector**](a-repluptodatevector.md)                        | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Berichte**](a-directreports.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Reps-from**](a-repsfrom.md)                                             | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Reps-to**](a-repsto.md)                                                 | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Novel**](a-revision.md)                                              | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**SD-Rechte**](a-sdrightseffective.md)                          | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Server Name**](a-servername.md)                                         | Richtig      | **Druck Warteschlange**                                                                          |
| [**Server-Reference-BL**](a-serverreferencebl.md)                          | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Short-Server-Name**](a-shortservername.md)                              | Richtig      | **Druck Warteschlange**                                                                          |
| [**Anzeigen-in-Advanced-nur anzeigen**](a-showinadvancedviewonly.md)              | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Struktur-Objekt-Klasse**](a-structuralobjectclass.md)                  | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Sub-Refs**](a-subrefs.md)                                               | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Subschemasubentry**](a-subschemasubentry.md)                            | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**SystemFlags**](a-systemflags.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**UNC-Name**](a-uncname.md)                                               | Richtig      | **Druck Warteschlange**                                                                          |
| [**Die Anwendung wurde geändert.**](a-usnchanged.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Von der Anwendung erstellte**](a-usncreated.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**USA-DSA-letzte-obj-entfernt**](a-usndsalastobjremoved.md)                  | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Standort-und standortübergreifende standortübergreifende**](a-usnintersite.md)                                     | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**"An-Last-obj-REM"**](a-usnlastobjrem.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Quell Code Quelle**](a-usnsource.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Versionsnummer**](a-versionnumber.md)                                   | Richtig      | **Druck Warteschlange**                                                                          |
| [**WBEM-Pfad**](a-wbempath.md)                                             | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Bekannte Objekte**](a-wellknownobjects.md)                            | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Bei Änderung**](a-whenchanged.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Bei Erstellung**](a-whencreated.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**WWW-Homepage**](a-wwwhomepage.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**WWW-Page-other**](a-url.md)                                             | False     | [**Nach oben**](c-top.md)<br/>                                                          |



## <a name="windows-server-2008"></a>Windows Server 2008

-   [Attribute](#windows-server-2008-attributes)



| Eingabe | Wert |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | False                                                                                                                                                                |
| Object-Category             | 1                                                                                                                                                                    |
| Default-Object-Category     | \-                                                                                                                                                                   |
| Governs-Id                  | 1.2.840.113556.1.5.23                                                                                                                                                |
| Standard-ausblenden-Wert        | 0                                                                                                                                                                    |
| RDN-ATT-ID                  | [**Gemeinsamer Name**](a-cn.md)<br/>                                                                                                                               |
| Unterklasse von                 | [**Verbindungspunkt**](c-connectionpoint.md)<br/>                                                                                                             |
| Mögliche Vorgesetzten          | [**Computer**](c-computer.md)[**Container**](c-container.md)[**Domäne-DNS**](c-domaindns.md)-[**Organisationseinheit**](c-organizationalunit.md)                   |
| Zusätzlich           | \-                                                                                                                                                                   |
| NT-Security-Descriptor      | o:Bag: schlecht: S:                                                                                                                                                         |
| Standard Sicherheits Beschreibung | D: (A;; rpwpcrccdclclorcwowdsddtsw;;;D a) (a;; Rpwpcrccdclclorcwowdsddtsw;;; SY) (A;; Rpwpcrccdclclorcwowdsddtsw;;; PO) (A;; Rpwpcrccdclclorcwowdsddtsw;;; Co) (A;; Rplclorc;;; Thaus |
| System-Flags                | 0x00000010                                                                                                                                                           |



## <a name="windows-server-2008-attributes"></a>Windows Server 2008-Attribute

Diese Klasse enthält die folgenden Attribute für Windows Server 2008:



| Attribut                                                                      | Obligatorisch. | Abgeleitet von                                                                             |
|--------------------------------------------------------------------------------|-----------|------------------------------------------------------------------------------------------|
| [**Administrator: Beschreibung**](a-admindescription.md)                                | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Administrator-Anzeige Name**](a-admindisplayname.md)                               | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Zulässige Attribute**](a-allowedattributes.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Zulässige Attribute-gültig**](a-allowedattributeseffective.md)           | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Zulässige, untergeordnete Klassen**](a-allowedchildclasses.md)                         | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Zulässig-untergeordnete Klassen-gültig**](a-allowedchildclasseseffective.md)      | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Assetnummer**](a-assetnumber.md)                                          | False     | **Druck Warteschlange**                                                                          |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                  | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Bytes pro Minute**](a-bytesperminute.md)                                   | False     | **Druck Warteschlange**                                                                          |
| [**Kanonischer Name**](a-canonicalname.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Gemeinsamer Name**](a-cn.md)                                                    | Richtig      | [**Verbindungspunkt**](c-connectionpoint.md)<br/> [**Nach oben**](c-top.md)<br/> |
| [**Create-Zeitstempel**](a-createtimestamp.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Standard-Priorität**](a-defaultpriority.md)                                  | False     | **Druck Warteschlange**                                                                          |
| [**Beschreibung**](a-description.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Anzeige Name**](a-displayname.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Anzeige Name-druckdruck**](a-displaynameprintable.md)                       | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Treiber Name**](a-drivername.md)                                            | False     | **Druck Warteschlange**                                                                          |
| [**Treiber Version**](a-driverversion.md)                                      | False     | **Druck Warteschlange**                                                                          |
| [**DSA-Signatur**](a-dsasignature.md)                                        | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**DS-Core-propagierungs Daten**](a-dscorepropagationdata.md)                    | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Erweiterungs Name**](a-extensionname.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Fahren**](a-flags.md)                                                       | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Aus-Eintrag**](a-fromentry.md)                                              | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                  | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                      | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**"F"-Rollen Besitzer**](a-fsmoroleowner.md)                                     | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Instanztyp**](a-instancetype.md)                                        | Richtig      | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Is-critical-System-Object**](a-iscriticalsystemobject.md)                  | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Ist-gelöscht**](a-isdeleted.md)                                              | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Is-Member-of-DL**](a-memberof.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Is-Privilege-Inhaber**](a-isprivilegeholder.md)                             | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Keywords**](a-keywords.md)                                                 | False     | [**Verbindungspunkt**](c-connectionpoint.md)<br/>                                 |
| [**Letztes-bekannt/übergeordnetes Element**](a-lastknownparent.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Hotels**](a-location.md)                                                 | False     | **Druck Warteschlange**                                                                          |
| [**Verwaltet von**](a-managedby.md)                                              | False     | [**Verbindungspunkt**](c-connectionpoint.md)<br/>                                 |
| [**Verwaltete Objekte**](a-managedobjects.md)                                    | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Verwaltet von**](a-masteredby.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Modify-Zeitstempel**](a-modifytimestamp.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**MS-com-partitionsetlink**](a-mscom-partitionsetlink.md)                    | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**MS-com-userlink**](a-mscom-userlink.md)                                    | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**MS-DFSR-computerreferencebl**](a-msdfsr-computerreferencebl.md)            | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**MS-DFSR-mitgliedreferencebl**](a-msdfsr-memberreferencebl.md)                | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-ca-immed-untergeordnete Elemente**](a-msds-approx-immed-subordinates.md)    | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-authentieredto-accountlist**](a-msds-authenticatedtoaccountlist.md) | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**MS-DS-Konsistenz-untergeordnet-Anzahl**](a-ms-ds-consistencychildcount.md)         | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                      | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-is-Domain-for**](a-msds-isdomainfor.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-is-full-Replica-for**](a-msds-isfullreplicafor.md)                   | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-is-Partial-Replica-for**](a-msds-ispartialreplicafor.md)             | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-krbtgt-Link-BL**](a-msds-krbtgtlinkbl.md)                            | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-gemastert von**](a-msds-masteredby.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Members-für-AZ-Role-BL**](a-msds-membersforazrolebl.md)              | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-repl-Cursor**](a-msds-ncreplcursors.md)                          | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-repl-Inbound-Nachbarn**](a-msds-ncreplinboundneighbors.md)       | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-repl-Outbound-Nachbarn**](a-msds-ncreploutboundneighbors.md)     | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)  | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-Typ**](a-msds-nctype.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                            | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                  | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)        | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)        | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                           | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-PSO-angewendet**](a-msds-psoapplied.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)         | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                 | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-offengelegt-DSAs**](a-msds-revealeddsas.md)                             | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-enthüllt-List-BL**](a-msds-revealedlistbl.md)                        | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Settings**](a-msds-settings.md)                                      | False     | [**Verbindungspunkt**](c-connectionpoint.md)<br/>                                 |
| [**ms-DS-Tasks-für-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                  | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Tasks-für-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                  | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**msSFU-30-POSIX-Member-of**](a-mssfu30posixmemberof.md)                     | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**NetBoot-SCP-BL**](a-netbootscpbl.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Nicht sicherheitsmitglied-BL**](a-nonsecuritymemberbl.md)                        | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                       | Richtig      | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Objekt-Kategorie**](a-objectcategory.md)                                    | Richtig      | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Object-Klasse**](a-objectclass.md)                                          | Richtig      | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Objekt-GUID**](a-objectguid.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Objekt-Version**](a-objectversion.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Betriebs System**](a-operatingsystem.md)                                  | False     | **Druck Warteschlange**                                                                          |
| [**Betriebs System-Hotfix**](a-operatingsystemhotfix.md)                     | False     | **Druck Warteschlange**                                                                          |
| [**Betriebs System-Service Pack**](a-operatingsystemservicepack.md)          | False     | **Druck Warteschlange**                                                                          |
| [**Betriebs System Version**](a-operatingsystemversion.md)                   | False     | **Druck Warteschlange**                                                                          |
| [**Andere-bekannte Objekte**](a-otherwellknownobjects.md)                    | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Partial-Attribute-löschen-List**](a-partialattributedeletionlist.md)      | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Partiell-Attribut Satz**](a-partialattributeset.md)                         | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Physical-Location-Object**](a-physicallocationobject.md)                   | False     | **Druck Warteschlange**                                                                          |
| [**Portname**](a-portname.md)                                                | False     | **Druck Warteschlange**                                                                          |
| [**Mögliche-minderwertig**](a-possibleinferiors.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Print-Attribute**](a-printattributes.md)                                  | False     | **Druck Warteschlange**                                                                          |
| [**Print-bin-Names**](a-printbinnames.md)                                     | False     | **Druck Warteschlange**                                                                          |
| [**Drucken-COLLATE**](a-printcollate.md)                                        | False     | **Druck Warteschlange**                                                                          |
| [**Druckfarbe**](a-printcolor.md)                                            | False     | **Druck Warteschlange**                                                                          |
| [**Print-Duplex-unterstützt**](a-printduplexsupported.md)                       | False     | **Druck Warteschlange**                                                                          |
| [**Druck-Endzeit**](a-printendtime.md)                                       | False     | **Druck Warteschlange**                                                                          |
| [**Drucker Name**](a-printername.md)                                          | Richtig      | **Druck Warteschlange**                                                                          |
| [**Print-Formular Name**](a-printformname.md)                                     | False     | **Druck Warteschlange**                                                                          |
| [**Print-Keep-Print-Jobs**](a-printkeepprintedjobs.md)                      | False     | **Druck Warteschlange**                                                                          |
| [**Druck Sprache**](a-printlanguage.md)                                      | False     | **Druck Warteschlange**                                                                          |
| [**Print-Mac-Adresse**](a-printmacaddress.md)                                 | False     | **Druck Warteschlange**                                                                          |
| [**Print-Max-Kopien**](a-printmaxcopies.md)                                   | False     | **Druck Warteschlange**                                                                          |
| [**Print-Max-Resolution wird unterstützt**](a-printmaxresolutionsupported.md)        | False     | **Druck Warteschlange**                                                                          |
| [**Print-Max-X-Block**](a-printmaxxextent.md)                                | False     | **Druck Warteschlange**                                                                          |
| [**Print-Max-Y-Block**](a-printmaxyextent.md)                                | False     | **Druck Warteschlange**                                                                          |
| [**Druck Medien-bereit**](a-printmediaready.md)                                 | False     | **Druck Warteschlange**                                                                          |
| [**Print-Media-supported**](a-printmediasupported.md)                         | False     | **Druck Warteschlange**                                                                          |
| [**Druck-Arbeitsspeicher**](a-printmemory.md)                                          | False     | **Druck Warteschlange**                                                                          |
| [**Print-min-X-Block**](a-printminxextent.md)                                | False     | **Druck Warteschlange**                                                                          |
| [**Druck-min-Y-Block**](a-printminyextent.md)                                | False     | **Druck Warteschlange**                                                                          |
| [**Print-Network-Address**](a-printnetworkaddress.md)                         | False     | **Druck Warteschlange**                                                                          |
| [**Druck Benachrichtigung**](a-printnotify.md)                                          | False     | **Druck Warteschlange**                                                                          |
| [**Print-Number-up**](a-printnumberup.md)                                     | False     | **Druck Warteschlange**                                                                          |
| [**Print-Ausrichtungen-unterstützt**](a-printorientationssupported.md)           | False     | **Druck Warteschlange**                                                                          |
| [**Druck Besitzer**](a-printowner.md)                                            | False     | **Druck Warteschlange**                                                                          |
| [**Druckseiten pro Minute**](a-printpagesperminute.md)                        | False     | **Druck Warteschlange**                                                                          |
| [**Druck Rate**](a-printrate.md)                                              | False     | **Druck Warteschlange**                                                                          |
| [**Druck Raten Einheit**](a-printrateunit.md)                                     | False     | **Druck Warteschlange**                                                                          |
| [**Druck Trennzeichen-Datei**](a-printseparatorfile.md)                           | False     | **Druck Warteschlange**                                                                          |
| [**Druckfreigabe Name**](a-printsharename.md)                                   | False     | **Druck Warteschlange**                                                                          |
| [**Druck Spoolvorgang**](a-printspooling.md)                                      | False     | **Druck Warteschlange**                                                                          |
| [**Print-Stapling-supported**](a-printstaplingsupported.md)                   | False     | **Druck Warteschlange**                                                                          |
| [**Druck-Startzeit**](a-printstarttime.md)                                   | False     | **Druck Warteschlange**                                                                          |
| [**Druck Status**](a-printstatus.md)                                          | False     | **Druck Warteschlange**                                                                          |
| [**Priorität**](a-priority.md)                                                 | False     | **Druck Warteschlange**                                                                          |
| [**Proxy-Objekt Name**](a-proxiedobjectname.md)                             | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Proxy Adressen**](a-proxyaddresses.md)                                    | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Abfrage-Richtlinie-BL**](a-querypolicybl.md)                                     | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**RDN**](a-name.md)                                                          | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                      | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**REPL-Update-Vector**](a-repluptodatevector.md)                           | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Berichte**](a-directreports.md)                                             | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Reps-from**](a-repsfrom.md)                                                | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Reps-to**](a-repsto.md)                                                    | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Novel**](a-revision.md)                                                 | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**SD-Rechte**](a-sdrightseffective.md)                             | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Server Name**](a-servername.md)                                            | Richtig      | **Druck Warteschlange**                                                                          |
| [**Server-Reference-BL**](a-serverreferencebl.md)                             | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Short-Server-Name**](a-shortservername.md)                                 | Richtig      | **Druck Warteschlange**                                                                          |
| [**Anzeigen-in-Advanced-nur anzeigen**](a-showinadvancedviewonly.md)                 | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Site-Object-BL**](a-siteobjectbl.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Struktur-Objekt-Klasse**](a-structuralobjectclass.md)                     | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Sub-Refs**](a-subrefs.md)                                                  | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Subschemasubentry**](a-subschemasubentry.md)                               | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**SystemFlags**](a-systemflags.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**UNC-Name**](a-uncname.md)                                                  | Richtig      | **Druck Warteschlange**                                                                          |
| [**Die Anwendung wurde geändert.**](a-usnchanged.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Von der Anwendung erstellte**](a-usncreated.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**USA-DSA-letzte-obj-entfernt**](a-usndsalastobjremoved.md)                     | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Standort-und standortübergreifende standortübergreifende**](a-usnintersite.md)                                        | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**"An-Last-obj-REM"**](a-usnlastobjrem.md)                                    | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Quell Code Quelle**](a-usnsource.md)                                              | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Versionsnummer**](a-versionnumber.md)                                      | Richtig      | **Druck Warteschlange**                                                                          |
| [**WBEM-Pfad**](a-wbempath.md)                                                | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Bekannte Objekte**](a-wellknownobjects.md)                               | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Bei Änderung**](a-whenchanged.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Bei Erstellung**](a-whencreated.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**WWW-Homepage**](a-wwwhomepage.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**WWW-Page-other**](a-url.md)                                                | False     | [**Nach oben**](c-top.md)<br/>                                                          |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2

-   [Attribute](#windows-server-2008-r2-attributes)



| Eingabe | Wert |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | False                                                                                                                                                                |
| Object-Category             | 1                                                                                                                                                                    |
| Default-Object-Category     | \-                                                                                                                                                                   |
| Governs-Id                  | 1.2.840.113556.1.5.23                                                                                                                                                |
| Standard-ausblenden-Wert        | 0                                                                                                                                                                    |
| RDN-ATT-ID                  | [**Gemeinsamer Name**](a-cn.md)<br/>                                                                                                                               |
| Unterklasse von                 | [**Verbindungspunkt**](c-connectionpoint.md)<br/>                                                                                                             |
| Mögliche Vorgesetzten          | [**Computer**](c-computer.md)[**Container**](c-container.md)[**Domäne-DNS**](c-domaindns.md)-[**Organisationseinheit**](c-organizationalunit.md)                   |
| Zusätzlich           | \-                                                                                                                                                                   |
| NT-Security-Descriptor      | o:Bag: schlecht: S:                                                                                                                                                         |
| Standard Sicherheits Beschreibung | D: (A;; rpwpcrccdclclorcwowdsddtsw;;;D a) (a;; Rpwpcrccdclclorcwowdsddtsw;;; SY) (A;; Rpwpcrccdclclorcwowdsddtsw;;; PO) (A;; Rpwpcrccdclclorcwowdsddtsw;;; Co) (A;; Rplclorc;;; Thaus |
| System-Flags                | 0x00000010                                                                                                                                                           |



## <a name="windows-server-2008-r2-attributes"></a>Windows Server 2008 R2-Attribute

Diese Klasse enthält die folgenden Attribute für Windows Server 2008 R2:



| Attribut                                                                        | Obligatorisch. | Abgeleitet von                                                                             |
|----------------------------------------------------------------------------------|-----------|------------------------------------------------------------------------------------------|
| [**Administrator: Beschreibung**](a-admindescription.md)                                  | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Administrator-Anzeige Name**](a-admindisplayname.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Zulässige Attribute**](a-allowedattributes.md)                                | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Zulässige Attribute-gültig**](a-allowedattributeseffective.md)             | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Zulässige, untergeordnete Klassen**](a-allowedchildclasses.md)                           | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Zulässig-untergeordnete Klassen-gültig**](a-allowedchildclasseseffective.md)        | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Assetnummer**](a-assetnumber.md)                                            | False     | **Druck Warteschlange**                                                                          |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                    | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Bytes pro Minute**](a-bytesperminute.md)                                     | False     | **Druck Warteschlange**                                                                          |
| [**Kanonischer Name**](a-canonicalname.md)                                        | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Gemeinsamer Name**](a-cn.md)                                                      | Richtig      | [**Verbindungspunkt**](c-connectionpoint.md)<br/> [**Nach oben**](c-top.md)<br/> |
| [**Create-Zeitstempel**](a-createtimestamp.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Standard-Priorität**](a-defaultpriority.md)                                    | False     | **Druck Warteschlange**                                                                          |
| [**Beschreibung**](a-description.md)                                             | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Anzeige Name**](a-displayname.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Anzeige Name-druckdruck**](a-displaynameprintable.md)                         | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Treiber Name**](a-drivername.md)                                              | False     | **Druck Warteschlange**                                                                          |
| [**Treiber Version**](a-driverversion.md)                                        | False     | **Druck Warteschlange**                                                                          |
| [**DSA-Signatur**](a-dsasignature.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**DS-Core-propagierungs Daten**](a-dscorepropagationdata.md)                      | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Erweiterungs Name**](a-extensionname.md)                                        | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Fahren**](a-flags.md)                                                         | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Aus-Eintrag**](a-fromentry.md)                                                | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                    | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                        | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**"F"-Rollen Besitzer**](a-fsmoroleowner.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Instanztyp**](a-instancetype.md)                                          | Richtig      | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Is-critical-System-Object**](a-iscriticalsystemobject.md)                    | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Ist-gelöscht**](a-isdeleted.md)                                                | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Is-Member-of-DL**](a-memberof.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Is-Privilege-Inhaber**](a-isprivilegeholder.md)                               | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Ist-recycelt**](a-isrecycled.md)                                              | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Keywords**](a-keywords.md)                                                   | False     | [**Verbindungspunkt**](c-connectionpoint.md)<br/>                                 |
| [**Letztes-bekannt/übergeordnetes Element**](a-lastknownparent.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Hotels**](a-location.md)                                                   | False     | **Druck Warteschlange**                                                                          |
| [**Verwaltet von**](a-managedby.md)                                                | False     | [**Verbindungspunkt**](c-connectionpoint.md)<br/>                                 |
| [**Verwaltete Objekte**](a-managedobjects.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Verwaltet von**](a-masteredby.md)                                              | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Modify-Zeitstempel**](a-modifytimestamp.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**MS-com-partitionsetlink**](a-mscom-partitionsetlink.md)                      | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**MS-com-userlink**](a-mscom-userlink.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**MS-DFSR-computerreferencebl**](a-msdfsr-computerreferencebl.md)              | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**MS-DFSR-mitgliedreferencebl**](a-msdfsr-memberreferencebl.md)                  | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-ca-immed-untergeordnete Elemente**](a-msds-approx-immed-subordinates.md)      | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-authentieredto-accountlist**](a-msds-authenticatedtoaccountlist.md)   | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**MS-DS-Konsistenz-untergeordnet-Anzahl**](a-ms-ds-consistencychildcount.md)           | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                        | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-aktiviert-Feature-BL**](a-msds-enabledfeaturebl.md)                      | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)             | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-is-Domain-for**](a-msds-isdomainfor.md)                                | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-is-full-Replica-for**](a-msds-isfullreplicafor.md)                     | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-is-Partial-Replica-for**](a-msds-ispartialreplicafor.md)               | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-krbtgt-Link-BL**](a-msds-krbtgtlinkbl.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-local-Effective-Lösch Zeit**](a-msds-localeffectivedeletiontime.md) | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-local-Effective-Papier-Time**](a-msds-localeffectiverecycletime.md)   | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-gemastert von**](a-msds-masteredby.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Members-für-AZ-Role-BL**](a-msds-membersforazrolebl.md)                | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-repl-Cursor**](a-msds-ncreplcursors.md)                            | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-repl-Inbound-Nachbarn**](a-msds-ncreplinboundneighbors.md)         | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-repl-Outbound-Nachbarn**](a-msds-ncreploutboundneighbors.md)       | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)    | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-Typ**](a-msds-nctype.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                    | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-oidtoidgruppe-Link-BL**](a-msds-oidtogrouplinkbl.md)                      | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)          | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)          | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                             | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-PSO-angewendet**](a-msds-psoapplied.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)           | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                   | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-offengelegt-DSAs**](a-msds-revealeddsas.md)                               | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-enthüllt-List-BL**](a-msds-revealedlistbl.md)                          | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Settings**](a-msds-settings.md)                                        | False     | [**Verbindungspunkt**](c-connectionpoint.md)<br/>                                 |
| [**ms-DS-Tasks-für-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                    | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Tasks-für-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                    | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**msSFU-30-POSIX-Member-of**](a-mssfu30posixmemberof.md)                       | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**NetBoot-SCP-BL**](a-netbootscpbl.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Nicht sicherheitsmitglied-BL**](a-nonsecuritymemberbl.md)                          | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                         | Richtig      | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                     | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Objekt-Kategorie**](a-objectcategory.md)                                      | Richtig      | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Object-Klasse**](a-objectclass.md)                                            | Richtig      | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Objekt-GUID**](a-objectguid.md)                                              | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Objekt-Version**](a-objectversion.md)                                        | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Betriebs System**](a-operatingsystem.md)                                    | False     | **Druck Warteschlange**                                                                          |
| [**Betriebs System-Hotfix**](a-operatingsystemhotfix.md)                       | False     | **Druck Warteschlange**                                                                          |
| [**Betriebs System-Service Pack**](a-operatingsystemservicepack.md)            | False     | **Druck Warteschlange**                                                                          |
| [**Betriebs System Version**](a-operatingsystemversion.md)                     | False     | **Druck Warteschlange**                                                                          |
| [**Andere-bekannte Objekte**](a-otherwellknownobjects.md)                      | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Partial-Attribute-löschen-List**](a-partialattributedeletionlist.md)        | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Partiell-Attribut Satz**](a-partialattributeset.md)                           | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Physical-Location-Object**](a-physicallocationobject.md)                     | False     | **Druck Warteschlange**                                                                          |
| [**Portname**](a-portname.md)                                                  | False     | **Druck Warteschlange**                                                                          |
| [**Mögliche-minderwertig**](a-possibleinferiors.md)                                | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Print-Attribute**](a-printattributes.md)                                    | False     | **Druck Warteschlange**                                                                          |
| [**Print-bin-Names**](a-printbinnames.md)                                       | False     | **Druck Warteschlange**                                                                          |
| [**Drucken-COLLATE**](a-printcollate.md)                                          | False     | **Druck Warteschlange**                                                                          |
| [**Druckfarbe**](a-printcolor.md)                                              | False     | **Druck Warteschlange**                                                                          |
| [**Print-Duplex-unterstützt**](a-printduplexsupported.md)                         | False     | **Druck Warteschlange**                                                                          |
| [**Druck-Endzeit**](a-printendtime.md)                                         | False     | **Druck Warteschlange**                                                                          |
| [**Drucker Name**](a-printername.md)                                            | Richtig      | **Druck Warteschlange**                                                                          |
| [**Print-Formular Name**](a-printformname.md)                                       | False     | **Druck Warteschlange**                                                                          |
| [**Print-Keep-Print-Jobs**](a-printkeepprintedjobs.md)                        | False     | **Druck Warteschlange**                                                                          |
| [**Druck Sprache**](a-printlanguage.md)                                        | False     | **Druck Warteschlange**                                                                          |
| [**Print-Mac-Adresse**](a-printmacaddress.md)                                   | False     | **Druck Warteschlange**                                                                          |
| [**Print-Max-Kopien**](a-printmaxcopies.md)                                     | False     | **Druck Warteschlange**                                                                          |
| [**Print-Max-Resolution wird unterstützt**](a-printmaxresolutionsupported.md)          | False     | **Druck Warteschlange**                                                                          |
| [**Print-Max-X-Block**](a-printmaxxextent.md)                                  | False     | **Druck Warteschlange**                                                                          |
| [**Print-Max-Y-Block**](a-printmaxyextent.md)                                  | False     | **Druck Warteschlange**                                                                          |
| [**Druck Medien-bereit**](a-printmediaready.md)                                   | False     | **Druck Warteschlange**                                                                          |
| [**Print-Media-supported**](a-printmediasupported.md)                           | False     | **Druck Warteschlange**                                                                          |
| [**Druck-Arbeitsspeicher**](a-printmemory.md)                                            | False     | **Druck Warteschlange**                                                                          |
| [**Print-min-X-Block**](a-printminxextent.md)                                  | False     | **Druck Warteschlange**                                                                          |
| [**Druck-min-Y-Block**](a-printminyextent.md)                                  | False     | **Druck Warteschlange**                                                                          |
| [**Print-Network-Address**](a-printnetworkaddress.md)                           | False     | **Druck Warteschlange**                                                                          |
| [**Druck Benachrichtigung**](a-printnotify.md)                                            | False     | **Druck Warteschlange**                                                                          |
| [**Print-Number-up**](a-printnumberup.md)                                       | False     | **Druck Warteschlange**                                                                          |
| [**Print-Ausrichtungen-unterstützt**](a-printorientationssupported.md)             | False     | **Druck Warteschlange**                                                                          |
| [**Druck Besitzer**](a-printowner.md)                                              | False     | **Druck Warteschlange**                                                                          |
| [**Druckseiten pro Minute**](a-printpagesperminute.md)                          | False     | **Druck Warteschlange**                                                                          |
| [**Druck Rate**](a-printrate.md)                                                | False     | **Druck Warteschlange**                                                                          |
| [**Druck Raten Einheit**](a-printrateunit.md)                                       | False     | **Druck Warteschlange**                                                                          |
| [**Druck Trennzeichen-Datei**](a-printseparatorfile.md)                             | False     | **Druck Warteschlange**                                                                          |
| [**Druckfreigabe Name**](a-printsharename.md)                                     | False     | **Druck Warteschlange**                                                                          |
| [**Druck Spoolvorgang**](a-printspooling.md)                                        | False     | **Druck Warteschlange**                                                                          |
| [**Print-Stapling-supported**](a-printstaplingsupported.md)                     | False     | **Druck Warteschlange**                                                                          |
| [**Druck-Startzeit**](a-printstarttime.md)                                     | False     | **Druck Warteschlange**                                                                          |
| [**Druck Status**](a-printstatus.md)                                            | False     | **Druck Warteschlange**                                                                          |
| [**Priorität**](a-priority.md)                                                   | False     | **Druck Warteschlange**                                                                          |
| [**Proxy-Objekt Name**](a-proxiedobjectname.md)                               | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Proxy Adressen**](a-proxyaddresses.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Abfrage-Richtlinie-BL**](a-querypolicybl.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**RDN**](a-name.md)                                                            | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                        | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**REPL-Update-Vector**](a-repluptodatevector.md)                             | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Berichte**](a-directreports.md)                                               | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Reps-from**](a-repsfrom.md)                                                  | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Reps-to**](a-repsto.md)                                                      | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Novel**](a-revision.md)                                                   | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**SD-Rechte**](a-sdrightseffective.md)                               | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Server Name**](a-servername.md)                                              | Richtig      | **Druck Warteschlange**                                                                          |
| [**Server-Reference-BL**](a-serverreferencebl.md)                               | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Short-Server-Name**](a-shortservername.md)                                   | Richtig      | **Druck Warteschlange**                                                                          |
| [**Anzeigen-in-Advanced-nur anzeigen**](a-showinadvancedviewonly.md)                   | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Site-Object-BL**](a-siteobjectbl.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Struktur-Objekt-Klasse**](a-structuralobjectclass.md)                       | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Sub-Refs**](a-subrefs.md)                                                    | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Subschemasubentry**](a-subschemasubentry.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**SystemFlags**](a-systemflags.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**UNC-Name**](a-uncname.md)                                                    | Richtig      | **Druck Warteschlange**                                                                          |
| [**Die Anwendung wurde geändert.**](a-usnchanged.md)                                              | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Von der Anwendung erstellte**](a-usncreated.md)                                              | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**USA-DSA-letzte-obj-entfernt**](a-usndsalastobjremoved.md)                       | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Standort-und standortübergreifende standortübergreifende**](a-usnintersite.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**"An-Last-obj-REM"**](a-usnlastobjrem.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Quell Code Quelle**](a-usnsource.md)                                                | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Versionsnummer**](a-versionnumber.md)                                        | Richtig      | **Druck Warteschlange**                                                                          |
| [**WBEM-Pfad**](a-wbempath.md)                                                  | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Bekannte Objekte**](a-wellknownobjects.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Bei Änderung**](a-whenchanged.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Bei Erstellung**](a-whencreated.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**WWW-Homepage**](a-wwwhomepage.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**WWW-Page-other**](a-url.md)                                                  | False     | [**Nach oben**](c-top.md)<br/>                                                          |



## <a name="windows-server-2012"></a>Windows Server 2012

-   [Attribute](#windows-server-2012-attributes)



| Eingabe | Wert |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | False                                                                                                                                                                |
| Object-Category             | 1                                                                                                                                                                    |
| Default-Object-Category     | \-                                                                                                                                                                   |
| Governs-Id                  | 1.2.840.113556.1.5.23                                                                                                                                                |
| Standard-ausblenden-Wert        | 0                                                                                                                                                                    |
| RDN-ATT-ID                  | [**Gemeinsamer Name**](a-cn.md)<br/>                                                                                                                               |
| Unterklasse von                 | [**Verbindungspunkt**](c-connectionpoint.md)<br/>                                                                                                             |
| Mögliche Vorgesetzten          | [**Computer**](c-computer.md)[**Container**](c-container.md)[**Domäne-DNS**](c-domaindns.md)-[**Organisationseinheit**](c-organizationalunit.md)                   |
| Zusätzlich           | \-                                                                                                                                                                   |
| NT-Security-Descriptor      | o:Bag: schlecht: S:                                                                                                                                                         |
| Standard Sicherheits Beschreibung | D: (A;; rpwpcrccdclclorcwowdsddtsw;;;D a) (a;; Rpwpcrccdclclorcwowdsddtsw;;; SY) (A;; Rpwpcrccdclclorcwowdsddtsw;;; PO) (A;; Rpwpcrccdclclorcwowdsddtsw;;; Co) (A;; Rplclorc;;; Thaus |
| System-Flags                | 0x00000010                                                                                                                                                           |



## <a name="windows-server-2012-attributes"></a>Windows Server 2012-Attribute

Diese Klasse enthält die folgenden Attribute für Windows Server 2012:



| Attribut                                                                                    | Obligatorisch. | Abgeleitet von                                                                             |
|----------------------------------------------------------------------------------------------|-----------|------------------------------------------------------------------------------------------|
| [**Administrator: Beschreibung**](a-admindescription.md)                                              | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Administrator-Anzeige Name**](a-admindisplayname.md)                                             | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Zulässige Attribute**](a-allowedattributes.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Zulässige Attribute-gültig**](a-allowedattributeseffective.md)                         | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Zulässige, untergeordnete Klassen**](a-allowedchildclasses.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Zulässig-untergeordnete Klassen-gültig**](a-allowedchildclasseseffective.md)                    | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Assetnummer**](a-assetnumber.md)                                                        | False     | **Druck Warteschlange**                                                                          |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                                | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Bytes pro Minute**](a-bytesperminute.md)                                                 | False     | **Druck Warteschlange**                                                                          |
| [**Kanonischer Name**](a-canonicalname.md)                                                    | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Gemeinsamer Name**](a-cn.md)                                                                  | Richtig      | [**Verbindungspunkt**](c-connectionpoint.md)<br/> [**Nach oben**](c-top.md)<br/> |
| [**Create-Zeitstempel**](a-createtimestamp.md)                                               | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Standard-Priorität**](a-defaultpriority.md)                                                | False     | **Druck Warteschlange**                                                                          |
| [**Beschreibung**](a-description.md)                                                         | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Anzeige Name**](a-displayname.md)                                                        | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Anzeige Name-druckdruck**](a-displaynameprintable.md)                                     | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Treiber Name**](a-drivername.md)                                                          | False     | **Druck Warteschlange**                                                                          |
| [**Treiber Version**](a-driverversion.md)                                                    | False     | **Druck Warteschlange**                                                                          |
| [**DSA-Signatur**](a-dsasignature.md)                                                      | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**DS-Core-propagierungs Daten**](a-dscorepropagationdata.md)                                  | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Erweiterungs Name**](a-extensionname.md)                                                    | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Fahren**](a-flags.md)                                                                     | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Aus-Eintrag**](a-fromentry.md)                                                            | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                                | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                                    | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**"F"-Rollen Besitzer**](a-fsmoroleowner.md)                                                   | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Instanztyp**](a-instancetype.md)                                                      | Richtig      | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Is-critical-System-Object**](a-iscriticalsystemobject.md)                                | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Ist-gelöscht**](a-isdeleted.md)                                                            | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Is-Member-of-DL**](a-memberof.md)                                                        | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Is-Privilege-Inhaber**](a-isprivilegeholder.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Ist-recycelt**](a-isrecycled.md)                                                          | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Keywords**](a-keywords.md)                                                               | False     | [**Verbindungspunkt**](c-connectionpoint.md)<br/>                                 |
| [**Letztes-bekannt/übergeordnetes Element**](a-lastknownparent.md)                                               | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Hotels**](a-location.md)                                                               | False     | **Druck Warteschlange**                                                                          |
| [**Verwaltet von**](a-managedby.md)                                                            | False     | [**Verbindungspunkt**](c-connectionpoint.md)<br/>                                 |
| [**Verwaltete Objekte**](a-managedobjects.md)                                                  | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Verwaltet von**](a-masteredby.md)                                                          | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Modify-Zeitstempel**](a-modifytimestamp.md)                                               | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**MS-com-partitionsetlink**](a-mscom-partitionsetlink.md)                                  | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**MS-com-userlink**](a-mscom-userlink.md)                                                  | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**MS-DFSR-computerreferencebl**](a-msdfsr-computerreferencebl.md)                          | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**MS-DFSR-mitgliedreferencebl**](a-msdfsr-memberreferencebl.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-ca-immed-untergeordnete Elemente**](a-msds-approx-immed-subordinates.md)                  | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-authentieredto-accountlist**](a-msds-authenticatedtoaccountlist.md)               | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Claim-Shares-mögliche-values-with-BL**](a-msds-claimsharespossiblevalueswithbl.md) | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**MS-DS-Konsistenz-untergeordnet-Anzahl**](a-ms-ds-consistencychildcount.md)                       | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                                    | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-aktiviert-Feature-BL**](a-msds-enabledfeaturebl.md)                                  | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)                         | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-is-Domain-for**](a-msds-isdomainfor.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-is-full-Replica-for**](a-msds-isfullreplicafor.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-is-Partial-Replica-for**](a-msds-ispartialreplicafor.md)                           | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-is-Primary-Computer-für**](a-msds-isprimarycomputerfor.md)                         | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-krbtgt-Link-BL**](a-msds-krbtgtlinkbl.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-local-Effective-Lösch Zeit**](a-msds-localeffectivedeletiontime.md)             | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-local-Effective-Papier-Time**](a-msds-localeffectiverecycletime.md)               | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-gemastert von**](a-msds-masteredby.md)                                               | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Members-für-AZ-Role-BL**](a-msds-membersforazrolebl.md)                            | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Members-of-Resource-Property-List-BL**](a-msds-membersofresourcepropertylistbl.md) | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-repl-Cursor**](a-msds-ncreplcursors.md)                                        | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-repl-Inbound-Nachbarn**](a-msds-ncreplinboundneighbors.md)                     | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-repl-Outbound-Nachbarn**](a-msds-ncreploutboundneighbors.md)                   | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)                | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-Typ**](a-msds-nctype.md)                                                       | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                                | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-oidtoidgruppe-Link-BL**](a-msds-oidtogrouplinkbl.md)                                  | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)                      | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)                      | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-PSO-angewendet**](a-msds-psoapplied.md)                                               | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)                       | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                               | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-offengelegt-DSAs**](a-msds-revealeddsas.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-enthüllt-List-BL**](a-msds-revealedlistbl.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Settings**](a-msds-settings.md)                                                    | False     | [**Verbindungspunkt**](c-connectionpoint.md)<br/>                                 |
| [**ms-DS-Tasks-für-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                                | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Tasks-für-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                                | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-TDO-Egress-BL**](a-msds-tdoegressbl.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-TDO-Ingress-BL**](a-msds-tdoingressbl.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-DS-Value-Type-Reference-BL**](a-msds-valuetypereferencebl.md)                         | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                                        | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**msSFU-30-POSIX-Member-of**](a-mssfu30posixmemberof.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**NetBoot-SCP-BL**](a-netbootscpbl.md)                                                     | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Nicht sicherheitsmitglied-BL**](a-nonsecuritymemberbl.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                                     | Richtig      | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                                 | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Objekt-Kategorie**](a-objectcategory.md)                                                  | Richtig      | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Object-Klasse**](a-objectclass.md)                                                        | Richtig      | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Objekt-GUID**](a-objectguid.md)                                                          | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Objekt-Version**](a-objectversion.md)                                                    | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Betriebs System**](a-operatingsystem.md)                                                | False     | **Druck Warteschlange**                                                                          |
| [**Betriebs System-Hotfix**](a-operatingsystemhotfix.md)                                   | False     | **Druck Warteschlange**                                                                          |
| [**Betriebs System-Service Pack**](a-operatingsystemservicepack.md)                        | False     | **Druck Warteschlange**                                                                          |
| [**Betriebs System Version**](a-operatingsystemversion.md)                                 | False     | **Druck Warteschlange**                                                                          |
| [**Andere-bekannte Objekte**](a-otherwellknownobjects.md)                                  | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Partial-Attribute-löschen-List**](a-partialattributedeletionlist.md)                    | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Partiell-Attribut Satz**](a-partialattributeset.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Physical-Location-Object**](a-physicallocationobject.md)                                 | False     | **Druck Warteschlange**                                                                          |
| [**Portname**](a-portname.md)                                                              | False     | **Druck Warteschlange**                                                                          |
| [**Mögliche-minderwertig**](a-possibleinferiors.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Print-Attribute**](a-printattributes.md)                                                | False     | **Druck Warteschlange**                                                                          |
| [**Print-bin-Names**](a-printbinnames.md)                                                   | False     | **Druck Warteschlange**                                                                          |
| [**Drucken-COLLATE**](a-printcollate.md)                                                      | False     | **Druck Warteschlange**                                                                          |
| [**Druckfarbe**](a-printcolor.md)                                                          | False     | **Druck Warteschlange**                                                                          |
| [**Print-Duplex-unterstützt**](a-printduplexsupported.md)                                     | False     | **Druck Warteschlange**                                                                          |
| [**Druck-Endzeit**](a-printendtime.md)                                                     | False     | **Druck Warteschlange**                                                                          |
| [**Drucker Name**](a-printername.md)                                                        | Richtig      | **Druck Warteschlange**                                                                          |
| [**Print-Formular Name**](a-printformname.md)                                                   | False     | **Druck Warteschlange**                                                                          |
| [**Print-Keep-Print-Jobs**](a-printkeepprintedjobs.md)                                    | False     | **Druck Warteschlange**                                                                          |
| [**Druck Sprache**](a-printlanguage.md)                                                    | False     | **Druck Warteschlange**                                                                          |
| [**Print-Mac-Adresse**](a-printmacaddress.md)                                               | False     | **Druck Warteschlange**                                                                          |
| [**Print-Max-Kopien**](a-printmaxcopies.md)                                                 | False     | **Druck Warteschlange**                                                                          |
| [**Print-Max-Resolution wird unterstützt**](a-printmaxresolutionsupported.md)                      | False     | **Druck Warteschlange**                                                                          |
| [**Print-Max-X-Block**](a-printmaxxextent.md)                                              | False     | **Druck Warteschlange**                                                                          |
| [**Print-Max-Y-Block**](a-printmaxyextent.md)                                              | False     | **Druck Warteschlange**                                                                          |
| [**Druck Medien-bereit**](a-printmediaready.md)                                               | False     | **Druck Warteschlange**                                                                          |
| [**Print-Media-supported**](a-printmediasupported.md)                                       | False     | **Druck Warteschlange**                                                                          |
| [**Druck-Arbeitsspeicher**](a-printmemory.md)                                                        | False     | **Druck Warteschlange**                                                                          |
| [**Print-min-X-Block**](a-printminxextent.md)                                              | False     | **Druck Warteschlange**                                                                          |
| [**Druck-min-Y-Block**](a-printminyextent.md)                                              | False     | **Druck Warteschlange**                                                                          |
| [**Print-Network-Address**](a-printnetworkaddress.md)                                       | False     | **Druck Warteschlange**                                                                          |
| [**Druck Benachrichtigung**](a-printnotify.md)                                                        | False     | **Druck Warteschlange**                                                                          |
| [**Print-Number-up**](a-printnumberup.md)                                                   | False     | **Druck Warteschlange**                                                                          |
| [**Print-Ausrichtungen-unterstützt**](a-printorientationssupported.md)                         | False     | **Druck Warteschlange**                                                                          |
| [**Druck Besitzer**](a-printowner.md)                                                          | False     | **Druck Warteschlange**                                                                          |
| [**Druckseiten pro Minute**](a-printpagesperminute.md)                                      | False     | **Druck Warteschlange**                                                                          |
| [**Druck Rate**](a-printrate.md)                                                            | False     | **Druck Warteschlange**                                                                          |
| [**Druck Raten Einheit**](a-printrateunit.md)                                                   | False     | **Druck Warteschlange**                                                                          |
| [**Druck Trennzeichen-Datei**](a-printseparatorfile.md)                                         | False     | **Druck Warteschlange**                                                                          |
| [**Druckfreigabe Name**](a-printsharename.md)                                                 | False     | **Druck Warteschlange**                                                                          |
| [**Druck Spoolvorgang**](a-printspooling.md)                                                    | False     | **Druck Warteschlange**                                                                          |
| [**Print-Stapling-supported**](a-printstaplingsupported.md)                                 | False     | **Druck Warteschlange**                                                                          |
| [**Druck-Startzeit**](a-printstarttime.md)                                                 | False     | **Druck Warteschlange**                                                                          |
| [**Druck Status**](a-printstatus.md)                                                        | False     | **Druck Warteschlange**                                                                          |
| [**Priorität**](a-priority.md)                                                               | False     | **Druck Warteschlange**                                                                          |
| [**Proxy-Objekt Name**](a-proxiedobjectname.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Proxy Adressen**](a-proxyaddresses.md)                                                  | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Abfrage-Richtlinie-BL**](a-querypolicybl.md)                                                   | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**RDN**](a-name.md)                                                                        | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                                    | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**REPL-Update-Vector**](a-repluptodatevector.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Berichte**](a-directreports.md)                                                           | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Reps-from**](a-repsfrom.md)                                                              | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Reps-to**](a-repsto.md)                                                                  | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Novel**](a-revision.md)                                                               | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**SD-Rechte**](a-sdrightseffective.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Server Name**](a-servername.md)                                                          | Richtig      | **Druck Warteschlange**                                                                          |
| [**Server-Reference-BL**](a-serverreferencebl.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Short-Server-Name**](a-shortservername.md)                                               | Richtig      | **Druck Warteschlange**                                                                          |
| [**Anzeigen-in-Advanced-nur anzeigen**](a-showinadvancedviewonly.md)                               | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Site-Object-BL**](a-siteobjectbl.md)                                                     | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Struktur-Objekt-Klasse**](a-structuralobjectclass.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Sub-Refs**](a-subrefs.md)                                                                | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Subschemasubentry**](a-subschemasubentry.md)                                             | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**SystemFlags**](a-systemflags.md)                                                        | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**UNC-Name**](a-uncname.md)                                                                | Richtig      | **Druck Warteschlange**                                                                          |
| [**Die Anwendung wurde geändert.**](a-usnchanged.md)                                                          | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Von der Anwendung erstellte**](a-usncreated.md)                                                          | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**USA-DSA-letzte-obj-entfernt**](a-usndsalastobjremoved.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Standort-und standortübergreifende standortübergreifende**](a-usnintersite.md)                                                      | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**"An-Last-obj-REM"**](a-usnlastobjrem.md)                                                  | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Quell Code Quelle**](a-usnsource.md)                                                            | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Versionsnummer**](a-versionnumber.md)                                                    | Richtig      | **Druck Warteschlange**                                                                          |
| [**WBEM-Pfad**](a-wbempath.md)                                                              | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Bekannte Objekte**](a-wellknownobjects.md)                                             | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Bei Änderung**](a-whenchanged.md)                                                        | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**Bei Erstellung**](a-whencreated.md)                                                        | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**WWW-Homepage**](a-wwwhomepage.md)                                                       | False     | [**Nach oben**](c-top.md)<br/>                                                          |
| [**WWW-Page-other**](a-url.md)                                                              | False     | [**Nach oben**](c-top.md)<br/>                                                          |



 

 





