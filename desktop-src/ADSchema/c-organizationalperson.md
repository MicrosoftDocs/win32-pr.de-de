---
title: Organizational-Person-Klasse
description: Diese Klasse wird für Objekte verwendet, die Organisations Informationen zu einem Benutzer enthalten, wie z. b. Mitarbeiternummer, Abteilung, Manager, Titel, Büroadresse usw.
ms.assetid: dbcecb0d-e7ab-4005-82ad-5ffe9b06a380
ms.tgt_platform: multiple
keywords:
- AD-Schema der Organizational-Person-Klasse
- OrganizationalPerson-Klasse AD-Schema
topic_type:
- apiref
api_name:
- Organizational-Person
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0f12e1a82f2386f213246c99b9f63570f14d00a
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104106772"
---
# <a name="organizational-person-class"></a>Organizational-Person-Klasse

Diese Klasse wird für Objekte verwendet, die Organisations Informationen zu einem Benutzer enthalten, wie z. b. Mitarbeiternummer, Abteilung, Manager, Titel, Büroadresse usw.



| Eingabe | Wert |
|-------------------|--------------------------------------|
| CN                | Unternehmensperson                |
| LDAP-Display-Name | OrganizationalPerson                 |
| Berechtigung aktualisieren  | Jeder kann dieses Objekt aktualisieren.       |
| Aktualisierungshäufigkeit  | \-                                   |
| Schema-ID-GUID    | bf967aa4-0de6-11d0-a285-00aa003049e2 |



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
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | False                                                                                        |
| Object-Category             | 2                                                                                            |
| Default-Object-Category     | [**Person**](c-person.md)<br/>                                                        |
| Governs-Id                  | 2.5.6.7                                                                                      |
| Standard-ausblenden-Wert        | 0                                                                                            |
| RDN-ATT-ID                  | [**Gemeinsamer Name**](a-cn.md)<br/>                                                       |
| Unterklasse von                 | [**Person**](c-person.md)<br/>                                                        |
| Mögliche Vorgesetzten          | [**Container**](c-container.md)                                                             |
| Zusätzlich           | \-                                                                                           |
| NT-Security-Descriptor      | o:Bag: schlecht: S:                                                                                 |
| Standard Sicherheits Beschreibung | D: (A;; rpwpcrccdclclorcwowdsddtsw;;;D a) (a;; Rpwpcrccdclclorcwowdsddtsw;;; SY) (A;; Rplclorc;;; Thaus |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-2000-server-attributes"></a>Windows 2000-Server Attribute

Diese Klasse enthält die folgenden Attribute für Windows 2000 Server:



| Attribut                                                                 | Obligatorisch. | Abgeleitet von                                                          |
|---------------------------------------------------------------------------|-----------|-----------------------------------------------------------------------|
| [**Adresse**](a-streetaddress.md)                                        | False     | **Unternehmensperson**                                             |
| [**Adresse-Startseite**](a-homepostaladdress.md)                               | False     | **Unternehmensperson**                                             |
| [**Administrator: Beschreibung**](a-admindescription.md)                           | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Administrator-Anzeige Name**](a-admindisplayname.md)                          | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Zulässige Attribute**](a-allowedattributes.md)                         | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Zulässige Attribute-gültig**](a-allowedattributeseffective.md)      | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Zulässige, untergeordnete Klassen**](a-allowedchildclasses.md)                    | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Zulässig-untergeordnete Klassen-gültig**](a-allowedchildclasseseffective.md) | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Geordneter**](a-assistant.md)                                          | False     | **Unternehmensperson**                                             |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)             | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Kanonischer Name**](a-canonicalname.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Gemeinsamer Name**](a-cn.md)                                               | Richtig      | [**Person**](c-person.md)<br/> [**Nach oben**](c-top.md)<br/> |
| [**Company**](a-company.md)                                              | False     | **Unternehmensperson**                                             |
| [**Länder Code**](a-countrycode.md)                                     | False     | **Unternehmensperson**                                             |
| [**Länder Name**](a-c.md)                                               | False     | **Unternehmensperson**                                             |
| [**Create-Zeitstempel**](a-createtimestamp.md)                            | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Klinik**](a-department.md)                                        | False     | **Unternehmensperson**                                             |
| [**Beschreibung**](a-description.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Ziel-Indikator**](a-destinationindicator.md)                   | False     | **Unternehmensperson**                                             |
| [**Anzeige Name**](a-displayname.md)                                     | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Anzeige Name-druckdruck**](a-displaynameprintable.md)                  | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Division**](a-division.md)                                            | False     | **Unternehmensperson**                                             |
| [**DSA-Signatur**](a-dsasignature.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**DS-Core-propagierungs Daten**](a-dscorepropagationdata.md)               | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**E-Mail-Adressen**](a-mail.md)                                        | False     | **Unternehmensperson**                                             |
| [**Mitarbeiter-ID**](a-employeeid.md)                                       | False     | **Unternehmensperson**                                             |
| [**Erweiterungs Name**](a-extensionname.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Fax-Telefonnummer**](a-facsimiletelephonenumber.md)          | False     | **Unternehmensperson**                                             |
| [**Fahren**](a-flags.md)                                                  | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Aus-Eintrag**](a-fromentry.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)             | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                 | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**"F"-Rollen Besitzer**](a-fsmoroleowner.md)                                | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Generierung-Qualifizierer**](a-generationqualifier.md)                     | False     | **Unternehmensperson**                                             |
| [**Vorname**](a-givenname.md)                                         | False     | **Unternehmensperson**                                             |
| [**Initialen**](a-initials.md)                                            | False     | **Unternehmensperson**                                             |
| [**Instanztyp**](a-instancetype.md)                                   | Richtig      | [**Nach oben**](c-top.md)<br/>                                       |
| [**International-ISDN-Number**](a-internationalisdnnumber.md)            | False     | **Unternehmensperson**                                             |
| [**Is-critical-System-Object**](a-iscriticalsystemobject.md)             | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Ist-gelöscht**](a-isdeleted.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Is-Member-of-DL**](a-memberof.md)                                     | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Is-Privilege-Inhaber**](a-isprivilegeholder.md)                        | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Letztes-bekannt/übergeordnetes Element**](a-lastknownparent.md)                            | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Lokalitäts Name**](a-l.md)                                              | False     | **Unternehmensperson**                                             |
| [**Logo**](a-thumbnaillogo.md)                                           | False     | **Unternehmensperson**                                             |
| [**Verwaltete Objekte**](a-managedobjects.md)                               | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Dienst**](a-manager.md)                                              | False     | **Unternehmensperson**                                             |
| [**Verwaltet von**](a-masteredby.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**MHS-or-address**](a-mhsoraddress.md)                                  | False     | **Unternehmensperson**                                             |
| [**Modify-Zeitstempel**](a-modifytimestamp.md)                            | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**MS-DS-Konsistenz-untergeordnet-Anzahl**](a-ms-ds-consistencychildcount.md)    | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                 | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**NetBoot-SCP-BL**](a-netbootscpbl.md)                                  | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Nicht sicherheitsmitglied-BL**](a-nonsecuritymemberbl.md)                   | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                  | Richtig      | [**Nach oben**](c-top.md)<br/>                                       |
| [**Obj-Dist-Name**](a-distinguishedname.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Objekt-Kategorie**](a-objectcategory.md)                               | Richtig      | [**Nach oben**](c-top.md)<br/>                                       |
| [**Object-Klasse**](a-objectclass.md)                                     | Richtig      | [**Nach oben**](c-top.md)<br/>                                       |
| [**Objekt-GUID**](a-objectguid.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Objekt-Version**](a-objectversion.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Organisations Einheits Name**](a-ou.md)                                  | False     | **Unternehmensperson**                                             |
| [**Name der Organisation**](a-o.md)                                          | False     | **Unternehmensperson**                                             |
| [**Sonstiges-Postfach**](a-othermailbox.md)                                   | False     | **Unternehmensperson**                                             |
| [**Anderer Name**](a-middlename.md)                                        | False     | **Unternehmensperson**                                             |
| [**Andere-bekannte Objekte**](a-otherwellknownobjects.md)               | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Partial-Attribute-löschen-List**](a-partialattributedeletionlist.md) | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Partiell-Attribut Satz**](a-partialattributeset.md)                    | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Persönliche Titel**](a-personaltitle.md)                                 | False     | **Unternehmensperson**                                             |
| [**Telefon-Fax-Sonstiges**](a-otherfacsimiletelephonenumber.md)                | False     | **Unternehmensperson**                                             |
| [**Telefon-privat (Sonstiges)**](a-otherhomephone.md)                              | False     | **Unternehmensperson**                                             |
| [**Telefon-Home-primär**](a-homephone.md)                                 | False     | **Unternehmensperson**                                             |
| [**Telefon-IP-Sonstiges**](a-otheripphone.md)                                  | False     | **Unternehmensperson**                                             |
| [**Telefon-IP-primär**](a-ipphone.md)                                     | False     | **Unternehmensperson**                                             |
| [**Phone-ISDN-Primary**](a-primaryinternationalisdnnumber.md)            | False     | **Unternehmensperson**                                             |
| [**Phone-Mobile-other**](a-othermobile.md)                               | False     | **Unternehmensperson**                                             |
| [**Phone-Mobile-Primary**](a-mobile.md)                                  | False     | **Unternehmensperson**                                             |
| [**Telefon-Office-Sonstiges**](a-othertelephone.md)                            | False     | **Unternehmensperson**                                             |
| [**Telefon-Pager-Sonstiges**](a-otherpager.md)                                 | False     | **Unternehmensperson**                                             |
| [**Telefon-Pager-primär**](a-pager.md)                                    | False     | **Unternehmensperson**                                             |
| [**Physical-delivery-Office-Name**](a-physicaldeliveryofficename.md)     | False     | **Unternehmensperson**                                             |
| [**Picture**](a-thumbnailphoto.md)                                       | False     | **Unternehmensperson**                                             |
| [**Mögliche-minderwertig**](a-possibleinferiors.md)                         | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Postanschrift**](a-postaladdress.md)                                 | False     | **Unternehmensperson**                                             |
| [**Postleitzahl**](a-postalcode.md)                                       | False     | **Unternehmensperson**                                             |
| [**Post-Office-Box**](a-postofficebox.md)                                | False     | **Unternehmensperson**                                             |
| [**Bevorzugte Übermittlungs Methode**](a-preferreddeliverymethod.md)            | False     | **Unternehmensperson**                                             |
| [**Proxy-Objekt Name**](a-proxiedobjectname.md)                        | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Proxy Adressen**](a-proxyaddresses.md)                               | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Abfrage-Richtlinie-BL**](a-querypolicybl.md)                                | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**RDN**](a-name.md)                                                     | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Registrierte Adresse**](a-registeredaddress.md)                         | False     | **Unternehmensperson**                                             |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                 | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**REPL-Update-Vector**](a-repluptodatevector.md)                      | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Berichte**](a-directreports.md)                                        | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Reps-from**](a-repsfrom.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Reps-to**](a-repsto.md)                                               | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Novel**](a-revision.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**SD-Rechte**](a-sdrightseffective.md)                        | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Siehe auch**](a-seealso.md)                                             | False     | [**Person**](c-person.md)<br/>                                 |
| [**Server-Reference-BL**](a-serverreferencebl.md)                        | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Anzeigen-in-Advanced-nur anzeigen**](a-showinadvancedviewonly.md)            | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Site-Object-BL**](a-siteobjectbl.md)                                  | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**State-or-Province-Name**](a-st.md)                                    | False     | **Unternehmensperson**                                             |
| [**Straße**](a-street.md)                                        | False     | **Unternehmensperson**                                             |
| [**Sub-Refs**](a-subrefs.md)                                             | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Subschemasubentry**](a-subschemasubentry.md)                          | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Nachname**](a-sn.md)                                                   | False     | [**Person**](c-person.md)<br/>                                 |
| [**SystemFlags**](a-systemflags.md)                                     | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Telefonnummer**](a-telephonenumber.md)                             | False     | [**Person**](c-person.md)<br/>                                 |
| [**Teletex-Terminal-Identifier**](a-teletexterminalidentifier.md)        | False     | **Unternehmensperson**                                             |
| [**Telex-Nummer**](a-telexnumber.md)                                     | False     | **Unternehmensperson**                                             |
| [**Telex-primär**](a-primarytelexnumber.md)                             | False     | **Unternehmensperson**                                             |
| [**Text-Country**](a-co.md)                                              | False     | **Unternehmensperson**                                             |
| [**Titel**](a-title.md)                                                  | False     | **Unternehmensperson**                                             |
| [**Benutzer Kommentar**](a-comment.md)                                         | False     | **Unternehmensperson**                                             |
| [**Benutzer Kennwort**](a-userpassword.md)                                   | False     | [**Person**](c-person.md)<br/>                                 |
| [**Die Anwendung wurde geändert.**](a-usnchanged.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Von der Anwendung erstellte**](a-usncreated.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**USA-DSA-letzte-obj-entfernt**](a-usndsalastobjremoved.md)                | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Standort-und standortübergreifende standortübergreifende**](a-usnintersite.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**"An-Last-obj-REM"**](a-usnlastobjrem.md)                               | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Quell Code Quelle**](a-usnsource.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**WBEM-Pfad**](a-wbempath.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Bekannte Objekte**](a-wellknownobjects.md)                          | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Bei Änderung**](a-whenchanged.md)                                     | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Bei Erstellung**](a-whencreated.md)                                     | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**WWW-Homepage**](a-wwwhomepage.md)                                    | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**WWW-Page-other**](a-url.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**X121-Adresse**](a-x121address.md)                                     | False     | **Unternehmensperson**                                             |



