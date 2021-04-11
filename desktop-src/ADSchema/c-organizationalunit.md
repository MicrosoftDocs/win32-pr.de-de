---
title: Organizational-Unit-Klasse
description: Ein Container zum Speichern von Benutzern, Computern und anderen Konto Objekten.
ms.assetid: a5a99dc7-9000-478c-9545-473cfb6ddf6c
ms.tgt_platform: multiple
keywords:
- AD-Schema der Organizational-Unit-Klasse
- OrganizationalUnit-Klasse, AD-Schema
topic_type:
- apiref
api_name:
- Organizational-Unit
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a02c893b09ec6a2292c0304c10e94cfda1616f91
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103957276"
---
# <a name="organizational-unit-class"></a>Organizational-Unit-Klasse

Ein Container zum Speichern von Benutzern, Computern und anderen Konto Objekten.



| Eingabe | Wert |
|-------------------|--------------------------------------|
| CN                | Organizational-Unit                  |
| LDAP-Display-Name | organizationalUnit                   |
| Berechtigung aktualisieren  | Jeder kann dieses Objekt aktualisieren.       |
| Aktualisierungshäufigkeit  | \-                                   |
| Schema-ID-GUID    | bf967aa5-0de6-11d0-a285-00aa003049e2 |



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
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | False                                                                                                                                                                                                                                                                                                    |
| Object-Category             | 1                                                                                                                                                                                                                                                                                                        |
| Default-Object-Category     | \-                                                                                                                                                                                                                                                                                                       |
| Governs-Id                  | 2.5.6.5                                                                                                                                                                                                                                                                                                  |
| Standard-ausblenden-Wert        | 0                                                                                                                                                                                                                                                                                                        |
| RDN-ATT-ID                  | [**Organisations Einheits Name**](a-ou.md)<br/>                                                                                                                                                                                                                                                      |
| Unterklasse von                 | [**Nach oben**](c-top.md)<br/>                                                                                                                                                                                                                                                                          |
| Mögliche Vorgesetzten          | [**Domänen-DNS**](c-domaindns.md)-[**Organisation**](c-organization.md) (**Organisationseinheit**)                                                                                                                                                                                                           |
| Zusätzlich           | \-                                                                                                                                                                                                                                                                                                       |
| NT-Security-Descriptor      | o:Bag: schlecht: S:                                                                                                                                                                                                                                                                                             |
| Standard Sicherheits Beschreibung | D: (A;; Rpwpcrccdclclorcwowdsddtsw;;; SY) (A;; rpwpcrccdclclorcwowdsddtsw;;;D A) (OA;; CCDC; bf967a86-0de6-11D0-A285-00aa003049e2;; AO) (OA;; CCDC; bf967aba-0de6-11D0-A285-00aa003049e2;; AO) (OA;; CCDC; bf967a9c-0de6-11D0-A285-00aa003049e2;; AO) (OA;; CCDC; bf967aa8-0de6-11D0-A285-00aa003049e2;; PO) (A;; Rplclorc;;; Thaus |
| System-Flags                | 0x00000010                                                                                                                                                                                                                                                                                               |



## <a name="windows-2000-server-attributes"></a>Windows 2000-Server Attribute

Diese Klasse enthält die folgenden Attribute für Windows 2000 Server:



| Attribut                                                                 | Obligatorisch. | Abgeleitet von                    |
|---------------------------------------------------------------------------|-----------|---------------------------------|
| [**Administrator: Beschreibung**](a-admindescription.md)                           | False     | [**Nach oben**](c-top.md)<br/> |
| [**Administrator-Anzeige Name**](a-admindisplayname.md)                          | False     | [**Nach oben**](c-top.md)<br/> |
| [**Zulässige Attribute**](a-allowedattributes.md)                         | False     | [**Nach oben**](c-top.md)<br/> |
| [**Zulässige Attribute-gültig**](a-allowedattributeseffective.md)      | False     | [**Nach oben**](c-top.md)<br/> |
| [**Zulässige, untergeordnete Klassen**](a-allowedchildclasses.md)                    | False     | [**Nach oben**](c-top.md)<br/> |
| [**Zulässig-untergeordnete Klassen-gültig**](a-allowedchildclasseseffective.md) | False     | [**Nach oben**](c-top.md)<br/> |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)             | False     | [**Nach oben**](c-top.md)<br/> |
| [**Geschäfts Kategorie**](a-businesscategory.md)                           | False     | **Organisationseinheit**         |
| [**Kanonischer Name**](a-canonicalname.md)                                 | False     | [**Nach oben**](c-top.md)<br/> |
| [**Gemeinsamer Name**](a-cn.md)                                               | False     | [**Nach oben**](c-top.md)<br/> |
| [**Länder Code**](a-countrycode.md)                                     | False     | **Organisationseinheit**         |
| [**Länder Name**](a-c.md)                                               | False     | **Organisationseinheit**         |
| [**Create-Zeitstempel**](a-createtimestamp.md)                            | False     | [**Nach oben**](c-top.md)<br/> |
| [**Standardgruppe**](a-defaultgroup.md)                                   | False     | **Organisationseinheit**         |
| [**Beschreibung**](a-description.md)                                      | False     | [**Nach oben**](c-top.md)<br/> |
| [**Desktop Profil**](a-desktopprofile.md)                               | False     | **Organisationseinheit**         |
| [**Ziel-Indikator**](a-destinationindicator.md)                   | False     | **Organisationseinheit**         |
| [**Anzeige Name**](a-displayname.md)                                     | False     | [**Nach oben**](c-top.md)<br/> |
| [**Anzeige Name-druckdruck**](a-displaynameprintable.md)                  | False     | [**Nach oben**](c-top.md)<br/> |
| [**DSA-Signatur**](a-dsasignature.md)                                   | False     | [**Nach oben**](c-top.md)<br/> |
| [**DS-Core-propagierungs Daten**](a-dscorepropagationdata.md)               | False     | [**Nach oben**](c-top.md)<br/> |
| [**Erweiterungs Name**](a-extensionname.md)                                 | False     | [**Nach oben**](c-top.md)<br/> |
| [**Fax-Telefonnummer**](a-facsimiletelephonenumber.md)          | False     | **Organisationseinheit**         |
| [**Fahren**](a-flags.md)                                                  | False     | [**Nach oben**](c-top.md)<br/> |
| [**Aus-Eintrag**](a-fromentry.md)                                         | False     | [**Nach oben**](c-top.md)<br/> |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)             | False     | [**Nach oben**](c-top.md)<br/> |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                 | False     | [**Nach oben**](c-top.md)<br/> |
| [**"F"-Rollen Besitzer**](a-fsmoroleowner.md)                                | False     | [**Nach oben**](c-top.md)<br/> |
| [**GP-Link**](a-gplink.md)                                               | False     | **Organisationseinheit**         |
| [**GP-Optionen**](a-gpoptions.md)                                         | False     | **Organisationseinheit**         |
| [**Instanztyp**](a-instancetype.md)                                   | Richtig      | [**Nach oben**](c-top.md)<br/> |
| [**International-ISDN-Number**](a-internationalisdnnumber.md)            | False     | **Organisationseinheit**         |
| [**Is-critical-System-Object**](a-iscriticalsystemobject.md)             | False     | [**Nach oben**](c-top.md)<br/> |
| [**Ist-gelöscht**](a-isdeleted.md)                                         | False     | [**Nach oben**](c-top.md)<br/> |
| [**Is-Member-of-DL**](a-memberof.md)                                     | False     | [**Nach oben**](c-top.md)<br/> |
| [**Is-Privilege-Inhaber**](a-isprivilegeholder.md)                        | False     | [**Nach oben**](c-top.md)<br/> |
| [**Letztes-bekannt/übergeordnetes Element**](a-lastknownparent.md)                            | False     | [**Nach oben**](c-top.md)<br/> |
| [**Lokalitäts Name**](a-l.md)                                              | False     | **Organisationseinheit**         |
| [**Logo**](a-thumbnaillogo.md)                                           | False     | **Organisationseinheit**         |
| [**Verwaltet von**](a-managedby.md)                                         | False     | **Organisationseinheit**         |
| [**Verwaltete Objekte**](a-managedobjects.md)                               | False     | [**Nach oben**](c-top.md)<br/> |
| [**Verwaltet von**](a-masteredby.md)                                       | False     | [**Nach oben**](c-top.md)<br/> |
| [**Modify-Zeitstempel**](a-modifytimestamp.md)                            | False     | [**Nach oben**](c-top.md)<br/> |
| [**MS-DS-Konsistenz-untergeordnet-Anzahl**](a-ms-ds-consistencychildcount.md)    | False     | [**Nach oben**](c-top.md)<br/> |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                 | False     | [**Nach oben**](c-top.md)<br/> |
| [**NetBoot-SCP-BL**](a-netbootscpbl.md)                                  | False     | [**Nach oben**](c-top.md)<br/> |
| [**Nicht sicherheitsmitglied-BL**](a-nonsecuritymemberbl.md)                   | False     | [**Nach oben**](c-top.md)<br/> |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                  | Richtig      | [**Nach oben**](c-top.md)<br/> |
| [**Obj-Dist-Name**](a-distinguishedname.md)                              | False     | [**Nach oben**](c-top.md)<br/> |
| [**Objekt-Kategorie**](a-objectcategory.md)                               | Richtig      | [**Nach oben**](c-top.md)<br/> |
| [**Object-Klasse**](a-objectclass.md)                                     | Richtig      | [**Nach oben**](c-top.md)<br/> |
| [**Objekt-GUID**](a-objectguid.md)                                       | False     | [**Nach oben**](c-top.md)<br/> |
| [**Objekt-Version**](a-objectversion.md)                                 | False     | [**Nach oben**](c-top.md)<br/> |
| [**Organisations Einheits Name**](a-ou.md)                                  | Richtig      | **Organisationseinheit**         |
| [**Andere-bekannte Objekte**](a-otherwellknownobjects.md)               | False     | [**Nach oben**](c-top.md)<br/> |
| [**Partial-Attribute-löschen-List**](a-partialattributedeletionlist.md) | False     | [**Nach oben**](c-top.md)<br/> |
| [**Partiell-Attribut Satz**](a-partialattributeset.md)                    | False     | [**Nach oben**](c-top.md)<br/> |
| [**Physical-delivery-Office-Name**](a-physicaldeliveryofficename.md)     | False     | **Organisationseinheit**         |
| [**Mögliche-minderwertig**](a-possibleinferiors.md)                         | False     | [**Nach oben**](c-top.md)<br/> |
| [**Postanschrift**](a-postaladdress.md)                                 | False     | **Organisationseinheit**         |
| [**Postleitzahl**](a-postalcode.md)                                       | False     | **Organisationseinheit**         |
| [**Post-Office-Box**](a-postofficebox.md)                                | False     | **Organisationseinheit**         |
| [**Bevorzugte Übermittlungs Methode**](a-preferreddeliverymethod.md)            | False     | **Organisationseinheit**         |
| [**Proxy-Objekt Name**](a-proxiedobjectname.md)                        | False     | [**Nach oben**](c-top.md)<br/> |
| [**Proxy Adressen**](a-proxyaddresses.md)                               | False     | [**Nach oben**](c-top.md)<br/> |
| [**Abfrage-Richtlinie-BL**](a-querypolicybl.md)                                | False     | [**Nach oben**](c-top.md)<br/> |
| [**RDN**](a-name.md)                                                     | False     | [**Nach oben**](c-top.md)<br/> |
| [**Registrierte Adresse**](a-registeredaddress.md)                         | False     | **Organisationseinheit**         |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                 | False     | [**Nach oben**](c-top.md)<br/> |
| [**REPL-Update-Vector**](a-repluptodatevector.md)                      | False     | [**Nach oben**](c-top.md)<br/> |
| [**Berichte**](a-directreports.md)                                        | False     | [**Nach oben**](c-top.md)<br/> |
| [**Reps-from**](a-repsfrom.md)                                           | False     | [**Nach oben**](c-top.md)<br/> |
| [**Reps-to**](a-repsto.md)                                               | False     | [**Nach oben**](c-top.md)<br/> |
| [**Novel**](a-revision.md)                                            | False     | [**Nach oben**](c-top.md)<br/> |
| [**SD-Rechte**](a-sdrightseffective.md)                        | False     | [**Nach oben**](c-top.md)<br/> |
| [**Such Handbuch**](a-searchguide.md)                                     | False     | **Organisationseinheit**         |
| [**Siehe auch**](a-seealso.md)                                             | False     | **Organisationseinheit**         |
| [**Server-Reference-BL**](a-serverreferencebl.md)                        | False     | [**Nach oben**](c-top.md)<br/> |
| [**Anzeigen-in-Advanced-nur anzeigen**](a-showinadvancedviewonly.md)            | False     | [**Nach oben**](c-top.md)<br/> |
| [**Site-Object-BL**](a-siteobjectbl.md)                                  | False     | [**Nach oben**](c-top.md)<br/> |
| [**State-or-Province-Name**](a-st.md)                                    | False     | **Organisationseinheit**         |
| [**Straße**](a-street.md)                                        | False     | **Organisationseinheit**         |
| [**Sub-Refs**](a-subrefs.md)                                             | False     | [**Nach oben**](c-top.md)<br/> |
| [**Subschemasubentry**](a-subschemasubentry.md)                          | False     | [**Nach oben**](c-top.md)<br/> |
| [**SystemFlags**](a-systemflags.md)                                     | False     | [**Nach oben**](c-top.md)<br/> |
| [**Telefonnummer**](a-telephonenumber.md)                             | False     | **Organisationseinheit**         |
| [**Teletex-Terminal-Identifier**](a-teletexterminalidentifier.md)        | False     | **Organisationseinheit**         |
| [**Telex-Nummer**](a-telexnumber.md)                                     | False     | **Organisationseinheit**         |
| [**Text-Country**](a-co.md)                                              | False     | **Organisationseinheit**         |
| [**UPN-Suffixe**](a-upnsuffixes.md)                                     | False     | **Organisationseinheit**         |
| [**Benutzer Kennwort**](a-userpassword.md)                                   | False     | **Organisationseinheit**         |
| [**Die Anwendung wurde geändert.**](a-usnchanged.md)                                       | False     | [**Nach oben**](c-top.md)<br/> |
| [**Von der Anwendung erstellte**](a-usncreated.md)                                       | False     | [**Nach oben**](c-top.md)<br/> |
| [**USA-DSA-letzte-obj-entfernt**](a-usndsalastobjremoved.md)                | False     | [**Nach oben**](c-top.md)<br/> |
| [**Standort-und standortübergreifende standortübergreifende**](a-usnintersite.md)                                   | False     | [**Nach oben**](c-top.md)<br/> |
| [**"An-Last-obj-REM"**](a-usnlastobjrem.md)                               | False     | [**Nach oben**](c-top.md)<br/> |
| [**Quell Code Quelle**](a-usnsource.md)                                         | False     | [**Nach oben**](c-top.md)<br/> |
| [**WBEM-Pfad**](a-wbempath.md)                                           | False     | [**Nach oben**](c-top.md)<br/> |
| [**Bekannte Objekte**](a-wellknownobjects.md)                          | False     | [**Nach oben**](c-top.md)<br/> |
| [**Bei Änderung**](a-whenchanged.md)                                     | False     | [**Nach oben**](c-top.md)<br/> |
| [**Bei Erstellung**](a-whencreated.md)                                     | False     | [**Nach oben**](c-top.md)<br/> |
| [**WWW-Homepage**](a-wwwhomepage.md)                                    | False     | [**Nach oben**](c-top.md)<br/> |
| [**WWW-Page-other**](a-url.md)                                           | False     | [**Nach oben**](c-top.md)<br/> |
| [**X121-Adresse**](a-x121address.md)                                     | False     | **Organisationseinheit**         |



