---
title: Organizational-Unit-Klasse
description: Ein Container zum Speichern von Benutzern, Computern und anderen Kontoobjekten.
ms.assetid: a5a99dc7-9000-478c-9545-473cfb6ddf6c
ms.tgt_platform: multiple
keywords:
- Organizational-Unit Ad-Schema der Klasse
- organizationalUnit-Klasse AD-Schema
topic_type:
- apiref
api_name:
- Organizational-Unit
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79807cc71f5e7690aca04b80f0d5560399b8b5415fc1d7f3cf9654884b7b9c1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120065290"
---
# <a name="organizational-unit-class"></a>Organizational-Unit-Klasse

Ein Container zum Speichern von Benutzern, Computern und anderen Kontoobjekten.



| Eingabe | Wert |
|-------------------|--------------------------------------|
| CN                | Organizational-Unit                  |
| Ldap-Anzeigename | organizationalUnit                   |
| Aktualisieren von Berechtigungen  | Jeder kann dieses Objekt aktualisieren.       |
| Updatehäufigkeit  | \-                                   |
| Schema-ID-GUID    | bf967aa5-0de6-11d0-a285-00aa003049e2 |



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



| Eingabe | Wert |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falsch                                                                                                                                                                                                                                                                                                    |
| Object-Category             | 1                                                                                                                                                                                                                                                                                                        |
| Default-Object-Category     | \-                                                                                                                                                                                                                                                                                                       |
| Governs-Id                  | 2.5.6.5                                                                                                                                                                                                                                                                                                  |
| Default-Hiding-Value        | 0                                                                                                                                                                                                                                                                                                        |
| Rdn-Att-Id                  | [**Name der Organisationseinheit**](a-ou.md)<br/>                                                                                                                                                                                                                                                      |
| Unterklasse von                 | [**Nach oben**](c-top.md)<br/>                                                                                                                                                                                                                                                                          |
| Mögliche Übergeordnete          | [**Domain-DNS**](c-domaindns.md)**Organizational-Unit**[**Organization**](c-organization.md)                                                                                                                                                                                                           |
| Zusätzlich           | \-                                                                                                                                                                                                                                                                                                       |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                             |
| Standardsicherheitsdeskriptor | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(OA;; CCDC;bf967a86-0de6-11d0-a285-00aa003049e2;; AO)(OA;; CCDC;bf967aba-0de6-11d0-a285-00aa003049e2;; AO)(OA;; CCDC;bf967a9c-0de6-11d0-a285-00aa003049e2;; AO)(OA;; CCDC;bf967aa8-0de6-11d0-a285-00aa003049e2;; PO)(A;; RPLCLORC;;; AU) |
| System-Flags                | 0x00000010                                                                                                                                                                                                                                                                                               |



## <a name="windows-2000-server-attributes"></a>Windows 2000 Serverattribute

Diese Klasse enthält die folgenden Attribute für Windows Server 2000:



| attribute                                                                 | Obligatorisch. | Abgeleitet von                    |
|---------------------------------------------------------------------------|-----------|---------------------------------|
| [**Administratorbeschreibung**](a-admindescription.md)                           | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Admin-Display-Name**](a-admindisplayname.md)                          | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Allowed-Attributes**](a-allowedattributes.md)                         | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)      | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                    | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md) | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)             | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Business-Category**](a-businesscategory.md)                           | Falsch     | **Organisationseinheit**         |
| [**Kanonischer Name**](a-canonicalname.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Allgemeiner Name**](a-cn.md)                                               | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Ländercode**](a-countrycode.md)                                     | Falsch     | **Organisationseinheit**         |
| [**Country-Name**](a-c.md)                                               | Falsch     | **Organisationseinheit**         |
| [**Erstellen eines Zeitstempels**](a-createtimestamp.md)                            | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Standardgruppe**](a-defaultgroup.md)                                   | Falsch     | **Organisationseinheit**         |
| [**Beschreibung**](a-description.md)                                      | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Desktopprofil**](a-desktopprofile.md)                               | Falsch     | **Organisationseinheit**         |
| [**Zielindikator**](a-destinationindicator.md)                   | Falsch     | **Organisationseinheit**         |
| [**Anzeigename**](a-displayname.md)                                     | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Anzeigename– druckbar**](a-displaynameprintable.md)                  | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**DSA-Signature**](a-dsasignature.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**DS-Core-Propagierungsdaten**](a-dscorepropagationdata.md)               | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Erweiterungsname**](a-extensionname.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Facsimile-Telephone-Number**](a-facsimiletelephonenumber.md)          | Falsch     | **Organisationseinheit**         |
| [**Flaggen**](a-flags.md)                                                  | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**From-Entry**](a-fromentry.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)             | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                 | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**GP-Link**](a-gplink.md)                                               | Falsch     | **Organisationseinheit**         |
| [**GP-Optionen**](a-gpoptions.md)                                         | Falsch     | **Organisationseinheit**         |
| [**Instanztyp**](a-instancetype.md)                                   | Richtig      | [**Nach oben**](c-top.md)<br/> |
| [**International-ISDN-Number**](a-internationalisdnnumber.md)            | Falsch     | **Organisationseinheit**         |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)             | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Is-Deleted**](a-isdeleted.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Is-Member-of-DL**](a-memberof.md)                                     | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                        | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Last-Known-Parent**](a-lastknownparent.md)                            | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Locality-Name**](a-l.md)                                              | Falsch     | **Organisationseinheit**         |
| [**Logo**](a-thumbnaillogo.md)                                           | Falsch     | **Organisationseinheit**         |
| [**Verwaltet von**](a-managedby.md)                                         | Falsch     | **Organisationseinheit**         |
| [**Verwaltete Objekte**](a-managedobjects.md)                               | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Mastered-By**](a-masteredby.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Modify-Time-Stamp**](a-modifytimestamp.md)                            | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)    | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                 | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                  | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Non-Security-Member-BL**](a-nonsecuritymemberbl.md)                   | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                  | Richtig      | [**Nach oben**](c-top.md)<br/> |
| [**Obj-Dist-Name**](a-distinguishedname.md)                              | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Objektkategorie**](a-objectcategory.md)                               | Richtig      | [**Nach oben**](c-top.md)<br/> |
| [**Object-Class**](a-objectclass.md)                                     | Richtig      | [**Nach oben**](c-top.md)<br/> |
| [**Objekt-GUID**](a-objectguid.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Object-Version**](a-objectversion.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Organisationseinheitsname**](a-ou.md)                                  | Richtig      | **Organisationseinheit**         |
| [**Andere bekannte Objekte**](a-otherwellknownobjects.md)               | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md) | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                    | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Physical-Delivery-Office-Name**](a-physicaldeliveryofficename.md)     | Falsch     | **Organisationseinheit**         |
| [**Mögliche 100000000000**](a-possibleinferiors.md)                         | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Postal-Address**](a-postaladdress.md)                                 | Falsch     | **Organisationseinheit**         |
| [**Postleitzahl**](a-postalcode.md)                                       | Falsch     | **Organisationseinheit**         |
| [**Post-Office-Box**](a-postofficebox.md)                                | Falsch     | **Organisationseinheit**         |
| [**Preferred-Delivery-Method**](a-preferreddeliverymethod.md)            | Falsch     | **Organisationseinheit**         |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                        | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Proxyadressen**](a-proxyaddresses.md)                               | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Query-Policy-BL**](a-querypolicybl.md)                                | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Rdn**](a-name.md)                                                     | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Registrierte Adresse**](a-registeredaddress.md)                         | Falsch     | **Organisationseinheit**         |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                 | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                      | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Berichte**](a-directreports.md)                                        | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Reps-From**](a-repsfrom.md)                                           | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Reps-To**](a-repsto.md)                                               | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Revision**](a-revision.md)                                            | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                        | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Search-Guide**](a-searchguide.md)                                     | Falsch     | **Organisationseinheit**         |
| [**Siehe auch**](a-seealso.md)                                             | Falsch     | **Organisationseinheit**         |
| [**Server-Reference-BL**](a-serverreferencebl.md)                        | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)            | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Site-Object-BL**](a-siteobjectbl.md)                                  | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**State-Or-Province-Name**](a-st.md)                                    | Falsch     | **Organisationseinheit**         |
| [**Street-Address**](a-street.md)                                        | Falsch     | **Organisationseinheit**         |
| [**Sub-Refs**](a-subrefs.md)                                             | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                          | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Systemflags**](a-systemflags.md)                                     | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Telefonnummer**](a-telephonenumber.md)                             | Falsch     | **Organisationseinheit**         |
| [**Teletex-Terminal-Identifier**](a-teletexterminalidentifier.md)        | Falsch     | **Organisationseinheit**         |
| [**Telex-Number**](a-telexnumber.md)                                     | Falsch     | **Organisationseinheit**         |
| [**Text-Country**](a-co.md)                                              | Falsch     | **Organisationseinheit**         |
| [**UPN-Suffixe**](a-upnsuffixes.md)                                     | Falsch     | **Organisationseinheit**         |
| [**Benutzerkennwort**](a-userpassword.md)                                   | Falsch     | **Organisationseinheit**         |
| [**USN geändert**](a-usnchanged.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**USN-erstellt**](a-usncreated.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**USN-DSA-last-obj-removed**](a-usndsalastobjremoved.md)                | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**USN-Intersite**](a-usnintersite.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                               | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**USN-Quelle**](a-usnsource.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Wbem-Pfad**](a-wbempath.md)                                           | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Bekannte Objekte**](a-wellknownobjects.md)                          | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Bei Änderung**](a-whenchanged.md)                                     | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Bei der Erstellung**](a-whencreated.md)                                     | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**WWW-Startseite**](a-wwwhomepage.md)                                    | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**WWW-Page-Other**](a-url.md)                                           | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**X121-Address**](a-x121address.md)                                     | Falsch     | **Organisationseinheit**         |