## <a name="windows-server-2003"></a>Windows Server 2003

-   [Attribute](#windows-server-2003-attributes)



| Eingabe | Wert |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | False                                                                                                                     |
| Object-Category             | 0                                                                                                                         |
| Default-Object-Category     | [**Person**](c-person.md)<br/>                                                                                     |
| Governs-Id                  | 2.5.6.7                                                                                                                   |
| Standard-ausblenden-Wert        | 1                                                                                                                         |
| RDN-ATT-ID                  | [**Gemeinsamer Name**](a-cn.md)<br/>                                                                                    |
| Unterklasse von                 | [**Person**](c-person.md)<br/>                                                                                     |
| Mögliche Vorgesetzten          | [**Organisationseinheit**](c-organizationalunit.md) für [**Container**](c-container.md)[**Organisation**](c-organization.md) |
| Zusätzlich           | \-                                                                                                                        |
| NT-Security-Descriptor      | o:Bag: schlecht: S:                                                                                                              |
| Standard Sicherheits Beschreibung | D: (A;; rpwpcrccdclclorcwowdsddtsw;;;D a) (a;; Rpwpcrccdclclorcwowdsddtsw;;; SY) (A;; Rplclorc;;; Thaus                              |
| System-Flags                | 0x00000010                                                                                                                |



## <a name="windows-server-2003-attributes"></a>Windows Server 2003-Attribute

Diese Klasse enthält die folgenden Attribute für Windows Server 2003:



| Attribut                                                                   | Obligatorisch. | Abgeleitet von                                                          |
|-----------------------------------------------------------------------------|-----------|-----------------------------------------------------------------------|
| [**Adresse**](a-streetaddress.md)                                          | False     | **Unternehmensperson**                                             |
| [**Adresse-Startseite**](a-homepostaladdress.md)                                 | False     | **Unternehmensperson**                                             |
| [**Administrator: Beschreibung**](a-admindescription.md)                             | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Administrator-Anzeige Name**](a-admindisplayname.md)                            | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Zulässige Attribute**](a-allowedattributes.md)                           | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Zulässige Attribute-gültig**](a-allowedattributeseffective.md)        | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Zulässige, untergeordnete Klassen**](a-allowedchildclasses.md)                      | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Zulässig-untergeordnete Klassen-gültig**](a-allowedchildclasseseffective.md)   | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Geordneter**](a-assistant.md)                                            | False     | **Unternehmensperson**                                             |
| [**attributecertificateattribute**](a-attributecertificateattribute.md)    | False     | [**Person**](c-person.md)<br/>                                 |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)               | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Kanonischer Name**](a-canonicalname.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Gemeinsamer Name**](a-cn.md)                                                 | Richtig      | [**Person**](c-person.md)<br/> [**Nach oben**](c-top.md)<br/> |
| [**Company**](a-company.md)                                                | False     | **Unternehmensperson**                                             |
| [**Länder Code**](a-countrycode.md)                                       | False     | **Unternehmensperson**                                             |
| [**Länder Name**](a-c.md)                                                 | False     | **Unternehmensperson**                                             |
| [**Create-Zeitstempel**](a-createtimestamp.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Klinik**](a-department.md)                                          | False     | **Unternehmensperson**                                             |
| [**Beschreibung**](a-description.md)                                        | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Ziel-Indikator**](a-destinationindicator.md)                     | False     | **Unternehmensperson**                                             |
| [**Anzeige Name**](a-displayname.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Anzeige Name-druckdruck**](a-displaynameprintable.md)                    | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Division**](a-division.md)                                              | False     | **Unternehmensperson**                                             |
| [**DSA-Signatur**](a-dsasignature.md)                                     | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**DS-Core-propagierungs Daten**](a-dscorepropagationdata.md)                 | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**E-Mail-Adressen**](a-mail.md)                                          | False     | **Unternehmensperson**                                             |
| [**Mitarbeiter-ID**](a-employeeid.md)                                         | False     | **Unternehmensperson**                                             |
| [**Erweiterungs Name**](a-extensionname.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Fax-Telefonnummer**](a-facsimiletelephonenumber.md)            | False     | **Unternehmensperson**                                             |
| [**Fahren**](a-flags.md)                                                    | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Aus-Eintrag**](a-fromentry.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)               | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                   | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**"F"-Rollen Besitzer**](a-fsmoroleowner.md)                                  | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Generierung-Qualifizierer**](a-generationqualifier.md)                       | False     | **Unternehmensperson**                                             |
| [**Vorname**](a-givenname.md)                                           | False     | **Unternehmensperson**                                             |
| [**HouseIdentifier**](a-houseidentifier.md)                                | False     | **Unternehmensperson**                                             |
| [**Initialen**](a-initials.md)                                              | False     | **Unternehmensperson**                                             |
| [**Instanztyp**](a-instancetype.md)                                     | Richtig      | [**Nach oben**](c-top.md)<br/>                                       |
| [**International-ISDN-Number**](a-internationalisdnnumber.md)              | False     | **Unternehmensperson**                                             |
| [**Is-critical-System-Object**](a-iscriticalsystemobject.md)               | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Ist-gelöscht**](a-isdeleted.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Is-Member-of-DL**](a-memberof.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Is-Privilege-Inhaber**](a-isprivilegeholder.md)                          | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Letztes-bekannt/übergeordnetes Element**](a-lastknownparent.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Lokalitäts Name**](a-l.md)                                                | False     | **Unternehmensperson**                                             |
| [**Logo**](a-thumbnaillogo.md)                                             | False     | **Unternehmensperson**                                             |
| [**Verwaltete Objekte**](a-managedobjects.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Dienst**](a-manager.md)                                                | False     | **Unternehmensperson**                                             |
| [**Verwaltet von**](a-masteredby.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**MHS-or-address**](a-mhsoraddress.md)                                    | False     | **Unternehmensperson**                                             |
| [**Modify-Zeitstempel**](a-modifytimestamp.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**MS-com-partitionsetlink**](a-mscom-partitionsetlink.md)                 | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**MS-com-userlink**](a-mscom-userlink.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-allowed-to-Delegat-an**](a-msds-allowedtodelegateto.md)          | False     | **Unternehmensperson**                                             |
| [**ms-DS-ca-immed-untergeordnete Elemente**](a-msds-approx-immed-subordinates.md) | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**MS-DS-Konsistenz-untergeordnet-Anzahl**](a-ms-ds-consistencychildcount.md)      | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-gemastert von**](a-msds-masteredby.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Members-für-AZ-Role-BL**](a-msds-membersforazrolebl.md)           | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-NC-repl-Cursor**](a-msds-ncreplcursors.md)                       | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-NC-repl-Inbound-Nachbarn**](a-msds-ncreplinboundneighbors.md)    | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-NC-repl-Outbound-Nachbarn**](a-msds-ncreploutboundneighbors.md)  | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                         | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)               | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)     | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)     | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)      | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)              | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Tasks-für-AZ-Role-BL**](a-msds-tasksforazrolebl.md)               | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Tasks-für-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)               | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-Exch-House-Identifier**](a-msexchhouseidentifier.md)                 | False     | **Unternehmensperson**                                             |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**NetBoot-SCP-BL**](a-netbootscpbl.md)                                    | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Nicht sicherheitsmitglied-BL**](a-nonsecuritymemberbl.md)                     | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                    | Richtig      | [**Nach oben**](c-top.md)<br/>                                       |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Objekt-Kategorie**](a-objectcategory.md)                                 | Richtig      | [**Nach oben**](c-top.md)<br/>                                       |
| [**Object-Klasse**](a-objectclass.md)                                       | Richtig      | [**Nach oben**](c-top.md)<br/>                                       |
| [**Objekt-GUID**](a-objectguid.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Objekt-Version**](a-objectversion.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Organisations Einheits Name**](a-ou.md)                                    | False     | **Unternehmensperson**                                             |
| [**Name der Organisation**](a-o.md)                                            | False     | **Unternehmensperson**                                             |
| [**Sonstiges-Postfach**](a-othermailbox.md)                                     | False     | **Unternehmensperson**                                             |
| [**Anderer Name**](a-middlename.md)                                          | False     | **Unternehmensperson**                                             |
| [**Andere-bekannte Objekte**](a-otherwellknownobjects.md)                 | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Partial-Attribute-löschen-List**](a-partialattributedeletionlist.md)   | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Partiell-Attribut Satz**](a-partialattributeset.md)                      | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Persönliche Titel**](a-personaltitle.md)                                   | False     | **Unternehmensperson**                                             |
| [**Telefon-Fax-Sonstiges**](a-otherfacsimiletelephonenumber.md)                  | False     | **Unternehmensperson**                                             |
| [**Telefon-privat (Sonstiges)**](a-otherhomephone.md)                                | False     | **Unternehmensperson**                                             |
| [**Telefon-Home-primär**](a-homephone.md)                                   | False     | **Unternehmensperson**                                             |
| [**Telefon-IP-Sonstiges**](a-otheripphone.md)                                    | False     | **Unternehmensperson**                                             |
| [**Telefon-IP-primär**](a-ipphone.md)                                       | False     | **Unternehmensperson**                                             |
| [**Phone-ISDN-Primary**](a-primaryinternationalisdnnumber.md)              | False     | **Unternehmensperson**                                             |
| [**Phone-Mobile-other**](a-othermobile.md)                                 | False     | **Unternehmensperson**                                             |
| [**Phone-Mobile-Primary**](a-mobile.md)                                    | False     | **Unternehmensperson**                                             |
| [**Telefon-Office-Sonstiges**](a-othertelephone.md)                              | False     | **Unternehmensperson**                                             |
| [**Telefon-Pager-Sonstiges**](a-otherpager.md)                                   | False     | **Unternehmensperson**                                             |
| [**Telefon-Pager-primär**](a-pager.md)                                      | False     | **Unternehmensperson**                                             |
| [**Physical-delivery-Office-Name**](a-physicaldeliveryofficename.md)       | False     | **Unternehmensperson**                                             |
| [**Picture**](a-thumbnailphoto.md)                                         | False     | **Unternehmensperson**                                             |
| [**Mögliche-minderwertig**](a-possibleinferiors.md)                           | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Postanschrift**](a-postaladdress.md)                                   | False     | **Unternehmensperson**                                             |
| [**Postleitzahl**](a-postalcode.md)                                         | False     | **Unternehmensperson**                                             |
| [**Post-Office-Box**](a-postofficebox.md)                                  | False     | **Unternehmensperson**                                             |
| [**Bevorzugte Übermittlungs Methode**](a-preferreddeliverymethod.md)              | False     | **Unternehmensperson**                                             |
| [**Proxy-Objekt Name**](a-proxiedobjectname.md)                          | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Proxy Adressen**](a-proxyaddresses.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Abfrage-Richtlinie-BL**](a-querypolicybl.md)                                  | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**RDN**](a-name.md)                                                       | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Registrierte Adresse**](a-registeredaddress.md)                           | False     | **Unternehmensperson**                                             |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                   | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**REPL-Update-Vector**](a-repluptodatevector.md)                        | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Berichte**](a-directreports.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Reps-from**](a-repsfrom.md)                                             | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Reps-to**](a-repsto.md)                                                 | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Novel**](a-revision.md)                                              | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**SD-Rechte**](a-sdrightseffective.md)                          | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Siehe auch**](a-seealso.md)                                               | False     | [**Person**](c-person.md)<br/>                                 |
| [**Seriennummer**](a-serialnumber.md)                                     | False     | [**Person**](c-person.md)<br/>                                 |
| [**Server-Reference-BL**](a-serverreferencebl.md)                          | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Anzeigen-in-Advanced-nur anzeigen**](a-showinadvancedviewonly.md)              | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**State-or-Province-Name**](a-st.md)                                      | False     | **Unternehmensperson**                                             |
| [**Straße**](a-street.md)                                          | False     | **Unternehmensperson**                                             |
| [**Struktur-Objekt-Klasse**](a-structuralobjectclass.md)                  | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Sub-Refs**](a-subrefs.md)                                               | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Subschemasubentry**](a-subschemasubentry.md)                            | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Nachname**](a-sn.md)                                                     | False     | [**Person**](c-person.md)<br/>                                 |
| [**SystemFlags**](a-systemflags.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Telefonnummer**](a-telephonenumber.md)                               | False     | [**Person**](c-person.md)<br/>                                 |
| [**Teletex-Terminal-Identifier**](a-teletexterminalidentifier.md)          | False     | **Unternehmensperson**                                             |
| [**Telex-Nummer**](a-telexnumber.md)                                       | False     | **Unternehmensperson**                                             |
| [**Telex-primär**](a-primarytelexnumber.md)                               | False     | **Unternehmensperson**                                             |
| [**Text-Country**](a-co.md)                                                | False     | **Unternehmensperson**                                             |
| [**Titel**](a-title.md)                                                    | False     | **Unternehmensperson**                                             |
| [**Benutzer Kommentar**](a-comment.md)                                           | False     | **Unternehmensperson**                                             |
| [**Benutzer Kennwort**](a-userpassword.md)                                     | False     | [**Person**](c-person.md)<br/>                                 |
| [**Die Anwendung wurde geändert.**](a-usnchanged.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Von der Anwendung erstellte**](a-usncreated.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**USA-DSA-letzte-obj-entfernt**](a-usndsalastobjremoved.md)                  | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Standort-und standortübergreifende standortübergreifende**](a-usnintersite.md)                                     | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**"An-Last-obj-REM"**](a-usnlastobjrem.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Quell Code Quelle**](a-usnsource.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**WBEM-Pfad**](a-wbempath.md)                                             | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Bekannte Objekte**](a-wellknownobjects.md)                            | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Bei Änderung**](a-whenchanged.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Bei Erstellung**](a-whencreated.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**WWW-Homepage**](a-wwwhomepage.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**WWW-Page-other**](a-url.md)                                             | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**X121-Adresse**](a-x121address.md)                                       | False     | **Unternehmensperson**                                             |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2