## <a name="windows-server-2003"></a>Windows Server 2003

-   [Attribute](#windows-server-2003-attributes)
-   [Erweiterte Rechte](#windows-server-2003-extended-rights)



| Eingabe | Wert |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | False                                                                                                                                                                                                                                                                                                                                                                         |
| Object-Category             | 1                                                                                                                                                                                                                                                                                                                                                                             |
| Default-Object-Category     | \-                                                                                                                                                                                                                                                                                                                                                                            |
| Governs-Id                  | 2.5.6.5                                                                                                                                                                                                                                                                                                                                                                       |
| Standard-ausblenden-Wert        | 0                                                                                                                                                                                                                                                                                                                                                                             |
| RDN-ATT-ID                  | [**Organisations Einheits Name**](a-ou.md)<br/>                                                                                                                                                                                                                                                                                                                           |
| Unterklasse von                 | [**Nach oben**](c-top.md)<br/>                                                                                                                                                                                                                                                                                                                                               |
| Mögliche Vorgesetzten          | [**Domänen-DNS**](c-domaindns.md)-**Organisationseinheiten-**[**Organisations**](c-organization.md)[**Land**](c-country.md)                                                                                                                                                                                                                                                    |
| Zusätzlich           | \-                                                                                                                                                                                                                                                                                                                                                                            |
| NT-Security-Descriptor      | o:Bag: schlecht: S:                                                                                                                                                                                                                                                                                                                                                                  |
| Standard Sicherheits Beschreibung | D: (A;; Rpwpcrccdclclorcwowdsddtsw;;; SY) (A;; rpwpcrccdclclorcwowdsddtsw;;;D A) (OA;; CCDC; bf967a86-0de6-11D0-A285-00aa003049e2;; AO) (OA;; CCDC; bf967aba-0de6-11D0-A285-00aa003049e2;; AO) (OA;; CCDC; bf967a9c-0de6-11D0-A285-00aa003049e2;; AO) (OA;; CCDC; bf967aa8-0de6-11D0-A285-00aa003049e2;; PO) (A;; Rplclorc;;; Au) (A;; Lcrplorc;;; ED) (OA;; CCDC; 4828cc14-1437-45bc-9b07-ad6f 015e5f 28;; OS |
| System-Flags                | 0x00000010                                                                                                                                                                                                                                                                                                                                                                    |



## <a name="windows-server-2003-attributes"></a>Windows Server 2003-Attribute

Diese Klasse enthält die folgenden Attribute für Windows Server 2003:



| Attribut                                                                   | Obligatorisch. | Abgeleitet von                    |
|-----------------------------------------------------------------------------|-----------|---------------------------------|
| [**Administrator: Beschreibung**](a-admindescription.md)                             | False     | [**Nach oben**](c-top.md)<br/> |
| [**Administrator-Anzeige Name**](a-admindisplayname.md)                            | False     | [**Nach oben**](c-top.md)<br/> |
| [**Zulässige Attribute**](a-allowedattributes.md)                           | False     | [**Nach oben**](c-top.md)<br/> |
| [**Zulässige Attribute-gültig**](a-allowedattributeseffective.md)        | False     | [**Nach oben**](c-top.md)<br/> |
| [**Zulässige, untergeordnete Klassen**](a-allowedchildclasses.md)                      | False     | [**Nach oben**](c-top.md)<br/> |
| [**Zulässig-untergeordnete Klassen-gültig**](a-allowedchildclasseseffective.md)   | False     | [**Nach oben**](c-top.md)<br/> |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)               | False     | [**Nach oben**](c-top.md)<br/> |
| [**Geschäfts Kategorie**](a-businesscategory.md)                             | False     | **Organisationseinheit**         |
| [**Kanonischer Name**](a-canonicalname.md)                                   | False     | [**Nach oben**](c-top.md)<br/> |
| [**Gemeinsamer Name**](a-cn.md)                                                 | False     | [**Nach oben**](c-top.md)<br/> |
| [**Länder Code**](a-countrycode.md)                                       | False     | **Organisationseinheit**         |
| [**Länder Name**](a-c.md)                                                 | False     | **Organisationseinheit**         |
| [**Create-Zeitstempel**](a-createtimestamp.md)                              | False     | [**Nach oben**](c-top.md)<br/> |
| [**Standardgruppe**](a-defaultgroup.md)                                     | False     | **Organisationseinheit**         |
| [**Beschreibung**](a-description.md)                                        | False     | [**Nach oben**](c-top.md)<br/> |
| [**Desktop Profil**](a-desktopprofile.md)                                 | False     | **Organisationseinheit**         |
| [**Ziel-Indikator**](a-destinationindicator.md)                     | False     | **Organisationseinheit**         |
| [**Anzeige Name**](a-displayname.md)                                       | False     | [**Nach oben**](c-top.md)<br/> |
| [**Anzeige Name-druckdruck**](a-displaynameprintable.md)                    | False     | [**Nach oben**](c-top.md)<br/> |
| [**DSA-Signatur**](a-dsasignature.md)                                     | False     | [**Nach oben**](c-top.md)<br/> |
| [**DS-Core-propagierungs Daten**](a-dscorepropagationdata.md)                 | False     | [**Nach oben**](c-top.md)<br/> |
| [**Erweiterungs Name**](a-extensionname.md)                                   | False     | [**Nach oben**](c-top.md)<br/> |
| [**Fax-Telefonnummer**](a-facsimiletelephonenumber.md)            | False     | **Organisationseinheit**         |
| [**Fahren**](a-flags.md)                                                    | False     | [**Nach oben**](c-top.md)<br/> |
| [**Aus-Eintrag**](a-fromentry.md)                                           | False     | [**Nach oben**](c-top.md)<br/> |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)               | False     | [**Nach oben**](c-top.md)<br/> |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                   | False     | [**Nach oben**](c-top.md)<br/> |
| [**"F"-Rollen Besitzer**](a-fsmoroleowner.md)                                  | False     | [**Nach oben**](c-top.md)<br/> |
| [**GP-Link**](a-gplink.md)                                                 | False     | **Organisationseinheit**         |
| [**GP-Optionen**](a-gpoptions.md)                                           | False     | **Organisationseinheit**         |
| [**Instanztyp**](a-instancetype.md)                                     | Richtig      | [**Nach oben**](c-top.md)<br/> |
| [**International-ISDN-Number**](a-internationalisdnnumber.md)              | False     | **Organisationseinheit**         |
| [**Is-critical-System-Object**](a-iscriticalsystemobject.md)               | False     | [**Nach oben**](c-top.md)<br/> |
| [**Ist-gelöscht**](a-isdeleted.md)                                           | False     | [**Nach oben**](c-top.md)<br/> |
| [**Is-Member-of-DL**](a-memberof.md)                                       | False     | [**Nach oben**](c-top.md)<br/> |
| [**Is-Privilege-Inhaber**](a-isprivilegeholder.md)                          | False     | [**Nach oben**](c-top.md)<br/> |
| [**Letztes-bekannt/übergeordnetes Element**](a-lastknownparent.md)                              | False     | [**Nach oben**](c-top.md)<br/> |
| [**Lokalitäts Name**](a-l.md)                                                | False     | **Organisationseinheit**         |
| [**Logo**](a-thumbnaillogo.md)                                             | False     | **Organisationseinheit**         |
| [**Verwaltet von**](a-managedby.md)                                           | False     | **Organisationseinheit**         |
| [**Verwaltete Objekte**](a-managedobjects.md)                                 | False     | [**Nach oben**](c-top.md)<br/> |
| [**Verwaltet von**](a-masteredby.md)                                         | False     | [**Nach oben**](c-top.md)<br/> |
| [**Modify-Zeitstempel**](a-modifytimestamp.md)                              | False     | [**Nach oben**](c-top.md)<br/> |
| [**MS-com-partitionsetlink**](a-mscom-partitionsetlink.md)                 | False     | [**Nach oben**](c-top.md)<br/> |
| [**MS-com-userlink**](a-mscom-userlink.md)                                 | False     | [**Nach oben**](c-top.md)<br/> |
| [**MS-com-userpartitionsetlink**](a-mscom-userpartitionsetlink.md)         | False     | **Organisationseinheit**         |
| [**ms-DS-ca-immed-untergeordnete Elemente**](a-msds-approx-immed-subordinates.md) | False     | [**Nach oben**](c-top.md)<br/> |
| [**MS-DS-Konsistenz-untergeordnet-Anzahl**](a-ms-ds-consistencychildcount.md)      | False     | [**Nach oben**](c-top.md)<br/> |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-gemastert von**](a-msds-masteredby.md)                              | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Members-für-AZ-Role-BL**](a-msds-membersforazrolebl.md)           | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-NC-repl-Cursor**](a-msds-ncreplcursors.md)                       | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-NC-repl-Inbound-Nachbarn**](a-msds-ncreplinboundneighbors.md)    | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-NC-repl-Outbound-Nachbarn**](a-msds-ncreploutboundneighbors.md)  | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                         | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)               | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)     | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)     | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)      | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)              | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Tasks-für-AZ-Role-BL**](a-msds-tasksforazrolebl.md)               | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Tasks-für-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)               | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                       | False     | [**Nach oben**](c-top.md)<br/> |
| [**NetBoot-SCP-BL**](a-netbootscpbl.md)                                    | False     | [**Nach oben**](c-top.md)<br/> |
| [**Nicht sicherheitsmitglied-BL**](a-nonsecuritymemberbl.md)                     | False     | [**Nach oben**](c-top.md)<br/> |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                    | Richtig      | [**Nach oben**](c-top.md)<br/> |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                | False     | [**Nach oben**](c-top.md)<br/> |
| [**Objekt-Kategorie**](a-objectcategory.md)                                 | Richtig      | [**Nach oben**](c-top.md)<br/> |
| [**Object-Klasse**](a-objectclass.md)                                       | Richtig      | [**Nach oben**](c-top.md)<br/> |
| [**Objekt-GUID**](a-objectguid.md)                                         | False     | [**Nach oben**](c-top.md)<br/> |
| [**Objekt-Version**](a-objectversion.md)                                   | False     | [**Nach oben**](c-top.md)<br/> |
| [**Organisations Einheits Name**](a-ou.md)                                    | Richtig      | **Organisationseinheit**         |
| [**Andere-bekannte Objekte**](a-otherwellknownobjects.md)                 | False     | [**Nach oben**](c-top.md)<br/> |
| [**Partial-Attribute-löschen-List**](a-partialattributedeletionlist.md)   | False     | [**Nach oben**](c-top.md)<br/> |
| [**Partiell-Attribut Satz**](a-partialattributeset.md)                      | False     | [**Nach oben**](c-top.md)<br/> |
| [**Physical-delivery-Office-Name**](a-physicaldeliveryofficename.md)       | False     | **Organisationseinheit**         |
| [**Mögliche-minderwertig**](a-possibleinferiors.md)                           | False     | [**Nach oben**](c-top.md)<br/> |
| [**Postanschrift**](a-postaladdress.md)                                   | False     | **Organisationseinheit**         |
| [**Postleitzahl**](a-postalcode.md)                                         | False     | **Organisationseinheit**         |
| [**Post-Office-Box**](a-postofficebox.md)                                  | False     | **Organisationseinheit**         |
| [**Bevorzugte Übermittlungs Methode**](a-preferreddeliverymethod.md)              | False     | **Organisationseinheit**         |
| [**Proxy-Objekt Name**](a-proxiedobjectname.md)                          | False     | [**Nach oben**](c-top.md)<br/> |
| [**Proxy Adressen**](a-proxyaddresses.md)                                 | False     | [**Nach oben**](c-top.md)<br/> |
| [**Abfrage-Richtlinie-BL**](a-querypolicybl.md)                                  | False     | [**Nach oben**](c-top.md)<br/> |
| [**RDN**](a-name.md)                                                       | False     | [**Nach oben**](c-top.md)<br/> |
| [**Registrierte Adresse**](a-registeredaddress.md)                           | False     | **Organisationseinheit**         |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                   | False     | [**Nach oben**](c-top.md)<br/> |
| [**REPL-Update-Vector**](a-repluptodatevector.md)                        | False     | [**Nach oben**](c-top.md)<br/> |
| [**Berichte**](a-directreports.md)                                          | False     | [**Nach oben**](c-top.md)<br/> |
| [**Reps-from**](a-repsfrom.md)                                             | False     | [**Nach oben**](c-top.md)<br/> |
| [**Reps-to**](a-repsto.md)                                                 | False     | [**Nach oben**](c-top.md)<br/> |
| [**Novel**](a-revision.md)                                              | False     | [**Nach oben**](c-top.md)<br/> |
| [**SD-Rechte**](a-sdrightseffective.md)                          | False     | [**Nach oben**](c-top.md)<br/> |
| [**Such Handbuch**](a-searchguide.md)                                       | False     | **Organisationseinheit**         |
| [**Siehe auch**](a-seealso.md)                                               | False     | **Organisationseinheit**         |
| [**Server-Reference-BL**](a-serverreferencebl.md)                          | False     | [**Nach oben**](c-top.md)<br/> |
| [**Anzeigen-in-Advanced-nur anzeigen**](a-showinadvancedviewonly.md)              | False     | [**Nach oben**](c-top.md)<br/> |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | False     | [**Nach oben**](c-top.md)<br/> |
| [**State-or-Province-Name**](a-st.md)                                      | False     | **Organisationseinheit**         |
| [**Straße**](a-street.md)                                          | False     | **Organisationseinheit**         |
| [**Struktur-Objekt-Klasse**](a-structuralobjectclass.md)                  | False     | [**Nach oben**](c-top.md)<br/> |
| [**Sub-Refs**](a-subrefs.md)                                               | False     | [**Nach oben**](c-top.md)<br/> |
| [**Subschemasubentry**](a-subschemasubentry.md)                            | False     | [**Nach oben**](c-top.md)<br/> |
| [**SystemFlags**](a-systemflags.md)                                       | False     | [**Nach oben**](c-top.md)<br/> |
| [**Telefonnummer**](a-telephonenumber.md)                               | False     | **Organisationseinheit**         |
| [**Teletex-Terminal-Identifier**](a-teletexterminalidentifier.md)          | False     | **Organisationseinheit**         |
| [**Telex-Nummer**](a-telexnumber.md)                                       | False     | **Organisationseinheit**         |
| [**Text-Country**](a-co.md)                                                | False     | **Organisationseinheit**         |
| [**UPN-Suffixe**](a-upnsuffixes.md)                                       | False     | **Organisationseinheit**         |
| [**Benutzer Kennwort**](a-userpassword.md)                                     | False     | **Organisationseinheit**         |
| [**Die Anwendung wurde geändert.**](a-usnchanged.md)                                         | False     | [**Nach oben**](c-top.md)<br/> |
| [**Von der Anwendung erstellte**](a-usncreated.md)                                         | False     | [**Nach oben**](c-top.md)<br/> |
| [**USA-DSA-letzte-obj-entfernt**](a-usndsalastobjremoved.md)                  | False     | [**Nach oben**](c-top.md)<br/> |
| [**Standort-und standortübergreifende standortübergreifende**](a-usnintersite.md)                                     | False     | [**Nach oben**](c-top.md)<br/> |
| [**"An-Last-obj-REM"**](a-usnlastobjrem.md)                                 | False     | [**Nach oben**](c-top.md)<br/> |
| [**Quell Code Quelle**](a-usnsource.md)                                           | False     | [**Nach oben**](c-top.md)<br/> |
| [**WBEM-Pfad**](a-wbempath.md)                                             | False     | [**Nach oben**](c-top.md)<br/> |
| [**Bekannte Objekte**](a-wellknownobjects.md)                            | False     | [**Nach oben**](c-top.md)<br/> |
| [**Bei Änderung**](a-whenchanged.md)                                       | False     | [**Nach oben**](c-top.md)<br/> |
| [**Bei Erstellung**](a-whencreated.md)                                       | False     | [**Nach oben**](c-top.md)<br/> |
| [**WWW-Homepage**](a-wwwhomepage.md)                                      | False     | [**Nach oben**](c-top.md)<br/> |
| [**WWW-Page-other**](a-url.md)                                             | False     | [**Nach oben**](c-top.md)<br/> |
| [**X121-Adresse**](a-x121address.md)                                       | False     | **Organisationseinheit**         |



