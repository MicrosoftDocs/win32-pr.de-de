---
title: Organizational-Person-Klasse
description: Diese Klasse wird für Objekte verwendet, die Organisationsinformationen zu einem Benutzer enthalten, z. B. Mitarbeiternummer, Abteilung, Vorgesetzter, Titel, Büroadresse usw.
ms.assetid: dbcecb0d-e7ab-4005-82ad-5ffe9b06a380
ms.tgt_platform: multiple
keywords:
- Organizational-Person Ad-Schema der Klasse
- organizationalPerson-Klasse AD-Schema
topic_type:
- apiref
api_name:
- Organizational-Person
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba9be35cfca3d08336c8b75bcb9a7f21fc2139e835fc6b74686e7f1e0a8a4202
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119753200"
---
# <a name="organizational-person-class"></a>Organizational-Person-Klasse

Diese Klasse wird für Objekte verwendet, die Organisationsinformationen zu einem Benutzer enthalten, z. B. Mitarbeiternummer, Abteilung, Vorgesetzter, Titel, Büroadresse usw.



| Eingabe | Wert |
|-------------------|--------------------------------------|
| CN                | Unternehmensperson                |
| Ldap-Anzeigename | organizationalPerson                 |
| Aktualisieren von Berechtigungen  | Jeder kann dieses Objekt aktualisieren.       |
| Updatehäufigkeit  | \-                                   |
| Schema-ID-GUID    | bf967aa4-0de6-11d0-a285-00aa003049e2 |



## <a name="implementations"></a>Implementierungen

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
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
| Default-Hiding-Value        | 0                                                                                            |
| Rdn-Att-Id                  | [**Allgemeiner Name**](a-cn.md)<br/>                                                       |
| Unterklasse von                 | [**Person**](c-person.md)<br/>                                                        |
| Mögliche Übergeordnete          | [**Container**](c-container.md)                                                             |
| Zusätzlich           | \-                                                                                           |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                 |
| Standardsicherheitsdeskriptor | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;;; AU) |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-2000-server-attributes"></a>Windows 2000-Serverattribute

Diese Klasse enthält die folgenden Attribute für Windows 2000 Server:



| attribute                                                                 | Obligatorisch. | Abgeleitet von                                                          |
|---------------------------------------------------------------------------|-----------|-----------------------------------------------------------------------|
| [**Adresse**](a-streetaddress.md)                                        | False     | **Unternehmensperson**                                             |
| [**Address-Home**](a-homepostaladdress.md)                               | False     | **Unternehmensperson**                                             |
| [**Administratorbeschreibung**](a-admindescription.md)                           | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Admin-Display-Name**](a-admindisplayname.md)                          | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Allowed-Attributes**](a-allowedattributes.md)                         | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)      | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                    | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md) | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Assistent**](a-assistant.md)                                          | False     | **Unternehmensperson**                                             |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)             | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Kanonischer Name**](a-canonicalname.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Allgemeiner Name**](a-cn.md)                                               | True      | [**Person**](c-person.md)<br/> [**Nach oben**](c-top.md)<br/> |
| [**Unternehmen**](a-company.md)                                              | False     | **Unternehmensperson**                                             |
| [**Ländercode**](a-countrycode.md)                                     | False     | **Unternehmensperson**                                             |
| [**Country-Name**](a-c.md)                                               | False     | **Unternehmensperson**                                             |
| [**Create-Time-Stamp**](a-createtimestamp.md)                            | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Department**](a-department.md)                                        | False     | **Unternehmensperson**                                             |
| [**Beschreibung**](a-description.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Destination-Indicator**](a-destinationindicator.md)                   | False     | **Unternehmensperson**                                             |
| [**Anzeigename**](a-displayname.md)                                     | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Display-Name-Printable**](a-displaynameprintable.md)                  | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Division**](a-division.md)                                            | False     | **Unternehmensperson**                                             |
| [**DSA-Signature**](a-dsasignature.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**DS-Core-Propagierungsdaten**](a-dscorepropagationdata.md)               | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**E-Mail-Adressen**](a-mail.md)                                        | False     | **Unternehmensperson**                                             |
| [**Mitarbeiter-ID**](a-employeeid.md)                                       | False     | **Unternehmensperson**                                             |
| [**Extension-Name**](a-extensionname.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Facsimile-Telephone-Number**](a-facsimiletelephonenumber.md)          | False     | **Unternehmensperson**                                             |
| [**Flaggen**](a-flags.md)                                                  | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**From-Entry**](a-fromentry.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)             | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                 | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Generation-Qualifier**](a-generationqualifier.md)                     | False     | **Unternehmensperson**                                             |
| [**Given-Name**](a-givenname.md)                                         | False     | **Unternehmensperson**                                             |
| [**Initialen**](a-initials.md)                                            | False     | **Unternehmensperson**                                             |
| [**Instanztyp**](a-instancetype.md)                                   | True      | [**Nach oben**](c-top.md)<br/>                                       |
| [**International-ISDN-Number**](a-internationalisdnnumber.md)            | False     | **Unternehmensperson**                                             |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)             | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Is-Deleted**](a-isdeleted.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Is-Member-of-DL**](a-memberof.md)                                     | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                        | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Letztes bekanntes übergeordnetes Element**](a-lastknownparent.md)                            | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Locality-Name**](a-l.md)                                              | False     | **Unternehmensperson**                                             |
| [**Logo**](a-thumbnaillogo.md)                                           | False     | **Unternehmensperson**                                             |
| [**Verwaltete Objekte**](a-managedobjects.md)                               | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Manager**](a-manager.md)                                              | False     | **Unternehmensperson**                                             |
| [**Mastered By**](a-masteredby.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**MHS-OR-Adresse**](a-mhsoraddress.md)                                  | False     | **Unternehmensperson**                                             |
| [**Modify-Time-Stamp**](a-modifytimestamp.md)                            | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)    | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                 | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                  | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Non-Security-Member-BL**](a-nonsecuritymemberbl.md)                   | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                  | True      | [**Nach oben**](c-top.md)<br/>                                       |
| [**Obj-Dist-Name**](a-distinguishedname.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Objektkategorie**](a-objectcategory.md)                               | True      | [**Nach oben**](c-top.md)<br/>                                       |
| [**Object-Class**](a-objectclass.md)                                     | True      | [**Nach oben**](c-top.md)<br/>                                       |
| [**Objekt-GUID**](a-objectguid.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Object-Version**](a-objectversion.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Organisationseinheitsname**](a-ou.md)                                  | False     | **Unternehmensperson**                                             |
| [**Organisationsname**](a-o.md)                                          | False     | **Unternehmensperson**                                             |
| [**Sonstiges Postfach**](a-othermailbox.md)                                   | False     | **Unternehmensperson**                                             |
| [**Other-Name**](a-middlename.md)                                        | False     | **Unternehmensperson**                                             |
| [**Andere bekannte Objekte**](a-otherwellknownobjects.md)               | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md) | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                    | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Personal-Title**](a-personaltitle.md)                                 | False     | **Unternehmensperson**                                             |
| [**Telefon-Fax-Other**](a-otherfacsimiletelephonenumber.md)                | False     | **Unternehmensperson**                                             |
| [**Telefon-Home-Other**](a-otherhomephone.md)                              | False     | **Unternehmensperson**                                             |
| [**Telefon-Home-Primary**](a-homephone.md)                                 | False     | **Unternehmensperson**                                             |
| [**Telefon-Ip-Other**](a-otheripphone.md)                                  | False     | **Unternehmensperson**                                             |
| [**Telefon-Ip-Primary**](a-ipphone.md)                                     | False     | **Unternehmensperson**                                             |
| [**Telefon-ISDN-Primary**](a-primaryinternationalisdnnumber.md)            | False     | **Unternehmensperson**                                             |
| [**Telefon-Mobile-Other**](a-othermobile.md)                               | False     | **Unternehmensperson**                                             |
| [**Telefon-Mobile-Primary**](a-mobile.md)                                  | False     | **Unternehmensperson**                                             |
| [**Telefon-Office-Other**](a-othertelephone.md)                            | False     | **Unternehmensperson**                                             |
| [**Telefon-Pager-Other**](a-otherpager.md)                                 | False     | **Unternehmensperson**                                             |
| [**Telefon-Pager-Primary**](a-pager.md)                                    | False     | **Unternehmensperson**                                             |
| [**Physical-Delivery-Office-Name**](a-physicaldeliveryofficename.md)     | False     | **Unternehmensperson**                                             |
| [**Bild**](a-thumbnailphoto.md)                                       | False     | **Unternehmensperson**                                             |
| [**Mögliche Hindernisse**](a-possibleinferiors.md)                         | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Postanschrift**](a-postaladdress.md)                                 | False     | **Unternehmensperson**                                             |
| [**Postleitzahl**](a-postalcode.md)                                       | False     | **Unternehmensperson**                                             |
| [**Post-Office-Box**](a-postofficebox.md)                                | False     | **Unternehmensperson**                                             |
| [**Preferred-Delivery-Method**](a-preferreddeliverymethod.md)            | False     | **Unternehmensperson**                                             |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                        | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Proxyadressen**](a-proxyaddresses.md)                               | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Query-Policy-BL**](a-querypolicybl.md)                                | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Rdn**](a-name.md)                                                     | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Registrierte Adresse**](a-registeredaddress.md)                         | False     | **Unternehmensperson**                                             |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                 | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                      | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Berichte**](a-directreports.md)                                        | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Reps-From**](a-repsfrom.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Reps-To**](a-repsto.md)                                               | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Revision**](a-revision.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                        | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Siehe auch**](a-seealso.md)                                             | False     | [**Person**](c-person.md)<br/>                                 |
| [**Server-Reference-BL**](a-serverreferencebl.md)                        | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Nur in erweiterter Ansicht anzeigen**](a-showinadvancedviewonly.md)            | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Site-Object-BL**](a-siteobjectbl.md)                                  | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**State-or-Province-Name**](a-st.md)                                    | False     | **Unternehmensperson**                                             |
| [**Adresse der Straße**](a-street.md)                                        | False     | **Unternehmensperson**                                             |
| [**Sub-Refs**](a-subrefs.md)                                             | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                          | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Nachname**](a-sn.md)                                                   | False     | [**Person**](c-person.md)<br/>                                 |
| [**Systemflags**](a-systemflags.md)                                     | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Telefonnummer**](a-telephonenumber.md)                             | False     | [**Person**](c-person.md)<br/>                                 |
| [**Teletex-Terminal-Identifier**](a-teletexterminalidentifier.md)        | False     | **Unternehmensperson**                                             |
| [**Telex-Number**](a-telexnumber.md)                                     | False     | **Unternehmensperson**                                             |
| [**Telex-Primary**](a-primarytelexnumber.md)                             | False     | **Unternehmensperson**                                             |
| [**Text-Country**](a-co.md)                                              | False     | **Unternehmensperson**                                             |
| [**Titel**](a-title.md)                                                  | False     | **Unternehmensperson**                                             |
| [**Benutzerkommentar**](a-comment.md)                                         | False     | **Unternehmensperson**                                             |
| [**Benutzerkennwort**](a-userpassword.md)                                   | False     | [**Person**](c-person.md)<br/>                                 |
| [**USN-Changed**](a-usnchanged.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**VON USN erstellt**](a-usncreated.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**USN-Intersite**](a-usnintersite.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                               | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**USN-Quelle**](a-usnsource.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Wbem-Path**](a-wbempath.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Bekannte Objekte**](a-wellknownobjects.md)                          | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Wenn geändert**](a-whenchanged.md)                                     | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Wenn erstellt**](a-whencreated.md)                                     | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**WWW-Homepage**](a-wwwhomepage.md)                                    | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**WWW-Page-Other**](a-url.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**X121-Adresse**](a-x121address.md)                                     | False     | **Unternehmensperson**                                             |



