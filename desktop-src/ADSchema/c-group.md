---
title: Group-Klasse
description: Speichert eine Liste von Benutzernamen. Dient zum Anwenden von Sicherheits Prinzipale auf Ressourcen.
ms.assetid: e8ce5c43-d0fb-4c67-a6ef-7094fb7e7669
ms.tgt_platform: multiple
keywords:
- AD-Schema der Gruppenklasse
- AD-Schema der Gruppenklasse
topic_type:
- apiref
api_name:
- Group
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 618adb97220f4cc1b1e4af7f42fd043c7bb1e6c5
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104106898"
---
# <a name="group-class"></a>Group-Klasse

Speichert eine Liste von Benutzernamen. Dient zum Anwenden von Sicherheits Prinzipale auf Ressourcen.



| Eingabe | Wert |
|-------------------|------------------------------------------------|
| CN                | Gruppieren                                          |
| LDAP-Display-Name | Gruppe                                          |
| Berechtigung aktualisieren  | Dieser Wert wird vom Domänen Administrator festgelegt. |
| Aktualisierungshäufigkeit  | \-                                             |
| Schema-ID-GUID    | bf967a9c-0de6-11d0-a285-00aa003049e2           |



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
-   [Erweiterte Rechte](#windows-2000-server-extended-rights)
-   [Überprüfte Schreibvorgänge](#windows-2000-server-validated-writes)
-   [Eigenschaftensätze](#windows-2000-server-property-sets)



| Eingabe | Wert |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | False                                                                                                                                                                                               |
| Object-Category             | 1                                                                                                                                                                                                   |
| Default-Object-Category     | \-                                                                                                                                                                                                  |
| Governs-Id                  | 1.2.840.113556.1.5.8                                                                                                                                                                                |
| Standard-ausblenden-Wert        | 0                                                                                                                                                                                                   |
| RDN-ATT-ID                  | [**Gemeinsamer Name**](a-cn.md)<br/>                                                                                                                                                              |
| Unterklasse von                 | [**Nach oben**](c-top.md)<br/>                                                                                                                                                                     |
| Mögliche Vorgesetzten          | [**Domain-DNS**](c-domaindns.md)[**-Domänen**](c-builtindomain.md)[**Container**](c-container.md) ([**Organisationseinheit**](c-organizationalunit.md))                                       |
| Zusätzlich           | [**Sicherheits Prinzipal**](c-securityprincipal.md) -e-[**Mail-Empfänger**](c-mailrecipient.md) (System)                                                                                        |
| NT-Security-Descriptor      | o:Bag: schlecht: S:                                                                                                                                                                                        |
| Standard Sicherheits Beschreibung | D: (A;; rpwpcrccdclclorcwowdsddtsw;;;D a) (a;; Rpwpcrccdclclorcwowdsddtsw;;; SY) (A;; Rplclorc;;; Au) (A;; Rpwpcrccdclclorcwowdsddtsw;;; AO) (A;; Rplclorc;;; PS) (OA;; CR; ab721a55-1e2f-11D0-9819-00aa0040529b;; Thaus |
| System-Flags                | 0x00000010                                                                                                                                                                                          |



## <a name="windows-2000-server-attributes"></a>Windows 2000-Server Attribute

Diese Klasse enthält die folgenden Attribute für Windows 2000 Server:



| Attribut                                                                    | Obligatorisch. | Abgeleitet von                                                                                 |
|------------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------|
| [**Konto Name-Verlauf**](a-accountnamehistory.md)                         | False     | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/>                                 |
| [**Admin: Anzahl**](a-admincount.md)                                          | False     | **Gruppieren**                                                                                    |
| [**Administrator: Beschreibung**](a-admindescription.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Administrator-Anzeige Name**](a-admindisplayname.md)                             | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Zulässige Attribute**](a-allowedattributes.md)                            | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Zulässige Attribute-gültig**](a-allowedattributeseffective.md)         | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Zulässige, untergeordnete Klassen**](a-allowedchildclasses.md)                       | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Zulässig-untergeordnete Klassen-gültig**](a-allowedchildclasseseffective.md)    | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Alt-Sicherheit-Identitäten**](a-altsecurityidentities.md)                   | False     | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/>                                 |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Kanonischer Name**](a-canonicalname.md)                                    | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Geäußert**](a-info.md)                                                    | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                         |
| [**Gemeinsamer Name**](a-cn.md)                                                  | Richtig      | [**Nach oben**](c-top.md)<br/> [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>         |
| [**Control-Access-Rights**](a-controlaccessrights.md)                       | False     | **Gruppieren**                                                                                    |
| [**Create-Zeitstempel**](a-createtimestamp.md)                               | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Beschreibung**](a-description.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Desktop Profil**](a-desktopprofile.md)                                  | False     | **Gruppieren**                                                                                    |
| [**Anzeige Name**](a-displayname.md)                                        | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Anzeige Name-druckdruck**](a-displaynameprintable.md)                     | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**DSA-Signatur**](a-dsasignature.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**DS-Core-propagierungs Daten**](a-dscorepropagationdata.md)                  | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**E-Mail-Adressen**](a-mail.md)                                           | False     | **Gruppieren**                                                                                    |
| [**Erweiterungs Name**](a-extensionname.md)                                    | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Fahren**](a-flags.md)                                                     | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Aus-Eintrag**](a-fromentry.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                    | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**"F"-Rollen Besitzer**](a-fsmoroleowner.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Garbage Koll-Zeitraum**](a-garbagecollperiod.md)                           | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                         |
| [**Group-Attribute**](a-groupattributes.md)                                | False     | **Gruppieren**                                                                                    |
| [**Gruppenmitgliedschaft: Sam**](a-groupmembershipsam.md)                         | False     | **Gruppieren**                                                                                    |
| [**Gruppentyp**](a-grouptype.md)                                            | Richtig      | **Gruppieren**                                                                                    |
| [**Instanztyp**](a-instancetype.md)                                      | Richtig      | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Is-critical-System-Object**](a-iscriticalsystemobject.md)                | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Ist-gelöscht**](a-isdeleted.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Is-Member-of-DL**](a-memberof.md)                                        | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Is-Privilege-Inhaber**](a-isprivilegeholder.md)                           | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Letztes-bekannt/übergeordnetes Element**](a-lastknownparent.md)                               | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Legacy-Exchange-DN**](a-legacyexchangedn.md)                             | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                         |
| [**Verwaltet von**](a-managedby.md)                                            | False     | **Gruppieren**                                                                                    |
| [**Verwaltete Objekte**](a-managedobjects.md)                                  | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Verwaltet von**](a-masteredby.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Member**](a-member.md)                                                   | False     | **Gruppieren**                                                                                    |
| [**Modify-Zeitstempel**](a-modifytimestamp.md)                               | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**MS-DS-Konsistenz-untergeordnet-Anzahl**](a-ms-ds-consistencychildcount.md)       | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                    | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**NetBoot-SCP-BL**](a-netbootscpbl.md)                                     | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Nicht sicherheitsmitglied**](a-nonsecuritymember.md)                           | False     | **Gruppieren**                                                                                    |
| [**Nicht sicherheitsmitglied-BL**](a-nonsecuritymemberbl.md)                      | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**NT-Gruppenmitglieder**](a-ntgroupmembers.md)                                 | False     | **Gruppieren**                                                                                    |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                     | Richtig      | [**Nach oben**](c-top.md)<br/> [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/> |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Objekt-Kategorie**](a-objectcategory.md)                                  | Richtig      | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Object-Klasse**](a-objectclass.md)                                        | Richtig      | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Objekt-GUID**](a-objectguid.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Objekt-sid**](a-objectsid.md)                                            | Richtig      | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/>                                 |
| [**Objekt-Version**](a-objectversion.md)                                    | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Operator-count**](a-operatorcount.md)                                    | False     | **Gruppieren**                                                                                    |
| [**Andere-bekannte Objekte**](a-otherwellknownobjects.md)                  | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Partial-Attribute-löschen-List**](a-partialattributedeletionlist.md)    | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Partiell-Attribut Satz**](a-partialattributeset.md)                       | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Mögliche-minderwertig**](a-possibleinferiors.md)                            | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Primary-Group-Token**](a-primarygrouptoken.md)                           | False     | **Gruppieren**                                                                                    |
| [**Proxy-Objekt Name**](a-proxiedobjectname.md)                           | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Proxy Adressen**](a-proxyaddresses.md)                                  | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Abfrage-Richtlinie-BL**](a-querypolicybl.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**RDN**](a-name.md)                                                        | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                    | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**REPL-Update-Vector**](a-repluptodatevector.md)                         | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Berichte**](a-directreports.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Reps-from**](a-repsfrom.md)                                              | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Reps-to**](a-repsto.md)                                                  | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Novel**](a-revision.md)                                               | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Gesagt**](a-rid.md)                                                         | False     | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/>                                 |
| [**Sam-Account-Name**](a-samaccountname.md)                                 | Richtig      | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/>                                 |
| [**Sam-Account-Type**](a-samaccounttype.md)                                 | False     | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/>                                 |
| [**SD-Rechte**](a-sdrightseffective.md)                           | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Sicherheits-ID**](a-securityidentifier.md)                          | False     | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/>                                 |
| [**Server-Reference-BL**](a-serverreferencebl.md)                           | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**In-Address-Book anzeigen**](a-showinaddressbook.md)                          | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                         |
| [**Anzeigen-in-Advanced-nur anzeigen**](a-showinadvancedviewonly.md)               | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**SID-Verlauf**](a-sidhistory.md)                                          | False     | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/>                                 |
| [**Site-Object-BL**](a-siteobjectbl.md)                                     | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Sub-Refs**](a-subrefs.md)                                                | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Subschemasubentry**](a-subschemasubentry.md)                             | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Ergänzende Anmelde Informationen**](a-supplementalcredentials.md)                | False     | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/>                                 |
| [**SystemFlags**](a-systemflags.md)                                        | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Telefonnummer**](a-telephonenumber.md)                                | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                         |
| [**Text-codiert-or-address**](a-textencodedoraddress.md)                    | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                         |
| [**Tokengruppen**](a-tokengroups.md)                                        | False     | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/>                                 |
| [**Token-Groups-Global-and-Universal**](a-tokengroupsglobalanduniversal.md) | False     | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/>                                 |
| [**Token-Groups-No-GC-akzeptabel**](a-tokengroupsnogcacceptable.md)         | False     | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/>                                 |
| [**Benutzerzertifikat**](a-usercert.md)                                              | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                         |
| [**Benutzersmime-Zertifikat**](a-usersmimecertificate.md)                     | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                         |
| [**Die Anwendung wurde geändert.**](a-usnchanged.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Von der Anwendung erstellte**](a-usncreated.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**USA-DSA-letzte-obj-entfernt**](a-usndsalastobjremoved.md)                   | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Standort-und standortübergreifende standortübergreifende**](a-usnintersite.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**"An-Last-obj-REM"**](a-usnlastobjrem.md)                                  | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Quell Code Quelle**](a-usnsource.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**WBEM-Pfad**](a-wbempath.md)                                              | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Bekannte Objekte**](a-wellknownobjects.md)                             | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Bei Änderung**](a-whenchanged.md)                                        | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Bei Erstellung**](a-whencreated.md)                                        | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**WWW-Homepage**](a-wwwhomepage.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**WWW-Page-other**](a-url.md)                                              | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**X509-CERT**](a-usercertificate.md)                                       | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                         |



## <a name="windows-2000-server-extended-rights"></a>Erweiterte Rechte für Windows 2000 Server

Diese Klasse enthält die folgenden erweiterten Rechte für Windows Server 2000-Server:



| Allgemeiner Name                  |
|------------------------------|
| [**Senden an**](r-send-to.md) |



## <a name="windows-2000-server-validated-writes"></a>Überprüfte Windows 2000-Server Schreibvorgänge

Diese Klasse enthält die folgenden validierten Schreibvorgänge für den Windows 2000-Server:



| Allgemeiner Name                                  |
|----------------------------------------------|
| [**Selbst Mitgliedschaft**](r-self-membership.md) |



## <a name="windows-2000-server-property-sets"></a>Eigenschaften Sätze für Windows 2000-Server

Diese Klasse enthält die folgenden Eigenschaften Sätze für Windows 2000 Server:



| Allgemeiner Name                                      |
|--------------------------------------------------|
| [**E-Mail-Informationen**](r-email-information.md) |