## <a name="windows-server-2003"></a>Windows Server 2003

-   [Attribute](#windows-server-2003-attributes)
-   [Erweiterte Rechte](#windows-server-2003-extended-rights)



| Eingabe | Wert |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falsch                                                                                                                                                                                                                                                                                                                                                                         |
| Object-Category             | 1                                                                                                                                                                                                                                                                                                                                                                             |
| Default-Object-Category     | \-                                                                                                                                                                                                                                                                                                                                                                            |
| Governs-Id                  | 2.5.6.5                                                                                                                                                                                                                                                                                                                                                                       |
| Default-Hiding-Value        | 0                                                                                                                                                                                                                                                                                                                                                                             |
| Rdn-Att-Id                  | [**Name der Organisationseinheit**](a-ou.md)<br/>                                                                                                                                                                                                                                                                                                                           |
| Unterklasse von                 | [**Nach oben**](c-top.md)<br/>                                                                                                                                                                                                                                                                                                                                               |
| Mögliche Übergeordnete          | [**Land**](c-country.md) der [**Organisation**](c-organization.md)der **Domänen-DNS-Organisationseinheit** [](c-domaindns.md)                                                                                                                                                                                                                                                    |
| Zusätzlich           | \-                                                                                                                                                                                                                                                                                                                                                                            |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                                  |
| Standardsicherheitsdeskriptor | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(OA;; CCDC;bf967a86-0de6-11d0-a285-00aa003049e2;; AO)(OA;; CCDC;bf967aba-0de6-11d0-a285-00aa003049e2;; AO)(OA;; CCDC;bf967a9c-0de6-11d0-a285-00aa003049e2;; AO)(OA;; CCDC;bf967aa8-0de6-11d0-a285-00aa003049e2;; PO)(A;; RPLCLORC;;; AU)(A;; LCRPLORC;;; ED)(OA;; CCDC;4828CC14-1437-45bc-9B07-AD6F015E5F28;; AO) |
| System-Flags                | 0x00000010                                                                                                                                                                                                                                                                                                                                                                    |



## <a name="windows-server-2003-attributes"></a>Windows Server 2003-Attribute

Diese Klasse enthält die folgenden Attribute für Windows Server 2003:



| attribute                                                                   | Obligatorisch. | Abgeleitet von                    |
|-----------------------------------------------------------------------------|-----------|---------------------------------|
| [**Admin-Description**](a-admindescription.md)                             | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Administratoranzeigename**](a-admindisplayname.md)                            | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Allowed-Attributes**](a-allowedattributes.md)                           | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)        | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                      | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)   | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)               | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Business-Category**](a-businesscategory.md)                             | Falsch     | **Organisationseinheit**         |
| [**Kanonischer Name**](a-canonicalname.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Common-Name**](a-cn.md)                                                 | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Ländercode**](a-countrycode.md)                                       | Falsch     | **Organisationseinheit**         |
| [**Country-Name**](a-c.md)                                                 | Falsch     | **Organisationseinheit**         |
| [**Create-Time-Stamp**](a-createtimestamp.md)                              | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Default-Group**](a-defaultgroup.md)                                     | Falsch     | **Organisationseinheit**         |
| [**Beschreibung**](a-description.md)                                        | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Desktop-Profile**](a-desktopprofile.md)                                 | Falsch     | **Organisationseinheit**         |
| [**Destination-Indicator**](a-destinationindicator.md)                     | Falsch     | **Organisationseinheit**         |
| [**Anzeigename**](a-displayname.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Display-Name-Printable**](a-displaynameprintable.md)                    | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**DSA-Signature**](a-dsasignature.md)                                     | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**DS-Core-Propagierungsdaten**](a-dscorepropagationdata.md)                 | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Extension-Name**](a-extensionname.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Facsimile-Telephone-Number**](a-facsimiletelephonenumber.md)            | Falsch     | **Organisationseinheit**         |
| [**Flaggen**](a-flags.md)                                                    | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**From-Entry**](a-fromentry.md)                                           | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)               | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                   | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                  | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**GP-Link**](a-gplink.md)                                                 | Falsch     | **Organisationseinheit**         |
| [**GP-Options**](a-gpoptions.md)                                           | Falsch     | **Organisationseinheit**         |
| [**Instanztyp**](a-instancetype.md)                                     | Richtig      | [**Nach oben**](c-top.md)<br/> |
| [**International-ISDN-Number**](a-internationalisdnnumber.md)              | Falsch     | **Organisationseinheit**         |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)               | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Is-Deleted**](a-isdeleted.md)                                           | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Is-Member-of-DL**](a-memberof.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                          | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Last-Known-Parent**](a-lastknownparent.md)                              | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Locality-Name**](a-l.md)                                                | Falsch     | **Organisationseinheit**         |
| [**Logo**](a-thumbnaillogo.md)                                             | Falsch     | **Organisationseinheit**         |
| [**Verwaltet von**](a-managedby.md)                                           | Falsch     | **Organisationseinheit**         |
| [**Verwaltete Objekte**](a-managedobjects.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Mastered-By**](a-masteredby.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Modify-Time-Stamp**](a-modifytimestamp.md)                              | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                 | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-COM-UserPartitionSetLink**](a-mscom-userpartitionsetlink.md)         | Falsch     | **Organisationseinheit**         |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md) | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)      | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                              | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Members-for-Az-Role-BL**](a-msds-membersforazrolebl.md)           | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                       | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)    | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)  | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                         | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)               | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Operations-for-Az-Role-BL**](a-msds-operationsforazrolebl.md)     | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Operations-for-Az-Task-BL**](a-msds-operationsforaztaskbl.md)     | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)      | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)              | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Tasks-for-Az-Role-BL**](a-msds-tasksforazrolebl.md)               | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Tasks-for-Az-Task-BL**](a-msds-tasksforaztaskbl.md)               | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                    | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Non-Security-Member-BL**](a-nonsecuritymemberbl.md)                     | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                    | Richtig      | [**Nach oben**](c-top.md)<br/> |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Objektkategorie**](a-objectcategory.md)                                 | Richtig      | [**Nach oben**](c-top.md)<br/> |
| [**Object-Class**](a-objectclass.md)                                       | Richtig      | [**Nach oben**](c-top.md)<br/> |
| [**Objekt-GUID**](a-objectguid.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Object-Version**](a-objectversion.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Organisationseinheitsname**](a-ou.md)                                    | Richtig      | **Organisationseinheit**         |
| [**Andere bekannte Objekte**](a-otherwellknownobjects.md)                 | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)   | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                      | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Physical-Delivery-Office-Name**](a-physicaldeliveryofficename.md)       | Falsch     | **Organisationseinheit**         |
| [**Mögliche 100000000000**](a-possibleinferiors.md)                           | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Postal-Address**](a-postaladdress.md)                                   | Falsch     | **Organisationseinheit**         |
| [**Postleitzahl**](a-postalcode.md)                                         | Falsch     | **Organisationseinheit**         |
| [**Post-Office-Box**](a-postofficebox.md)                                  | Falsch     | **Organisationseinheit**         |
| [**Preferred-Delivery-Method**](a-preferreddeliverymethod.md)              | Falsch     | **Organisationseinheit**         |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                          | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Proxyadressen**](a-proxyaddresses.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Query-Policy-BL**](a-querypolicybl.md)                                  | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Rdn**](a-name.md)                                                       | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Registrierte Adresse**](a-registeredaddress.md)                           | Falsch     | **Organisationseinheit**         |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                   | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                        | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Berichte**](a-directreports.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Reps-From**](a-repsfrom.md)                                             | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Reps-To**](a-repsto.md)                                                 | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Revision**](a-revision.md)                                              | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                          | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Search-Guide**](a-searchguide.md)                                       | Falsch     | **Organisationseinheit**         |
| [**Siehe auch**](a-seealso.md)                                               | Falsch     | **Organisationseinheit**         |
| [**Server-Reference-BL**](a-serverreferencebl.md)                          | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)              | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**State-Or-Province-Name**](a-st.md)                                      | Falsch     | **Organisationseinheit**         |
| [**Street-Address**](a-street.md)                                          | Falsch     | **Organisationseinheit**         |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                  | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Sub-Refs**](a-subrefs.md)                                               | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Systemflags**](a-systemflags.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Telefonnummer**](a-telephonenumber.md)                               | Falsch     | **Organisationseinheit**         |
| [**Teletex-Terminal-Identifier**](a-teletexterminalidentifier.md)          | Falsch     | **Organisationseinheit**         |
| [**Telex-Number**](a-telexnumber.md)                                       | Falsch     | **Organisationseinheit**         |
| [**Text-Country**](a-co.md)                                                | Falsch     | **Organisationseinheit**         |
| [**UPN-Suffixe**](a-upnsuffixes.md)                                       | Falsch     | **Organisationseinheit**         |
| [**Benutzerkennwort**](a-userpassword.md)                                     | Falsch     | **Organisationseinheit**         |
| [**USN geändert**](a-usnchanged.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**USN-erstellt**](a-usncreated.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**USN-DSA-last-obj-removed**](a-usndsalastobjremoved.md)                  | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**USN-Intersite**](a-usnintersite.md)                                     | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**USN-Quelle**](a-usnsource.md)                                           | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Wbem-Pfad**](a-wbempath.md)                                             | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Bekannte Objekte**](a-wellknownobjects.md)                            | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Bei Änderung**](a-whenchanged.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Bei der Erstellung**](a-whencreated.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**WWW-Startseite**](a-wwwhomepage.md)                                      | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**WWW-Page-Other**](a-url.md)                                             | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**X121-Address**](a-x121address.md)                                       | Falsch     | **Organisationseinheit**         |