-   [Attribute](#windows-server-2003-r2-attributes)



| Eingabe | Wert |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | False                                                                                                                     |
| Object-Category             | 0                                                                                                                         |
| Default-Object-Category     | [**Person**](c-person.md)<br/>                                                                                     |
| Governs-Id                  | 2.5.6.7                                                                                                                   |
| Standard-ausblenden-Wert        | 1                                                                                                                         |
| RDN-ATT-ID                  | [**Gemeinsamer Name**](a-cn.md)<br/>                                                                                    |
| Unterklasse von                 | [**Person**](c-person.md)<br/>                                                                                     |
| Mögliche Vorgesetzten          | [**Organisationseinheit**](c-organizationalunit.md) für [**Container**](c-container.md)[**Organisation**](c-organization.md) |
| Zusätzlich           | \-                                                                                                                        |
| NT-Security-Descriptor      | o:Bag: schlecht: S:                                                                                                              |
| Standard Sicherheits Beschreibung | D: (A;; rpwpcrccdclclorcwowdsddtsw;;;D a) (a;; Rpwpcrccdclclorcwowdsddtsw;;; SY) (A;; Rplclorc;;; Thaus                              |
| System-Flags                | 0x00000010                                                                                                                |



## <a name="windows-server-2003-r2-attributes"></a>Windows Server 2003 R2-Attribute

Diese Klasse enthält die folgenden Attribute für Windows Server 2003 R2:



| Attribut                                                                   | Obligatorisch. | Abgeleitet von                                                          |
|-----------------------------------------------------------------------------|-----------|-----------------------------------------------------------------------|
| [**Adresse**](a-streetaddress.md)                                          | False     | **Unternehmensperson**                                             |
| [**Adresse-Startseite**](a-homepostaladdress.md)                                 | False     | **Unternehmensperson**                                             |
| [**Administrator: Beschreibung**](a-admindescription.md)                             | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Administrator-Anzeige Name**](a-admindisplayname.md)                            | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Zulässige Attribute**](a-allowedattributes.md)                           | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Zulässige Attribute-gültig**](a-allowedattributeseffective.md)        | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Zulässige, untergeordnete Klassen**](a-allowedchildclasses.md)                      | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Zulässig-untergeordnete Klassen-gültig**](a-allowedchildclasseseffective.md)   | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Geordneter**](a-assistant.md)                                            | False     | **Unternehmensperson**                                             |
| [**attributecertificateattribute**](a-attributecertificateattribute.md)    | False     | [**Person**](c-person.md)<br/>                                 |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)               | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Kanonischer Name**](a-canonicalname.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Gemeinsamer Name**](a-cn.md)                                                 | Richtig      | [**Person**](c-person.md)<br/> [**Nach oben**](c-top.md)<br/> |
| [**Company**](a-company.md)                                                | False     | **Unternehmensperson**                                             |
| [**Länder Code**](a-countrycode.md)                                       | False     | **Unternehmensperson**                                             |
| [**Länder Name**](a-c.md)                                                 | False     | **Unternehmensperson**                                             |
| [**Create-Zeitstempel**](a-createtimestamp.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Klinik**](a-department.md)                                          | False     | **Unternehmensperson**                                             |
| [**Beschreibung**](a-description.md)                                        | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Ziel-Indikator**](a-destinationindicator.md)                     | False     | **Unternehmensperson**                                             |
| [**Anzeige Name**](a-displayname.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Anzeige Name-druckdruck**](a-displaynameprintable.md)                    | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Division**](a-division.md)                                              | False     | **Unternehmensperson**                                             |
| [**DSA-Signatur**](a-dsasignature.md)                                     | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**DS-Core-propagierungs Daten**](a-dscorepropagationdata.md)                 | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**E-Mail-Adressen**](a-mail.md)                                          | False     | **Unternehmensperson**                                             |
| [**Mitarbeiter-ID**](a-employeeid.md)                                         | False     | **Unternehmensperson**                                             |
| [**Erweiterungs Name**](a-extensionname.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Fax-Telefonnummer**](a-facsimiletelephonenumber.md)            | False     | **Unternehmensperson**                                             |
| [**Fahren**](a-flags.md)                                                    | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Aus-Eintrag**](a-fromentry.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)               | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                   | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**"F"-Rollen Besitzer**](a-fsmoroleowner.md)                                  | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Generierung-Qualifizierer**](a-generationqualifier.md)                       | False     | **Unternehmensperson**                                             |
| [**Vorname**](a-givenname.md)                                           | False     | **Unternehmensperson**                                             |
| [**HouseIdentifier**](a-houseidentifier.md)                                | False     | **Unternehmensperson**                                             |
| [**Initialen**](a-initials.md)                                              | False     | **Unternehmensperson**                                             |
| [**Instanztyp**](a-instancetype.md)                                     | Richtig      | [**Nach oben**](c-top.md)<br/>                                       |
| [**International-ISDN-Number**](a-internationalisdnnumber.md)              | False     | **Unternehmensperson**                                             |
| [**Is-critical-System-Object**](a-iscriticalsystemobject.md)               | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Ist-gelöscht**](a-isdeleted.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Is-Member-of-DL**](a-memberof.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Is-Privilege-Inhaber**](a-isprivilegeholder.md)                          | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Letztes-bekannt/übergeordnetes Element**](a-lastknownparent.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Lokalitäts Name**](a-l.md)                                                | False     | **Unternehmensperson**                                             |
| [**Logo**](a-thumbnaillogo.md)                                             | False     | **Unternehmensperson**                                             |
| [**Verwaltete Objekte**](a-managedobjects.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Dienst**](a-manager.md)                                                | False     | **Unternehmensperson**                                             |
| [**Verwaltet von**](a-masteredby.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**MHS-or-address**](a-mhsoraddress.md)                                    | False     | **Unternehmensperson**                                             |
| [**Modify-Zeitstempel**](a-modifytimestamp.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**MS-com-partitionsetlink**](a-mscom-partitionsetlink.md)                 | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**MS-com-userlink**](a-mscom-userlink.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**MS-DFSR-computerreferencebl**](a-msdfsr-computerreferencebl.md)         | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**MS-DFSR-mitgliedreferencebl**](a-msdfsr-memberreferencebl.md)             | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-allowed-to-Delegat-an**](a-msds-allowedtodelegateto.md)          | False     | **Unternehmensperson**                                             |
| [**ms-DS-ca-immed-untergeordnete Elemente**](a-msds-approx-immed-subordinates.md) | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**MS-DS-Konsistenz-untergeordnet-Anzahl**](a-ms-ds-consistencychildcount.md)      | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-gemastert von**](a-msds-masteredby.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Members-für-AZ-Role-BL**](a-msds-membersforazrolebl.md)           | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-NC-repl-Cursor**](a-msds-ncreplcursors.md)                       | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-NC-repl-Inbound-Nachbarn**](a-msds-ncreplinboundneighbors.md)    | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-NC-repl-Outbound-Nachbarn**](a-msds-ncreploutboundneighbors.md)  | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                         | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)               | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)     | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)     | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)      | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)              | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Tasks-für-AZ-Role-BL**](a-msds-tasksforazrolebl.md)               | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Tasks-für-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)               | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-Exch-House-Identifier**](a-msexchhouseidentifier.md)                 | False     | **Unternehmensperson**                                             |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**msSFU-30-POSIX-Member-of**](a-mssfu30posixmemberof.md)                  | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**NetBoot-SCP-BL**](a-netbootscpbl.md)                                    | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Nicht sicherheitsmitglied-BL**](a-nonsecuritymemberbl.md)                     | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                    | Richtig      | [**Nach oben**](c-top.md)<br/>                                       |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Objekt-Kategorie**](a-objectcategory.md)                                 | Richtig      | [**Nach oben**](c-top.md)<br/>                                       |
| [**Object-Klasse**](a-objectclass.md)                                       | Richtig      | [**Nach oben**](c-top.md)<br/>                                       |
| [**Objekt-GUID**](a-objectguid.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Objekt-Version**](a-objectversion.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Organisations Einheits Name**](a-ou.md)                                    | False     | **Unternehmensperson**                                             |
| [**Name der Organisation**](a-o.md)                                            | False     | **Unternehmensperson**                                             |
| [**Sonstiges-Postfach**](a-othermailbox.md)                                     | False     | **Unternehmensperson**                                             |
| [**Anderer Name**](a-middlename.md)                                          | False     | **Unternehmensperson**                                             |
| [**Andere-bekannte Objekte**](a-otherwellknownobjects.md)                 | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Partial-Attribute-löschen-List**](a-partialattributedeletionlist.md)   | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Partiell-Attribut Satz**](a-partialattributeset.md)                      | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Persönliche Titel**](a-personaltitle.md)                                   | False     | **Unternehmensperson**                                             |
| [**Telefon-Fax-Sonstiges**](a-otherfacsimiletelephonenumber.md)                  | False     | **Unternehmensperson**                                             |
| [**Telefon-privat (Sonstiges)**](a-otherhomephone.md)                                | False     | **Unternehmensperson**                                             |
| [**Telefon-Home-primär**](a-homephone.md)                                   | False     | **Unternehmensperson**                                             |
| [**Telefon-IP-Sonstiges**](a-otheripphone.md)                                    | False     | **Unternehmensperson**                                             |
| [**Telefon-IP-primär**](a-ipphone.md)                                       | False     | **Unternehmensperson**                                             |
| [**Phone-ISDN-Primary**](a-primaryinternationalisdnnumber.md)              | False     | **Unternehmensperson**                                             |
| [**Phone-Mobile-other**](a-othermobile.md)                                 | False     | **Unternehmensperson**                                             |
| [**Phone-Mobile-Primary**](a-mobile.md)                                    | False     | **Unternehmensperson**                                             |
| [**Telefon-Office-Sonstiges**](a-othertelephone.md)                              | False     | **Unternehmensperson**                                             |
| [**Telefon-Pager-Sonstiges**](a-otherpager.md)                                   | False     | **Unternehmensperson**                                             |
| [**Telefon-Pager-primär**](a-pager.md)                                      | False     | **Unternehmensperson**                                             |
| [**Physical-delivery-Office-Name**](a-physicaldeliveryofficename.md)       | False     | **Unternehmensperson**                                             |
| [**Picture**](a-thumbnailphoto.md)                                         | False     | **Unternehmensperson**                                             |
| [**Mögliche-minderwertig**](a-possibleinferiors.md)                           | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Postanschrift**](a-postaladdress.md)                                   | False     | **Unternehmensperson**                                             |
| [**Postleitzahl**](a-postalcode.md)                                         | False     | **Unternehmensperson**                                             |
| [**Post-Office-Box**](a-postofficebox.md)                                  | False     | **Unternehmensperson**                                             |
| [**Bevorzugte Übermittlungs Methode**](a-preferreddeliverymethod.md)              | False     | **Unternehmensperson**                                             |
| [**Proxy-Objekt Name**](a-proxiedobjectname.md)                          | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Proxy Adressen**](a-proxyaddresses.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Abfrage-Richtlinie-BL**](a-querypolicybl.md)                                  | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**RDN**](a-name.md)                                                       | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Registrierte Adresse**](a-registeredaddress.md)                           | False     | **Unternehmensperson**                                             |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                   | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**REPL-Update-Vector**](a-repluptodatevector.md)                        | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Berichte**](a-directreports.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Reps-from**](a-repsfrom.md)                                             | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Reps-to**](a-repsto.md)                                                 | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Novel**](a-revision.md)                                              | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**SD-Rechte**](a-sdrightseffective.md)                          | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Siehe auch**](a-seealso.md)                                               | False     | [**Person**](c-person.md)<br/>                                 |
| [**Seriennummer**](a-serialnumber.md)                                     | False     | [**Person**](c-person.md)<br/>                                 |
| [**Server-Reference-BL**](a-serverreferencebl.md)                          | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Anzeigen-in-Advanced-nur anzeigen**](a-showinadvancedviewonly.md)              | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**State-or-Province-Name**](a-st.md)                                      | False     | **Unternehmensperson**                                             |
| [**Straße**](a-street.md)                                          | False     | **Unternehmensperson**                                             |
| [**Struktur-Objekt-Klasse**](a-structuralobjectclass.md)                  | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Sub-Refs**](a-subrefs.md)                                               | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Subschemasubentry**](a-subschemasubentry.md)                            | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Nachname**](a-sn.md)                                                     | False     | [**Person**](c-person.md)<br/>                                 |
| [**SystemFlags**](a-systemflags.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Telefonnummer**](a-telephonenumber.md)                               | False     | [**Person**](c-person.md)<br/>                                 |
| [**Teletex-Terminal-Identifier**](a-teletexterminalidentifier.md)          | False     | **Unternehmensperson**                                             |
| [**Telex-Nummer**](a-telexnumber.md)                                       | False     | **Unternehmensperson**                                             |
| [**Telex-primär**](a-primarytelexnumber.md)                               | False     | **Unternehmensperson**                                             |
| [**Text-Country**](a-co.md)                                                | False     | **Unternehmensperson**                                             |
| [**Titel**](a-title.md)                                                    | False     | **Unternehmensperson**                                             |
| [**Benutzer Kommentar**](a-comment.md)                                           | False     | **Unternehmensperson**                                             |
| [**Benutzer Kennwort**](a-userpassword.md)                                     | False     | [**Person**](c-person.md)<br/>                                 |
| [**Die Anwendung wurde geändert.**](a-usnchanged.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Von der Anwendung erstellte**](a-usncreated.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**USA-DSA-letzte-obj-entfernt**](a-usndsalastobjremoved.md)                  | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Standort-und standortübergreifende standortübergreifende**](a-usnintersite.md)                                     | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**"An-Last-obj-REM"**](a-usnlastobjrem.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Quell Code Quelle**](a-usnsource.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**WBEM-Pfad**](a-wbempath.md)                                             | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Bekannte Objekte**](a-wellknownobjects.md)                            | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Bei Änderung**](a-whenchanged.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Bei Erstellung**](a-whencreated.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**WWW-Homepage**](a-wwwhomepage.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**WWW-Page-other**](a-url.md)                                             | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**X121-Adresse**](a-x121address.md)                                       | False     | **Unternehmensperson**                                             |