## <a name="windows-server-2003"></a>Windows Server 2003

-   [Attribute](#windows-server-2003-attributes)
-   [Erweiterte Rechte](#windows-server-2003-extended-rights)
-   [Überprüfte Schreibvorgänge](#windows-server-2003-validated-writes)
-   [Eigenschaftensätze](#windows-server-2003-property-sets)



| Eingabe | Wert |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | False                                                                                                                                                                                                                                                                                                            |
| Object-Category             | 1                                                                                                                                                                                                                                                                                                                |
| Default-Object-Category     | \-                                                                                                                                                                                                                                                                                                               |
| Governs-Id                  | 1.2.840.113556.1.5.8                                                                                                                                                                                                                                                                                             |
| Standard-ausblenden-Wert        | 0                                                                                                                                                                                                                                                                                                                |
| RDN-ATT-ID                  | [**Gemeinsamer Name**](a-cn.md)<br/>                                                                                                                                                                                                                                                                           |
| Unterklasse von                 | [**Nach oben**](c-top.md)<br/>                                                                                                                                                                                                                                                                                  |
| Mögliche Vorgesetzten          | [**Domäne-DNS**](c-domaindns.md)[**Organisationseinheit**](c-organizationalunit.md)[**BuiltIn-Domänen**](c-builtindomain.md)[**Container**](c-container.md)[**ms-DS-AZ-Admin-Manager**](c-msds-azadminmanager.md)[**ms-DS-AZ-Application**](c-msds-azapplication.md)[**ms-DS-AZ-Scope**](c-msds-azscope.md) |
| Zusätzlich           | [**Sicherheits Prinzipal**](c-securityprincipal.md) -e-[**Mail-Empfänger**](c-mailrecipient.md) (System)                                                                                                                                                                                                     |
| NT-Security-Descriptor      | o:Bag: schlecht: S:                                                                                                                                                                                                                                                                                                     |
| Standard Sicherheits Beschreibung | D: (A;; rpwpcrccdclclorcwowdsddtsw;;;D a) (a;; Rpwpcrccdclclorcwowdsddtsw;;; SY) (A;; Rplclorc;;; Au) (A;; Rpwpcrccdclclorcwowdsddtsw;;; AO) (A;; Rplclorc;;; PS) (OA;; CR; ab721a55-1e2f-11D0-9819-00aa0040529b;; Au) (OA;; RP; 46a9b11d-60ae-405a-b7e8-ff8a58d456d2;; S-1-5-32-560)                                                   |
| System-Flags                | 0x00000010                                                                                                                                                                                                                                                                                                       |



## <a name="windows-server-2003-attributes"></a>Windows Server 2003-Attribute

Diese Klasse enthält die folgenden Attribute für Windows Server 2003:



| Attribut                                                                    | Obligatorisch. | Abgeleitet von                                                                                 |
|------------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------|
| [**Konto Name-Verlauf**](a-accountnamehistory.md)                         | False     | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/>                                 |
| [**Admin: Anzahl**](a-admincount.md)                                          | False     | **Gruppieren**                                                                                    |
| [**Administrator: Beschreibung**](a-admindescription.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Administrator-Anzeige Name**](a-admindisplayname.md)                             | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Zulässige Attribute**](a-allowedattributes.md)                            | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Zulässige Attribute-gültig**](a-allowedattributeseffective.md)         | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Zulässige, untergeordnete Klassen**](a-allowedchildclasses.md)                       | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Zulässig-untergeordnete Klassen-gültig**](a-allowedchildclasseseffective.md)    | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Alt-Sicherheit-Identitäten**](a-altsecurityidentities.md)                   | False     | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/>                                 |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Kanonischer Name**](a-canonicalname.md)                                    | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Geäußert**](a-info.md)                                                    | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                         |
| [**Gemeinsamer Name**](a-cn.md)                                                  | Richtig      | [**Nach oben**](c-top.md)<br/> [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>         |
| [**Control-Access-Rights**](a-controlaccessrights.md)                       | False     | **Gruppieren**                                                                                    |
| [**Create-Zeitstempel**](a-createtimestamp.md)                               | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Beschreibung**](a-description.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Desktop Profil**](a-desktopprofile.md)                                  | False     | **Gruppieren**                                                                                    |
| [**Anzeige Name**](a-displayname.md)                                        | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Anzeige Name-druckdruck**](a-displaynameprintable.md)                     | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**DSA-Signatur**](a-dsasignature.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**DS-Core-propagierungs Daten**](a-dscorepropagationdata.md)                  | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**E-Mail-Adressen**](a-mail.md)                                           | False     | **Gruppieren**                                                                                    |
| [**Erweiterungs Name**](a-extensionname.md)                                    | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Fahren**](a-flags.md)                                                     | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Aus-Eintrag**](a-fromentry.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                    | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**"F"-Rollen Besitzer**](a-fsmoroleowner.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Garbage Koll-Zeitraum**](a-garbagecollperiod.md)                           | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                         |
| [**Group-Attribute**](a-groupattributes.md)                                | False     | **Gruppieren**                                                                                    |
| [**Gruppenmitgliedschaft: Sam**](a-groupmembershipsam.md)                         | False     | **Gruppieren**                                                                                    |
| [**Gruppentyp**](a-grouptype.md)                                            | Richtig      | **Gruppieren**                                                                                    |
| [**Instanztyp**](a-instancetype.md)                                      | Richtig      | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Is-critical-System-Object**](a-iscriticalsystemobject.md)                | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Ist-gelöscht**](a-isdeleted.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Is-Member-of-DL**](a-memberof.md)                                        | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Is-Privilege-Inhaber**](a-isprivilegeholder.md)                           | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**LabeledURI**](a-labeleduri.md)                                           | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                         |
| [**Letztes-bekannt/übergeordnetes Element**](a-lastknownparent.md)                               | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Legacy-Exchange-DN**](a-legacyexchangedn.md)                             | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                         |
| [**Verwaltet von**](a-managedby.md)                                            | False     | **Gruppieren**                                                                                    |
| [**Verwaltete Objekte**](a-managedobjects.md)                                  | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Verwaltet von**](a-masteredby.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Member**](a-member.md)                                                   | False     | **Gruppieren**                                                                                    |
| [**Modify-Zeitstempel**](a-modifytimestamp.md)                               | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**MS-com-partitionsetlink**](a-mscom-partitionsetlink.md)                  | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**MS-com-userlink**](a-mscom-userlink.md)                                  | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**ms-DS-ca-immed-untergeordnete Elemente**](a-msds-approx-immed-subordinates.md)  | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**ms-DS-AZ-LDAP-Query**](a-msds-azldapquery.md)                            | False     | **Gruppieren**                                                                                    |
| [**MS-DS-Konsistenz-untergeordnet-Anzahl**](a-ms-ds-consistencychildcount.md)       | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                    | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**ms-DS-keyversionnumber**](a-msds-keyversionnumber.md)                    | False     | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/>                                 |
| [**ms-DS-gemastert von**](a-msds-masteredby.md)                               | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**ms-DS-Members-für-AZ-Role-BL**](a-msds-membersforazrolebl.md)            | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**ms-DS-NC-repl-Cursor**](a-msds-ncreplcursors.md)                        | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**ms-DS-NC-repl-Inbound-Nachbarn**](a-msds-ncreplinboundneighbors.md)     | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**ms-DS-NC-repl-Outbound-Nachbarn**](a-msds-ncreploutboundneighbors.md)   | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**ms-DS-nicht-Member**](a-msds-nonmembers.md)                               | False     | **Gruppieren**                                                                                    |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                          | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)      | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)      | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**ms-DS-repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)       | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**ms-DS-repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)               | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**ms-DS-Tasks-für-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**ms-DS-Tasks-für-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**ms-Exch-Assistant-Name**](a-msexchassistantname.md)                      | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                         |
| [**ms-Exch-LabeledURI**](a-msexchlabeleduri.md)                             | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                         |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                        | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**NetBoot-SCP-BL**](a-netbootscpbl.md)                                     | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Nicht sicherheitsmitglied**](a-nonsecuritymember.md)                           | False     | **Gruppieren**                                                                                    |
| [**Nicht sicherheitsmitglied-BL**](a-nonsecuritymemberbl.md)                      | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**NT-Gruppenmitglieder**](a-ntgroupmembers.md)                                 | False     | **Gruppieren**                                                                                    |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                     | Richtig      | [**Nach oben**](c-top.md)<br/> [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/> |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Objekt-Kategorie**](a-objectcategory.md)                                  | Richtig      | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Object-Klasse**](a-objectclass.md)                                        | Richtig      | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Objekt-GUID**](a-objectguid.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Objekt-sid**](a-objectsid.md)                                            | Richtig      | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/>                                 |
| [**Objekt-Version**](a-objectversion.md)                                    | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Operator-count**](a-operatorcount.md)                                    | False     | **Gruppieren**                                                                                    |
| [**Andere-bekannte Objekte**](a-otherwellknownobjects.md)                  | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Partial-Attribute-löschen-List**](a-partialattributedeletionlist.md)    | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Partiell-Attribut Satz**](a-partialattributeset.md)                       | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Mögliche-minderwertig**](a-possibleinferiors.md)                            | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Primary-Group-Token**](a-primarygrouptoken.md)                           | False     | **Gruppieren**                                                                                    |
| [**Proxy-Objekt Name**](a-proxiedobjectname.md)                           | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Proxy Adressen**](a-proxyaddresses.md)                                  | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Abfrage-Richtlinie-BL**](a-querypolicybl.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**RDN**](a-name.md)                                                        | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                    | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**REPL-Update-Vector**](a-repluptodatevector.md)                         | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Berichte**](a-directreports.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Reps-from**](a-repsfrom.md)                                              | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Reps-to**](a-repsto.md)                                                  | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Novel**](a-revision.md)                                               | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Gesagt**](a-rid.md)                                                         | False     | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/>                                 |
| [**Sam-Account-Name**](a-samaccountname.md)                                 | Richtig      | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/>                                 |
| [**Sam-Account-Type**](a-samaccounttype.md)                                 | False     | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/>                                 |
| [**SD-Rechte**](a-sdrightseffective.md)                           | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**secretary**](a-secretary.md)                                             | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                         |
| [**Sicherheits-ID**](a-securityidentifier.md)                          | False     | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/>                                 |
| [**Server-Reference-BL**](a-serverreferencebl.md)                           | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**In-Address-Book anzeigen**](a-showinaddressbook.md)                          | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                         |
| [**Anzeigen-in-Advanced-nur anzeigen**](a-showinadvancedviewonly.md)               | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**SID-Verlauf**](a-sidhistory.md)                                          | False     | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/>                                 |
| [**Site-Object-BL**](a-siteobjectbl.md)                                     | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Struktur-Objekt-Klasse**](a-structuralobjectclass.md)                   | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Sub-Refs**](a-subrefs.md)                                                | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Subschemasubentry**](a-subschemasubentry.md)                             | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Ergänzende Anmelde Informationen**](a-supplementalcredentials.md)                | False     | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/>                                 |
| [**SystemFlags**](a-systemflags.md)                                        | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Telefonnummer**](a-telephonenumber.md)                                | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                         |
| [**Text-codiert-or-address**](a-textencodedoraddress.md)                    | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                         |
| [**Tokengruppen**](a-tokengroups.md)                                        | False     | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/>                                 |
| [**Token-Groups-Global-and-Universal**](a-tokengroupsglobalanduniversal.md) | False     | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/>                                 |
| [**Token-Groups-No-GC-akzeptabel**](a-tokengroupsnogcacceptable.md)         | False     | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/>                                 |
| [**Benutzerzertifikat**](a-usercert.md)                                              | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                         |
| [**Benutzersmime-Zertifikat**](a-usersmimecertificate.md)                     | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                         |
| [**Die Anwendung wurde geändert.**](a-usnchanged.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Von der Anwendung erstellte**](a-usncreated.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**USA-DSA-letzte-obj-entfernt**](a-usndsalastobjremoved.md)                   | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Standort-und standortübergreifende standortübergreifende**](a-usnintersite.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**"An-Last-obj-REM"**](a-usnlastobjrem.md)                                  | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Quell Code Quelle**](a-usnsource.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**WBEM-Pfad**](a-wbempath.md)                                              | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Bekannte Objekte**](a-wellknownobjects.md)                             | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Bei Änderung**](a-whenchanged.md)                                        | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Bei Erstellung**](a-whencreated.md)                                        | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**WWW-Homepage**](a-wwwhomepage.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**WWW-Page-other**](a-url.md)                                              | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**X509-CERT**](a-usercertificate.md)                                       | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                         |