## <a name="windows-server-2003-extended-rights"></a>Windows Erweiterte Rechte für Server 2003

Diese Klasse enthält die folgenden erweiterten Rechte für Windows Server 2003:



| Allgemeiner Name                                                |
|------------------------------------------------------------|
| [**Generate-RSoP-Planning**](r-generate-rsop-planning.md) |
| [**Generate-RSoP-Logging**](r-generate-rsop-logging.md)   |



## <a name="adam"></a>Adam

-   [Attribute](#adam-attributes)



| Eingabe | Wert |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falsch                                                                                                                      |
| Object-Category             | 1                                                                                                                          |
| Default-Object-Category     | \-                                                                                                                         |
| Governs-Id                  | 2.5.6.5                                                                                                                    |
| Default-Hiding-Value        | 0                                                                                                                          |
| Rdn-Att-Id                  | [**Name der Organisationseinheit**](a-ou.md)<br/>                                                                        |
| Unterklasse von                 | [**Nach oben**](c-top.md)<br/>                                                                                            |
| Mögliche Übergeordnete          | [**Land**](c-country.md) der [**Organisation**](c-organization.md)der **Domänen-DNS-Organisationseinheit** [](c-domaindns.md) |
| Zusätzlich           | \-                                                                                                                         |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                                               |
| Standardsicherheitsdeskriptor | D:S:                                                                                                                       |
| System-Flags                | 0x00000010                                                                                                                 |



## <a name="adam-attributes"></a>ADAM-Attribute

Diese Klasse enthält die folgenden Attribute für ADAM:



| attribute                                                                   | Obligatorisch. | Abgeleitet von                    |
|-----------------------------------------------------------------------------|-----------|---------------------------------|
| [**Admin-Description**](a-admindescription.md)                             | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Administratoranzeigename**](a-admindisplayname.md)                            | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Allowed-Attributes**](a-allowedattributes.md)                           | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)        | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                      | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)   | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)               | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Business-Category**](a-businesscategory.md)                             | Falsch     | **Organisationseinheit**         |
| [**Kanonischer Name**](a-canonicalname.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Common-Name**](a-cn.md)                                                 | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Ländercode**](a-countrycode.md)                                       | Falsch     | **Organisationseinheit**         |
| [**Country-Name**](a-c.md)                                                 | Falsch     | **Organisationseinheit**         |
| [**Create-Time-Stamp**](a-createtimestamp.md)                              | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Default-Group**](a-defaultgroup.md)                                     | Falsch     | **Organisationseinheit**         |
| [**Beschreibung**](a-description.md)                                        | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Desktop-Profile**](a-desktopprofile.md)                                 | Falsch     | **Organisationseinheit**         |
| [**Destination-Indicator**](a-destinationindicator.md)                     | Falsch     | **Organisationseinheit**         |
| [**Anzeigename**](a-displayname.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**DSA-Signature**](a-dsasignature.md)                                     | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**DS-Core-Propagierungsdaten**](a-dscorepropagationdata.md)                 | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Facsimile-Telephone-Number**](a-facsimiletelephonenumber.md)            | Falsch     | **Organisationseinheit**         |
| [**From-Entry**](a-fromentry.md)                                           | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                  | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Instanztyp**](a-instancetype.md)                                     | Richtig      | [**Nach oben**](c-top.md)<br/> |
| [**International-ISDN-Number**](a-internationalisdnnumber.md)              | Falsch     | **Organisationseinheit**         |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)               | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Is-Deleted**](a-isdeleted.md)                                           | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Is-Member-of-DL**](a-memberof.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Letztes bekanntes übergeordnetes Element**](a-lastknownparent.md)                              | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Locality-Name**](a-l.md)                                                | Falsch     | **Organisationseinheit**         |
| [**Logo**](a-thumbnaillogo.md)                                             | Falsch     | **Organisationseinheit**         |
| [**Verwaltet von**](a-managedby.md)                                           | Falsch     | **Organisationseinheit**         |
| [**Verwaltete Objekte**](a-managedobjects.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Mastered By**](a-masteredby.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Modify-Time-Stamp**](a-modifytimestamp.md)                              | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md) | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)      | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Disable-For-Instances-BL**](a-msds-disableforinstancesbl.md)      | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                              | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                       | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)    | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)  | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)      | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)              | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Service-Account-BL**](a-msds-serviceaccountbl.md)                 | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                    | Richtig      | [**Nach oben**](c-top.md)<br/> |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Objektkategorie**](a-objectcategory.md)                                 | Richtig      | [**Nach oben**](c-top.md)<br/> |
| [**Object-Class**](a-objectclass.md)                                       | Richtig      | [**Nach oben**](c-top.md)<br/> |
| [**Objekt-GUID**](a-objectguid.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Object-Version**](a-objectversion.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Organisationseinheitsname**](a-ou.md)                                    | Richtig      | **Organisationseinheit**         |
| [**Andere bekannte Objekte**](a-otherwellknownobjects.md)                 | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)   | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                      | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Physical-Delivery-Office-Name**](a-physicaldeliveryofficename.md)       | Falsch     | **Organisationseinheit**         |
| [**Mögliche 100000000000**](a-possibleinferiors.md)                           | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Postal-Address**](a-postaladdress.md)                                   | Falsch     | **Organisationseinheit**         |
| [**Postleitzahl**](a-postalcode.md)                                         | Falsch     | **Organisationseinheit**         |
| [**Post-Office-Box**](a-postofficebox.md)                                  | Falsch     | **Organisationseinheit**         |
| [**Preferred-Delivery-Method**](a-preferreddeliverymethod.md)              | Falsch     | **Organisationseinheit**         |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                          | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Proxyadressen**](a-proxyaddresses.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Query-Policy-BL**](a-querypolicybl.md)                                  | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Rdn**](a-name.md)                                                       | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Registrierte Adresse**](a-registeredaddress.md)                           | Falsch     | **Organisationseinheit**         |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                   | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                        | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Reps-From**](a-repsfrom.md)                                             | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Reps-To**](a-repsto.md)                                                 | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Revision**](a-revision.md)                                              | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                          | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Search-Guide**](a-searchguide.md)                                       | Falsch     | **Organisationseinheit**         |
| [**Siehe auch**](a-seealso.md)                                               | Falsch     | **Organisationseinheit**         |
| [**Server-Reference-BL**](a-serverreferencebl.md)                          | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Nur in erweiterter Ansicht anzeigen**](a-showinadvancedviewonly.md)              | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**State-or-Province-Name**](a-st.md)                                      | Falsch     | **Organisationseinheit**         |
| [**Adresse der Straße**](a-street.md)                                          | Falsch     | **Organisationseinheit**         |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                  | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Sub-Refs**](a-subrefs.md)                                               | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Systemflags**](a-systemflags.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Telefonnummer**](a-telephonenumber.md)                               | Falsch     | **Organisationseinheit**         |
| [**Teletex-Terminal-Identifier**](a-teletexterminalidentifier.md)          | Falsch     | **Organisationseinheit**         |
| [**Telex-Number**](a-telexnumber.md)                                       | Falsch     | **Organisationseinheit**         |
| [**Text-Country**](a-co.md)                                                | Falsch     | **Organisationseinheit**         |
| [**UPN-Suffixe**](a-upnsuffixes.md)                                       | Falsch     | **Organisationseinheit**         |
| [**Benutzerkennwort**](a-userpassword.md)                                     | Falsch     | **Organisationseinheit**         |
| [**USN geändert**](a-usnchanged.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**USN-erstellt**](a-usncreated.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**USN-DSA-last-obj-removed**](a-usndsalastobjremoved.md)                  | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**USN-Intersite**](a-usnintersite.md)                                     | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**USN-Quelle**](a-usnsource.md)                                           | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Wbem-Pfad**](a-wbempath.md)                                             | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Bekannte Objekte**](a-wellknownobjects.md)                            | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Bei Änderung**](a-whenchanged.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Wenn erstellt**](a-whencreated.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**WWW-Homepage**](a-wwwhomepage.md)                                      | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**WWW-Page-Other**](a-url.md)                                             | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**X121-Adresse**](a-x121address.md)                                       | Falsch     | **Organisationseinheit**         |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2