## <a name="windows-server-2003"></a>Windows Server 2003

-   [Attribute](#windows-server-2003-attributes)



| Eingabe | Wert |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | False                                                                                                                     |
| Object-Category             | 0                                                                                                                         |
| Default-Object-Category     | [**Person**](c-person.md)<br/>                                                                                     |
| Governs-Id                  | 2.5.6.7                                                                                                                   |
| Default-Hiding-Value        | 1                                                                                                                         |
| Rdn-Att-Id                  | [**Common-Name**](a-cn.md)<br/>                                                                                    |
| Unterklasse von                 | [**Person**](c-person.md)<br/>                                                                                     |
| Mögliche Vorgesetzte          | [**Organisationseinheit**](c-container.md)[**der**](c-organization.md)[**Containerorganisation**](c-organizationalunit.md) |
| Zusätzlich           | \-                                                                                                                        |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                                              |
| Standardsicherheitsdeskriptor | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;;; AU)                              |
| System-Flags                | 0x00000010                                                                                                                |



## <a name="windows-server-2003-attributes"></a>Windows Server 2003-Attribute

Diese Klasse enthält die folgenden Attribute für Windows Server 2003:



| attribute                                                                   | Obligatorisch. | Abgeleitet von                                                          |
|-----------------------------------------------------------------------------|-----------|-----------------------------------------------------------------------|
| [**Adresse**](a-streetaddress.md)                                          | False     | **Unternehmensperson**                                             |
| [**Address-Home**](a-homepostaladdress.md)                                 | False     | **Unternehmensperson**                                             |
| [**Admin-Description**](a-admindescription.md)                             | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Administratoranzeigename**](a-admindisplayname.md)                            | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Allowed-Attributes**](a-allowedattributes.md)                           | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)        | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                      | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)   | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Assistent**](a-assistant.md)                                            | False     | **Unternehmensperson**                                             |
| [**attributeCertificateAttribute**](a-attributecertificateattribute.md)    | False     | [**Person**](c-person.md)<br/>                                 |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)               | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Kanonischer Name**](a-canonicalname.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Common-Name**](a-cn.md)                                                 | True      | [**Person**](c-person.md)<br/> [**Nach oben**](c-top.md)<br/> |
| [**Unternehmen**](a-company.md)                                                | False     | **Unternehmensperson**                                             |
| [**Ländercode**](a-countrycode.md)                                       | False     | **Unternehmensperson**                                             |
| [**Country-Name**](a-c.md)                                                 | False     | **Unternehmensperson**                                             |
| [**Create-Time-Stamp**](a-createtimestamp.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Department**](a-department.md)                                          | False     | **Unternehmensperson**                                             |
| [**Beschreibung**](a-description.md)                                        | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Destination-Indicator**](a-destinationindicator.md)                     | False     | **Unternehmensperson**                                             |
| [**Anzeigename**](a-displayname.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Display-Name-Printable**](a-displaynameprintable.md)                    | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Division**](a-division.md)                                              | False     | **Unternehmensperson**                                             |
| [**DSA-Signature**](a-dsasignature.md)                                     | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**DS-Core-Propagierungsdaten**](a-dscorepropagationdata.md)                 | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**E-Mail-Adressen**](a-mail.md)                                          | False     | **Unternehmensperson**                                             |
| [**Mitarbeiter-ID**](a-employeeid.md)                                         | False     | **Unternehmensperson**                                             |
| [**Extension-Name**](a-extensionname.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Facsimile-Telephone-Number**](a-facsimiletelephonenumber.md)            | False     | **Unternehmensperson**                                             |
| [**Flaggen**](a-flags.md)                                                    | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**From-Entry**](a-fromentry.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)               | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                   | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                  | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Generation-Qualifier**](a-generationqualifier.md)                       | False     | **Unternehmensperson**                                             |
| [**Given-Name**](a-givenname.md)                                           | False     | **Unternehmensperson**                                             |
| [**houseIdentifier**](a-houseidentifier.md)                                | False     | **Unternehmensperson**                                             |
| [**Initialen**](a-initials.md)                                              | False     | **Unternehmensperson**                                             |
| [**Instanztyp**](a-instancetype.md)                                     | True      | [**Nach oben**](c-top.md)<br/>                                       |
| [**International-ISDN-Number**](a-internationalisdnnumber.md)              | False     | **Unternehmensperson**                                             |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)               | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Is-Deleted**](a-isdeleted.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Is-Member-of-DL**](a-memberof.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                          | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Letztes bekanntes übergeordnetes Element**](a-lastknownparent.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Locality-Name**](a-l.md)                                                | False     | **Unternehmensperson**                                             |
| [**Logo**](a-thumbnaillogo.md)                                             | False     | **Unternehmensperson**                                             |
| [**Verwaltete Objekte**](a-managedobjects.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Manager**](a-manager.md)                                                | False     | **Unternehmensperson**                                             |
| [**Mastered By**](a-masteredby.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**MHS-OR-Adresse**](a-mhsoraddress.md)                                    | False     | **Unternehmensperson**                                             |
| [**Modify-Time-Stamp**](a-modifytimestamp.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                 | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Allowed-to-Delegate-To**](a-msds-allowedtodelegateto.md)          | False     | **Unternehmensperson**                                             |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md) | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)      | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Members-For-Az-Role-BL**](a-msds-membersforazrolebl.md)           | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                       | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)    | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)  | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                         | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)               | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)     | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)     | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)      | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)              | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)               | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)               | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-Exch-House-Identifier**](a-msexchhouseidentifier.md)                 | False     | **Unternehmensperson**                                             |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                    | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Non-Security-Member-BL**](a-nonsecuritymemberbl.md)                     | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                    | True      | [**Nach oben**](c-top.md)<br/>                                       |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Objektkategorie**](a-objectcategory.md)                                 | True      | [**Nach oben**](c-top.md)<br/>                                       |
| [**Object-Class**](a-objectclass.md)                                       | True      | [**Nach oben**](c-top.md)<br/>                                       |
| [**Objekt-GUID**](a-objectguid.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Object-Version**](a-objectversion.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Organisationseinheitsname**](a-ou.md)                                    | False     | **Unternehmensperson**                                             |
| [**Organisationsname**](a-o.md)                                            | False     | **Unternehmensperson**                                             |
| [**Sonstiges Postfach**](a-othermailbox.md)                                     | False     | **Unternehmensperson**                                             |
| [**Other-Name**](a-middlename.md)                                          | False     | **Unternehmensperson**                                             |
| [**Andere bekannte Objekte**](a-otherwellknownobjects.md)                 | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)   | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                      | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Personal-Title**](a-personaltitle.md)                                   | False     | **Unternehmensperson**                                             |
| [**Telefon-Fax-Other**](a-otherfacsimiletelephonenumber.md)                  | False     | **Unternehmensperson**                                             |
| [**Telefon-Home-Other**](a-otherhomephone.md)                                | False     | **Unternehmensperson**                                             |
| [**Telefon-Home-Primary**](a-homephone.md)                                   | False     | **Unternehmensperson**                                             |
| [**Telefon-Ip-Other**](a-otheripphone.md)                                    | False     | **Unternehmensperson**                                             |
| [**Telefon-Ip-Primary**](a-ipphone.md)                                       | False     | **Unternehmensperson**                                             |
| [**Telefon-ISDN-Primary**](a-primaryinternationalisdnnumber.md)              | False     | **Unternehmensperson**                                             |
| [**Telefon-Mobile-Other**](a-othermobile.md)                                 | False     | **Unternehmensperson**                                             |
| [**Telefon-Mobile-Primary**](a-mobile.md)                                    | False     | **Unternehmensperson**                                             |
| [**Telefon-Office-Other**](a-othertelephone.md)                              | False     | **Unternehmensperson**                                             |
| [**Telefon-Pager-Other**](a-otherpager.md)                                   | False     | **Unternehmensperson**                                             |
| [**Telefon-Pager-Primary**](a-pager.md)                                      | False     | **Unternehmensperson**                                             |
| [**Physical-Delivery-Office-Name**](a-physicaldeliveryofficename.md)       | False     | **Unternehmensperson**                                             |
| [**Bild**](a-thumbnailphoto.md)                                         | False     | **Unternehmensperson**                                             |
| [**Mögliche 100000000000**](a-possibleinferiors.md)                           | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Postal-Address**](a-postaladdress.md)                                   | False     | **Unternehmensperson**                                             |
| [**Postleitzahl**](a-postalcode.md)                                         | False     | **Unternehmensperson**                                             |
| [**Post-Office-Box**](a-postofficebox.md)                                  | False     | **Unternehmensperson**                                             |
| [**Preferred-Delivery-Method**](a-preferreddeliverymethod.md)              | False     | **Unternehmensperson**                                             |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                          | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Proxyadressen**](a-proxyaddresses.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Query-Policy-BL**](a-querypolicybl.md)                                  | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Rdn**](a-name.md)                                                       | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Registrierte Adresse**](a-registeredaddress.md)                           | False     | **Unternehmensperson**                                             |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                   | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                        | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Berichte**](a-directreports.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Reps-From**](a-repsfrom.md)                                             | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Reps-To**](a-repsto.md)                                                 | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Revision**](a-revision.md)                                              | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                          | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Siehe auch**](a-seealso.md)                                               | False     | [**Person**](c-person.md)<br/>                                 |
| [**Seriennummer**](a-serialnumber.md)                                     | False     | [**Person**](c-person.md)<br/>                                 |
| [**Server-Reference-BL**](a-serverreferencebl.md)                          | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)              | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**State-Or-Province-Name**](a-st.md)                                      | False     | **Unternehmensperson**                                             |
| [**Street-Address**](a-street.md)                                          | False     | **Unternehmensperson**                                             |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                  | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Sub-Refs**](a-subrefs.md)                                               | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Nachname**](a-sn.md)                                                     | False     | [**Person**](c-person.md)<br/>                                 |
| [**Systemflags**](a-systemflags.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Telefonnummer**](a-telephonenumber.md)                               | False     | [**Person**](c-person.md)<br/>                                 |
| [**Teletex-Terminal-Identifier**](a-teletexterminalidentifier.md)          | False     | **Unternehmensperson**                                             |
| [**Telex-Number**](a-telexnumber.md)                                       | False     | **Unternehmensperson**                                             |
| [**Telex-Primary**](a-primarytelexnumber.md)                               | False     | **Unternehmensperson**                                             |
| [**Text-Country**](a-co.md)                                                | False     | **Unternehmensperson**                                             |
| [**Titel**](a-title.md)                                                    | False     | **Unternehmensperson**                                             |
| [**Benutzerkommentar**](a-comment.md)                                           | False     | **Unternehmensperson**                                             |
| [**Benutzerkennwort**](a-userpassword.md)                                     | False     | [**Person**](c-person.md)<br/>                                 |
| [**USN-Changed**](a-usnchanged.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**VON USN erstellt**](a-usncreated.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                  | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**USN-Intersite**](a-usnintersite.md)                                     | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**USN-Quelle**](a-usnsource.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Wbem-Path**](a-wbempath.md)                                             | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Bekannte Objekte**](a-wellknownobjects.md)                            | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Wenn geändert**](a-whenchanged.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Wenn erstellt**](a-whencreated.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**WWW-Homepage**](a-wwwhomepage.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**WWW-Page-Other**](a-url.md)                                             | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**X121-Adresse**](a-x121address.md)                                       | False     | **Unternehmensperson**                                             |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2