## <a name="windows-server-2003-extended-rights"></a>Erweiterte Rechte für Windows Server 2003

Diese Klasse enthält die folgenden erweiterten Rechte für Windows Server 2003:



| Allgemeiner Name                  |
|------------------------------|
| [**Senden an**](r-send-to.md) |



## <a name="windows-server-2003-validated-writes"></a>Windows Server 2003 validierte Schreibvorgänge

Diese Klasse enthält die folgenden validierten Schreibvorgänge für Windows Server 2003:



| Allgemeiner Name                                  |
|----------------------------------------------|
| [**Selbst Mitgliedschaft**](r-self-membership.md) |



## <a name="windows-server-2003-property-sets"></a>Windows Server 2003-Eigenschaften Sätze

Diese Klasse enthält die folgenden Eigenschaften Sätze für Windows Server 2003:



| Allgemeiner Name                                      |
|--------------------------------------------------|
| [**E-Mail-Informationen**](r-email-information.md) |



## <a name="adam"></a>Adam

-   [Attribute](#adam-attributes)
-   [Überprüfte Schreibvorgänge](#adam-validated-writes)
-   [Eigenschaftensätze](#adam-property-sets)



| Eingabe | Wert |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------|
| System-Only                 | False                                                                                                                |
| Object-Category             | 1                                                                                                                    |
| Default-Object-Category     | \-                                                                                                                   |
| Governs-Id                  | 1.2.840.113556.1.5.8                                                                                                 |
| Standard-ausblenden-Wert        | 0                                                                                                                    |
| RDN-ATT-ID                  | [**Gemeinsamer Name**](a-cn.md)<br/>                                                                               |
| Unterklasse von                 | [**Nach oben**](c-top.md)<br/>                                                                                      |
| Mögliche Vorgesetzten          | [**Domänen-DNS**](c-domaindns.md)-[**Container**](c-container.md) für [**Organisationseinheiten**](c-organizationalunit.md) |
| Zusätzlich           | [**Sicherheits Prinzipal**](c-securityprincipal.md) (System)                                                           |
| NT-Security-Descriptor      | o:Bag: schlecht: S:                                                                                                         |
| Standard Sicherheits Beschreibung | d:s:                                                                                                                 |
| System-Flags                | 0x00000010                                                                                                           |



## <a name="adam-attributes"></a>Adam-Attribute

Diese Klasse enthält die folgenden Attribute für Adam:



| Attribut                                                                   | Obligatorisch. | Abgeleitet von                                                                                 |
|-----------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------|
| [**Administrator: Beschreibung**](a-admindescription.md)                             | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Administrator-Anzeige Name**](a-admindisplayname.md)                            | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Zulässige Attribute**](a-allowedattributes.md)                           | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Zulässige Attribute-gültig**](a-allowedattributeseffective.md)        | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Zulässige, untergeordnete Klassen**](a-allowedchildclasses.md)                      | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Zulässig-untergeordnete Klassen-gültig**](a-allowedchildclasseseffective.md)   | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)               | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Kanonischer Name**](a-canonicalname.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Gemeinsamer Name**](a-cn.md)                                                 | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Create-Zeitstempel**](a-createtimestamp.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Beschreibung**](a-description.md)                                        | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Desktop Profil**](a-desktopprofile.md)                                 | False     | **Gruppieren**                                                                                    |
| [**Anzeige Name**](a-displayname.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**DSA-Signatur**](a-dsasignature.md)                                     | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**DS-Core-propagierungs Daten**](a-dscorepropagationdata.md)                 | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Aus-Eintrag**](a-fromentry.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**"F"-Rollen Besitzer**](a-fsmoroleowner.md)                                  | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Gruppentyp**](a-grouptype.md)                                           | Richtig      | **Gruppieren**                                                                                    |
| [**Instanztyp**](a-instancetype.md)                                     | Richtig      | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Is-critical-System-Object**](a-iscriticalsystemobject.md)               | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Ist-gelöscht**](a-isdeleted.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Is-Member-of-DL**](a-memberof.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Letztes-bekannt/übergeordnetes Element**](a-lastknownparent.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Verwaltet von**](a-managedby.md)                                           | False     | **Gruppieren**                                                                                    |
| [**Verwaltete Objekte**](a-managedobjects.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Verwaltet von**](a-masteredby.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Member**](a-member.md)                                                  | False     | **Gruppieren**                                                                                    |
| [**Modify-Zeitstempel**](a-modifytimestamp.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**ms-DS-ca-immed-untergeordnete Elemente**](a-msds-approx-immed-subordinates.md) | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**MS-DS-Konsistenz-untergeordnet-Anzahl**](a-ms-ds-consistencychildcount.md)      | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**ms-DS-deaktivieren-für-Instanzen-BL**](a-msds-disableforinstancesbl.md)      | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**ms-DS-gemastert von**](a-msds-masteredby.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**ms-DS-NC-repl-Cursor**](a-msds-ncreplcursors.md)                       | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**ms-DS-NC-repl-Inbound-Nachbarn**](a-msds-ncreplinboundneighbors.md)    | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**ms-DS-NC-repl-Outbound-Nachbarn**](a-msds-ncreploutboundneighbors.md)  | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**ms-DS-repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)      | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**ms-DS-repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)              | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**ms-DS-Service-Account-BL**](a-msds-serviceaccountbl.md)                 | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                    | Richtig      | [**Nach oben**](c-top.md)<br/> [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/> |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Objekt-Kategorie**](a-objectcategory.md)                                 | Richtig      | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Object-Klasse**](a-objectclass.md)                                       | Richtig      | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Objekt-GUID**](a-objectguid.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Objekt-sid**](a-objectsid.md)                                           | Richtig      | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/>                                 |
| [**Objekt-Version**](a-objectversion.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Andere-bekannte Objekte**](a-otherwellknownobjects.md)                 | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Partial-Attribute-löschen-List**](a-partialattributedeletionlist.md)   | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Partiell-Attribut Satz**](a-partialattributeset.md)                      | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Mögliche-minderwertig**](a-possibleinferiors.md)                           | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Primary-Group-Token**](a-primarygrouptoken.md)                          | False     | **Gruppieren**                                                                                    |
| [**Proxy-Objekt Name**](a-proxiedobjectname.md)                          | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Proxy Adressen**](a-proxyaddresses.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Abfrage-Richtlinie-BL**](a-querypolicybl.md)                                  | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**RDN**](a-name.md)                                                       | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                   | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**REPL-Update-Vector**](a-repluptodatevector.md)                        | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Reps-from**](a-repsfrom.md)                                             | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Reps-to**](a-repsto.md)                                                 | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Novel**](a-revision.md)                                              | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**SD-Rechte**](a-sdrightseffective.md)                          | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Server-Reference-BL**](a-serverreferencebl.md)                          | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Anzeigen-in-Advanced-nur anzeigen**](a-showinadvancedviewonly.md)              | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Struktur-Objekt-Klasse**](a-structuralobjectclass.md)                  | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Sub-Refs**](a-subrefs.md)                                               | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Subschemasubentry**](a-subschemasubentry.md)                            | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Ergänzende Anmelde Informationen**](a-supplementalcredentials.md)               | False     | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/>                                 |
| [**SystemFlags**](a-systemflags.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Tokengruppen**](a-tokengroups.md)                                       | False     | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/>                                 |
| [**Die Anwendung wurde geändert.**](a-usnchanged.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Von der Anwendung erstellte**](a-usncreated.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**USA-DSA-letzte-obj-entfernt**](a-usndsalastobjremoved.md)                  | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Standort-und standortübergreifende standortübergreifende**](a-usnintersite.md)                                     | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**"An-Last-obj-REM"**](a-usnlastobjrem.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Quell Code Quelle**](a-usnsource.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**WBEM-Pfad**](a-wbempath.md)                                             | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Bekannte Objekte**](a-wellknownobjects.md)                            | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Bei Änderung**](a-whenchanged.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Bei Erstellung**](a-whencreated.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**WWW-Homepage**](a-wwwhomepage.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**WWW-Page-other**](a-url.md)                                             | False     | [**Nach oben**](c-top.md)<br/>                                                              |



## <a name="adam-validated-writes"></a>Adam validierte Schreibvorgänge

Diese Klasse enthält die folgenden validierten Schreibvorgänge für Adam:



| Allgemeiner Name                                  |
|----------------------------------------------|
| [**Selbst Mitgliedschaft**](r-self-membership.md) |



## <a name="adam-property-sets"></a>Adam-Eigenschaften Sätze

Diese Klasse enthält die folgenden Eigenschaften Sätze für Adam:



| Allgemeiner Name                                      |
|--------------------------------------------------|
| [**E-Mail-Informationen**](r-email-information.md) |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2