-   [Attribute](#windows-server-2003-r2-attributes)
-   [Erweiterte Rechte](#windows-server-2003-r2-extended-rights)



| Eingabe | Wert |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falsch                                                                                                                                                                                                                                                                                                                                                                         |
| Object-Category             | 1                                                                                                                                                                                                                                                                                                                                                                             |
| Default-Object-Category     | \-                                                                                                                                                                                                                                                                                                                                                                            |
| Governs-Id                  | 2.5.6.5                                                                                                                                                                                                                                                                                                                                                                       |
| Default-Hiding-Value        | 0                                                                                                                                                                                                                                                                                                                                                                             |
| Rdn-Att-Id                  | [**Organisationseinheitsname**](a-ou.md)<br/>                                                                                                                                                                                                                                                                                                                           |
| Unterklasse von                 | [**Nach oben**](c-top.md)<br/>                                                                                                                                                                                                                                                                                                                                               |
| Mögliche Vorgesetzte          | [**Domain-DNS**](c-domaindns.md)**Organizational-Unit**[**Organization**](c-organization.md)[**Country**](c-country.md)                                                                                                                                                                                                                                                    |
| Zusätzlich           | \-                                                                                                                                                                                                                                                                                                                                                                            |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                                  |
| Standardsicherheitsdeskriptor | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(OA;; CCDC;bf967a86-0de6-11d0-a285-00aa003049e2;; AO)(OA;; CCDC;bf967aba-0de6-11d0-a285-00aa003049e2;; AO)(OA;; CCDC;bf967a9c-0de6-11d0-a285-00aa003049e2;; AO)(OA;; CCDC;bf967aa8-0de6-11d0-a285-00aa003049e2;; PO)(A;; RPLCLORC;;; AU)(A;; LCRPLORC;;; ED)(OA;; CCDC;4828CC14-1437-45bc-9B07-AD6F015E5F28;; AO) |
| System-Flags                | 0x00000010                                                                                                                                                                                                                                                                                                                                                                    |



## <a name="windows-server-2003-r2-attributes"></a>Windows Server 2003 R2-Attribute

Diese Klasse enthält die folgenden Attribute für Windows Server 2003 R2:



| attribute                                                                   | Obligatorisch. | Abgeleitet von                    |
|-----------------------------------------------------------------------------|-----------|---------------------------------|
| [**Admin-Description**](a-admindescription.md)                             | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Administratoranzeigename**](a-admindisplayname.md)                            | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Allowed-Attributes**](a-allowedattributes.md)                           | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)        | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                      | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)   | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)               | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Business-Category**](a-businesscategory.md)                             | Falsch     | **Organisationseinheit**         |
| [**Kanonischer Name**](a-canonicalname.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Common-Name**](a-cn.md)                                                 | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Ländercode**](a-countrycode.md)                                       | Falsch     | **Organisationseinheit**         |
| [**Country-Name**](a-c.md)                                                 | Falsch     | **Organisationseinheit**         |
| [**Create-Time-Stamp**](a-createtimestamp.md)                              | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Default-Group**](a-defaultgroup.md)                                     | Falsch     | **Organisationseinheit**         |
| [**Beschreibung**](a-description.md)                                        | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Desktop-Profile**](a-desktopprofile.md)                                 | Falsch     | **Organisationseinheit**         |
| [**Destination-Indicator**](a-destinationindicator.md)                     | Falsch     | **Organisationseinheit**         |
| [**Anzeigename**](a-displayname.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Anzeigename– druckbar**](a-displaynameprintable.md)                    | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**DSA-Signature**](a-dsasignature.md)                                     | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**DS-Core-Propagierungsdaten**](a-dscorepropagationdata.md)                 | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Erweiterungsname**](a-extensionname.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Facsimile-Telephone-Number**](a-facsimiletelephonenumber.md)            | Falsch     | **Organisationseinheit**         |
| [**Flaggen**](a-flags.md)                                                    | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**From-Entry**](a-fromentry.md)                                           | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)               | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                   | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                  | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**GP-Link**](a-gplink.md)                                                 | Falsch     | **Organisationseinheit**         |
| [**GP-Optionen**](a-gpoptions.md)                                           | Falsch     | **Organisationseinheit**         |
| [**Instanztyp**](a-instancetype.md)                                     | Richtig      | [**Nach oben**](c-top.md)<br/> |
| [**International-ISDN-Number**](a-internationalisdnnumber.md)              | Falsch     | **Organisationseinheit**         |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)               | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Is-Deleted**](a-isdeleted.md)                                           | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Is-Member-of-DL**](a-memberof.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                          | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Last-Known-Parent**](a-lastknownparent.md)                              | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Locality-Name**](a-l.md)                                                | Falsch     | **Organisationseinheit**         |
| [**Logo**](a-thumbnaillogo.md)                                             | Falsch     | **Organisationseinheit**         |
| [**Verwaltet von**](a-managedby.md)                                           | Falsch     | **Organisationseinheit**         |
| [**Verwaltete Objekte**](a-managedobjects.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Mastered-By**](a-masteredby.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Modify-Time-Stamp**](a-modifytimestamp.md)                              | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                 | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-COM-UserPartitionSetLink**](a-mscom-userpartitionsetlink.md)         | Falsch     | **Organisationseinheit**         |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)         | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)             | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md) | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)      | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                              | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Members-for-Az-Role-BL**](a-msds-membersforazrolebl.md)           | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                       | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)    | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)  | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                         | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)               | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Operations-for-Az-Role-BL**](a-msds-operationsforazrolebl.md)     | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Operations-for-Az-Task-BL**](a-msds-operationsforaztaskbl.md)     | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)      | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)              | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Tasks-for-Az-Role-BL**](a-msds-tasksforazrolebl.md)               | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Tasks-for-Az-Task-BL**](a-msds-tasksforaztaskbl.md)               | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                  | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                    | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Non-Security-Member-BL**](a-nonsecuritymemberbl.md)                     | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                    | Richtig      | [**Nach oben**](c-top.md)<br/> |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Objektkategorie**](a-objectcategory.md)                                 | Richtig      | [**Nach oben**](c-top.md)<br/> |
| [**Objektklasse**](a-objectclass.md)                                       | Richtig      | [**Nach oben**](c-top.md)<br/> |
| [**Objekt-GUID**](a-objectguid.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Objektversion**](a-objectversion.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Name der Organisationseinheit**](a-ou.md)                                    | Richtig      | **Organisationseinheit**         |
| [**Andere bekannte Objekte**](a-otherwellknownobjects.md)                 | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Teilattributlöschungsliste**](a-partialattributedeletionlist.md)   | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Teilattributsatz**](a-partialattributeset.md)                      | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Physical-Delivery-Office-Name**](a-physicaldeliveryofficename.md)       | Falsch     | **Organisationseinheit**         |
| [**Mögliche Hindernisse**](a-possibleinferiors.md)                           | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Postanschrift**](a-postaladdress.md)                                   | Falsch     | **Organisationseinheit**         |
| [**Postleitzahl**](a-postalcode.md)                                         | Falsch     | **Organisationseinheit**         |
| [**Post-Office-Box**](a-postofficebox.md)                                  | Falsch     | **Organisationseinheit**         |
| [**Preferred-Delivery-Method**](a-preferreddeliverymethod.md)              | Falsch     | **Organisationseinheit**         |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                          | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Proxyadressen**](a-proxyaddresses.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Query-Policy-BL**](a-querypolicybl.md)                                  | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Rdn**](a-name.md)                                                       | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Registrierte Adresse**](a-registeredaddress.md)                           | Falsch     | **Organisationseinheit**         |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                   | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                        | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Berichte**](a-directreports.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Reps-From**](a-repsfrom.md)                                             | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Reps-To**](a-repsto.md)                                                 | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Revision**](a-revision.md)                                              | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                          | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Search-Guide**](a-searchguide.md)                                       | Falsch     | **Organisationseinheit**         |
| [**Siehe auch**](a-seealso.md)                                               | Falsch     | **Organisationseinheit**         |
| [**Server-Reference-BL**](a-serverreferencebl.md)                          | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Nur in erweiterter Ansicht anzeigen**](a-showinadvancedviewonly.md)              | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**State-or-Province-Name**](a-st.md)                                      | Falsch     | **Organisationseinheit**         |
| [**Adresse der Straße**](a-street.md)                                          | Falsch     | **Organisationseinheit**         |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                  | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Sub-Refs**](a-subrefs.md)                                               | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Systemflags**](a-systemflags.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Telefonnummer**](a-telephonenumber.md)                               | Falsch     | **Organisationseinheit**         |
| [**Teletex-Terminal-Identifier**](a-teletexterminalidentifier.md)          | Falsch     | **Organisationseinheit**         |
| [**Telex-Number**](a-telexnumber.md)                                       | Falsch     | **Organisationseinheit**         |
| [**Text-Country**](a-co.md)                                                | Falsch     | **Organisationseinheit**         |
| [**UPN-Suffixe**](a-upnsuffixes.md)                                       | Falsch     | **Organisationseinheit**         |
| [**Benutzerkennwort**](a-userpassword.md)                                     | Falsch     | **Organisationseinheit**         |
| [**USN geändert**](a-usnchanged.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**USN-erstellt**](a-usncreated.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**USN-DSA-last-obj-removed**](a-usndsalastobjremoved.md)                  | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**USN-Intersite**](a-usnintersite.md)                                     | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**USN-Quelle**](a-usnsource.md)                                           | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Wbem-Pfad**](a-wbempath.md)                                             | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Bekannte Objekte**](a-wellknownobjects.md)                            | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Bei Änderung**](a-whenchanged.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Bei der Erstellung**](a-whencreated.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**WWW-Startseite**](a-wwwhomepage.md)                                      | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**WWW-Page-Other**](a-url.md)                                             | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**X121-Address**](a-x121address.md)                                       | Falsch     | **Organisationseinheit**         |