## <a name="windows-server-2003-extended-rights"></a>Erweiterte Rechte für Windows Server 2003

Diese Klasse enthält die folgenden erweiterten Rechte für Windows Server 2003:



| Allgemeiner Name                                                |
|------------------------------------------------------------|
| [**Generieren von RSoP-Planning**](r-generate-rsop-planning.md) |
| [**Generieren von RSoP-Protokollierung**](r-generate-rsop-logging.md)   |



## <a name="adam"></a>Adam

-   [Attribute](#adam-attributes)



| Eingabe | Wert |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | False                                                                                                                      |
| Object-Category             | 1                                                                                                                          |
| Default-Object-Category     | \-                                                                                                                         |
| Governs-Id                  | 2.5.6.5                                                                                                                    |
| Standard-ausblenden-Wert        | 0                                                                                                                          |
| RDN-ATT-ID                  | [**Organisations Einheits Name**](a-ou.md)<br/>                                                                        |
| Unterklasse von                 | [**Nach oben**](c-top.md)<br/>                                                                                            |
| Mögliche Vorgesetzten          | [**Domänen-DNS**](c-domaindns.md)-**Organisationseinheiten-**[**Organisations**](c-organization.md)[**Land**](c-country.md) |
| Zusätzlich           | \-                                                                                                                         |
| NT-Security-Descriptor      | o:Bag: schlecht: S:                                                                                                               |
| Standard Sicherheits Beschreibung | d:s:                                                                                                                       |
| System-Flags                | 0x00000010                                                                                                                 |



## <a name="adam-attributes"></a>Adam-Attribute

Diese Klasse enthält die folgenden Attribute für Adam:



| Attribut                                                                   | Obligatorisch. | Abgeleitet von                    |
|-----------------------------------------------------------------------------|-----------|---------------------------------|
| [**Administrator: Beschreibung**](a-admindescription.md)                             | False     | [**Nach oben**](c-top.md)<br/> |
| [**Administrator-Anzeige Name**](a-admindisplayname.md)                            | False     | [**Nach oben**](c-top.md)<br/> |
| [**Zulässige Attribute**](a-allowedattributes.md)                           | False     | [**Nach oben**](c-top.md)<br/> |
| [**Zulässige Attribute-gültig**](a-allowedattributeseffective.md)        | False     | [**Nach oben**](c-top.md)<br/> |
| [**Zulässige, untergeordnete Klassen**](a-allowedchildclasses.md)                      | False     | [**Nach oben**](c-top.md)<br/> |
| [**Zulässig-untergeordnete Klassen-gültig**](a-allowedchildclasseseffective.md)   | False     | [**Nach oben**](c-top.md)<br/> |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)               | False     | [**Nach oben**](c-top.md)<br/> |
| [**Geschäfts Kategorie**](a-businesscategory.md)                             | False     | **Organisationseinheit**         |
| [**Kanonischer Name**](a-canonicalname.md)                                   | False     | [**Nach oben**](c-top.md)<br/> |
| [**Gemeinsamer Name**](a-cn.md)                                                 | False     | [**Nach oben**](c-top.md)<br/> |
| [**Länder Code**](a-countrycode.md)                                       | False     | **Organisationseinheit**         |
| [**Länder Name**](a-c.md)                                                 | False     | **Organisationseinheit**         |
| [**Create-Zeitstempel**](a-createtimestamp.md)                              | False     | [**Nach oben**](c-top.md)<br/> |
| [**Standardgruppe**](a-defaultgroup.md)                                     | False     | **Organisationseinheit**         |
| [**Beschreibung**](a-description.md)                                        | False     | [**Nach oben**](c-top.md)<br/> |
| [**Desktop Profil**](a-desktopprofile.md)                                 | False     | **Organisationseinheit**         |
| [**Ziel-Indikator**](a-destinationindicator.md)                     | False     | **Organisationseinheit**         |
| [**Anzeige Name**](a-displayname.md)                                       | False     | [**Nach oben**](c-top.md)<br/> |
| [**DSA-Signatur**](a-dsasignature.md)                                     | False     | [**Nach oben**](c-top.md)<br/> |
| [**DS-Core-propagierungs Daten**](a-dscorepropagationdata.md)                 | False     | [**Nach oben**](c-top.md)<br/> |
| [**Fax-Telefonnummer**](a-facsimiletelephonenumber.md)            | False     | **Organisationseinheit**         |
| [**Aus-Eintrag**](a-fromentry.md)                                           | False     | [**Nach oben**](c-top.md)<br/> |
| [**"F"-Rollen Besitzer**](a-fsmoroleowner.md)                                  | False     | [**Nach oben**](c-top.md)<br/> |
| [**Instanztyp**](a-instancetype.md)                                     | Richtig      | [**Nach oben**](c-top.md)<br/> |
| [**International-ISDN-Number**](a-internationalisdnnumber.md)              | False     | **Organisationseinheit**         |
| [**Is-critical-System-Object**](a-iscriticalsystemobject.md)               | False     | [**Nach oben**](c-top.md)<br/> |
| [**Ist-gelöscht**](a-isdeleted.md)                                           | False     | [**Nach oben**](c-top.md)<br/> |
| [**Is-Member-of-DL**](a-memberof.md)                                       | False     | [**Nach oben**](c-top.md)<br/> |
| [**Letztes-bekannt/übergeordnetes Element**](a-lastknownparent.md)                              | False     | [**Nach oben**](c-top.md)<br/> |
| [**Lokalitäts Name**](a-l.md)                                                | False     | **Organisationseinheit**         |
| [**Logo**](a-thumbnaillogo.md)                                             | False     | **Organisationseinheit**         |
| [**Verwaltet von**](a-managedby.md)                                           | False     | **Organisationseinheit**         |
| [**Verwaltete Objekte**](a-managedobjects.md)                                 | False     | [**Nach oben**](c-top.md)<br/> |
| [**Verwaltet von**](a-masteredby.md)                                         | False     | [**Nach oben**](c-top.md)<br/> |
| [**Modify-Zeitstempel**](a-modifytimestamp.md)                              | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-ca-immed-untergeordnete Elemente**](a-msds-approx-immed-subordinates.md) | False     | [**Nach oben**](c-top.md)<br/> |
| [**MS-DS-Konsistenz-untergeordnet-Anzahl**](a-ms-ds-consistencychildcount.md)      | False     | [**Nach oben**](c-top.md)<br/> |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-deaktivieren-für-Instanzen-BL**](a-msds-disableforinstancesbl.md)      | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-gemastert von**](a-msds-masteredby.md)                              | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-NC-repl-Cursor**](a-msds-ncreplcursors.md)                       | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-NC-repl-Inbound-Nachbarn**](a-msds-ncreplinboundneighbors.md)    | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-NC-repl-Outbound-Nachbarn**](a-msds-ncreploutboundneighbors.md)  | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)      | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)              | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Service-Account-BL**](a-msds-serviceaccountbl.md)                 | False     | [**Nach oben**](c-top.md)<br/> |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                    | Richtig      | [**Nach oben**](c-top.md)<br/> |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                | False     | [**Nach oben**](c-top.md)<br/> |
| [**Objekt-Kategorie**](a-objectcategory.md)                                 | Richtig      | [**Nach oben**](c-top.md)<br/> |
| [**Object-Klasse**](a-objectclass.md)                                       | Richtig      | [**Nach oben**](c-top.md)<br/> |
| [**Objekt-GUID**](a-objectguid.md)                                         | False     | [**Nach oben**](c-top.md)<br/> |
| [**Objekt-Version**](a-objectversion.md)                                   | False     | [**Nach oben**](c-top.md)<br/> |
| [**Organisations Einheits Name**](a-ou.md)                                    | Richtig      | **Organisationseinheit**         |
| [**Andere-bekannte Objekte**](a-otherwellknownobjects.md)                 | False     | [**Nach oben**](c-top.md)<br/> |
| [**Partial-Attribute-löschen-List**](a-partialattributedeletionlist.md)   | False     | [**Nach oben**](c-top.md)<br/> |
| [**Partiell-Attribut Satz**](a-partialattributeset.md)                      | False     | [**Nach oben**](c-top.md)<br/> |
| [**Physical-delivery-Office-Name**](a-physicaldeliveryofficename.md)       | False     | **Organisationseinheit**         |
| [**Mögliche-minderwertig**](a-possibleinferiors.md)                           | False     | [**Nach oben**](c-top.md)<br/> |
| [**Postanschrift**](a-postaladdress.md)                                   | False     | **Organisationseinheit**         |
| [**Postleitzahl**](a-postalcode.md)                                         | False     | **Organisationseinheit**         |
| [**Post-Office-Box**](a-postofficebox.md)                                  | False     | **Organisationseinheit**         |
| [**Bevorzugte Übermittlungs Methode**](a-preferreddeliverymethod.md)              | False     | **Organisationseinheit**         |
| [**Proxy-Objekt Name**](a-proxiedobjectname.md)                          | False     | [**Nach oben**](c-top.md)<br/> |
| [**Proxy Adressen**](a-proxyaddresses.md)                                 | False     | [**Nach oben**](c-top.md)<br/> |
| [**Abfrage-Richtlinie-BL**](a-querypolicybl.md)                                  | False     | [**Nach oben**](c-top.md)<br/> |
| [**RDN**](a-name.md)                                                       | False     | [**Nach oben**](c-top.md)<br/> |
| [**Registrierte Adresse**](a-registeredaddress.md)                           | False     | **Organisationseinheit**         |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                   | False     | [**Nach oben**](c-top.md)<br/> |
| [**REPL-Update-Vector**](a-repluptodatevector.md)                        | False     | [**Nach oben**](c-top.md)<br/> |
| [**Reps-from**](a-repsfrom.md)                                             | False     | [**Nach oben**](c-top.md)<br/> |
| [**Reps-to**](a-repsto.md)                                                 | False     | [**Nach oben**](c-top.md)<br/> |
| [**Novel**](a-revision.md)                                              | False     | [**Nach oben**](c-top.md)<br/> |
| [**SD-Rechte**](a-sdrightseffective.md)                          | False     | [**Nach oben**](c-top.md)<br/> |
| [**Such Handbuch**](a-searchguide.md)                                       | False     | **Organisationseinheit**         |
| [**Siehe auch**](a-seealso.md)                                               | False     | **Organisationseinheit**         |
| [**Server-Reference-BL**](a-serverreferencebl.md)                          | False     | [**Nach oben**](c-top.md)<br/> |
| [**Anzeigen-in-Advanced-nur anzeigen**](a-showinadvancedviewonly.md)              | False     | [**Nach oben**](c-top.md)<br/> |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | False     | [**Nach oben**](c-top.md)<br/> |
| [**State-or-Province-Name**](a-st.md)                                      | False     | **Organisationseinheit**         |
| [**Straße**](a-street.md)                                          | False     | **Organisationseinheit**         |
| [**Struktur-Objekt-Klasse**](a-structuralobjectclass.md)                  | False     | [**Nach oben**](c-top.md)<br/> |
| [**Sub-Refs**](a-subrefs.md)                                               | False     | [**Nach oben**](c-top.md)<br/> |
| [**Subschemasubentry**](a-subschemasubentry.md)                            | False     | [**Nach oben**](c-top.md)<br/> |
| [**SystemFlags**](a-systemflags.md)                                       | False     | [**Nach oben**](c-top.md)<br/> |
| [**Telefonnummer**](a-telephonenumber.md)                               | False     | **Organisationseinheit**         |
| [**Teletex-Terminal-Identifier**](a-teletexterminalidentifier.md)          | False     | **Organisationseinheit**         |
| [**Telex-Nummer**](a-telexnumber.md)                                       | False     | **Organisationseinheit**         |
| [**Text-Country**](a-co.md)                                                | False     | **Organisationseinheit**         |
| [**UPN-Suffixe**](a-upnsuffixes.md)                                       | False     | **Organisationseinheit**         |
| [**Benutzer Kennwort**](a-userpassword.md)                                     | False     | **Organisationseinheit**         |
| [**Die Anwendung wurde geändert.**](a-usnchanged.md)                                         | False     | [**Nach oben**](c-top.md)<br/> |
| [**Von der Anwendung erstellte**](a-usncreated.md)                                         | False     | [**Nach oben**](c-top.md)<br/> |
| [**USA-DSA-letzte-obj-entfernt**](a-usndsalastobjremoved.md)                  | False     | [**Nach oben**](c-top.md)<br/> |
| [**Standort-und standortübergreifende standortübergreifende**](a-usnintersite.md)                                     | False     | [**Nach oben**](c-top.md)<br/> |
| [**"An-Last-obj-REM"**](a-usnlastobjrem.md)                                 | False     | [**Nach oben**](c-top.md)<br/> |
| [**Quell Code Quelle**](a-usnsource.md)                                           | False     | [**Nach oben**](c-top.md)<br/> |
| [**WBEM-Pfad**](a-wbempath.md)                                             | False     | [**Nach oben**](c-top.md)<br/> |
| [**Bekannte Objekte**](a-wellknownobjects.md)                            | False     | [**Nach oben**](c-top.md)<br/> |
| [**Bei Änderung**](a-whenchanged.md)                                       | False     | [**Nach oben**](c-top.md)<br/> |
| [**Bei Erstellung**](a-whencreated.md)                                       | False     | [**Nach oben**](c-top.md)<br/> |
| [**WWW-Homepage**](a-wwwhomepage.md)                                      | False     | [**Nach oben**](c-top.md)<br/> |
| [**WWW-Page-other**](a-url.md)                                             | False     | [**Nach oben**](c-top.md)<br/> |
| [**X121-Adresse**](a-x121address.md)                                       | False     | **Organisationseinheit**         |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2