## <a name="windows-server-2008"></a>Windows Server 2008

-   [Attribute](#windows-server-2008-attributes)



| Eingabe | Wert |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | False                                                                                                                     |
| Object-Category             | 0                                                                                                                         |
| Default-Object-Category     | [**Person**](c-person.md)<br/>                                                                                     |
| Governs-Id                  | 2.5.6.7                                                                                                                   |
| Standard-ausblenden-Wert        | 1                                                                                                                         |
| RDN-ATT-ID                  | [**Gemeinsamer Name**](a-cn.md)<br/>                                                                                    |
| Unterklasse von                 | [**Person**](c-person.md)<br/>                                                                                     |
| Mögliche Vorgesetzten          | [**Organisationseinheit**](c-organizationalunit.md) für [**Container**](c-container.md)[**Organisation**](c-organization.md) |
| Zusätzlich           | \-                                                                                                                        |
| NT-Security-Descriptor      | o:Bag: schlecht: S:                                                                                                              |
| Standard Sicherheits Beschreibung | D: (A;; rpwpcrccdclclorcwowdsddtsw;;;D a) (a;; Rpwpcrccdclclorcwowdsddtsw;;; SY) (A;; Rplclorc;;; Thaus                              |
| System-Flags                | 0x00000010                                                                                                                |



## <a name="windows-server-2008-attributes"></a>Windows Server 2008-Attribute

Diese Klasse enthält die folgenden Attribute für Windows Server 2008:



| Attribut                                                                      | Obligatorisch. | Abgeleitet von                                                          |
|--------------------------------------------------------------------------------|-----------|-----------------------------------------------------------------------|
| [**Adresse**](a-streetaddress.md)                                             | False     | **Unternehmensperson**                                             |
| [**Adresse-Startseite**](a-homepostaladdress.md)                                    | False     | **Unternehmensperson**                                             |
| [**Administrator: Beschreibung**](a-admindescription.md)                                | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Administrator-Anzeige Name**](a-admindisplayname.md)                               | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Zulässige Attribute**](a-allowedattributes.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Zulässige Attribute-gültig**](a-allowedattributeseffective.md)           | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Zulässige, untergeordnete Klassen**](a-allowedchildclasses.md)                         | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Zulässig-untergeordnete Klassen-gültig**](a-allowedchildclasseseffective.md)      | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Geordneter**](a-assistant.md)                                               | False     | **Unternehmensperson**                                             |
| [**attributecertificateattribute**](a-attributecertificateattribute.md)       | False     | [**Person**](c-person.md)<br/>                                 |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                  | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Kanonischer Name**](a-canonicalname.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Gemeinsamer Name**](a-cn.md)                                                    | Richtig      | [**Person**](c-person.md)<br/> [**Nach oben**](c-top.md)<br/> |
| [**Company**](a-company.md)                                                   | False     | **Unternehmensperson**                                             |
| [**Länder Code**](a-countrycode.md)                                          | False     | **Unternehmensperson**                                             |
| [**Länder Name**](a-c.md)                                                    | False     | **Unternehmensperson**                                             |
| [**Create-Zeitstempel**](a-createtimestamp.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Klinik**](a-department.md)                                             | False     | **Unternehmensperson**                                             |
| [**Beschreibung**](a-description.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Ziel-Indikator**](a-destinationindicator.md)                        | False     | **Unternehmensperson**                                             |
| [**Anzeige Name**](a-displayname.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Anzeige Name-druckdruck**](a-displaynameprintable.md)                       | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Division**](a-division.md)                                                 | False     | **Unternehmensperson**                                             |
| [**DSA-Signatur**](a-dsasignature.md)                                        | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**DS-Core-propagierungs Daten**](a-dscorepropagationdata.md)                    | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**E-Mail-Adressen**](a-mail.md)                                             | False     | **Unternehmensperson**                                             |
| [**Mitarbeiter-ID**](a-employeeid.md)                                            | False     | **Unternehmensperson**                                             |
| [**Erweiterungs Name**](a-extensionname.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Fax-Telefonnummer**](a-facsimiletelephonenumber.md)               | False     | **Unternehmensperson**                                             |
| [**Fahren**](a-flags.md)                                                       | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Aus-Eintrag**](a-fromentry.md)                                              | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                  | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                      | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**"F"-Rollen Besitzer**](a-fsmoroleowner.md)                                     | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Generierung-Qualifizierer**](a-generationqualifier.md)                          | False     | **Unternehmensperson**                                             |
| [**Vorname**](a-givenname.md)                                              | False     | **Unternehmensperson**                                             |
| [**HouseIdentifier**](a-houseidentifier.md)                                   | False     | **Unternehmensperson**                                             |
| [**Initialen**](a-initials.md)                                                 | False     | **Unternehmensperson**                                             |
| [**Instanztyp**](a-instancetype.md)                                        | Richtig      | [**Nach oben**](c-top.md)<br/>                                       |
| [**International-ISDN-Number**](a-internationalisdnnumber.md)                 | False     | **Unternehmensperson**                                             |
| [**Is-critical-System-Object**](a-iscriticalsystemobject.md)                  | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Ist-gelöscht**](a-isdeleted.md)                                              | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Is-Member-of-DL**](a-memberof.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Is-Privilege-Inhaber**](a-isprivilegeholder.md)                             | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Letztes-bekannt/übergeordnetes Element**](a-lastknownparent.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Lokalitäts Name**](a-l.md)                                                   | False     | **Unternehmensperson**                                             |
| [**Logo**](a-thumbnaillogo.md)                                                | False     | **Unternehmensperson**                                             |
| [**Verwaltete Objekte**](a-managedobjects.md)                                    | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Dienst**](a-manager.md)                                                   | False     | **Unternehmensperson**                                             |
| [**Verwaltet von**](a-masteredby.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**MHS-or-address**](a-mhsoraddress.md)                                       | False     | **Unternehmensperson**                                             |
| [**Modify-Zeitstempel**](a-modifytimestamp.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**MS-com-partitionsetlink**](a-mscom-partitionsetlink.md)                    | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**MS-com-userlink**](a-mscom-userlink.md)                                    | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**MS-DFSR-computerreferencebl**](a-msdfsr-computerreferencebl.md)            | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**MS-DFSR-mitgliedreferencebl**](a-msdfsr-memberreferencebl.md)                | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-allowed-to-Delegat-an**](a-msds-allowedtodelegateto.md)             | False     | **Unternehmensperson**                                             |
| [**ms-DS-ca-immed-untergeordnete Elemente**](a-msds-approx-immed-subordinates.md)    | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-authentieredto-accountlist**](a-msds-authenticatedtoaccountlist.md) | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**MS-DS-Konsistenz-untergeordnet-Anzahl**](a-ms-ds-consistencychildcount.md)         | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                      | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-hab-Seniority-Index**](a-msds-habseniorityindex.md)                  | False     | **Unternehmensperson**                                             |
| [**ms-DS-is-Domain-for**](a-msds-isdomainfor.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-is-full-Replica-for**](a-msds-isfullreplicafor.md)                   | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-is-Partial-Replica-for**](a-msds-ispartialreplicafor.md)             | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-krbtgt-Link-BL**](a-msds-krbtgtlinkbl.md)                            | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-gemastert von**](a-msds-masteredby.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Members-für-AZ-Role-BL**](a-msds-membersforazrolebl.md)              | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-NC-repl-Cursor**](a-msds-ncreplcursors.md)                          | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-NC-repl-Inbound-Nachbarn**](a-msds-ncreplinboundneighbors.md)       | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-NC-repl-Outbound-Nachbarn**](a-msds-ncreploutboundneighbors.md)     | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)  | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-NC-Typ**](a-msds-nctype.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                            | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                  | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)        | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)        | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Phonetic-Company-Name**](a-msds-phoneticcompanyname.md)              | False     | **Unternehmensperson**                                             |
| [**ms-DS-Phonetic-Department**](a-msds-phoneticdepartment.md)                 | False     | **Unternehmensperson**                                             |
| [**ms-DS-Phonetic-Display-Name**](a-msds-phoneticdisplayname.md)              | False     | **Unternehmensperson**                                             |
| [**ms-DS-Phonetic-First-Name**](a-msds-phoneticfirstname.md)                  | False     | **Unternehmensperson**                                             |
| [**ms-DS-Phonetic-Last-Name**](a-msds-phoneticlastname.md)                    | False     | **Unternehmensperson**                                             |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                           | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-PSO-angewendet**](a-msds-psoapplied.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)         | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                 | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-offengelegt-DSAs**](a-msds-revealeddsas.md)                             | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-enthüllt-List-BL**](a-msds-revealedlistbl.md)                        | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Tasks-für-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                  | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Tasks-für-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                  | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-Exch-House-Identifier**](a-msexchhouseidentifier.md)                    | False     | **Unternehmensperson**                                             |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**msSFU-30-POSIX-Member-of**](a-mssfu30posixmemberof.md)                     | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**NetBoot-SCP-BL**](a-netbootscpbl.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Nicht sicherheitsmitglied-BL**](a-nonsecuritymemberbl.md)                        | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                       | Richtig      | [**Nach oben**](c-top.md)<br/>                                       |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Objekt-Kategorie**](a-objectcategory.md)                                    | Richtig      | [**Nach oben**](c-top.md)<br/>                                       |
| [**Object-Klasse**](a-objectclass.md)                                          | Richtig      | [**Nach oben**](c-top.md)<br/>                                       |
| [**Objekt-GUID**](a-objectguid.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Objekt-Version**](a-objectversion.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Organisations Einheits Name**](a-ou.md)                                       | False     | **Unternehmensperson**                                             |
| [**Name der Organisation**](a-o.md)                                               | False     | **Unternehmensperson**                                             |
| [**Sonstiges-Postfach**](a-othermailbox.md)                                        | False     | **Unternehmensperson**                                             |
| [**Anderer Name**](a-middlename.md)                                             | False     | **Unternehmensperson**                                             |
| [**Andere-bekannte Objekte**](a-otherwellknownobjects.md)                    | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Partial-Attribute-löschen-List**](a-partialattributedeletionlist.md)      | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Partiell-Attribut Satz**](a-partialattributeset.md)                         | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Persönliche Titel**](a-personaltitle.md)                                      | False     | **Unternehmensperson**                                             |
| [**Telefon-Fax-Sonstiges**](a-otherfacsimiletelephonenumber.md)                     | False     | **Unternehmensperson**                                             |
| [**Telefon-privat (Sonstiges)**](a-otherhomephone.md)                                   | False     | **Unternehmensperson**                                             |
| [**Telefon-Home-primär**](a-homephone.md)                                      | False     | **Unternehmensperson**                                             |
| [**Telefon-IP-Sonstiges**](a-otheripphone.md)                                       | False     | **Unternehmensperson**                                             |
| [**Telefon-IP-primär**](a-ipphone.md)                                          | False     | **Unternehmensperson**                                             |
| [**Phone-ISDN-Primary**](a-primaryinternationalisdnnumber.md)                 | False     | **Unternehmensperson**                                             |
| [**Phone-Mobile-other**](a-othermobile.md)                                    | False     | **Unternehmensperson**                                             |
| [**Phone-Mobile-Primary**](a-mobile.md)                                       | False     | **Unternehmensperson**                                             |
| [**Telefon-Office-Sonstiges**](a-othertelephone.md)                                 | False     | **Unternehmensperson**                                             |
| [**Telefon-Pager-Sonstiges**](a-otherpager.md)                                      | False     | **Unternehmensperson**                                             |
| [**Telefon-Pager-primär**](a-pager.md)                                         | False     | **Unternehmensperson**                                             |
| [**Physical-delivery-Office-Name**](a-physicaldeliveryofficename.md)          | False     | **Unternehmensperson**                                             |
| [**Picture**](a-thumbnailphoto.md)                                            | False     | **Unternehmensperson**                                             |
| [**Mögliche-minderwertig**](a-possibleinferiors.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Postanschrift**](a-postaladdress.md)                                      | False     | **Unternehmensperson**                                             |
| [**Postleitzahl**](a-postalcode.md)                                            | False     | **Unternehmensperson**                                             |
| [**Post-Office-Box**](a-postofficebox.md)                                     | False     | **Unternehmensperson**                                             |
| [**Bevorzugte Übermittlungs Methode**](a-preferreddeliverymethod.md)                 | False     | **Unternehmensperson**                                             |
| [**Proxy-Objekt Name**](a-proxiedobjectname.md)                             | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Proxy Adressen**](a-proxyaddresses.md)                                    | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Abfrage-Richtlinie-BL**](a-querypolicybl.md)                                     | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**RDN**](a-name.md)                                                          | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Registrierte Adresse**](a-registeredaddress.md)                              | False     | **Unternehmensperson**                                             |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                      | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**REPL-Update-Vector**](a-repluptodatevector.md)                           | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Berichte**](a-directreports.md)                                             | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Reps-from**](a-repsfrom.md)                                                | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Reps-to**](a-repsto.md)                                                    | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Novel**](a-revision.md)                                                 | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**SD-Rechte**](a-sdrightseffective.md)                             | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Siehe auch**](a-seealso.md)                                                  | False     | [**Person**](c-person.md)<br/>                                 |
| [**Seriennummer**](a-serialnumber.md)                                        | False     | [**Person**](c-person.md)<br/>                                 |
| [**Server-Reference-BL**](a-serverreferencebl.md)                             | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Anzeigen-in-Advanced-nur anzeigen**](a-showinadvancedviewonly.md)                 | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Site-Object-BL**](a-siteobjectbl.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**State-or-Province-Name**](a-st.md)                                         | False     | **Unternehmensperson**                                             |
| [**Straße**](a-street.md)                                             | False     | **Unternehmensperson**                                             |
| [**Struktur-Objekt-Klasse**](a-structuralobjectclass.md)                     | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Sub-Refs**](a-subrefs.md)                                                  | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Subschemasubentry**](a-subschemasubentry.md)                               | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Nachname**](a-sn.md)                                                        | False     | [**Person**](c-person.md)<br/>                                 |
| [**SystemFlags**](a-systemflags.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Telefonnummer**](a-telephonenumber.md)                                  | False     | [**Person**](c-person.md)<br/>                                 |
| [**Teletex-Terminal-Identifier**](a-teletexterminalidentifier.md)             | False     | **Unternehmensperson**                                             |
| [**Telex-Nummer**](a-telexnumber.md)                                          | False     | **Unternehmensperson**                                             |
| [**Telex-primär**](a-primarytelexnumber.md)                                  | False     | **Unternehmensperson**                                             |
| [**Text-Country**](a-co.md)                                                   | False     | **Unternehmensperson**                                             |
| [**Titel**](a-title.md)                                                       | False     | **Unternehmensperson**                                             |
| [**Benutzer Kommentar**](a-comment.md)                                              | False     | **Unternehmensperson**                                             |
| [**Benutzer Kennwort**](a-userpassword.md)                                        | False     | [**Person**](c-person.md)<br/>                                 |
| [**Die Anwendung wurde geändert.**](a-usnchanged.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Von der Anwendung erstellte**](a-usncreated.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**USA-DSA-letzte-obj-entfernt**](a-usndsalastobjremoved.md)                     | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Standort-und standortübergreifende standortübergreifende**](a-usnintersite.md)                                        | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**"An-Last-obj-REM"**](a-usnlastobjrem.md)                                    | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Quell Code Quelle**](a-usnsource.md)                                              | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**WBEM-Pfad**](a-wbempath.md)                                                | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Bekannte Objekte**](a-wellknownobjects.md)                               | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Bei Änderung**](a-whenchanged.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Bei Erstellung**](a-whencreated.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**WWW-Homepage**](a-wwwhomepage.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**WWW-Page-other**](a-url.md)                                                | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**X121-Adresse**](a-x121address.md)                                          | False     | **Unternehmensperson**                                             |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2