-   [Attribute](#windows-server-2003-r2-attributes)



| Eingabe | Wert |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | False                                                                                                                     |
| Object-Category             | 0                                                                                                                         |
| Default-Object-Category     | [**Person**](c-person.md)<br/>                                                                                     |
| Governs-Id                  | 2.5.6.7                                                                                                                   |
| Default-Hiding-Value        | 1                                                                                                                         |
| Rdn-Att-Id                  | [**Common-Name**](a-cn.md)<br/>                                                                                    |
| Unterklasse von                 | [**Person**](c-person.md)<br/>                                                                                     |
| Mögliche Vorgesetzte          | [**Organisationseinheit**](c-container.md)[**der**](c-organization.md)[**Containerorganisation**](c-organizationalunit.md) |
| Zusätzlich           | \-                                                                                                                        |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                                              |
| Standardsicherheitsdeskriptor | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;;; AU)                              |
| System-Flags                | 0x00000010                                                                                                                |



## <a name="windows-server-2003-r2-attributes"></a>Windows Server 2003 R2-Attribute

Diese Klasse enthält die folgenden Attribute für Windows Server 2003 R2:



| attribute                                                                   | Obligatorisch. | Abgeleitet von                                                          |
|-----------------------------------------------------------------------------|-----------|-----------------------------------------------------------------------|
| [**Adresse**](a-streetaddress.md)                                          | False     | **Unternehmensperson**                                             |
| [**Address-Home**](a-homepostaladdress.md)                                 | False     | **Unternehmensperson**                                             |
| [**Admin-Description**](a-admindescription.md)                             | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Administratoranzeigename**](a-admindisplayname.md)                            | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Allowed-Attributes**](a-allowedattributes.md)                           | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)        | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                      | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)   | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Assistent**](a-assistant.md)                                            | False     | **Unternehmensperson**                                             |
| [**attributeCertificateAttribute**](a-attributecertificateattribute.md)    | False     | [**Person**](c-person.md)<br/>                                 |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)               | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Kanonischer Name**](a-canonicalname.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Common-Name**](a-cn.md)                                                 | True      | [**Person**](c-person.md)<br/> [**Nach oben**](c-top.md)<br/> |
| [**Unternehmen**](a-company.md)                                                | False     | **Unternehmensperson**                                             |
| [**Ländercode**](a-countrycode.md)                                       | False     | **Unternehmensperson**                                             |
| [**Country-Name**](a-c.md)                                                 | False     | **Unternehmensperson**                                             |
| [**Create-Time-Stamp**](a-createtimestamp.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Department**](a-department.md)                                          | False     | **Unternehmensperson**                                             |
| [**Beschreibung**](a-description.md)                                        | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Destination-Indicator**](a-destinationindicator.md)                     | False     | **Unternehmensperson**                                             |
| [**Anzeigename**](a-displayname.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Display-Name-Printable**](a-displaynameprintable.md)                    | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Division**](a-division.md)                                              | False     | **Unternehmensperson**                                             |
| [**DSA-Signature**](a-dsasignature.md)                                     | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**DS-Core-Propagierungsdaten**](a-dscorepropagationdata.md)                 | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**E-Mail-Adressen**](a-mail.md)                                          | False     | **Unternehmensperson**                                             |
| [**Mitarbeiter-ID**](a-employeeid.md)                                         | False     | **Unternehmensperson**                                             |
| [**Extension-Name**](a-extensionname.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Facsimile-Telephone-Number**](a-facsimiletelephonenumber.md)            | False     | **Unternehmensperson**                                             |
| [**Flaggen**](a-flags.md)                                                    | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**From-Entry**](a-fromentry.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)               | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                   | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                  | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Generation-Qualifier**](a-generationqualifier.md)                       | False     | **Unternehmensperson**                                             |
| [**Given-Name**](a-givenname.md)                                           | False     | **Unternehmensperson**                                             |
| [**houseIdentifier**](a-houseidentifier.md)                                | False     | **Unternehmensperson**                                             |
| [**Initialen**](a-initials.md)                                              | False     | **Unternehmensperson**                                             |
| [**Instanztyp**](a-instancetype.md)                                     | True      | [**Nach oben**](c-top.md)<br/>                                       |
| [**International-ISDN-Number**](a-internationalisdnnumber.md)              | False     | **Unternehmensperson**                                             |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)               | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Is-Deleted**](a-isdeleted.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Is-Member-of-DL**](a-memberof.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                          | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Letztes bekanntes übergeordnetes Element**](a-lastknownparent.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Locality-Name**](a-l.md)                                                | False     | **Unternehmensperson**                                             |
| [**Logo**](a-thumbnaillogo.md)                                             | False     | **Unternehmensperson**                                             |
| [**Verwaltete Objekte**](a-managedobjects.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Manager**](a-manager.md)                                                | False     | **Unternehmensperson**                                             |
| [**Mastered-By**](a-masteredby.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**MHS-OR-Adresse**](a-mhsoraddress.md)                                    | False     | **Unternehmensperson**                                             |
| [**Modify-Time-Stamp**](a-modifytimestamp.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                 | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)         | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)             | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Allowed-to-Delegate-To**](a-msds-allowedtodelegateto.md)          | False     | **Unternehmensperson**                                             |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md) | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)      | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Members-for-Az-Role-BL**](a-msds-membersforazrolebl.md)           | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                       | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)    | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)  | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                         | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)               | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Operations-for-Az-Role-BL**](a-msds-operationsforazrolebl.md)     | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Operations-for-Az-Task-BL**](a-msds-operationsforaztaskbl.md)     | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)      | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)              | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Tasks-for-Az-Role-BL**](a-msds-tasksforazrolebl.md)               | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Tasks-for-Az-Task-BL**](a-msds-tasksforaztaskbl.md)               | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-Exch-House-Identifier**](a-msexchhouseidentifier.md)                 | False     | **Unternehmensperson**                                             |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                  | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                    | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Non-Security-Member-BL**](a-nonsecuritymemberbl.md)                     | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                    | True      | [**Nach oben**](c-top.md)<br/>                                       |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Objektkategorie**](a-objectcategory.md)                                 | True      | [**Nach oben**](c-top.md)<br/>                                       |
| [**Objektklasse**](a-objectclass.md)                                       | True      | [**Nach oben**](c-top.md)<br/>                                       |
| [**Objekt-GUID**](a-objectguid.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Objektversion**](a-objectversion.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Name der Organisationseinheit**](a-ou.md)                                    | False     | **Unternehmensperson**                                             |
| [**Organisationsname**](a-o.md)                                            | False     | **Unternehmensperson**                                             |
| [**Sonstiges Postfach**](a-othermailbox.md)                                     | False     | **Unternehmensperson**                                             |
| [**Anderer Name**](a-middlename.md)                                          | False     | **Unternehmensperson**                                             |
| [**Andere bekannte Objekte**](a-otherwellknownobjects.md)                 | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Teilattributlöschungsliste**](a-partialattributedeletionlist.md)   | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Teilattributsatz**](a-partialattributeset.md)                      | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Personal-Title**](a-personaltitle.md)                                   | False     | **Unternehmensperson**                                             |
| [**Telefon-Fax-Other**](a-otherfacsimiletelephonenumber.md)                  | False     | **Unternehmensperson**                                             |
| [**Telefon-Home-Other**](a-otherhomephone.md)                                | False     | **Unternehmensperson**                                             |
| [**Telefon-Home-Primary**](a-homephone.md)                                   | False     | **Unternehmensperson**                                             |
| [**Telefon-Ip-Other**](a-otheripphone.md)                                    | False     | **Unternehmensperson**                                             |
| [**Telefon-Ip-Primary**](a-ipphone.md)                                       | False     | **Unternehmensperson**                                             |
| [**Telefon-ISDN-Primary**](a-primaryinternationalisdnnumber.md)              | False     | **Unternehmensperson**                                             |
| [**Telefon-Mobile-Other**](a-othermobile.md)                                 | False     | **Unternehmensperson**                                             |
| [**Telefon-Mobile-Primary**](a-mobile.md)                                    | False     | **Unternehmensperson**                                             |
| [**Telefon-Office-Other**](a-othertelephone.md)                              | False     | **Unternehmensperson**                                             |
| [**Telefon-Pager-Other**](a-otherpager.md)                                   | False     | **Unternehmensperson**                                             |
| [**Telefon-Pager-Primary**](a-pager.md)                                      | False     | **Unternehmensperson**                                             |
| [**Physical-Delivery-Office-Name**](a-physicaldeliveryofficename.md)       | False     | **Unternehmensperson**                                             |
| [**Bild**](a-thumbnailphoto.md)                                         | False     | **Unternehmensperson**                                             |
| [**Mögliche Hindernisse**](a-possibleinferiors.md)                           | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Postanschrift**](a-postaladdress.md)                                   | False     | **Unternehmensperson**                                             |
| [**Postleitzahl**](a-postalcode.md)                                         | False     | **Unternehmensperson**                                             |
| [**Post-Office-Box**](a-postofficebox.md)                                  | False     | **Unternehmensperson**                                             |
| [**Preferred-Delivery-Method**](a-preferreddeliverymethod.md)              | False     | **Unternehmensperson**                                             |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                          | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Proxyadressen**](a-proxyaddresses.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Query-Policy-BL**](a-querypolicybl.md)                                  | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Rdn**](a-name.md)                                                       | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Registrierte Adresse**](a-registeredaddress.md)                           | False     | **Unternehmensperson**                                             |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                   | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                        | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Berichte**](a-directreports.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Reps-From**](a-repsfrom.md)                                             | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Reps-To**](a-repsto.md)                                                 | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Revision**](a-revision.md)                                              | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                          | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Siehe auch**](a-seealso.md)                                               | False     | [**Person**](c-person.md)<br/>                                 |
| [**Seriennummer**](a-serialnumber.md)                                     | False     | [**Person**](c-person.md)<br/>                                 |
| [**Server-Reference-BL**](a-serverreferencebl.md)                          | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)              | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**State-Or-Province-Name**](a-st.md)                                      | False     | **Unternehmensperson**                                             |
| [**Street-Address**](a-street.md)                                          | False     | **Unternehmensperson**                                             |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                  | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Sub-Refs**](a-subrefs.md)                                               | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Nachname**](a-sn.md)                                                     | False     | [**Person**](c-person.md)<br/>                                 |
| [**Systemflags**](a-systemflags.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Telefonnummer**](a-telephonenumber.md)                               | False     | [**Person**](c-person.md)<br/>                                 |
| [**Teletex-Terminal-Identifier**](a-teletexterminalidentifier.md)          | False     | **Unternehmensperson**                                             |
| [**Telex-Number**](a-telexnumber.md)                                       | False     | **Unternehmensperson**                                             |
| [**Telex-Primary**](a-primarytelexnumber.md)                               | False     | **Unternehmensperson**                                             |
| [**Text-Country**](a-co.md)                                                | False     | **Unternehmensperson**                                             |
| [**Titel**](a-title.md)                                                    | False     | **Unternehmensperson**                                             |
| [**Benutzerkommentar**](a-comment.md)                                           | False     | **Unternehmensperson**                                             |
| [**Benutzerkennwort**](a-userpassword.md)                                     | False     | [**Person**](c-person.md)<br/>                                 |
| [**USN-Changed**](a-usnchanged.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**VON USN erstellt**](a-usncreated.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                  | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**USN-Intersite**](a-usnintersite.md)                                     | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**USN-Quelle**](a-usnsource.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Wbem-Path**](a-wbempath.md)                                             | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Bekannte Objekte**](a-wellknownobjects.md)                            | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Wenn geändert**](a-whenchanged.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Wenn erstellt**](a-whencreated.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**WWW-Homepage**](a-wwwhomepage.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**WWW-Page-Other**](a-url.md)                                             | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**X121-Adresse**](a-x121address.md)                                       | False     | **Unternehmensperson**                                             |