-   [Attribute](#windows-server-2003-r2-attributes)
-   [Erweiterte Rechte](#windows-server-2003-r2-extended-rights)



| Eingabe | Wert |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | False                                                                                                                                                                                                                                                                                                                                                                         |
| Object-Category             | 1                                                                                                                                                                                                                                                                                                                                                                             |
| Default-Object-Category     | \-                                                                                                                                                                                                                                                                                                                                                                            |
| Governs-Id                  | 2.5.6.5                                                                                                                                                                                                                                                                                                                                                                       |
| Standard-ausblenden-Wert        | 0                                                                                                                                                                                                                                                                                                                                                                             |
| RDN-ATT-ID                  | [**Organisations Einheits Name**](a-ou.md)<br/>                                                                                                                                                                                                                                                                                                                           |
| Unterklasse von                 | [**Nach oben**](c-top.md)<br/>                                                                                                                                                                                                                                                                                                                                               |
| Mögliche Vorgesetzten          | [**Domänen-DNS**](c-domaindns.md)-**Organisationseinheiten-**[**Organisations**](c-organization.md)[**Land**](c-country.md)                                                                                                                                                                                                                                                    |
| Zusätzlich           | \-                                                                                                                                                                                                                                                                                                                                                                            |
| NT-Security-Descriptor      | o:Bag: schlecht: S:                                                                                                                                                                                                                                                                                                                                                                  |
| Standard Sicherheits Beschreibung | D: (A;; Rpwpcrccdclclorcwowdsddtsw;;; SY) (A;; rpwpcrccdclclorcwowdsddtsw;;;D A) (OA;; CCDC; bf967a86-0de6-11D0-A285-00aa003049e2;; AO) (OA;; CCDC; bf967aba-0de6-11D0-A285-00aa003049e2;; AO) (OA;; CCDC; bf967a9c-0de6-11D0-A285-00aa003049e2;; AO) (OA;; CCDC; bf967aa8-0de6-11D0-A285-00aa003049e2;; PO) (A;; Rplclorc;;; Au) (A;; Lcrplorc;;; ED) (OA;; CCDC; 4828cc14-1437-45bc-9b07-ad6f 015e5f 28;; OS |
| System-Flags                | 0x00000010                                                                                                                                                                                                                                                                                                                                                                    |



## <a name="windows-server-2003-r2-attributes"></a>Windows Server 2003 R2-Attribute

Diese Klasse enthält die folgenden Attribute für Windows Server 2003 R2:



| Attribut                                                                   | Obligatorisch. | Abgeleitet von                    |
|-----------------------------------------------------------------------------|-----------|---------------------------------|
| [**Administrator: Beschreibung**](a-admindescription.md)                             | False     | [**Nach oben**](c-top.md)<br/> |
| [**Administrator-Anzeige Name**](a-admindisplayname.md)                            | False     | [**Nach oben**](c-top.md)<br/> |
| [**Zulässige Attribute**](a-allowedattributes.md)                           | False     | [**Nach oben**](c-top.md)<br/> |
| [**Zulässige Attribute-gültig**](a-allowedattributeseffective.md)        | False     | [**Nach oben**](c-top.md)<br/> |
| [**Zulässige, untergeordnete Klassen**](a-allowedchildclasses.md)                      | False     | [**Nach oben**](c-top.md)<br/> |
| [**Zulässig-untergeordnete Klassen-gültig**](a-allowedchildclasseseffective.md)   | False     | [**Nach oben**](c-top.md)<br/> |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)               | False     | [**Nach oben**](c-top.md)<br/> |
| [**Geschäfts Kategorie**](a-businesscategory.md)                             | False     | **Organisationseinheit**         |
| [**Kanonischer Name**](a-canonicalname.md)                                   | False     | [**Nach oben**](c-top.md)<br/> |
| [**Gemeinsamer Name**](a-cn.md)                                                 | False     | [**Nach oben**](c-top.md)<br/> |
| [**Länder Code**](a-countrycode.md)                                       | False     | **Organisationseinheit**         |
| [**Länder Name**](a-c.md)                                                 | False     | **Organisationseinheit**         |
| [**Create-Zeitstempel**](a-createtimestamp.md)                              | False     | [**Nach oben**](c-top.md)<br/> |
| [**Standardgruppe**](a-defaultgroup.md)                                     | False     | **Organisationseinheit**         |
| [**Beschreibung**](a-description.md)                                        | False     | [**Nach oben**](c-top.md)<br/> |
| [**Desktop Profil**](a-desktopprofile.md)                                 | False     | **Organisationseinheit**         |
| [**Ziel-Indikator**](a-destinationindicator.md)                     | False     | **Organisationseinheit**         |
| [**Anzeige Name**](a-displayname.md)                                       | False     | [**Nach oben**](c-top.md)<br/> |
| [**Anzeige Name-druckdruck**](a-displaynameprintable.md)                    | False     | [**Nach oben**](c-top.md)<br/> |
| [**DSA-Signatur**](a-dsasignature.md)                                     | False     | [**Nach oben**](c-top.md)<br/> |
| [**DS-Core-propagierungs Daten**](a-dscorepropagationdata.md)                 | False     | [**Nach oben**](c-top.md)<br/> |
| [**Erweiterungs Name**](a-extensionname.md)                                   | False     | [**Nach oben**](c-top.md)<br/> |
| [**Fax-Telefonnummer**](a-facsimiletelephonenumber.md)            | False     | **Organisationseinheit**         |
| [**Fahren**](a-flags.md)                                                    | False     | [**Nach oben**](c-top.md)<br/> |
| [**Aus-Eintrag**](a-fromentry.md)                                           | False     | [**Nach oben**](c-top.md)<br/> |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)               | False     | [**Nach oben**](c-top.md)<br/> |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                   | False     | [**Nach oben**](c-top.md)<br/> |
| [**"F"-Rollen Besitzer**](a-fsmoroleowner.md)                                  | False     | [**Nach oben**](c-top.md)<br/> |
| [**GP-Link**](a-gplink.md)                                                 | False     | **Organisationseinheit**         |
| [**GP-Optionen**](a-gpoptions.md)                                           | False     | **Organisationseinheit**         |
| [**Instanztyp**](a-instancetype.md)                                     | Richtig      | [**Nach oben**](c-top.md)<br/> |
| [**International-ISDN-Number**](a-internationalisdnnumber.md)              | False     | **Organisationseinheit**         |
| [**Is-critical-System-Object**](a-iscriticalsystemobject.md)               | False     | [**Nach oben**](c-top.md)<br/> |
| [**Ist-gelöscht**](a-isdeleted.md)                                           | False     | [**Nach oben**](c-top.md)<br/> |
| [**Is-Member-of-DL**](a-memberof.md)                                       | False     | [**Nach oben**](c-top.md)<br/> |
| [**Is-Privilege-Inhaber**](a-isprivilegeholder.md)                          | False     | [**Nach oben**](c-top.md)<br/> |
| [**Letztes-bekannt/übergeordnetes Element**](a-lastknownparent.md)                              | False     | [**Nach oben**](c-top.md)<br/> |
| [**Lokalitäts Name**](a-l.md)                                                | False     | **Organisationseinheit**         |
| [**Logo**](a-thumbnaillogo.md)                                             | False     | **Organisationseinheit**         |
| [**Verwaltet von**](a-managedby.md)                                           | False     | **Organisationseinheit**         |
| [**Verwaltete Objekte**](a-managedobjects.md)                                 | False     | [**Nach oben**](c-top.md)<br/> |
| [**Verwaltet von**](a-masteredby.md)                                         | False     | [**Nach oben**](c-top.md)<br/> |
| [**Modify-Zeitstempel**](a-modifytimestamp.md)                              | False     | [**Nach oben**](c-top.md)<br/> |
| [**MS-com-partitionsetlink**](a-mscom-partitionsetlink.md)                 | False     | [**Nach oben**](c-top.md)<br/> |
| [**MS-com-userlink**](a-mscom-userlink.md)                                 | False     | [**Nach oben**](c-top.md)<br/> |
| [**MS-com-userpartitionsetlink**](a-mscom-userpartitionsetlink.md)         | False     | **Organisationseinheit**         |
| [**MS-DFSR-computerreferencebl**](a-msdfsr-computerreferencebl.md)         | False     | [**Nach oben**](c-top.md)<br/> |
| [**MS-DFSR-mitgliedreferencebl**](a-msdfsr-memberreferencebl.md)             | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-ca-immed-untergeordnete Elemente**](a-msds-approx-immed-subordinates.md) | False     | [**Nach oben**](c-top.md)<br/> |
| [**MS-DS-Konsistenz-untergeordnet-Anzahl**](a-ms-ds-consistencychildcount.md)      | False     | [**Nach oben**](c-top.md)<br/> |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-gemastert von**](a-msds-masteredby.md)                              | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Members-für-AZ-Role-BL**](a-msds-membersforazrolebl.md)           | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-NC-repl-Cursor**](a-msds-ncreplcursors.md)                       | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-NC-repl-Inbound-Nachbarn**](a-msds-ncreplinboundneighbors.md)    | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-NC-repl-Outbound-Nachbarn**](a-msds-ncreploutboundneighbors.md)  | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                         | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)               | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)     | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)     | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)      | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)              | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Tasks-für-AZ-Role-BL**](a-msds-tasksforazrolebl.md)               | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Tasks-für-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)               | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                       | False     | [**Nach oben**](c-top.md)<br/> |
| [**msSFU-30-POSIX-Member-of**](a-mssfu30posixmemberof.md)                  | False     | [**Nach oben**](c-top.md)<br/> |
| [**NetBoot-SCP-BL**](a-netbootscpbl.md)                                    | False     | [**Nach oben**](c-top.md)<br/> |
| [**Nicht sicherheitsmitglied-BL**](a-nonsecuritymemberbl.md)                     | False     | [**Nach oben**](c-top.md)<br/> |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                    | Richtig      | [**Nach oben**](c-top.md)<br/> |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                | False     | [**Nach oben**](c-top.md)<br/> |
| [**Objekt-Kategorie**](a-objectcategory.md)                                 | Richtig      | [**Nach oben**](c-top.md)<br/> |
| [**Object-Klasse**](a-objectclass.md)                                       | Richtig      | [**Nach oben**](c-top.md)<br/> |
| [**Objekt-GUID**](a-objectguid.md)                                         | False     | [**Nach oben**](c-top.md)<br/> |
| [**Objekt-Version**](a-objectversion.md)                                   | False     | [**Nach oben**](c-top.md)<br/> |
| [**Organisations Einheits Name**](a-ou.md)                                    | Richtig      | **Organisationseinheit**         |
| [**Andere-bekannte Objekte**](a-otherwellknownobjects.md)                 | False     | [**Nach oben**](c-top.md)<br/> |
| [**Partial-Attribute-löschen-List**](a-partialattributedeletionlist.md)   | False     | [**Nach oben**](c-top.md)<br/> |
| [**Partiell-Attribut Satz**](a-partialattributeset.md)                      | False     | [**Nach oben**](c-top.md)<br/> |
| [**Physical-delivery-Office-Name**](a-physicaldeliveryofficename.md)       | False     | **Organisationseinheit**         |
| [**Mögliche-minderwertig**](a-possibleinferiors.md)                           | False     | [**Nach oben**](c-top.md)<br/> |
| [**Postanschrift**](a-postaladdress.md)                                   | False     | **Organisationseinheit**         |
| [**Postleitzahl**](a-postalcode.md)                                         | False     | **Organisationseinheit**         |
| [**Post-Office-Box**](a-postofficebox.md)                                  | False     | **Organisationseinheit**         |
| [**Bevorzugte Übermittlungs Methode**](a-preferreddeliverymethod.md)              | False     | **Organisationseinheit**         |
| [**Proxy-Objekt Name**](a-proxiedobjectname.md)                          | False     | [**Nach oben**](c-top.md)<br/> |
| [**Proxy Adressen**](a-proxyaddresses.md)                                 | False     | [**Nach oben**](c-top.md)<br/> |
| [**Abfrage-Richtlinie-BL**](a-querypolicybl.md)                                  | False     | [**Nach oben**](c-top.md)<br/> |
| [**RDN**](a-name.md)                                                       | False     | [**Nach oben**](c-top.md)<br/> |
| [**Registrierte Adresse**](a-registeredaddress.md)                           | False     | **Organisationseinheit**         |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                   | False     | [**Nach oben**](c-top.md)<br/> |
| [**REPL-Update-Vector**](a-repluptodatevector.md)                        | False     | [**Nach oben**](c-top.md)<br/> |
| [**Berichte**](a-directreports.md)                                          | False     | [**Nach oben**](c-top.md)<br/> |
| [**Reps-from**](a-repsfrom.md)                                             | False     | [**Nach oben**](c-top.md)<br/> |
| [**Reps-to**](a-repsto.md)                                                 | False     | [**Nach oben**](c-top.md)<br/> |
| [**Novel**](a-revision.md)                                              | False     | [**Nach oben**](c-top.md)<br/> |
| [**SD-Rechte**](a-sdrightseffective.md)                          | False     | [**Nach oben**](c-top.md)<br/> |
| [**Such Handbuch**](a-searchguide.md)                                       | False     | **Organisationseinheit**         |
| [**Siehe auch**](a-seealso.md)                                               | False     | **Organisationseinheit**         |
| [**Server-Reference-BL**](a-serverreferencebl.md)                          | False     | [**Nach oben**](c-top.md)<br/> |
| [**Anzeigen-in-Advanced-nur anzeigen**](a-showinadvancedviewonly.md)              | False     | [**Nach oben**](c-top.md)<br/> |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | False     | [**Nach oben**](c-top.md)<br/> |
| [**State-or-Province-Name**](a-st.md)                                      | False     | **Organisationseinheit**         |
| [**Straße**](a-street.md)                                          | False     | **Organisationseinheit**         |
| [**Struktur-Objekt-Klasse**](a-structuralobjectclass.md)                  | False     | [**Nach oben**](c-top.md)<br/> |
| [**Sub-Refs**](a-subrefs.md)                                               | False     | [**Nach oben**](c-top.md)<br/> |
| [**Subschemasubentry**](a-subschemasubentry.md)                            | False     | [**Nach oben**](c-top.md)<br/> |
| [**SystemFlags**](a-systemflags.md)                                       | False     | [**Nach oben**](c-top.md)<br/> |
| [**Telefonnummer**](a-telephonenumber.md)                               | False     | **Organisationseinheit**         |
| [**Teletex-Terminal-Identifier**](a-teletexterminalidentifier.md)          | False     | **Organisationseinheit**         |
| [**Telex-Nummer**](a-telexnumber.md)                                       | False     | **Organisationseinheit**         |
| [**Text-Country**](a-co.md)                                                | False     | **Organisationseinheit**         |
| [**UPN-Suffixe**](a-upnsuffixes.md)                                       | False     | **Organisationseinheit**         |
| [**Benutzer Kennwort**](a-userpassword.md)                                     | False     | **Organisationseinheit**         |
| [**Die Anwendung wurde geändert.**](a-usnchanged.md)                                         | False     | [**Nach oben**](c-top.md)<br/> |
| [**Von der Anwendung erstellte**](a-usncreated.md)                                         | False     | [**Nach oben**](c-top.md)<br/> |
| [**USA-DSA-letzte-obj-entfernt**](a-usndsalastobjremoved.md)                  | False     | [**Nach oben**](c-top.md)<br/> |
| [**Standort-und standortübergreifende standortübergreifende**](a-usnintersite.md)                                     | False     | [**Nach oben**](c-top.md)<br/> |
| [**"An-Last-obj-REM"**](a-usnlastobjrem.md)                                 | False     | [**Nach oben**](c-top.md)<br/> |
| [**Quell Code Quelle**](a-usnsource.md)                                           | False     | [**Nach oben**](c-top.md)<br/> |
| [**WBEM-Pfad**](a-wbempath.md)                                             | False     | [**Nach oben**](c-top.md)<br/> |
| [**Bekannte Objekte**](a-wellknownobjects.md)                            | False     | [**Nach oben**](c-top.md)<br/> |
| [**Bei Änderung**](a-whenchanged.md)                                       | False     | [**Nach oben**](c-top.md)<br/> |
| [**Bei Erstellung**](a-whencreated.md)                                       | False     | [**Nach oben**](c-top.md)<br/> |
| [**WWW-Homepage**](a-wwwhomepage.md)                                      | False     | [**Nach oben**](c-top.md)<br/> |
| [**WWW-Page-other**](a-url.md)                                             | False     | [**Nach oben**](c-top.md)<br/> |
| [**X121-Adresse**](a-x121address.md)                                       | False     | **Organisationseinheit**         |