-   [Attribute](#windows-server-2008-r2-attributes)



| Eingabe | Wert |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | False                                                                                                                     |
| Object-Category             | 0                                                                                                                         |
| Default-Object-Category     | [**Person**](c-person.md)<br/>                                                                                     |
| Governs-Id                  | 2.5.6.7                                                                                                                   |
| Standard-ausblenden-Wert        | 1                                                                                                                         |
| RDN-ATT-ID                  | [**Gemeinsamer Name**](a-cn.md)<br/>                                                                                    |
| Unterklasse von                 | [**Person**](c-person.md)<br/>                                                                                     |
| Mögliche Vorgesetzten          | [**Organisationseinheit**](c-organizationalunit.md) für [**Container**](c-container.md)[**Organisation**](c-organization.md) |
| Zusätzlich           | \-                                                                                                                        |
| NT-Security-Descriptor      | o:Bag: schlecht: S:                                                                                                              |
| Standard Sicherheits Beschreibung | D: (A;; rpwpcrccdclclorcwowdsddtsw;;;D a) (a;; Rpwpcrccdclclorcwowdsddtsw;;; SY) (A;; Rplclorc;;; Thaus                              |
| System-Flags                | 0x00000010                                                                                                                |



## <a name="windows-server-2008-r2-attributes"></a>Windows Server 2008 R2-Attribute

Diese Klasse enthält die folgenden Attribute für Windows Server 2008 R2:



| Attribut                                                                        | Obligatorisch. | Abgeleitet von                                                          |
|----------------------------------------------------------------------------------|-----------|-----------------------------------------------------------------------|
| [**Adresse**](a-streetaddress.md)                                               | False     | **Unternehmensperson**                                             |
| [**Adresse-Startseite**](a-homepostaladdress.md)                                      | False     | **Unternehmensperson**                                             |
| [**Administrator: Beschreibung**](a-admindescription.md)                                  | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Administrator-Anzeige Name**](a-admindisplayname.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Zulässige Attribute**](a-allowedattributes.md)                                | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Zulässige Attribute-gültig**](a-allowedattributeseffective.md)             | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Zulässige, untergeordnete Klassen**](a-allowedchildclasses.md)                           | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Zulässig-untergeordnete Klassen-gültig**](a-allowedchildclasseseffective.md)        | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Geordneter**](a-assistant.md)                                                 | False     | **Unternehmensperson**                                             |
| [**attributecertificateattribute**](a-attributecertificateattribute.md)         | False     | [**Person**](c-person.md)<br/>                                 |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                    | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Kanonischer Name**](a-canonicalname.md)                                        | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Gemeinsamer Name**](a-cn.md)                                                      | Richtig      | [**Person**](c-person.md)<br/> [**Nach oben**](c-top.md)<br/> |
| [**Company**](a-company.md)                                                     | False     | **Unternehmensperson**                                             |
| [**Länder Code**](a-countrycode.md)                                            | False     | **Unternehmensperson**                                             |
| [**Länder Name**](a-c.md)                                                      | False     | **Unternehmensperson**                                             |
| [**Create-Zeitstempel**](a-createtimestamp.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Klinik**](a-department.md)                                               | False     | **Unternehmensperson**                                             |
| [**Beschreibung**](a-description.md)                                             | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Ziel-Indikator**](a-destinationindicator.md)                          | False     | **Unternehmensperson**                                             |
| [**Anzeige Name**](a-displayname.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Anzeige Name-druckdruck**](a-displaynameprintable.md)                         | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Division**](a-division.md)                                                   | False     | **Unternehmensperson**                                             |
| [**DSA-Signatur**](a-dsasignature.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**DS-Core-propagierungs Daten**](a-dscorepropagationdata.md)                      | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**E-Mail-Adressen**](a-mail.md)                                               | False     | **Unternehmensperson**                                             |
| [**Mitarbeiter-ID**](a-employeeid.md)                                              | False     | **Unternehmensperson**                                             |
| [**Erweiterungs Name**](a-extensionname.md)                                        | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Fax-Telefonnummer**](a-facsimiletelephonenumber.md)                 | False     | **Unternehmensperson**                                             |
| [**Fahren**](a-flags.md)                                                         | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Aus-Eintrag**](a-fromentry.md)                                                | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                    | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                        | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**"F"-Rollen Besitzer**](a-fsmoroleowner.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Generierung-Qualifizierer**](a-generationqualifier.md)                            | False     | **Unternehmensperson**                                             |
| [**Vorname**](a-givenname.md)                                                | False     | **Unternehmensperson**                                             |
| [**HouseIdentifier**](a-houseidentifier.md)                                     | False     | **Unternehmensperson**                                             |
| [**Initialen**](a-initials.md)                                                   | False     | **Unternehmensperson**                                             |
| [**Instanztyp**](a-instancetype.md)                                          | Richtig      | [**Nach oben**](c-top.md)<br/>                                       |
| [**International-ISDN-Number**](a-internationalisdnnumber.md)                   | False     | **Unternehmensperson**                                             |
| [**Is-critical-System-Object**](a-iscriticalsystemobject.md)                    | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Ist-gelöscht**](a-isdeleted.md)                                                | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Is-Member-of-DL**](a-memberof.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Is-Privilege-Inhaber**](a-isprivilegeholder.md)                               | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Ist-recycelt**](a-isrecycled.md)                                              | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Letztes-bekannt/übergeordnetes Element**](a-lastknownparent.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Lokalitäts Name**](a-l.md)                                                     | False     | **Unternehmensperson**                                             |
| [**Logo**](a-thumbnaillogo.md)                                                  | False     | **Unternehmensperson**                                             |
| [**Verwaltete Objekte**](a-managedobjects.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Dienst**](a-manager.md)                                                     | False     | **Unternehmensperson**                                             |
| [**Verwaltet von**](a-masteredby.md)                                              | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**MHS-or-address**](a-mhsoraddress.md)                                         | False     | **Unternehmensperson**                                             |
| [**Modify-Zeitstempel**](a-modifytimestamp.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**MS-com-partitionsetlink**](a-mscom-partitionsetlink.md)                      | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**MS-com-userlink**](a-mscom-userlink.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**MS-DFSR-computerreferencebl**](a-msdfsr-computerreferencebl.md)              | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**MS-DFSR-mitgliedreferencebl**](a-msdfsr-memberreferencebl.md)                  | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-allowed-to-Delegat-an**](a-msds-allowedtodelegateto.md)               | False     | **Unternehmensperson**                                             |
| [**ms-DS-ca-immed-untergeordnete Elemente**](a-msds-approx-immed-subordinates.md)      | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-authentieredto-accountlist**](a-msds-authenticatedtoaccountlist.md)   | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**MS-DS-Konsistenz-untergeordnet-Anzahl**](a-ms-ds-consistencychildcount.md)           | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                        | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-aktiviert-Feature-BL**](a-msds-enabledfeaturebl.md)                      | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-hab-Seniority-Index**](a-msds-habseniorityindex.md)                    | False     | **Unternehmensperson**                                             |
| [**ms-DS-Host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)             | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-is-Domain-for**](a-msds-isdomainfor.md)                                | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-is-full-Replica-for**](a-msds-isfullreplicafor.md)                     | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-is-Partial-Replica-for**](a-msds-ispartialreplicafor.md)               | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-krbtgt-Link-BL**](a-msds-krbtgtlinkbl.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-local-Effective-Lösch Zeit**](a-msds-localeffectivedeletiontime.md) | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-local-Effective-Papier-Time**](a-msds-localeffectiverecycletime.md)   | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-gemastert von**](a-msds-masteredby.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Members-für-AZ-Role-BL**](a-msds-membersforazrolebl.md)                | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-NC-repl-Cursor**](a-msds-ncreplcursors.md)                            | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-NC-repl-Inbound-Nachbarn**](a-msds-ncreplinboundneighbors.md)         | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-NC-repl-Outbound-Nachbarn**](a-msds-ncreploutboundneighbors.md)       | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)    | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-NC-Typ**](a-msds-nctype.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                    | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-oidtoidgruppe-Link-BL**](a-msds-oidtogrouplinkbl.md)                      | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)          | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)          | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Phonetic-Company-Name**](a-msds-phoneticcompanyname.md)                | False     | **Unternehmensperson**                                             |
| [**ms-DS-Phonetic-Department**](a-msds-phoneticdepartment.md)                   | False     | **Unternehmensperson**                                             |
| [**ms-DS-Phonetic-Display-Name**](a-msds-phoneticdisplayname.md)                | False     | **Unternehmensperson**                                             |
| [**ms-DS-Phonetic-First-Name**](a-msds-phoneticfirstname.md)                    | False     | **Unternehmensperson**                                             |
| [**ms-DS-Phonetic-Last-Name**](a-msds-phoneticlastname.md)                      | False     | **Unternehmensperson**                                             |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                             | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-PSO-angewendet**](a-msds-psoapplied.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)           | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                   | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-offengelegt-DSAs**](a-msds-revealeddsas.md)                               | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-enthüllt-List-BL**](a-msds-revealedlistbl.md)                          | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Tasks-für-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                    | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Tasks-für-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                    | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-Exch-House-Identifier**](a-msexchhouseidentifier.md)                      | False     | **Unternehmensperson**                                             |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**msSFU-30-POSIX-Member-of**](a-mssfu30posixmemberof.md)                       | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**NetBoot-SCP-BL**](a-netbootscpbl.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Nicht sicherheitsmitglied-BL**](a-nonsecuritymemberbl.md)                          | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                         | Richtig      | [**Nach oben**](c-top.md)<br/>                                       |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                     | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Objekt-Kategorie**](a-objectcategory.md)                                      | Richtig      | [**Nach oben**](c-top.md)<br/>                                       |
| [**Object-Klasse**](a-objectclass.md)                                            | Richtig      | [**Nach oben**](c-top.md)<br/>                                       |
| [**Objekt-GUID**](a-objectguid.md)                                              | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Objekt-Version**](a-objectversion.md)                                        | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Organisations Einheits Name**](a-ou.md)                                         | False     | **Unternehmensperson**                                             |
| [**Name der Organisation**](a-o.md)                                                 | False     | **Unternehmensperson**                                             |
| [**Sonstiges-Postfach**](a-othermailbox.md)                                          | False     | **Unternehmensperson**                                             |
| [**Anderer Name**](a-middlename.md)                                               | False     | **Unternehmensperson**                                             |
| [**Andere-bekannte Objekte**](a-otherwellknownobjects.md)                      | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Partial-Attribute-löschen-List**](a-partialattributedeletionlist.md)        | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Partiell-Attribut Satz**](a-partialattributeset.md)                           | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Persönliche Titel**](a-personaltitle.md)                                        | False     | **Unternehmensperson**                                             |
| [**Telefon-Fax-Sonstiges**](a-otherfacsimiletelephonenumber.md)                       | False     | **Unternehmensperson**                                             |
| [**Telefon-privat (Sonstiges)**](a-otherhomephone.md)                                     | False     | **Unternehmensperson**                                             |
| [**Telefon-Home-primär**](a-homephone.md)                                        | False     | **Unternehmensperson**                                             |
| [**Telefon-IP-Sonstiges**](a-otheripphone.md)                                         | False     | **Unternehmensperson**                                             |
| [**Telefon-IP-primär**](a-ipphone.md)                                            | False     | **Unternehmensperson**                                             |
| [**Phone-ISDN-Primary**](a-primaryinternationalisdnnumber.md)                   | False     | **Unternehmensperson**                                             |
| [**Phone-Mobile-other**](a-othermobile.md)                                      | False     | **Unternehmensperson**                                             |
| [**Phone-Mobile-Primary**](a-mobile.md)                                         | False     | **Unternehmensperson**                                             |
| [**Telefon-Office-Sonstiges**](a-othertelephone.md)                                   | False     | **Unternehmensperson**                                             |
| [**Telefon-Pager-Sonstiges**](a-otherpager.md)                                        | False     | **Unternehmensperson**                                             |
| [**Telefon-Pager-primär**](a-pager.md)                                           | False     | **Unternehmensperson**                                             |
| [**Physical-delivery-Office-Name**](a-physicaldeliveryofficename.md)            | False     | **Unternehmensperson**                                             |
| [**Picture**](a-thumbnailphoto.md)                                              | False     | **Unternehmensperson**                                             |
| [**Mögliche-minderwertig**](a-possibleinferiors.md)                                | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Postanschrift**](a-postaladdress.md)                                        | False     | **Unternehmensperson**                                             |
| [**Postleitzahl**](a-postalcode.md)                                              | False     | **Unternehmensperson**                                             |
| [**Post-Office-Box**](a-postofficebox.md)                                       | False     | **Unternehmensperson**                                             |
| [**Bevorzugte Übermittlungs Methode**](a-preferreddeliverymethod.md)                   | False     | **Unternehmensperson**                                             |
| [**Proxy-Objekt Name**](a-proxiedobjectname.md)                               | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Proxy Adressen**](a-proxyaddresses.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Abfrage-Richtlinie-BL**](a-querypolicybl.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**RDN**](a-name.md)                                                            | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Registrierte Adresse**](a-registeredaddress.md)                                | False     | **Unternehmensperson**                                             |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                        | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**REPL-Update-Vector**](a-repluptodatevector.md)                             | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Berichte**](a-directreports.md)                                               | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Reps-from**](a-repsfrom.md)                                                  | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Reps-to**](a-repsto.md)                                                      | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Novel**](a-revision.md)                                                   | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**SD-Rechte**](a-sdrightseffective.md)                               | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Siehe auch**](a-seealso.md)                                                    | False     | [**Person**](c-person.md)<br/>                                 |
| [**Seriennummer**](a-serialnumber.md)                                          | False     | [**Person**](c-person.md)<br/>                                 |
| [**Server-Reference-BL**](a-serverreferencebl.md)                               | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Anzeigen-in-Advanced-nur anzeigen**](a-showinadvancedviewonly.md)                   | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Site-Object-BL**](a-siteobjectbl.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**State-or-Province-Name**](a-st.md)                                           | False     | **Unternehmensperson**                                             |
| [**Straße**](a-street.md)                                               | False     | **Unternehmensperson**                                             |
| [**Struktur-Objekt-Klasse**](a-structuralobjectclass.md)                       | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Sub-Refs**](a-subrefs.md)                                                    | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Subschemasubentry**](a-subschemasubentry.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Nachname**](a-sn.md)                                                          | False     | [**Person**](c-person.md)<br/>                                 |
| [**SystemFlags**](a-systemflags.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Telefonnummer**](a-telephonenumber.md)                                    | False     | [**Person**](c-person.md)<br/>                                 |
| [**Teletex-Terminal-Identifier**](a-teletexterminalidentifier.md)               | False     | **Unternehmensperson**                                             |
| [**Telex-Nummer**](a-telexnumber.md)                                            | False     | **Unternehmensperson**                                             |
| [**Telex-primär**](a-primarytelexnumber.md)                                    | False     | **Unternehmensperson**                                             |
| [**Text-Country**](a-co.md)                                                     | False     | **Unternehmensperson**                                             |
| [**Titel**](a-title.md)                                                         | False     | **Unternehmensperson**                                             |
| [**Benutzer Kommentar**](a-comment.md)                                                | False     | **Unternehmensperson**                                             |
| [**Benutzer Kennwort**](a-userpassword.md)                                          | False     | [**Person**](c-person.md)<br/>                                 |
| [**Die Anwendung wurde geändert.**](a-usnchanged.md)                                              | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Von der Anwendung erstellte**](a-usncreated.md)                                              | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**USA-DSA-letzte-obj-entfernt**](a-usndsalastobjremoved.md)                       | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Standort-und standortübergreifende standortübergreifende**](a-usnintersite.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**"An-Last-obj-REM"**](a-usnlastobjrem.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Quell Code Quelle**](a-usnsource.md)                                                | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**WBEM-Pfad**](a-wbempath.md)                                                  | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Bekannte Objekte**](a-wellknownobjects.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Bei Änderung**](a-whenchanged.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Bei Erstellung**](a-whencreated.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**WWW-Homepage**](a-wwwhomepage.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**WWW-Page-other**](a-url.md)                                                  | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**X121-Adresse**](a-x121address.md)                                            | False     | **Unternehmensperson**                                             |



