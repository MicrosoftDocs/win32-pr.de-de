---
title: Contact Klasse
description: Diese Klasse enthält Informationen zu einer Person oder einem Unternehmen, die Sie möglicherweise regelmäßig kontaktieren müssen.
ms.assetid: 2372ea2b-1ac3-4173-950f-4ee00138fe22
ms.tgt_platform: multiple
keywords:
- Kontaktklasse AD-Schema
- Contact Class AD Schema
topic_type:
- apiref
api_name:
- Contact
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4b54d5929e11382c1680090adf376f670d8610fd767a193e349a31f54c1f2cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119021888"
---
# <a name="contact-class"></a>Contact Klasse

Diese Klasse enthält Informationen zu einer Person oder einem Unternehmen, die Sie möglicherweise regelmäßig kontaktieren müssen.



| Eingabe | Wert |
|-------------------|------------------------------------------------|
| CN                | Contact                                        |
| Ldap-Anzeigename | contact                                        |
| Aktualisieren von Berechtigungen  | Dieser Wert wird vom Domänenadministrator festgelegt. |
| Updatehäufigkeit  | \-                                             |
| Schema-ID-GUID    | 5cb41ed0-0e4c-11d0-a286-00aa003049e2           |



## <a name="implementations"></a>Implementierungen

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server

-   [Attribute](#windows-2000-server-attributes)
-   [Eigenschaftensätze](#windows-2000-server-property-sets)



| Eingabe | Wert |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Falsch                                                                                        |
| Object-Category             | 1                                                                                            |
| Default-Object-Category     | [**Person**](c-person.md)<br/>                                                        |
| Governs-Id                  | 1.2.840.113556.1.5.15                                                                        |
| Default-Hiding-Value        | 0                                                                                            |
| Rdn-Att-Id                  | [**Common-Name**](a-cn.md)<br/>                                                       |
| Unterklasse von                 | [**Unternehmensperson**](c-organizationalperson.md)<br/>                           |
| Mögliche Vorgesetzte          | [**Organisationseinheit "Domain-DNS"**](c-domaindns.md)[](c-organizationalunit.md)         |
| Zusätzlich           | [**E-Mail-Empfänger**](c-mailrecipient.md) (System)                                           |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                 |
| Standardsicherheitsdeskriptor | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;;; AU) |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-2000-server-attributes"></a>Windows 2000-Serverattribute

Diese Klasse enthält die folgenden Attribute für Windows 2000-Server:



| attribute                                                                 | Obligatorisch. | Abgeleitet von                                                                                                                           |
|---------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**Zusätzliche Informationen**](a-notes.md)                                 | Falsch     | **Kontakt**                                                                                                                            |
| [**Adresse**](a-streetaddress.md)                                        | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Address-Home**](a-homepostaladdress.md)                               | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Admin-Description**](a-admindescription.md)                           | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Administratoranzeigename**](a-admindisplayname.md)                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Attributes**](a-allowedattributes.md)                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)      | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md) | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Assistent**](a-assistant.md)                                          | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)             | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Kanonischer Name**](a-canonicalname.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Kommentar**](a-info.md)                                                 | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Common-Name**](a-cn.md)                                               | Richtig      | **Kontaktperson** [](c-person.md)<br/> [**E-Mail-Empfänger**](c-mailrecipient.md)<br/> [**Nach oben**](c-top.md)<br/> |
| [**Unternehmen**](a-company.md)                                              | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Ländercode**](a-countrycode.md)                                     | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Country-Name**](a-c.md)                                               | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Erstellen eines Zeitstempels**](a-createtimestamp.md)                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Department**](a-department.md)                                        | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Beschreibung**](a-description.md)                                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Zielindikator**](a-destinationindicator.md)                   | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Anzeigename**](a-displayname.md)                                     | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Anzeigename– druckbar**](a-displaynameprintable.md)                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Division**](a-division.md)                                            | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**DSA-Signature**](a-dsasignature.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**DS-Core-Propagierungsdaten**](a-dscorepropagationdata.md)               | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**E-Mail-Adressen**](a-mail.md)                                        | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Mitarbeiter-ID**](a-employeeid.md)                                       | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Erweiterungsname**](a-extensionname.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Facsimile-Telephone-Number**](a-facsimiletelephonenumber.md)          | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Flaggen**](a-flags.md)                                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**From-Entry**](a-fromentry.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)             | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Garbage-Coll-Period**](a-garbagecollperiod.md)                        | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Generation-Qualifier**](a-generationqualifier.md)                     | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Vorname**](a-givenname.md)                                         | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Initialen**](a-initials.md)                                            | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Instanztyp**](a-instancetype.md)                                   | Richtig      | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**International-ISDN-Number**](a-internationalisdnnumber.md)            | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)             | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Is-Deleted**](a-isdeleted.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Is-Member-of-DL**](a-memberof.md)                                     | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Last-Known-Parent**](a-lastknownparent.md)                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Legacy-Exchange-DN**](a-legacyexchangedn.md)                          | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Locality-Name**](a-l.md)                                              | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Logo**](a-thumbnaillogo.md)                                           | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Verwaltete Objekte**](a-managedobjects.md)                               | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Manager**](a-manager.md)                                              | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Mastered-By**](a-masteredby.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**MHS-OR-Adresse**](a-mhsoraddress.md)                                  | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Modify-Time-Stamp**](a-modifytimestamp.md)                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Non-Security-Member-BL**](a-nonsecuritymemberbl.md)                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                  | Richtig      | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Obj-Dist-Name**](a-distinguishedname.md)                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Objektkategorie**](a-objectcategory.md)                               | Richtig      | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Objektklasse**](a-objectclass.md)                                     | Richtig      | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Objekt-GUID**](a-objectguid.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Objektversion**](a-objectversion.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Name der Organisationseinheit**](a-ou.md)                                  | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Organisationsname**](a-o.md)                                          | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Sonstiges Postfach**](a-othermailbox.md)                                   | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Anderer Name**](a-middlename.md)                                        | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Andere bekannte Objekte**](a-otherwellknownobjects.md)               | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Teilattributlöschungsliste**](a-partialattributedeletionlist.md) | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Teilattributsatz**](a-partialattributeset.md)                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Personal-Title**](a-personaltitle.md)                                 | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-Fax-Other**](a-otherfacsimiletelephonenumber.md)                | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-Home-Other**](a-otherhomephone.md)                              | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-Home-Primary**](a-homephone.md)                                 | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-Ip-Other**](a-otheripphone.md)                                  | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-Ip-Primary**](a-ipphone.md)                                     | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-ISDN-Primary**](a-primaryinternationalisdnnumber.md)            | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-Mobile-Other**](a-othermobile.md)                               | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-Mobile-Primary**](a-mobile.md)                                  | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-Office-Other**](a-othertelephone.md)                            | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-Pager-Other**](a-otherpager.md)                                 | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-Pager-Primary**](a-pager.md)                                    | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Physical-Delivery-Office-Name**](a-physicaldeliveryofficename.md)     | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Bild**](a-thumbnailphoto.md)                                       | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Mögliche Hindernisse**](a-possibleinferiors.md)                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Postanschrift**](a-postaladdress.md)                                 | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Postleitzahl**](a-postalcode.md)                                       | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Post-Office-Box**](a-postofficebox.md)                                | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Preferred-Delivery-Method**](a-preferreddeliverymethod.md)            | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Proxyadressen**](a-proxyaddresses.md)                               | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Query-Policy-BL**](a-querypolicybl.md)                                | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Rdn**](a-name.md)                                                     | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Registrierte Adresse**](a-registeredaddress.md)                         | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Berichte**](a-directreports.md)                                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Reps-From**](a-repsfrom.md)                                           | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Reps-To**](a-repsto.md)                                               | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Revision**](a-revision.md)                                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Siehe auch**](a-seealso.md)                                             | Falsch     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**Server-Reference-BL**](a-serverreferencebl.md)                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Show-In-Address-Book**](a-showinaddressbook.md)                       | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Nur in erweiterter Ansicht anzeigen**](a-showinadvancedviewonly.md)            | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Site-Object-BL**](a-siteobjectbl.md)                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**State-or-Province-Name**](a-st.md)                                    | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Adresse der Straße**](a-street.md)                                        | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Sub-Refs**](a-subrefs.md)                                             | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Nachname**](a-sn.md)                                                   | Falsch     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**Systemflags**](a-systemflags.md)                                     | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Telefonnummer**](a-telephonenumber.md)                             | Falsch     | [**Person**](c-person.md)<br/> [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                             |
| [**Teletex-Terminal-Identifier**](a-teletexterminalidentifier.md)        | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telex-Number**](a-telexnumber.md)                                     | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telex-Primary**](a-primarytelexnumber.md)                             | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Text-Country**](a-co.md)                                              | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Textcodierte OR-Adresse**](a-textencodedoraddress.md)                 | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Titel**](a-title.md)                                                  | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**User-Cert**](a-usercert.md)                                           | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Benutzerkommentar**](a-comment.md)                                         | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Benutzerkennwort**](a-userpassword.md)                                   | Falsch     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**User-SMIME-Certificate**](a-usersmimecertificate.md)                  | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**USN geändert**](a-usnchanged.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**USN-erstellt**](a-usncreated.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**USN-DSA-last-obj-removed**](a-usndsalastobjremoved.md)                | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**USN-Intersite**](a-usnintersite.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                               | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**USN-Quelle**](a-usnsource.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Wbem-Pfad**](a-wbempath.md)                                           | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Bekannte Objekte**](a-wellknownobjects.md)                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Bei Änderung**](a-whenchanged.md)                                     | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Bei der Erstellung**](a-whencreated.md)                                     | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**WWW-Startseite**](a-wwwhomepage.md)                                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**WWW-Page-Other**](a-url.md)                                           | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**X121-Address**](a-x121address.md)                                     | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**X509-Cert**](a-usercertificate.md)                                    | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |



## <a name="windows-2000-server-property-sets"></a>Windows 2000-Servereigenschaftensätze

Diese Klasse enthält die folgenden Eigenschaftensätze für Windows 2000 Server:



| Allgemeiner Name                                            |
|--------------------------------------------------------|
| [**Persönliche Informationen**](r-personal-information.md) |
| [**Webinformationen**](r-web-information.md)           |



## <a name="windows-server-2003"></a>Windows Server 2003

-   [Attribute](#windows-server-2003-attributes)
-   [Eigenschaftensätze](#windows-server-2003-property-sets)



| Eingabe | Wert |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Falsch                                                                                        |
| Object-Category             | 1                                                                                            |
| Default-Object-Category     | [**Person**](c-person.md)<br/>                                                        |
| Governs-Id                  | 1.2.840.113556.1.5.15                                                                        |
| Default-Hiding-Value        | 0                                                                                            |
| Rdn-Att-Id                  | [**Allgemeiner Name**](a-cn.md)<br/>                                                       |
| Unterklasse von                 | [**Unternehmensperson**](c-organizationalperson.md)<br/>                           |
| Mögliche Übergeordnete          | [**Domänen-DNS-Organisationseinheit**](c-domaindns.md)[](c-organizationalunit.md)         |
| Zusätzlich           | [**E-Mail-Empfänger**](c-mailrecipient.md) (System)                                           |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                 |
| Standardsicherheitsdeskriptor | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;;; AU) |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2003-attributes"></a>Windows Server 2003-Attribute

Diese Klasse enthält die folgenden Attribute für Windows Server 2003:



| attribute                                                                   | Obligatorisch. | Abgeleitet von                                                                                                                           |
|-----------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**Zusätzliche Informationen**](a-notes.md)                                   | Falsch     | **Kontakt**                                                                                                                            |
| [**Adresse**](a-streetaddress.md)                                          | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Address-Home**](a-homepostaladdress.md)                                 | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Administratorbeschreibung**](a-admindescription.md)                             | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Admin-Display-Name**](a-admindisplayname.md)                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Attributes**](a-allowedattributes.md)                           | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)        | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)   | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Assistent**](a-assistant.md)                                            | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**attributeCertificateAttribute**](a-attributecertificateattribute.md)    | Falsch     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)               | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Kanonischer Name**](a-canonicalname.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Kommentar**](a-info.md)                                                   | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Allgemeiner Name**](a-cn.md)                                                 | Richtig      |  [ **Kontaktperson**](c-person.md)<br/> [**E-Mail-Empfänger**](c-mailrecipient.md)<br/> [**Nach oben**](c-top.md)<br/> |
| [**Unternehmen**](a-company.md)                                                | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Ländercode**](a-countrycode.md)                                       | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Country-Name**](a-c.md)                                                 | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Erstellen eines Zeitstempels**](a-createtimestamp.md)                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Department**](a-department.md)                                          | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Beschreibung**](a-description.md)                                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Zielindikator**](a-destinationindicator.md)                     | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Anzeigename**](a-displayname.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Anzeigename– druckbar**](a-displaynameprintable.md)                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Division**](a-division.md)                                              | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**DSA-Signature**](a-dsasignature.md)                                     | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**DS-Core-Propagierungsdaten**](a-dscorepropagationdata.md)                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**E-Mail-Adressen**](a-mail.md)                                          | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Mitarbeiter-ID**](a-employeeid.md)                                         | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Extension-Name**](a-extensionname.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Facsimile-Telephone-Number**](a-facsimiletelephonenumber.md)            | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Flaggen**](a-flags.md)                                                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**From-Entry**](a-fromentry.md)                                           | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)               | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Garbage Coll-Period**](a-garbagecollperiod.md)                          | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Generation-Qualifier**](a-generationqualifier.md)                       | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Given-Name**](a-givenname.md)                                           | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**houseIdentifier**](a-houseidentifier.md)                                | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Initialen**](a-initials.md)                                              | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Instanztyp**](a-instancetype.md)                                     | Richtig      | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**International-ISDN-Number**](a-internationalisdnnumber.md)              | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)               | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Is-Deleted**](a-isdeleted.md)                                           | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Is-Member-of-DL**](a-memberof.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**labeledURI**](a-labeleduri.md)                                          | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Letztes bekanntes übergeordnetes Element**](a-lastknownparent.md)                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Legacy-Exchange-DN**](a-legacyexchangedn.md)                            | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Locality-Name**](a-l.md)                                                | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Logo**](a-thumbnaillogo.md)                                             | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Verwaltete Objekte**](a-managedobjects.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Manager**](a-manager.md)                                                | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Mastered By**](a-masteredby.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**MHS-OR-Adresse**](a-mhsoraddress.md)                                    | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Modify-Time-Stamp**](a-modifytimestamp.md)                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Allowed-to-Delegate-To**](a-msds-allowedtodelegateto.md)          | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md) | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)      | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Members-for-Az-Role-BL**](a-msds-membersforazrolebl.md)           | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)  | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)               | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Operations-for-Az-Role-BL**](a-msds-operationsforazrolebl.md)     | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Operations-for-Az-Task-BL**](a-msds-operationsforaztaskbl.md)     | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)      | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)              | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Tasks-for-Az-Role-BL**](a-msds-tasksforazrolebl.md)               | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Tasks-for-Az-Task-BL**](a-msds-tasksforaztaskbl.md)               | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-Exch-Assistant-Name**](a-msexchassistantname.md)                     | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**ms-Exch-House-Identifier**](a-msexchhouseidentifier.md)                 | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-Exch-LabeledURI**](a-msexchlabeleduri.md)                            | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Non-Security-Member-BL**](a-nonsecuritymemberbl.md)                     | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                    | Richtig      | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Objektkategorie**](a-objectcategory.md)                                 | Richtig      | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Objektklasse**](a-objectclass.md)                                       | Richtig      | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Objekt-GUID**](a-objectguid.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Objektversion**](a-objectversion.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Name der Organisationseinheit**](a-ou.md)                                    | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Organisationsname**](a-o.md)                                            | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Sonstiges Postfach**](a-othermailbox.md)                                     | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Anderer Name**](a-middlename.md)                                          | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Andere bekannte Objekte**](a-otherwellknownobjects.md)                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Teilattributlöschungsliste**](a-partialattributedeletionlist.md)   | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Teilattributsatz**](a-partialattributeset.md)                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Personal-Title**](a-personaltitle.md)                                   | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-Fax-Other**](a-otherfacsimiletelephonenumber.md)                  | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-Home-Other**](a-otherhomephone.md)                                | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-Home-Primary**](a-homephone.md)                                   | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-Ip-Other**](a-otheripphone.md)                                    | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-Ip-Primary**](a-ipphone.md)                                       | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-ISDN-Primary**](a-primaryinternationalisdnnumber.md)              | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-Mobile-Other**](a-othermobile.md)                                 | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-Mobile-Primary**](a-mobile.md)                                    | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-Office-Other**](a-othertelephone.md)                              | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-Pager-Other**](a-otherpager.md)                                   | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-Pager-Primary**](a-pager.md)                                      | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Physical-Delivery-Office-Name**](a-physicaldeliveryofficename.md)       | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Bild**](a-thumbnailphoto.md)                                         | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Mögliche Hindernisse**](a-possibleinferiors.md)                           | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Postanschrift**](a-postaladdress.md)                                   | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Postleitzahl**](a-postalcode.md)                                         | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Post-Office-Box**](a-postofficebox.md)                                  | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Preferred-Delivery-Method**](a-preferreddeliverymethod.md)              | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Proxyadressen**](a-proxyaddresses.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Query-Policy-BL**](a-querypolicybl.md)                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Rdn**](a-name.md)                                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Registrierte Adresse**](a-registeredaddress.md)                           | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Berichte**](a-directreports.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Reps-From**](a-repsfrom.md)                                             | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Reps-To**](a-repsto.md)                                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Revision**](a-revision.md)                                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**secretary**](a-secretary.md)                                            | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Siehe auch**](a-seealso.md)                                               | Falsch     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**Seriennummer**](a-serialnumber.md)                                     | Falsch     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**Server-Reference-BL**](a-serverreferencebl.md)                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Show-In-Address-Book**](a-showinaddressbook.md)                         | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Nur in erweiterter Ansicht anzeigen**](a-showinadvancedviewonly.md)              | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**State-or-Province-Name**](a-st.md)                                      | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Adresse der Straße**](a-street.md)                                          | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Sub-Refs**](a-subrefs.md)                                               | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Nachname**](a-sn.md)                                                     | Falsch     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**Systemflags**](a-systemflags.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Telefonnummer**](a-telephonenumber.md)                               | Falsch     | [**Person**](c-person.md)<br/> [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                             |
| [**Teletex-Terminal-Identifier**](a-teletexterminalidentifier.md)          | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telex-Number**](a-telexnumber.md)                                       | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telex-Primary**](a-primarytelexnumber.md)                               | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Text-Country**](a-co.md)                                                | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Textcodierte OR-Adresse**](a-textencodedoraddress.md)                   | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Titel**](a-title.md)                                                    | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**User-Cert**](a-usercert.md)                                             | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Benutzerkommentar**](a-comment.md)                                           | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Benutzerkennwort**](a-userpassword.md)                                     | Falsch     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**User-SMIME-Certificate**](a-usersmimecertificate.md)                    | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**USN geändert**](a-usnchanged.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**USN-erstellt**](a-usncreated.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**USN-DSA-last-obj-removed**](a-usndsalastobjremoved.md)                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**USN-Intersite**](a-usnintersite.md)                                     | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**USN-Quelle**](a-usnsource.md)                                           | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Wbem-Pfad**](a-wbempath.md)                                             | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Bekannte Objekte**](a-wellknownobjects.md)                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Bei Änderung**](a-whenchanged.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Bei der Erstellung**](a-whencreated.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**WWW-Homepage**](a-wwwhomepage.md)                                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**WWW-Page-Other**](a-url.md)                                             | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**X121-Adresse**](a-x121address.md)                                       | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**X509-Cert**](a-usercertificate.md)                                      | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |



## <a name="windows-server-2003-property-sets"></a>Windows Server 2003-Eigenschaftensätze

Diese Klasse enthält die folgenden Eigenschaftensätze für Windows Server 2003:



| Allgemeiner Name                                            |
|--------------------------------------------------------|
| [**Persönliche Informationen**](r-personal-information.md) |
| [**Webinformationen**](r-web-information.md)           |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2

-   [Attribute](#windows-server-2003-r2-attributes)
-   [Eigenschaftensätze](#windows-server-2003-r2-property-sets)



| Eingabe | Wert |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Falsch                                                                                        |
| Object-Category             | 1                                                                                            |
| Default-Object-Category     | [**Person**](c-person.md)<br/>                                                        |
| Governs-Id                  | 1.2.840.113556.1.5.15                                                                        |
| Default-Hiding-Value        | 0                                                                                            |
| Rdn-Att-Id                  | [**Common-Name**](a-cn.md)<br/>                                                       |
| Unterklasse von                 | [**Unternehmensperson**](c-organizationalperson.md)<br/>                           |
| Mögliche Vorgesetzte          | [**Organisationseinheit "Domain-DNS"**](c-domaindns.md)[](c-organizationalunit.md)         |
| Zusätzlich           | [**E-Mail-Empfänger**](c-mailrecipient.md) (System)                                           |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                 |
| Standardsicherheitsdeskriptor | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;;; AU) |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2003-r2-attributes"></a>Windows Server 2003 R2-Attribute

Diese Klasse enthält die folgenden Attribute für Windows Server 2003 R2:



| attribute                                                                   | Obligatorisch. | Abgeleitet von                                                                                                                           |
|-----------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**Zusätzliche Informationen**](a-notes.md)                                   | Falsch     | **Kontakt**                                                                                                                            |
| [**Adresse**](a-streetaddress.md)                                          | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Address-Home**](a-homepostaladdress.md)                                 | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Admin-Description**](a-admindescription.md)                             | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Administratoranzeigename**](a-admindisplayname.md)                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Attributes**](a-allowedattributes.md)                           | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)        | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)   | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Assistent**](a-assistant.md)                                            | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**attributeCertificateAttribute**](a-attributecertificateattribute.md)    | Falsch     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)               | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Kanonischer Name**](a-canonicalname.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Kommentar**](a-info.md)                                                   | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Common-Name**](a-cn.md)                                                 | Richtig      | **Kontaktperson** [](c-person.md)<br/> [**E-Mail-Empfänger**](c-mailrecipient.md)<br/> [**Nach oben**](c-top.md)<br/> |
| [**Unternehmen**](a-company.md)                                                | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Ländercode**](a-countrycode.md)                                       | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Country-Name**](a-c.md)                                                 | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Create-Time-Stamp**](a-createtimestamp.md)                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Department**](a-department.md)                                          | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Beschreibung**](a-description.md)                                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Destination-Indicator**](a-destinationindicator.md)                     | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Anzeigename**](a-displayname.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Display-Name-Printable**](a-displaynameprintable.md)                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Division**](a-division.md)                                              | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**DSA-Signature**](a-dsasignature.md)                                     | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**DS-Core-Propagierungsdaten**](a-dscorepropagationdata.md)                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**E-Mail-Adressen**](a-mail.md)                                          | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Mitarbeiter-ID**](a-employeeid.md)                                         | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Extension-Name**](a-extensionname.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Facsimile-Telephone-Number**](a-facsimiletelephonenumber.md)            | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Flaggen**](a-flags.md)                                                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**From-Entry**](a-fromentry.md)                                           | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)               | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Garbage Coll-Period**](a-garbagecollperiod.md)                          | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Generation-Qualifier**](a-generationqualifier.md)                       | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Given-Name**](a-givenname.md)                                           | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**houseIdentifier**](a-houseidentifier.md)                                | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Initialen**](a-initials.md)                                              | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Instanztyp**](a-instancetype.md)                                     | Richtig      | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**International-ISDN-Number**](a-internationalisdnnumber.md)              | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)               | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Is-Deleted**](a-isdeleted.md)                                           | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Is-Member-of-DL**](a-memberof.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**labeledURI**](a-labeleduri.md)                                          | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Letztes bekanntes übergeordnetes Element**](a-lastknownparent.md)                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Legacy-Exchange-DN**](a-legacyexchangedn.md)                            | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Locality-Name**](a-l.md)                                                | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Logo**](a-thumbnaillogo.md)                                             | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Verwaltete Objekte**](a-managedobjects.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Manager**](a-manager.md)                                                | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Mastered-By**](a-masteredby.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**MHS-OR-Adresse**](a-mhsoraddress.md)                                    | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Modify-Time-Stamp**](a-modifytimestamp.md)                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)         | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)             | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Allowed-to-Delegate-To**](a-msds-allowedtodelegateto.md)          | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md) | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)      | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Members-for-Az-Role-BL**](a-msds-membersforazrolebl.md)           | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)  | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)               | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Operations-for-Az-Role-BL**](a-msds-operationsforazrolebl.md)     | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Operations-for-Az-Task-BL**](a-msds-operationsforaztaskbl.md)     | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)      | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)              | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Source-Object-DN**](a-msds-sourceobjectdn.md)                     | Falsch     | **Kontakt**                                                                                                                            |
| [**ms-DS-Tasks-for-Az-Role-BL**](a-msds-tasksforazrolebl.md)               | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Tasks-for-Az-Task-BL**](a-msds-tasksforaztaskbl.md)               | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-Exch-Assistant-Name**](a-msexchassistantname.md)                     | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**ms-Exch-House-Identifier**](a-msexchhouseidentifier.md)                 | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-Exch-LabeledURI**](a-msexchlabeleduri.md)                            | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Non-Security-Member-BL**](a-nonsecuritymemberbl.md)                     | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                    | Richtig      | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Objektkategorie**](a-objectcategory.md)                                 | Richtig      | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Object-Class**](a-objectclass.md)                                       | Richtig      | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Objekt-GUID**](a-objectguid.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Object-Version**](a-objectversion.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Organisationseinheitsname**](a-ou.md)                                    | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Organisationsname**](a-o.md)                                            | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Sonstiges Postfach**](a-othermailbox.md)                                     | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Other-Name**](a-middlename.md)                                          | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Andere bekannte Objekte**](a-otherwellknownobjects.md)                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)   | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Personal-Title**](a-personaltitle.md)                                   | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-Fax-Other**](a-otherfacsimiletelephonenumber.md)                  | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-Home-Other**](a-otherhomephone.md)                                | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-Home-Primary**](a-homephone.md)                                   | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-Ip-Other**](a-otheripphone.md)                                    | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-Ip-Primary**](a-ipphone.md)                                       | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-ISDN-Primary**](a-primaryinternationalisdnnumber.md)              | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-Mobile-Other**](a-othermobile.md)                                 | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-Mobile-Primary**](a-mobile.md)                                    | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-Office-Other**](a-othertelephone.md)                              | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-Pager-Other**](a-otherpager.md)                                   | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-Pager-Primary**](a-pager.md)                                      | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Physical-Delivery-Office-Name**](a-physicaldeliveryofficename.md)       | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Bild**](a-thumbnailphoto.md)                                         | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Mögliche 100000000000**](a-possibleinferiors.md)                           | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Postal-Address**](a-postaladdress.md)                                   | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Postleitzahl**](a-postalcode.md)                                         | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Post-Office-Box**](a-postofficebox.md)                                  | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Preferred-Delivery-Method**](a-preferreddeliverymethod.md)              | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Proxyadressen**](a-proxyaddresses.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Query-Policy-BL**](a-querypolicybl.md)                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Rdn**](a-name.md)                                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Registrierte Adresse**](a-registeredaddress.md)                           | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Berichte**](a-directreports.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Reps-From**](a-repsfrom.md)                                             | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Reps-To**](a-repsto.md)                                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Revision**](a-revision.md)                                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**secretary**](a-secretary.md)                                            | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Siehe auch**](a-seealso.md)                                               | Falsch     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**Seriennummer**](a-serialnumber.md)                                     | Falsch     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**Server-Reference-BL**](a-serverreferencebl.md)                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Show-In-Address-Book**](a-showinaddressbook.md)                         | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Nur in erweiterter Ansicht anzeigen**](a-showinadvancedviewonly.md)              | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**State-or-Province-Name**](a-st.md)                                      | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Adresse der Straße**](a-street.md)                                          | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Sub-Refs**](a-subrefs.md)                                               | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Nachname**](a-sn.md)                                                     | Falsch     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**Systemflags**](a-systemflags.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Telefonnummer**](a-telephonenumber.md)                               | Falsch     | [**Person**](c-person.md)<br/> [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                             |
| [**Teletex-Terminal-Identifier**](a-teletexterminalidentifier.md)          | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telex-Number**](a-telexnumber.md)                                       | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telex-Primary**](a-primarytelexnumber.md)                               | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Text-Country**](a-co.md)                                                | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Textcodierte OR-Adresse**](a-textencodedoraddress.md)                   | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Titel**](a-title.md)                                                    | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**User-Cert**](a-usercert.md)                                             | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Benutzerkommentar**](a-comment.md)                                           | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Benutzerkennwort**](a-userpassword.md)                                     | Falsch     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**User-SMIME-Certificate**](a-usersmimecertificate.md)                    | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**USN-Changed**](a-usnchanged.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**VON USN erstellt**](a-usncreated.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**USN-Intersite**](a-usnintersite.md)                                     | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**USN-Quelle**](a-usnsource.md)                                           | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Wbem-Path**](a-wbempath.md)                                             | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Bekannte Objekte**](a-wellknownobjects.md)                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Wenn geändert**](a-whenchanged.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Wenn erstellt**](a-whencreated.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**WWW-Homepage**](a-wwwhomepage.md)                                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**WWW-Page-Other**](a-url.md)                                             | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**X121-Adresse**](a-x121address.md)                                       | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**X509-Cert**](a-usercertificate.md)                                      | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |



## <a name="windows-server-2003-r2-property-sets"></a>Windows Server 2003 R2-Eigenschaftensätze

Diese Klasse enthält die folgenden Eigenschaftensätze für Windows Server 2003 R2:



| Allgemeiner Name                                            |
|--------------------------------------------------------|
| [**Persönliche Informationen**](r-personal-information.md) |
| [**Webinformationen**](r-web-information.md)           |



## <a name="windows-server-2008"></a>Windows Server 2008

-   [Attribute](#windows-server-2008-attributes)
-   [Eigenschaftensätze](#windows-server-2008-property-sets)



| Eingabe | Wert |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Falsch                                                                                        |
| Object-Category             | 1                                                                                            |
| Default-Object-Category     | [**Person**](c-person.md)<br/>                                                        |
| Governs-Id                  | 1.2.840.113556.1.5.15                                                                        |
| Default-Hiding-Value        | 0                                                                                            |
| Rdn-Att-Id                  | [**Common-Name**](a-cn.md)<br/>                                                       |
| Unterklasse von                 | [**Unternehmensperson**](c-organizationalperson.md)<br/>                           |
| Mögliche Vorgesetzte          | [**Organisationseinheit "Domain-DNS"**](c-domaindns.md)[](c-organizationalunit.md)         |
| Zusätzlich           | [**E-Mail-Empfänger**](c-mailrecipient.md) (System)                                           |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                 |
| Standardsicherheitsdeskriptor | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;;; AU) |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2008-attributes"></a>Windows Server 2008-Attribute

Diese Klasse enthält die folgenden Attribute für Windows Server 2008:



| attribute                                                                      | Obligatorisch. | Abgeleitet von                                                                                                                           |
|--------------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**Zusätzliche Informationen**](a-notes.md)                                      | Falsch     | **Kontakt**                                                                                                                            |
| [**Adresse**](a-streetaddress.md)                                             | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Address-Home**](a-homepostaladdress.md)                                    | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Admin-Description**](a-admindescription.md)                                | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Administratoranzeigename**](a-admindisplayname.md)                               | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Attributes**](a-allowedattributes.md)                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)           | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)      | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Assistent**](a-assistant.md)                                               | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**attributeCertificateAttribute**](a-attributecertificateattribute.md)       | Falsch     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Kanonischer Name**](a-canonicalname.md)                                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Kommentar**](a-info.md)                                                      | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Common-Name**](a-cn.md)                                                    | Richtig      | **Kontaktperson** [](c-person.md)<br/> [**E-Mail-Empfänger**](c-mailrecipient.md)<br/> [**Nach oben**](c-top.md)<br/> |
| [**Unternehmen**](a-company.md)                                                   | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Ländercode**](a-countrycode.md)                                          | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Country-Name**](a-c.md)                                                    | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Create-Time-Stamp**](a-createtimestamp.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Department**](a-department.md)                                             | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Beschreibung**](a-description.md)                                           | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Destination-Indicator**](a-destinationindicator.md)                        | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Anzeigename**](a-displayname.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Display-Name-Printable**](a-displaynameprintable.md)                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Division**](a-division.md)                                                 | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**DSA-Signature**](a-dsasignature.md)                                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**DS-Core-Propagierungsdaten**](a-dscorepropagationdata.md)                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**E-Mail-Adressen**](a-mail.md)                                             | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Mitarbeiter-ID**](a-employeeid.md)                                            | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Extension-Name**](a-extensionname.md)                                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Facsimile-Telephone-Number**](a-facsimiletelephonenumber.md)               | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Flaggen**](a-flags.md)                                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**From-Entry**](a-fromentry.md)                                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                     | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Garbage Coll-Period**](a-garbagecollperiod.md)                             | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Generation-Qualifier**](a-generationqualifier.md)                          | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Given-Name**](a-givenname.md)                                              | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**houseIdentifier**](a-houseidentifier.md)                                   | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Initialen**](a-initials.md)                                                 | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Instanztyp**](a-instancetype.md)                                        | Richtig      | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**International-ISDN-Number**](a-internationalisdnnumber.md)                 | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Is-Deleted**](a-isdeleted.md)                                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Is-Member-of-DL**](a-memberof.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                             | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**labeledURI**](a-labeleduri.md)                                             | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Letztes bekanntes übergeordnetes Element**](a-lastknownparent.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Legacy-Exchange-DN**](a-legacyexchangedn.md)                               | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Locality-Name**](a-l.md)                                                   | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Logo**](a-thumbnaillogo.md)                                                | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Verwaltete Objekte**](a-managedobjects.md)                                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Manager**](a-manager.md)                                                   | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Mastered By**](a-masteredby.md)                                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**MHS-OR-Adresse**](a-mhsoraddress.md)                                       | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Modify-Time-Stamp**](a-modifytimestamp.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)            | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Allowed-to-Delegate-To**](a-msds-allowedtodelegateto.md)             | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md)    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md) | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)         | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-IGE-Seniority-Index**](a-msds-habseniorityindex.md)                  | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-Is-Domain-For**](a-msds-isdomainfor.md)                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-is-full-replica-for**](a-msds-isfullreplicafor.md)                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-is-partial-replica-for**](a-msds-ispartialreplicafor.md)             | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Members-for-Az-Role-BL**](a-msds-membersforazrolebl.md)              | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)       | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)     | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)  | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-NC-Type**](a-msds-nctype.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Operations-for-Az-Role-BL**](a-msds-operationsforazrolebl.md)        | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Operations-for-Az-Task-BL**](a-msds-operationsforaztaskbl.md)        | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Phonetic-Company-Name**](a-msds-phoneticcompanyname.md)              | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-Phonetic-Department**](a-msds-phoneticdepartment.md)                 | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-Phonetic-Display-Name**](a-msds-phoneticdisplayname.md)              | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/> [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                |
| [**ms-DS-Phonetic-First-Name**](a-msds-phoneticfirstname.md)                  | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-Phonetic-Last-Name**](a-msds-phoneticlastname.md)                    | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                           | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-PSO-Applied**](a-msds-psoapplied.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)         | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Revealed-DSAs**](a-msds-revealeddsas.md)                             | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Revealed-List-BL**](a-msds-revealedlistbl.md)                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Source-Object-DN**](a-msds-sourceobjectdn.md)                        | Falsch     | **Kontakt**                                                                                                                            |
| [**ms-DS-Tasks-for-Az-Role-BL**](a-msds-tasksforazrolebl.md)                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Tasks-for-Az-Task-BL**](a-msds-tasksforaztaskbl.md)                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-Exch-Assistant-Name**](a-msexchassistantname.md)                        | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**ms-Exch-House-Identifier**](a-msexchhouseidentifier.md)                    | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-Exch-LabeledURI**](a-msexchlabeleduri.md)                               | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                     | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Non-Security-Member-BL**](a-nonsecuritymemberbl.md)                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                       | Richtig      | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Objektkategorie**](a-objectcategory.md)                                    | Richtig      | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Object-Class**](a-objectclass.md)                                          | Richtig      | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Objekt-GUID**](a-objectguid.md)                                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Object-Version**](a-objectversion.md)                                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Organisationseinheitsname**](a-ou.md)                                       | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Organisationsname**](a-o.md)                                               | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Sonstiges Postfach**](a-othermailbox.md)                                        | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Other-Name**](a-middlename.md)                                             | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Andere bekannte Objekte**](a-otherwellknownobjects.md)                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)      | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Personal-Title**](a-personaltitle.md)                                      | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-Fax-Other**](a-otherfacsimiletelephonenumber.md)                     | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-Home-Other**](a-otherhomephone.md)                                   | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-Home-Primary**](a-homephone.md)                                      | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-Ip-Other**](a-otheripphone.md)                                       | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-Ip-Primary**](a-ipphone.md)                                          | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-ISDN-Primary**](a-primaryinternationalisdnnumber.md)                 | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-Mobile-Other**](a-othermobile.md)                                    | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-Mobile-Primary**](a-mobile.md)                                       | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-Office-Other**](a-othertelephone.md)                                 | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-Pager-Other**](a-otherpager.md)                                      | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-Pager-Primary**](a-pager.md)                                         | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Physical-Delivery-Office-Name**](a-physicaldeliveryofficename.md)          | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Bild**](a-thumbnailphoto.md)                                            | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Mögliche 100000000000**](a-possibleinferiors.md)                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Postal-Address**](a-postaladdress.md)                                      | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Postleitzahl**](a-postalcode.md)                                            | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Post-Office-Box**](a-postofficebox.md)                                     | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Preferred-Delivery-Method**](a-preferreddeliverymethod.md)                 | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                             | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Proxyadressen**](a-proxyaddresses.md)                                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Query-Policy-BL**](a-querypolicybl.md)                                     | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Rdn**](a-name.md)                                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Registrierte Adresse**](a-registeredaddress.md)                              | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                           | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Berichte**](a-directreports.md)                                             | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Reps-From**](a-repsfrom.md)                                                | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Reps-To**](a-repsto.md)                                                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Revision**](a-revision.md)                                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                             | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**secretary**](a-secretary.md)                                               | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Siehe auch**](a-seealso.md)                                                  | Falsch     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**Seriennummer**](a-serialnumber.md)                                        | Falsch     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**Server-Reference-BL**](a-serverreferencebl.md)                             | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Show-In-Address-Book**](a-showinaddressbook.md)                            | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Nur in erweiterter Ansicht anzeigen**](a-showinadvancedviewonly.md)                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Site-Object-BL**](a-siteobjectbl.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**State-or-Province-Name**](a-st.md)                                         | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Adresse der Straße**](a-street.md)                                             | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                     | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Sub-Refs**](a-subrefs.md)                                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                               | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Nachname**](a-sn.md)                                                        | Falsch     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**Systemflags**](a-systemflags.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Telefonnummer**](a-telephonenumber.md)                                  | Falsch     | [**Person**](c-person.md)<br/> [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                             |
| [**Teletex-Terminal-Identifier**](a-teletexterminalidentifier.md)             | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telex-Number**](a-telexnumber.md)                                          | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telex-Primary**](a-primarytelexnumber.md)                                  | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Text-Country**](a-co.md)                                                   | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Textcodierte OR-Adresse**](a-textencodedoraddress.md)                      | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Titel**](a-title.md)                                                       | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**User-Cert**](a-usercert.md)                                                | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Benutzerkommentar**](a-comment.md)                                              | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Benutzerkennwort**](a-userpassword.md)                                        | Falsch     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**User-SMIME-Certificate**](a-usersmimecertificate.md)                       | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**USN geändert**](a-usnchanged.md)                                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**USN-erstellt**](a-usncreated.md)                                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**USN-DSA-last-obj-removed**](a-usndsalastobjremoved.md)                     | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**USN-Intersite**](a-usnintersite.md)                                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**USN-Quelle**](a-usnsource.md)                                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Wbem-Pfad**](a-wbempath.md)                                                | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Bekannte Objekte**](a-wellknownobjects.md)                               | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Bei Änderung**](a-whenchanged.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Bei der Erstellung**](a-whencreated.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**WWW-Startseite**](a-wwwhomepage.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**WWW-Page-Other**](a-url.md)                                                | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**X121-Address**](a-x121address.md)                                          | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**X509-Cert**](a-usercertificate.md)                                         | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |



## <a name="windows-server-2008-property-sets"></a>Windows Server 2008-Eigenschaftensätze

Diese Klasse enthält die folgenden Eigenschaftensätze für Windows Server 2008:



| Allgemeiner Name                                            |
|--------------------------------------------------------|
| [**Persönliche Informationen**](r-personal-information.md) |
| [**Webinformationen**](r-web-information.md)           |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2

-   [Attribute](#windows-server-2008-r2-attributes)
-   [Eigenschaftensätze](#windows-server-2008-r2-property-sets)



| Eingabe | Wert |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Falsch                                                                                        |
| Object-Category             | 1                                                                                            |
| Default-Object-Category     | [**Person**](c-person.md)<br/>                                                        |
| Governs-Id                  | 1.2.840.113556.1.5.15                                                                        |
| Default-Hiding-Value        | 0                                                                                            |
| Rdn-Att-Id                  | [**Allgemeiner Name**](a-cn.md)<br/>                                                       |
| Unterklasse von                 | [**Unternehmensperson**](c-organizationalperson.md)<br/>                           |
| Mögliche Übergeordnete          | [**Domänen-DNS-Organisationseinheit**](c-domaindns.md)[](c-organizationalunit.md)         |
| Zusätzlich           | [**E-Mail-Empfänger**](c-mailrecipient.md) (System)                                           |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                 |
| Standardsicherheitsdeskriptor | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;;; AU) |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2008-r2-attributes"></a>Windows Server 2008 R2-Attribute

Diese Klasse enthält die folgenden Attribute für Windows Server 2008 R2:



| attribute                                                                        | Obligatorisch. | Abgeleitet von                                                                                                                           |
|----------------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**Zusätzliche Informationen**](a-notes.md)                                        | Falsch     | **Kontakt**                                                                                                                            |
| [**Adresse**](a-streetaddress.md)                                               | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Address-Home**](a-homepostaladdress.md)                                      | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Admin-Description**](a-admindescription.md)                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Administratoranzeigename**](a-admindisplayname.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Attributes**](a-allowedattributes.md)                                | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)             | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                           | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)        | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Assistent**](a-assistant.md)                                                 | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**attributeCertificateAttribute**](a-attributecertificateattribute.md)         | Falsch     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Kanonischer Name**](a-canonicalname.md)                                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Kommentar**](a-info.md)                                                        | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Common-Name**](a-cn.md)                                                      | Richtig      | **Kontaktperson** [](c-person.md)<br/> [**E-Mail-Empfänger**](c-mailrecipient.md)<br/> [**Nach oben**](c-top.md)<br/> |
| [**Unternehmen**](a-company.md)                                                     | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Ländercode**](a-countrycode.md)                                            | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Country-Name**](a-c.md)                                                      | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Create-Time-Stamp**](a-createtimestamp.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Department**](a-department.md)                                               | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Beschreibung**](a-description.md)                                             | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Destination-Indicator**](a-destinationindicator.md)                          | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Anzeigename**](a-displayname.md)                                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Display-Name-Printable**](a-displaynameprintable.md)                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Division**](a-division.md)                                                   | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**DSA-Signature**](a-dsasignature.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**DS-Core-Propagierungsdaten**](a-dscorepropagationdata.md)                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**E-Mail-Adressen**](a-mail.md)                                               | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Mitarbeiter-ID**](a-employeeid.md)                                              | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Extension-Name**](a-extensionname.md)                                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Facsimile-Telephone-Number**](a-facsimiletelephonenumber.md)                 | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Flaggen**](a-flags.md)                                                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**From-Entry**](a-fromentry.md)                                                | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Garbage Coll-Period**](a-garbagecollperiod.md)                               | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Generation-Qualifier**](a-generationqualifier.md)                            | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Given-Name**](a-givenname.md)                                                | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**houseIdentifier**](a-houseidentifier.md)                                     | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Initialen**](a-initials.md)                                                   | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Instanztyp**](a-instancetype.md)                                          | Richtig      | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**International-ISDN-Number**](a-internationalisdnnumber.md)                   | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Is-Deleted**](a-isdeleted.md)                                                | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Is-Member-of-DL**](a-memberof.md)                                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                               | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Wird wiederverwendet**](a-isrecycled.md)                                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**labeledURI**](a-labeleduri.md)                                               | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Letztes bekanntes übergeordnetes Element**](a-lastknownparent.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Legacy-Exchange-DN**](a-legacyexchangedn.md)                                 | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Locality-Name**](a-l.md)                                                     | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Logo**](a-thumbnaillogo.md)                                                  | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Verwaltete Objekte**](a-managedobjects.md)                                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Manager**](a-manager.md)                                                     | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Mastered By**](a-masteredby.md)                                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**MHS-OR-Adresse**](a-mhsoraddress.md)                                         | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Modify-Time-Stamp**](a-modifytimestamp.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)              | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Allowed-to-Delegate-To**](a-msds-allowedtodelegateto.md)               | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md)      | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md)   | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)           | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Enabled-Feature-BL**](a-msds-enabledfeaturebl.md)                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-IGE-Seniority-Index**](a-msds-habseniorityindex.md)                    | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-Host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)             | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Is-Domain-For**](a-msds-isdomainfor.md)                                | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-is-full-replica-for**](a-msds-isfullreplicafor.md)                     | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-is-partial-replica-for**](a-msds-ispartialreplicafor.md)               | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-local-Effective-Deletion-Time**](a-msds-localeffectivedeletiontime.md) | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-local-Effective-Recycle-Time**](a-msds-localeffectiverecycletime.md)   | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Members-for-Az-Role-BL**](a-msds-membersforazrolebl.md)                | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)         | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)       | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-NC-Type**](a-msds-nctype.md)                                           | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-OIDToGroup-Link-BL**](a-msds-oidtogrouplinkbl.md)                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Operations-for-Az-Role-BL**](a-msds-operationsforazrolebl.md)          | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Operations-for-Az-Task-BL**](a-msds-operationsforaztaskbl.md)          | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Phonetic-Company-Name**](a-msds-phoneticcompanyname.md)                | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-Phonetic-Department**](a-msds-phoneticdepartment.md)                   | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-Phonetic-Display-Name**](a-msds-phoneticdisplayname.md)                | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/> [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                |
| [**ms-DS-Phonetic-First-Name**](a-msds-phoneticfirstname.md)                    | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-Phonetic-Last-Name**](a-msds-phoneticlastname.md)                      | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                             | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-PSO-Applied**](a-msds-psoapplied.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)           | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Revealed-DSAs**](a-msds-revealeddsas.md)                               | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Revealed-List-BL**](a-msds-revealedlistbl.md)                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Source-Object-DN**](a-msds-sourceobjectdn.md)                          | Falsch     | **Kontakt**                                                                                                                            |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-Exch-Assistant-Name**](a-msexchassistantname.md)                          | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**ms-Exch-House-Identifier**](a-msexchhouseidentifier.md)                      | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-Exch-LabeledURI**](a-msexchlabeleduri.md)                                 | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Non-Security-Member-BL**](a-nonsecuritymemberbl.md)                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                         | Richtig      | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                     | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Objektkategorie**](a-objectcategory.md)                                      | Richtig      | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Object-Class**](a-objectclass.md)                                            | Richtig      | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Objekt-GUID**](a-objectguid.md)                                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Object-Version**](a-objectversion.md)                                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Organisationseinheitsname**](a-ou.md)                                         | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Organisationsname**](a-o.md)                                                 | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Sonstiges Postfach**](a-othermailbox.md)                                          | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Other-Name**](a-middlename.md)                                               | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Andere bekannte Objekte**](a-otherwellknownobjects.md)                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)        | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                           | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Personal-Title**](a-personaltitle.md)                                        | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-Fax-Other**](a-otherfacsimiletelephonenumber.md)                       | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-Home-Other**](a-otherhomephone.md)                                     | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-Home-Primary**](a-homephone.md)                                        | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-Ip-Other**](a-otheripphone.md)                                         | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-Ip-Primary**](a-ipphone.md)                                            | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-ISDN-Primary**](a-primaryinternationalisdnnumber.md)                   | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-Mobile-Other**](a-othermobile.md)                                      | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-Mobile-Primary**](a-mobile.md)                                         | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-Office-Other**](a-othertelephone.md)                                   | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-Pager-Other**](a-otherpager.md)                                        | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-Pager-Primary**](a-pager.md)                                           | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Physical-Delivery-Office-Name**](a-physicaldeliveryofficename.md)            | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Bild**](a-thumbnailphoto.md)                                              | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Mögliche Hindernisse**](a-possibleinferiors.md)                                | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Postanschrift**](a-postaladdress.md)                                        | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Postleitzahl**](a-postalcode.md)                                              | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Post-Office-Box**](a-postofficebox.md)                                       | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Preferred-Delivery-Method**](a-preferreddeliverymethod.md)                   | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                               | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Proxyadressen**](a-proxyaddresses.md)                                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Query-Policy-BL**](a-querypolicybl.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Rdn**](a-name.md)                                                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Registrierte Adresse**](a-registeredaddress.md)                                | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                             | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Berichte**](a-directreports.md)                                               | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Reps-From**](a-repsfrom.md)                                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Reps-To**](a-repsto.md)                                                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Revision**](a-revision.md)                                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                               | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**secretary**](a-secretary.md)                                                 | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Siehe auch**](a-seealso.md)                                                    | Falsch     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**Seriennummer**](a-serialnumber.md)                                          | Falsch     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**Server-Reference-BL**](a-serverreferencebl.md)                               | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Show-In-Address-Book**](a-showinaddressbook.md)                              | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Nur in erweiterter Ansicht anzeigen**](a-showinadvancedviewonly.md)                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Site-Object-BL**](a-siteobjectbl.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**State-or-Province-Name**](a-st.md)                                           | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Adresse der Straße**](a-street.md)                                               | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Sub-Refs**](a-subrefs.md)                                                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Nachname**](a-sn.md)                                                          | Falsch     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**Systemflags**](a-systemflags.md)                                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Telefonnummer**](a-telephonenumber.md)                                    | Falsch     | [**Person**](c-person.md)<br/> [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                             |
| [**Teletex-Terminal-Identifier**](a-teletexterminalidentifier.md)               | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telex-Number**](a-telexnumber.md)                                            | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telex-Primary**](a-primarytelexnumber.md)                                    | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Text-Country**](a-co.md)                                                     | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Textcodierte OR-Adresse**](a-textencodedoraddress.md)                        | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Titel**](a-title.md)                                                         | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**User-Cert**](a-usercert.md)                                                  | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Benutzerkommentar**](a-comment.md)                                                | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Benutzerkennwort**](a-userpassword.md)                                          | Falsch     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**User-SMIME-Certificate**](a-usersmimecertificate.md)                         | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**USN-Changed**](a-usnchanged.md)                                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**VON USN erstellt**](a-usncreated.md)                                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**USN-Intersite**](a-usnintersite.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**USN-Quelle**](a-usnsource.md)                                                | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Wbem-Path**](a-wbempath.md)                                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Bekannte Objekte**](a-wellknownobjects.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Wenn geändert**](a-whenchanged.md)                                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Wenn erstellt**](a-whencreated.md)                                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**WWW-Homepage**](a-wwwhomepage.md)                                           | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**WWW-Page-Other**](a-url.md)                                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**X121-Adresse**](a-x121address.md)                                            | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**X509-Cert**](a-usercertificate.md)                                           | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |



## <a name="windows-server-2008-r2-property-sets"></a>Windows Server 2008 R2-Eigenschaftensätze

Diese Klasse enthält die folgenden Eigenschaftensätze für Windows Server 2008 R2:



| Allgemeiner Name                                            |
|--------------------------------------------------------|
| [**Persönliche Informationen**](r-personal-information.md) |
| [**Webinformationen**](r-web-information.md)           |



## <a name="windows-server-2012"></a>Windows Server 2012

-   [Attribute](#windows-server-2012-attributes)
-   [Eigenschaftensätze](#windows-server-2012-property-sets)



| Eingabe | Wert |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Falsch                                                                                        |
| Object-Category             | 1                                                                                            |
| Default-Object-Category     | [**Person**](c-person.md)<br/>                                                        |
| Governs-Id                  | 1.2.840.113556.1.5.15                                                                        |
| Default-Hiding-Value        | 0                                                                                            |
| Rdn-Att-Id                  | [**Common-Name**](a-cn.md)<br/>                                                       |
| Unterklasse von                 | [**Unternehmensperson**](c-organizationalperson.md)<br/>                           |
| Mögliche Vorgesetzte          | [**Organisationseinheit "Domain-DNS"**](c-domaindns.md)[](c-organizationalunit.md)         |
| Zusätzlich           | [**E-Mail-Empfänger**](c-mailrecipient.md) (System)                                           |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                 |
| Standardsicherheitsdeskriptor | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;;; AU) |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2012-attributes"></a>Windows Server 2012 Attribute

Diese Klasse enthält die folgenden Attribute für Windows Server 2012:



| attribute                                                                                              | Obligatorisch. | Abgeleitet von                                                                                                                           |
|--------------------------------------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**Zusätzliche Informationen**](a-notes.md)                                                              | Falsch     | **Kontakt**                                                                                                                            |
| [**Adresse**](a-streetaddress.md)                                                                     | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Address-Home**](a-homepostaladdress.md)                                                            | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Admin-Description**](a-admindescription.md)                                                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Administratoranzeigename**](a-admindisplayname.md)                                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Attributes**](a-allowedattributes.md)                                                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Assistent**](a-assistant.md)                                                                       | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**attributeCertificateAttribute**](a-attributecertificateattribute.md)                               | Falsch     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Kanonischer Name**](a-canonicalname.md)                                                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Kommentar**](a-info.md)                                                                              | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Common-Name**](a-cn.md)                                                                            | Richtig      | **Kontaktperson** [](c-person.md)<br/> [**E-Mail-Empfänger**](c-mailrecipient.md)<br/> [**Nach oben**](c-top.md)<br/> |
| [**Unternehmen**](a-company.md)                                                                           | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Ländercode**](a-countrycode.md)                                                                  | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Country-Name**](a-c.md)                                                                            | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Create-Time-Stamp**](a-createtimestamp.md)                                                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Department**](a-department.md)                                                                     | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Beschreibung**](a-description.md)                                                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Destination-Indicator**](a-destinationindicator.md)                                                | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Anzeigename**](a-displayname.md)                                                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Display-Name-Printable**](a-displaynameprintable.md)                                               | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Division**](a-division.md)                                                                         | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**DSA-Signature**](a-dsasignature.md)                                                                | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**DS-Core-Propagierungsdaten**](a-dscorepropagationdata.md)                                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**E-Mail-Adressen**](a-mail.md)                                                                     | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Mitarbeiter-ID**](a-employeeid.md)                                                                    | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Extension-Name**](a-extensionname.md)                                                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Facsimile-Telephone-Number**](a-facsimiletelephonenumber.md)                                       | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Flaggen**](a-flags.md)                                                                               | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**From-Entry**](a-fromentry.md)                                                                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                                             | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Garbage Coll-Period**](a-garbagecollperiod.md)                                                     | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Generation-Qualifier**](a-generationqualifier.md)                                                  | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Given-Name**](a-givenname.md)                                                                      | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**houseIdentifier**](a-houseidentifier.md)                                                           | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Initialen**](a-initials.md)                                                                         | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Instanztyp**](a-instancetype.md)                                                                | Richtig      | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**International-ISDN-Number**](a-internationalisdnnumber.md)                                         | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Is-Deleted**](a-isdeleted.md)                                                                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Is-Member-of-DL**](a-memberof.md)                                                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                                                     | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Wird wiederverwendet**](a-isrecycled.md)                                                                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**labeledURI**](a-labeleduri.md)                                                                     | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Letztes bekanntes übergeordnetes Element**](a-lastknownparent.md)                                                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Legacy-Exchange-DN**](a-legacyexchangedn.md)                                                       | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Locality-Name**](a-l.md)                                                                           | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Logo**](a-thumbnaillogo.md)                                                                        | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Verwaltete Objekte**](a-managedobjects.md)                                                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Manager**](a-manager.md)                                                                           | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Mastered By**](a-masteredby.md)                                                                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**MHS-OR-Adresse**](a-mhsoraddress.md)                                                               | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Modify-Time-Stamp**](a-modifytimestamp.md)                                                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)                                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Allowed-To-Act-On-Behalf-of-Other-Identity**](a-msds-allowedtoactonbehalfofotheridentity.md) | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-Allowed-to-Delegate-To**](a-msds-allowedtodelegateto.md)                                     | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md)                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md)                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Claim-Shares-Possible-Values-With-BL**](a-msds-claimsharespossiblevalueswithbl.md)           | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Enabled-Feature-BL**](a-msds-enabledfeaturebl.md)                                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-GeoCoordinates-Altitude**](a-msds-geocoordinatesaltitude.md)                                 | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**ms-DS-GeoCoordinates-Latitude**](a-msds-geocoordinateslatitude.md)                                 | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**ms-DS-GeoCoordinates-Longitude**](a-msds-geocoordinateslongitude.md)                               | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**ms-DS-HEIT-Seniority-Index**](a-msds-habseniorityindex.md)                                          | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-Host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-is-Domain-for**](a-msds-isdomainfor.md)                                                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-is-full-replica-for**](a-msds-isfullreplicafor.md)                                           | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-is-partial-replica-for**](a-msds-ispartialreplicafor.md)                                     | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Is-Primary-Computer-for**](a-msds-isprimarycomputerfor.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                                                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                                                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-local-Effective-Deletion-Time**](a-msds-localeffectivedeletiontime.md)                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-local-Effective-Recycle-Time**](a-msds-localeffectiverecycletime.md)                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                                                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Members-For-Az-Role-BL**](a-msds-membersforazrolebl.md)                                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Members-of-Resource-Property-List-BL**](a-msds-membersofresourcepropertylistbl.md)           | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)                               | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)                             | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-NC-Type**](a-msds-nctype.md)                                                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                                                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-OIDToGroup-Link-BL**](a-msds-oidtogrouplinkbl.md)                                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Operations-for-Az-Role-BL**](a-msds-operationsforazrolebl.md)                                | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Operations-for-Az-Task-BL**](a-msds-operationsforaztaskbl.md)                                | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Phonetic-Company-Name**](a-msds-phoneticcompanyname.md)                                      | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-Phonetic-Department**](a-msds-phoneticdepartment.md)                                         | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-Phonetic-Display-Name**](a-msds-phoneticdisplayname.md)                                      | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/> [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                |
| [**ms-DS-Phonetic-First-Name**](a-msds-phoneticfirstname.md)                                          | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-Phonetic-Last-Name**](a-msds-phoneticlastname.md)                                            | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-PSO-Applied**](a-msds-psoapplied.md)                                                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Revealed-DSAs**](a-msds-revealeddsas.md)                                                     | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Revealed-List-BL**](a-msds-revealedlistbl.md)                                                | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Source-Object-DN**](a-msds-sourceobjectdn.md)                                                | Falsch     | **Kontakt**                                                                                                                            |
| [**ms-DS-Tasks-for-Az-Role-BL**](a-msds-tasksforazrolebl.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Tasks-for-Az-Task-BL**](a-msds-tasksforaztaskbl.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-TDO-Egress-BL**](a-msds-tdoegressbl.md)                                                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-TDO-Ingress-BL**](a-msds-tdoingressbl.md)                                                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Value-Type-Reference-BL**](a-msds-valuetypereferencebl.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**ms-Exch-Assistant-Name**](a-msexchassistantname.md)                                                | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**ms-Exch-House-Identifier**](a-msexchhouseidentifier.md)                                            | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-Exch-LabeledURI**](a-msexchlabeleduri.md)                                                       | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                                             | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                                               | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Non-Security-Member-BL**](a-nonsecuritymemberbl.md)                                                | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                                               | Richtig      | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                                           | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Objektkategorie**](a-objectcategory.md)                                                            | Richtig      | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Objektklasse**](a-objectclass.md)                                                                  | Richtig      | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Objekt-GUID**](a-objectguid.md)                                                                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Objektversion**](a-objectversion.md)                                                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Name der Organisationseinheit**](a-ou.md)                                                               | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Organisationsname**](a-o.md)                                                                       | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Sonstiges Postfach**](a-othermailbox.md)                                                                | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Anderer Name**](a-middlename.md)                                                                     | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Andere bekannte Objekte**](a-otherwellknownobjects.md)                                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Teilattributlöschungsliste**](a-partialattributedeletionlist.md)                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Teilattributsatz**](a-partialattributeset.md)                                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Personal-Title**](a-personaltitle.md)                                                              | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-Fax-Other**](a-otherfacsimiletelephonenumber.md)                                             | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-Home-Other**](a-otherhomephone.md)                                                           | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-Home-Primary**](a-homephone.md)                                                              | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-Ip-Other**](a-otheripphone.md)                                                               | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-Ip-Primary**](a-ipphone.md)                                                                  | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-ISDN-Primary**](a-primaryinternationalisdnnumber.md)                                         | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-Mobile-Other**](a-othermobile.md)                                                            | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-Mobile-Primary**](a-mobile.md)                                                               | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-Office-Other**](a-othertelephone.md)                                                         | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-Pager-Other**](a-otherpager.md)                                                              | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefon-Pager-Primary**](a-pager.md)                                                                 | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Physical-Delivery-Office-Name**](a-physicaldeliveryofficename.md)                                  | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Bild**](a-thumbnailphoto.md)                                                                    | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Mögliche Hindernisse**](a-possibleinferiors.md)                                                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Postanschrift**](a-postaladdress.md)                                                              | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Postleitzahl**](a-postalcode.md)                                                                    | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Post-Office-Box**](a-postofficebox.md)                                                             | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Preferred-Delivery-Method**](a-preferreddeliverymethod.md)                                         | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                                                     | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Proxyadressen**](a-proxyaddresses.md)                                                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Query-Policy-BL**](a-querypolicybl.md)                                                             | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Rdn**](a-name.md)                                                                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Registrierte Adresse**](a-registeredaddress.md)                                                      | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Berichte**](a-directreports.md)                                                                     | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Reps-From**](a-repsfrom.md)                                                                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Reps-To**](a-repsto.md)                                                                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Revision**](a-revision.md)                                                                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                                                     | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**secretary**](a-secretary.md)                                                                       | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Siehe auch**](a-seealso.md)                                                                          | Falsch     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**Seriennummer**](a-serialnumber.md)                                                                | Falsch     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**Server-Reference-BL**](a-serverreferencebl.md)                                                     | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Show-In-Address-Book**](a-showinaddressbook.md)                                                    | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Site-Object-BL**](a-siteobjectbl.md)                                                               | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**State-Or-Province-Name**](a-st.md)                                                                 | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Street-Address**](a-street.md)                                                                     | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                                             | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Sub-Refs**](a-subrefs.md)                                                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Nachname**](a-sn.md)                                                                                | Falsch     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**Systemflags**](a-systemflags.md)                                                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Telefonnummer**](a-telephonenumber.md)                                                          | Falsch     | [**Person**](c-person.md)<br/> [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                             |
| [**Teletex-Terminal-Identifier**](a-teletexterminalidentifier.md)                                     | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telex-Number**](a-telexnumber.md)                                                                  | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Telex-Primary**](a-primarytelexnumber.md)                                                          | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Text-Country**](a-co.md)                                                                           | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Textcodierte OR-Adresse**](a-textencodedoraddress.md)                                              | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Titel**](a-title.md)                                                                               | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**User-Cert**](a-usercert.md)                                                                        | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**Benutzerkommentar**](a-comment.md)                                                                      | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**Benutzerkennwort**](a-userpassword.md)                                                                | Falsch     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**User-SMIME-Certificate**](a-usersmimecertificate.md)                                               | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |
| [**USN-Changed**](a-usnchanged.md)                                                                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**VON USN erstellt**](a-usncreated.md)                                                                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**USN-DSA-last-obj-removed**](a-usndsalastobjremoved.md)                                             | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**USN-Intersite**](a-usnintersite.md)                                                                | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**USN-Quelle**](a-usnsource.md)                                                                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Wbem-Pfad**](a-wbempath.md)                                                                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Bekannte Objekte**](a-wellknownobjects.md)                                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Bei Änderung**](a-whenchanged.md)                                                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**Bei der Erstellung**](a-whencreated.md)                                                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**WWW-Startseite**](a-wwwhomepage.md)                                                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**WWW-Page-Other**](a-url.md)                                                                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                        |
| [**X121-Address**](a-x121address.md)                                                                  | Falsch     | [**Unternehmensperson**](c-organizationalperson.md)<br/>                                                                     |
| [**X509-Cert**](a-usercertificate.md)                                                                 | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                                   |



## <a name="windows-server-2012-property-sets"></a>Windows Server 2012 Eigenschaftensätze

Diese Klasse enthält die folgenden Eigenschaftensätze für Windows Server 2012:



| Allgemeiner Name                                            |
|--------------------------------------------------------|
| [**Persönliche Informationen**](r-personal-information.md) |
| [**Webinformationen**](r-web-information.md)           |



 

 