## <a name="windows-server-2003-r2-extended-rights"></a>Erweiterte Rechte für Windows Server 2003 R2

Diese Klasse enthält die folgenden erweiterten Rechte für Windows Server 2003 R2:



| Allgemeiner Name                                                |
|------------------------------------------------------------|
| [**Generieren von RSoP-Planning**](r-generate-rsop-planning.md) |
| [**Generieren von RSoP-Protokollierung**](r-generate-rsop-logging.md)   |



## <a name="windows-server-2008"></a>Windows Server 2008

-   [Attribute](#windows-server-2008-attributes)
-   [Erweiterte Rechte](#windows-server-2008-extended-rights)



| Eingabe | Wert |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | False                                                                                                                                                                                                                                                                                                                                                                         |
| Object-Category             | 1                                                                                                                                                                                                                                                                                                                                                                             |
| Default-Object-Category     | \-                                                                                                                                                                                                                                                                                                                                                                            |
| Governs-Id                  | 2.5.6.5                                                                                                                                                                                                                                                                                                                                                                       |
| Standard-ausblenden-Wert        | 0                                                                                                                                                                                                                                                                                                                                                                             |
| RDN-ATT-ID                  | [**Organisations Einheits Name**](a-ou.md)<br/>                                                                                                                                                                                                                                                                                                                           |
| Unterklasse von                 | [**Nach oben**](c-top.md)<br/>                                                                                                                                                                                                                                                                                                                                               |
| Mögliche Vorgesetzten          | [**Domänen-DNS**](c-domaindns.md)-**Organisationseinheiten-**[**Organisations**](c-organization.md)[**Land**](c-country.md)                                                                                                                                                                                                                                                    |
| Zusätzlich           | \-                                                                                                                                                                                                                                                                                                                                                                            |
| NT-Security-Descriptor      | o:Bag: schlecht: S:                                                                                                                                                                                                                                                                                                                                                                  |
| Standard Sicherheits Beschreibung | D: (A;; Rpwpcrccdclclorcwowdsddtsw;;; SY) (A;; rpwpcrccdclclorcwowdsddtsw;;;D A) (OA;; CCDC; bf967a86-0de6-11D0-A285-00aa003049e2;; AO) (OA;; CCDC; bf967aba-0de6-11D0-A285-00aa003049e2;; AO) (OA;; CCDC; bf967a9c-0de6-11D0-A285-00aa003049e2;; AO) (OA;; CCDC; bf967aa8-0de6-11D0-A285-00aa003049e2;; PO) (A;; Rplclorc;;; Au) (A;; Lcrplorc;;; ED) (OA;; CCDC; 4828cc14-1437-45bc-9b07-ad6f 015e5f 28;; OS |
| System-Flags                | 0x00000010                                                                                                                                                                                                                                                                                                                                                                    |



## <a name="windows-server-2008-attributes"></a>Windows Server 2008-Attribute

Diese Klasse enthält die folgenden Attribute für Windows Server 2008:



| Attribut                                                                      | Obligatorisch. | Abgeleitet von                    |
|--------------------------------------------------------------------------------|-----------|---------------------------------|
| [**Administrator: Beschreibung**](a-admindescription.md)                                | False     | [**Nach oben**](c-top.md)<br/> |
| [**Administrator-Anzeige Name**](a-admindisplayname.md)                               | False     | [**Nach oben**](c-top.md)<br/> |
| [**Zulässige Attribute**](a-allowedattributes.md)                              | False     | [**Nach oben**](c-top.md)<br/> |
| [**Zulässige Attribute-gültig**](a-allowedattributeseffective.md)           | False     | [**Nach oben**](c-top.md)<br/> |
| [**Zulässige, untergeordnete Klassen**](a-allowedchildclasses.md)                         | False     | [**Nach oben**](c-top.md)<br/> |
| [**Zulässig-untergeordnete Klassen-gültig**](a-allowedchildclasseseffective.md)      | False     | [**Nach oben**](c-top.md)<br/> |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                  | False     | [**Nach oben**](c-top.md)<br/> |
| [**Geschäfts Kategorie**](a-businesscategory.md)                                | False     | **Organisationseinheit**         |
| [**Kanonischer Name**](a-canonicalname.md)                                      | False     | [**Nach oben**](c-top.md)<br/> |
| [**Gemeinsamer Name**](a-cn.md)                                                    | False     | [**Nach oben**](c-top.md)<br/> |
| [**Länder Code**](a-countrycode.md)                                          | False     | **Organisationseinheit**         |
| [**Länder Name**](a-c.md)                                                    | False     | **Organisationseinheit**         |
| [**Create-Zeitstempel**](a-createtimestamp.md)                                 | False     | [**Nach oben**](c-top.md)<br/> |
| [**Standardgruppe**](a-defaultgroup.md)                                        | False     | **Organisationseinheit**         |
| [**Beschreibung**](a-description.md)                                           | False     | [**Nach oben**](c-top.md)<br/> |
| [**Desktop Profil**](a-desktopprofile.md)                                    | False     | **Organisationseinheit**         |
| [**Ziel-Indikator**](a-destinationindicator.md)                        | False     | **Organisationseinheit**         |
| [**Anzeige Name**](a-displayname.md)                                          | False     | [**Nach oben**](c-top.md)<br/> |
| [**Anzeige Name-druckdruck**](a-displaynameprintable.md)                       | False     | [**Nach oben**](c-top.md)<br/> |
| [**DSA-Signatur**](a-dsasignature.md)                                        | False     | [**Nach oben**](c-top.md)<br/> |
| [**DS-Core-propagierungs Daten**](a-dscorepropagationdata.md)                    | False     | [**Nach oben**](c-top.md)<br/> |
| [**Erweiterungs Name**](a-extensionname.md)                                      | False     | [**Nach oben**](c-top.md)<br/> |
| [**Fax-Telefonnummer**](a-facsimiletelephonenumber.md)               | False     | **Organisationseinheit**         |
| [**Fahren**](a-flags.md)                                                       | False     | [**Nach oben**](c-top.md)<br/> |
| [**Aus-Eintrag**](a-fromentry.md)                                              | False     | [**Nach oben**](c-top.md)<br/> |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                  | False     | [**Nach oben**](c-top.md)<br/> |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                      | False     | [**Nach oben**](c-top.md)<br/> |
| [**"F"-Rollen Besitzer**](a-fsmoroleowner.md)                                     | False     | [**Nach oben**](c-top.md)<br/> |
| [**GP-Link**](a-gplink.md)                                                    | False     | **Organisationseinheit**         |
| [**GP-Optionen**](a-gpoptions.md)                                              | False     | **Organisationseinheit**         |
| [**Instanztyp**](a-instancetype.md)                                        | Richtig      | [**Nach oben**](c-top.md)<br/> |
| [**International-ISDN-Number**](a-internationalisdnnumber.md)                 | False     | **Organisationseinheit**         |
| [**Is-critical-System-Object**](a-iscriticalsystemobject.md)                  | False     | [**Nach oben**](c-top.md)<br/> |
| [**Ist-gelöscht**](a-isdeleted.md)                                              | False     | [**Nach oben**](c-top.md)<br/> |
| [**Is-Member-of-DL**](a-memberof.md)                                          | False     | [**Nach oben**](c-top.md)<br/> |
| [**Is-Privilege-Inhaber**](a-isprivilegeholder.md)                             | False     | [**Nach oben**](c-top.md)<br/> |
| [**Letztes-bekannt/übergeordnetes Element**](a-lastknownparent.md)                                 | False     | [**Nach oben**](c-top.md)<br/> |
| [**Lokalitäts Name**](a-l.md)                                                   | False     | **Organisationseinheit**         |
| [**Logo**](a-thumbnaillogo.md)                                                | False     | **Organisationseinheit**         |
| [**Verwaltet von**](a-managedby.md)                                              | False     | **Organisationseinheit**         |
| [**Verwaltete Objekte**](a-managedobjects.md)                                    | False     | [**Nach oben**](c-top.md)<br/> |
| [**Verwaltet von**](a-masteredby.md)                                            | False     | [**Nach oben**](c-top.md)<br/> |
| [**Modify-Zeitstempel**](a-modifytimestamp.md)                                 | False     | [**Nach oben**](c-top.md)<br/> |
| [**MS-com-partitionsetlink**](a-mscom-partitionsetlink.md)                    | False     | [**Nach oben**](c-top.md)<br/> |
| [**MS-com-userlink**](a-mscom-userlink.md)                                    | False     | [**Nach oben**](c-top.md)<br/> |
| [**MS-com-userpartitionsetlink**](a-mscom-userpartitionsetlink.md)            | False     | **Organisationseinheit**         |
| [**MS-DFSR-computerreferencebl**](a-msdfsr-computerreferencebl.md)            | False     | [**Nach oben**](c-top.md)<br/> |
| [**MS-DFSR-mitgliedreferencebl**](a-msdfsr-memberreferencebl.md)                | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-ca-immed-untergeordnete Elemente**](a-msds-approx-immed-subordinates.md)    | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-authentieredto-accountlist**](a-msds-authenticatedtoaccountlist.md) | False     | [**Nach oben**](c-top.md)<br/> |
| [**MS-DS-Konsistenz-untergeordnet-Anzahl**](a-ms-ds-consistencychildcount.md)         | False     | [**Nach oben**](c-top.md)<br/> |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                      | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-is-Domain-for**](a-msds-isdomainfor.md)                              | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-is-full-Replica-for**](a-msds-isfullreplicafor.md)                   | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-is-Partial-Replica-for**](a-msds-ispartialreplicafor.md)             | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-krbtgt-Link-BL**](a-msds-krbtgtlinkbl.md)                            | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-gemastert von**](a-msds-masteredby.md)                                 | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Members-für-AZ-Role-BL**](a-msds-membersforazrolebl.md)              | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-NC-repl-Cursor**](a-msds-ncreplcursors.md)                          | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-NC-repl-Inbound-Nachbarn**](a-msds-ncreplinboundneighbors.md)       | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-NC-repl-Outbound-Nachbarn**](a-msds-ncreploutboundneighbors.md)     | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)  | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-NC-Typ**](a-msds-nctype.md)                                         | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                            | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                  | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)        | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)        | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                           | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-PSO-angewendet**](a-msds-psoapplied.md)                                 | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)         | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                 | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-offengelegt-DSAs**](a-msds-revealeddsas.md)                             | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-enthüllt-List-BL**](a-msds-revealedlistbl.md)                        | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Tasks-für-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                  | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Tasks-für-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                  | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                          | False     | [**Nach oben**](c-top.md)<br/> |
| [**msSFU-30-POSIX-Member-of**](a-mssfu30posixmemberof.md)                     | False     | [**Nach oben**](c-top.md)<br/> |
| [**NetBoot-SCP-BL**](a-netbootscpbl.md)                                       | False     | [**Nach oben**](c-top.md)<br/> |
| [**Nicht sicherheitsmitglied-BL**](a-nonsecuritymemberbl.md)                        | False     | [**Nach oben**](c-top.md)<br/> |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                       | Richtig      | [**Nach oben**](c-top.md)<br/> |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                   | False     | [**Nach oben**](c-top.md)<br/> |
| [**Objekt-Kategorie**](a-objectcategory.md)                                    | Richtig      | [**Nach oben**](c-top.md)<br/> |
| [**Object-Klasse**](a-objectclass.md)                                          | Richtig      | [**Nach oben**](c-top.md)<br/> |
| [**Objekt-GUID**](a-objectguid.md)                                            | False     | [**Nach oben**](c-top.md)<br/> |
| [**Objekt-Version**](a-objectversion.md)                                      | False     | [**Nach oben**](c-top.md)<br/> |
| [**Organisations Einheits Name**](a-ou.md)                                       | Richtig      | **Organisationseinheit**         |
| [**Andere-bekannte Objekte**](a-otherwellknownobjects.md)                    | False     | [**Nach oben**](c-top.md)<br/> |
| [**Partial-Attribute-löschen-List**](a-partialattributedeletionlist.md)      | False     | [**Nach oben**](c-top.md)<br/> |
| [**Partiell-Attribut Satz**](a-partialattributeset.md)                         | False     | [**Nach oben**](c-top.md)<br/> |
| [**Physical-delivery-Office-Name**](a-physicaldeliveryofficename.md)          | False     | **Organisationseinheit**         |
| [**Mögliche-minderwertig**](a-possibleinferiors.md)                              | False     | [**Nach oben**](c-top.md)<br/> |
| [**Postanschrift**](a-postaladdress.md)                                      | False     | **Organisationseinheit**         |
| [**Postleitzahl**](a-postalcode.md)                                            | False     | **Organisationseinheit**         |
| [**Post-Office-Box**](a-postofficebox.md)                                     | False     | **Organisationseinheit**         |
| [**Bevorzugte Übermittlungs Methode**](a-preferreddeliverymethod.md)                 | False     | **Organisationseinheit**         |
| [**Proxy-Objekt Name**](a-proxiedobjectname.md)                             | False     | [**Nach oben**](c-top.md)<br/> |
| [**Proxy Adressen**](a-proxyaddresses.md)                                    | False     | [**Nach oben**](c-top.md)<br/> |
| [**Abfrage-Richtlinie-BL**](a-querypolicybl.md)                                     | False     | [**Nach oben**](c-top.md)<br/> |
| [**RDN**](a-name.md)                                                          | False     | [**Nach oben**](c-top.md)<br/> |
| [**Registrierte Adresse**](a-registeredaddress.md)                              | False     | **Organisationseinheit**         |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                      | False     | [**Nach oben**](c-top.md)<br/> |
| [**REPL-Update-Vector**](a-repluptodatevector.md)                           | False     | [**Nach oben**](c-top.md)<br/> |
| [**Berichte**](a-directreports.md)                                             | False     | [**Nach oben**](c-top.md)<br/> |
| [**Reps-from**](a-repsfrom.md)                                                | False     | [**Nach oben**](c-top.md)<br/> |
| [**Reps-to**](a-repsto.md)                                                    | False     | [**Nach oben**](c-top.md)<br/> |
| [**Novel**](a-revision.md)                                                 | False     | [**Nach oben**](c-top.md)<br/> |
| [**SD-Rechte**](a-sdrightseffective.md)                             | False     | [**Nach oben**](c-top.md)<br/> |
| [**Such Handbuch**](a-searchguide.md)                                          | False     | **Organisationseinheit**         |
| [**Siehe auch**](a-seealso.md)                                                  | False     | **Organisationseinheit**         |
| [**Server-Reference-BL**](a-serverreferencebl.md)                             | False     | [**Nach oben**](c-top.md)<br/> |
| [**Anzeigen-in-Advanced-nur anzeigen**](a-showinadvancedviewonly.md)                 | False     | [**Nach oben**](c-top.md)<br/> |
| [**Site-Object-BL**](a-siteobjectbl.md)                                       | False     | [**Nach oben**](c-top.md)<br/> |
| [**State-or-Province-Name**](a-st.md)                                         | False     | **Organisationseinheit**         |
| [**Straße**](a-street.md)                                             | False     | **Organisationseinheit**         |
| [**Struktur-Objekt-Klasse**](a-structuralobjectclass.md)                     | False     | [**Nach oben**](c-top.md)<br/> |
| [**Sub-Refs**](a-subrefs.md)                                                  | False     | [**Nach oben**](c-top.md)<br/> |
| [**Subschemasubentry**](a-subschemasubentry.md)                               | False     | [**Nach oben**](c-top.md)<br/> |
| [**SystemFlags**](a-systemflags.md)                                          | False     | [**Nach oben**](c-top.md)<br/> |
| [**Telefonnummer**](a-telephonenumber.md)                                  | False     | **Organisationseinheit**         |
| [**Teletex-Terminal-Identifier**](a-teletexterminalidentifier.md)             | False     | **Organisationseinheit**         |
| [**Telex-Nummer**](a-telexnumber.md)                                          | False     | **Organisationseinheit**         |
| [**Text-Country**](a-co.md)                                                   | False     | **Organisationseinheit**         |
| [**UPN-Suffixe**](a-upnsuffixes.md)                                          | False     | **Organisationseinheit**         |
| [**Benutzer Kennwort**](a-userpassword.md)                                        | False     | **Organisationseinheit**         |
| [**Die Anwendung wurde geändert.**](a-usnchanged.md)                                            | False     | [**Nach oben**](c-top.md)<br/> |
| [**Von der Anwendung erstellte**](a-usncreated.md)                                            | False     | [**Nach oben**](c-top.md)<br/> |
| [**USA-DSA-letzte-obj-entfernt**](a-usndsalastobjremoved.md)                     | False     | [**Nach oben**](c-top.md)<br/> |
| [**Standort-und standortübergreifende standortübergreifende**](a-usnintersite.md)                                        | False     | [**Nach oben**](c-top.md)<br/> |
| [**"An-Last-obj-REM"**](a-usnlastobjrem.md)                                    | False     | [**Nach oben**](c-top.md)<br/> |
| [**Quell Code Quelle**](a-usnsource.md)                                              | False     | [**Nach oben**](c-top.md)<br/> |
| [**WBEM-Pfad**](a-wbempath.md)                                                | False     | [**Nach oben**](c-top.md)<br/> |
| [**Bekannte Objekte**](a-wellknownobjects.md)                               | False     | [**Nach oben**](c-top.md)<br/> |
| [**Bei Änderung**](a-whenchanged.md)                                          | False     | [**Nach oben**](c-top.md)<br/> |
| [**Bei Erstellung**](a-whencreated.md)                                          | False     | [**Nach oben**](c-top.md)<br/> |
| [**WWW-Homepage**](a-wwwhomepage.md)                                         | False     | [**Nach oben**](c-top.md)<br/> |
| [**WWW-Page-other**](a-url.md)                                                | False     | [**Nach oben**](c-top.md)<br/> |
| [**X121-Adresse**](a-x121address.md)                                          | False     | **Organisationseinheit**         |