## <a name="windows-server-2012"></a>Windows Server 2012

-   [Attribute](#windows-server-2012-attributes)



| Eingabe | Wert |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | False                                                                                                                     |
| Object-Category             | 0                                                                                                                         |
| Default-Object-Category     | [**Person**](c-person.md)<br/>                                                                                     |
| Governs-Id                  | 2.5.6.7                                                                                                                   |
| Standard-ausblenden-Wert        | 1                                                                                                                         |
| RDN-ATT-ID                  | [**Gemeinsamer Name**](a-cn.md)<br/>                                                                                    |
| Unterklasse von                 | [**Person**](c-person.md)<br/>                                                                                     |
| Mögliche Vorgesetzten          | [**Organisationseinheit**](c-organizationalunit.md) für [**Container**](c-container.md)[**Organisation**](c-organization.md) |
| Zusätzlich           | \-                                                                                                                        |
| NT-Security-Descriptor      | o:Bag: schlecht: S:                                                                                                              |
| Standard Sicherheits Beschreibung | D: (A;; rpwpcrccdclclorcwowdsddtsw;;;D a) (a;; Rpwpcrccdclclorcwowdsddtsw;;; SY) (A;; Rplclorc;;; Thaus                              |
| System-Flags                | 0x00000010                                                                                                                |



## <a name="windows-server-2012-attributes"></a>Windows Server 2012-Attribute

Diese Klasse enthält die folgenden Attribute für Windows Server 2012:



| Attribut                                                                                              | Obligatorisch. | Abgeleitet von                                                          |
|--------------------------------------------------------------------------------------------------------|-----------|-----------------------------------------------------------------------|
| [**Adresse**](a-streetaddress.md)                                                                     | False     | **Unternehmensperson**                                             |
| [**Adresse-Startseite**](a-homepostaladdress.md)                                                            | False     | **Unternehmensperson**                                             |
| [**Administrator: Beschreibung**](a-admindescription.md)                                                        | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Administrator-Anzeige Name**](a-admindisplayname.md)                                                       | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Zulässige Attribute**](a-allowedattributes.md)                                                      | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Zulässige Attribute-gültig**](a-allowedattributeseffective.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Zulässige, untergeordnete Klassen**](a-allowedchildclasses.md)                                                 | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Zulässig-untergeordnete Klassen-gültig**](a-allowedchildclasseseffective.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Geordneter**](a-assistant.md)                                                                       | False     | **Unternehmensperson**                                             |
| [**attributecertificateattribute**](a-attributecertificateattribute.md)                               | False     | [**Person**](c-person.md)<br/>                                 |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Kanonischer Name**](a-canonicalname.md)                                                              | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Gemeinsamer Name**](a-cn.md)                                                                            | Richtig      | [**Person**](c-person.md)<br/> [**Nach oben**](c-top.md)<br/> |
| [**Company**](a-company.md)                                                                           | False     | **Unternehmensperson**                                             |
| [**Länder Code**](a-countrycode.md)                                                                  | False     | **Unternehmensperson**                                             |
| [**Länder Name**](a-c.md)                                                                            | False     | **Unternehmensperson**                                             |
| [**Create-Zeitstempel**](a-createtimestamp.md)                                                         | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Klinik**](a-department.md)                                                                     | False     | **Unternehmensperson**                                             |
| [**Beschreibung**](a-description.md)                                                                   | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Ziel-Indikator**](a-destinationindicator.md)                                                | False     | **Unternehmensperson**                                             |
| [**Anzeige Name**](a-displayname.md)                                                                  | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Anzeige Name-druckdruck**](a-displaynameprintable.md)                                               | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Division**](a-division.md)                                                                         | False     | **Unternehmensperson**                                             |
| [**DSA-Signatur**](a-dsasignature.md)                                                                | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**DS-Core-propagierungs Daten**](a-dscorepropagationdata.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**E-Mail-Adressen**](a-mail.md)                                                                     | False     | **Unternehmensperson**                                             |
| [**Mitarbeiter-ID**](a-employeeid.md)                                                                    | False     | **Unternehmensperson**                                             |
| [**Erweiterungs Name**](a-extensionname.md)                                                              | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Fax-Telefonnummer**](a-facsimiletelephonenumber.md)                                       | False     | **Unternehmensperson**                                             |
| [**Fahren**](a-flags.md)                                                                               | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Aus-Eintrag**](a-fromentry.md)                                                                      | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                                              | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**"F"-Rollen Besitzer**](a-fsmoroleowner.md)                                                             | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Generierung-Qualifizierer**](a-generationqualifier.md)                                                  | False     | **Unternehmensperson**                                             |
| [**Vorname**](a-givenname.md)                                                                      | False     | **Unternehmensperson**                                             |
| [**HouseIdentifier**](a-houseidentifier.md)                                                           | False     | **Unternehmensperson**                                             |
| [**Initialen**](a-initials.md)                                                                         | False     | **Unternehmensperson**                                             |
| [**Instanztyp**](a-instancetype.md)                                                                | Richtig      | [**Nach oben**](c-top.md)<br/>                                       |
| [**International-ISDN-Number**](a-internationalisdnnumber.md)                                         | False     | **Unternehmensperson**                                             |
| [**Is-critical-System-Object**](a-iscriticalsystemobject.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Ist-gelöscht**](a-isdeleted.md)                                                                      | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Is-Member-of-DL**](a-memberof.md)                                                                  | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Is-Privilege-Inhaber**](a-isprivilegeholder.md)                                                     | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Ist-recycelt**](a-isrecycled.md)                                                                    | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Letztes-bekannt/übergeordnetes Element**](a-lastknownparent.md)                                                         | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Lokalitäts Name**](a-l.md)                                                                           | False     | **Unternehmensperson**                                             |
| [**Logo**](a-thumbnaillogo.md)                                                                        | False     | **Unternehmensperson**                                             |
| [**Verwaltete Objekte**](a-managedobjects.md)                                                            | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Dienst**](a-manager.md)                                                                           | False     | **Unternehmensperson**                                             |
| [**Verwaltet von**](a-masteredby.md)                                                                    | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**MHS-or-address**](a-mhsoraddress.md)                                                               | False     | **Unternehmensperson**                                             |
| [**Modify-Zeitstempel**](a-modifytimestamp.md)                                                         | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**MS-com-partitionsetlink**](a-mscom-partitionsetlink.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**MS-com-userlink**](a-mscom-userlink.md)                                                            | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**MS-DFSR-computerreferencebl**](a-msdfsr-computerreferencebl.md)                                    | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**MS-DFSR-mitgliedreferencebl**](a-msdfsr-memberreferencebl.md)                                        | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-allowed-to-act-on-Do-of-other-Identity**](a-msds-allowedtoactonbehalfofotheridentity.md) | False     | **Unternehmensperson**                                             |
| [**ms-DS-allowed-to-Delegat-an**](a-msds-allowedtodelegateto.md)                                     | False     | **Unternehmensperson**                                             |
| [**ms-DS-ca-immed-untergeordnete Elemente**](a-msds-approx-immed-subordinates.md)                            | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-authentieredto-accountlist**](a-msds-authenticatedtoaccountlist.md)                         | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Claim-Shares-mögliche-values-with-BL**](a-msds-claimsharespossiblevalueswithbl.md)           | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**MS-DS-Konsistenz-untergeordnet-Anzahl**](a-ms-ds-consistencychildcount.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                                              | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-aktiviert-Feature-BL**](a-msds-enabledfeaturebl.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-hab-Seniority-Index**](a-msds-habseniorityindex.md)                                          | False     | **Unternehmensperson**                                             |
| [**ms-DS-Host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-is-Domain-for**](a-msds-isdomainfor.md)                                                      | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-is-full-Replica-for**](a-msds-isfullreplicafor.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-is-Partial-Replica-for**](a-msds-ispartialreplicafor.md)                                     | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-is-Primary-Computer-für**](a-msds-isprimarycomputerfor.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-krbtgt-Link-BL**](a-msds-krbtgtlinkbl.md)                                                    | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                                                    | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-local-Effective-Lösch Zeit**](a-msds-localeffectivedeletiontime.md)                       | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-local-Effective-Papier-Time**](a-msds-localeffectiverecycletime.md)                         | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-gemastert von**](a-msds-masteredby.md)                                                         | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Members-für-AZ-Role-BL**](a-msds-membersforazrolebl.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Members-of-Resource-Property-List-BL**](a-msds-membersofresourcepropertylistbl.md)           | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-NC-repl-Cursor**](a-msds-ncreplcursors.md)                                                  | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-NC-repl-Inbound-Nachbarn**](a-msds-ncreplinboundneighbors.md)                               | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-NC-repl-Outbound-Nachbarn**](a-msds-ncreploutboundneighbors.md)                             | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)                          | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-NC-Typ**](a-msds-nctype.md)                                                                 | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                                                    | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-oidtoidgruppe-Link-BL**](a-msds-oidtogrouplinkbl.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)                                | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)                                | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Phonetic-Company-Name**](a-msds-phoneticcompanyname.md)                                      | False     | **Unternehmensperson**                                             |
| [**ms-DS-Phonetic-Department**](a-msds-phoneticdepartment.md)                                         | False     | **Unternehmensperson**                                             |
| [**ms-DS-Phonetic-Display-Name**](a-msds-phoneticdisplayname.md)                                      | False     | **Unternehmensperson**                                             |
| [**ms-DS-Phonetic-First-Name**](a-msds-phoneticfirstname.md)                                          | False     | **Unternehmensperson**                                             |
| [**ms-DS-Phonetic-Last-Name**](a-msds-phoneticlastname.md)                                            | False     | **Unternehmensperson**                                             |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                                                   | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-PSO-angewendet**](a-msds-psoapplied.md)                                                         | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-offengelegt-DSAs**](a-msds-revealeddsas.md)                                                     | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-enthüllt-List-BL**](a-msds-revealedlistbl.md)                                                | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Tasks-für-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Tasks-für-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-TDO-Egress-BL**](a-msds-tdoegressbl.md)                                                      | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-TDO-Ingress-BL**](a-msds-tdoingressbl.md)                                                    | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Value-Type-Reference-BL**](a-msds-valuetypereferencebl.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-Exch-House-Identifier**](a-msexchhouseidentifier.md)                                            | False     | **Unternehmensperson**                                             |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                                                  | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**msSFU-30-POSIX-Member-of**](a-mssfu30posixmemberof.md)                                             | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**NetBoot-SCP-BL**](a-netbootscpbl.md)                                                               | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Nicht sicherheitsmitglied-BL**](a-nonsecuritymemberbl.md)                                                | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                                               | Richtig      | [**Nach oben**](c-top.md)<br/>                                       |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                                           | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Objekt-Kategorie**](a-objectcategory.md)                                                            | Richtig      | [**Nach oben**](c-top.md)<br/>                                       |
| [**Object-Klasse**](a-objectclass.md)                                                                  | Richtig      | [**Nach oben**](c-top.md)<br/>                                       |
| [**Objekt-GUID**](a-objectguid.md)                                                                    | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Objekt-Version**](a-objectversion.md)                                                              | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Organisations Einheits Name**](a-ou.md)                                                               | False     | **Unternehmensperson**                                             |
| [**Name der Organisation**](a-o.md)                                                                       | False     | **Unternehmensperson**                                             |
| [**Sonstiges-Postfach**](a-othermailbox.md)                                                                | False     | **Unternehmensperson**                                             |
| [**Anderer Name**](a-middlename.md)                                                                     | False     | **Unternehmensperson**                                             |
| [**Andere-bekannte Objekte**](a-otherwellknownobjects.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Partial-Attribute-löschen-List**](a-partialattributedeletionlist.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Partiell-Attribut Satz**](a-partialattributeset.md)                                                 | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Persönliche Titel**](a-personaltitle.md)                                                              | False     | **Unternehmensperson**                                             |
| [**Telefon-Fax-Sonstiges**](a-otherfacsimiletelephonenumber.md)                                             | False     | **Unternehmensperson**                                             |
| [**Telefon-privat (Sonstiges)**](a-otherhomephone.md)                                                           | False     | **Unternehmensperson**                                             |
| [**Telefon-Home-primär**](a-homephone.md)                                                              | False     | **Unternehmensperson**                                             |
| [**Telefon-IP-Sonstiges**](a-otheripphone.md)                                                               | False     | **Unternehmensperson**                                             |
| [**Telefon-IP-primär**](a-ipphone.md)                                                                  | False     | **Unternehmensperson**                                             |
| [**Phone-ISDN-Primary**](a-primaryinternationalisdnnumber.md)                                         | False     | **Unternehmensperson**                                             |
| [**Phone-Mobile-other**](a-othermobile.md)                                                            | False     | **Unternehmensperson**                                             |
| [**Phone-Mobile-Primary**](a-mobile.md)                                                               | False     | **Unternehmensperson**                                             |
| [**Telefon-Office-Sonstiges**](a-othertelephone.md)                                                         | False     | **Unternehmensperson**                                             |
| [**Telefon-Pager-Sonstiges**](a-otherpager.md)                                                              | False     | **Unternehmensperson**                                             |
| [**Telefon-Pager-primär**](a-pager.md)                                                                 | False     | **Unternehmensperson**                                             |
| [**Physical-delivery-Office-Name**](a-physicaldeliveryofficename.md)                                  | False     | **Unternehmensperson**                                             |
| [**Picture**](a-thumbnailphoto.md)                                                                    | False     | **Unternehmensperson**                                             |
| [**Mögliche-minderwertig**](a-possibleinferiors.md)                                                      | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Postanschrift**](a-postaladdress.md)                                                              | False     | **Unternehmensperson**                                             |
| [**Postleitzahl**](a-postalcode.md)                                                                    | False     | **Unternehmensperson**                                             |
| [**Post-Office-Box**](a-postofficebox.md)                                                             | False     | **Unternehmensperson**                                             |
| [**Bevorzugte Übermittlungs Methode**](a-preferreddeliverymethod.md)                                         | False     | **Unternehmensperson**                                             |
| [**Proxy-Objekt Name**](a-proxiedobjectname.md)                                                     | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Proxy Adressen**](a-proxyaddresses.md)                                                            | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Abfrage-Richtlinie-BL**](a-querypolicybl.md)                                                             | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**RDN**](a-name.md)                                                                                  | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Registrierte Adresse**](a-registeredaddress.md)                                                      | False     | **Unternehmensperson**                                             |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                                              | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**REPL-Update-Vector**](a-repluptodatevector.md)                                                   | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Berichte**](a-directreports.md)                                                                     | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Reps-from**](a-repsfrom.md)                                                                        | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Reps-to**](a-repsto.md)                                                                            | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Novel**](a-revision.md)                                                                         | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**SD-Rechte**](a-sdrightseffective.md)                                                     | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Siehe auch**](a-seealso.md)                                                                          | False     | [**Person**](c-person.md)<br/>                                 |
| [**Seriennummer**](a-serialnumber.md)                                                                | False     | [**Person**](c-person.md)<br/>                                 |
| [**Server-Reference-BL**](a-serverreferencebl.md)                                                     | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Anzeigen-in-Advanced-nur anzeigen**](a-showinadvancedviewonly.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Site-Object-BL**](a-siteobjectbl.md)                                                               | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**State-or-Province-Name**](a-st.md)                                                                 | False     | **Unternehmensperson**                                             |
| [**Straße**](a-street.md)                                                                     | False     | **Unternehmensperson**                                             |
| [**Struktur-Objekt-Klasse**](a-structuralobjectclass.md)                                             | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Sub-Refs**](a-subrefs.md)                                                                          | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Subschemasubentry**](a-subschemasubentry.md)                                                       | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Nachname**](a-sn.md)                                                                                | False     | [**Person**](c-person.md)<br/>                                 |
| [**SystemFlags**](a-systemflags.md)                                                                  | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Telefonnummer**](a-telephonenumber.md)                                                          | False     | [**Person**](c-person.md)<br/>                                 |
| [**Teletex-Terminal-Identifier**](a-teletexterminalidentifier.md)                                     | False     | **Unternehmensperson**                                             |
| [**Telex-Nummer**](a-telexnumber.md)                                                                  | False     | **Unternehmensperson**                                             |
| [**Telex-primär**](a-primarytelexnumber.md)                                                          | False     | **Unternehmensperson**                                             |
| [**Text-Country**](a-co.md)                                                                           | False     | **Unternehmensperson**                                             |
| [**Titel**](a-title.md)                                                                               | False     | **Unternehmensperson**                                             |
| [**Benutzer Kommentar**](a-comment.md)                                                                      | False     | **Unternehmensperson**                                             |
| [**Benutzer Kennwort**](a-userpassword.md)                                                                | False     | [**Person**](c-person.md)<br/>                                 |
| [**Die Anwendung wurde geändert.**](a-usnchanged.md)                                                                    | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Von der Anwendung erstellte**](a-usncreated.md)                                                                    | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**USA-DSA-letzte-obj-entfernt**](a-usndsalastobjremoved.md)                                             | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Standort-und standortübergreifende standortübergreifende**](a-usnintersite.md)                                                                | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**"An-Last-obj-REM"**](a-usnlastobjrem.md)                                                            | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Quell Code Quelle**](a-usnsource.md)                                                                      | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**WBEM-Pfad**](a-wbempath.md)                                                                        | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Bekannte Objekte**](a-wellknownobjects.md)                                                       | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Bei Änderung**](a-whenchanged.md)                                                                  | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Bei Erstellung**](a-whencreated.md)                                                                  | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**WWW-Homepage**](a-wwwhomepage.md)                                                                 | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**WWW-Page-other**](a-url.md)                                                                        | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**X121-Adresse**](a-x121address.md)                                                                  | False     | **Unternehmensperson**                                             |



 

 