## <a name="windows-server-2008"></a>Windows Server 2008

-   [Attribute](#windows-server-2008-attributes)



| Eingabe | Wert |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | False                                                                                                                     |
| Object-Category             | 0                                                                                                                         |
| Default-Object-Category     | [**Person**](c-person.md)<br/>                                                                                     |
| Governs-Id                  | 2.5.6.7                                                                                                                   |
| Default-Hiding-Value        | 1                                                                                                                         |
| Rdn-Att-Id                  | [**Common-Name**](a-cn.md)<br/>                                                                                    |
| Unterklasse von                 | [**Person**](c-person.md)<br/>                                                                                     |
| Mögliche Vorgesetzte          | [**Organisationseinheit**](c-container.md)[**der**](c-organization.md)[**Containerorganisation**](c-organizationalunit.md) |
| Zusätzlich           | \-                                                                                                                        |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                                              |
| Standardsicherheitsdeskriptor | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;;; AU)                              |
| System-Flags                | 0x00000010                                                                                                                |



## <a name="windows-server-2008-attributes"></a>Windows Server 2008-Attribute

Diese Klasse enthält die folgenden Attribute für Windows Server 2008:



| attribute                                                                      | Obligatorisch. | Abgeleitet von                                                          |
|--------------------------------------------------------------------------------|-----------|-----------------------------------------------------------------------|
| [**Adresse**](a-streetaddress.md)                                             | False     | **Unternehmensperson**                                             |
| [**Address-Home**](a-homepostaladdress.md)                                    | False     | **Unternehmensperson**                                             |
| [**Admin-Description**](a-admindescription.md)                                | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Administratoranzeigename**](a-admindisplayname.md)                               | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Allowed-Attributes**](a-allowedattributes.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)           | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                         | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)      | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Assistent**](a-assistant.md)                                               | False     | **Unternehmensperson**                                             |
| [**attributeCertificateAttribute**](a-attributecertificateattribute.md)       | False     | [**Person**](c-person.md)<br/>                                 |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                  | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Kanonischer Name**](a-canonicalname.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Common-Name**](a-cn.md)                                                    | True      | [**Person**](c-person.md)<br/> [**Nach oben**](c-top.md)<br/> |
| [**Unternehmen**](a-company.md)                                                   | False     | **Unternehmensperson**                                             |
| [**Ländercode**](a-countrycode.md)                                          | False     | **Unternehmensperson**                                             |
| [**Country-Name**](a-c.md)                                                    | False     | **Unternehmensperson**                                             |
| [**Create-Time-Stamp**](a-createtimestamp.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Department**](a-department.md)                                             | False     | **Unternehmensperson**                                             |
| [**Beschreibung**](a-description.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Destination-Indicator**](a-destinationindicator.md)                        | False     | **Unternehmensperson**                                             |
| [**Anzeigename**](a-displayname.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Display-Name-Printable**](a-displaynameprintable.md)                       | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Division**](a-division.md)                                                 | False     | **Unternehmensperson**                                             |
| [**DSA-Signature**](a-dsasignature.md)                                        | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**DS-Core-Propagierungsdaten**](a-dscorepropagationdata.md)                    | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**E-Mail-Adressen**](a-mail.md)                                             | False     | **Unternehmensperson**                                             |
| [**Mitarbeiter-ID**](a-employeeid.md)                                            | False     | **Unternehmensperson**                                             |
| [**Extension-Name**](a-extensionname.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Facsimile-Telephone-Number**](a-facsimiletelephonenumber.md)               | False     | **Unternehmensperson**                                             |
| [**Flaggen**](a-flags.md)                                                       | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**From-Entry**](a-fromentry.md)                                              | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)                  | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                      | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                     | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Generation-Qualifier**](a-generationqualifier.md)                          | False     | **Unternehmensperson**                                             |
| [**Given-Name**](a-givenname.md)                                              | False     | **Unternehmensperson**                                             |
| [**houseIdentifier**](a-houseidentifier.md)                                   | False     | **Unternehmensperson**                                             |
| [**Initialen**](a-initials.md)                                                 | False     | **Unternehmensperson**                                             |
| [**Instanztyp**](a-instancetype.md)                                        | True      | [**Nach oben**](c-top.md)<br/>                                       |
| [**International-ISDN-Number**](a-internationalisdnnumber.md)                 | False     | **Unternehmensperson**                                             |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                  | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Is-Deleted**](a-isdeleted.md)                                              | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Is-Member-of-DL**](a-memberof.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                             | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Letztes bekanntes übergeordnetes Element**](a-lastknownparent.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Locality-Name**](a-l.md)                                                   | False     | **Unternehmensperson**                                             |
| [**Logo**](a-thumbnaillogo.md)                                                | False     | **Unternehmensperson**                                             |
| [**Verwaltete Objekte**](a-managedobjects.md)                                    | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Manager**](a-manager.md)                                                   | False     | **Unternehmensperson**                                             |
| [**Mastered-By**](a-masteredby.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**MHS-OR-Adresse**](a-mhsoraddress.md)                                       | False     | **Unternehmensperson**                                             |
| [**Modify-Time-Stamp**](a-modifytimestamp.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                    | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                    | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)            | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Allowed-to-Delegate-To**](a-msds-allowedtodelegateto.md)             | False     | **Unternehmensperson**                                             |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md)    | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md) | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)         | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                      | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-IGE-Seniority-Index**](a-msds-habseniorityindex.md)                  | False     | **Unternehmensperson**                                             |
| [**ms-DS-Is-Domain-For**](a-msds-isdomainfor.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-is-full-replica-for**](a-msds-isfullreplicafor.md)                   | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-is-partial-replica-for**](a-msds-ispartialreplicafor.md)             | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                            | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Members-for-Az-Role-BL**](a-msds-membersforazrolebl.md)              | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                          | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)       | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)     | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)  | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-NC-Type**](a-msds-nctype.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                            | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                  | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Operations-for-Az-Role-BL**](a-msds-operationsforazrolebl.md)        | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Operations-for-Az-Task-BL**](a-msds-operationsforaztaskbl.md)        | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Phonetic-Company-Name**](a-msds-phoneticcompanyname.md)              | False     | **Unternehmensperson**                                             |
| [**ms-DS-Phonetic-Department**](a-msds-phoneticdepartment.md)                 | False     | **Unternehmensperson**                                             |
| [**ms-DS-Phonetic-Display-Name**](a-msds-phoneticdisplayname.md)              | False     | **Unternehmensperson**                                             |
| [**ms-DS-Phonetic-First-Name**](a-msds-phoneticfirstname.md)                  | False     | **Unternehmensperson**                                             |
| [**ms-DS-Phonetic-Last-Name**](a-msds-phoneticlastname.md)                    | False     | **Unternehmensperson**                                             |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                           | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-PSO-Applied**](a-msds-psoapplied.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)         | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                 | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Revealed-DSAs**](a-msds-revealeddsas.md)                             | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Revealed-List-BL**](a-msds-revealedlistbl.md)                        | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)                  | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)                  | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-Exch-House-Identifier**](a-msexchhouseidentifier.md)                    | False     | **Unternehmensperson**                                             |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                     | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Non-Security-Member-BL**](a-nonsecuritymemberbl.md)                        | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                       | True      | [**Nach oben**](c-top.md)<br/>                                       |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Objektkategorie**](a-objectcategory.md)                                    | True      | [**Nach oben**](c-top.md)<br/>                                       |
| [**Object-Class**](a-objectclass.md)                                          | True      | [**Nach oben**](c-top.md)<br/>                                       |
| [**Objekt-GUID**](a-objectguid.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Object-Version**](a-objectversion.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Organisationseinheitsname**](a-ou.md)                                       | False     | **Unternehmensperson**                                             |
| [**Organisationsname**](a-o.md)                                               | False     | **Unternehmensperson**                                             |
| [**Sonstiges Postfach**](a-othermailbox.md)                                        | False     | **Unternehmensperson**                                             |
| [**Other-Name**](a-middlename.md)                                             | False     | **Unternehmensperson**                                             |
| [**Andere bekannte Objekte**](a-otherwellknownobjects.md)                    | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)      | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                         | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Personal-Title**](a-personaltitle.md)                                      | False     | **Unternehmensperson**                                             |
| [**Telefon-Fax-Other**](a-otherfacsimiletelephonenumber.md)                     | False     | **Unternehmensperson**                                             |
| [**Telefon-Home-Other**](a-otherhomephone.md)                                   | False     | **Unternehmensperson**                                             |
| [**Telefon-Home-Primary**](a-homephone.md)                                      | False     | **Unternehmensperson**                                             |
| [**Telefon-Ip-Other**](a-otheripphone.md)                                       | False     | **Unternehmensperson**                                             |
| [**Telefon-Ip-Primary**](a-ipphone.md)                                          | False     | **Unternehmensperson**                                             |
| [**Telefon-ISDN-Primary**](a-primaryinternationalisdnnumber.md)                 | False     | **Unternehmensperson**                                             |
| [**Telefon-Mobile-Other**](a-othermobile.md)                                    | False     | **Unternehmensperson**                                             |
| [**Telefon-Mobile-Primary**](a-mobile.md)                                       | False     | **Unternehmensperson**                                             |
| [**Telefon-Office-Other**](a-othertelephone.md)                                 | False     | **Unternehmensperson**                                             |
| [**Telefon-Pager-Other**](a-otherpager.md)                                      | False     | **Unternehmensperson**                                             |
| [**Telefon-Pager-Primary**](a-pager.md)                                         | False     | **Unternehmensperson**                                             |
| [**Physical-Delivery-Office-Name**](a-physicaldeliveryofficename.md)          | False     | **Unternehmensperson**                                             |
| [**Bild**](a-thumbnailphoto.md)                                            | False     | **Unternehmensperson**                                             |
| [**Mögliche Hindernisse**](a-possibleinferiors.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Postanschrift**](a-postaladdress.md)                                      | False     | **Unternehmensperson**                                             |
| [**Postleitzahl**](a-postalcode.md)                                            | False     | **Unternehmensperson**                                             |
| [**Post-Office-Box**](a-postofficebox.md)                                     | False     | **Unternehmensperson**                                             |
| [**Preferred-Delivery-Method**](a-preferreddeliverymethod.md)                 | False     | **Unternehmensperson**                                             |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                             | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Proxyadressen**](a-proxyaddresses.md)                                    | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Query-Policy-BL**](a-querypolicybl.md)                                     | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Rdn**](a-name.md)                                                          | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Registrierte Adresse**](a-registeredaddress.md)                              | False     | **Unternehmensperson**                                             |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                      | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                           | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Berichte**](a-directreports.md)                                             | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Reps-From**](a-repsfrom.md)                                                | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Reps-To**](a-repsto.md)                                                    | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Revision**](a-revision.md)                                                 | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                             | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Siehe auch**](a-seealso.md)                                                  | False     | [**Person**](c-person.md)<br/>                                 |
| [**Seriennummer**](a-serialnumber.md)                                        | False     | [**Person**](c-person.md)<br/>                                 |
| [**Server-Reference-BL**](a-serverreferencebl.md)                             | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Nur in erweiterter Ansicht anzeigen**](a-showinadvancedviewonly.md)                 | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Site-Object-BL**](a-siteobjectbl.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**State-or-Province-Name**](a-st.md)                                         | False     | **Unternehmensperson**                                             |
| [**Adresse der Straße**](a-street.md)                                             | False     | **Unternehmensperson**                                             |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                     | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Sub-Refs**](a-subrefs.md)                                                  | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                               | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Nachname**](a-sn.md)                                                        | False     | [**Person**](c-person.md)<br/>                                 |
| [**Systemflags**](a-systemflags.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Telefonnummer**](a-telephonenumber.md)                                  | False     | [**Person**](c-person.md)<br/>                                 |
| [**Teletex-Terminal-Identifier**](a-teletexterminalidentifier.md)             | False     | **Unternehmensperson**                                             |
| [**Telex-Number**](a-telexnumber.md)                                          | False     | **Unternehmensperson**                                             |
| [**Telex-Primary**](a-primarytelexnumber.md)                                  | False     | **Unternehmensperson**                                             |
| [**Text-Country**](a-co.md)                                                   | False     | **Unternehmensperson**                                             |
| [**Titel**](a-title.md)                                                       | False     | **Unternehmensperson**                                             |
| [**Benutzerkommentar**](a-comment.md)                                              | False     | **Unternehmensperson**                                             |
| [**Benutzerkennwort**](a-userpassword.md)                                        | False     | [**Person**](c-person.md)<br/>                                 |
| [**USN geändert**](a-usnchanged.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**USN-erstellt**](a-usncreated.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**USN-DSA-last-obj-removed**](a-usndsalastobjremoved.md)                     | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**USN-Intersite**](a-usnintersite.md)                                        | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                    | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**USN-Quelle**](a-usnsource.md)                                              | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Wbem-Pfad**](a-wbempath.md)                                                | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Bekannte Objekte**](a-wellknownobjects.md)                               | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Bei Änderung**](a-whenchanged.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Bei der Erstellung**](a-whencreated.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**WWW-Startseite**](a-wwwhomepage.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**WWW-Page-Other**](a-url.md)                                                | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**X121-Address**](a-x121address.md)                                          | False     | **Unternehmensperson**                                             |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2