## <a name="windows-server-2003-r2-extended-rights"></a>Windows Erweiterte Rechte für Server 2003 R2

Diese Klasse enthält die folgenden erweiterten Rechte für Windows Server 2003 R2:



| Allgemeiner Name                                                |
|------------------------------------------------------------|
| [**Generate-RSoP-Planning**](r-generate-rsop-planning.md) |
| [**Generate-RSoP-Logging**](r-generate-rsop-logging.md)   |



## <a name="windows-server-2008"></a>Windows Server 2008

-   [Attribute](#windows-server-2008-attributes)
-   [Erweiterte Rechte](#windows-server-2008-extended-rights)



| Eingabe | Wert |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falsch                                                                                                                                                                                                                                                                                                                                                                         |
| Object-Category             | 1                                                                                                                                                                                                                                                                                                                                                                             |
| Default-Object-Category     | \-                                                                                                                                                                                                                                                                                                                                                                            |
| Governs-Id                  | 2.5.6.5                                                                                                                                                                                                                                                                                                                                                                       |
| Default-Hiding-Value        | 0                                                                                                                                                                                                                                                                                                                                                                             |
| Rdn-Att-Id                  | [**Name der Organisationseinheit**](a-ou.md)<br/>                                                                                                                                                                                                                                                                                                                           |
| Unterklasse von                 | [**Nach oben**](c-top.md)<br/>                                                                                                                                                                                                                                                                                                                                               |
| Mögliche Übergeordnete          | [**Land**](c-country.md) der [**Organisation**](c-organization.md)der **Domänen-DNS-Organisationseinheit** [](c-domaindns.md)                                                                                                                                                                                                                                                    |
| Zusätzlich           | \-                                                                                                                                                                                                                                                                                                                                                                            |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                                  |
| Standardsicherheitsdeskriptor | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(OA;; CCDC;bf967a86-0de6-11d0-a285-00aa003049e2;; AO)(OA;; CCDC;bf967aba-0de6-11d0-a285-00aa003049e2;; AO)(OA;; CCDC;bf967a9c-0de6-11d0-a285-00aa003049e2;; AO)(OA;; CCDC;bf967aa8-0de6-11d0-a285-00aa003049e2;; PO)(A;; RPLCLORC;;; AU)(A;; LCRPLORC;;; ED)(OA;; CCDC;4828CC14-1437-45bc-9B07-AD6F015E5F28;; AO) |
| System-Flags                | 0x00000010                                                                                                                                                                                                                                                                                                                                                                    |



## <a name="windows-server-2008-attributes"></a>Windows Server 2008-Attribute

Diese Klasse enthält die folgenden Attribute für Windows Server 2008:



| attribute                                                                      | Obligatorisch. | Abgeleitet von                    |
|--------------------------------------------------------------------------------|-----------|---------------------------------|
| [**Administratorbeschreibung**](a-admindescription.md)                                | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Admin-Display-Name**](a-admindisplayname.md)                               | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Allowed-Attributes**](a-allowedattributes.md)                              | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)           | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                         | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)      | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                  | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Business-Category**](a-businesscategory.md)                                | Falsch     | **Organisationseinheit**         |
| [**Kanonischer Name**](a-canonicalname.md)                                      | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Allgemeiner Name**](a-cn.md)                                                    | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Ländercode**](a-countrycode.md)                                          | Falsch     | **Organisationseinheit**         |
| [**Country-Name**](a-c.md)                                                    | Falsch     | **Organisationseinheit**         |
| [**Erstellen eines Zeitstempels**](a-createtimestamp.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Standardgruppe**](a-defaultgroup.md)                                        | Falsch     | **Organisationseinheit**         |
| [**Beschreibung**](a-description.md)                                           | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Desktopprofil**](a-desktopprofile.md)                                    | Falsch     | **Organisationseinheit**         |
| [**Zielindikator**](a-destinationindicator.md)                        | Falsch     | **Organisationseinheit**         |
| [**Anzeigename**](a-displayname.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Anzeigename– druckbar**](a-displaynameprintable.md)                       | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**DSA-Signature**](a-dsasignature.md)                                        | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**DS-Core-Propagierungsdaten**](a-dscorepropagationdata.md)                    | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Erweiterungsname**](a-extensionname.md)                                      | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Facsimile-Telephone-Number**](a-facsimiletelephonenumber.md)               | Falsch     | **Organisationseinheit**         |
| [**Flaggen**](a-flags.md)                                                       | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**From-Entry**](a-fromentry.md)                                              | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)                  | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                      | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                     | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**GP-Link**](a-gplink.md)                                                    | Falsch     | **Organisationseinheit**         |
| [**GP-Optionen**](a-gpoptions.md)                                              | Falsch     | **Organisationseinheit**         |
| [**Instanztyp**](a-instancetype.md)                                        | Richtig      | [**Nach oben**](c-top.md)<br/> |
| [**International-ISDN-Number**](a-internationalisdnnumber.md)                 | Falsch     | **Organisationseinheit**         |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                  | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Is-Deleted**](a-isdeleted.md)                                              | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Is-Member-of-DL**](a-memberof.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                             | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Last-Known-Parent**](a-lastknownparent.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Locality-Name**](a-l.md)                                                   | Falsch     | **Organisationseinheit**         |
| [**Logo**](a-thumbnaillogo.md)                                                | Falsch     | **Organisationseinheit**         |
| [**Verwaltet von**](a-managedby.md)                                              | Falsch     | **Organisationseinheit**         |
| [**Verwaltete Objekte**](a-managedobjects.md)                                    | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Mastered-By**](a-masteredby.md)                                            | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Modify-Time-Stamp**](a-modifytimestamp.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                    | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                    | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-COM-UserPartitionSetLink**](a-mscom-userpartitionsetlink.md)            | Falsch     | **Organisationseinheit**         |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)            | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md)    | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md) | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)         | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                      | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Is-Domain-For**](a-msds-isdomainfor.md)                              | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-is-full-replica-for**](a-msds-isfullreplicafor.md)                   | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-is-partial-replica-for**](a-msds-ispartialreplicafor.md)             | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                            | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Members-for-Az-Role-BL**](a-msds-membersforazrolebl.md)              | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                          | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)       | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)     | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)  | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-NC-Type**](a-msds-nctype.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                            | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                  | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Operations-for-Az-Role-BL**](a-msds-operationsforazrolebl.md)        | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Operations-for-Az-Task-BL**](a-msds-operationsforaztaskbl.md)        | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                           | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-PSO-Applied**](a-msds-psoapplied.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)         | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                 | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Revealed-DSAs**](a-msds-revealeddsas.md)                             | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Revealed-List-BL**](a-msds-revealedlistbl.md)                        | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Tasks-for-Az-Role-BL**](a-msds-tasksforazrolebl.md)                  | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Tasks-for-Az-Task-BL**](a-msds-tasksforaztaskbl.md)                  | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                     | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Non-Security-Member-BL**](a-nonsecuritymemberbl.md)                        | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                       | Richtig      | [**Nach oben**](c-top.md)<br/> |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Objektkategorie**](a-objectcategory.md)                                    | Richtig      | [**Nach oben**](c-top.md)<br/> |
| [**Object-Class**](a-objectclass.md)                                          | Richtig      | [**Nach oben**](c-top.md)<br/> |
| [**Objekt-GUID**](a-objectguid.md)                                            | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Object-Version**](a-objectversion.md)                                      | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Organisationseinheitsname**](a-ou.md)                                       | Richtig      | **Organisationseinheit**         |
| [**Andere bekannte Objekte**](a-otherwellknownobjects.md)                    | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)      | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                         | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Physical-Delivery-Office-Name**](a-physicaldeliveryofficename.md)          | Falsch     | **Organisationseinheit**         |
| [**Mögliche 100000000000**](a-possibleinferiors.md)                              | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Postal-Address**](a-postaladdress.md)                                      | Falsch     | **Organisationseinheit**         |
| [**Postleitzahl**](a-postalcode.md)                                            | Falsch     | **Organisationseinheit**         |
| [**Post-Office-Box**](a-postofficebox.md)                                     | Falsch     | **Organisationseinheit**         |
| [**Preferred-Delivery-Method**](a-preferreddeliverymethod.md)                 | Falsch     | **Organisationseinheit**         |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                             | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Proxyadressen**](a-proxyaddresses.md)                                    | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Query-Policy-BL**](a-querypolicybl.md)                                     | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Rdn**](a-name.md)                                                          | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Registrierte Adresse**](a-registeredaddress.md)                              | Falsch     | **Organisationseinheit**         |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                      | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                           | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Berichte**](a-directreports.md)                                             | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Reps-From**](a-repsfrom.md)                                                | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Reps-To**](a-repsto.md)                                                    | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Revision**](a-revision.md)                                                 | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                             | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Search-Guide**](a-searchguide.md)                                          | Falsch     | **Organisationseinheit**         |
| [**Siehe auch**](a-seealso.md)                                                  | Falsch     | **Organisationseinheit**         |
| [**Server-Reference-BL**](a-serverreferencebl.md)                             | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)                 | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Site-Object-BL**](a-siteobjectbl.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**State-Or-Province-Name**](a-st.md)                                         | Falsch     | **Organisationseinheit**         |
| [**Adresse der Straße**](a-street.md)                                             | Falsch     | **Organisationseinheit**         |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                     | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Sub-Refs**](a-subrefs.md)                                                  | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                               | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Systemflags**](a-systemflags.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Telefonnummer**](a-telephonenumber.md)                                  | Falsch     | **Organisationseinheit**         |
| [**Teletex-Terminal-Identifier**](a-teletexterminalidentifier.md)             | Falsch     | **Organisationseinheit**         |
| [**Telex-Number**](a-telexnumber.md)                                          | Falsch     | **Organisationseinheit**         |
| [**Text-Country**](a-co.md)                                                   | Falsch     | **Organisationseinheit**         |
| [**UPN-Suffixe**](a-upnsuffixes.md)                                          | Falsch     | **Organisationseinheit**         |
| [**Benutzerkennwort**](a-userpassword.md)                                        | Falsch     | **Organisationseinheit**         |
| [**USN geändert**](a-usnchanged.md)                                            | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**USN-erstellt**](a-usncreated.md)                                            | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**USN-DSA-last-obj-removed**](a-usndsalastobjremoved.md)                     | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**USN-Intersite**](a-usnintersite.md)                                        | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                    | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**USN-Quelle**](a-usnsource.md)                                              | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Wbem-Pfad**](a-wbempath.md)                                                | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Bekannte Objekte**](a-wellknownobjects.md)                               | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Bei Änderung**](a-whenchanged.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Bei der Erstellung**](a-whencreated.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**WWW-Startseite**](a-wwwhomepage.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**WWW-Page-Other**](a-url.md)                                                | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**X121-Address**](a-x121address.md)                                          | Falsch     | **Organisationseinheit**         |