-   [Attribute](#windows-server-2003-r2-attributes)
-   [Erweiterte Rechte](#windows-server-2003-r2-extended-rights)
-   [Überprüfte Schreibvorgänge](#windows-server-2003-r2-validated-writes)
-   [Eigenschaftensätze](#windows-server-2003-r2-property-sets)



| Eingabe | Wert |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | False                                                                                                                                                                                                                                                                                                            |
| Object-Category             | 1                                                                                                                                                                                                                                                                                                                |
| Default-Object-Category     | \-                                                                                                                                                                                                                                                                                                               |
| Governs-Id                  | 1.2.840.113556.1.5.8                                                                                                                                                                                                                                                                                             |
| Standard-ausblenden-Wert        | 0                                                                                                                                                                                                                                                                                                                |
| RDN-ATT-ID                  | [**Gemeinsamer Name**](a-cn.md)<br/>                                                                                                                                                                                                                                                                           |
| Unterklasse von                 | [**Nach oben**](c-top.md)<br/>                                                                                                                                                                                                                                                                                  |
| Mögliche Vorgesetzten          | [**Domäne-DNS**](c-domaindns.md)[**Organisationseinheit**](c-organizationalunit.md)[**BuiltIn-Domänen**](c-builtindomain.md)[**Container**](c-container.md)[**ms-DS-AZ-Admin-Manager**](c-msds-azadminmanager.md)[**ms-DS-AZ-Application**](c-msds-azapplication.md)[**ms-DS-AZ-Scope**](c-msds-azscope.md) |
| Zusätzlich           | [**posixgroup**](c-posixgroup.md)[**-Sicherheits Prinzipal**](c-securityprincipal.md) (System)[**Mail-Empfänger**](c-mailrecipient.md) (System)                                                                                                                                                                   |
| NT-Security-Descriptor      | o:Bag: schlecht: S:                                                                                                                                                                                                                                                                                                     |
| Standard Sicherheits Beschreibung | D: (A;; rpwpcrccdclclorcwowdsddtsw;;;D a) (a;; Rpwpcrccdclclorcwowdsddtsw;;; SY) (A;; Rplclorc;;; Au) (A;; Rpwpcrccdclclorcwowdsddtsw;;; AO) (A;; Rplclorc;;; PS) (OA;; CR; ab721a55-1e2f-11D0-9819-00aa0040529b;; Au) (OA;; RP; 46a9b11d-60ae-405a-b7e8-ff8a58d456d2;; S-1-5-32-560)                                                   |
| System-Flags                | 0x00000010                                                                                                                                                                                                                                                                                                       |



## <a name="windows-server-2003-r2-attributes"></a>Windows Server 2003 R2-Attribute

Diese Klasse enthält die folgenden Attribute für Windows Server 2003 R2:



| Attribut                                                                    | Obligatorisch. | Abgeleitet von                                                                                                                       |
|------------------------------------------------------------------------------|-----------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Konto Name-Verlauf**](a-accountnamehistory.md)                         | False     | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**Admin: Anzahl**](a-admincount.md)                                          | False     | **Gruppieren**                                                                                                                          |
| [**Administrator: Beschreibung**](a-admindescription.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Administrator-Anzeige Name**](a-admindisplayname.md)                             | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Zulässige Attribute**](a-allowedattributes.md)                            | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Zulässige Attribute-gültig**](a-allowedattributeseffective.md)         | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Zulässige, untergeordnete Klassen**](a-allowedchildclasses.md)                       | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Zulässig-untergeordnete Klassen-gültig**](a-allowedchildclasseseffective.md)    | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Alt-Sicherheit-Identitäten**](a-altsecurityidentities.md)                   | False     | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Kanonischer Name**](a-canonicalname.md)                                    | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Geäußert**](a-info.md)                                                    | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**Gemeinsamer Name**](a-cn.md)                                                  | Richtig      | [**Nach oben**](c-top.md)<br/> [**posixgroup**](c-posixgroup.md)<br/> [**E-Mail-Empfänger**](c-mailrecipient.md)<br/> |
| [**Control-Access-Rights**](a-controlaccessrights.md)                       | False     | **Gruppieren**                                                                                                                          |
| [**Create-Zeitstempel**](a-createtimestamp.md)                               | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Beschreibung**](a-description.md)                                         | False     | [**Nach oben**](c-top.md)<br/> [**posixgroup**](c-posixgroup.md)<br/>                                                      |
| [**Desktop Profil**](a-desktopprofile.md)                                  | False     | **Gruppieren**                                                                                                                          |
| [**Anzeige Name**](a-displayname.md)                                        | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Anzeige Name-druckdruck**](a-displaynameprintable.md)                     | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**DSA-Signatur**](a-dsasignature.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**DS-Core-propagierungs Daten**](a-dscorepropagationdata.md)                  | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**E-Mail-Adressen**](a-mail.md)                                           | False     | **Gruppieren**                                                                                                                          |
| [**Erweiterungs Name**](a-extensionname.md)                                    | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Fahren**](a-flags.md)                                                     | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Aus-Eintrag**](a-fromentry.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                    | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**"F"-Rollen Besitzer**](a-fsmoroleowner.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Garbage Koll-Zeitraum**](a-garbagecollperiod.md)                           | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**gidNumber**](a-gidnumber.md)                                             | False     | [**posixgroup**](c-posixgroup.md)<br/>                                                                                      |
| [**Group-Attribute**](a-groupattributes.md)                                | False     | **Gruppieren**                                                                                                                          |
| [**Gruppenmitgliedschaft: Sam**](a-groupmembershipsam.md)                         | False     | **Gruppieren**                                                                                                                          |
| [**Gruppentyp**](a-grouptype.md)                                            | Richtig      | **Gruppieren**                                                                                                                          |
| [**Instanztyp**](a-instancetype.md)                                      | Richtig      | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Is-critical-System-Object**](a-iscriticalsystemobject.md)                | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Ist-gelöscht**](a-isdeleted.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Is-Member-of-DL**](a-memberof.md)                                        | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Is-Privilege-Inhaber**](a-isprivilegeholder.md)                           | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**LabeledURI**](a-labeleduri.md)                                           | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**Letztes-bekannt/übergeordnetes Element**](a-lastknownparent.md)                               | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Legacy-Exchange-DN**](a-legacyexchangedn.md)                             | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**Verwaltet von**](a-managedby.md)                                            | False     | **Gruppieren**                                                                                                                          |
| [**Verwaltete Objekte**](a-managedobjects.md)                                  | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Verwaltet von**](a-masteredby.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Member**](a-member.md)                                                   | False     | **Gruppieren**                                                                                                                          |
| [**memberuid**](a-memberuid.md)                                             | False     | [**posixgroup**](c-posixgroup.md)<br/>                                                                                      |
| [**Modify-Zeitstempel**](a-modifytimestamp.md)                               | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**MS-com-partitionsetlink**](a-mscom-partitionsetlink.md)                  | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**MS-com-userlink**](a-mscom-userlink.md)                                  | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**MS-DFSR-computerreferencebl**](a-msdfsr-computerreferencebl.md)          | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**MS-DFSR-mitgliedreferencebl**](a-msdfsr-memberreferencebl.md)              | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-ca-immed-untergeordnete Elemente**](a-msds-approx-immed-subordinates.md)  | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-AZ-LDAP-Query**](a-msds-azldapquery.md)                            | False     | **Gruppieren**                                                                                                                          |
| [**MS-DS-Konsistenz-untergeordnet-Anzahl**](a-ms-ds-consistencychildcount.md)       | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                    | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-keyversionnumber**](a-msds-keyversionnumber.md)                    | False     | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**ms-DS-gemastert von**](a-msds-masteredby.md)                               | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Members-für-AZ-Role-BL**](a-msds-membersforazrolebl.md)            | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-repl-Cursor**](a-msds-ncreplcursors.md)                        | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-repl-Inbound-Nachbarn**](a-msds-ncreplinboundneighbors.md)     | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-repl-Outbound-Nachbarn**](a-msds-ncreploutboundneighbors.md)   | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-nicht-Member**](a-msds-nonmembers.md)                               | False     | **Gruppieren**                                                                                                                          |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                          | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)      | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)      | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)       | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)               | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Tasks-für-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Tasks-für-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-Exch-Assistant-Name**](a-msexchassistantname.md)                      | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-Exch-LabeledURI**](a-msexchlabeleduri.md)                             | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                        | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**msSFU-30: Name**](a-mssfu30name.md)                                       | False     | **Gruppieren**                                                                                                                          |
| [**msSFU-30-NIS-Domäne**](a-mssfu30nisdomain.md)                            | False     | **Gruppieren**                                                                                                                          |
| [**msSFU-30-POSIX-Member**](a-mssfu30posixmember.md)                        | False     | **Gruppieren**                                                                                                                          |
| [**msSFU-30-POSIX-Member-of**](a-mssfu30posixmemberof.md)                   | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**NetBoot-SCP-BL**](a-netbootscpbl.md)                                     | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Nicht sicherheitsmitglied**](a-nonsecuritymember.md)                           | False     | **Gruppieren**                                                                                                                          |
| [**Nicht sicherheitsmitglied-BL**](a-nonsecuritymemberbl.md)                      | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**NT-Gruppenmitglieder**](a-ntgroupmembers.md)                                 | False     | **Gruppieren**                                                                                                                          |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                     | Richtig      | [**Nach oben**](c-top.md)<br/> [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/>                                       |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Objekt-Kategorie**](a-objectcategory.md)                                  | Richtig      | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Object-Klasse**](a-objectclass.md)                                        | Richtig      | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Objekt-GUID**](a-objectguid.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Objekt-sid**](a-objectsid.md)                                            | Richtig      | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**Objekt-Version**](a-objectversion.md)                                    | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Operator-count**](a-operatorcount.md)                                    | False     | **Gruppieren**                                                                                                                          |
| [**Andere-bekannte Objekte**](a-otherwellknownobjects.md)                  | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Partial-Attribute-löschen-List**](a-partialattributedeletionlist.md)    | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Partiell-Attribut Satz**](a-partialattributeset.md)                       | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Mögliche-minderwertig**](a-possibleinferiors.md)                            | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Primary-Group-Token**](a-primarygrouptoken.md)                           | False     | **Gruppieren**                                                                                                                          |
| [**Proxy-Objekt Name**](a-proxiedobjectname.md)                           | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Proxy Adressen**](a-proxyaddresses.md)                                  | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Abfrage-Richtlinie-BL**](a-querypolicybl.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**RDN**](a-name.md)                                                        | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                    | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**REPL-Update-Vector**](a-repluptodatevector.md)                         | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Berichte**](a-directreports.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Reps-from**](a-repsfrom.md)                                              | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Reps-to**](a-repsto.md)                                                  | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Novel**](a-revision.md)                                               | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Gesagt**](a-rid.md)                                                         | False     | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**Sam-Account-Name**](a-samaccountname.md)                                 | Richtig      | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**Sam-Account-Type**](a-samaccounttype.md)                                 | False     | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**SD-Rechte**](a-sdrightseffective.md)                           | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**secretary**](a-secretary.md)                                             | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**Sicherheits-ID**](a-securityidentifier.md)                          | False     | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**Server-Reference-BL**](a-serverreferencebl.md)                           | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**In-Address-Book anzeigen**](a-showinaddressbook.md)                          | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**Anzeigen-in-Advanced-nur anzeigen**](a-showinadvancedviewonly.md)               | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**SID-Verlauf**](a-sidhistory.md)                                          | False     | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**Site-Object-BL**](a-siteobjectbl.md)                                     | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Struktur-Objekt-Klasse**](a-structuralobjectclass.md)                   | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Sub-Refs**](a-subrefs.md)                                                | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Subschemasubentry**](a-subschemasubentry.md)                             | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Ergänzende Anmelde Informationen**](a-supplementalcredentials.md)                | False     | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**SystemFlags**](a-systemflags.md)                                        | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Telefonnummer**](a-telephonenumber.md)                                | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**Text-codiert-or-address**](a-textencodedoraddress.md)                    | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**Tokengruppen**](a-tokengroups.md)                                        | False     | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**Token-Groups-Global-and-Universal**](a-tokengroupsglobalanduniversal.md) | False     | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**Token-Groups-No-GC-akzeptabel**](a-tokengroupsnogcacceptable.md)         | False     | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**unixUserPassword**](a-unixuserpassword.md)                               | False     | [**posixgroup**](c-posixgroup.md)<br/>                                                                                      |
| [**Benutzerzertifikat**](a-usercert.md)                                              | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**Benutzer Kennwort**](a-userpassword.md)                                      | False     | [**posixgroup**](c-posixgroup.md)<br/>                                                                                      |
| [**Benutzersmime-Zertifikat**](a-usersmimecertificate.md)                     | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**Die Anwendung wurde geändert.**](a-usnchanged.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Von der Anwendung erstellte**](a-usncreated.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**USA-DSA-letzte-obj-entfernt**](a-usndsalastobjremoved.md)                   | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Standort-und standortübergreifende standortübergreifende**](a-usnintersite.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**"An-Last-obj-REM"**](a-usnlastobjrem.md)                                  | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Quell Code Quelle**](a-usnsource.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**WBEM-Pfad**](a-wbempath.md)                                              | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Bekannte Objekte**](a-wellknownobjects.md)                             | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Bei Änderung**](a-whenchanged.md)                                        | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Bei Erstellung**](a-whencreated.md)                                        | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**WWW-Homepage**](a-wwwhomepage.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**WWW-Page-other**](a-url.md)                                              | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**X509-CERT**](a-usercertificate.md)                                       | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |



## <a name="windows-server-2003-r2-extended-rights"></a>Erweiterte Rechte für Windows Server 2003 R2

Diese Klasse enthält die folgenden erweiterten Rechte für Windows Server 2003 R2:



| Allgemeiner Name                  |
|------------------------------|
| [**Senden an**](r-send-to.md) |



## <a name="windows-server-2003-r2-validated-writes"></a>Windows Server 2003 R2 validierte Schreibvorgänge

Diese Klasse enthält die folgenden validierten Schreibvorgänge für Windows Server 2003 R2:



| Allgemeiner Name                                  |
|----------------------------------------------|
| [**Selbst Mitgliedschaft**](r-self-membership.md) |



## <a name="windows-server-2003-r2-property-sets"></a>Windows Server 2003 R2-Eigenschaften Sätze

Diese Klasse enthält die folgenden Eigenschaften Sätze für Windows Server 2003 R2:



| Allgemeiner Name                                      |
|--------------------------------------------------|
| [**E-Mail-Informationen**](r-email-information.md) |



## <a name="windows-server-2008"></a>Windows Server 2008