-   [Attribute](#windows-server-2008-r2-attributes)



| Eingabe | Wert |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | False                                                                                                                     |
| Object-Category             | 0                                                                                                                         |
| Default-Object-Category     | [**Person**](c-person.md)<br/>                                                                                     |
| Governs-Id                  | 2.5.6.7                                                                                                                   |
| Default-Hiding-Value        | 1                                                                                                                         |
| Rdn-Att-Id                  | [**Allgemeiner Name**](a-cn.md)<br/>                                                                                    |
| Unterklasse von                 | [**Person**](c-person.md)<br/>                                                                                     |
| Mögliche Übergeordnete          | [**Organisationseinheit**](c-organizationalunit.md) der [**Containerorganisation**](c-container.md)[](c-organization.md) |
| Zusätzlich           | \-                                                                                                                        |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                                              |
| Standardsicherheitsdeskriptor | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;;; AU)                              |
| System-Flags                | 0x00000010                                                                                                                |



## <a name="windows-server-2008-r2-attributes"></a>Windows Server 2008 R2-Attribute

Diese Klasse enthält die folgenden Attribute für Windows Server 2008 R2:



| attribute                                                                        | Obligatorisch. | Abgeleitet von                                                          |
|----------------------------------------------------------------------------------|-----------|-----------------------------------------------------------------------|
| [**Adresse**](a-streetaddress.md)                                               | False     | **Unternehmensperson**                                             |
| [**Address-Home**](a-homepostaladdress.md)                                      | False     | **Unternehmensperson**                                             |
| [**Administratorbeschreibung**](a-admindescription.md)                                  | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Admin-Display-Name**](a-admindisplayname.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Allowed-Attributes**](a-allowedattributes.md)                                | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)             | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                           | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)        | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Assistent**](a-assistant.md)                                                 | False     | **Unternehmensperson**                                             |
| [**attributeCertificateAttribute**](a-attributecertificateattribute.md)         | False     | [**Person**](c-person.md)<br/>                                 |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                    | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Kanonischer Name**](a-canonicalname.md)                                        | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Allgemeiner Name**](a-cn.md)                                                      | True      | [**Person**](c-person.md)<br/> [**Nach oben**](c-top.md)<br/> |
| [**Unternehmen**](a-company.md)                                                     | False     | **Unternehmensperson**                                             |
| [**Ländercode**](a-countrycode.md)                                            | False     | **Unternehmensperson**                                             |
| [**Country-Name**](a-c.md)                                                      | False     | **Unternehmensperson**                                             |
| [**Erstellen eines Zeitstempels**](a-createtimestamp.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Department**](a-department.md)                                               | False     | **Unternehmensperson**                                             |
| [**Beschreibung**](a-description.md)                                             | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Zielindikator**](a-destinationindicator.md)                          | False     | **Unternehmensperson**                                             |
| [**Anzeigename**](a-displayname.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Anzeigename– druckbar**](a-displaynameprintable.md)                         | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Division**](a-division.md)                                                   | False     | **Unternehmensperson**                                             |
| [**DSA-Signature**](a-dsasignature.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**DS-Core-Propagierungsdaten**](a-dscorepropagationdata.md)                      | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**E-Mail-Adressen**](a-mail.md)                                               | False     | **Unternehmensperson**                                             |
| [**Mitarbeiter-ID**](a-employeeid.md)                                              | False     | **Unternehmensperson**                                             |
| [**Erweiterungsname**](a-extensionname.md)                                        | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Facsimile-Telephone-Number**](a-facsimiletelephonenumber.md)                 | False     | **Unternehmensperson**                                             |
| [**Flaggen**](a-flags.md)                                                         | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**From-Entry**](a-fromentry.md)                                                | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)                    | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                        | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Generation-Qualifier**](a-generationqualifier.md)                            | False     | **Unternehmensperson**                                             |
| [**Vorname**](a-givenname.md)                                                | False     | **Unternehmensperson**                                             |
| [**houseIdentifier**](a-houseidentifier.md)                                     | False     | **Unternehmensperson**                                             |
| [**Initialen**](a-initials.md)                                                   | False     | **Unternehmensperson**                                             |
| [**Instanztyp**](a-instancetype.md)                                          | True      | [**Nach oben**](c-top.md)<br/>                                       |
| [**International-ISDN-Number**](a-internationalisdnnumber.md)                   | False     | **Unternehmensperson**                                             |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                    | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Is-Deleted**](a-isdeleted.md)                                                | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Is-Member-of-DL**](a-memberof.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                               | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Wird wiederverwendet**](a-isrecycled.md)                                              | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Last-Known-Parent**](a-lastknownparent.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Locality-Name**](a-l.md)                                                     | False     | **Unternehmensperson**                                             |
| [**Logo**](a-thumbnaillogo.md)                                                  | False     | **Unternehmensperson**                                             |
| [**Verwaltete Objekte**](a-managedobjects.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Manager**](a-manager.md)                                                     | False     | **Unternehmensperson**                                             |
| [**Mastered-By**](a-masteredby.md)                                              | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**MHS-OR-Adresse**](a-mhsoraddress.md)                                         | False     | **Unternehmensperson**                                             |
| [**Modify-Time-Stamp**](a-modifytimestamp.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                      | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)              | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                  | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Allowed-to-Delegate-To**](a-msds-allowedtodelegateto.md)               | False     | **Unternehmensperson**                                             |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md)      | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md)   | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)           | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                        | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Enabled-Feature-BL**](a-msds-enabledfeaturebl.md)                      | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-IGE-Seniority-Index**](a-msds-habseniorityindex.md)                    | False     | **Unternehmensperson**                                             |
| [**ms-DS-Host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)             | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Is-Domain-For**](a-msds-isdomainfor.md)                                | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-is-full-replica-for**](a-msds-isfullreplicafor.md)                     | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-is-partial-replica-for**](a-msds-ispartialreplicafor.md)               | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-local-Effective-Deletion-Time**](a-msds-localeffectivedeletiontime.md) | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-local-Effective-Recycle-Time**](a-msds-localeffectiverecycletime.md)   | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Members-for-Az-Role-BL**](a-msds-membersforazrolebl.md)                | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                            | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)         | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)       | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)    | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-NC-Type**](a-msds-nctype.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                    | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-OIDToGroup-Link-BL**](a-msds-oidtogrouplinkbl.md)                      | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Operations-for-Az-Role-BL**](a-msds-operationsforazrolebl.md)          | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Operations-for-Az-Task-BL**](a-msds-operationsforaztaskbl.md)          | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Phonetic-Company-Name**](a-msds-phoneticcompanyname.md)                | False     | **Unternehmensperson**                                             |
| [**ms-DS-Phonetic-Department**](a-msds-phoneticdepartment.md)                   | False     | **Unternehmensperson**                                             |
| [**ms-DS-Phonetic-Display-Name**](a-msds-phoneticdisplayname.md)                | False     | **Unternehmensperson**                                             |
| [**ms-DS-Phonetic-First-Name**](a-msds-phoneticfirstname.md)                    | False     | **Unternehmensperson**                                             |
| [**ms-DS-Phonetic-Last-Name**](a-msds-phoneticlastname.md)                      | False     | **Unternehmensperson**                                             |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                             | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-PSO-Applied**](a-msds-psoapplied.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)           | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                   | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Revealed-DSAs**](a-msds-revealeddsas.md)                               | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Revealed-List-BL**](a-msds-revealedlistbl.md)                          | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Tasks-for-Az-Role-BL**](a-msds-tasksforazrolebl.md)                    | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)                    | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-Exch-House-Identifier**](a-msexchhouseidentifier.md)                      | False     | **Unternehmensperson**                                             |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                       | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Non-Security-Member-BL**](a-nonsecuritymemberbl.md)                          | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                         | True      | [**Nach oben**](c-top.md)<br/>                                       |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                     | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Objektkategorie**](a-objectcategory.md)                                      | True      | [**Nach oben**](c-top.md)<br/>                                       |
| [**Object-Class**](a-objectclass.md)                                            | True      | [**Nach oben**](c-top.md)<br/>                                       |
| [**Objekt-GUID**](a-objectguid.md)                                              | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Object-Version**](a-objectversion.md)                                        | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Organisationseinheitsname**](a-ou.md)                                         | False     | **Unternehmensperson**                                             |
| [**Organisationsname**](a-o.md)                                                 | False     | **Unternehmensperson**                                             |
| [**Sonstiges Postfach**](a-othermailbox.md)                                          | False     | **Unternehmensperson**                                             |
| [**Other-Name**](a-middlename.md)                                               | False     | **Unternehmensperson**                                             |
| [**Andere bekannte Objekte**](a-otherwellknownobjects.md)                      | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)        | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                           | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Personal-Title**](a-personaltitle.md)                                        | False     | **Unternehmensperson**                                             |
| [**Telefon-Fax-Other**](a-otherfacsimiletelephonenumber.md)                       | False     | **Unternehmensperson**                                             |
| [**Telefon-Home-Other**](a-otherhomephone.md)                                     | False     | **Unternehmensperson**                                             |
| [**Telefon-Home-Primary**](a-homephone.md)                                        | False     | **Unternehmensperson**                                             |
| [**Telefon-Ip-Other**](a-otheripphone.md)                                         | False     | **Unternehmensperson**                                             |
| [**Telefon-Ip-Primary**](a-ipphone.md)                                            | False     | **Unternehmensperson**                                             |
| [**Telefon-ISDN-Primary**](a-primaryinternationalisdnnumber.md)                   | False     | **Unternehmensperson**                                             |
| [**Telefon-Mobile-Other**](a-othermobile.md)                                      | False     | **Unternehmensperson**                                             |
| [**Telefon-Mobile-Primary**](a-mobile.md)                                         | False     | **Unternehmensperson**                                             |
| [**Telefon-Office-Other**](a-othertelephone.md)                                   | False     | **Unternehmensperson**                                             |
| [**Telefon-Pager-Other**](a-otherpager.md)                                        | False     | **Unternehmensperson**                                             |
| [**Telefon-Pager-Primary**](a-pager.md)                                           | False     | **Unternehmensperson**                                             |
| [**Physical-Delivery-Office-Name**](a-physicaldeliveryofficename.md)            | False     | **Unternehmensperson**                                             |
| [**Bild**](a-thumbnailphoto.md)                                              | False     | **Unternehmensperson**                                             |
| [**Mögliche Hindernisse**](a-possibleinferiors.md)                                | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Postanschrift**](a-postaladdress.md)                                        | False     | **Unternehmensperson**                                             |
| [**Postleitzahl**](a-postalcode.md)                                              | False     | **Unternehmensperson**                                             |
| [**Post-Office-Box**](a-postofficebox.md)                                       | False     | **Unternehmensperson**                                             |
| [**Preferred-Delivery-Method**](a-preferreddeliverymethod.md)                   | False     | **Unternehmensperson**                                             |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                               | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Proxyadressen**](a-proxyaddresses.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Query-Policy-BL**](a-querypolicybl.md)                                       | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Rdn**](a-name.md)                                                            | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Registrierte Adresse**](a-registeredaddress.md)                                | False     | **Unternehmensperson**                                             |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                        | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                             | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Berichte**](a-directreports.md)                                               | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Reps-From**](a-repsfrom.md)                                                  | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Reps-To**](a-repsto.md)                                                      | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Revision**](a-revision.md)                                                   | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                               | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Siehe auch**](a-seealso.md)                                                    | False     | [**Person**](c-person.md)<br/>                                 |
| [**Seriennummer**](a-serialnumber.md)                                          | False     | [**Person**](c-person.md)<br/>                                 |
| [**Server-Reference-BL**](a-serverreferencebl.md)                               | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Nur in erweiterter Ansicht anzeigen**](a-showinadvancedviewonly.md)                   | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Site-Object-BL**](a-siteobjectbl.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**State-or-Province-Name**](a-st.md)                                           | False     | **Unternehmensperson**                                             |
| [**Adresse der Straße**](a-street.md)                                               | False     | **Unternehmensperson**                                             |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                       | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Sub-Refs**](a-subrefs.md)                                                    | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Nachname**](a-sn.md)                                                          | False     | [**Person**](c-person.md)<br/>                                 |
| [**Systemflags**](a-systemflags.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Telefonnummer**](a-telephonenumber.md)                                    | False     | [**Person**](c-person.md)<br/>                                 |
| [**Teletex-Terminal-Identifier**](a-teletexterminalidentifier.md)               | False     | **Unternehmensperson**                                             |
| [**Telex-Number**](a-telexnumber.md)                                            | False     | **Unternehmensperson**                                             |
| [**Telex-Primary**](a-primarytelexnumber.md)                                    | False     | **Unternehmensperson**                                             |
| [**Text-Country**](a-co.md)                                                     | False     | **Unternehmensperson**                                             |
| [**Titel**](a-title.md)                                                         | False     | **Unternehmensperson**                                             |
| [**Benutzerkommentar**](a-comment.md)                                                | False     | **Unternehmensperson**                                             |
| [**Benutzerkennwort**](a-userpassword.md)                                          | False     | [**Person**](c-person.md)<br/>                                 |
| [**USN geändert**](a-usnchanged.md)                                              | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**USN-erstellt**](a-usncreated.md)                                              | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**USN-DSA-last-obj-removed**](a-usndsalastobjremoved.md)                       | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**USN-Intersite**](a-usnintersite.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**USN-Quelle**](a-usnsource.md)                                                | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Wbem-Pfad**](a-wbempath.md)                                                  | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Bekannte Objekte**](a-wellknownobjects.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Bei Änderung**](a-whenchanged.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Bei der Erstellung**](a-whencreated.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**WWW-Startseite**](a-wwwhomepage.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**WWW-Page-Other**](a-url.md)                                                  | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**X121-Address**](a-x121address.md)                                            | False     | **Unternehmensperson**                                             |