## <a name="windows-server-2008-extended-rights"></a>Erweiterte Rechte für Windows Server 2008

Diese Klasse enthält die folgenden erweiterten Rechte für Windows Server 2008:



| Allgemeiner Name                                                |
|------------------------------------------------------------|
| [**Generieren von RSoP-Planning**](r-generate-rsop-planning.md) |
| [**Generieren von RSoP-Protokollierung**](r-generate-rsop-logging.md)   |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2

-   [Attribute](#windows-server-2008-r2-attributes)
-   [Erweiterte Rechte](#windows-server-2008-r2-extended-rights)



| Eingabe | Wert |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | False                                                                                                                                                                                                                                                                                                                                                                         |
| Object-Category             | 1                                                                                                                                                                                                                                                                                                                                                                             |
| Default-Object-Category     | \-                                                                                                                                                                                                                                                                                                                                                                            |
| Governs-Id                  | 2.5.6.5                                                                                                                                                                                                                                                                                                                                                                       |
| Standard-ausblenden-Wert        | 0                                                                                                                                                                                                                                                                                                                                                                             |
| RDN-ATT-ID                  | [**Organisations Einheits Name**](a-ou.md)<br/>                                                                                                                                                                                                                                                                                                                           |
| Unterklasse von                 | [**Nach oben**](c-top.md)<br/>                                                                                                                                                                                                                                                                                                                                               |
| Mögliche Vorgesetzten          | [**Domänen-DNS**](c-domaindns.md)-**Organisationseinheiten-**[**Organisations**](c-organization.md)[**Land**](c-country.md)                                                                                                                                                                                                                                                    |
| Zusätzlich           | \-                                                                                                                                                                                                                                                                                                                                                                            |
| NT-Security-Descriptor      | o:Bag: schlecht: S:                                                                                                                                                                                                                                                                                                                                                                  |
| Standard Sicherheits Beschreibung | D: (A;; Rpwpcrccdclclorcwowdsddtsw;;; SY) (A;; rpwpcrccdclclorcwowdsddtsw;;;D A) (OA;; CCDC; bf967a86-0de6-11D0-A285-00aa003049e2;; AO) (OA;; CCDC; bf967aba-0de6-11D0-A285-00aa003049e2;; AO) (OA;; CCDC; bf967a9c-0de6-11D0-A285-00aa003049e2;; AO) (OA;; CCDC; bf967aa8-0de6-11D0-A285-00aa003049e2;; PO) (A;; Rplclorc;;; Au) (A;; Lcrplorc;;; ED) (OA;; CCDC; 4828cc14-1437-45bc-9b07-ad6f 015e5f 28;; OS |
| System-Flags                | 0x00000010                                                                                                                                                                                                                                                                                                                                                                    |



## <a name="windows-server-2008-r2-attributes"></a>Windows Server 2008 R2-Attribute

Diese Klasse enthält die folgenden Attribute für Windows Server 2008 R2:



| Attribut                                                                        | Obligatorisch. | Abgeleitet von                    |
|----------------------------------------------------------------------------------|-----------|---------------------------------|
| [**Administrator: Beschreibung**](a-admindescription.md)                                  | False     | [**Nach oben**](c-top.md)<br/> |
| [**Administrator-Anzeige Name**](a-admindisplayname.md)                                 | False     | [**Nach oben**](c-top.md)<br/> |
| [**Zulässige Attribute**](a-allowedattributes.md)                                | False     | [**Nach oben**](c-top.md)<br/> |
| [**Zulässige Attribute-gültig**](a-allowedattributeseffective.md)             | False     | [**Nach oben**](c-top.md)<br/> |
| [**Zulässige, untergeordnete Klassen**](a-allowedchildclasses.md)                           | False     | [**Nach oben**](c-top.md)<br/> |
| [**Zulässig-untergeordnete Klassen-gültig**](a-allowedchildclasseseffective.md)        | False     | [**Nach oben**](c-top.md)<br/> |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                    | False     | [**Nach oben**](c-top.md)<br/> |
| [**Geschäfts Kategorie**](a-businesscategory.md)                                  | False     | **Organisationseinheit**         |
| [**Kanonischer Name**](a-canonicalname.md)                                        | False     | [**Nach oben**](c-top.md)<br/> |
| [**Gemeinsamer Name**](a-cn.md)                                                      | False     | [**Nach oben**](c-top.md)<br/> |
| [**Länder Code**](a-countrycode.md)                                            | False     | **Organisationseinheit**         |
| [**Länder Name**](a-c.md)                                                      | False     | **Organisationseinheit**         |
| [**Create-Zeitstempel**](a-createtimestamp.md)                                   | False     | [**Nach oben**](c-top.md)<br/> |
| [**Standardgruppe**](a-defaultgroup.md)                                          | False     | **Organisationseinheit**         |
| [**Beschreibung**](a-description.md)                                             | False     | [**Nach oben**](c-top.md)<br/> |
| [**Desktop Profil**](a-desktopprofile.md)                                      | False     | **Organisationseinheit**         |
| [**Ziel-Indikator**](a-destinationindicator.md)                          | False     | **Organisationseinheit**         |
| [**Anzeige Name**](a-displayname.md)                                            | False     | [**Nach oben**](c-top.md)<br/> |
| [**Anzeige Name-druckdruck**](a-displaynameprintable.md)                         | False     | [**Nach oben**](c-top.md)<br/> |
| [**DSA-Signatur**](a-dsasignature.md)                                          | False     | [**Nach oben**](c-top.md)<br/> |
| [**DS-Core-propagierungs Daten**](a-dscorepropagationdata.md)                      | False     | [**Nach oben**](c-top.md)<br/> |
| [**Erweiterungs Name**](a-extensionname.md)                                        | False     | [**Nach oben**](c-top.md)<br/> |
| [**Fax-Telefonnummer**](a-facsimiletelephonenumber.md)                 | False     | **Organisationseinheit**         |
| [**Fahren**](a-flags.md)                                                         | False     | [**Nach oben**](c-top.md)<br/> |
| [**Aus-Eintrag**](a-fromentry.md)                                                | False     | [**Nach oben**](c-top.md)<br/> |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                    | False     | [**Nach oben**](c-top.md)<br/> |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                        | False     | [**Nach oben**](c-top.md)<br/> |
| [**"F"-Rollen Besitzer**](a-fsmoroleowner.md)                                       | False     | [**Nach oben**](c-top.md)<br/> |
| [**GP-Link**](a-gplink.md)                                                      | False     | **Organisationseinheit**         |
| [**GP-Optionen**](a-gpoptions.md)                                                | False     | **Organisationseinheit**         |
| [**Instanztyp**](a-instancetype.md)                                          | Richtig      | [**Nach oben**](c-top.md)<br/> |
| [**International-ISDN-Number**](a-internationalisdnnumber.md)                   | False     | **Organisationseinheit**         |
| [**Is-critical-System-Object**](a-iscriticalsystemobject.md)                    | False     | [**Nach oben**](c-top.md)<br/> |
| [**Ist-gelöscht**](a-isdeleted.md)                                                | False     | [**Nach oben**](c-top.md)<br/> |
| [**Is-Member-of-DL**](a-memberof.md)                                            | False     | [**Nach oben**](c-top.md)<br/> |
| [**Is-Privilege-Inhaber**](a-isprivilegeholder.md)                               | False     | [**Nach oben**](c-top.md)<br/> |
| [**Ist-recycelt**](a-isrecycled.md)                                              | False     | [**Nach oben**](c-top.md)<br/> |
| [**Letztes-bekannt/übergeordnetes Element**](a-lastknownparent.md)                                   | False     | [**Nach oben**](c-top.md)<br/> |
| [**Lokalitäts Name**](a-l.md)                                                     | False     | **Organisationseinheit**         |
| [**Logo**](a-thumbnaillogo.md)                                                  | False     | **Organisationseinheit**         |
| [**Verwaltet von**](a-managedby.md)                                                | False     | **Organisationseinheit**         |
| [**Verwaltete Objekte**](a-managedobjects.md)                                      | False     | [**Nach oben**](c-top.md)<br/> |
| [**Verwaltet von**](a-masteredby.md)                                              | False     | [**Nach oben**](c-top.md)<br/> |
| [**Modify-Zeitstempel**](a-modifytimestamp.md)                                   | False     | [**Nach oben**](c-top.md)<br/> |
| [**MS-com-partitionsetlink**](a-mscom-partitionsetlink.md)                      | False     | [**Nach oben**](c-top.md)<br/> |
| [**MS-com-userlink**](a-mscom-userlink.md)                                      | False     | [**Nach oben**](c-top.md)<br/> |
| [**MS-com-userpartitionsetlink**](a-mscom-userpartitionsetlink.md)              | False     | **Organisationseinheit**         |
| [**MS-DFSR-computerreferencebl**](a-msdfsr-computerreferencebl.md)              | False     | [**Nach oben**](c-top.md)<br/> |
| [**MS-DFSR-mitgliedreferencebl**](a-msdfsr-memberreferencebl.md)                  | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-ca-immed-untergeordnete Elemente**](a-msds-approx-immed-subordinates.md)      | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-authentieredto-accountlist**](a-msds-authenticatedtoaccountlist.md)   | False     | [**Nach oben**](c-top.md)<br/> |
| [**MS-DS-Konsistenz-untergeordnet-Anzahl**](a-ms-ds-consistencychildcount.md)           | False     | [**Nach oben**](c-top.md)<br/> |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                        | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-aktiviert-Feature-BL**](a-msds-enabledfeaturebl.md)                      | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)             | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-is-Domain-for**](a-msds-isdomainfor.md)                                | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-is-full-Replica-for**](a-msds-isfullreplicafor.md)                     | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-is-Partial-Replica-for**](a-msds-ispartialreplicafor.md)               | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-krbtgt-Link-BL**](a-msds-krbtgtlinkbl.md)                              | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                              | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-local-Effective-Lösch Zeit**](a-msds-localeffectivedeletiontime.md) | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-local-Effective-Papier-Time**](a-msds-localeffectiverecycletime.md)   | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-gemastert von**](a-msds-masteredby.md)                                   | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Members-für-AZ-Role-BL**](a-msds-membersforazrolebl.md)                | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-NC-repl-Cursor**](a-msds-ncreplcursors.md)                            | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-NC-repl-Inbound-Nachbarn**](a-msds-ncreplinboundneighbors.md)         | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-NC-repl-Outbound-Nachbarn**](a-msds-ncreploutboundneighbors.md)       | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)    | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-NC-Typ**](a-msds-nctype.md)                                           | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                              | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                    | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-oidtoidgruppe-Link-BL**](a-msds-oidtogrouplinkbl.md)                      | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)          | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)          | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                             | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-PSO-angewendet**](a-msds-psoapplied.md)                                   | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)           | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                   | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-offengelegt-DSAs**](a-msds-revealeddsas.md)                               | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-enthüllt-List-BL**](a-msds-revealedlistbl.md)                          | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Tasks-für-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                    | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Tasks-für-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                    | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                            | False     | [**Nach oben**](c-top.md)<br/> |
| [**msSFU-30-POSIX-Member-of**](a-mssfu30posixmemberof.md)                       | False     | [**Nach oben**](c-top.md)<br/> |
| [**NetBoot-SCP-BL**](a-netbootscpbl.md)                                         | False     | [**Nach oben**](c-top.md)<br/> |
| [**Nicht sicherheitsmitglied-BL**](a-nonsecuritymemberbl.md)                          | False     | [**Nach oben**](c-top.md)<br/> |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                         | Richtig      | [**Nach oben**](c-top.md)<br/> |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                     | False     | [**Nach oben**](c-top.md)<br/> |
| [**Objekt-Kategorie**](a-objectcategory.md)                                      | Richtig      | [**Nach oben**](c-top.md)<br/> |
| [**Object-Klasse**](a-objectclass.md)                                            | Richtig      | [**Nach oben**](c-top.md)<br/> |
| [**Objekt-GUID**](a-objectguid.md)                                              | False     | [**Nach oben**](c-top.md)<br/> |
| [**Objekt-Version**](a-objectversion.md)                                        | False     | [**Nach oben**](c-top.md)<br/> |
| [**Organisations Einheits Name**](a-ou.md)                                         | Richtig      | **Organisationseinheit**         |
| [**Andere-bekannte Objekte**](a-otherwellknownobjects.md)                      | False     | [**Nach oben**](c-top.md)<br/> |
| [**Partial-Attribute-löschen-List**](a-partialattributedeletionlist.md)        | False     | [**Nach oben**](c-top.md)<br/> |
| [**Partiell-Attribut Satz**](a-partialattributeset.md)                           | False     | [**Nach oben**](c-top.md)<br/> |
| [**Physical-delivery-Office-Name**](a-physicaldeliveryofficename.md)            | False     | **Organisationseinheit**         |
| [**Mögliche-minderwertig**](a-possibleinferiors.md)                                | False     | [**Nach oben**](c-top.md)<br/> |
| [**Postanschrift**](a-postaladdress.md)                                        | False     | **Organisationseinheit**         |
| [**Postleitzahl**](a-postalcode.md)                                              | False     | **Organisationseinheit**         |
| [**Post-Office-Box**](a-postofficebox.md)                                       | False     | **Organisationseinheit**         |
| [**Bevorzugte Übermittlungs Methode**](a-preferreddeliverymethod.md)                   | False     | **Organisationseinheit**         |
| [**Proxy-Objekt Name**](a-proxiedobjectname.md)                               | False     | [**Nach oben**](c-top.md)<br/> |
| [**Proxy Adressen**](a-proxyaddresses.md)                                      | False     | [**Nach oben**](c-top.md)<br/> |
| [**Abfrage-Richtlinie-BL**](a-querypolicybl.md)                                       | False     | [**Nach oben**](c-top.md)<br/> |
| [**RDN**](a-name.md)                                                            | False     | [**Nach oben**](c-top.md)<br/> |
| [**Registrierte Adresse**](a-registeredaddress.md)                                | False     | **Organisationseinheit**         |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                        | False     | [**Nach oben**](c-top.md)<br/> |
| [**REPL-Update-Vector**](a-repluptodatevector.md)                             | False     | [**Nach oben**](c-top.md)<br/> |
| [**Berichte**](a-directreports.md)                                               | False     | [**Nach oben**](c-top.md)<br/> |
| [**Reps-from**](a-repsfrom.md)                                                  | False     | [**Nach oben**](c-top.md)<br/> |
| [**Reps-to**](a-repsto.md)                                                      | False     | [**Nach oben**](c-top.md)<br/> |
| [**Novel**](a-revision.md)                                                   | False     | [**Nach oben**](c-top.md)<br/> |
| [**SD-Rechte**](a-sdrightseffective.md)                               | False     | [**Nach oben**](c-top.md)<br/> |
| [**Such Handbuch**](a-searchguide.md)                                            | False     | **Organisationseinheit**         |
| [**Siehe auch**](a-seealso.md)                                                    | False     | **Organisationseinheit**         |
| [**Server-Reference-BL**](a-serverreferencebl.md)                               | False     | [**Nach oben**](c-top.md)<br/> |
| [**Anzeigen-in-Advanced-nur anzeigen**](a-showinadvancedviewonly.md)                   | False     | [**Nach oben**](c-top.md)<br/> |
| [**Site-Object-BL**](a-siteobjectbl.md)                                         | False     | [**Nach oben**](c-top.md)<br/> |
| [**State-or-Province-Name**](a-st.md)                                           | False     | **Organisationseinheit**         |
| [**Straße**](a-street.md)                                               | False     | **Organisationseinheit**         |
| [**Struktur-Objekt-Klasse**](a-structuralobjectclass.md)                       | False     | [**Nach oben**](c-top.md)<br/> |
| [**Sub-Refs**](a-subrefs.md)                                                    | False     | [**Nach oben**](c-top.md)<br/> |
| [**Subschemasubentry**](a-subschemasubentry.md)                                 | False     | [**Nach oben**](c-top.md)<br/> |
| [**SystemFlags**](a-systemflags.md)                                            | False     | [**Nach oben**](c-top.md)<br/> |
| [**Telefonnummer**](a-telephonenumber.md)                                    | False     | **Organisationseinheit**         |
| [**Teletex-Terminal-Identifier**](a-teletexterminalidentifier.md)               | False     | **Organisationseinheit**         |
| [**Telex-Nummer**](a-telexnumber.md)                                            | False     | **Organisationseinheit**         |
| [**Text-Country**](a-co.md)                                                     | False     | **Organisationseinheit**         |
| [**UPN-Suffixe**](a-upnsuffixes.md)                                            | False     | **Organisationseinheit**         |
| [**Benutzer Kennwort**](a-userpassword.md)                                          | False     | **Organisationseinheit**         |
| [**Die Anwendung wurde geändert.**](a-usnchanged.md)                                              | False     | [**Nach oben**](c-top.md)<br/> |
| [**Von der Anwendung erstellte**](a-usncreated.md)                                              | False     | [**Nach oben**](c-top.md)<br/> |
| [**USA-DSA-letzte-obj-entfernt**](a-usndsalastobjremoved.md)                       | False     | [**Nach oben**](c-top.md)<br/> |
| [**Standort-und standortübergreifende standortübergreifende**](a-usnintersite.md)                                          | False     | [**Nach oben**](c-top.md)<br/> |
| [**"An-Last-obj-REM"**](a-usnlastobjrem.md)                                      | False     | [**Nach oben**](c-top.md)<br/> |
| [**Quell Code Quelle**](a-usnsource.md)                                                | False     | [**Nach oben**](c-top.md)<br/> |
| [**WBEM-Pfad**](a-wbempath.md)                                                  | False     | [**Nach oben**](c-top.md)<br/> |
| [**Bekannte Objekte**](a-wellknownobjects.md)                                 | False     | [**Nach oben**](c-top.md)<br/> |
| [**Bei Änderung**](a-whenchanged.md)                                            | False     | [**Nach oben**](c-top.md)<br/> |
| [**Bei Erstellung**](a-whencreated.md)                                            | False     | [**Nach oben**](c-top.md)<br/> |
| [**WWW-Homepage**](a-wwwhomepage.md)                                           | False     | [**Nach oben**](c-top.md)<br/> |
| [**WWW-Page-other**](a-url.md)                                                  | False     | [**Nach oben**](c-top.md)<br/> |
| [**X121-Adresse**](a-x121address.md)                                            | False     | **Organisationseinheit**         |