-   [Attribute](#windows-server-2008-attributes)
-   [Erweiterte Rechte](#windows-server-2008-extended-rights)
-   [Überprüfte Schreibvorgänge](#windows-server-2008-validated-writes)
-   [Eigenschaftensätze](#windows-server-2008-property-sets)



| Eingabe | Wert |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | False                                                                                                                                                                                                                                                                                                            |
| Object-Category             | 1                                                                                                                                                                                                                                                                                                                |
| Default-Object-Category     | \-                                                                                                                                                                                                                                                                                                               |
| Governs-Id                  | 1.2.840.113556.1.5.8                                                                                                                                                                                                                                                                                             |
| Standard-ausblenden-Wert        | 0                                                                                                                                                                                                                                                                                                                |
| RDN-ATT-ID                  | [**Gemeinsamer Name**](a-cn.md)<br/>                                                                                                                                                                                                                                                                           |
| Unterklasse von                 | [**Nach oben**](c-top.md)<br/>                                                                                                                                                                                                                                                                                  |
| Mögliche Vorgesetzten          | [**Domäne-DNS**](c-domaindns.md)[**Organisationseinheit**](c-organizationalunit.md)[**BuiltIn-Domänen**](c-builtindomain.md)[**Container**](c-container.md)[**ms-DS-AZ-Admin-Manager**](c-msds-azadminmanager.md)[**ms-DS-AZ-Application**](c-msds-azapplication.md)[**ms-DS-AZ-Scope**](c-msds-azscope.md) |
| Zusätzlich           | [**posixgroup**](c-posixgroup.md)[**-Sicherheits Prinzipal**](c-securityprincipal.md) (System)[**Mail-Empfänger**](c-mailrecipient.md) (System)                                                                                                                                                                   |
| NT-Security-Descriptor      | o:Bag: schlecht: S:                                                                                                                                                                                                                                                                                                     |
| Standard Sicherheits Beschreibung | D: (A;; rpwpcrccdclclorcwowdsddtsw;;;D a) (a;; Rpwpcrccdclclorcwowdsddtsw;;; SY) (A;; Rplclorc;;; Au) (A;; Rpwpcrccdclclorcwowdsddtsw;;; AO) (A;; Rplclorc;;; PS) (OA;; CR; ab721a55-1e2f-11D0-9819-00aa0040529b;; Au) (OA;; RP; 46a9b11d-60ae-405a-b7e8-ff8a58d456d2;; S-1-5-32-560)                                                   |
| System-Flags                | 0x00000010                                                                                                                                                                                                                                                                                                       |



## <a name="windows-server-2008-attributes"></a>Windows Server 2008-Attribute

Diese Klasse enthält die folgenden Attribute für Windows Server 2008:



| Attribut                                                                        | Obligatorisch. | Abgeleitet von                                                                                                                       |
|----------------------------------------------------------------------------------|-----------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Konto Name-Verlauf**](a-accountnamehistory.md)                             | False     | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**Admin: Anzahl**](a-admincount.md)                                              | False     | **Gruppieren**                                                                                                                          |
| [**Administrator: Beschreibung**](a-admindescription.md)                                  | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Administrator-Anzeige Name**](a-admindisplayname.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Zulässige Attribute**](a-allowedattributes.md)                                | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Zulässige Attribute-gültig**](a-allowedattributeseffective.md)             | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Zulässige, untergeordnete Klassen**](a-allowedchildclasses.md)                           | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Zulässig-untergeordnete Klassen-gültig**](a-allowedchildclasseseffective.md)        | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Alt-Sicherheit-Identitäten**](a-altsecurityidentities.md)                       | False     | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                    | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Kanonischer Name**](a-canonicalname.md)                                        | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Geäußert**](a-info.md)                                                        | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**Gemeinsamer Name**](a-cn.md)                                                      | Richtig      | [**Nach oben**](c-top.md)<br/> [**posixgroup**](c-posixgroup.md)<br/> [**E-Mail-Empfänger**](c-mailrecipient.md)<br/> |
| [**Control-Access-Rights**](a-controlaccessrights.md)                           | False     | **Gruppieren**                                                                                                                          |
| [**Create-Zeitstempel**](a-createtimestamp.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Beschreibung**](a-description.md)                                             | False     | [**Nach oben**](c-top.md)<br/> [**posixgroup**](c-posixgroup.md)<br/>                                                      |
| [**Desktop Profil**](a-desktopprofile.md)                                      | False     | **Gruppieren**                                                                                                                          |
| [**Anzeige Name**](a-displayname.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Anzeige Name-druckdruck**](a-displaynameprintable.md)                         | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**DSA-Signatur**](a-dsasignature.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**DS-Core-propagierungs Daten**](a-dscorepropagationdata.md)                      | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**E-Mail-Adressen**](a-mail.md)                                               | False     | **Gruppieren**                                                                                                                          |
| [**Erweiterungs Name**](a-extensionname.md)                                        | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Fahren**](a-flags.md)                                                         | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Aus-Eintrag**](a-fromentry.md)                                                | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                    | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                        | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**"F"-Rollen Besitzer**](a-fsmoroleowner.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Garbage Koll-Zeitraum**](a-garbagecollperiod.md)                               | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**gidNumber**](a-gidnumber.md)                                                 | False     | [**posixgroup**](c-posixgroup.md)<br/>                                                                                      |
| [**Group-Attribute**](a-groupattributes.md)                                    | False     | **Gruppieren**                                                                                                                          |
| [**Gruppenmitgliedschaft: Sam**](a-groupmembershipsam.md)                             | False     | **Gruppieren**                                                                                                                          |
| [**Gruppentyp**](a-grouptype.md)                                                | Richtig      | **Gruppieren**                                                                                                                          |
| [**Instanztyp**](a-instancetype.md)                                          | Richtig      | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Is-critical-System-Object**](a-iscriticalsystemobject.md)                    | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Ist-gelöscht**](a-isdeleted.md)                                                | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Is-Member-of-DL**](a-memberof.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Is-Privilege-Inhaber**](a-isprivilegeholder.md)                               | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**LabeledURI**](a-labeleduri.md)                                               | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**Letztes-bekannt/übergeordnetes Element**](a-lastknownparent.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Legacy-Exchange-DN**](a-legacyexchangedn.md)                                 | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**Verwaltet von**](a-managedby.md)                                                | False     | **Gruppieren**                                                                                                                          |
| [**Verwaltete Objekte**](a-managedobjects.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Verwaltet von**](a-masteredby.md)                                              | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Member**](a-member.md)                                                       | False     | **Gruppieren**                                                                                                                          |
| [**memberuid**](a-memberuid.md)                                                 | False     | [**posixgroup**](c-posixgroup.md)<br/>                                                                                      |
| [**Modify-Zeitstempel**](a-modifytimestamp.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**MS-com-partitionsetlink**](a-mscom-partitionsetlink.md)                      | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**MS-com-userlink**](a-mscom-userlink.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**MS-DFSR-computerreferencebl**](a-msdfsr-computerreferencebl.md)              | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**MS-DFSR-mitgliedreferencebl**](a-msdfsr-memberreferencebl.md)                  | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-ca-immed-untergeordnete Elemente**](a-msds-approx-immed-subordinates.md)      | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-authentieredto-accountlist**](a-msds-authenticatedtoaccountlist.md)   | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-AZ-Application-Data**](a-msds-azapplicationdata.md)                    | False     | **Gruppieren**                                                                                                                          |
| [**ms-DS-AZ-BIZ-Rule**](a-msds-azbizrule.md)                                    | False     | **Gruppieren**                                                                                                                          |
| [**ms-DS-AZ-BIZ-Rule-Language**](a-msds-azbizrulelanguage.md)                   | False     | **Gruppieren**                                                                                                                          |
| [**ms-DS-AZ-Generic-Data**](a-msds-azgenericdata.md)                            | False     | **Gruppieren**                                                                                                                          |
| [**ms-DS-AZ-Last-Import-BIZ-Rule-Path**](a-msds-azlastimportedbizrulepath.md) | False     | **Gruppieren**                                                                                                                          |
| [**ms-DS-AZ-LDAP-Query**](a-msds-azldapquery.md)                                | False     | **Gruppieren**                                                                                                                          |
| [**ms-DS-AZ-Object-GUID**](a-msds-azobjectguid.md)                              | False     | **Gruppieren**                                                                                                                          |
| [**MS-DS-Konsistenz-untergeordnet-Anzahl**](a-ms-ds-consistencychildcount.md)           | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                        | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-is-Domain-for**](a-msds-isdomainfor.md)                                | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-is-full-Replica-for**](a-msds-isfullreplicafor.md)                     | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-is-Partial-Replica-for**](a-msds-ispartialreplicafor.md)               | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-keyversionnumber**](a-msds-keyversionnumber.md)                        | False     | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**ms-DS-krbtgt-Link-BL**](a-msds-krbtgtlinkbl.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-gemastert von**](a-msds-masteredby.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Members-für-AZ-Role-BL**](a-msds-membersforazrolebl.md)                | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-repl-Cursor**](a-msds-ncreplcursors.md)                            | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-repl-Inbound-Nachbarn**](a-msds-ncreplinboundneighbors.md)         | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-repl-Outbound-Nachbarn**](a-msds-ncreploutboundneighbors.md)       | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)    | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-Typ**](a-msds-nctype.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-nicht-Member**](a-msds-nonmembers.md)                                   | False     | **Gruppieren**                                                                                                                          |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                    | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)          | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)          | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Phonetic-Display-Name**](a-msds-phoneticdisplayname.md)                | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                             | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-PSO-angewendet**](a-msds-psoapplied.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)           | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                   | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-offengelegt-DSAs**](a-msds-revealeddsas.md)                               | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-enthüllt-List-BL**](a-msds-revealedlistbl.md)                          | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Tasks-für-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                    | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Tasks-für-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                    | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-Exch-Assistant-Name**](a-msexchassistantname.md)                          | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-Exch-LabeledURI**](a-msexchlabeleduri.md)                                 | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**msSFU-30: Name**](a-mssfu30name.md)                                           | False     | **Gruppieren**                                                                                                                          |
| [**msSFU-30-NIS-Domäne**](a-mssfu30nisdomain.md)                                | False     | **Gruppieren**                                                                                                                          |
| [**msSFU-30-POSIX-Member**](a-mssfu30posixmember.md)                            | False     | **Gruppieren**                                                                                                                          |
| [**msSFU-30-POSIX-Member-of**](a-mssfu30posixmemberof.md)                       | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**NetBoot-SCP-BL**](a-netbootscpbl.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Nicht sicherheitsmitglied**](a-nonsecuritymember.md)                               | False     | **Gruppieren**                                                                                                                          |
| [**Nicht sicherheitsmitglied-BL**](a-nonsecuritymemberbl.md)                          | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**NT-Gruppenmitglieder**](a-ntgroupmembers.md)                                     | False     | **Gruppieren**                                                                                                                          |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                         | Richtig      | [**Nach oben**](c-top.md)<br/> [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/>                                       |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                     | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Objekt-Kategorie**](a-objectcategory.md)                                      | Richtig      | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Object-Klasse**](a-objectclass.md)                                            | Richtig      | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Objekt-GUID**](a-objectguid.md)                                              | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Objekt-sid**](a-objectsid.md)                                                | Richtig      | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**Objekt-Version**](a-objectversion.md)                                        | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Operator-count**](a-operatorcount.md)                                        | False     | **Gruppieren**                                                                                                                          |
| [**Andere-bekannte Objekte**](a-otherwellknownobjects.md)                      | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Partial-Attribute-löschen-List**](a-partialattributedeletionlist.md)        | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Partiell-Attribut Satz**](a-partialattributeset.md)                           | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Mögliche-minderwertig**](a-possibleinferiors.md)                                | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Primary-Group-Token**](a-primarygrouptoken.md)                               | False     | **Gruppieren**                                                                                                                          |
| [**Proxy-Objekt Name**](a-proxiedobjectname.md)                               | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Proxy Adressen**](a-proxyaddresses.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Abfrage-Richtlinie-BL**](a-querypolicybl.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**RDN**](a-name.md)                                                            | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                        | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**REPL-Update-Vector**](a-repluptodatevector.md)                             | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Berichte**](a-directreports.md)                                               | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Reps-from**](a-repsfrom.md)                                                  | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Reps-to**](a-repsto.md)                                                      | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Novel**](a-revision.md)                                                   | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Gesagt**](a-rid.md)                                                             | False     | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**Sam-Account-Name**](a-samaccountname.md)                                     | Richtig      | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**Sam-Account-Type**](a-samaccounttype.md)                                     | False     | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**SD-Rechte**](a-sdrightseffective.md)                               | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**secretary**](a-secretary.md)                                                 | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**Sicherheits-ID**](a-securityidentifier.md)                              | False     | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**Server-Reference-BL**](a-serverreferencebl.md)                               | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**In-Address-Book anzeigen**](a-showinaddressbook.md)                              | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**Anzeigen-in-Advanced-nur anzeigen**](a-showinadvancedviewonly.md)                   | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**SID-Verlauf**](a-sidhistory.md)                                              | False     | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**Site-Object-BL**](a-siteobjectbl.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Struktur-Objekt-Klasse**](a-structuralobjectclass.md)                       | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Sub-Refs**](a-subrefs.md)                                                    | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Subschemasubentry**](a-subschemasubentry.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Ergänzende Anmelde Informationen**](a-supplementalcredentials.md)                    | False     | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**SystemFlags**](a-systemflags.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Telefonnummer**](a-telephonenumber.md)                                    | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**Text-codiert-or-address**](a-textencodedoraddress.md)                        | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**Tokengruppen**](a-tokengroups.md)                                            | False     | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**Token-Groups-Global-and-Universal**](a-tokengroupsglobalanduniversal.md)     | False     | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**Token-Groups-No-GC-akzeptabel**](a-tokengroupsnogcacceptable.md)             | False     | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**unixUserPassword**](a-unixuserpassword.md)                                   | False     | [**posixgroup**](c-posixgroup.md)<br/>                                                                                      |
| [**Benutzerzertifikat**](a-usercert.md)                                                  | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**Benutzer Kennwort**](a-userpassword.md)                                          | False     | [**posixgroup**](c-posixgroup.md)<br/>                                                                                      |
| [**Benutzersmime-Zertifikat**](a-usersmimecertificate.md)                         | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**Die Anwendung wurde geändert.**](a-usnchanged.md)                                              | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Von der Anwendung erstellte**](a-usncreated.md)                                              | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**USA-DSA-letzte-obj-entfernt**](a-usndsalastobjremoved.md)                       | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Standort-und standortübergreifende standortübergreifende**](a-usnintersite.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**"An-Last-obj-REM"**](a-usnlastobjrem.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Quell Code Quelle**](a-usnsource.md)                                                | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**WBEM-Pfad**](a-wbempath.md)                                                  | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Bekannte Objekte**](a-wellknownobjects.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Bei Änderung**](a-whenchanged.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Bei Erstellung**](a-whencreated.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**WWW-Homepage**](a-wwwhomepage.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**WWW-Page-other**](a-url.md)                                                  | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**X509-CERT**](a-usercertificate.md)                                           | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |



## <a name="windows-server-2008-extended-rights"></a>Erweiterte Rechte für Windows Server 2008

Diese Klasse enthält die folgenden erweiterten Rechte für Windows Server 2008:



| Allgemeiner Name                  |
|------------------------------|
| [**Senden an**](r-send-to.md) |



## <a name="windows-server-2008-validated-writes"></a>Windows Server 2008 validierte Schreibvorgänge

Diese Klasse enthält die folgenden validierten Schreibvorgänge für Windows Server 2008:



| Allgemeiner Name                                  |
|----------------------------------------------|
| [**Selbst Mitgliedschaft**](r-self-membership.md) |



## <a name="windows-server-2008-property-sets"></a>Windows Server 2008-Eigenschaften Sätze

Diese Klasse enthält die folgenden Eigenschaften Sätze für Windows Server 2008:



| Allgemeiner Name                                      |
|--------------------------------------------------|
| [**E-Mail-Informationen**](r-email-information.md) |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2

-   [Attribute](#windows-server-2008-r2-attributes)
-   [Erweiterte Rechte](#windows-server-2008-r2-extended-rights)
-   [Überprüfte Schreibvorgänge](#windows-server-2008-r2-validated-writes)
-   [Eigenschaftensätze](#windows-server-2008-r2-property-sets)



| Eingabe | Wert |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | False                                                                                                                                                                                                                                                                                                            |
| Object-Category             | 1                                                                                                                                                                                                                                                                                                                |
| Default-Object-Category     | \-                                                                                                                                                                                                                                                                                                               |
| Governs-Id                  | 1.2.840.113556.1.5.8                                                                                                                                                                                                                                                                                             |
| Standard-ausblenden-Wert        | 0                                                                                                                                                                                                                                                                                                                |
| RDN-ATT-ID                  | [**Gemeinsamer Name**](a-cn.md)<br/>                                                                                                                                                                                                                                                                           |
| Unterklasse von                 | [**Nach oben**](c-top.md)<br/>                                                                                                                                                                                                                                                                                  |
| Mögliche Vorgesetzten          | [**Domäne-DNS**](c-domaindns.md)[**Organisationseinheit**](c-organizationalunit.md)[**BuiltIn-Domänen**](c-builtindomain.md)[**Container**](c-container.md)[**ms-DS-AZ-Admin-Manager**](c-msds-azadminmanager.md)[**ms-DS-AZ-Application**](c-msds-azapplication.md)[**ms-DS-AZ-Scope**](c-msds-azscope.md) |
| Zusätzlich           | [**posixgroup**](c-posixgroup.md)[**-Sicherheits Prinzipal**](c-securityprincipal.md) (System)[**Mail-Empfänger**](c-mailrecipient.md) (System)                                                                                                                                                                   |
| NT-Security-Descriptor      | o:Bag: schlecht: S:                                                                                                                                                                                                                                                                                                     |
| Standard Sicherheits Beschreibung | D: (A;; rpwpcrccdclclorcwowdsddtsw;;;D a) (a;; Rpwpcrccdclclorcwowdsddtsw;;; SY) (A;; Rplclorc;;; Au) (A;; Rpwpcrccdclclorcwowdsddtsw;;; AO) (A;; Rplclorc;;; PS) (OA;; CR; ab721a55-1e2f-11D0-9819-00aa0040529b;; Au) (OA;; RP; 46a9b11d-60ae-405a-b7e8-ff8a58d456d2;; S-1-5-32-560)                                                   |
| System-Flags                | 0x00000010                                                                                                                                                                                                                                                                                                       |



## <a name="windows-server-2008-r2-attributes"></a>Windows Server 2008 R2-Attribute

Diese Klasse enthält die folgenden Attribute für Windows Server 2008 R2:



| Attribut                                                                        | Obligatorisch. | Abgeleitet von                                                                                                                       |
|----------------------------------------------------------------------------------|-----------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Konto Name-Verlauf**](a-accountnamehistory.md)                             | False     | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**Admin: Anzahl**](a-admincount.md)                                              | False     | **Gruppieren**                                                                                                                          |
| [**Administrator: Beschreibung**](a-admindescription.md)                                  | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Administrator-Anzeige Name**](a-admindisplayname.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Zulässige Attribute**](a-allowedattributes.md)                                | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Zulässige Attribute-gültig**](a-allowedattributeseffective.md)             | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Zulässige, untergeordnete Klassen**](a-allowedchildclasses.md)                           | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Zulässig-untergeordnete Klassen-gültig**](a-allowedchildclasseseffective.md)        | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Alt-Sicherheit-Identitäten**](a-altsecurityidentities.md)                       | False     | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                    | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Kanonischer Name**](a-canonicalname.md)                                        | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Geäußert**](a-info.md)                                                        | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**Gemeinsamer Name**](a-cn.md)                                                      | Richtig      | [**Nach oben**](c-top.md)<br/> [**posixgroup**](c-posixgroup.md)<br/> [**E-Mail-Empfänger**](c-mailrecipient.md)<br/> |
| [**Control-Access-Rights**](a-controlaccessrights.md)                           | False     | **Gruppieren**                                                                                                                          |
| [**Create-Zeitstempel**](a-createtimestamp.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Beschreibung**](a-description.md)                                             | False     | [**Nach oben**](c-top.md)<br/> [**posixgroup**](c-posixgroup.md)<br/>                                                      |
| [**Desktop Profil**](a-desktopprofile.md)                                      | False     | **Gruppieren**                                                                                                                          |
| [**Anzeige Name**](a-displayname.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Anzeige Name-druckdruck**](a-displaynameprintable.md)                         | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**DSA-Signatur**](a-dsasignature.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**DS-Core-propagierungs Daten**](a-dscorepropagationdata.md)                      | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**E-Mail-Adressen**](a-mail.md)                                               | False     | **Gruppieren**                                                                                                                          |
| [**Erweiterungs Name**](a-extensionname.md)                                        | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Fahren**](a-flags.md)                                                         | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Aus-Eintrag**](a-fromentry.md)                                                | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                    | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                        | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**"F"-Rollen Besitzer**](a-fsmoroleowner.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Garbage Koll-Zeitraum**](a-garbagecollperiod.md)                               | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**gidNumber**](a-gidnumber.md)                                                 | False     | [**posixgroup**](c-posixgroup.md)<br/>                                                                                      |
| [**Group-Attribute**](a-groupattributes.md)                                    | False     | **Gruppieren**                                                                                                                          |
| [**Gruppenmitgliedschaft: Sam**](a-groupmembershipsam.md)                             | False     | **Gruppieren**                                                                                                                          |
| [**Gruppentyp**](a-grouptype.md)                                                | Richtig      | **Gruppieren**                                                                                                                          |
| [**Instanztyp**](a-instancetype.md)                                          | Richtig      | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Is-critical-System-Object**](a-iscriticalsystemobject.md)                    | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Ist-gelöscht**](a-isdeleted.md)                                                | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Is-Member-of-DL**](a-memberof.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Is-Privilege-Inhaber**](a-isprivilegeholder.md)                               | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Ist-recycelt**](a-isrecycled.md)                                              | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**LabeledURI**](a-labeleduri.md)                                               | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**Letztes-bekannt/übergeordnetes Element**](a-lastknownparent.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Legacy-Exchange-DN**](a-legacyexchangedn.md)                                 | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**Verwaltet von**](a-managedby.md)                                                | False     | **Gruppieren**                                                                                                                          |
| [**Verwaltete Objekte**](a-managedobjects.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Verwaltet von**](a-masteredby.md)                                              | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Member**](a-member.md)                                                       | False     | **Gruppieren**                                                                                                                          |
| [**memberuid**](a-memberuid.md)                                                 | False     | [**posixgroup**](c-posixgroup.md)<br/>                                                                                      |
| [**Modify-Zeitstempel**](a-modifytimestamp.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**MS-com-partitionsetlink**](a-mscom-partitionsetlink.md)                      | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**MS-com-userlink**](a-mscom-userlink.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**MS-DFSR-computerreferencebl**](a-msdfsr-computerreferencebl.md)              | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**MS-DFSR-mitgliedreferencebl**](a-msdfsr-memberreferencebl.md)                  | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-ca-immed-untergeordnete Elemente**](a-msds-approx-immed-subordinates.md)      | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-authentieredto-accountlist**](a-msds-authenticatedtoaccountlist.md)   | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-AZ-Application-Data**](a-msds-azapplicationdata.md)                    | False     | **Gruppieren**                                                                                                                          |
| [**ms-DS-AZ-BIZ-Rule**](a-msds-azbizrule.md)                                    | False     | **Gruppieren**                                                                                                                          |
| [**ms-DS-AZ-BIZ-Rule-Language**](a-msds-azbizrulelanguage.md)                   | False     | **Gruppieren**                                                                                                                          |
| [**ms-DS-AZ-Generic-Data**](a-msds-azgenericdata.md)                            | False     | **Gruppieren**                                                                                                                          |
| [**ms-DS-AZ-Last-Import-BIZ-Rule-Path**](a-msds-azlastimportedbizrulepath.md) | False     | **Gruppieren**                                                                                                                          |
| [**ms-DS-AZ-LDAP-Query**](a-msds-azldapquery.md)                                | False     | **Gruppieren**                                                                                                                          |
| [**ms-DS-AZ-Object-GUID**](a-msds-azobjectguid.md)                              | False     | **Gruppieren**                                                                                                                          |
| [**MS-DS-Konsistenz-untergeordnet-Anzahl**](a-ms-ds-consistencychildcount.md)           | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                        | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-aktiviert-Feature-BL**](a-msds-enabledfeaturebl.md)                      | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)             | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-is-Domain-for**](a-msds-isdomainfor.md)                                | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-is-full-Replica-for**](a-msds-isfullreplicafor.md)                     | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-is-Partial-Replica-for**](a-msds-ispartialreplicafor.md)               | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-keyversionnumber**](a-msds-keyversionnumber.md)                        | False     | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**ms-DS-krbtgt-Link-BL**](a-msds-krbtgtlinkbl.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-local-Effective-Lösch Zeit**](a-msds-localeffectivedeletiontime.md) | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-local-Effective-Papier-Time**](a-msds-localeffectiverecycletime.md)   | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-gemastert von**](a-msds-masteredby.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Members-für-AZ-Role-BL**](a-msds-membersforazrolebl.md)                | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-repl-Cursor**](a-msds-ncreplcursors.md)                            | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-repl-Inbound-Nachbarn**](a-msds-ncreplinboundneighbors.md)         | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-repl-Outbound-Nachbarn**](a-msds-ncreploutboundneighbors.md)       | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)    | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-Typ**](a-msds-nctype.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-nicht-Member**](a-msds-nonmembers.md)                                   | False     | **Gruppieren**                                                                                                                          |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                    | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-oidtoidgruppe-Link-BL**](a-msds-oidtogrouplinkbl.md)                      | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)          | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)          | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Phonetic-Display-Name**](a-msds-phoneticdisplayname.md)                | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                             | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-PSO-angewendet**](a-msds-psoapplied.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)           | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                   | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-offengelegt-DSAs**](a-msds-revealeddsas.md)                               | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-enthüllt-List-BL**](a-msds-revealedlistbl.md)                          | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Tasks-für-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                    | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Tasks-für-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                    | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-Exch-Assistant-Name**](a-msexchassistantname.md)                          | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-Exch-LabeledURI**](a-msexchlabeleduri.md)                                 | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**msSFU-30: Name**](a-mssfu30name.md)                                           | False     | **Gruppieren**                                                                                                                          |
| [**msSFU-30-NIS-Domäne**](a-mssfu30nisdomain.md)                                | False     | **Gruppieren**                                                                                                                          |
| [**msSFU-30-POSIX-Member**](a-mssfu30posixmember.md)                            | False     | **Gruppieren**                                                                                                                          |
| [**msSFU-30-POSIX-Member-of**](a-mssfu30posixmemberof.md)                       | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**NetBoot-SCP-BL**](a-netbootscpbl.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Nicht sicherheitsmitglied**](a-nonsecuritymember.md)                               | False     | **Gruppieren**                                                                                                                          |
| [**Nicht sicherheitsmitglied-BL**](a-nonsecuritymemberbl.md)                          | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**NT-Gruppenmitglieder**](a-ntgroupmembers.md)                                     | False     | **Gruppieren**                                                                                                                          |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                         | Richtig      | [**Nach oben**](c-top.md)<br/> [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/>                                       |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                     | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Objekt-Kategorie**](a-objectcategory.md)                                      | Richtig      | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Object-Klasse**](a-objectclass.md)                                            | Richtig      | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Objekt-GUID**](a-objectguid.md)                                              | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Objekt-sid**](a-objectsid.md)                                                | Richtig      | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**Objekt-Version**](a-objectversion.md)                                        | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Operator-count**](a-operatorcount.md)                                        | False     | **Gruppieren**                                                                                                                          |
| [**Andere-bekannte Objekte**](a-otherwellknownobjects.md)                      | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Partial-Attribute-löschen-List**](a-partialattributedeletionlist.md)        | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Partiell-Attribut Satz**](a-partialattributeset.md)                           | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Mögliche-minderwertig**](a-possibleinferiors.md)                                | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Primary-Group-Token**](a-primarygrouptoken.md)                               | False     | **Gruppieren**                                                                                                                          |
| [**Proxy-Objekt Name**](a-proxiedobjectname.md)                               | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Proxy Adressen**](a-proxyaddresses.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Abfrage-Richtlinie-BL**](a-querypolicybl.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**RDN**](a-name.md)                                                            | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                        | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**REPL-Update-Vector**](a-repluptodatevector.md)                             | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Berichte**](a-directreports.md)                                               | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Reps-from**](a-repsfrom.md)                                                  | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Reps-to**](a-repsto.md)                                                      | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Novel**](a-revision.md)                                                   | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Gesagt**](a-rid.md)                                                             | False     | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**Sam-Account-Name**](a-samaccountname.md)                                     | Richtig      | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**Sam-Account-Type**](a-samaccounttype.md)                                     | False     | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**SD-Rechte**](a-sdrightseffective.md)                               | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**secretary**](a-secretary.md)                                                 | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**Sicherheits-ID**](a-securityidentifier.md)                              | False     | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**Server-Reference-BL**](a-serverreferencebl.md)                               | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**In-Address-Book anzeigen**](a-showinaddressbook.md)                              | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**Anzeigen-in-Advanced-nur anzeigen**](a-showinadvancedviewonly.md)                   | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**SID-Verlauf**](a-sidhistory.md)                                              | False     | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**Site-Object-BL**](a-siteobjectbl.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Struktur-Objekt-Klasse**](a-structuralobjectclass.md)                       | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Sub-Refs**](a-subrefs.md)                                                    | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Subschemasubentry**](a-subschemasubentry.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Ergänzende Anmelde Informationen**](a-supplementalcredentials.md)                    | False     | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**SystemFlags**](a-systemflags.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Telefonnummer**](a-telephonenumber.md)                                    | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**Text-codiert-or-address**](a-textencodedoraddress.md)                        | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**Tokengruppen**](a-tokengroups.md)                                            | False     | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**Token-Groups-Global-and-Universal**](a-tokengroupsglobalanduniversal.md)     | False     | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**Token-Groups-No-GC-akzeptabel**](a-tokengroupsnogcacceptable.md)             | False     | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**unixUserPassword**](a-unixuserpassword.md)                                   | False     | [**posixgroup**](c-posixgroup.md)<br/>                                                                                      |
| [**Benutzerzertifikat**](a-usercert.md)                                                  | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**Benutzer Kennwort**](a-userpassword.md)                                          | False     | [**posixgroup**](c-posixgroup.md)<br/>                                                                                      |
| [**Benutzersmime-Zertifikat**](a-usersmimecertificate.md)                         | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**Die Anwendung wurde geändert.**](a-usnchanged.md)                                              | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Von der Anwendung erstellte**](a-usncreated.md)                                              | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**USA-DSA-letzte-obj-entfernt**](a-usndsalastobjremoved.md)                       | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Standort-und standortübergreifende standortübergreifende**](a-usnintersite.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**"An-Last-obj-REM"**](a-usnlastobjrem.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Quell Code Quelle**](a-usnsource.md)                                                | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**WBEM-Pfad**](a-wbempath.md)                                                  | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Bekannte Objekte**](a-wellknownobjects.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Bei Änderung**](a-whenchanged.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Bei Erstellung**](a-whencreated.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**WWW-Homepage**](a-wwwhomepage.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**WWW-Page-other**](a-url.md)                                                  | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**X509-CERT**](a-usercertificate.md)                                           | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |



## <a name="windows-server-2008-r2-extended-rights"></a>Erweiterte Rechte für Windows Server 2008 R2

Diese Klasse enthält die folgenden erweiterten Rechte für Windows Server 2008 R2:



| Allgemeiner Name                  |
|------------------------------|
| [**Senden an**](r-send-to.md) |



## <a name="windows-server-2008-r2-validated-writes"></a>Windows Server 2008 R2 validierte Schreibvorgänge

Diese Klasse enthält die folgenden validierten Schreibvorgänge für Windows Server 2008 R2:



| Allgemeiner Name                                  |
|----------------------------------------------|
| [**Selbst Mitgliedschaft**](r-self-membership.md) |



## <a name="windows-server-2008-r2-property-sets"></a>Windows Server 2008 R2-Eigenschaften Sätze

Diese Klasse enthält die folgenden Eigenschaften Sätze für Windows Server 2008 R2:



| Allgemeiner Name                                      |
|--------------------------------------------------|
| [**E-Mail-Informationen**](r-email-information.md) |



## <a name="windows-server-2012"></a>Windows Server 2012

-   [Attribute](#windows-server-2012-attributes)
-   [Erweiterte Rechte](#windows-server-2012-extended-rights)
-   [Überprüfte Schreibvorgänge](#windows-server-2012-validated-writes)
-   [Eigenschaftensätze](#windows-server-2012-property-sets)



| Eingabe | Wert |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | False                                                                                                                                                                                                                                                                                                            |
| Object-Category             | 1                                                                                                                                                                                                                                                                                                                |
| Default-Object-Category     | \-                                                                                                                                                                                                                                                                                                               |
| Governs-Id                  | 1.2.840.113556.1.5.8                                                                                                                                                                                                                                                                                             |
| Standard-ausblenden-Wert        | 0                                                                                                                                                                                                                                                                                                                |
| RDN-ATT-ID                  | [**Gemeinsamer Name**](a-cn.md)<br/>                                                                                                                                                                                                                                                                           |
| Unterklasse von                 | [**Nach oben**](c-top.md)<br/>                                                                                                                                                                                                                                                                                  |
| Mögliche Vorgesetzten          | [**Domäne-DNS**](c-domaindns.md)[**Organisationseinheit**](c-organizationalunit.md)[**BuiltIn-Domänen**](c-builtindomain.md)[**Container**](c-container.md)[**ms-DS-AZ-Admin-Manager**](c-msds-azadminmanager.md)[**ms-DS-AZ-Application**](c-msds-azapplication.md)[**ms-DS-AZ-Scope**](c-msds-azscope.md) |
| Zusätzlich           | [**posixgroup**](c-posixgroup.md)[**-Sicherheits Prinzipal**](c-securityprincipal.md) (System)[**Mail-Empfänger**](c-mailrecipient.md) (System)                                                                                                                                                                   |
| NT-Security-Descriptor      | o:Bag: schlecht: S:                                                                                                                                                                                                                                                                                                     |
| Standard Sicherheits Beschreibung | D: (A;; rpwpcrccdclclorcwowdsddtsw;;;D a) (a;; Rpwpcrccdclclorcwowdsddtsw;;; SY) (A;; Rplclorc;;; Au) (A;; Rpwpcrccdclclorcwowdsddtsw;;; AO) (A;; Rplclorc;;; PS) (OA;; CR; ab721a55-1e2f-11D0-9819-00aa0040529b;; Au) (OA;; RP; 46a9b11d-60ae-405a-b7e8-ff8a58d456d2;; S-1-5-32-560)                                                   |
| System-Flags                | 0x00000010                                                                                                                                                                                                                                                                                                       |



## <a name="windows-server-2012-attributes"></a>Windows Server 2012-Attribute

Diese Klasse enthält die folgenden Attribute für Windows Server 2012:



| Attribut                                                                                    | Obligatorisch. | Abgeleitet von                                                                                                                       |
|----------------------------------------------------------------------------------------------|-----------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Konto Name-Verlauf**](a-accountnamehistory.md)                                         | False     | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**Admin: Anzahl**](a-admincount.md)                                                          | False     | **Gruppieren**                                                                                                                          |
| [**Administrator: Beschreibung**](a-admindescription.md)                                              | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Administrator-Anzeige Name**](a-admindisplayname.md)                                             | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Zulässige Attribute**](a-allowedattributes.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Zulässige Attribute-gültig**](a-allowedattributeseffective.md)                         | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Zulässige, untergeordnete Klassen**](a-allowedchildclasses.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Zulässig-untergeordnete Klassen-gültig**](a-allowedchildclasseseffective.md)                    | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Alt-Sicherheit-Identitäten**](a-altsecurityidentities.md)                                   | False     | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                                | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Kanonischer Name**](a-canonicalname.md)                                                    | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Geäußert**](a-info.md)                                                                    | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**Gemeinsamer Name**](a-cn.md)                                                                  | Richtig      | [**Nach oben**](c-top.md)<br/> [**posixgroup**](c-posixgroup.md)<br/> [**E-Mail-Empfänger**](c-mailrecipient.md)<br/> |
| [**Control-Access-Rights**](a-controlaccessrights.md)                                       | False     | **Gruppieren**                                                                                                                          |
| [**Create-Zeitstempel**](a-createtimestamp.md)                                               | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Beschreibung**](a-description.md)                                                         | False     | [**Nach oben**](c-top.md)<br/> [**posixgroup**](c-posixgroup.md)<br/>                                                      |
| [**Desktop Profil**](a-desktopprofile.md)                                                  | False     | **Gruppieren**                                                                                                                          |
| [**Anzeige Name**](a-displayname.md)                                                        | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Anzeige Name-druckdruck**](a-displaynameprintable.md)                                     | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**DSA-Signatur**](a-dsasignature.md)                                                      | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**DS-Core-propagierungs Daten**](a-dscorepropagationdata.md)                                  | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**E-Mail-Adressen**](a-mail.md)                                                           | False     | **Gruppieren**                                                                                                                          |
| [**Erweiterungs Name**](a-extensionname.md)                                                    | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Fahren**](a-flags.md)                                                                     | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Aus-Eintrag**](a-fromentry.md)                                                            | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                                | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                                    | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**"F"-Rollen Besitzer**](a-fsmoroleowner.md)                                                   | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Garbage Koll-Zeitraum**](a-garbagecollperiod.md)                                           | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**gidNumber**](a-gidnumber.md)                                                             | False     | [**posixgroup**](c-posixgroup.md)<br/>                                                                                      |
| [**Group-Attribute**](a-groupattributes.md)                                                | False     | **Gruppieren**                                                                                                                          |
| [**Gruppenmitgliedschaft: Sam**](a-groupmembershipsam.md)                                         | False     | **Gruppieren**                                                                                                                          |
| [**Gruppentyp**](a-grouptype.md)                                                            | Richtig      | **Gruppieren**                                                                                                                          |
| [**Instanztyp**](a-instancetype.md)                                                      | Richtig      | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Is-critical-System-Object**](a-iscriticalsystemobject.md)                                | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Ist-gelöscht**](a-isdeleted.md)                                                            | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Is-Member-of-DL**](a-memberof.md)                                                        | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Is-Privilege-Inhaber**](a-isprivilegeholder.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Ist-recycelt**](a-isrecycled.md)                                                          | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**LabeledURI**](a-labeleduri.md)                                                           | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**Letztes-bekannt/übergeordnetes Element**](a-lastknownparent.md)                                               | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Legacy-Exchange-DN**](a-legacyexchangedn.md)                                             | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**Verwaltet von**](a-managedby.md)                                                            | False     | **Gruppieren**                                                                                                                          |
| [**Verwaltete Objekte**](a-managedobjects.md)                                                  | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Verwaltet von**](a-masteredby.md)                                                          | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Member**](a-member.md)                                                                   | False     | **Gruppieren**                                                                                                                          |
| [**memberuid**](a-memberuid.md)                                                             | False     | [**posixgroup**](c-posixgroup.md)<br/>                                                                                      |
| [**Modify-Zeitstempel**](a-modifytimestamp.md)                                               | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**MS-com-partitionsetlink**](a-mscom-partitionsetlink.md)                                  | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**MS-com-userlink**](a-mscom-userlink.md)                                                  | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**MS-DFSR-computerreferencebl**](a-msdfsr-computerreferencebl.md)                          | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**MS-DFSR-mitgliedreferencebl**](a-msdfsr-memberreferencebl.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-ca-immed-untergeordnete Elemente**](a-msds-approx-immed-subordinates.md)                  | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-authentieredto-accountlist**](a-msds-authenticatedtoaccountlist.md)               | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-AZ-Application-Data**](a-msds-azapplicationdata.md)                                | False     | **Gruppieren**                                                                                                                          |
| [**ms-DS-AZ-BIZ-Rule**](a-msds-azbizrule.md)                                                | False     | **Gruppieren**                                                                                                                          |
| [**ms-DS-AZ-BIZ-Rule-Language**](a-msds-azbizrulelanguage.md)                               | False     | **Gruppieren**                                                                                                                          |
| [**ms-DS-AZ-Generic-Data**](a-msds-azgenericdata.md)                                        | False     | **Gruppieren**                                                                                                                          |
| [**ms-DS-AZ-Last-Import-BIZ-Rule-Path**](a-msds-azlastimportedbizrulepath.md)             | False     | **Gruppieren**                                                                                                                          |
| [**ms-DS-AZ-LDAP-Query**](a-msds-azldapquery.md)                                            | False     | **Gruppieren**                                                                                                                          |
| [**ms-DS-AZ-Object-GUID**](a-msds-azobjectguid.md)                                          | False     | **Gruppieren**                                                                                                                          |
| [**ms-DS-Claim-Shares-mögliche-values-with-BL**](a-msds-claimsharespossiblevalueswithbl.md) | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Konsistenz-untergeordnet-Anzahl**](a-ms-ds-consistencychildcount.md)                       | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                                    | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-aktiviert-Feature-BL**](a-msds-enabledfeaturebl.md)                                  | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Geokoordinaten-Höhe**](a-msds-geocoordinatesaltitude.md)                       | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-DS-Geokoordinaten-Breitengrad**](a-msds-geocoordinateslatitude.md)                       | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-DS-Geokoordinaten-Längengrad**](a-msds-geocoordinateslongitude.md)                     | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-DS-Host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)                         | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-is-Domain-for**](a-msds-isdomainfor.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-is-full-Replica-for**](a-msds-isfullreplicafor.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-is-Partial-Replica-for**](a-msds-ispartialreplicafor.md)                           | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-is-Primary-Computer-für**](a-msds-isprimarycomputerfor.md)                         | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-keyversionnumber**](a-msds-keyversionnumber.md)                                    | False     | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**ms-DS-krbtgt-Link-BL**](a-msds-krbtgtlinkbl.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-local-Effective-Lösch Zeit**](a-msds-localeffectivedeletiontime.md)             | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-local-Effective-Papier-Time**](a-msds-localeffectiverecycletime.md)               | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-gemastert von**](a-msds-masteredby.md)                                               | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Members-für-AZ-Role-BL**](a-msds-membersforazrolebl.md)                            | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Members-of-Resource-Property-List-BL**](a-msds-membersofresourcepropertylistbl.md) | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-repl-Cursor**](a-msds-ncreplcursors.md)                                        | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-repl-Inbound-Nachbarn**](a-msds-ncreplinboundneighbors.md)                     | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-repl-Outbound-Nachbarn**](a-msds-ncreploutboundneighbors.md)                   | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)                | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-Typ**](a-msds-nctype.md)                                                       | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-nicht-Member**](a-msds-nonmembers.md)                                               | False     | **Gruppieren**                                                                                                                          |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                                | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-oidtoidgruppe-Link-BL**](a-msds-oidtogrouplinkbl.md)                                  | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)                      | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)                      | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Phonetic-Display-Name**](a-msds-phoneticdisplayname.md)                            | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-DS-primär-Computer**](a-msds-primarycomputer.md)                                     | False     | **Gruppieren**                                                                                                                          |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-PSO-angewendet**](a-msds-psoapplied.md)                                               | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)                       | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                               | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-offengelegt-DSAs**](a-msds-revealeddsas.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-enthüllt-List-BL**](a-msds-revealedlistbl.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Tasks-für-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                                | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Tasks-für-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                                | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-TDO-Egress-BL**](a-msds-tdoegressbl.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-TDO-Ingress-BL**](a-msds-tdoingressbl.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Value-Type-Reference-BL**](a-msds-valuetypereferencebl.md)                         | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-Exch-Assistant-Name**](a-msexchassistantname.md)                                      | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-Exch-LabeledURI**](a-msexchlabeleduri.md)                                             | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                                        | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**msSFU-30: Name**](a-mssfu30name.md)                                                       | False     | **Gruppieren**                                                                                                                          |
| [**msSFU-30-NIS-Domäne**](a-mssfu30nisdomain.md)                                            | False     | **Gruppieren**                                                                                                                          |
| [**msSFU-30-POSIX-Member**](a-mssfu30posixmember.md)                                        | False     | **Gruppieren**                                                                                                                          |
| [**msSFU-30-POSIX-Member-of**](a-mssfu30posixmemberof.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**NetBoot-SCP-BL**](a-netbootscpbl.md)                                                     | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Nicht sicherheitsmitglied**](a-nonsecuritymember.md)                                           | False     | **Gruppieren**                                                                                                                          |
| [**Nicht sicherheitsmitglied-BL**](a-nonsecuritymemberbl.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**NT-Gruppenmitglieder**](a-ntgroupmembers.md)                                                 | False     | **Gruppieren**                                                                                                                          |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                                     | Richtig      | [**Nach oben**](c-top.md)<br/> [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/>                                       |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                                 | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Objekt-Kategorie**](a-objectcategory.md)                                                  | Richtig      | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Object-Klasse**](a-objectclass.md)                                                        | Richtig      | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Objekt-GUID**](a-objectguid.md)                                                          | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Objekt-sid**](a-objectsid.md)                                                            | Richtig      | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**Objekt-Version**](a-objectversion.md)                                                    | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Operator-count**](a-operatorcount.md)                                                    | False     | **Gruppieren**                                                                                                                          |
| [**Andere-bekannte Objekte**](a-otherwellknownobjects.md)                                  | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Partial-Attribute-löschen-List**](a-partialattributedeletionlist.md)                    | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Partiell-Attribut Satz**](a-partialattributeset.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Mögliche-minderwertig**](a-possibleinferiors.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Primary-Group-Token**](a-primarygrouptoken.md)                                           | False     | **Gruppieren**                                                                                                                          |
| [**Proxy-Objekt Name**](a-proxiedobjectname.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Proxy Adressen**](a-proxyaddresses.md)                                                  | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Abfrage-Richtlinie-BL**](a-querypolicybl.md)                                                   | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**RDN**](a-name.md)                                                                        | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                                    | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**REPL-Update-Vector**](a-repluptodatevector.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Berichte**](a-directreports.md)                                                           | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Reps-from**](a-repsfrom.md)                                                              | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Reps-to**](a-repsto.md)                                                                  | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Novel**](a-revision.md)                                                               | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Gesagt**](a-rid.md)                                                                         | False     | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**Sam-Account-Name**](a-samaccountname.md)                                                 | Richtig      | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**Sam-Account-Type**](a-samaccounttype.md)                                                 | False     | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**SD-Rechte**](a-sdrightseffective.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**secretary**](a-secretary.md)                                                             | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**Sicherheits-ID**](a-securityidentifier.md)                                          | False     | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**Server-Reference-BL**](a-serverreferencebl.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**In-Address-Book anzeigen**](a-showinaddressbook.md)                                          | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**Anzeigen-in-Advanced-nur anzeigen**](a-showinadvancedviewonly.md)                               | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**SID-Verlauf**](a-sidhistory.md)                                                          | False     | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**Site-Object-BL**](a-siteobjectbl.md)                                                     | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Struktur-Objekt-Klasse**](a-structuralobjectclass.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Sub-Refs**](a-subrefs.md)                                                                | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Subschemasubentry**](a-subschemasubentry.md)                                             | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Ergänzende Anmelde Informationen**](a-supplementalcredentials.md)                                | False     | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**SystemFlags**](a-systemflags.md)                                                        | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Telefonnummer**](a-telephonenumber.md)                                                | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**Text-codiert-or-address**](a-textencodedoraddress.md)                                    | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**Tokengruppen**](a-tokengroups.md)                                                        | False     | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**Token-Groups-Global-and-Universal**](a-tokengroupsglobalanduniversal.md)                 | False     | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**Token-Groups-No-GC-akzeptabel**](a-tokengroupsnogcacceptable.md)                         | False     | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**unixUserPassword**](a-unixuserpassword.md)                                               | False     | [**posixgroup**](c-posixgroup.md)<br/>                                                                                      |
| [**Benutzerzertifikat**](a-usercert.md)                                                              | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**Benutzer Kennwort**](a-userpassword.md)                                                      | False     | [**posixgroup**](c-posixgroup.md)<br/>                                                                                      |
| [**Benutzersmime-Zertifikat**](a-usersmimecertificate.md)                                     | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**Die Anwendung wurde geändert.**](a-usnchanged.md)                                                          | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Von der Anwendung erstellte**](a-usncreated.md)                                                          | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**USA-DSA-letzte-obj-entfernt**](a-usndsalastobjremoved.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Standort-und standortübergreifende standortübergreifende**](a-usnintersite.md)                                                      | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**"An-Last-obj-REM"**](a-usnlastobjrem.md)                                                  | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Quell Code Quelle**](a-usnsource.md)                                                            | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**WBEM-Pfad**](a-wbempath.md)                                                              | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Bekannte Objekte**](a-wellknownobjects.md)                                             | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Bei Änderung**](a-whenchanged.md)                                                        | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Bei Erstellung**](a-whencreated.md)                                                        | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**WWW-Homepage**](a-wwwhomepage.md)                                                       | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**WWW-Page-other**](a-url.md)                                                              | False     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**X509-CERT**](a-usercertificate.md)                                                       | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |



## <a name="windows-server-2012-extended-rights"></a>Erweiterte Rechte für Windows Server 2012

Diese Klasse enthält die folgenden erweiterten Rechte für Windows Server 2012:



| Allgemeiner Name                  |
|------------------------------|
| [**Senden an**](r-send-to.md) |



## <a name="windows-server-2012-validated-writes"></a>Windows Server 2012 validierte Schreibvorgänge

Diese Klasse enthält die folgenden validierten Schreibvorgänge für Windows Server 2012:



| Allgemeiner Name                                  |
|----------------------------------------------|
| [**Selbst Mitgliedschaft**](r-self-membership.md) |



## <a name="windows-server-2012-property-sets"></a>Windows Server 2012-Eigenschaften Sätze

Diese Klasse enthält die folgenden Eigenschaften Sätze für Windows Server 2012:



| Allgemeiner Name                                      |
|--------------------------------------------------|
| [**E-Mail-Informationen**](r-email-information.md) |



 

 





