---
title: Contact Klasse
description: Diese Klasse enthält Informationen über eine Person oder ein Unternehmen, die Sie in regelmäßigen Abständen kontaktieren müssen.
ms.assetid: 2372ea2b-1ac3-4173-950f-4ee00138fe22
ms.tgt_platform: multiple
keywords:
- AD-Schema der Kontakt Klasse
- AD-Schema der Kontakt Klasse
topic_type:
- apiref
api_name:
- Contact
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab728fbd87007f01076405730dcfee9f6d935a23
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104479858"
---
# <a name="contact-class"></a>Contact Klasse

Diese Klasse enthält Informationen über eine Person oder ein Unternehmen, die Sie in regelmäßigen Abständen kontaktieren müssen.



| Eingabe | Wert |
|-------------------|------------------------------------------------|
| CN                | Kontakt                                        |
| LDAP-Display-Name | contact                                        |
| Berechtigung aktualisieren  | Dieser Wert wird vom Domänen Administrator festgelegt. |
| Aktualisierungshäufigkeit  | \-                                             |
| Schema-ID-GUID    | 5cb41ed0-0e4c-11D0-a286-00aa003049e2           |



## <a name="implementations"></a>Implementierungen

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server

-   [Attribute](#windows-2000-server-attributes)
-   [Eigenschaftensätze](#windows-2000-server-property-sets)



| Eingabe | Wert |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | False                                                                                        |
| Object-Category             | 1                                                                                            |
| Default-Object-Category     | [**Person**](c-person.md)<br/>                                                        |
| Governs-Id                  | 1.2.840.113556.1.5.15                                                                        |
| Standard-ausblenden-Wert        | 0                                                                                            |
| RDN-ATT-ID                  | [**Gemeinsamer Name**](a-cn.md)<br/>                                                       |
| Unterklasse von                 | [**Unternehmensperson**](c-organizationalperson.md)<br/>                           |
| Mögliche Vorgesetzten          | [**Domänen-DNS**](c-domaindns.md)[**-Organisationseinheit**](c-organizationalunit.md)         |
| Zusätzlich           | E [**-Mail-Empfänger**](c-mailrecipient.md) (System)                                           |
| NT-Security-Descriptor      | o:Bag: schlecht: S:                                                                                 |
| Standard Sicherheits Beschreibung | D: (A;; rpwpcrccdclclorcwowdsddtsw;;;D a) (a;; Rpwpcrccdclclorcwowdsddtsw;;; SY) (A;; Rplclorc;;; Thaus |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-2000-server-attributes"></a>Windows 2000-Server Attribute

Diese Klasse enthält die folgenden Attribute für Windows 2000 Server:



| Attribut                                                                 | Obligatorisch. | Abgeleitet von                                                                                                                           |
|---------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**Weitere Informationen**](a-notes.md)                                 | False     | **Kontakt**                                                                                                                            |
| [**Adresse**](a-streetaddress.md)                                        | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Adresse-Startseite**](a-homepostaladdress.md)                               | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Administrator: Beschreibung**](a-admindescription.md)                           | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Administrator-Anzeige Name**](a-admindisplayname.md)                          | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Zulässige Attribute**](a-allowedattributes.md)                         | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Zulässige Attribute-gültig**](a-allowedattributeseffective.md)      | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Zulässige, untergeordnete Klassen**](a-allowedchildclasses.md)                    | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Zulässig-untergeordnete Klassen-gültig**](a-allowedchildclasseseffective.md) | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Geordneter**](a-assistant.md)                                          | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)             | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Kanonischer Name**](a-canonicalname.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Geäußert**](a-info.md)                                                 | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Gemeinsamer Name**](a-cn.md)                                               | Richtig      | **Kontakt** [ **Person**](c-person.md)<br/> [**E-Mail-Empfänger**](c-mailrecipient.md)<br/> [**Nach oben**](c-top.md)<br/> |
| [**Company**](a-company.md)                                              | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Länder Code**](a-countrycode.md)                                     | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Länder Name**](a-c.md)                                               | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Create-Zeitstempel**](a-createtimestamp.md)                            | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Klinik**](a-department.md)                                        | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Beschreibung**](a-description.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Ziel-Indikator**](a-destinationindicator.md)                   | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Anzeige Name**](a-displayname.md)                                     | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Anzeige Name-druckdruck**](a-displaynameprintable.md)                  | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Division**](a-division.md)                                            | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**DSA-Signatur**](a-dsasignature.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**DS-Core-propagierungs Daten**](a-dscorepropagationdata.md)               | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**E-Mail-Adressen**](a-mail.md)                                        | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Mitarbeiter-ID**](a-employeeid.md)                                       | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Erweiterungs Name**](a-extensionname.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Fax-Telefonnummer**](a-facsimiletelephonenumber.md)          | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Fahren**](a-flags.md)                                                  | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Aus-Eintrag**](a-fromentry.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)             | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                 | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**"F"-Rollen Besitzer**](a-fsmoroleowner.md)                                | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Garbage Koll-Zeitraum**](a-garbagecollperiod.md)                        | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Generierung-Qualifizierer**](a-generationqualifier.md)                     | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Vorname**](a-givenname.md)                                         | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Initialen**](a-initials.md)                                            | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Instanztyp**](a-instancetype.md)                                   | Richtig      | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**International-ISDN-Number**](a-internationalisdnnumber.md)            | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Is-critical-System-Object**](a-iscriticalsystemobject.md)             | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Ist-gelöscht**](a-isdeleted.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Is-Member-of-DL**](a-memberof.md)                                     | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Is-Privilege-Inhaber**](a-isprivilegeholder.md)                        | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Letztes-bekannt/übergeordnetes Element**](a-lastknownparent.md)                            | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Legacy-Exchange-DN**](a-legacyexchangedn.md)                          | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Lokalitäts Name**](a-l.md)                                              | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Logo**](a-thumbnaillogo.md)                                           | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Verwaltete Objekte**](a-managedobjects.md)                               | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Dienst**](a-manager.md)                                              | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Verwaltet von**](a-masteredby.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**MHS-or-address**](a-mhsoraddress.md)                                  | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Modify-Zeitstempel**](a-modifytimestamp.md)                            | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Konsistenz-untergeordnet-Anzahl**](a-ms-ds-consistencychildcount.md)    | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                 | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**NetBoot-SCP-BL**](a-netbootscpbl.md)                                  | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Nicht sicherheitsmitglied-BL**](a-nonsecuritymemberbl.md)                   | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                  | Richtig      | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Obj-Dist-Name**](a-distinguishedname.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Objekt-Kategorie**](a-objectcategory.md)                               | Richtig      | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Object-Klasse**](a-objectclass.md)                                     | Richtig      | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Objekt-GUID**](a-objectguid.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Objekt-Version**](a-objectversion.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Organisations Einheits Name**](a-ou.md)                                  | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Name der Organisation**](a-o.md)                                          | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Sonstiges-Postfach**](a-othermailbox.md)                                   | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Anderer Name**](a-middlename.md)                                        | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Andere-bekannte Objekte**](a-otherwellknownobjects.md)               | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Partial-Attribute-löschen-List**](a-partialattributedeletionlist.md) | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Partiell-Attribut Satz**](a-partialattributeset.md)                    | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Persönliche Titel**](a-personaltitle.md)                                 | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-Fax-Sonstiges**](a-otherfacsimiletelephonenumber.md)                | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-privat (Sonstiges)**](a-otherhomephone.md)                              | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-Home-primär**](a-homephone.md)                                 | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-IP-Sonstiges**](a-otheripphone.md)                                  | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-IP-primär**](a-ipphone.md)                                     | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Phone-ISDN-Primary**](a-primaryinternationalisdnnumber.md)            | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Phone-Mobile-other**](a-othermobile.md)                               | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Phone-Mobile-Primary**](a-mobile.md)                                  | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-Office-Sonstiges**](a-othertelephone.md)                            | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-Pager-Sonstiges**](a-otherpager.md)                                 | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-Pager-primär**](a-pager.md)                                    | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Physical-delivery-Office-Name**](a-physicaldeliveryofficename.md)     | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Picture**](a-thumbnailphoto.md)                                       | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Mögliche-minderwertig**](a-possibleinferiors.md)                         | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Postanschrift**](a-postaladdress.md)                                 | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Postleitzahl**](a-postalcode.md)                                       | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Post-Office-Box**](a-postofficebox.md)                                | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Bevorzugte Übermittlungs Methode**](a-preferreddeliverymethod.md)            | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Proxy-Objekt Name**](a-proxiedobjectname.md)                        | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Proxy Adressen**](a-proxyaddresses.md)                               | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Abfrage-Richtlinie-BL**](a-querypolicybl.md)                                | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**RDN**](a-name.md)                                                     | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Registrierte Adresse**](a-registeredaddress.md)                         | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                 | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**REPL-Update-Vector**](a-repluptodatevector.md)                      | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Berichte**](a-directreports.md)                                        | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Reps-from**](a-repsfrom.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Reps-to**](a-repsto.md)                                               | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Novel**](a-revision.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**SD-Rechte**](a-sdrightseffective.md)                        | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Siehe auch**](a-seealso.md)                                             | False     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**Server-Reference-BL**](a-serverreferencebl.md)                        | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**In-Address-Book anzeigen**](a-showinaddressbook.md)                       | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Anzeigen-in-Advanced-nur anzeigen**](a-showinadvancedviewonly.md)            | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Site-Object-BL**](a-siteobjectbl.md)                                  | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**State-or-Province-Name**](a-st.md)                                    | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Straße**](a-street.md)                                        | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Sub-Refs**](a-subrefs.md)                                             | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Subschemasubentry**](a-subschemasubentry.md)                          | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Nachname**](a-sn.md)                                                   | False     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**SystemFlags**](a-systemflags.md)                                     | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Telefonnummer**](a-telephonenumber.md)                             | False     | [**Person**](c-person.md)<br/> [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                             |
| [**Teletex-Terminal-Identifier**](a-teletexterminalidentifier.md)        | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telex-Nummer**](a-telexnumber.md)                                     | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telex-primär**](a-primarytelexnumber.md)                             | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Text-Country**](a-co.md)                                              | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Text-codiert-or-address**](a-textencodedoraddress.md)                 | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Titel**](a-title.md)                                                  | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Benutzerzertifikat**](a-usercert.md)                                           | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Benutzer Kommentar**](a-comment.md)                                         | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Benutzer Kennwort**](a-userpassword.md)                                   | False     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**Benutzersmime-Zertifikat**](a-usersmimecertificate.md)                  | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Die Anwendung wurde geändert.**](a-usnchanged.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Von der Anwendung erstellte**](a-usncreated.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**USA-DSA-letzte-obj-entfernt**](a-usndsalastobjremoved.md)                | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Standort-und standortübergreifende standortübergreifende**](a-usnintersite.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**"An-Last-obj-REM"**](a-usnlastobjrem.md)                               | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Quell Code Quelle**](a-usnsource.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**WBEM-Pfad**](a-wbempath.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Bekannte Objekte**](a-wellknownobjects.md)                          | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Bei Änderung**](a-whenchanged.md)                                     | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Bei Erstellung**](a-whencreated.md)                                     | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**WWW-Homepage**](a-wwwhomepage.md)                                    | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**WWW-Page-other**](a-url.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**X121-Adresse**](a-x121address.md)                                     | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**X509-CERT**](a-usercertificate.md)                                    | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |



## <a name="windows-2000-server-property-sets"></a>Eigenschaften Sätze für Windows 2000-Server

Diese Klasse enthält die folgenden Eigenschaften Sätze für Windows 2000 Server:



| Allgemeiner Name                                            |
|--------------------------------------------------------|
| [**Persönliche Informationen**](r-personal-information.md) |
| [**Webinformationen**](r-web-information.md)           |



## <a name="windows-server-2003"></a>Windows Server 2003

-   [Attribute](#windows-server-2003-attributes)
-   [Eigenschaftensätze](#windows-server-2003-property-sets)



| Eingabe | Wert |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | False                                                                                        |
| Object-Category             | 1                                                                                            |
| Default-Object-Category     | [**Person**](c-person.md)<br/>                                                        |
| Governs-Id                  | 1.2.840.113556.1.5.15                                                                        |
| Standard-ausblenden-Wert        | 0                                                                                            |
| RDN-ATT-ID                  | [**Gemeinsamer Name**](a-cn.md)<br/>                                                       |
| Unterklasse von                 | [**Unternehmensperson**](c-organizationalperson.md)<br/>                           |
| Mögliche Vorgesetzten          | [**Domänen-DNS**](c-domaindns.md)[**-Organisationseinheit**](c-organizationalunit.md)         |
| Zusätzlich           | E [**-Mail-Empfänger**](c-mailrecipient.md) (System)                                           |
| NT-Security-Descriptor      | o:Bag: schlecht: S:                                                                                 |
| Standard Sicherheits Beschreibung | D: (A;; rpwpcrccdclclorcwowdsddtsw;;;D a) (a;; Rpwpcrccdclclorcwowdsddtsw;;; SY) (A;; Rplclorc;;; Thaus |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2003-attributes"></a>Windows Server 2003-Attribute

Diese Klasse enthält die folgenden Attribute für Windows Server 2003:



| Attribut                                                                   | Obligatorisch. | Abgeleitet von                                                                                                                           |
|-----------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**Weitere Informationen**](a-notes.md)                                   | False     | **Kontakt**                                                                                                                            |
| [**Adresse**](a-streetaddress.md)                                          | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Adresse-Startseite**](a-homepostaladdress.md)                                 | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Administrator: Beschreibung**](a-admindescription.md)                             | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Administrator-Anzeige Name**](a-admindisplayname.md)                            | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Zulässige Attribute**](a-allowedattributes.md)                           | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Zulässige Attribute-gültig**](a-allowedattributeseffective.md)        | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Zulässige, untergeordnete Klassen**](a-allowedchildclasses.md)                      | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Zulässig-untergeordnete Klassen-gültig**](a-allowedchildclasseseffective.md)   | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Geordneter**](a-assistant.md)                                            | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**attributecertificateattribute**](a-attributecertificateattribute.md)    | False     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)               | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Kanonischer Name**](a-canonicalname.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Geäußert**](a-info.md)                                                   | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Gemeinsamer Name**](a-cn.md)                                                 | Richtig      | **Kontakt** [ **Person**](c-person.md)<br/> [**E-Mail-Empfänger**](c-mailrecipient.md)<br/> [**Nach oben**](c-top.md)<br/> |
| [**Company**](a-company.md)                                                | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Länder Code**](a-countrycode.md)                                       | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Länder Name**](a-c.md)                                                 | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Create-Zeitstempel**](a-createtimestamp.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Klinik**](a-department.md)                                          | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Beschreibung**](a-description.md)                                        | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Ziel-Indikator**](a-destinationindicator.md)                     | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Anzeige Name**](a-displayname.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Anzeige Name-druckdruck**](a-displaynameprintable.md)                    | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Division**](a-division.md)                                              | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**DSA-Signatur**](a-dsasignature.md)                                     | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**DS-Core-propagierungs Daten**](a-dscorepropagationdata.md)                 | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**E-Mail-Adressen**](a-mail.md)                                          | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Mitarbeiter-ID**](a-employeeid.md)                                         | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Erweiterungs Name**](a-extensionname.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Fax-Telefonnummer**](a-facsimiletelephonenumber.md)            | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Fahren**](a-flags.md)                                                    | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Aus-Eintrag**](a-fromentry.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)               | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                   | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**"F"-Rollen Besitzer**](a-fsmoroleowner.md)                                  | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Garbage Koll-Zeitraum**](a-garbagecollperiod.md)                          | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Generierung-Qualifizierer**](a-generationqualifier.md)                       | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Vorname**](a-givenname.md)                                           | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**HouseIdentifier**](a-houseidentifier.md)                                | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Initialen**](a-initials.md)                                              | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Instanztyp**](a-instancetype.md)                                     | Richtig      | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**International-ISDN-Number**](a-internationalisdnnumber.md)              | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Is-critical-System-Object**](a-iscriticalsystemobject.md)               | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Ist-gelöscht**](a-isdeleted.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Is-Member-of-DL**](a-memberof.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Is-Privilege-Inhaber**](a-isprivilegeholder.md)                          | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**LabeledURI**](a-labeleduri.md)                                          | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Letztes-bekannt/übergeordnetes Element**](a-lastknownparent.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Legacy-Exchange-DN**](a-legacyexchangedn.md)                            | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Lokalitäts Name**](a-l.md)                                                | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Logo**](a-thumbnaillogo.md)                                             | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Verwaltete Objekte**](a-managedobjects.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Dienst**](a-manager.md)                                                | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Verwaltet von**](a-masteredby.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**MHS-or-address**](a-mhsoraddress.md)                                    | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Modify-Zeitstempel**](a-modifytimestamp.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**MS-com-partitionsetlink**](a-mscom-partitionsetlink.md)                 | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**MS-com-userlink**](a-mscom-userlink.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-allowed-to-Delegat-an**](a-msds-allowedtodelegateto.md)          | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-ca-immed-untergeordnete Elemente**](a-msds-approx-immed-subordinates.md) | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Konsistenz-untergeordnet-Anzahl**](a-ms-ds-consistencychildcount.md)      | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-gemastert von**](a-msds-masteredby.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Members-für-AZ-Role-BL**](a-msds-membersforazrolebl.md)           | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-NC-repl-Cursor**](a-msds-ncreplcursors.md)                       | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-NC-repl-Inbound-Nachbarn**](a-msds-ncreplinboundneighbors.md)    | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-NC-repl-Outbound-Nachbarn**](a-msds-ncreploutboundneighbors.md)  | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                         | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)               | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)     | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)     | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)      | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)              | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Tasks-für-AZ-Role-BL**](a-msds-tasksforazrolebl.md)               | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Tasks-für-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)               | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-Exch-Assistant-Name**](a-msexchassistantname.md)                     | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**ms-Exch-House-Identifier**](a-msexchhouseidentifier.md)                 | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-Exch-LabeledURI**](a-msexchlabeleduri.md)                            | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**NetBoot-SCP-BL**](a-netbootscpbl.md)                                    | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Nicht sicherheitsmitglied-BL**](a-nonsecuritymemberbl.md)                     | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                    | Richtig      | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Objekt-Kategorie**](a-objectcategory.md)                                 | Richtig      | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Object-Klasse**](a-objectclass.md)                                       | Richtig      | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Objekt-GUID**](a-objectguid.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Objekt-Version**](a-objectversion.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Organisations Einheits Name**](a-ou.md)                                    | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Name der Organisation**](a-o.md)                                            | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Sonstiges-Postfach**](a-othermailbox.md)                                     | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Anderer Name**](a-middlename.md)                                          | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Andere-bekannte Objekte**](a-otherwellknownobjects.md)                 | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Partial-Attribute-löschen-List**](a-partialattributedeletionlist.md)   | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Partiell-Attribut Satz**](a-partialattributeset.md)                      | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Persönliche Titel**](a-personaltitle.md)                                   | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-Fax-Sonstiges**](a-otherfacsimiletelephonenumber.md)                  | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-privat (Sonstiges)**](a-otherhomephone.md)                                | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-Home-primär**](a-homephone.md)                                   | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-IP-Sonstiges**](a-otheripphone.md)                                    | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-IP-primär**](a-ipphone.md)                                       | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Phone-ISDN-Primary**](a-primaryinternationalisdnnumber.md)              | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Phone-Mobile-other**](a-othermobile.md)                                 | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Phone-Mobile-Primary**](a-mobile.md)                                    | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-Office-Sonstiges**](a-othertelephone.md)                              | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-Pager-Sonstiges**](a-otherpager.md)                                   | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-Pager-primär**](a-pager.md)                                      | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Physical-delivery-Office-Name**](a-physicaldeliveryofficename.md)       | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Picture**](a-thumbnailphoto.md)                                         | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Mögliche-minderwertig**](a-possibleinferiors.md)                           | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Postanschrift**](a-postaladdress.md)                                   | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Postleitzahl**](a-postalcode.md)                                         | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Post-Office-Box**](a-postofficebox.md)                                  | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Bevorzugte Übermittlungs Methode**](a-preferreddeliverymethod.md)              | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Proxy-Objekt Name**](a-proxiedobjectname.md)                          | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Proxy Adressen**](a-proxyaddresses.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Abfrage-Richtlinie-BL**](a-querypolicybl.md)                                  | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**RDN**](a-name.md)                                                       | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Registrierte Adresse**](a-registeredaddress.md)                           | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                   | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**REPL-Update-Vector**](a-repluptodatevector.md)                        | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Berichte**](a-directreports.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Reps-from**](a-repsfrom.md)                                             | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Reps-to**](a-repsto.md)                                                 | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Novel**](a-revision.md)                                              | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**SD-Rechte**](a-sdrightseffective.md)                          | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**secretary**](a-secretary.md)                                            | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Siehe auch**](a-seealso.md)                                               | False     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**Seriennummer**](a-serialnumber.md)                                     | False     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**Server-Reference-BL**](a-serverreferencebl.md)                          | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**In-Address-Book anzeigen**](a-showinaddressbook.md)                         | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Anzeigen-in-Advanced-nur anzeigen**](a-showinadvancedviewonly.md)              | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**State-or-Province-Name**](a-st.md)                                      | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Straße**](a-street.md)                                          | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Struktur-Objekt-Klasse**](a-structuralobjectclass.md)                  | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Sub-Refs**](a-subrefs.md)                                               | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Subschemasubentry**](a-subschemasubentry.md)                            | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Nachname**](a-sn.md)                                                     | False     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**SystemFlags**](a-systemflags.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Telefonnummer**](a-telephonenumber.md)                               | False     | [**Person**](c-person.md)<br/> [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                             |
| [**Teletex-Terminal-Identifier**](a-teletexterminalidentifier.md)          | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telex-Nummer**](a-telexnumber.md)                                       | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telex-primär**](a-primarytelexnumber.md)                               | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Text-Country**](a-co.md)                                                | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Text-codiert-or-address**](a-textencodedoraddress.md)                   | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Titel**](a-title.md)                                                    | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Benutzerzertifikat**](a-usercert.md)                                             | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Benutzer Kommentar**](a-comment.md)                                           | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Benutzer Kennwort**](a-userpassword.md)                                     | False     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**Benutzersmime-Zertifikat**](a-usersmimecertificate.md)                    | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Die Anwendung wurde geändert.**](a-usnchanged.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Von der Anwendung erstellte**](a-usncreated.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**USA-DSA-letzte-obj-entfernt**](a-usndsalastobjremoved.md)                  | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Standort-und standortübergreifende standortübergreifende**](a-usnintersite.md)                                     | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**"An-Last-obj-REM"**](a-usnlastobjrem.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Quell Code Quelle**](a-usnsource.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**WBEM-Pfad**](a-wbempath.md)                                             | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Bekannte Objekte**](a-wellknownobjects.md)                            | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Bei Änderung**](a-whenchanged.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Bei Erstellung**](a-whencreated.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**WWW-Homepage**](a-wwwhomepage.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**WWW-Page-other**](a-url.md)                                             | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**X121-Adresse**](a-x121address.md)                                       | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**X509-CERT**](a-usercertificate.md)                                      | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |



## <a name="windows-server-2003-property-sets"></a>Windows Server 2003-Eigenschaften Sätze

Diese Klasse enthält die folgenden Eigenschaften Sätze für Windows Server 2003:



| Allgemeiner Name                                            |
|--------------------------------------------------------|
| [**Persönliche Informationen**](r-personal-information.md) |
| [**Webinformationen**](r-web-information.md)           |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2

-   [Attribute](#windows-server-2003-r2-attributes)
-   [Eigenschaftensätze](#windows-server-2003-r2-property-sets)



| Eingabe | Wert |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | False                                                                                        |
| Object-Category             | 1                                                                                            |
| Default-Object-Category     | [**Person**](c-person.md)<br/>                                                        |
| Governs-Id                  | 1.2.840.113556.1.5.15                                                                        |
| Standard-ausblenden-Wert        | 0                                                                                            |
| RDN-ATT-ID                  | [**Gemeinsamer Name**](a-cn.md)<br/>                                                       |
| Unterklasse von                 | [**Unternehmensperson**](c-organizationalperson.md)<br/>                           |
| Mögliche Vorgesetzten          | [**Domänen-DNS**](c-domaindns.md)[**-Organisationseinheit**](c-organizationalunit.md)         |
| Zusätzlich           | E [**-Mail-Empfänger**](c-mailrecipient.md) (System)                                           |
| NT-Security-Descriptor      | o:Bag: schlecht: S:                                                                                 |
| Standard Sicherheits Beschreibung | D: (A;; rpwpcrccdclclorcwowdsddtsw;;;D a) (a;; Rpwpcrccdclclorcwowdsddtsw;;; SY) (A;; Rplclorc;;; Thaus |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2003-r2-attributes"></a>Windows Server 2003 R2-Attribute

Diese Klasse enthält die folgenden Attribute für Windows Server 2003 R2:



| Attribut                                                                   | Obligatorisch. | Abgeleitet von                                                                                                                           |
|-----------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**Weitere Informationen**](a-notes.md)                                   | False     | **Kontakt**                                                                                                                            |
| [**Adresse**](a-streetaddress.md)                                          | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Adresse-Startseite**](a-homepostaladdress.md)                                 | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Administrator: Beschreibung**](a-admindescription.md)                             | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Administrator-Anzeige Name**](a-admindisplayname.md)                            | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Zulässige Attribute**](a-allowedattributes.md)                           | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Zulässige Attribute-gültig**](a-allowedattributeseffective.md)        | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Zulässige, untergeordnete Klassen**](a-allowedchildclasses.md)                      | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Zulässig-untergeordnete Klassen-gültig**](a-allowedchildclasseseffective.md)   | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Geordneter**](a-assistant.md)                                            | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**attributecertificateattribute**](a-attributecertificateattribute.md)    | False     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)               | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Kanonischer Name**](a-canonicalname.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Geäußert**](a-info.md)                                                   | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Gemeinsamer Name**](a-cn.md)                                                 | Richtig      | **Kontakt** [ **Person**](c-person.md)<br/> [**E-Mail-Empfänger**](c-mailrecipient.md)<br/> [**Nach oben**](c-top.md)<br/> |
| [**Company**](a-company.md)                                                | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Länder Code**](a-countrycode.md)                                       | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Länder Name**](a-c.md)                                                 | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Create-Zeitstempel**](a-createtimestamp.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Klinik**](a-department.md)                                          | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Beschreibung**](a-description.md)                                        | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Ziel-Indikator**](a-destinationindicator.md)                     | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Anzeige Name**](a-displayname.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Anzeige Name-druckdruck**](a-displaynameprintable.md)                    | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Division**](a-division.md)                                              | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**DSA-Signatur**](a-dsasignature.md)                                     | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**DS-Core-propagierungs Daten**](a-dscorepropagationdata.md)                 | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**E-Mail-Adressen**](a-mail.md)                                          | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Mitarbeiter-ID**](a-employeeid.md)                                         | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Erweiterungs Name**](a-extensionname.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Fax-Telefonnummer**](a-facsimiletelephonenumber.md)            | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Fahren**](a-flags.md)                                                    | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Aus-Eintrag**](a-fromentry.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)               | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                   | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**"F"-Rollen Besitzer**](a-fsmoroleowner.md)                                  | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Garbage Koll-Zeitraum**](a-garbagecollperiod.md)                          | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Generierung-Qualifizierer**](a-generationqualifier.md)                       | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Vorname**](a-givenname.md)                                           | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**HouseIdentifier**](a-houseidentifier.md)                                | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Initialen**](a-initials.md)                                              | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Instanztyp**](a-instancetype.md)                                     | Richtig      | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**International-ISDN-Number**](a-internationalisdnnumber.md)              | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Is-critical-System-Object**](a-iscriticalsystemobject.md)               | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Ist-gelöscht**](a-isdeleted.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Is-Member-of-DL**](a-memberof.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Is-Privilege-Inhaber**](a-isprivilegeholder.md)                          | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**LabeledURI**](a-labeleduri.md)                                          | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Letztes-bekannt/übergeordnetes Element**](a-lastknownparent.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Legacy-Exchange-DN**](a-legacyexchangedn.md)                            | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Lokalitäts Name**](a-l.md)                                                | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Logo**](a-thumbnaillogo.md)                                             | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Verwaltete Objekte**](a-managedobjects.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Dienst**](a-manager.md)                                                | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Verwaltet von**](a-masteredby.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**MHS-or-address**](a-mhsoraddress.md)                                    | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Modify-Zeitstempel**](a-modifytimestamp.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**MS-com-partitionsetlink**](a-mscom-partitionsetlink.md)                 | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**MS-com-userlink**](a-mscom-userlink.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**MS-DFSR-computerreferencebl**](a-msdfsr-computerreferencebl.md)         | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**MS-DFSR-mitgliedreferencebl**](a-msdfsr-memberreferencebl.md)             | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-allowed-to-Delegat-an**](a-msds-allowedtodelegateto.md)          | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-ca-immed-untergeordnete Elemente**](a-msds-approx-immed-subordinates.md) | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Konsistenz-untergeordnet-Anzahl**](a-ms-ds-consistencychildcount.md)      | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-gemastert von**](a-msds-masteredby.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Members-für-AZ-Role-BL**](a-msds-membersforazrolebl.md)           | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-NC-repl-Cursor**](a-msds-ncreplcursors.md)                       | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-NC-repl-Inbound-Nachbarn**](a-msds-ncreplinboundneighbors.md)    | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-NC-repl-Outbound-Nachbarn**](a-msds-ncreploutboundneighbors.md)  | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                         | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)               | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)     | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)     | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)      | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)              | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Source-Object-DN**](a-msds-sourceobjectdn.md)                     | False     | **Kontakt**                                                                                                                            |
| [**ms-DS-Tasks-für-AZ-Role-BL**](a-msds-tasksforazrolebl.md)               | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Tasks-für-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)               | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-Exch-Assistant-Name**](a-msexchassistantname.md)                     | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**ms-Exch-House-Identifier**](a-msexchhouseidentifier.md)                 | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-Exch-LabeledURI**](a-msexchlabeleduri.md)                            | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**msSFU-30-POSIX-Member-of**](a-mssfu30posixmemberof.md)                  | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**NetBoot-SCP-BL**](a-netbootscpbl.md)                                    | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Nicht sicherheitsmitglied-BL**](a-nonsecuritymemberbl.md)                     | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                    | Richtig      | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Objekt-Kategorie**](a-objectcategory.md)                                 | Richtig      | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Object-Klasse**](a-objectclass.md)                                       | Richtig      | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Objekt-GUID**](a-objectguid.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Objekt-Version**](a-objectversion.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Organisations Einheits Name**](a-ou.md)                                    | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Name der Organisation**](a-o.md)                                            | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Sonstiges-Postfach**](a-othermailbox.md)                                     | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Anderer Name**](a-middlename.md)                                          | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Andere-bekannte Objekte**](a-otherwellknownobjects.md)                 | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Partial-Attribute-löschen-List**](a-partialattributedeletionlist.md)   | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Partiell-Attribut Satz**](a-partialattributeset.md)                      | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Persönliche Titel**](a-personaltitle.md)                                   | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-Fax-Sonstiges**](a-otherfacsimiletelephonenumber.md)                  | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-privat (Sonstiges)**](a-otherhomephone.md)                                | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-Home-primär**](a-homephone.md)                                   | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-IP-Sonstiges**](a-otheripphone.md)                                    | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-IP-primär**](a-ipphone.md)                                       | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Phone-ISDN-Primary**](a-primaryinternationalisdnnumber.md)              | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Phone-Mobile-other**](a-othermobile.md)                                 | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Phone-Mobile-Primary**](a-mobile.md)                                    | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-Office-Sonstiges**](a-othertelephone.md)                              | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-Pager-Sonstiges**](a-otherpager.md)                                   | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-Pager-primär**](a-pager.md)                                      | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Physical-delivery-Office-Name**](a-physicaldeliveryofficename.md)       | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Picture**](a-thumbnailphoto.md)                                         | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Mögliche-minderwertig**](a-possibleinferiors.md)                           | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Postanschrift**](a-postaladdress.md)                                   | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Postleitzahl**](a-postalcode.md)                                         | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Post-Office-Box**](a-postofficebox.md)                                  | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Bevorzugte Übermittlungs Methode**](a-preferreddeliverymethod.md)              | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Proxy-Objekt Name**](a-proxiedobjectname.md)                          | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Proxy Adressen**](a-proxyaddresses.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Abfrage-Richtlinie-BL**](a-querypolicybl.md)                                  | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**RDN**](a-name.md)                                                       | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Registrierte Adresse**](a-registeredaddress.md)                           | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                   | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**REPL-Update-Vector**](a-repluptodatevector.md)                        | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Berichte**](a-directreports.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Reps-from**](a-repsfrom.md)                                             | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Reps-to**](a-repsto.md)                                                 | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Novel**](a-revision.md)                                              | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**SD-Rechte**](a-sdrightseffective.md)                          | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**secretary**](a-secretary.md)                                            | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Siehe auch**](a-seealso.md)                                               | False     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**Seriennummer**](a-serialnumber.md)                                     | False     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**Server-Reference-BL**](a-serverreferencebl.md)                          | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**In-Address-Book anzeigen**](a-showinaddressbook.md)                         | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Anzeigen-in-Advanced-nur anzeigen**](a-showinadvancedviewonly.md)              | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**State-or-Province-Name**](a-st.md)                                      | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Straße**](a-street.md)                                          | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Struktur-Objekt-Klasse**](a-structuralobjectclass.md)                  | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Sub-Refs**](a-subrefs.md)                                               | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Subschemasubentry**](a-subschemasubentry.md)                            | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Nachname**](a-sn.md)                                                     | False     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**SystemFlags**](a-systemflags.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Telefonnummer**](a-telephonenumber.md)                               | False     | [**Person**](c-person.md)<br/> [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                             |
| [**Teletex-Terminal-Identifier**](a-teletexterminalidentifier.md)          | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telex-Nummer**](a-telexnumber.md)                                       | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telex-primär**](a-primarytelexnumber.md)                               | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Text-Country**](a-co.md)                                                | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Text-codiert-or-address**](a-textencodedoraddress.md)                   | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Titel**](a-title.md)                                                    | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Benutzerzertifikat**](a-usercert.md)                                             | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Benutzer Kommentar**](a-comment.md)                                           | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Benutzer Kennwort**](a-userpassword.md)                                     | False     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**Benutzersmime-Zertifikat**](a-usersmimecertificate.md)                    | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Die Anwendung wurde geändert.**](a-usnchanged.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Von der Anwendung erstellte**](a-usncreated.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**USA-DSA-letzte-obj-entfernt**](a-usndsalastobjremoved.md)                  | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Standort-und standortübergreifende standortübergreifende**](a-usnintersite.md)                                     | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**"An-Last-obj-REM"**](a-usnlastobjrem.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Quell Code Quelle**](a-usnsource.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**WBEM-Pfad**](a-wbempath.md)                                             | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Bekannte Objekte**](a-wellknownobjects.md)                            | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Bei Änderung**](a-whenchanged.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Bei Erstellung**](a-whencreated.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**WWW-Homepage**](a-wwwhomepage.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**WWW-Page-other**](a-url.md)                                             | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**X121-Adresse**](a-x121address.md)                                       | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**X509-CERT**](a-usercertificate.md)                                      | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |



## <a name="windows-server-2003-r2-property-sets"></a>Windows Server 2003 R2-Eigenschaften Sätze

Diese Klasse enthält die folgenden Eigenschaften Sätze für Windows Server 2003 R2:



| Allgemeiner Name                                            |
|--------------------------------------------------------|
| [**Persönliche Informationen**](r-personal-information.md) |
| [**Webinformationen**](r-web-information.md)           |



## <a name="windows-server-2008"></a>Windows Server 2008

-   [Attribute](#windows-server-2008-attributes)
-   [Eigenschaftensätze](#windows-server-2008-property-sets)



| Eingabe | Wert |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | False                                                                                        |
| Object-Category             | 1                                                                                            |
| Default-Object-Category     | [**Person**](c-person.md)<br/>                                                        |
| Governs-Id                  | 1.2.840.113556.1.5.15                                                                        |
| Standard-ausblenden-Wert        | 0                                                                                            |
| RDN-ATT-ID                  | [**Gemeinsamer Name**](a-cn.md)<br/>                                                       |
| Unterklasse von                 | [**Unternehmensperson**](c-organizationalperson.md)<br/>                           |
| Mögliche Vorgesetzten          | [**Domänen-DNS**](c-domaindns.md)[**-Organisationseinheit**](c-organizationalunit.md)         |
| Zusätzlich           | E [**-Mail-Empfänger**](c-mailrecipient.md) (System)                                           |
| NT-Security-Descriptor      | o:Bag: schlecht: S:                                                                                 |
| Standard Sicherheits Beschreibung | D: (A;; rpwpcrccdclclorcwowdsddtsw;;;D a) (a;; Rpwpcrccdclclorcwowdsddtsw;;; SY) (A;; Rplclorc;;; Thaus |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2008-attributes"></a>Windows Server 2008-Attribute

Diese Klasse enthält die folgenden Attribute für Windows Server 2008:



| Attribut                                                                      | Obligatorisch. | Abgeleitet von                                                                                                                           |
|--------------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**Weitere Informationen**](a-notes.md)                                      | False     | **Kontakt**                                                                                                                            |
| [**Adresse**](a-streetaddress.md)                                             | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Adresse-Startseite**](a-homepostaladdress.md)                                    | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Administrator: Beschreibung**](a-admindescription.md)                                | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Administrator-Anzeige Name**](a-admindisplayname.md)                               | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Zulässige Attribute**](a-allowedattributes.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Zulässige Attribute-gültig**](a-allowedattributeseffective.md)           | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Zulässige, untergeordnete Klassen**](a-allowedchildclasses.md)                         | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Zulässig-untergeordnete Klassen-gültig**](a-allowedchildclasseseffective.md)      | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Geordneter**](a-assistant.md)                                               | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**attributecertificateattribute**](a-attributecertificateattribute.md)       | False     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                  | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Kanonischer Name**](a-canonicalname.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Geäußert**](a-info.md)                                                      | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Gemeinsamer Name**](a-cn.md)                                                    | Richtig      | **Kontakt** [ **Person**](c-person.md)<br/> [**E-Mail-Empfänger**](c-mailrecipient.md)<br/> [**Nach oben**](c-top.md)<br/> |
| [**Company**](a-company.md)                                                   | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Länder Code**](a-countrycode.md)                                          | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Länder Name**](a-c.md)                                                    | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Create-Zeitstempel**](a-createtimestamp.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Klinik**](a-department.md)                                             | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Beschreibung**](a-description.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Ziel-Indikator**](a-destinationindicator.md)                        | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Anzeige Name**](a-displayname.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Anzeige Name-druckdruck**](a-displaynameprintable.md)                       | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Division**](a-division.md)                                                 | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**DSA-Signatur**](a-dsasignature.md)                                        | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**DS-Core-propagierungs Daten**](a-dscorepropagationdata.md)                    | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**E-Mail-Adressen**](a-mail.md)                                             | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Mitarbeiter-ID**](a-employeeid.md)                                            | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Erweiterungs Name**](a-extensionname.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Fax-Telefonnummer**](a-facsimiletelephonenumber.md)               | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Fahren**](a-flags.md)                                                       | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Aus-Eintrag**](a-fromentry.md)                                              | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                  | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                      | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**"F"-Rollen Besitzer**](a-fsmoroleowner.md)                                     | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Garbage Koll-Zeitraum**](a-garbagecollperiod.md)                             | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Generierung-Qualifizierer**](a-generationqualifier.md)                          | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Vorname**](a-givenname.md)                                              | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**HouseIdentifier**](a-houseidentifier.md)                                   | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Initialen**](a-initials.md)                                                 | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Instanztyp**](a-instancetype.md)                                        | Richtig      | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**International-ISDN-Number**](a-internationalisdnnumber.md)                 | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Is-critical-System-Object**](a-iscriticalsystemobject.md)                  | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Ist-gelöscht**](a-isdeleted.md)                                              | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Is-Member-of-DL**](a-memberof.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Is-Privilege-Inhaber**](a-isprivilegeholder.md)                             | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**LabeledURI**](a-labeleduri.md)                                             | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Letztes-bekannt/übergeordnetes Element**](a-lastknownparent.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Legacy-Exchange-DN**](a-legacyexchangedn.md)                               | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Lokalitäts Name**](a-l.md)                                                   | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Logo**](a-thumbnaillogo.md)                                                | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Verwaltete Objekte**](a-managedobjects.md)                                    | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Dienst**](a-manager.md)                                                   | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Verwaltet von**](a-masteredby.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**MHS-or-address**](a-mhsoraddress.md)                                       | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Modify-Zeitstempel**](a-modifytimestamp.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**MS-com-partitionsetlink**](a-mscom-partitionsetlink.md)                    | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**MS-com-userlink**](a-mscom-userlink.md)                                    | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**MS-DFSR-computerreferencebl**](a-msdfsr-computerreferencebl.md)            | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**MS-DFSR-mitgliedreferencebl**](a-msdfsr-memberreferencebl.md)                | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-allowed-to-Delegat-an**](a-msds-allowedtodelegateto.md)             | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-ca-immed-untergeordnete Elemente**](a-msds-approx-immed-subordinates.md)    | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-authentieredto-accountlist**](a-msds-authenticatedtoaccountlist.md) | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Konsistenz-untergeordnet-Anzahl**](a-ms-ds-consistencychildcount.md)         | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                      | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-hab-Seniority-Index**](a-msds-habseniorityindex.md)                  | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-is-Domain-for**](a-msds-isdomainfor.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-is-full-Replica-for**](a-msds-isfullreplicafor.md)                   | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-is-Partial-Replica-for**](a-msds-ispartialreplicafor.md)             | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-krbtgt-Link-BL**](a-msds-krbtgtlinkbl.md)                            | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-gemastert von**](a-msds-masteredby.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Members-für-AZ-Role-BL**](a-msds-membersforazrolebl.md)              | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-NC-repl-Cursor**](a-msds-ncreplcursors.md)                          | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-NC-repl-Inbound-Nachbarn**](a-msds-ncreplinboundneighbors.md)       | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-NC-repl-Outbound-Nachbarn**](a-msds-ncreploutboundneighbors.md)     | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)  | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-NC-Typ**](a-msds-nctype.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                            | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                  | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)        | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)        | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Phonetic-Company-Name**](a-msds-phoneticcompanyname.md)              | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-Phonetic-Department**](a-msds-phoneticdepartment.md)                 | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-Phonetic-Display-Name**](a-msds-phoneticdisplayname.md)              | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/> [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                |
| [**ms-DS-Phonetic-First-Name**](a-msds-phoneticfirstname.md)                  | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-Phonetic-Last-Name**](a-msds-phoneticlastname.md)                    | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                           | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-PSO-angewendet**](a-msds-psoapplied.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)         | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                 | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-offengelegt-DSAs**](a-msds-revealeddsas.md)                             | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-enthüllt-List-BL**](a-msds-revealedlistbl.md)                        | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Source-Object-DN**](a-msds-sourceobjectdn.md)                        | False     | **Kontakt**                                                                                                                            |
| [**ms-DS-Tasks-für-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                  | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Tasks-für-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                  | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-Exch-Assistant-Name**](a-msexchassistantname.md)                        | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**ms-Exch-House-Identifier**](a-msexchhouseidentifier.md)                    | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-Exch-LabeledURI**](a-msexchlabeleduri.md)                               | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**msSFU-30-POSIX-Member-of**](a-mssfu30posixmemberof.md)                     | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**NetBoot-SCP-BL**](a-netbootscpbl.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Nicht sicherheitsmitglied-BL**](a-nonsecuritymemberbl.md)                        | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                       | Richtig      | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Objekt-Kategorie**](a-objectcategory.md)                                    | Richtig      | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Object-Klasse**](a-objectclass.md)                                          | Richtig      | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Objekt-GUID**](a-objectguid.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Objekt-Version**](a-objectversion.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Organisations Einheits Name**](a-ou.md)                                       | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Name der Organisation**](a-o.md)                                               | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Sonstiges-Postfach**](a-othermailbox.md)                                        | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Anderer Name**](a-middlename.md)                                             | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Andere-bekannte Objekte**](a-otherwellknownobjects.md)                    | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Partial-Attribute-löschen-List**](a-partialattributedeletionlist.md)      | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Partiell-Attribut Satz**](a-partialattributeset.md)                         | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Persönliche Titel**](a-personaltitle.md)                                      | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-Fax-Sonstiges**](a-otherfacsimiletelephonenumber.md)                     | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-privat (Sonstiges)**](a-otherhomephone.md)                                   | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-Home-primär**](a-homephone.md)                                      | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-IP-Sonstiges**](a-otheripphone.md)                                       | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-IP-primär**](a-ipphone.md)                                          | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Phone-ISDN-Primary**](a-primaryinternationalisdnnumber.md)                 | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Phone-Mobile-other**](a-othermobile.md)                                    | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Phone-Mobile-Primary**](a-mobile.md)                                       | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-Office-Sonstiges**](a-othertelephone.md)                                 | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-Pager-Sonstiges**](a-otherpager.md)                                      | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-Pager-primär**](a-pager.md)                                         | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Physical-delivery-Office-Name**](a-physicaldeliveryofficename.md)          | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Picture**](a-thumbnailphoto.md)                                            | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Mögliche-minderwertig**](a-possibleinferiors.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Postanschrift**](a-postaladdress.md)                                      | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Postleitzahl**](a-postalcode.md)                                            | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Post-Office-Box**](a-postofficebox.md)                                     | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Bevorzugte Übermittlungs Methode**](a-preferreddeliverymethod.md)                 | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Proxy-Objekt Name**](a-proxiedobjectname.md)                             | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Proxy Adressen**](a-proxyaddresses.md)                                    | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Abfrage-Richtlinie-BL**](a-querypolicybl.md)                                     | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**RDN**](a-name.md)                                                          | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Registrierte Adresse**](a-registeredaddress.md)                              | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                      | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**REPL-Update-Vector**](a-repluptodatevector.md)                           | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Berichte**](a-directreports.md)                                             | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Reps-from**](a-repsfrom.md)                                                | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Reps-to**](a-repsto.md)                                                    | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Novel**](a-revision.md)                                                 | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**SD-Rechte**](a-sdrightseffective.md)                             | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**secretary**](a-secretary.md)                                               | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Siehe auch**](a-seealso.md)                                                  | False     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**Seriennummer**](a-serialnumber.md)                                        | False     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**Server-Reference-BL**](a-serverreferencebl.md)                             | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**In-Address-Book anzeigen**](a-showinaddressbook.md)                            | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Anzeigen-in-Advanced-nur anzeigen**](a-showinadvancedviewonly.md)                 | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Site-Object-BL**](a-siteobjectbl.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**State-or-Province-Name**](a-st.md)                                         | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Straße**](a-street.md)                                             | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Struktur-Objekt-Klasse**](a-structuralobjectclass.md)                     | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Sub-Refs**](a-subrefs.md)                                                  | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Subschemasubentry**](a-subschemasubentry.md)                               | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Nachname**](a-sn.md)                                                        | False     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**SystemFlags**](a-systemflags.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Telefonnummer**](a-telephonenumber.md)                                  | False     | [**Person**](c-person.md)<br/> [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                             |
| [**Teletex-Terminal-Identifier**](a-teletexterminalidentifier.md)             | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telex-Nummer**](a-telexnumber.md)                                          | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telex-primär**](a-primarytelexnumber.md)                                  | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Text-Country**](a-co.md)                                                   | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Text-codiert-or-address**](a-textencodedoraddress.md)                      | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Titel**](a-title.md)                                                       | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Benutzerzertifikat**](a-usercert.md)                                                | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Benutzer Kommentar**](a-comment.md)                                              | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Benutzer Kennwort**](a-userpassword.md)                                        | False     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**Benutzersmime-Zertifikat**](a-usersmimecertificate.md)                       | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Die Anwendung wurde geändert.**](a-usnchanged.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Von der Anwendung erstellte**](a-usncreated.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**USA-DSA-letzte-obj-entfernt**](a-usndsalastobjremoved.md)                     | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Standort-und standortübergreifende standortübergreifende**](a-usnintersite.md)                                        | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**"An-Last-obj-REM"**](a-usnlastobjrem.md)                                    | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Quell Code Quelle**](a-usnsource.md)                                              | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**WBEM-Pfad**](a-wbempath.md)                                                | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Bekannte Objekte**](a-wellknownobjects.md)                               | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Bei Änderung**](a-whenchanged.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Bei Erstellung**](a-whencreated.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**WWW-Homepage**](a-wwwhomepage.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**WWW-Page-other**](a-url.md)                                                | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**X121-Adresse**](a-x121address.md)                                          | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**X509-CERT**](a-usercertificate.md)                                         | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |



## <a name="windows-server-2008-property-sets"></a>Windows Server 2008-Eigenschaften Sätze

Diese Klasse enthält die folgenden Eigenschaften Sätze für Windows Server 2008:



| Allgemeiner Name                                            |
|--------------------------------------------------------|
| [**Persönliche Informationen**](r-personal-information.md) |
| [**Webinformationen**](r-web-information.md)           |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2

-   [Attribute](#windows-server-2008-r2-attributes)
-   [Eigenschaftensätze](#windows-server-2008-r2-property-sets)



| Eingabe | Wert |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | False                                                                                        |
| Object-Category             | 1                                                                                            |
| Default-Object-Category     | [**Person**](c-person.md)<br/>                                                        |
| Governs-Id                  | 1.2.840.113556.1.5.15                                                                        |
| Standard-ausblenden-Wert        | 0                                                                                            |
| RDN-ATT-ID                  | [**Gemeinsamer Name**](a-cn.md)<br/>                                                       |
| Unterklasse von                 | [**Unternehmensperson**](c-organizationalperson.md)<br/>                           |
| Mögliche Vorgesetzten          | [**Domänen-DNS**](c-domaindns.md)[**-Organisationseinheit**](c-organizationalunit.md)         |
| Zusätzlich           | E [**-Mail-Empfänger**](c-mailrecipient.md) (System)                                           |
| NT-Security-Descriptor      | o:Bag: schlecht: S:                                                                                 |
| Standard Sicherheits Beschreibung | D: (A;; rpwpcrccdclclorcwowdsddtsw;;;D a) (a;; Rpwpcrccdclclorcwowdsddtsw;;; SY) (A;; Rplclorc;;; Thaus |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2008-r2-attributes"></a>Windows Server 2008 R2-Attribute

Diese Klasse enthält die folgenden Attribute für Windows Server 2008 R2:



| Attribut                                                                        | Obligatorisch. | Abgeleitet von                                                                                                                           |
|----------------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**Weitere Informationen**](a-notes.md)                                        | False     | **Kontakt**                                                                                                                            |
| [**Adresse**](a-streetaddress.md)                                               | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Adresse-Startseite**](a-homepostaladdress.md)                                      | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Administrator: Beschreibung**](a-admindescription.md)                                  | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Administrator-Anzeige Name**](a-admindisplayname.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Zulässige Attribute**](a-allowedattributes.md)                                | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Zulässige Attribute-gültig**](a-allowedattributeseffective.md)             | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Zulässige, untergeordnete Klassen**](a-allowedchildclasses.md)                           | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Zulässig-untergeordnete Klassen-gültig**](a-allowedchildclasseseffective.md)        | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Geordneter**](a-assistant.md)                                                 | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**attributecertificateattribute**](a-attributecertificateattribute.md)         | False     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                    | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Kanonischer Name**](a-canonicalname.md)                                        | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Geäußert**](a-info.md)                                                        | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Gemeinsamer Name**](a-cn.md)                                                      | Richtig      | **Kontakt** [ **Person**](c-person.md)<br/> [**E-Mail-Empfänger**](c-mailrecipient.md)<br/> [**Nach oben**](c-top.md)<br/> |
| [**Company**](a-company.md)                                                     | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Länder Code**](a-countrycode.md)                                            | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Länder Name**](a-c.md)                                                      | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Create-Zeitstempel**](a-createtimestamp.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Klinik**](a-department.md)                                               | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Beschreibung**](a-description.md)                                             | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Ziel-Indikator**](a-destinationindicator.md)                          | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Anzeige Name**](a-displayname.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Anzeige Name-druckdruck**](a-displaynameprintable.md)                         | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Division**](a-division.md)                                                   | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**DSA-Signatur**](a-dsasignature.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**DS-Core-propagierungs Daten**](a-dscorepropagationdata.md)                      | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**E-Mail-Adressen**](a-mail.md)                                               | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Mitarbeiter-ID**](a-employeeid.md)                                              | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Erweiterungs Name**](a-extensionname.md)                                        | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Fax-Telefonnummer**](a-facsimiletelephonenumber.md)                 | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Fahren**](a-flags.md)                                                         | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Aus-Eintrag**](a-fromentry.md)                                                | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                    | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                        | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**"F"-Rollen Besitzer**](a-fsmoroleowner.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Garbage Koll-Zeitraum**](a-garbagecollperiod.md)                               | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Generierung-Qualifizierer**](a-generationqualifier.md)                            | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Vorname**](a-givenname.md)                                                | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**HouseIdentifier**](a-houseidentifier.md)                                     | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Initialen**](a-initials.md)                                                   | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Instanztyp**](a-instancetype.md)                                          | Richtig      | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**International-ISDN-Number**](a-internationalisdnnumber.md)                   | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Is-critical-System-Object**](a-iscriticalsystemobject.md)                    | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Ist-gelöscht**](a-isdeleted.md)                                                | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Is-Member-of-DL**](a-memberof.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Is-Privilege-Inhaber**](a-isprivilegeholder.md)                               | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Ist-recycelt**](a-isrecycled.md)                                              | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**LabeledURI**](a-labeleduri.md)                                               | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Letztes-bekannt/übergeordnetes Element**](a-lastknownparent.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Legacy-Exchange-DN**](a-legacyexchangedn.md)                                 | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Lokalitäts Name**](a-l.md)                                                     | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Logo**](a-thumbnaillogo.md)                                                  | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Verwaltete Objekte**](a-managedobjects.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Dienst**](a-manager.md)                                                     | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Verwaltet von**](a-masteredby.md)                                              | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**MHS-or-address**](a-mhsoraddress.md)                                         | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Modify-Zeitstempel**](a-modifytimestamp.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**MS-com-partitionsetlink**](a-mscom-partitionsetlink.md)                      | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**MS-com-userlink**](a-mscom-userlink.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**MS-DFSR-computerreferencebl**](a-msdfsr-computerreferencebl.md)              | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**MS-DFSR-mitgliedreferencebl**](a-msdfsr-memberreferencebl.md)                  | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-allowed-to-Delegat-an**](a-msds-allowedtodelegateto.md)               | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-ca-immed-untergeordnete Elemente**](a-msds-approx-immed-subordinates.md)      | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-authentieredto-accountlist**](a-msds-authenticatedtoaccountlist.md)   | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Konsistenz-untergeordnet-Anzahl**](a-ms-ds-consistencychildcount.md)           | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                        | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-aktiviert-Feature-BL**](a-msds-enabledfeaturebl.md)                      | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-hab-Seniority-Index**](a-msds-habseniorityindex.md)                    | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-Host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)             | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-is-Domain-for**](a-msds-isdomainfor.md)                                | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-is-full-Replica-for**](a-msds-isfullreplicafor.md)                     | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-is-Partial-Replica-for**](a-msds-ispartialreplicafor.md)               | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-krbtgt-Link-BL**](a-msds-krbtgtlinkbl.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-local-Effective-Lösch Zeit**](a-msds-localeffectivedeletiontime.md) | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-local-Effective-Papier-Time**](a-msds-localeffectiverecycletime.md)   | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-gemastert von**](a-msds-masteredby.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Members-für-AZ-Role-BL**](a-msds-membersforazrolebl.md)                | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-NC-repl-Cursor**](a-msds-ncreplcursors.md)                            | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-NC-repl-Inbound-Nachbarn**](a-msds-ncreplinboundneighbors.md)         | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-NC-repl-Outbound-Nachbarn**](a-msds-ncreploutboundneighbors.md)       | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)    | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-NC-Typ**](a-msds-nctype.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                    | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-oidtoidgruppe-Link-BL**](a-msds-oidtogrouplinkbl.md)                      | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)          | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)          | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Phonetic-Company-Name**](a-msds-phoneticcompanyname.md)                | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-Phonetic-Department**](a-msds-phoneticdepartment.md)                   | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-Phonetic-Display-Name**](a-msds-phoneticdisplayname.md)                | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/> [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                |
| [**ms-DS-Phonetic-First-Name**](a-msds-phoneticfirstname.md)                    | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-Phonetic-Last-Name**](a-msds-phoneticlastname.md)                      | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                             | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-PSO-angewendet**](a-msds-psoapplied.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)           | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                   | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-offengelegt-DSAs**](a-msds-revealeddsas.md)                               | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-enthüllt-List-BL**](a-msds-revealedlistbl.md)                          | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Source-Object-DN**](a-msds-sourceobjectdn.md)                          | False     | **Kontakt**                                                                                                                            |
| [**ms-DS-Tasks-für-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                    | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Tasks-für-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                    | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-Exch-Assistant-Name**](a-msexchassistantname.md)                          | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**ms-Exch-House-Identifier**](a-msexchhouseidentifier.md)                      | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-Exch-LabeledURI**](a-msexchlabeleduri.md)                                 | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**msSFU-30-POSIX-Member-of**](a-mssfu30posixmemberof.md)                       | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**NetBoot-SCP-BL**](a-netbootscpbl.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Nicht sicherheitsmitglied-BL**](a-nonsecuritymemberbl.md)                          | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                         | Richtig      | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                     | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Objekt-Kategorie**](a-objectcategory.md)                                      | Richtig      | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Object-Klasse**](a-objectclass.md)                                            | Richtig      | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Objekt-GUID**](a-objectguid.md)                                              | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Objekt-Version**](a-objectversion.md)                                        | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Organisations Einheits Name**](a-ou.md)                                         | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Name der Organisation**](a-o.md)                                                 | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Sonstiges-Postfach**](a-othermailbox.md)                                          | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Anderer Name**](a-middlename.md)                                               | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Andere-bekannte Objekte**](a-otherwellknownobjects.md)                      | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Partial-Attribute-löschen-List**](a-partialattributedeletionlist.md)        | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Partiell-Attribut Satz**](a-partialattributeset.md)                           | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Persönliche Titel**](a-personaltitle.md)                                        | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-Fax-Sonstiges**](a-otherfacsimiletelephonenumber.md)                       | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-privat (Sonstiges)**](a-otherhomephone.md)                                     | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-Home-primär**](a-homephone.md)                                        | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-IP-Sonstiges**](a-otheripphone.md)                                         | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-IP-primär**](a-ipphone.md)                                            | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Phone-ISDN-Primary**](a-primaryinternationalisdnnumber.md)                   | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Phone-Mobile-other**](a-othermobile.md)                                      | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Phone-Mobile-Primary**](a-mobile.md)                                         | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-Office-Sonstiges**](a-othertelephone.md)                                   | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-Pager-Sonstiges**](a-otherpager.md)                                        | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-Pager-primär**](a-pager.md)                                           | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Physical-delivery-Office-Name**](a-physicaldeliveryofficename.md)            | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Picture**](a-thumbnailphoto.md)                                              | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Mögliche-minderwertig**](a-possibleinferiors.md)                                | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Postanschrift**](a-postaladdress.md)                                        | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Postleitzahl**](a-postalcode.md)                                              | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Post-Office-Box**](a-postofficebox.md)                                       | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Bevorzugte Übermittlungs Methode**](a-preferreddeliverymethod.md)                   | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Proxy-Objekt Name**](a-proxiedobjectname.md)                               | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Proxy Adressen**](a-proxyaddresses.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Abfrage-Richtlinie-BL**](a-querypolicybl.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**RDN**](a-name.md)                                                            | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Registrierte Adresse**](a-registeredaddress.md)                                | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                        | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**REPL-Update-Vector**](a-repluptodatevector.md)                             | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Berichte**](a-directreports.md)                                               | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Reps-from**](a-repsfrom.md)                                                  | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Reps-to**](a-repsto.md)                                                      | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Novel**](a-revision.md)                                                   | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**SD-Rechte**](a-sdrightseffective.md)                               | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**secretary**](a-secretary.md)                                                 | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Siehe auch**](a-seealso.md)                                                    | False     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**Seriennummer**](a-serialnumber.md)                                          | False     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**Server-Reference-BL**](a-serverreferencebl.md)                               | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**In-Address-Book anzeigen**](a-showinaddressbook.md)                              | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Anzeigen-in-Advanced-nur anzeigen**](a-showinadvancedviewonly.md)                   | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Site-Object-BL**](a-siteobjectbl.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**State-or-Province-Name**](a-st.md)                                           | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Straße**](a-street.md)                                               | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Struktur-Objekt-Klasse**](a-structuralobjectclass.md)                       | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Sub-Refs**](a-subrefs.md)                                                    | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Subschemasubentry**](a-subschemasubentry.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Nachname**](a-sn.md)                                                          | False     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**SystemFlags**](a-systemflags.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Telefonnummer**](a-telephonenumber.md)                                    | False     | [**Person**](c-person.md)<br/> [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                             |
| [**Teletex-Terminal-Identifier**](a-teletexterminalidentifier.md)               | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telex-Nummer**](a-telexnumber.md)                                            | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telex-primär**](a-primarytelexnumber.md)                                    | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Text-Country**](a-co.md)                                                     | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Text-codiert-or-address**](a-textencodedoraddress.md)                        | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Titel**](a-title.md)                                                         | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Benutzerzertifikat**](a-usercert.md)                                                  | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Benutzer Kommentar**](a-comment.md)                                                | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Benutzer Kennwort**](a-userpassword.md)                                          | False     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**Benutzersmime-Zertifikat**](a-usersmimecertificate.md)                         | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Die Anwendung wurde geändert.**](a-usnchanged.md)                                              | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Von der Anwendung erstellte**](a-usncreated.md)                                              | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**USA-DSA-letzte-obj-entfernt**](a-usndsalastobjremoved.md)                       | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Standort-und standortübergreifende standortübergreifende**](a-usnintersite.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**"An-Last-obj-REM"**](a-usnlastobjrem.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Quell Code Quelle**](a-usnsource.md)                                                | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**WBEM-Pfad**](a-wbempath.md)                                                  | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Bekannte Objekte**](a-wellknownobjects.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Bei Änderung**](a-whenchanged.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Bei Erstellung**](a-whencreated.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**WWW-Homepage**](a-wwwhomepage.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**WWW-Page-other**](a-url.md)                                                  | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**X121-Adresse**](a-x121address.md)                                            | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**X509-CERT**](a-usercertificate.md)                                           | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |



## <a name="windows-server-2008-r2-property-sets"></a>Windows Server 2008 R2-Eigenschaften Sätze

Diese Klasse enthält die folgenden Eigenschaften Sätze für Windows Server 2008 R2:



| Allgemeiner Name                                            |
|--------------------------------------------------------|
| [**Persönliche Informationen**](r-personal-information.md) |
| [**Webinformationen**](r-web-information.md)           |



## <a name="windows-server-2012"></a>Windows Server 2012

-   [Attribute](#windows-server-2012-attributes)
-   [Eigenschaftensätze](#windows-server-2012-property-sets)



| Eingabe | Wert |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | False                                                                                        |
| Object-Category             | 1                                                                                            |
| Default-Object-Category     | [**Person**](c-person.md)<br/>                                                        |
| Governs-Id                  | 1.2.840.113556.1.5.15                                                                        |
| Standard-ausblenden-Wert        | 0                                                                                            |
| RDN-ATT-ID                  | [**Gemeinsamer Name**](a-cn.md)<br/>                                                       |
| Unterklasse von                 | [**Unternehmensperson**](c-organizationalperson.md)<br/>                           |
| Mögliche Vorgesetzten          | [**Domänen-DNS**](c-domaindns.md)[**-Organisationseinheit**](c-organizationalunit.md)         |
| Zusätzlich           | E [**-Mail-Empfänger**](c-mailrecipient.md) (System)                                           |
| NT-Security-Descriptor      | o:Bag: schlecht: S:                                                                                 |
| Standard Sicherheits Beschreibung | D: (A;; rpwpcrccdclclorcwowdsddtsw;;;D a) (a;; Rpwpcrccdclclorcwowdsddtsw;;; SY) (A;; Rplclorc;;; Thaus |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2012-attributes"></a>Windows Server 2012-Attribute

Diese Klasse enthält die folgenden Attribute für Windows Server 2012:



| Attribut                                                                                              | Obligatorisch. | Abgeleitet von                                                                                                                           |
|--------------------------------------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**Weitere Informationen**](a-notes.md)                                                              | False     | **Kontakt**                                                                                                                            |
| [**Adresse**](a-streetaddress.md)                                                                     | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Adresse-Startseite**](a-homepostaladdress.md)                                                            | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Administrator: Beschreibung**](a-admindescription.md)                                                        | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Administrator-Anzeige Name**](a-admindisplayname.md)                                                       | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Zulässige Attribute**](a-allowedattributes.md)                                                      | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Zulässige Attribute-gültig**](a-allowedattributeseffective.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Zulässige, untergeordnete Klassen**](a-allowedchildclasses.md)                                                 | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Zulässig-untergeordnete Klassen-gültig**](a-allowedchildclasseseffective.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Geordneter**](a-assistant.md)                                                                       | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**attributecertificateattribute**](a-attributecertificateattribute.md)                               | False     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Kanonischer Name**](a-canonicalname.md)                                                              | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Geäußert**](a-info.md)                                                                              | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Gemeinsamer Name**](a-cn.md)                                                                            | Richtig      | **Kontakt** [ **Person**](c-person.md)<br/> [**E-Mail-Empfänger**](c-mailrecipient.md)<br/> [**Nach oben**](c-top.md)<br/> |
| [**Company**](a-company.md)                                                                           | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Länder Code**](a-countrycode.md)                                                                  | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Länder Name**](a-c.md)                                                                            | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Create-Zeitstempel**](a-createtimestamp.md)                                                         | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Klinik**](a-department.md)                                                                     | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Beschreibung**](a-description.md)                                                                   | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Ziel-Indikator**](a-destinationindicator.md)                                                | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Anzeige Name**](a-displayname.md)                                                                  | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Anzeige Name-druckdruck**](a-displaynameprintable.md)                                               | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Division**](a-division.md)                                                                         | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**DSA-Signatur**](a-dsasignature.md)                                                                | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**DS-Core-propagierungs Daten**](a-dscorepropagationdata.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**E-Mail-Adressen**](a-mail.md)                                                                     | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Mitarbeiter-ID**](a-employeeid.md)                                                                    | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Erweiterungs Name**](a-extensionname.md)                                                              | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Fax-Telefonnummer**](a-facsimiletelephonenumber.md)                                       | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Fahren**](a-flags.md)                                                                               | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Aus-Eintrag**](a-fromentry.md)                                                                      | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                                              | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**"F"-Rollen Besitzer**](a-fsmoroleowner.md)                                                             | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Garbage Koll-Zeitraum**](a-garbagecollperiod.md)                                                     | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Generierung-Qualifizierer**](a-generationqualifier.md)                                                  | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Vorname**](a-givenname.md)                                                                      | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**HouseIdentifier**](a-houseidentifier.md)                                                           | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Initialen**](a-initials.md)                                                                         | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Instanztyp**](a-instancetype.md)                                                                | Richtig      | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**International-ISDN-Number**](a-internationalisdnnumber.md)                                         | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Is-critical-System-Object**](a-iscriticalsystemobject.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Ist-gelöscht**](a-isdeleted.md)                                                                      | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Is-Member-of-DL**](a-memberof.md)                                                                  | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Is-Privilege-Inhaber**](a-isprivilegeholder.md)                                                     | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Ist-recycelt**](a-isrecycled.md)                                                                    | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**LabeledURI**](a-labeleduri.md)                                                                     | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Letztes-bekannt/übergeordnetes Element**](a-lastknownparent.md)                                                         | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Legacy-Exchange-DN**](a-legacyexchangedn.md)                                                       | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Lokalitäts Name**](a-l.md)                                                                           | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Logo**](a-thumbnaillogo.md)                                                                        | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Verwaltete Objekte**](a-managedobjects.md)                                                            | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Dienst**](a-manager.md)                                                                           | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Verwaltet von**](a-masteredby.md)                                                                    | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**MHS-or-address**](a-mhsoraddress.md)                                                               | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Modify-Zeitstempel**](a-modifytimestamp.md)                                                         | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**MS-com-partitionsetlink**](a-mscom-partitionsetlink.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**MS-com-userlink**](a-mscom-userlink.md)                                                            | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**MS-DFSR-computerreferencebl**](a-msdfsr-computerreferencebl.md)                                    | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**MS-DFSR-mitgliedreferencebl**](a-msdfsr-memberreferencebl.md)                                        | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-allowed-to-act-on-Do-of-other-Identity**](a-msds-allowedtoactonbehalfofotheridentity.md) | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-allowed-to-Delegat-an**](a-msds-allowedtodelegateto.md)                                     | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-ca-immed-untergeordnete Elemente**](a-msds-approx-immed-subordinates.md)                            | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-authentieredto-accountlist**](a-msds-authenticatedtoaccountlist.md)                         | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Claim-Shares-mögliche-values-with-BL**](a-msds-claimsharespossiblevalueswithbl.md)           | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Konsistenz-untergeordnet-Anzahl**](a-ms-ds-consistencychildcount.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                                              | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-aktiviert-Feature-BL**](a-msds-enabledfeaturebl.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Geokoordinaten-Höhe**](a-msds-geocoordinatesaltitude.md)                                 | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**ms-DS-Geokoordinaten-Breitengrad**](a-msds-geocoordinateslatitude.md)                                 | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**ms-DS-Geokoordinaten-Längengrad**](a-msds-geocoordinateslongitude.md)                               | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**ms-DS-hab-Seniority-Index**](a-msds-habseniorityindex.md)                                          | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-Host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-is-Domain-for**](a-msds-isdomainfor.md)                                                      | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-is-full-Replica-for**](a-msds-isfullreplicafor.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-is-Partial-Replica-for**](a-msds-ispartialreplicafor.md)                                     | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-is-Primary-Computer-für**](a-msds-isprimarycomputerfor.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-krbtgt-Link-BL**](a-msds-krbtgtlinkbl.md)                                                    | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                                                    | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-local-Effective-Lösch Zeit**](a-msds-localeffectivedeletiontime.md)                       | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-local-Effective-Papier-Time**](a-msds-localeffectiverecycletime.md)                         | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-gemastert von**](a-msds-masteredby.md)                                                         | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Members-für-AZ-Role-BL**](a-msds-membersforazrolebl.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Members-of-Resource-Property-List-BL**](a-msds-membersofresourcepropertylistbl.md)           | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-NC-repl-Cursor**](a-msds-ncreplcursors.md)                                                  | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-NC-repl-Inbound-Nachbarn**](a-msds-ncreplinboundneighbors.md)                               | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-NC-repl-Outbound-Nachbarn**](a-msds-ncreploutboundneighbors.md)                             | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)                          | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-NC-Typ**](a-msds-nctype.md)                                                                 | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                                                    | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-oidtoidgruppe-Link-BL**](a-msds-oidtogrouplinkbl.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)                                | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)                                | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Phonetic-Company-Name**](a-msds-phoneticcompanyname.md)                                      | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-Phonetic-Department**](a-msds-phoneticdepartment.md)                                         | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-Phonetic-Display-Name**](a-msds-phoneticdisplayname.md)                                      | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/> [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                |
| [**ms-DS-Phonetic-First-Name**](a-msds-phoneticfirstname.md)                                          | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-Phonetic-Last-Name**](a-msds-phoneticlastname.md)                                            | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                                                   | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-PSO-angewendet**](a-msds-psoapplied.md)                                                         | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-offengelegt-DSAs**](a-msds-revealeddsas.md)                                                     | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-enthüllt-List-BL**](a-msds-revealedlistbl.md)                                                | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Source-Object-DN**](a-msds-sourceobjectdn.md)                                                | False     | **Kontakt**                                                                                                                            |
| [**ms-DS-Tasks-für-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Tasks-für-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-TDO-Egress-BL**](a-msds-tdoegressbl.md)                                                      | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-TDO-Ingress-BL**](a-msds-tdoingressbl.md)                                                    | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Value-Type-Reference-BL**](a-msds-valuetypereferencebl.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-Exch-Assistant-Name**](a-msexchassistantname.md)                                                | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**ms-Exch-House-Identifier**](a-msexchhouseidentifier.md)                                            | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-Exch-LabeledURI**](a-msexchlabeleduri.md)                                                       | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                                                  | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**msSFU-30-POSIX-Member-of**](a-mssfu30posixmemberof.md)                                             | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**NetBoot-SCP-BL**](a-netbootscpbl.md)                                                               | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Nicht sicherheitsmitglied-BL**](a-nonsecuritymemberbl.md)                                                | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                                               | Richtig      | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                                           | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Objekt-Kategorie**](a-objectcategory.md)                                                            | Richtig      | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Object-Klasse**](a-objectclass.md)                                                                  | Richtig      | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Objekt-GUID**](a-objectguid.md)                                                                    | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Objekt-Version**](a-objectversion.md)                                                              | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Organisations Einheits Name**](a-ou.md)                                                               | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Name der Organisation**](a-o.md)                                                                       | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Sonstiges-Postfach**](a-othermailbox.md)                                                                | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Anderer Name**](a-middlename.md)                                                                     | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Andere-bekannte Objekte**](a-otherwellknownobjects.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Partial-Attribute-löschen-List**](a-partialattributedeletionlist.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Partiell-Attribut Satz**](a-partialattributeset.md)                                                 | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Persönliche Titel**](a-personaltitle.md)                                                              | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-Fax-Sonstiges**](a-otherfacsimiletelephonenumber.md)                                             | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-privat (Sonstiges)**](a-otherhomephone.md)                                                           | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-Home-primär**](a-homephone.md)                                                              | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-IP-Sonstiges**](a-otheripphone.md)                                                               | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-IP-primär**](a-ipphone.md)                                                                  | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Phone-ISDN-Primary**](a-primaryinternationalisdnnumber.md)                                         | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Phone-Mobile-other**](a-othermobile.md)                                                            | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Phone-Mobile-Primary**](a-mobile.md)                                                               | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-Office-Sonstiges**](a-othertelephone.md)                                                         | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-Pager-Sonstiges**](a-otherpager.md)                                                              | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-Pager-primär**](a-pager.md)                                                                 | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Physical-delivery-Office-Name**](a-physicaldeliveryofficename.md)                                  | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Picture**](a-thumbnailphoto.md)                                                                    | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Mögliche-minderwertig**](a-possibleinferiors.md)                                                      | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Postanschrift**](a-postaladdress.md)                                                              | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Postleitzahl**](a-postalcode.md)                                                                    | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Post-Office-Box**](a-postofficebox.md)                                                             | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Bevorzugte Übermittlungs Methode**](a-preferreddeliverymethod.md)                                         | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Proxy-Objekt Name**](a-proxiedobjectname.md)                                                     | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Proxy Adressen**](a-proxyaddresses.md)                                                            | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Abfrage-Richtlinie-BL**](a-querypolicybl.md)                                                             | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**RDN**](a-name.md)                                                                                  | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Registrierte Adresse**](a-registeredaddress.md)                                                      | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                                              | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**REPL-Update-Vector**](a-repluptodatevector.md)                                                   | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Berichte**](a-directreports.md)                                                                     | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Reps-from**](a-repsfrom.md)                                                                        | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Reps-to**](a-repsto.md)                                                                            | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Novel**](a-revision.md)                                                                         | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**SD-Rechte**](a-sdrightseffective.md)                                                     | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**secretary**](a-secretary.md)                                                                       | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Siehe auch**](a-seealso.md)                                                                          | False     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**Seriennummer**](a-serialnumber.md)                                                                | False     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**Server-Reference-BL**](a-serverreferencebl.md)                                                     | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**In-Address-Book anzeigen**](a-showinaddressbook.md)                                                    | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Anzeigen-in-Advanced-nur anzeigen**](a-showinadvancedviewonly.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Site-Object-BL**](a-siteobjectbl.md)                                                               | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**State-or-Province-Name**](a-st.md)                                                                 | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Straße**](a-street.md)                                                                     | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Struktur-Objekt-Klasse**](a-structuralobjectclass.md)                                             | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Sub-Refs**](a-subrefs.md)                                                                          | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Subschemasubentry**](a-subschemasubentry.md)                                                       | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Nachname**](a-sn.md)                                                                                | False     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**SystemFlags**](a-systemflags.md)                                                                  | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Telefonnummer**](a-telephonenumber.md)                                                          | False     | [**Person**](c-person.md)<br/> [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                             |
| [**Teletex-Terminal-Identifier**](a-teletexterminalidentifier.md)                                     | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telex-Nummer**](a-telexnumber.md)                                                                  | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telex-primär**](a-primarytelexnumber.md)                                                          | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Text-Country**](a-co.md)                                                                           | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Text-codiert-or-address**](a-textencodedoraddress.md)                                              | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Titel**](a-title.md)                                                                               | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Benutzerzertifikat**](a-usercert.md)                                                                        | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Benutzer Kommentar**](a-comment.md)                                                                      | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Benutzer Kennwort**](a-userpassword.md)                                                                | False     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**Benutzersmime-Zertifikat**](a-usersmimecertificate.md)                                               | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Die Anwendung wurde geändert.**](a-usnchanged.md)                                                                    | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Von der Anwendung erstellte**](a-usncreated.md)                                                                    | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**USA-DSA-letzte-obj-entfernt**](a-usndsalastobjremoved.md)                                             | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Standort-und standortübergreifende standortübergreifende**](a-usnintersite.md)                                                                | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**"An-Last-obj-REM"**](a-usnlastobjrem.md)                                                            | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Quell Code Quelle**](a-usnsource.md)                                                                      | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**WBEM-Pfad**](a-wbempath.md)                                                                        | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Bekannte Objekte**](a-wellknownobjects.md)                                                       | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Bei Änderung**](a-whenchanged.md)                                                                  | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Bei Erstellung**](a-whencreated.md)                                                                  | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**WWW-Homepage**](a-wwwhomepage.md)                                                                 | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**WWW-Page-other**](a-url.md)                                                                        | False     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**X121-Adresse**](a-x121address.md)                                                                  | False     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**X509-CERT**](a-usercertificate.md)                                                                 | False     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |



## <a name="windows-server-2012-property-sets"></a>Windows Server 2012-Eigenschaften Sätze

Diese Klasse enthält die folgenden Eigenschaften Sätze für Windows Server 2012:



| Allgemeiner Name                                            |
|--------------------------------------------------------|
| [**Persönliche Informationen**](r-personal-information.md) |
| [**Webinformationen**](r-web-information.md)           |



 

 