## <a name="windows-server-2008-r2-extended-rights"></a>Erweiterte Rechte für Windows Server 2008 R2

Diese Klasse enthält die folgenden erweiterten Rechte für Windows Server 2008 R2:



| Allgemeiner Name                                                |
|------------------------------------------------------------|
| [**Generieren von RSoP-Planning**](r-generate-rsop-planning.md) |
| [**Generieren von RSoP-Protokollierung**](r-generate-rsop-logging.md)   |



## <a name="windows-server-2012"></a>Windows Server 2012

-   [Attribute](#windows-server-2012-attributes)
-   [Erweiterte Rechte](#windows-server-2012-extended-rights)



| Eingabe | Wert |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | False                                                                                                                                                                                                                                                                                                                                                                         |
| Object-Category             | 1                                                                                                                                                                                                                                                                                                                                                                             |
| Default-Object-Category     | \-                                                                                                                                                                                                                                                                                                                                                                            |
| Governs-Id                  | 2.5.6.5                                                                                                                                                                                                                                                                                                                                                                       |
| Standard-ausblenden-Wert        | 0                                                                                                                                                                                                                                                                                                                                                                             |
| RDN-ATT-ID                  | [**Organisations Einheits Name**](a-ou.md)<br/>                                                                                                                                                                                                                                                                                                                           |
| Unterklasse von                 | [**Nach oben**](c-top.md)<br/>                                                                                                                                                                                                                                                                                                                                               |
| Mögliche Vorgesetzten          | [**Domänen-DNS**](c-domaindns.md)-**Organisationseinheiten-**[**Organisations**](c-organization.md)[**Land**](c-country.md)                                                                                                                                                                                                                                                    |
| Zusätzlich           | \-                                                                                                                                                                                                                                                                                                                                                                            |
| NT-Security-Descriptor      | o:Bag: schlecht: S:                                                                                                                                                                                                                                                                                                                                                                  |
| Standard Sicherheits Beschreibung | D: (A;; Rpwpcrccdclclorcwowdsddtsw;;; SY) (A;; rpwpcrccdclclorcwowdsddtsw;;;D A) (OA;; CCDC; bf967a86-0de6-11D0-A285-00aa003049e2;; AO) (OA;; CCDC; bf967aba-0de6-11D0-A285-00aa003049e2;; AO) (OA;; CCDC; bf967a9c-0de6-11D0-A285-00aa003049e2;; AO) (OA;; CCDC; bf967aa8-0de6-11D0-A285-00aa003049e2;; PO) (A;; Rplclorc;;; Au) (A;; Lcrplorc;;; ED) (OA;; CCDC; 4828cc14-1437-45bc-9b07-ad6f 015e5f 28;; OS |
| System-Flags                | 0x00000010                                                                                                                                                                                                                                                                                                                                                                    |



## <a name="windows-server-2012-attributes"></a>Windows Server 2012-Attribute

Diese Klasse enthält die folgenden Attribute für Windows Server 2012:



| Attribut                                                                                    | Obligatorisch. | Abgeleitet von                    |
|----------------------------------------------------------------------------------------------|-----------|---------------------------------|
| [**Administrator: Beschreibung**](a-admindescription.md)                                              | False     | [**Nach oben**](c-top.md)<br/> |
| [**Administrator-Anzeige Name**](a-admindisplayname.md)                                             | False     | [**Nach oben**](c-top.md)<br/> |
| [**Zulässige Attribute**](a-allowedattributes.md)                                            | False     | [**Nach oben**](c-top.md)<br/> |
| [**Zulässige Attribute-gültig**](a-allowedattributeseffective.md)                         | False     | [**Nach oben**](c-top.md)<br/> |
| [**Zulässige, untergeordnete Klassen**](a-allowedchildclasses.md)                                       | False     | [**Nach oben**](c-top.md)<br/> |
| [**Zulässig-untergeordnete Klassen-gültig**](a-allowedchildclasseseffective.md)                    | False     | [**Nach oben**](c-top.md)<br/> |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                                | False     | [**Nach oben**](c-top.md)<br/> |
| [**Geschäfts Kategorie**](a-businesscategory.md)                                              | False     | **Organisationseinheit**         |
| [**Kanonischer Name**](a-canonicalname.md)                                                    | False     | [**Nach oben**](c-top.md)<br/> |
| [**Gemeinsamer Name**](a-cn.md)                                                                  | False     | [**Nach oben**](c-top.md)<br/> |
| [**Länder Code**](a-countrycode.md)                                                        | False     | **Organisationseinheit**         |
| [**Länder Name**](a-c.md)                                                                  | False     | **Organisationseinheit**         |
| [**Create-Zeitstempel**](a-createtimestamp.md)                                               | False     | [**Nach oben**](c-top.md)<br/> |
| [**Standardgruppe**](a-defaultgroup.md)                                                      | False     | **Organisationseinheit**         |
| [**Beschreibung**](a-description.md)                                                         | False     | [**Nach oben**](c-top.md)<br/> |
| [**Desktop Profil**](a-desktopprofile.md)                                                  | False     | **Organisationseinheit**         |
| [**Ziel-Indikator**](a-destinationindicator.md)                                      | False     | **Organisationseinheit**         |
| [**Anzeige Name**](a-displayname.md)                                                        | False     | [**Nach oben**](c-top.md)<br/> |
| [**Anzeige Name-druckdruck**](a-displaynameprintable.md)                                     | False     | [**Nach oben**](c-top.md)<br/> |
| [**DSA-Signatur**](a-dsasignature.md)                                                      | False     | [**Nach oben**](c-top.md)<br/> |
| [**DS-Core-propagierungs Daten**](a-dscorepropagationdata.md)                                  | False     | [**Nach oben**](c-top.md)<br/> |
| [**Erweiterungs Name**](a-extensionname.md)                                                    | False     | [**Nach oben**](c-top.md)<br/> |
| [**Fax-Telefonnummer**](a-facsimiletelephonenumber.md)                             | False     | **Organisationseinheit**         |
| [**Fahren**](a-flags.md)                                                                     | False     | [**Nach oben**](c-top.md)<br/> |
| [**Aus-Eintrag**](a-fromentry.md)                                                            | False     | [**Nach oben**](c-top.md)<br/> |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                                | False     | [**Nach oben**](c-top.md)<br/> |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                                    | False     | [**Nach oben**](c-top.md)<br/> |
| [**"F"-Rollen Besitzer**](a-fsmoroleowner.md)                                                   | False     | [**Nach oben**](c-top.md)<br/> |
| [**GP-Link**](a-gplink.md)                                                                  | False     | **Organisationseinheit**         |
| [**GP-Optionen**](a-gpoptions.md)                                                            | False     | **Organisationseinheit**         |
| [**Instanztyp**](a-instancetype.md)                                                      | Richtig      | [**Nach oben**](c-top.md)<br/> |
| [**International-ISDN-Number**](a-internationalisdnnumber.md)                               | False     | **Organisationseinheit**         |
| [**Is-critical-System-Object**](a-iscriticalsystemobject.md)                                | False     | [**Nach oben**](c-top.md)<br/> |
| [**Ist-gelöscht**](a-isdeleted.md)                                                            | False     | [**Nach oben**](c-top.md)<br/> |
| [**Is-Member-of-DL**](a-memberof.md)                                                        | False     | [**Nach oben**](c-top.md)<br/> |
| [**Is-Privilege-Inhaber**](a-isprivilegeholder.md)                                           | False     | [**Nach oben**](c-top.md)<br/> |
| [**Ist-recycelt**](a-isrecycled.md)                                                          | False     | [**Nach oben**](c-top.md)<br/> |
| [**Letztes-bekannt/übergeordnetes Element**](a-lastknownparent.md)                                               | False     | [**Nach oben**](c-top.md)<br/> |
| [**Lokalitäts Name**](a-l.md)                                                                 | False     | **Organisationseinheit**         |
| [**Logo**](a-thumbnaillogo.md)                                                              | False     | **Organisationseinheit**         |
| [**Verwaltet von**](a-managedby.md)                                                            | False     | **Organisationseinheit**         |
| [**Verwaltete Objekte**](a-managedobjects.md)                                                  | False     | [**Nach oben**](c-top.md)<br/> |
| [**Verwaltet von**](a-masteredby.md)                                                          | False     | [**Nach oben**](c-top.md)<br/> |
| [**Modify-Zeitstempel**](a-modifytimestamp.md)                                               | False     | [**Nach oben**](c-top.md)<br/> |
| [**MS-com-partitionsetlink**](a-mscom-partitionsetlink.md)                                  | False     | [**Nach oben**](c-top.md)<br/> |
| [**MS-com-userlink**](a-mscom-userlink.md)                                                  | False     | [**Nach oben**](c-top.md)<br/> |
| [**MS-com-userpartitionsetlink**](a-mscom-userpartitionsetlink.md)                          | False     | **Organisationseinheit**         |
| [**MS-DFSR-computerreferencebl**](a-msdfsr-computerreferencebl.md)                          | False     | [**Nach oben**](c-top.md)<br/> |
| [**MS-DFSR-mitgliedreferencebl**](a-msdfsr-memberreferencebl.md)                              | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-ca-immed-untergeordnete Elemente**](a-msds-approx-immed-subordinates.md)                  | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-authentieredto-accountlist**](a-msds-authenticatedtoaccountlist.md)               | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Claim-Shares-mögliche-values-with-BL**](a-msds-claimsharespossiblevalueswithbl.md) | False     | [**Nach oben**](c-top.md)<br/> |
| [**MS-DS-Konsistenz-untergeordnet-Anzahl**](a-ms-ds-consistencychildcount.md)                       | False     | [**Nach oben**](c-top.md)<br/> |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                                    | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-aktiviert-Feature-BL**](a-msds-enabledfeaturebl.md)                                  | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)                         | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-is-Domain-for**](a-msds-isdomainfor.md)                                            | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-is-full-Replica-for**](a-msds-isfullreplicafor.md)                                 | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-is-Partial-Replica-for**](a-msds-ispartialreplicafor.md)                           | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-is-Primary-Computer-für**](a-msds-isprimarycomputerfor.md)                         | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-krbtgt-Link-BL**](a-msds-krbtgtlinkbl.md)                                          | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                                          | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-local-Effective-Lösch Zeit**](a-msds-localeffectivedeletiontime.md)             | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-local-Effective-Papier-Time**](a-msds-localeffectiverecycletime.md)               | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-gemastert von**](a-msds-masteredby.md)                                               | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Members-für-AZ-Role-BL**](a-msds-membersforazrolebl.md)                            | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Members-of-Resource-Property-List-BL**](a-msds-membersofresourcepropertylistbl.md) | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-NC-repl-Cursor**](a-msds-ncreplcursors.md)                                        | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-NC-repl-Inbound-Nachbarn**](a-msds-ncreplinboundneighbors.md)                     | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-NC-repl-Outbound-Nachbarn**](a-msds-ncreploutboundneighbors.md)                   | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)                | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-NC-Typ**](a-msds-nctype.md)                                                       | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                                          | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                                | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-oidtoidgruppe-Link-BL**](a-msds-oidtogrouplinkbl.md)                                  | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)                      | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)                      | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                                         | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-PSO-angewendet**](a-msds-psoapplied.md)                                               | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)                       | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                               | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-offengelegt-DSAs**](a-msds-revealeddsas.md)                                           | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-enthüllt-List-BL**](a-msds-revealedlistbl.md)                                      | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Tasks-für-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                                | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Tasks-für-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                                | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-TDO-Egress-BL**](a-msds-tdoegressbl.md)                                            | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-TDO-Ingress-BL**](a-msds-tdoingressbl.md)                                          | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Value-Type-Reference-BL**](a-msds-valuetypereferencebl.md)                         | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                                        | False     | [**Nach oben**](c-top.md)<br/> |
| [**msSFU-30-POSIX-Member-of**](a-mssfu30posixmemberof.md)                                   | False     | [**Nach oben**](c-top.md)<br/> |
| [**NetBoot-SCP-BL**](a-netbootscpbl.md)                                                     | False     | [**Nach oben**](c-top.md)<br/> |
| [**Nicht sicherheitsmitglied-BL**](a-nonsecuritymemberbl.md)                                      | False     | [**Nach oben**](c-top.md)<br/> |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                                     | Richtig      | [**Nach oben**](c-top.md)<br/> |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                                 | False     | [**Nach oben**](c-top.md)<br/> |
| [**Objekt-Kategorie**](a-objectcategory.md)                                                  | Richtig      | [**Nach oben**](c-top.md)<br/> |
| [**Object-Klasse**](a-objectclass.md)                                                        | Richtig      | [**Nach oben**](c-top.md)<br/> |
| [**Objekt-GUID**](a-objectguid.md)                                                          | False     | [**Nach oben**](c-top.md)<br/> |
| [**Objekt-Version**](a-objectversion.md)                                                    | False     | [**Nach oben**](c-top.md)<br/> |
| [**Organisations Einheits Name**](a-ou.md)                                                     | Richtig      | **Organisationseinheit**         |
| [**Andere-bekannte Objekte**](a-otherwellknownobjects.md)                                  | False     | [**Nach oben**](c-top.md)<br/> |
| [**Partial-Attribute-löschen-List**](a-partialattributedeletionlist.md)                    | False     | [**Nach oben**](c-top.md)<br/> |
| [**Partiell-Attribut Satz**](a-partialattributeset.md)                                       | False     | [**Nach oben**](c-top.md)<br/> |
| [**Physical-delivery-Office-Name**](a-physicaldeliveryofficename.md)                        | False     | **Organisationseinheit**         |
| [**Mögliche-minderwertig**](a-possibleinferiors.md)                                            | False     | [**Nach oben**](c-top.md)<br/> |
| [**Postanschrift**](a-postaladdress.md)                                                    | False     | **Organisationseinheit**         |
| [**Postleitzahl**](a-postalcode.md)                                                          | False     | **Organisationseinheit**         |
| [**Post-Office-Box**](a-postofficebox.md)                                                   | False     | **Organisationseinheit**         |
| [**Bevorzugte Übermittlungs Methode**](a-preferreddeliverymethod.md)                               | False     | **Organisationseinheit**         |
| [**Proxy-Objekt Name**](a-proxiedobjectname.md)                                           | False     | [**Nach oben**](c-top.md)<br/> |
| [**Proxy Adressen**](a-proxyaddresses.md)                                                  | False     | [**Nach oben**](c-top.md)<br/> |
| [**Abfrage-Richtlinie-BL**](a-querypolicybl.md)                                                   | False     | [**Nach oben**](c-top.md)<br/> |
| [**RDN**](a-name.md)                                                                        | False     | [**Nach oben**](c-top.md)<br/> |
| [**Registrierte Adresse**](a-registeredaddress.md)                                            | False     | **Organisationseinheit**         |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                                    | False     | [**Nach oben**](c-top.md)<br/> |
| [**REPL-Update-Vector**](a-repluptodatevector.md)                                         | False     | [**Nach oben**](c-top.md)<br/> |
| [**Berichte**](a-directreports.md)                                                           | False     | [**Nach oben**](c-top.md)<br/> |
| [**Reps-from**](a-repsfrom.md)                                                              | False     | [**Nach oben**](c-top.md)<br/> |
| [**Reps-to**](a-repsto.md)                                                                  | False     | [**Nach oben**](c-top.md)<br/> |
| [**Novel**](a-revision.md)                                                               | False     | [**Nach oben**](c-top.md)<br/> |
| [**SD-Rechte**](a-sdrightseffective.md)                                           | False     | [**Nach oben**](c-top.md)<br/> |
| [**Such Handbuch**](a-searchguide.md)                                                        | False     | **Organisationseinheit**         |
| [**Siehe auch**](a-seealso.md)                                                                | False     | **Organisationseinheit**         |
| [**Server-Reference-BL**](a-serverreferencebl.md)                                           | False     | [**Nach oben**](c-top.md)<br/> |
| [**Anzeigen-in-Advanced-nur anzeigen**](a-showinadvancedviewonly.md)                               | False     | [**Nach oben**](c-top.md)<br/> |
| [**Site-Object-BL**](a-siteobjectbl.md)                                                     | False     | [**Nach oben**](c-top.md)<br/> |
| [**State-or-Province-Name**](a-st.md)                                                       | False     | **Organisationseinheit**         |
| [**Straße**](a-street.md)                                                           | False     | **Organisationseinheit**         |
| [**Struktur-Objekt-Klasse**](a-structuralobjectclass.md)                                   | False     | [**Nach oben**](c-top.md)<br/> |
| [**Sub-Refs**](a-subrefs.md)                                                                | False     | [**Nach oben**](c-top.md)<br/> |
| [**Subschemasubentry**](a-subschemasubentry.md)                                             | False     | [**Nach oben**](c-top.md)<br/> |
| [**SystemFlags**](a-systemflags.md)                                                        | False     | [**Nach oben**](c-top.md)<br/> |
| [**Telefonnummer**](a-telephonenumber.md)                                                | False     | **Organisationseinheit**         |
| [**Teletex-Terminal-Identifier**](a-teletexterminalidentifier.md)                           | False     | **Organisationseinheit**         |
| [**Telex-Nummer**](a-telexnumber.md)                                                        | False     | **Organisationseinheit**         |
| [**Text-Country**](a-co.md)                                                                 | False     | **Organisationseinheit**         |
| [**UPN-Suffixe**](a-upnsuffixes.md)                                                        | False     | **Organisationseinheit**         |
| [**Benutzer Kennwort**](a-userpassword.md)                                                      | False     | **Organisationseinheit**         |
| [**Die Anwendung wurde geändert.**](a-usnchanged.md)                                                          | False     | [**Nach oben**](c-top.md)<br/> |
| [**Von der Anwendung erstellte**](a-usncreated.md)                                                          | False     | [**Nach oben**](c-top.md)<br/> |
| [**USA-DSA-letzte-obj-entfernt**](a-usndsalastobjremoved.md)                                   | False     | [**Nach oben**](c-top.md)<br/> |
| [**Standort-und standortübergreifende standortübergreifende**](a-usnintersite.md)                                                      | False     | [**Nach oben**](c-top.md)<br/> |
| [**"An-Last-obj-REM"**](a-usnlastobjrem.md)                                                  | False     | [**Nach oben**](c-top.md)<br/> |
| [**Quell Code Quelle**](a-usnsource.md)                                                            | False     | [**Nach oben**](c-top.md)<br/> |
| [**WBEM-Pfad**](a-wbempath.md)                                                              | False     | [**Nach oben**](c-top.md)<br/> |
| [**Bekannte Objekte**](a-wellknownobjects.md)                                             | False     | [**Nach oben**](c-top.md)<br/> |
| [**Bei Änderung**](a-whenchanged.md)                                                        | False     | [**Nach oben**](c-top.md)<br/> |
| [**Bei Erstellung**](a-whencreated.md)                                                        | False     | [**Nach oben**](c-top.md)<br/> |
| [**WWW-Homepage**](a-wwwhomepage.md)                                                       | False     | [**Nach oben**](c-top.md)<br/> |
| [**WWW-Page-other**](a-url.md)                                                              | False     | [**Nach oben**](c-top.md)<br/> |
| [**X121-Adresse**](a-x121address.md)                                                        | False     | **Organisationseinheit**         |



## <a name="windows-server-2012-extended-rights"></a>Erweiterte Rechte für Windows Server 2012

Diese Klasse enthält die folgenden erweiterten Rechte für Windows Server 2012:



| Allgemeiner Name                                                |
|------------------------------------------------------------|
| [**Generieren von RSoP-Planning**](r-generate-rsop-planning.md) |
| [**Generieren von RSoP-Protokollierung**](r-generate-rsop-logging.md)   |



 

 