## <a name="windows-server-2012"></a>Windows Server 2012

-   [Attribute](#windows-server-2012-attributes)



| Eingabe | Wert |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | False                                                                                                                     |
| Object-Category             | 0                                                                                                                         |
| Default-Object-Category     | [**Person**](c-person.md)<br/>                                                                                     |
| Governs-Id                  | 2.5.6.7                                                                                                                   |
| Default-Hiding-Value        | 1                                                                                                                         |
| Rdn-Att-Id                  | [**Allgemeiner Name**](a-cn.md)<br/>                                                                                    |
| Unterklasse von                 | [**Person**](c-person.md)<br/>                                                                                     |
| Mögliche Übergeordnete          | [**Organisationseinheit**](c-organizationalunit.md) der [**Containerorganisation**](c-container.md)[](c-organization.md) |
| Zusätzlich           | \-                                                                                                                        |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                                              |
| Standardsicherheitsdeskriptor | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;;; AU)                              |
| System-Flags                | 0x00000010                                                                                                                |



## <a name="windows-server-2012-attributes"></a>Windows Server 2012 Attribute

Diese Klasse enthält die folgenden Attribute für Windows Server 2012:



| attribute                                                                                              | Obligatorisch. | Abgeleitet von                                                          |
|--------------------------------------------------------------------------------------------------------|-----------|-----------------------------------------------------------------------|
| [**Adresse**](a-streetaddress.md)                                                                     | False     | **Unternehmensperson**                                             |
| [**Address-Home**](a-homepostaladdress.md)                                                            | False     | **Unternehmensperson**                                             |
| [**Administratorbeschreibung**](a-admindescription.md)                                                        | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Admin-Display-Name**](a-admindisplayname.md)                                                       | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Allowed-Attributes**](a-allowedattributes.md)                                                      | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                                                 | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Assistent**](a-assistant.md)                                                                       | False     | **Unternehmensperson**                                             |
| [**attributeCertificateAttribute**](a-attributecertificateattribute.md)                               | False     | [**Person**](c-person.md)<br/>                                 |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Kanonischer Name**](a-canonicalname.md)                                                              | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Allgemeiner Name**](a-cn.md)                                                                            | True      | [**Person**](c-person.md)<br/> [**Nach oben**](c-top.md)<br/> |
| [**Unternehmen**](a-company.md)                                                                           | False     | **Unternehmensperson**                                             |
| [**Ländercode**](a-countrycode.md)                                                                  | False     | **Unternehmensperson**                                             |
| [**Country-Name**](a-c.md)                                                                            | False     | **Unternehmensperson**                                             |
| [**Erstellen eines Zeitstempels**](a-createtimestamp.md)                                                         | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Department**](a-department.md)                                                                     | False     | **Unternehmensperson**                                             |
| [**Beschreibung**](a-description.md)                                                                   | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Zielindikator**](a-destinationindicator.md)                                                | False     | **Unternehmensperson**                                             |
| [**Anzeigename**](a-displayname.md)                                                                  | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Anzeigename– druckbar**](a-displaynameprintable.md)                                               | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Division**](a-division.md)                                                                         | False     | **Unternehmensperson**                                             |
| [**DSA-Signature**](a-dsasignature.md)                                                                | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**DS-Core-Propagierungsdaten**](a-dscorepropagationdata.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**E-Mail-Adressen**](a-mail.md)                                                                     | False     | **Unternehmensperson**                                             |
| [**Mitarbeiter-ID**](a-employeeid.md)                                                                    | False     | **Unternehmensperson**                                             |
| [**Erweiterungsname**](a-extensionname.md)                                                              | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Facsimile-Telephone-Number**](a-facsimiletelephonenumber.md)                                       | False     | **Unternehmensperson**                                             |
| [**Flaggen**](a-flags.md)                                                                               | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**From-Entry**](a-fromentry.md)                                                                      | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                                              | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                                             | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Generation-Qualifier**](a-generationqualifier.md)                                                  | False     | **Unternehmensperson**                                             |
| [**Vorname**](a-givenname.md)                                                                      | False     | **Unternehmensperson**                                             |
| [**houseIdentifier**](a-houseidentifier.md)                                                           | False     | **Unternehmensperson**                                             |
| [**Initialen**](a-initials.md)                                                                         | False     | **Unternehmensperson**                                             |
| [**Instanztyp**](a-instancetype.md)                                                                | True      | [**Nach oben**](c-top.md)<br/>                                       |
| [**International-ISDN-Number**](a-internationalisdnnumber.md)                                         | False     | **Unternehmensperson**                                             |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Is-Deleted**](a-isdeleted.md)                                                                      | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Is-Member-of-DL**](a-memberof.md)                                                                  | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                                                     | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Wird wiederverwendet**](a-isrecycled.md)                                                                    | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Last-Known-Parent**](a-lastknownparent.md)                                                         | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Locality-Name**](a-l.md)                                                                           | False     | **Unternehmensperson**                                             |
| [**Logo**](a-thumbnaillogo.md)                                                                        | False     | **Unternehmensperson**                                             |
| [**Verwaltete Objekte**](a-managedobjects.md)                                                            | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Manager**](a-manager.md)                                                                           | False     | **Unternehmensperson**                                             |
| [**Mastered-By**](a-masteredby.md)                                                                    | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**MHS-OR-Adresse**](a-mhsoraddress.md)                                                               | False     | **Unternehmensperson**                                             |
| [**Modify-Time-Stamp**](a-modifytimestamp.md)                                                         | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                                            | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)                                    | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                                        | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Allowed-to-Act-On-Behalf-of-Other-Identity**](a-msds-allowedtoactonbehalfofotheridentity.md) | False     | **Unternehmensperson**                                             |
| [**ms-DS-Allowed-to-Delegate-To**](a-msds-allowedtodelegateto.md)                                     | False     | **Unternehmensperson**                                             |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md)                            | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md)                         | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Claim-Shares-Possible-Values-with-BL**](a-msds-claimsharespossiblevalueswithbl.md)           | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                                              | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Enabled-Feature-BL**](a-msds-enabledfeaturebl.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-IGE-Seniority-Index**](a-msds-habseniorityindex.md)                                          | False     | **Unternehmensperson**                                             |
| [**ms-DS-Host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Is-Domain-For**](a-msds-isdomainfor.md)                                                      | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-is-full-replica-for**](a-msds-isfullreplicafor.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-is-partial-replica-for**](a-msds-ispartialreplicafor.md)                                     | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Is-Primary-Computer-For**](a-msds-isprimarycomputerfor.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                                                    | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                                                    | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-local-Effective-Deletion-Time**](a-msds-localeffectivedeletiontime.md)                       | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-local-Effective-Recycle-Time**](a-msds-localeffectiverecycletime.md)                         | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                                                         | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Members-for-Az-Role-BL**](a-msds-membersforazrolebl.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Members-of-Resource-Property-List-BL**](a-msds-membersofresourcepropertylistbl.md)           | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                                                  | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)                               | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)                             | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)                          | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-NC-Type**](a-msds-nctype.md)                                                                 | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                                                    | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-OIDToGroup-Link-BL**](a-msds-oidtogrouplinkbl.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Operations-for-Az-Role-BL**](a-msds-operationsforazrolebl.md)                                | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Operations-for-Az-Task-BL**](a-msds-operationsforaztaskbl.md)                                | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Phonetic-Company-Name**](a-msds-phoneticcompanyname.md)                                      | False     | **Unternehmensperson**                                             |
| [**ms-DS-Phonetic-Department**](a-msds-phoneticdepartment.md)                                         | False     | **Unternehmensperson**                                             |
| [**ms-DS-Phonetic-Display-Name**](a-msds-phoneticdisplayname.md)                                      | False     | **Unternehmensperson**                                             |
| [**ms-DS-Phonetic-First-Name**](a-msds-phoneticfirstname.md)                                          | False     | **Unternehmensperson**                                             |
| [**ms-DS-Phonetic-Last-Name**](a-msds-phoneticlastname.md)                                            | False     | **Unternehmensperson**                                             |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                                                   | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-PSO-Applied**](a-msds-psoapplied.md)                                                         | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Revealed-DSAs**](a-msds-revealeddsas.md)                                                     | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Revealed-List-BL**](a-msds-revealedlistbl.md)                                                | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Tasks-for-Az-Role-BL**](a-msds-tasksforazrolebl.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Tasks-for-Az-Task-BL**](a-msds-tasksforaztaskbl.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-TDO-Egress-BL**](a-msds-tdoegressbl.md)                                                      | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-TDO-Ingress-BL**](a-msds-tdoingressbl.md)                                                    | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-DS-Value-Type-Reference-BL**](a-msds-valuetypereferencebl.md)                                   | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**ms-Exch-House-Identifier**](a-msexchhouseidentifier.md)                                            | False     | **Unternehmensperson**                                             |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                                                  | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                                             | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                                               | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Non-Security-Member-BL**](a-nonsecuritymemberbl.md)                                                | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                                               | True      | [**Nach oben**](c-top.md)<br/>                                       |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                                           | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Objektkategorie**](a-objectcategory.md)                                                            | True      | [**Nach oben**](c-top.md)<br/>                                       |
| [**Object-Class**](a-objectclass.md)                                                                  | True      | [**Nach oben**](c-top.md)<br/>                                       |
| [**Objekt-GUID**](a-objectguid.md)                                                                    | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Object-Version**](a-objectversion.md)                                                              | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Organisationseinheitsname**](a-ou.md)                                                               | False     | **Unternehmensperson**                                             |
| [**Organisationsname**](a-o.md)                                                                       | False     | **Unternehmensperson**                                             |
| [**Sonstiges Postfach**](a-othermailbox.md)                                                                | False     | **Unternehmensperson**                                             |
| [**Other-Name**](a-middlename.md)                                                                     | False     | **Unternehmensperson**                                             |
| [**Andere bekannte Objekte**](a-otherwellknownobjects.md)                                            | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)                              | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                                                 | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Personal-Title**](a-personaltitle.md)                                                              | False     | **Unternehmensperson**                                             |
| [**Telefon-Fax-Other**](a-otherfacsimiletelephonenumber.md)                                             | False     | **Unternehmensperson**                                             |
| [**Telefon-Home-Other**](a-otherhomephone.md)                                                           | False     | **Unternehmensperson**                                             |
| [**Telefon-Home-Primary**](a-homephone.md)                                                              | False     | **Unternehmensperson**                                             |
| [**Telefon-Ip-Other**](a-otheripphone.md)                                                               | False     | **Unternehmensperson**                                             |
| [**Telefon-Ip-Primary**](a-ipphone.md)                                                                  | False     | **Unternehmensperson**                                             |
| [**Telefon-ISDN-Primary**](a-primaryinternationalisdnnumber.md)                                         | False     | **Unternehmensperson**                                             |
| [**Telefon-Mobile-Other**](a-othermobile.md)                                                            | False     | **Unternehmensperson**                                             |
| [**Telefon-Mobile-Primary**](a-mobile.md)                                                               | False     | **Unternehmensperson**                                             |
| [**Telefon-Office-Other**](a-othertelephone.md)                                                         | False     | **Unternehmensperson**                                             |
| [**Telefon-Pager-Other**](a-otherpager.md)                                                              | False     | **Unternehmensperson**                                             |
| [**Telefon-Pager-Primary**](a-pager.md)                                                                 | False     | **Unternehmensperson**                                             |
| [**Physical-Delivery-Office-Name**](a-physicaldeliveryofficename.md)                                  | False     | **Unternehmensperson**                                             |
| [**Bild**](a-thumbnailphoto.md)                                                                    | False     | **Unternehmensperson**                                             |
| [**Mögliche 100000000000**](a-possibleinferiors.md)                                                      | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Postal-Address**](a-postaladdress.md)                                                              | False     | **Unternehmensperson**                                             |
| [**Postleitzahl**](a-postalcode.md)                                                                    | False     | **Unternehmensperson**                                             |
| [**Post-Office-Box**](a-postofficebox.md)                                                             | False     | **Unternehmensperson**                                             |
| [**Preferred-Delivery-Method**](a-preferreddeliverymethod.md)                                         | False     | **Unternehmensperson**                                             |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                                                     | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Proxyadressen**](a-proxyaddresses.md)                                                            | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Query-Policy-BL**](a-querypolicybl.md)                                                             | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Rdn**](a-name.md)                                                                                  | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Registrierte Adresse**](a-registeredaddress.md)                                                      | False     | **Unternehmensperson**                                             |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                                              | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                                                   | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Berichte**](a-directreports.md)                                                                     | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Reps-From**](a-repsfrom.md)                                                                        | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Reps-To**](a-repsto.md)                                                                            | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Revision**](a-revision.md)                                                                         | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                                                     | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Siehe auch**](a-seealso.md)                                                                          | False     | [**Person**](c-person.md)<br/>                                 |
| [**Seriennummer**](a-serialnumber.md)                                                                | False     | [**Person**](c-person.md)<br/>                                 |
| [**Server-Reference-BL**](a-serverreferencebl.md)                                                     | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Nur in erweiterter Ansicht anzeigen**](a-showinadvancedviewonly.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Site-Object-BL**](a-siteobjectbl.md)                                                               | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**State-or-Province-Name**](a-st.md)                                                                 | False     | **Unternehmensperson**                                             |
| [**Adresse der Straße**](a-street.md)                                                                     | False     | **Unternehmensperson**                                             |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                                             | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Sub-Refs**](a-subrefs.md)                                                                          | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                                       | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Nachname**](a-sn.md)                                                                                | False     | [**Person**](c-person.md)<br/>                                 |
| [**Systemflags**](a-systemflags.md)                                                                  | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Telefonnummer**](a-telephonenumber.md)                                                          | False     | [**Person**](c-person.md)<br/>                                 |
| [**Teletex-Terminal-Identifier**](a-teletexterminalidentifier.md)                                     | False     | **Unternehmensperson**                                             |
| [**Telex-Number**](a-telexnumber.md)                                                                  | False     | **Unternehmensperson**                                             |
| [**Telex-Primary**](a-primarytelexnumber.md)                                                          | False     | **Unternehmensperson**                                             |
| [**Text-Country**](a-co.md)                                                                           | False     | **Unternehmensperson**                                             |
| [**Titel**](a-title.md)                                                                               | False     | **Unternehmensperson**                                             |
| [**Benutzerkommentar**](a-comment.md)                                                                      | False     | **Unternehmensperson**                                             |
| [**Benutzerkennwort**](a-userpassword.md)                                                                | False     | [**Person**](c-person.md)<br/>                                 |
| [**USN-Changed**](a-usnchanged.md)                                                                    | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**VON USN erstellt**](a-usncreated.md)                                                                    | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                                             | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**USN-Intersite**](a-usnintersite.md)                                                                | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                                            | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**USN-Quelle**](a-usnsource.md)                                                                      | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Wbem-Path**](a-wbempath.md)                                                                        | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Bekannte Objekte**](a-wellknownobjects.md)                                                       | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Wenn geändert**](a-whenchanged.md)                                                                  | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**Wenn erstellt**](a-whencreated.md)                                                                  | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**WWW-Homepage**](a-wwwhomepage.md)                                                                 | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**WWW-Page-Other**](a-url.md)                                                                        | False     | [**Nach oben**](c-top.md)<br/>                                       |
| [**X121-Adresse**](a-x121address.md)                                                                  | False     | **Unternehmensperson**                                             |



 

 