## <a name="windows-server-2008-extended-rights"></a>Windows Erweiterte Rechte für Server 2008

Diese Klasse enthält die folgenden erweiterten Rechte für Windows Server 2008:



| Allgemeiner Name                                                |
|------------------------------------------------------------|
| [**Generate-RSoP-Planning**](r-generate-rsop-planning.md) |
| [**Generate-RSoP-Logging**](r-generate-rsop-logging.md)   |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2

-   [Attribute](#windows-server-2008-r2-attributes)
-   [Erweiterte Rechte](#windows-server-2008-r2-extended-rights)



| Eingabe | Wert |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falsch                                                                                                                                                                                                                                                                                                                                                                         |
| Object-Category             | 1                                                                                                                                                                                                                                                                                                                                                                             |
| Default-Object-Category     | \-                                                                                                                                                                                                                                                                                                                                                                            |
| Governs-Id                  | 2.5.6.5                                                                                                                                                                                                                                                                                                                                                                       |
| Default-Hiding-Value        | 0                                                                                                                                                                                                                                                                                                                                                                             |
| Rdn-Att-Id                  | [**Name der Organisationseinheit**](a-ou.md)<br/>                                                                                                                                                                                                                                                                                                                           |
| Unterklasse von                 | [**Nach oben**](c-top.md)<br/>                                                                                                                                                                                                                                                                                                                                               |
| Mögliche Übergeordnete          | [**Land**](c-country.md) der [**Organisation**](c-organization.md)der **Domänen-DNS-Organisationseinheit** [](c-domaindns.md)                                                                                                                                                                                                                                                    |
| Zusätzlich           | \-                                                                                                                                                                                                                                                                                                                                                                            |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                                  |
| Standardsicherheitsdeskriptor | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(OA;; CCDC;bf967a86-0de6-11d0-a285-00aa003049e2;; AO)(OA;; CCDC;bf967aba-0de6-11d0-a285-00aa003049e2;; AO)(OA;; CCDC;bf967a9c-0de6-11d0-a285-00aa003049e2;; AO)(OA;; CCDC;bf967aa8-0de6-11d0-a285-00aa003049e2;; PO)(A;; RPLCLORC;;; AU)(A;; LCRPLORC;;; ED)(OA;; CCDC;4828CC14-1437-45bc-9B07-AD6F015E5F28;; AO) |
| System-Flags                | 0x00000010                                                                                                                                                                                                                                                                                                                                                                    |



## <a name="windows-server-2008-r2-attributes"></a>Windows Server 2008 R2-Attribute

Diese Klasse enthält die folgenden Attribute für Windows Server 2008 R2:



| attribute                                                                        | Obligatorisch. | Abgeleitet von                    |
|----------------------------------------------------------------------------------|-----------|---------------------------------|
| [**Admin-Description**](a-admindescription.md)                                  | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Administratoranzeigename**](a-admindisplayname.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Allowed-Attributes**](a-allowedattributes.md)                                | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)             | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                           | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)        | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                    | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Business-Category**](a-businesscategory.md)                                  | Falsch     | **Organisationseinheit**         |
| [**Kanonischer Name**](a-canonicalname.md)                                        | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Common-Name**](a-cn.md)                                                      | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Ländercode**](a-countrycode.md)                                            | Falsch     | **Organisationseinheit**         |
| [**Country-Name**](a-c.md)                                                      | Falsch     | **Organisationseinheit**         |
| [**Create-Time-Stamp**](a-createtimestamp.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Default-Group**](a-defaultgroup.md)                                          | Falsch     | **Organisationseinheit**         |
| [**Beschreibung**](a-description.md)                                             | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Desktop-Profile**](a-desktopprofile.md)                                      | Falsch     | **Organisationseinheit**         |
| [**Destination-Indicator**](a-destinationindicator.md)                          | Falsch     | **Organisationseinheit**         |
| [**Anzeigename**](a-displayname.md)                                            | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Display-Name-Printable**](a-displaynameprintable.md)                         | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**DSA-Signature**](a-dsasignature.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**DS-Core-Propagierungsdaten**](a-dscorepropagationdata.md)                      | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Extension-Name**](a-extensionname.md)                                        | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Facsimile-Telephone-Number**](a-facsimiletelephonenumber.md)                 | Falsch     | **Organisationseinheit**         |
| [**Flaggen**](a-flags.md)                                                         | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**From-Entry**](a-fromentry.md)                                                | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)                    | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                        | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**GP-Link**](a-gplink.md)                                                      | Falsch     | **Organisationseinheit**         |
| [**GP-Options**](a-gpoptions.md)                                                | Falsch     | **Organisationseinheit**         |
| [**Instanztyp**](a-instancetype.md)                                          | Richtig      | [**Nach oben**](c-top.md)<br/> |
| [**International-ISDN-Number**](a-internationalisdnnumber.md)                   | Falsch     | **Organisationseinheit**         |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                    | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Is-Deleted**](a-isdeleted.md)                                                | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Is-Member-of-DL**](a-memberof.md)                                            | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                               | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Wird wiederverwendet**](a-isrecycled.md)                                              | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Last-Known-Parent**](a-lastknownparent.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Locality-Name**](a-l.md)                                                     | Falsch     | **Organisationseinheit**         |
| [**Logo**](a-thumbnaillogo.md)                                                  | Falsch     | **Organisationseinheit**         |
| [**Verwaltet von**](a-managedby.md)                                                | Falsch     | **Organisationseinheit**         |
| [**Verwaltete Objekte**](a-managedobjects.md)                                      | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Mastered-By**](a-masteredby.md)                                              | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Modify-Time-Stamp**](a-modifytimestamp.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                      | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                      | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-COM-UserPartitionSetLink**](a-mscom-userpartitionsetlink.md)              | Falsch     | **Organisationseinheit**         |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)              | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                  | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md)      | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md)   | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)           | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                        | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Enabled-Feature-BL**](a-msds-enabledfeaturebl.md)                      | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)             | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Is-Domain-For**](a-msds-isdomainfor.md)                                | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-is-full-replica-for**](a-msds-isfullreplicafor.md)                     | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-is-partial-replica-for**](a-msds-ispartialreplicafor.md)               | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                              | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                              | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-local-Effective-Deletion-Time**](a-msds-localeffectivedeletiontime.md) | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-local-Effective-Recycle-Time**](a-msds-localeffectiverecycletime.md)   | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Members-for-Az-Role-BL**](a-msds-membersforazrolebl.md)                | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                            | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)         | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)       | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)    | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-NC-Type**](a-msds-nctype.md)                                           | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                              | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                    | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-OIDToGroup-Link-BL**](a-msds-oidtogrouplinkbl.md)                      | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)          | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)          | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                             | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-PSO-Applied**](a-msds-psoapplied.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)           | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                   | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Revealed-DSAs**](a-msds-revealeddsas.md)                               | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Revealed-List-BL**](a-msds-revealedlistbl.md)                          | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)                    | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)                    | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                            | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                       | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Non-Security-Member-BL**](a-nonsecuritymemberbl.md)                          | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                         | Richtig      | [**Nach oben**](c-top.md)<br/> |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                     | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Objektkategorie**](a-objectcategory.md)                                      | Richtig      | [**Nach oben**](c-top.md)<br/> |
| [**Object-Class**](a-objectclass.md)                                            | Richtig      | [**Nach oben**](c-top.md)<br/> |
| [**Objekt-GUID**](a-objectguid.md)                                              | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Object-Version**](a-objectversion.md)                                        | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Organisationseinheitsname**](a-ou.md)                                         | Richtig      | **Organisationseinheit**         |
| [**Andere bekannte Objekte**](a-otherwellknownobjects.md)                      | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)        | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                           | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Physical-Delivery-Office-Name**](a-physicaldeliveryofficename.md)            | Falsch     | **Organisationseinheit**         |
| [**Mögliche Hindernisse**](a-possibleinferiors.md)                                | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Postanschrift**](a-postaladdress.md)                                        | Falsch     | **Organisationseinheit**         |
| [**Postleitzahl**](a-postalcode.md)                                              | Falsch     | **Organisationseinheit**         |
| [**Post-Office-Box**](a-postofficebox.md)                                       | Falsch     | **Organisationseinheit**         |
| [**Preferred-Delivery-Method**](a-preferreddeliverymethod.md)                   | Falsch     | **Organisationseinheit**         |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                               | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Proxyadressen**](a-proxyaddresses.md)                                      | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Query-Policy-BL**](a-querypolicybl.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Rdn**](a-name.md)                                                            | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Registrierte Adresse**](a-registeredaddress.md)                                | Falsch     | **Organisationseinheit**         |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                        | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                             | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Berichte**](a-directreports.md)                                               | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Reps-From**](a-repsfrom.md)                                                  | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Reps-To**](a-repsto.md)                                                      | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Revision**](a-revision.md)                                                   | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                               | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Search-Guide**](a-searchguide.md)                                            | Falsch     | **Organisationseinheit**         |
| [**Siehe auch**](a-seealso.md)                                                    | Falsch     | **Organisationseinheit**         |
| [**Server-Reference-BL**](a-serverreferencebl.md)                               | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Nur in erweiterter Ansicht anzeigen**](a-showinadvancedviewonly.md)                   | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Site-Object-BL**](a-siteobjectbl.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**State-or-Province-Name**](a-st.md)                                           | Falsch     | **Organisationseinheit**         |
| [**Adresse der Straße**](a-street.md)                                               | Falsch     | **Organisationseinheit**         |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                       | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Sub-Refs**](a-subrefs.md)                                                    | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Systemflags**](a-systemflags.md)                                            | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Telefonnummer**](a-telephonenumber.md)                                    | Falsch     | **Organisationseinheit**         |
| [**Teletex-Terminal-Identifier**](a-teletexterminalidentifier.md)               | Falsch     | **Organisationseinheit**         |
| [**Telex-Number**](a-telexnumber.md)                                            | Falsch     | **Organisationseinheit**         |
| [**Text-Country**](a-co.md)                                                     | Falsch     | **Organisationseinheit**         |
| [**UPN-Suffixe**](a-upnsuffixes.md)                                            | Falsch     | **Organisationseinheit**         |
| [**Benutzerkennwort**](a-userpassword.md)                                          | Falsch     | **Organisationseinheit**         |
| [**USN-Changed**](a-usnchanged.md)                                              | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**VON USN erstellt**](a-usncreated.md)                                              | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                       | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**USN-Intersite**](a-usnintersite.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                      | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**USN-Quelle**](a-usnsource.md)                                                | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Wbem-Path**](a-wbempath.md)                                                  | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Bekannte Objekte**](a-wellknownobjects.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Wenn geändert**](a-whenchanged.md)                                            | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Wenn erstellt**](a-whencreated.md)                                            | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**WWW-Homepage**](a-wwwhomepage.md)                                           | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**WWW-Page-Other**](a-url.md)                                                  | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**X121-Adresse**](a-x121address.md)                                            | Falsch     | **Organisationseinheit**         |



## <a name="windows-server-2008-r2-extended-rights"></a>Windows Erweiterte Server 2008 R2-Rechte

Diese Klasse enthält die folgenden erweiterten Rechte für Windows Server 2008 R2:



| Allgemeiner Name                                                |
|------------------------------------------------------------|
| [**Generate-RSoP-Planning**](r-generate-rsop-planning.md) |
| [**Generate-RSoP-Logging**](r-generate-rsop-logging.md)   |



## <a name="windows-server-2012"></a>Windows Server 2012

-   [Attribute](#windows-server-2012-attributes)
-   [Erweiterte Rechte](#windows-server-2012-extended-rights)



| Eingabe | Wert |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falsch                                                                                                                                                                                                                                                                                                                                                                         |
| Object-Category             | 1                                                                                                                                                                                                                                                                                                                                                                             |
| Default-Object-Category     | \-                                                                                                                                                                                                                                                                                                                                                                            |
| Governs-Id                  | 2.5.6.5                                                                                                                                                                                                                                                                                                                                                                       |
| Default-Hiding-Value        | 0                                                                                                                                                                                                                                                                                                                                                                             |
| Rdn-Att-Id                  | [**Organisationseinheitsname**](a-ou.md)<br/>                                                                                                                                                                                                                                                                                                                           |
| Unterklasse von                 | [**Nach oben**](c-top.md)<br/>                                                                                                                                                                                                                                                                                                                                               |
| Mögliche Vorgesetzte          | [**Domain-DNS**](c-domaindns.md)**Organizational-Unit**[**Organization**](c-organization.md)[**Country**](c-country.md)                                                                                                                                                                                                                                                    |
| Zusätzlich           | \-                                                                                                                                                                                                                                                                                                                                                                            |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                                  |
| Standardsicherheitsdeskriptor | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(OA;; CCDC;bf967a86-0de6-11d0-a285-00aa003049e2;; AO)(OA;; CCDC;bf967aba-0de6-11d0-a285-00aa003049e2;; AO)(OA;; CCDC;bf967a9c-0de6-11d0-a285-00aa003049e2;; AO)(OA;; CCDC;bf967aa8-0de6-11d0-a285-00aa003049e2;; PO)(A;; RPLCLORC;;; AU)(A;; LCRPLORC;;; ED)(OA;; CCDC;4828CC14-1437-45bc-9B07-AD6F015E5F28;; AO) |
| System-Flags                | 0x00000010                                                                                                                                                                                                                                                                                                                                                                    |



## <a name="windows-server-2012-attributes"></a>Windows Server 2012 Attribute

Diese Klasse enthält die folgenden Attribute für Windows Server 2012:



| attribute                                                                                    | Obligatorisch. | Abgeleitet von                    |
|----------------------------------------------------------------------------------------------|-----------|---------------------------------|
| [**Admin-Description**](a-admindescription.md)                                              | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Administratoranzeigename**](a-admindisplayname.md)                                             | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Allowed-Attributes**](a-allowedattributes.md)                                            | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)                         | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)                    | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                                | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Business-Category**](a-businesscategory.md)                                              | Falsch     | **Organisationseinheit**         |
| [**Kanonischer Name**](a-canonicalname.md)                                                    | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Allgemeiner Name**](a-cn.md)                                                                  | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Ländercode**](a-countrycode.md)                                                        | Falsch     | **Organisationseinheit**         |
| [**Country-Name**](a-c.md)                                                                  | Falsch     | **Organisationseinheit**         |
| [**Erstellen eines Zeitstempels**](a-createtimestamp.md)                                               | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Standardgruppe**](a-defaultgroup.md)                                                      | Falsch     | **Organisationseinheit**         |
| [**Beschreibung**](a-description.md)                                                         | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Desktopprofil**](a-desktopprofile.md)                                                  | Falsch     | **Organisationseinheit**         |
| [**Zielindikator**](a-destinationindicator.md)                                      | Falsch     | **Organisationseinheit**         |
| [**Anzeigename**](a-displayname.md)                                                        | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Anzeigename– druckbar**](a-displaynameprintable.md)                                     | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**DSA-Signature**](a-dsasignature.md)                                                      | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**DS-Core-Propagierungsdaten**](a-dscorepropagationdata.md)                                  | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Erweiterungsname**](a-extensionname.md)                                                    | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Facsimile-Telephone-Number**](a-facsimiletelephonenumber.md)                             | Falsch     | **Organisationseinheit**         |
| [**Flaggen**](a-flags.md)                                                                     | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**From-Entry**](a-fromentry.md)                                                            | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)                                | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                                    | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                                   | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**GP-Link**](a-gplink.md)                                                                  | Falsch     | **Organisationseinheit**         |
| [**GP-Optionen**](a-gpoptions.md)                                                            | Falsch     | **Organisationseinheit**         |
| [**Instanztyp**](a-instancetype.md)                                                      | Richtig      | [**Nach oben**](c-top.md)<br/> |
| [**International-ISDN-Number**](a-internationalisdnnumber.md)                               | Falsch     | **Organisationseinheit**         |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                                | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Is-Deleted**](a-isdeleted.md)                                                            | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Is-Member-of-DL**](a-memberof.md)                                                        | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                                           | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Wird wiederverwendet**](a-isrecycled.md)                                                          | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Last-Known-Parent**](a-lastknownparent.md)                                               | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Locality-Name**](a-l.md)                                                                 | Falsch     | **Organisationseinheit**         |
| [**Logo**](a-thumbnaillogo.md)                                                              | Falsch     | **Organisationseinheit**         |
| [**Verwaltet von**](a-managedby.md)                                                            | Falsch     | **Organisationseinheit**         |
| [**Verwaltete Objekte**](a-managedobjects.md)                                                  | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Mastered-By**](a-masteredby.md)                                                          | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Modify-Time-Stamp**](a-modifytimestamp.md)                                               | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                                  | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                                  | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-COM-UserPartitionSetLink**](a-mscom-userpartitionsetlink.md)                          | Falsch     | **Organisationseinheit**         |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)                          | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                              | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md)                  | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md)               | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Claim-Shares-Possible-Values-with-BL**](a-msds-claimsharespossiblevalueswithbl.md) | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)                       | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                                    | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Enabled-Feature-BL**](a-msds-enabledfeaturebl.md)                                  | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)                         | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Is-Domain-For**](a-msds-isdomainfor.md)                                            | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-is-full-replica-for**](a-msds-isfullreplicafor.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-is-partial-replica-for**](a-msds-ispartialreplicafor.md)                           | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Is-Primary-Computer-For**](a-msds-isprimarycomputerfor.md)                         | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-local-Effective-Deletion-Time**](a-msds-localeffectivedeletiontime.md)             | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-local-Effective-Recycle-Time**](a-msds-localeffectiverecycletime.md)               | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                                               | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Members-for-Az-Role-BL**](a-msds-membersforazrolebl.md)                            | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Members-of-Resource-Property-List-BL**](a-msds-membersofresourcepropertylistbl.md) | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                                        | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)                     | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)                   | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)                | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-NC-Type**](a-msds-nctype.md)                                                       | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                                | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-OIDToGroup-Link-BL**](a-msds-oidtogrouplinkbl.md)                                  | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)                      | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)                      | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-PSO-Applied**](a-msds-psoapplied.md)                                               | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)                       | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                               | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Revealed-DSAs**](a-msds-revealeddsas.md)                                           | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Revealed-List-BL**](a-msds-revealedlistbl.md)                                      | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)                                | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)                                | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-TDO-Egress-BL**](a-msds-tdoegressbl.md)                                            | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-TDO-Ingress-BL**](a-msds-tdoingressbl.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Value-Type-Reference-BL**](a-msds-valuetypereferencebl.md)                         | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                                        | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                                     | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Non-Security-Member-BL**](a-nonsecuritymemberbl.md)                                      | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                                     | Richtig      | [**Nach oben**](c-top.md)<br/> |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                                 | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Objektkategorie**](a-objectcategory.md)                                                  | Richtig      | [**Nach oben**](c-top.md)<br/> |
| [**Object-Class**](a-objectclass.md)                                                        | Richtig      | [**Nach oben**](c-top.md)<br/> |
| [**Objekt-GUID**](a-objectguid.md)                                                          | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Object-Version**](a-objectversion.md)                                                    | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Organisationseinheitsname**](a-ou.md)                                                     | Richtig      | **Organisationseinheit**         |
| [**Andere bekannte Objekte**](a-otherwellknownobjects.md)                                  | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)                    | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Physical-Delivery-Office-Name**](a-physicaldeliveryofficename.md)                        | Falsch     | **Organisationseinheit**         |
| [**Mögliche 100000000000**](a-possibleinferiors.md)                                            | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Postal-Address**](a-postaladdress.md)                                                    | Falsch     | **Organisationseinheit**         |
| [**Postleitzahl**](a-postalcode.md)                                                          | Falsch     | **Organisationseinheit**         |
| [**Post-Office-Box**](a-postofficebox.md)                                                   | Falsch     | **Organisationseinheit**         |
| [**Preferred-Delivery-Method**](a-preferreddeliverymethod.md)                               | Falsch     | **Organisationseinheit**         |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                                           | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Proxyadressen**](a-proxyaddresses.md)                                                  | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Query-Policy-BL**](a-querypolicybl.md)                                                   | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Rdn**](a-name.md)                                                                        | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Registrierte Adresse**](a-registeredaddress.md)                                            | Falsch     | **Organisationseinheit**         |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                                    | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Berichte**](a-directreports.md)                                                           | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Reps-From**](a-repsfrom.md)                                                              | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Reps-To**](a-repsto.md)                                                                  | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Revision**](a-revision.md)                                                               | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                                           | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Search-Guide**](a-searchguide.md)                                                        | Falsch     | **Organisationseinheit**         |
| [**Siehe auch**](a-seealso.md)                                                                | Falsch     | **Organisationseinheit**         |
| [**Server-Reference-BL**](a-serverreferencebl.md)                                           | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Nur in erweiterter Ansicht anzeigen**](a-showinadvancedviewonly.md)                               | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Site-Object-BL**](a-siteobjectbl.md)                                                     | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**State-or-Province-Name**](a-st.md)                                                       | Falsch     | **Organisationseinheit**         |
| [**Adresse der Straße**](a-street.md)                                                           | Falsch     | **Organisationseinheit**         |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Sub-Refs**](a-subrefs.md)                                                                | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                             | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Systemflags**](a-systemflags.md)                                                        | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Telefonnummer**](a-telephonenumber.md)                                                | Falsch     | **Organisationseinheit**         |
| [**Teletex-Terminal-Identifier**](a-teletexterminalidentifier.md)                           | Falsch     | **Organisationseinheit**         |
| [**Telex-Number**](a-telexnumber.md)                                                        | Falsch     | **Organisationseinheit**         |
| [**Text-Country**](a-co.md)                                                                 | Falsch     | **Organisationseinheit**         |
| [**UPN-Suffixe**](a-upnsuffixes.md)                                                        | Falsch     | **Organisationseinheit**         |
| [**Benutzerkennwort**](a-userpassword.md)                                                      | Falsch     | **Organisationseinheit**         |
| [**USN geändert**](a-usnchanged.md)                                                          | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**USN-erstellt**](a-usncreated.md)                                                          | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**USN-DSA-last-obj-removed**](a-usndsalastobjremoved.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**USN-Intersite**](a-usnintersite.md)                                                      | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                                  | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**USN-Quelle**](a-usnsource.md)                                                            | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Wbem-Path**](a-wbempath.md)                                                              | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Bekannte Objekte**](a-wellknownobjects.md)                                             | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Wenn geändert**](a-whenchanged.md)                                                        | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Wenn erstellt**](a-whencreated.md)                                                        | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**WWW-Homepage**](a-wwwhomepage.md)                                                       | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**WWW-Page-Other**](a-url.md)                                                              | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**X121-Adresse**](a-x121address.md)                                                        | Falsch     | **Organisationseinheit**         |



## <a name="windows-server-2012-extended-rights"></a>Windows Server 2012 Erweiterte Rechte

Diese Klasse enthält die folgenden erweiterten Rechte für Windows Server 2012:



| Allgemeiner Name                                                |
|------------------------------------------------------------|
| [**Generate-RSoP-Planning**](r-generate-rsop-planning.md) |
| [**Generate-RSoP-Logging**](r-generate-rsop-logging.md)   |



 

 





