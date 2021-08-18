---
title: Group-Klasse
description: Speichert eine Liste von Benutzernamen. Wird verwendet, um Sicherheitsprinzipale auf Ressourcen anzuwenden.
ms.assetid: e8ce5c43-d0fb-4c67-a6ef-7094fb7e7669
ms.tgt_platform: multiple
keywords:
- AD-Schema der Gruppenklasse
- Group Class AD Schema
topic_type:
- apiref
api_name:
- Group
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eae33b53eff8305fee4698c5aed2bb072f3fa5b90a5922d0099e40e90f9b3fe4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119021908"
---
# <a name="group-class"></a>Group-Klasse

Speichert eine Liste von Benutzernamen. Wird verwendet, um Sicherheitsprinzipale auf Ressourcen anzuwenden.



| Eingabe | Wert |
|-------------------|------------------------------------------------|
| CN                | Group                                          |
| Ldap-Anzeigename | group                                          |
| Aktualisieren von Berechtigungen  | Dieser Wert wird vom Domänenadministrator festgelegt. |
| Updatehäufigkeit  | \-                                             |
| Schema-ID-GUID    | bf967a9c-0de6-11d0-a285-00aa003049e2           |



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
-   [Erweiterte Rechte](#windows-2000-server-extended-rights)
-   [Überprüfte Schreibvorgänge](#windows-2000-server-validated-writes)
-   [Eigenschaftensätze](#windows-2000-server-property-sets)



| Eingabe | Wert |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falsch                                                                                                                                                                                               |
| Object-Category             | 1                                                                                                                                                                                                   |
| Default-Object-Category     | \-                                                                                                                                                                                                  |
| Governs-Id                  | 1.2.840.113556.1.5.8                                                                                                                                                                                |
| Default-Hiding-Value        | 0                                                                                                                                                                                                   |
| Rdn-Att-Id                  | [**Common-Name**](a-cn.md)<br/>                                                                                                                                                              |
| Unterklasse von                 | [**Nach oben**](c-top.md)<br/>                                                                                                                                                                     |
| Mögliche Vorgesetzte          | [**Domain-DNS**](c-domaindns.md)[**Organizational-Unit**](c-organizationalunit.md)[**Builtin-Domain**](c-builtindomain.md)[**Container**](c-container.md)                                       |
| Zusätzlich           | [**Sicherheitsprinzipal**](c-securityprincipal.md) (System)[**E-Mail-Empfänger**](c-mailrecipient.md) (System)                                                                                        |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                                                                                                                        |
| Standardsicherheitsdeskriptor | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;;; AU)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; AO)(A;; RPLCLORC;;; PS)(OA;; CR;ab721a55-1e2f-11d0-9819-00aa0040529b;; AU) |
| System-Flags                | 0x00000010                                                                                                                                                                                          |



## <a name="windows-2000-server-attributes"></a>Windows 2000-Serverattribute

Diese Klasse enthält die folgenden Attribute für Windows 2000-Server:



| attribute                                                                    | Obligatorisch. | Abgeleitet von                                                                                 |
|------------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------|
| [**Account-Name-History**](a-accountnamehistory.md)                         | Falsch     | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/>                                 |
| [**Admin-Count**](a-admincount.md)                                          | Falsch     | **Gruppe**                                                                                    |
| [**Admin-Description**](a-admindescription.md)                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Administratoranzeigename**](a-admindisplayname.md)                             | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Allowed-Attributes**](a-allowedattributes.md)                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)         | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Alt-Sicherheitsidentitäten**](a-altsecurityidentities.md)                   | Falsch     | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/>                                 |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Kanonischer Name**](a-canonicalname.md)                                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Kommentar**](a-info.md)                                                    | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                         |
| [**Common-Name**](a-cn.md)                                                  | Richtig      | [**Nach oben**](c-top.md)<br/> [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>         |
| [**Control-Access-Rights**](a-controlaccessrights.md)                       | Falsch     | **Gruppe**                                                                                    |
| [**Erstellen eines Zeitstempels**](a-createtimestamp.md)                               | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Beschreibung**](a-description.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Desktopprofil**](a-desktopprofile.md)                                  | Falsch     | **Gruppe**                                                                                    |
| [**Anzeigename**](a-displayname.md)                                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Anzeigename– druckbar**](a-displaynameprintable.md)                     | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**DSA-Signature**](a-dsasignature.md)                                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**DS-Core-Propagierungsdaten**](a-dscorepropagationdata.md)                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**E-Mail-Adressen**](a-mail.md)                                           | Falsch     | **Gruppe**                                                                                    |
| [**Erweiterungsname**](a-extensionname.md)                                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Flaggen**](a-flags.md)                                                     | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**From-Entry**](a-fromentry.md)                                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)                | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Garbage-Coll-Period**](a-garbagecollperiod.md)                           | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                         |
| [**Gruppenattribute**](a-groupattributes.md)                                | Falsch     | **Gruppe**                                                                                    |
| [**Gruppenmitgliedschafts-SAM**](a-groupmembershipsam.md)                         | Falsch     | **Gruppe**                                                                                    |
| [**Gruppentyp**](a-grouptype.md)                                            | Richtig      | **Gruppe**                                                                                    |
| [**Instanztyp**](a-instancetype.md)                                      | Richtig      | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Is-Deleted**](a-isdeleted.md)                                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Is-Member-of-DL**](a-memberof.md)                                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                           | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Last-Known-Parent**](a-lastknownparent.md)                               | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Legacy-Exchange-DN**](a-legacyexchangedn.md)                             | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                         |
| [**Verwaltet von**](a-managedby.md)                                            | Falsch     | **Gruppe**                                                                                    |
| [**Verwaltete Objekte**](a-managedobjects.md)                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Mastered-By**](a-masteredby.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Member**](a-member.md)                                                   | Falsch     | **Gruppe**                                                                                    |
| [**Modify-Time-Stamp**](a-modifytimestamp.md)                               | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)       | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                     | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Nicht-Sicherheitsmitglied**](a-nonsecuritymember.md)                           | Falsch     | **Gruppe**                                                                                    |
| [**Non-Security-Member-BL**](a-nonsecuritymemberbl.md)                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**NT-Group-Members**](a-ntgroupmembers.md)                                 | Falsch     | **Gruppe**                                                                                    |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                     | Richtig      | [**Nach oben**](c-top.md)<br/> [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/> |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Objektkategorie**](a-objectcategory.md)                                  | Richtig      | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Objektklasse**](a-objectclass.md)                                        | Richtig      | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Objekt-GUID**](a-objectguid.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Object-Sid**](a-objectsid.md)                                            | Richtig      | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/>                                 |
| [**Objektversion**](a-objectversion.md)                                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Operatoranzahl**](a-operatorcount.md)                                    | Falsch     | **Gruppe**                                                                                    |
| [**Andere bekannte Objekte**](a-otherwellknownobjects.md)                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Teilattributlöschungsliste**](a-partialattributedeletionlist.md)    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Teilattributsatz**](a-partialattributeset.md)                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Mögliche Hindernisse**](a-possibleinferiors.md)                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Primäres Gruppentoken**](a-primarygrouptoken.md)                           | Falsch     | **Gruppe**                                                                                    |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                           | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Proxyadressen**](a-proxyaddresses.md)                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Query-Policy-BL**](a-querypolicybl.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Rdn**](a-name.md)                                                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Berichte**](a-directreports.md)                                           | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Reps-From**](a-repsfrom.md)                                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Reps-To**](a-repsto.md)                                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Revision**](a-revision.md)                                               | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**los**](a-rid.md)                                                         | Falsch     | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/>                                 |
| [**SAM-Account-Name**](a-samaccountname.md)                                 | Richtig      | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/>                                 |
| [**SAM-Account-Type**](a-samaccounttype.md)                                 | Falsch     | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/>                                 |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                           | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Sicherheitsbezeichner**](a-securityidentifier.md)                          | Falsch     | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/>                                 |
| [**Server-Reference-BL**](a-serverreferencebl.md)                           | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Show-In-Address-Book**](a-showinaddressbook.md)                          | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                         |
| [**Nur in erweiterter Ansicht anzeigen**](a-showinadvancedviewonly.md)               | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**SID-Verlauf**](a-sidhistory.md)                                          | Falsch     | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/>                                 |
| [**Site-Object-BL**](a-siteobjectbl.md)                                     | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Sub-Refs**](a-subrefs.md)                                                | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                             | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Supplemental-Credentials**](a-supplementalcredentials.md)                | Falsch     | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/>                                 |
| [**Systemflags**](a-systemflags.md)                                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Telefonnummer**](a-telephonenumber.md)                                | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                         |
| [**Textcodierte OR-Adresse**](a-textencodedoraddress.md)                    | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                         |
| [**Tokengruppen**](a-tokengroups.md)                                        | Falsch     | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/>                                 |
| [**Tokengruppen– global und universell**](a-tokengroupsglobalanduniversal.md) | Falsch     | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/>                                 |
| [**Tokengruppen– keine GC-akzeptabel**](a-tokengroupsnogcacceptable.md)         | Falsch     | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/>                                 |
| [**User-Cert**](a-usercert.md)                                              | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                         |
| [**User-SMIME-Certificate**](a-usersmimecertificate.md)                     | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                         |
| [**USN geändert**](a-usnchanged.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**USN-erstellt**](a-usncreated.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**USN-DSA-last-obj-removed**](a-usndsalastobjremoved.md)                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**USN-Intersite**](a-usnintersite.md)                                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**USN-Quelle**](a-usnsource.md)                                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Wbem-Pfad**](a-wbempath.md)                                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Bekannte Objekte**](a-wellknownobjects.md)                             | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Bei Änderung**](a-whenchanged.md)                                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Bei der Erstellung**](a-whencreated.md)                                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**WWW-Startseite**](a-wwwhomepage.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**WWW-Page-Other**](a-url.md)                                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**X509-Cert**](a-usercertificate.md)                                       | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                         |



## <a name="windows-2000-server-extended-rights"></a>erweiterte Rechte für Windows 2000-Server

Diese Klasse enthält die folgenden erweiterten Rechte für Windows 2000 Server:



| Allgemeiner Name                  |
|------------------------------|
| [**Senden an**](r-send-to.md) |



## <a name="windows-2000-server-validated-writes"></a>Windows 2000 servervalidierte Schreibvorgänge

Diese Klasse enthält die folgenden überprüften Schreibvorgänge für Windows 2000 Server:



| Allgemeiner Name                                  |
|----------------------------------------------|
| [**Selbstmitgliedschaft**](r-self-membership.md) |



## <a name="windows-2000-server-property-sets"></a>Windows 2000-Servereigenschaftensätze

Diese Klasse enthält die folgenden Eigenschaftensätze für Windows 2000 Server:



| Allgemeiner Name                                      |
|--------------------------------------------------|
| [**E-Mail-Informationen**](r-email-information.md) |



## <a name="windows-server-2003"></a>Windows Server 2003

-   [Attribute](#windows-server-2003-attributes)
-   [Erweiterte Rechte](#windows-server-2003-extended-rights)
-   [Überprüfte Schreibvorgänge](#windows-server-2003-validated-writes)
-   [Eigenschaftensätze](#windows-server-2003-property-sets)



| Eingabe | Wert |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falsch                                                                                                                                                                                                                                                                                                            |
| Object-Category             | 1                                                                                                                                                                                                                                                                                                                |
| Default-Object-Category     | \-                                                                                                                                                                                                                                                                                                               |
| Governs-Id                  | 1.2.840.113556.1.5.8                                                                                                                                                                                                                                                                                             |
| Default-Hiding-Value        | 0                                                                                                                                                                                                                                                                                                                |
| Rdn-Att-Id                  | [**Allgemeiner Name**](a-cn.md)<br/>                                                                                                                                                                                                                                                                           |
| Unterklasse von                 | [**Nach oben**](c-top.md)<br/>                                                                                                                                                                                                                                                                                  |
| Mögliche Übergeordnete          | [**Domänen-DNS**](c-domaindns.md)[**Organizational-Unit**](c-organizationalunit.md)[**Builtin-Domain**](c-builtindomain.md)[**Container**](c-container.md)[**ms-DS-Az-Admin-Manager**](c-msds-azadminmanager.md)[**ms-DS-Az-Application**](c-msds-azapplication.md)[**ms-DS-Az-Scope**](c-msds-azscope.md) |
| Zusätzlich           | [**Sicherheitsprinzipal**](c-securityprincipal.md) (System)[**E-Mail-Empfänger**](c-mailrecipient.md) (System)                                                                                                                                                                                                     |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                     |
| Standardsicherheitsdeskriptor | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;;; AU)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; AO)(A;; RPLCLORC;;; PS)(OA;; CR;ab721a55-1e2f-11d0-9819-00aa0040529b;; AU)(OA;; RP;46a9b11d-60ae-405a-b7e8-ff8a58d456d2;; S-1-5-32-560)                                                   |
| System-Flags                | 0x00000010                                                                                                                                                                                                                                                                                                       |



## <a name="windows-server-2003-attributes"></a>Windows Server 2003-Attribute

Diese Klasse enthält die folgenden Attribute für Windows Server 2003:



| attribute                                                                    | Obligatorisch. | Abgeleitet von                                                                                 |
|------------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------|
| [**Kontoname-Verlauf**](a-accountnamehistory.md)                         | Falsch     | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/>                                 |
| [**Admin-Count**](a-admincount.md)                                          | Falsch     | **Gruppe**                                                                                    |
| [**Administratorbeschreibung**](a-admindescription.md)                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Admin-Display-Name**](a-admindisplayname.md)                             | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Allowed-Attributes**](a-allowedattributes.md)                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)         | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**ALT-SICHERHEITSIDENTITÄTEN**](a-altsecurityidentities.md)                   | Falsch     | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/>                                 |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Kanonischer Name**](a-canonicalname.md)                                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Kommentar**](a-info.md)                                                    | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                         |
| [**Allgemeiner Name**](a-cn.md)                                                  | Richtig      | [**Nach oben**](c-top.md)<br/> [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>         |
| [**Control-Access-Rights**](a-controlaccessrights.md)                       | Falsch     | **Gruppe**                                                                                    |
| [**Erstellen eines Zeitstempels**](a-createtimestamp.md)                               | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Beschreibung**](a-description.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Desktopprofil**](a-desktopprofile.md)                                  | Falsch     | **Gruppe**                                                                                    |
| [**Anzeigename**](a-displayname.md)                                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Anzeigename– druckbar**](a-displaynameprintable.md)                     | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**DSA-Signature**](a-dsasignature.md)                                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**DS-Core-Propagierungsdaten**](a-dscorepropagationdata.md)                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**E-Mail-Adressen**](a-mail.md)                                           | Falsch     | **Gruppe**                                                                                    |
| [**Erweiterungsname**](a-extensionname.md)                                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Flaggen**](a-flags.md)                                                     | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**From-Entry**](a-fromentry.md)                                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)                | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Garbage Coll-Period**](a-garbagecollperiod.md)                           | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                         |
| [**Gruppenattribute**](a-groupattributes.md)                                | Falsch     | **Gruppe**                                                                                    |
| [**Group-Membership-SAM**](a-groupmembershipsam.md)                         | Falsch     | **Gruppe**                                                                                    |
| [**Gruppentyp**](a-grouptype.md)                                            | Richtig      | **Gruppe**                                                                                    |
| [**Instanztyp**](a-instancetype.md)                                      | Richtig      | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Is-Deleted**](a-isdeleted.md)                                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Is-Member-of-DL**](a-memberof.md)                                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                           | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**labeledURI**](a-labeleduri.md)                                           | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                         |
| [**Letztes bekanntes übergeordnetes Element**](a-lastknownparent.md)                               | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Legacy-Exchange-DN**](a-legacyexchangedn.md)                             | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                         |
| [**Verwaltet von**](a-managedby.md)                                            | Falsch     | **Gruppe**                                                                                    |
| [**Verwaltete Objekte**](a-managedobjects.md)                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Mastered By**](a-masteredby.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Member**](a-member.md)                                                   | Falsch     | **Gruppe**                                                                                    |
| [**Modify-Time-Stamp**](a-modifytimestamp.md)                               | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md)  | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**ms-DS-Az-LDAP-Query**](a-msds-azldapquery.md)                            | Falsch     | **Gruppe**                                                                                    |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)       | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**ms-DS-KeyVersionNumber**](a-msds-keyversionnumber.md)                    | Falsch     | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/>                                 |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                               | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**ms-DS-Members-For-Az-Role-BL**](a-msds-membersforazrolebl.md)            | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)     | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)   | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**ms-DS-Non-Members**](a-msds-nonmembers.md)                               | Falsch     | **Gruppe**                                                                                    |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**ms-DS-Operations-for-Az-Role-BL**](a-msds-operationsforazrolebl.md)      | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**ms-DS-Operations-for-Az-Task-BL**](a-msds-operationsforaztaskbl.md)      | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)       | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)               | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**ms-DS-Tasks-for-Az-Role-BL**](a-msds-tasksforazrolebl.md)                | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**ms-DS-Tasks-for-Az-Task-BL**](a-msds-tasksforaztaskbl.md)                | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**ms-Exch-Assistant-Name**](a-msexchassistantname.md)                      | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                         |
| [**ms-Exch-LabeledURI**](a-msexchlabeleduri.md)                             | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                         |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                     | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Nicht-Sicherheitsmitglied**](a-nonsecuritymember.md)                           | Falsch     | **Gruppe**                                                                                    |
| [**Non-Security-Member-BL**](a-nonsecuritymemberbl.md)                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**NT-Group-Members**](a-ntgroupmembers.md)                                 | Falsch     | **Gruppe**                                                                                    |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                     | Richtig      | [**Nach oben**](c-top.md)<br/> [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/> |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Objektkategorie**](a-objectcategory.md)                                  | Richtig      | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Objektklasse**](a-objectclass.md)                                        | Richtig      | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Objekt-GUID**](a-objectguid.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Object-Sid**](a-objectsid.md)                                            | Richtig      | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/>                                 |
| [**Objektversion**](a-objectversion.md)                                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Operatoranzahl**](a-operatorcount.md)                                    | Falsch     | **Gruppe**                                                                                    |
| [**Andere bekannte Objekte**](a-otherwellknownobjects.md)                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Teilattributlöschungsliste**](a-partialattributedeletionlist.md)    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Teilattributsatz**](a-partialattributeset.md)                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Mögliche Hindernisse**](a-possibleinferiors.md)                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Primäres Gruppentoken**](a-primarygrouptoken.md)                           | Falsch     | **Gruppe**                                                                                    |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                           | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Proxyadressen**](a-proxyaddresses.md)                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Query-Policy-BL**](a-querypolicybl.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Rdn**](a-name.md)                                                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Berichte**](a-directreports.md)                                           | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Reps-From**](a-repsfrom.md)                                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Reps-To**](a-repsto.md)                                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Revision**](a-revision.md)                                               | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**los**](a-rid.md)                                                         | Falsch     | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/>                                 |
| [**SAM-Account-Name**](a-samaccountname.md)                                 | Richtig      | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/>                                 |
| [**SAM-Account-Type**](a-samaccounttype.md)                                 | Falsch     | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/>                                 |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                           | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**secretary**](a-secretary.md)                                             | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                         |
| [**Sicherheitsbezeichner**](a-securityidentifier.md)                          | Falsch     | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/>                                 |
| [**Server-Reference-BL**](a-serverreferencebl.md)                           | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Show-In-Address-Book**](a-showinaddressbook.md)                          | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                         |
| [**Nur in erweiterter Ansicht anzeigen**](a-showinadvancedviewonly.md)               | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**SID-Verlauf**](a-sidhistory.md)                                          | Falsch     | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/>                                 |
| [**Site-Object-BL**](a-siteobjectbl.md)                                     | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Sub-Refs**](a-subrefs.md)                                                | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                             | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Supplemental-Credentials**](a-supplementalcredentials.md)                | Falsch     | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/>                                 |
| [**Systemflags**](a-systemflags.md)                                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Telefonnummer**](a-telephonenumber.md)                                | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                         |
| [**Textcodierte OR-Adresse**](a-textencodedoraddress.md)                    | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                         |
| [**Tokengruppen**](a-tokengroups.md)                                        | Falsch     | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/>                                 |
| [**Tokengruppen– global und universell**](a-tokengroupsglobalanduniversal.md) | Falsch     | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/>                                 |
| [**Tokengruppen– keine GC-akzeptabel**](a-tokengroupsnogcacceptable.md)         | Falsch     | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/>                                 |
| [**User-Cert**](a-usercert.md)                                              | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                         |
| [**User-SMIME-Certificate**](a-usersmimecertificate.md)                     | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                         |
| [**USN geändert**](a-usnchanged.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**USN-erstellt**](a-usncreated.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**USN-DSA-last-obj-removed**](a-usndsalastobjremoved.md)                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**USN-Intersite**](a-usnintersite.md)                                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**USN-Quelle**](a-usnsource.md)                                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Wbem-Path**](a-wbempath.md)                                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Bekannte Objekte**](a-wellknownobjects.md)                             | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Wenn geändert**](a-whenchanged.md)                                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Wenn erstellt**](a-whencreated.md)                                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**WWW-Homepage**](a-wwwhomepage.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**WWW-Page-Other**](a-url.md)                                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**X509-Cert**](a-usercertificate.md)                                       | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                         |



## <a name="windows-server-2003-extended-rights"></a>Windows Erweiterte Server 2003-Rechte

Diese Klasse enthält die folgenden erweiterten Rechte für Windows Server 2003:



| Allgemeiner Name                  |
|------------------------------|
| [**Senden an**](r-send-to.md) |



## <a name="windows-server-2003-validated-writes"></a>Windows Von Server 2003 überprüfte Schreibvorgänge

Diese Klasse enthält die folgenden überprüften Schreibvorgänge für Windows Server 2003:



| Allgemeiner Name                                  |
|----------------------------------------------|
| [**Selbstmitgliedschaft**](r-self-membership.md) |



## <a name="windows-server-2003-property-sets"></a>Windows Server 2003-Eigenschaftensätze

Diese Klasse enthält die folgenden Eigenschaftensätze für Windows Server 2003:



| Allgemeiner Name                                      |
|--------------------------------------------------|
| [**E-Mail-Informationen**](r-email-information.md) |



## <a name="adam"></a>Adam

-   [Attribute](#adam-attributes)
-   [Überprüfte Schreibvorgänge](#adam-validated-writes)
-   [Eigenschaftensätze](#adam-property-sets)



| Eingabe | Wert |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falsch                                                                                                                |
| Object-Category             | 1                                                                                                                    |
| Default-Object-Category     | \-                                                                                                                   |
| Governs-Id                  | 1.2.840.113556.1.5.8                                                                                                 |
| Default-Hiding-Value        | 0                                                                                                                    |
| Rdn-Att-Id                  | [**Common-Name**](a-cn.md)<br/>                                                                               |
| Unterklasse von                 | [**Nach oben**](c-top.md)<br/>                                                                                      |
| Mögliche Vorgesetzte          | [**Container für Domänen-DNS-Organisationseinheit**](c-domaindns.md)[](c-organizationalunit.md)[](c-container.md) |
| Zusätzlich           | [**Sicherheitsprinzipal**](c-securityprincipal.md) (System)                                                           |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                                         |
| Standardsicherheitsdeskriptor | D:S:                                                                                                                 |
| System-Flags                | 0x00000010                                                                                                           |



## <a name="adam-attributes"></a>ADAM-Attribute

Diese Klasse enthält die folgenden Attribute für ADAM:



| attribute                                                                   | Obligatorisch. | Abgeleitet von                                                                                 |
|-----------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------|
| [**Admin-Description**](a-admindescription.md)                             | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Administratoranzeigename**](a-admindisplayname.md)                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Allowed-Attributes**](a-allowedattributes.md)                           | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)        | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)   | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)               | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Kanonischer Name**](a-canonicalname.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Allgemeiner Name**](a-cn.md)                                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Erstellen eines Zeitstempels**](a-createtimestamp.md)                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Beschreibung**](a-description.md)                                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Desktopprofil**](a-desktopprofile.md)                                 | Falsch     | **Gruppe**                                                                                    |
| [**Anzeigename**](a-displayname.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**DSA-Signature**](a-dsasignature.md)                                     | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**DS-Core-Propagierungsdaten**](a-dscorepropagationdata.md)                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**From-Entry**](a-fromentry.md)                                           | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Gruppentyp**](a-grouptype.md)                                           | Richtig      | **Gruppe**                                                                                    |
| [**Instanztyp**](a-instancetype.md)                                     | Richtig      | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)               | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Is-Deleted**](a-isdeleted.md)                                           | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Is-Member-of-DL**](a-memberof.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Last-Known-Parent**](a-lastknownparent.md)                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Verwaltet von**](a-managedby.md)                                           | Falsch     | **Gruppe**                                                                                    |
| [**Verwaltete Objekte**](a-managedobjects.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Mastered-By**](a-masteredby.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Member**](a-member.md)                                                  | Falsch     | **Gruppe**                                                                                    |
| [**Modify-Time-Stamp**](a-modifytimestamp.md)                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md) | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)      | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**ms-DS-Disable-For-Instances-BL**](a-msds-disableforinstancesbl.md)      | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)  | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)      | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)              | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**ms-DS-Service-Account-BL**](a-msds-serviceaccountbl.md)                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                    | Richtig      | [**Nach oben**](c-top.md)<br/> [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/> |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Objektkategorie**](a-objectcategory.md)                                 | Richtig      | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Object-Class**](a-objectclass.md)                                       | Richtig      | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Objekt-GUID**](a-objectguid.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Object-Sid**](a-objectsid.md)                                           | Richtig      | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/>                                 |
| [**Object-Version**](a-objectversion.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Andere bekannte Objekte**](a-otherwellknownobjects.md)                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)   | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Mögliche 100000000000**](a-possibleinferiors.md)                           | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Primary-Group-Token**](a-primarygrouptoken.md)                          | Falsch     | **Gruppe**                                                                                    |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Proxyadressen**](a-proxyaddresses.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Query-Policy-BL**](a-querypolicybl.md)                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Rdn**](a-name.md)                                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Reps-From**](a-repsfrom.md)                                             | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Reps-To**](a-repsto.md)                                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Revision**](a-revision.md)                                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Server-Reference-BL**](a-serverreferencebl.md)                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)              | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Sub-Refs**](a-subrefs.md)                                               | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Zusätzliche Anmeldeinformationen**](a-supplementalcredentials.md)               | Falsch     | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/>                                 |
| [**Systemflags**](a-systemflags.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Tokengruppen**](a-tokengroups.md)                                       | Falsch     | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/>                                 |
| [**USN-Changed**](a-usnchanged.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**VON USN erstellt**](a-usncreated.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**USN-Intersite**](a-usnintersite.md)                                     | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**USN-Quelle**](a-usnsource.md)                                           | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Wbem-Path**](a-wbempath.md)                                             | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Bekannte Objekte**](a-wellknownobjects.md)                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Wenn geändert**](a-whenchanged.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Wenn erstellt**](a-whencreated.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**WWW-Homepage**](a-wwwhomepage.md)                                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**WWW-Page-Other**](a-url.md)                                             | Falsch     | [**Nach oben**](c-top.md)<br/>                                                              |



## <a name="adam-validated-writes"></a>ADAM-überprüfte Schreibvorgänge

Diese Klasse enthält die folgenden überprüften Schreibvorgänge für ADAM:



| Allgemeiner Name                                  |
|----------------------------------------------|
| [**Selbstmitgliedschaft**](r-self-membership.md) |



## <a name="adam-property-sets"></a>ADAM-Eigenschaftensätze

Diese Klasse enthält die folgenden Eigenschaftensätze für ADAM:



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
| System-Only                 | Falsch                                                                                                                                                                                                                                                                                                            |
| Object-Category             | 1                                                                                                                                                                                                                                                                                                                |
| Default-Object-Category     | \-                                                                                                                                                                                                                                                                                                               |
| Governs-Id                  | 1.2.840.113556.1.5.8                                                                                                                                                                                                                                                                                             |
| Default-Hiding-Value        | 0                                                                                                                                                                                                                                                                                                                |
| Rdn-Att-Id                  | [**Common-Name**](a-cn.md)<br/>                                                                                                                                                                                                                                                                           |
| Unterklasse von                 | [**Nach oben**](c-top.md)<br/>                                                                                                                                                                                                                                                                                  |
| Mögliche Vorgesetzte          | [**Domain-DNS**](c-domaindns.md)[**Organizational-Unit**](c-organizationalunit.md)[**Builtin-Domain Container**](c-builtindomain.md)[](c-container.md)[**ms-DS-Az-Admin-Manager**](c-msds-azadminmanager.md)[**ms-DS-Az-Application**](c-msds-azapplication.md)[**ms-DS-Az-Scope**](c-msds-azscope.md) |
| Zusätzlich           | [**posixGroup**](c-posixgroup.md)[**Security-Principal**](c-securityprincipal.md) (System)[**Mail-Recipient**](c-mailrecipient.md) (System)                                                                                                                                                                   |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                     |
| Standardsicherheitsdeskriptor | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;;; AU)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; AO)(A;; RPLCLORC;;; PS)(OA;; CR;ab721a55-1e2f-11d0-9819-00aa0040529b;; AU)(OA;; RP;46a9b11d-60ae-405a-b7e8-ff8a58d456d2;; S-1-5-32-560)                                                   |
| System-Flags                | 0x00000010                                                                                                                                                                                                                                                                                                       |



## <a name="windows-server-2003-r2-attributes"></a>Windows Server 2003 R2-Attribute

Diese Klasse enthält die folgenden Attribute für Windows Server 2003 R2:



| attribute                                                                    | Obligatorisch. | Abgeleitet von                                                                                                                       |
|------------------------------------------------------------------------------|-----------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Account-Name-History**](a-accountnamehistory.md)                         | Falsch     | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**Admin-Count**](a-admincount.md)                                          | Falsch     | **Gruppe**                                                                                                                          |
| [**Admin-Description**](a-admindescription.md)                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Administratoranzeigename**](a-admindisplayname.md)                             | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Allowed-Attributes**](a-allowedattributes.md)                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)         | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Alt-Sicherheitsidentitäten**](a-altsecurityidentities.md)                   | Falsch     | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Kanonischer Name**](a-canonicalname.md)                                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Kommentar**](a-info.md)                                                    | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**Common-Name**](a-cn.md)                                                  | Richtig      | [**Nach oben**](c-top.md)<br/> [**posixGroup**](c-posixgroup.md)<br/> [**E-Mail-Empfänger**](c-mailrecipient.md)<br/> |
| [**Control-Access-Rights**](a-controlaccessrights.md)                       | Falsch     | **Gruppe**                                                                                                                          |
| [**Create-Time-Stamp**](a-createtimestamp.md)                               | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Beschreibung**](a-description.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/> [**posixGroup**](c-posixgroup.md)<br/>                                                      |
| [**Desktop-Profile**](a-desktopprofile.md)                                  | Falsch     | **Gruppe**                                                                                                                          |
| [**Anzeigename**](a-displayname.md)                                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Display-Name-Printable**](a-displaynameprintable.md)                     | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**DSA-Signature**](a-dsasignature.md)                                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**DS-Core-Propagierungsdaten**](a-dscorepropagationdata.md)                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**E-Mail-Adressen**](a-mail.md)                                           | Falsch     | **Gruppe**                                                                                                                          |
| [**Extension-Name**](a-extensionname.md)                                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Flaggen**](a-flags.md)                                                     | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**From-Entry**](a-fromentry.md)                                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)                | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Garbage Coll-Period**](a-garbagecollperiod.md)                           | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**gidNumber**](a-gidnumber.md)                                             | Falsch     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**Gruppenattribute**](a-groupattributes.md)                                | Falsch     | **Gruppe**                                                                                                                          |
| [**Group-Membership-SAM**](a-groupmembershipsam.md)                         | Falsch     | **Gruppe**                                                                                                                          |
| [**Gruppentyp**](a-grouptype.md)                                            | Richtig      | **Gruppe**                                                                                                                          |
| [**Instanztyp**](a-instancetype.md)                                      | Richtig      | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Is-Deleted**](a-isdeleted.md)                                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Is-Member-of-DL**](a-memberof.md)                                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                           | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**labeledURI**](a-labeleduri.md)                                           | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**Letztes bekanntes übergeordnetes Element**](a-lastknownparent.md)                               | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Legacy-Exchange-DN**](a-legacyexchangedn.md)                             | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**Verwaltet von**](a-managedby.md)                                            | Falsch     | **Gruppe**                                                                                                                          |
| [**Verwaltete Objekte**](a-managedobjects.md)                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Mastered By**](a-masteredby.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Member**](a-member.md)                                                   | Falsch     | **Gruppe**                                                                                                                          |
| [**memberUid**](a-memberuid.md)                                             | Falsch     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**Modify-Time-Stamp**](a-modifytimestamp.md)                               | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)          | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)              | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md)  | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Az-LDAP-Query**](a-msds-azldapquery.md)                            | Falsch     | **Gruppe**                                                                                                                          |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)       | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-KeyVersionNumber**](a-msds-keyversionnumber.md)                    | Falsch     | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                               | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Members-For-Az-Role-BL**](a-msds-membersforazrolebl.md)            | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)     | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)   | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Non-Members**](a-msds-nonmembers.md)                               | Falsch     | **Gruppe**                                                                                                                          |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)      | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)      | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)       | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)               | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)                | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)                | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-Exch-Assistant-Name**](a-msexchassistantname.md)                      | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-Exch-LabeledURI**](a-msexchlabeleduri.md)                             | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**msSFU-30-Name**](a-mssfu30name.md)                                       | Falsch     | **Gruppe**                                                                                                                          |
| [**msSFU-30-Nis-Domain**](a-mssfu30nisdomain.md)                            | Falsch     | **Gruppe**                                                                                                                          |
| [**msSFU-30-Posix-Member**](a-mssfu30posixmember.md)                        | Falsch     | **Gruppe**                                                                                                                          |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                     | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Nicht-Sicherheitsmitglied**](a-nonsecuritymember.md)                           | Falsch     | **Gruppe**                                                                                                                          |
| [**Non-Security-Member-BL**](a-nonsecuritymemberbl.md)                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**NT-Group-Members**](a-ntgroupmembers.md)                                 | Falsch     | **Gruppe**                                                                                                                          |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                     | Richtig      | [**Nach oben**](c-top.md)<br/> [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/>                                       |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Objektkategorie**](a-objectcategory.md)                                  | Richtig      | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Objektklasse**](a-objectclass.md)                                        | Richtig      | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Objekt-GUID**](a-objectguid.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Object-Sid**](a-objectsid.md)                                            | Richtig      | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**Objektversion**](a-objectversion.md)                                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Operatoranzahl**](a-operatorcount.md)                                    | Falsch     | **Gruppe**                                                                                                                          |
| [**Andere bekannte Objekte**](a-otherwellknownobjects.md)                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Teilattributlöschungsliste**](a-partialattributedeletionlist.md)    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Teilattributsatz**](a-partialattributeset.md)                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Mögliche Hindernisse**](a-possibleinferiors.md)                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Primäres Gruppentoken**](a-primarygrouptoken.md)                           | Falsch     | **Gruppe**                                                                                                                          |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                           | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Proxyadressen**](a-proxyaddresses.md)                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Query-Policy-BL**](a-querypolicybl.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Rdn**](a-name.md)                                                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Berichte**](a-directreports.md)                                           | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Reps-From**](a-repsfrom.md)                                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Reps-To**](a-repsto.md)                                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Revision**](a-revision.md)                                               | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**los**](a-rid.md)                                                         | Falsch     | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**SAM-Account-Name**](a-samaccountname.md)                                 | Richtig      | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**SAM-Account-Type**](a-samaccounttype.md)                                 | Falsch     | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                           | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**secretary**](a-secretary.md)                                             | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**Sicherheitsbezeichner**](a-securityidentifier.md)                          | Falsch     | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**Server-Reference-BL**](a-serverreferencebl.md)                           | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Show-In-Address-Book**](a-showinaddressbook.md)                          | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**Nur in erweiterter Ansicht anzeigen**](a-showinadvancedviewonly.md)               | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**SID-Verlauf**](a-sidhistory.md)                                          | Falsch     | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**Site-Object-BL**](a-siteobjectbl.md)                                     | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Sub-Refs**](a-subrefs.md)                                                | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                             | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Supplemental-Credentials**](a-supplementalcredentials.md)                | Falsch     | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**Systemflags**](a-systemflags.md)                                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Telefonnummer**](a-telephonenumber.md)                                | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**Textcodierte OR-Adresse**](a-textencodedoraddress.md)                    | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**Tokengruppen**](a-tokengroups.md)                                        | Falsch     | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**Tokengruppen– global und universell**](a-tokengroupsglobalanduniversal.md) | Falsch     | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**Tokengruppen– keine GC-akzeptabel**](a-tokengroupsnogcacceptable.md)         | Falsch     | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**unixUserPassword**](a-unixuserpassword.md)                               | Falsch     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**User-Cert**](a-usercert.md)                                              | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**Benutzerkennwort**](a-userpassword.md)                                      | Falsch     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**User-SMIME-Certificate**](a-usersmimecertificate.md)                     | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**USN geändert**](a-usnchanged.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**USN-erstellt**](a-usncreated.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**USN-DSA-last-obj-removed**](a-usndsalastobjremoved.md)                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**USN-Intersite**](a-usnintersite.md)                                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**USN-Quelle**](a-usnsource.md)                                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Wbem-Pfad**](a-wbempath.md)                                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Bekannte Objekte**](a-wellknownobjects.md)                             | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Bei Änderung**](a-whenchanged.md)                                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Bei der Erstellung**](a-whencreated.md)                                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**WWW-Startseite**](a-wwwhomepage.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**WWW-Page-Other**](a-url.md)                                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**X509-Cert**](a-usercertificate.md)                                       | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |



## <a name="windows-server-2003-r2-extended-rights"></a>Windows Erweiterte Rechte für Server 2003 R2

Diese Klasse enthält die folgenden erweiterten Rechte für Windows Server 2003 R2:



| Allgemeiner Name                  |
|------------------------------|
| [**Senden an**](r-send-to.md) |



## <a name="windows-server-2003-r2-validated-writes"></a>Windows Von Server 2003 R2 überprüfte Schreibvorgänge

Diese Klasse enthält die folgenden überprüften Schreibvorgänge für Windows Server 2003 R2:



| Allgemeiner Name                                  |
|----------------------------------------------|
| [**Selbstmitgliedschaft**](r-self-membership.md) |



## <a name="windows-server-2003-r2-property-sets"></a>Windows Server 2003 R2-Eigenschaftensätze

Diese Klasse enthält die folgenden Eigenschaftensätze für Windows Server 2003 R2:



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
| System-Only                 | Falsch                                                                                                                                                                                                                                                                                                            |
| Object-Category             | 1                                                                                                                                                                                                                                                                                                                |
| Default-Object-Category     | \-                                                                                                                                                                                                                                                                                                               |
| Governs-Id                  | 1.2.840.113556.1.5.8                                                                                                                                                                                                                                                                                             |
| Default-Hiding-Value        | 0                                                                                                                                                                                                                                                                                                                |
| Rdn-Att-Id                  | [**Allgemeiner Name**](a-cn.md)<br/>                                                                                                                                                                                                                                                                           |
| Unterklasse von                 | [**Nach oben**](c-top.md)<br/>                                                                                                                                                                                                                                                                                  |
| Mögliche Übergeordnete          | [**Domänen-DNS**](c-domaindns.md)[**Organizational-Unit**](c-organizationalunit.md)[**Builtin-Domain**](c-builtindomain.md)[**Container**](c-container.md)[**ms-DS-Az-Admin-Manager**](c-msds-azadminmanager.md)[**ms-DS-Az-Application**](c-msds-azapplication.md)[**ms-DS-Az-Scope**](c-msds-azscope.md) |
| Zusätzlich           | [**posixGroup**](c-posixgroup.md)[**Security-Principal**](c-securityprincipal.md) (System)[**Mail-Recipient**](c-mailrecipient.md) (System)                                                                                                                                                                   |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                     |
| Standardsicherheitsdeskriptor | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;;; AU)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; AO)(A;; RPLCLORC;;; PS)(OA;; CR;ab721a55-1e2f-11d0-9819-00aa0040529b;; AU)(OA;; RP;46a9b11d-60ae-405a-b7e8-ff8a58d456d2;; S-1-5-32-560)                                                   |
| System-Flags                | 0x00000010                                                                                                                                                                                                                                                                                                       |



## <a name="windows-server-2008-attributes"></a>Windows Server 2008-Attribute

Diese Klasse enthält die folgenden Attribute für Windows Server 2008:



| attribute                                                                        | Obligatorisch. | Abgeleitet von                                                                                                                       |
|----------------------------------------------------------------------------------|-----------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Kontoname-Verlauf**](a-accountnamehistory.md)                             | Falsch     | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**Admin-Count**](a-admincount.md)                                              | Falsch     | **Gruppe**                                                                                                                          |
| [**Administratorbeschreibung**](a-admindescription.md)                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Admin-Display-Name**](a-admindisplayname.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Allowed-Attributes**](a-allowedattributes.md)                                | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)             | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                           | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)        | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ALT-SICHERHEITSIDENTITÄTEN**](a-altsecurityidentities.md)                       | Falsch     | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Kanonischer Name**](a-canonicalname.md)                                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Kommentar**](a-info.md)                                                        | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**Allgemeiner Name**](a-cn.md)                                                      | Richtig      | [**Nach oben**](c-top.md)<br/> [**posixGroup**](c-posixgroup.md)<br/> [**E-Mail-Empfänger**](c-mailrecipient.md)<br/> |
| [**Control-Access-Rights**](a-controlaccessrights.md)                           | Falsch     | **Gruppe**                                                                                                                          |
| [**Erstellen eines Zeitstempels**](a-createtimestamp.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Beschreibung**](a-description.md)                                             | Falsch     | [**Nach oben**](c-top.md)<br/> [**posixGroup**](c-posixgroup.md)<br/>                                                      |
| [**Desktopprofil**](a-desktopprofile.md)                                      | Falsch     | **Gruppe**                                                                                                                          |
| [**Anzeigename**](a-displayname.md)                                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Display-Name-Printable**](a-displaynameprintable.md)                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**DSA-Signature**](a-dsasignature.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**DS-Core-Propagierungsdaten**](a-dscorepropagationdata.md)                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**E-Mail-Adressen**](a-mail.md)                                               | Falsch     | **Gruppe**                                                                                                                          |
| [**Extension-Name**](a-extensionname.md)                                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Flaggen**](a-flags.md)                                                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**From-Entry**](a-fromentry.md)                                                | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Garbage Coll-Period**](a-garbagecollperiod.md)                               | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**gidNumber**](a-gidnumber.md)                                                 | Falsch     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**Gruppenattribute**](a-groupattributes.md)                                    | Falsch     | **Gruppe**                                                                                                                          |
| [**Group-Membership-SAM**](a-groupmembershipsam.md)                             | Falsch     | **Gruppe**                                                                                                                          |
| [**Gruppentyp**](a-grouptype.md)                                                | Richtig      | **Gruppe**                                                                                                                          |
| [**Instanztyp**](a-instancetype.md)                                          | Richtig      | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Is-Deleted**](a-isdeleted.md)                                                | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Is-Member-of-DL**](a-memberof.md)                                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                               | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**labeledURI**](a-labeleduri.md)                                               | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**Letztes bekanntes übergeordnetes Element**](a-lastknownparent.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Legacy-Exchange-DN**](a-legacyexchangedn.md)                                 | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**Verwaltet von**](a-managedby.md)                                                | Falsch     | **Gruppe**                                                                                                                          |
| [**Verwaltete Objekte**](a-managedobjects.md)                                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Mastered By**](a-masteredby.md)                                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Member**](a-member.md)                                                       | Falsch     | **Gruppe**                                                                                                                          |
| [**memberUid**](a-memberuid.md)                                                 | Falsch     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**Modify-Time-Stamp**](a-modifytimestamp.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)              | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md)      | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md)   | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Az-Application-Data**](a-msds-azapplicationdata.md)                    | Falsch     | **Gruppe**                                                                                                                          |
| [**ms-DS-Az-Biz-Rule**](a-msds-azbizrule.md)                                    | Falsch     | **Gruppe**                                                                                                                          |
| [**ms-DS-Az-Biz-Rule-Language**](a-msds-azbizrulelanguage.md)                   | Falsch     | **Gruppe**                                                                                                                          |
| [**ms-DS-Az-Generic-Data**](a-msds-azgenericdata.md)                            | Falsch     | **Gruppe**                                                                                                                          |
| [**ms-DS-Az-Last-Imported-Biz-Rule-Path**](a-msds-azlastimportedbizrulepath.md) | Falsch     | **Gruppe**                                                                                                                          |
| [**ms-DS-Az-LDAP-Query**](a-msds-azldapquery.md)                                | Falsch     | **Gruppe**                                                                                                                          |
| [**ms-DS-Az-Object-Guid**](a-msds-azobjectguid.md)                              | Falsch     | **Gruppe**                                                                                                                          |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)           | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Is-Domain-For**](a-msds-isdomainfor.md)                                | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-is-full-replica-for**](a-msds-isfullreplicafor.md)                     | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-is-partial-replica-for**](a-msds-ispartialreplicafor.md)               | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-KeyVersionNumber**](a-msds-keyversionnumber.md)                        | Falsch     | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Members-for-Az-Role-BL**](a-msds-membersforazrolebl.md)                | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)         | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)       | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-Type**](a-msds-nctype.md)                                           | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Non-Members**](a-msds-nonmembers.md)                                   | Falsch     | **Gruppe**                                                                                                                          |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Operations-for-Az-Role-BL**](a-msds-operationsforazrolebl.md)          | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Operations-for-Az-Task-BL**](a-msds-operationsforaztaskbl.md)          | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Phonetic-Display-Name**](a-msds-phoneticdisplayname.md)                | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                             | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-PSO-Applied**](a-msds-psoapplied.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)           | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Revealed-DSAs**](a-msds-revealeddsas.md)                               | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Revealed-List-BL**](a-msds-revealedlistbl.md)                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Tasks-for-Az-Role-BL**](a-msds-tasksforazrolebl.md)                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Tasks-for-Az-Task-BL**](a-msds-tasksforaztaskbl.md)                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-Exch-Assistant-Name**](a-msexchassistantname.md)                          | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-Exch-LabeledURI**](a-msexchlabeleduri.md)                                 | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**msSFU-30-Name**](a-mssfu30name.md)                                           | Falsch     | **Gruppe**                                                                                                                          |
| [**msSFU-30-Nis-Domain**](a-mssfu30nisdomain.md)                                | Falsch     | **Gruppe**                                                                                                                          |
| [**msSFU-30-Posix-Member**](a-mssfu30posixmember.md)                            | Falsch     | **Gruppe**                                                                                                                          |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Nicht-Sicherheitsmitglied**](a-nonsecuritymember.md)                               | Falsch     | **Gruppe**                                                                                                                          |
| [**Non-Security-Member-BL**](a-nonsecuritymemberbl.md)                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**NT-Group-Members**](a-ntgroupmembers.md)                                     | Falsch     | **Gruppe**                                                                                                                          |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                         | Richtig      | [**Nach oben**](c-top.md)<br/> [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/>                                       |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                     | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Objektkategorie**](a-objectcategory.md)                                      | Richtig      | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Objektklasse**](a-objectclass.md)                                            | Richtig      | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Objekt-GUID**](a-objectguid.md)                                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Object-Sid**](a-objectsid.md)                                                | Richtig      | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**Objektversion**](a-objectversion.md)                                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Operatoranzahl**](a-operatorcount.md)                                        | Falsch     | **Gruppe**                                                                                                                          |
| [**Andere bekannte Objekte**](a-otherwellknownobjects.md)                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Teilattributlöschungsliste**](a-partialattributedeletionlist.md)        | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Teilattributsatz**](a-partialattributeset.md)                           | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Mögliche Hindernisse**](a-possibleinferiors.md)                                | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Primäres Gruppentoken**](a-primarygrouptoken.md)                               | Falsch     | **Gruppe**                                                                                                                          |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                               | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Proxyadressen**](a-proxyaddresses.md)                                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Query-Policy-BL**](a-querypolicybl.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Rdn**](a-name.md)                                                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                             | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Berichte**](a-directreports.md)                                               | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Reps-From**](a-repsfrom.md)                                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Reps-To**](a-repsto.md)                                                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Revision**](a-revision.md)                                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**los**](a-rid.md)                                                             | Falsch     | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**SAM-Account-Name**](a-samaccountname.md)                                     | Richtig      | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**SAM-Account-Type**](a-samaccounttype.md)                                     | Falsch     | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                               | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**secretary**](a-secretary.md)                                                 | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**Sicherheits-ID**](a-securityidentifier.md)                              | Falsch     | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**Server-Reference-BL**](a-serverreferencebl.md)                               | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Show-In-Address-Book**](a-showinaddressbook.md)                              | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**SID-Verlauf**](a-sidhistory.md)                                              | Falsch     | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**Site-Object-BL**](a-siteobjectbl.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Sub-Refs**](a-subrefs.md)                                                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Zusätzliche Anmeldeinformationen**](a-supplementalcredentials.md)                    | Falsch     | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**Systemflags**](a-systemflags.md)                                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Telefonnummer**](a-telephonenumber.md)                                    | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**Textcodierte OR-Adresse**](a-textencodedoraddress.md)                        | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**Tokengruppen**](a-tokengroups.md)                                            | Falsch     | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**Tokengruppen –global und universell**](a-tokengroupsglobalanduniversal.md)     | Falsch     | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**Tokengruppen-No-GC-Acceptable**](a-tokengroupsnogcacceptable.md)             | Falsch     | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**unixUserPassword**](a-unixuserpassword.md)                                   | Falsch     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**User-Cert**](a-usercert.md)                                                  | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**Benutzerkennwort**](a-userpassword.md)                                          | Falsch     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**User-SMIME-Certificate**](a-usersmimecertificate.md)                         | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**USN-Changed**](a-usnchanged.md)                                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**VON USN erstellt**](a-usncreated.md)                                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**USN-Intersite**](a-usnintersite.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**USN-Quelle**](a-usnsource.md)                                                | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Wbem-Path**](a-wbempath.md)                                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Bekannte Objekte**](a-wellknownobjects.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Wenn geändert**](a-whenchanged.md)                                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Wenn erstellt**](a-whencreated.md)                                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**WWW-Homepage**](a-wwwhomepage.md)                                           | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**WWW-Page-Other**](a-url.md)                                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**X509-Cert**](a-usercertificate.md)                                           | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |



## <a name="windows-server-2008-extended-rights"></a>Windows Erweiterte Server 2008-Rechte

Diese Klasse enthält die folgenden erweiterten Rechte für Windows Server 2008:



| Allgemeiner Name                  |
|------------------------------|
| [**Senden an**](r-send-to.md) |



## <a name="windows-server-2008-validated-writes"></a>Windows Von Server 2008 überprüfte Schreibvorgänge

Diese Klasse enthält die folgenden überprüften Schreibvorgänge für Windows Server 2008:



| Allgemeiner Name                                  |
|----------------------------------------------|
| [**Selbstmitgliedschaft**](r-self-membership.md) |



## <a name="windows-server-2008-property-sets"></a>Windows Server 2008-Eigenschaftensätze

Diese Klasse enthält die folgenden Eigenschaftensätze für Windows Server 2008:



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
| System-Only                 | Falsch                                                                                                                                                                                                                                                                                                            |
| Object-Category             | 1                                                                                                                                                                                                                                                                                                                |
| Default-Object-Category     | \-                                                                                                                                                                                                                                                                                                               |
| Governs-Id                  | 1.2.840.113556.1.5.8                                                                                                                                                                                                                                                                                             |
| Default-Hiding-Value        | 0                                                                                                                                                                                                                                                                                                                |
| Rdn-Att-Id                  | [**Common-Name**](a-cn.md)<br/>                                                                                                                                                                                                                                                                           |
| Unterklasse von                 | [**Nach oben**](c-top.md)<br/>                                                                                                                                                                                                                                                                                  |
| Mögliche Vorgesetzte          | [**Domain-DNS**](c-domaindns.md)[**Organizational-Unit**](c-organizationalunit.md)[**Builtin-Domain Container**](c-builtindomain.md)[](c-container.md)[**ms-DS-Az-Admin-Manager**](c-msds-azadminmanager.md)[**ms-DS-Az-Application**](c-msds-azapplication.md)[**ms-DS-Az-Scope**](c-msds-azscope.md) |
| Zusätzlich           | [**posixGroup**](c-posixgroup.md)[**Security-Principal**](c-securityprincipal.md) (System)[**Mail-Recipient**](c-mailrecipient.md) (System)                                                                                                                                                                   |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                     |
| Standardsicherheitsdeskriptor | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;;; AU)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; AO)(A;; RPLCLORC;;; PS)(OA;; CR;ab721a55-1e2f-11d0-9819-00aa0040529b;; AU)(OA;; RP;46a9b11d-60ae-405a-b7e8-ff8a58d456d2;; S-1-5-32-560)                                                   |
| System-Flags                | 0x00000010                                                                                                                                                                                                                                                                                                       |



## <a name="windows-server-2008-r2-attributes"></a>Windows Server 2008 R2-Attribute

Diese Klasse enthält die folgenden Attribute für Windows Server 2008 R2:



| attribute                                                                        | Obligatorisch. | Abgeleitet von                                                                                                                       |
|----------------------------------------------------------------------------------|-----------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Account-Name-History**](a-accountnamehistory.md)                             | Falsch     | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**Admin-Count**](a-admincount.md)                                              | Falsch     | **Gruppe**                                                                                                                          |
| [**Admin-Description**](a-admindescription.md)                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Administratoranzeigename**](a-admindisplayname.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Allowed-Attributes**](a-allowedattributes.md)                                | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)             | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                           | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)        | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Alt-Sicherheitsidentitäten**](a-altsecurityidentities.md)                       | Falsch     | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Kanonischer Name**](a-canonicalname.md)                                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Kommentar**](a-info.md)                                                        | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**Allgemeiner Name**](a-cn.md)                                                      | Richtig      | [**Nach oben**](c-top.md)<br/> [**posixGroup**](c-posixgroup.md)<br/> [**E-Mail-Empfänger**](c-mailrecipient.md)<br/> |
| [**Control-Access-Rights**](a-controlaccessrights.md)                           | Falsch     | **Gruppe**                                                                                                                          |
| [**Erstellen eines Zeitstempels**](a-createtimestamp.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Beschreibung**](a-description.md)                                             | Falsch     | [**Nach oben**](c-top.md)<br/> [**posixGroup**](c-posixgroup.md)<br/>                                                      |
| [**Desktopprofil**](a-desktopprofile.md)                                      | Falsch     | **Gruppe**                                                                                                                          |
| [**Anzeigename**](a-displayname.md)                                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Anzeigename– druckbar**](a-displaynameprintable.md)                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**DSA-Signature**](a-dsasignature.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**DS-Core-Propagierungsdaten**](a-dscorepropagationdata.md)                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**E-Mail-Adressen**](a-mail.md)                                               | Falsch     | **Gruppe**                                                                                                                          |
| [**Erweiterungsname**](a-extensionname.md)                                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Flaggen**](a-flags.md)                                                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**From-Entry**](a-fromentry.md)                                                | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Garbage-Coll-Period**](a-garbagecollperiod.md)                               | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**gidNumber**](a-gidnumber.md)                                                 | Falsch     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**Gruppenattribute**](a-groupattributes.md)                                    | Falsch     | **Gruppe**                                                                                                                          |
| [**Gruppenmitgliedschafts-SAM**](a-groupmembershipsam.md)                             | Falsch     | **Gruppe**                                                                                                                          |
| [**Gruppentyp**](a-grouptype.md)                                                | Richtig      | **Gruppe**                                                                                                                          |
| [**Instanztyp**](a-instancetype.md)                                          | Richtig      | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Is-Deleted**](a-isdeleted.md)                                                | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Is-Member-of-DL**](a-memberof.md)                                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                               | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Wird wiederverwendet**](a-isrecycled.md)                                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**labeledURI**](a-labeleduri.md)                                               | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**Last-Known-Parent**](a-lastknownparent.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Legacy-Exchange-DN**](a-legacyexchangedn.md)                                 | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**Verwaltet von**](a-managedby.md)                                                | Falsch     | **Gruppe**                                                                                                                          |
| [**Verwaltete Objekte**](a-managedobjects.md)                                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Mastered By**](a-masteredby.md)                                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Member**](a-member.md)                                                       | Falsch     | **Gruppe**                                                                                                                          |
| [**memberUid**](a-memberuid.md)                                                 | Falsch     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**Modify-Time-Stamp**](a-modifytimestamp.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)              | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md)      | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md)   | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Az-Application-Data**](a-msds-azapplicationdata.md)                    | Falsch     | **Gruppe**                                                                                                                          |
| [**ms-DS-Az-Biz-Rule**](a-msds-azbizrule.md)                                    | Falsch     | **Gruppe**                                                                                                                          |
| [**ms-DS-Az-Biz-Rule-Language**](a-msds-azbizrulelanguage.md)                   | Falsch     | **Gruppe**                                                                                                                          |
| [**ms-DS-Az-Generic-Data**](a-msds-azgenericdata.md)                            | Falsch     | **Gruppe**                                                                                                                          |
| [**ms-DS-Az-Last-Imported-Biz-Rule-Path**](a-msds-azlastimportedbizrulepath.md) | Falsch     | **Gruppe**                                                                                                                          |
| [**ms-DS-Az-LDAP-Query**](a-msds-azldapquery.md)                                | Falsch     | **Gruppe**                                                                                                                          |
| [**ms-DS-Az-Object-Guid**](a-msds-azobjectguid.md)                              | Falsch     | **Gruppe**                                                                                                                          |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)           | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Enabled-Feature-BL**](a-msds-enabledfeaturebl.md)                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)             | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-is-Domain-for**](a-msds-isdomainfor.md)                                | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-is-full-replica-for**](a-msds-isfullreplicafor.md)                     | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-is-partial-replica-for**](a-msds-ispartialreplicafor.md)               | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-KeyVersionNumber**](a-msds-keyversionnumber.md)                        | Falsch     | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-local-Effective-Deletion-Time**](a-msds-localeffectivedeletiontime.md) | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-local-Effective-Recycle-Time**](a-msds-localeffectiverecycletime.md)   | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Members-For-Az-Role-BL**](a-msds-membersforazrolebl.md)                | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)         | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)       | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-Type**](a-msds-nctype.md)                                           | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Non-Members**](a-msds-nonmembers.md)                                   | Falsch     | **Gruppe**                                                                                                                          |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-OIDToGroup-Link-BL**](a-msds-oidtogrouplinkbl.md)                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)          | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)          | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Phonetic-Display-Name**](a-msds-phoneticdisplayname.md)                | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                             | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-PSO-Applied**](a-msds-psoapplied.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)           | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Revealed-DSAs**](a-msds-revealeddsas.md)                               | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Revealed-List-BL**](a-msds-revealedlistbl.md)                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-Exch-Assistant-Name**](a-msexchassistantname.md)                          | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-Exch-LabeledURI**](a-msexchlabeleduri.md)                                 | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**msSFU-30-Name**](a-mssfu30name.md)                                           | Falsch     | **Gruppe**                                                                                                                          |
| [**msSFU-30-Nis-Domain**](a-mssfu30nisdomain.md)                                | Falsch     | **Gruppe**                                                                                                                          |
| [**msSFU-30-Posix-Member**](a-mssfu30posixmember.md)                            | Falsch     | **Gruppe**                                                                                                                          |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Nicht-Sicherheitsmitglied**](a-nonsecuritymember.md)                               | Falsch     | **Gruppe**                                                                                                                          |
| [**Non-Security-Member-BL**](a-nonsecuritymemberbl.md)                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**NT-Group-Members**](a-ntgroupmembers.md)                                     | Falsch     | **Gruppe**                                                                                                                          |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                         | Richtig      | [**Nach oben**](c-top.md)<br/> [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/>                                       |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                     | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Objektkategorie**](a-objectcategory.md)                                      | Richtig      | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Object-Class**](a-objectclass.md)                                            | Richtig      | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Objekt-GUID**](a-objectguid.md)                                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Object-Sid**](a-objectsid.md)                                                | Richtig      | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**Object-Version**](a-objectversion.md)                                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Operatoranzahl**](a-operatorcount.md)                                        | Falsch     | **Gruppe**                                                                                                                          |
| [**Andere bekannte Objekte**](a-otherwellknownobjects.md)                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)        | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                           | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Mögliche 100000000000**](a-possibleinferiors.md)                                | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Primary-Group-Token**](a-primarygrouptoken.md)                               | Falsch     | **Gruppe**                                                                                                                          |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                               | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Proxyadressen**](a-proxyaddresses.md)                                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Query-Policy-BL**](a-querypolicybl.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Rdn**](a-name.md)                                                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                             | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Berichte**](a-directreports.md)                                               | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Reps-From**](a-repsfrom.md)                                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Reps-To**](a-repsto.md)                                                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Revision**](a-revision.md)                                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**los**](a-rid.md)                                                             | Falsch     | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**SAM-Account-Name**](a-samaccountname.md)                                     | Richtig      | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**SAM-Account-Type**](a-samaccounttype.md)                                     | Falsch     | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                               | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**secretary**](a-secretary.md)                                                 | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**Sicherheits-ID**](a-securityidentifier.md)                              | Falsch     | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**Server-Reference-BL**](a-serverreferencebl.md)                               | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Show-In-Address-Book**](a-showinaddressbook.md)                              | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**SID-Verlauf**](a-sidhistory.md)                                              | Falsch     | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**Site-Object-BL**](a-siteobjectbl.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Sub-Refs**](a-subrefs.md)                                                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Zusätzliche Anmeldeinformationen**](a-supplementalcredentials.md)                    | Falsch     | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**Systemflags**](a-systemflags.md)                                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Telefonnummer**](a-telephonenumber.md)                                    | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**Textcodierte OR-Adresse**](a-textencodedoraddress.md)                        | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**Tokengruppen**](a-tokengroups.md)                                            | Falsch     | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**Tokengruppen –global und universell**](a-tokengroupsglobalanduniversal.md)     | Falsch     | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**Tokengruppen-No-GC-Acceptable**](a-tokengroupsnogcacceptable.md)             | Falsch     | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**unixUserPassword**](a-unixuserpassword.md)                                   | Falsch     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**User-Cert**](a-usercert.md)                                                  | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**Benutzerkennwort**](a-userpassword.md)                                          | Falsch     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**User-SMIME-Certificate**](a-usersmimecertificate.md)                         | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**USN-Changed**](a-usnchanged.md)                                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**VON USN erstellt**](a-usncreated.md)                                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**USN-Intersite**](a-usnintersite.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**USN-Quelle**](a-usnsource.md)                                                | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Wbem-Path**](a-wbempath.md)                                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Bekannte Objekte**](a-wellknownobjects.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Wenn geändert**](a-whenchanged.md)                                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Wenn erstellt**](a-whencreated.md)                                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**WWW-Homepage**](a-wwwhomepage.md)                                           | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**WWW-Page-Other**](a-url.md)                                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**X509-Cert**](a-usercertificate.md)                                           | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |



## <a name="windows-server-2008-r2-extended-rights"></a>Windows Erweiterte Server 2008 R2-Rechte

Diese Klasse enthält die folgenden erweiterten Rechte für Windows Server 2008 R2:



| Allgemeiner Name                  |
|------------------------------|
| [**Senden an**](r-send-to.md) |



## <a name="windows-server-2008-r2-validated-writes"></a>Windows Von Server 2008 R2 überprüfte Schreibvorgänge

Diese Klasse enthält die folgenden überprüften Schreibvorgänge für Windows Server 2008 R2:



| Allgemeiner Name                                  |
|----------------------------------------------|
| [**Selbstmitgliedschaft**](r-self-membership.md) |



## <a name="windows-server-2008-r2-property-sets"></a>Windows Server 2008 R2-Eigenschaftensätze

Diese Klasse enthält die folgenden Eigenschaftensätze für Windows Server 2008 R2:



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
| System-Only                 | Falsch                                                                                                                                                                                                                                                                                                            |
| Object-Category             | 1                                                                                                                                                                                                                                                                                                                |
| Default-Object-Category     | \-                                                                                                                                                                                                                                                                                                               |
| Governs-Id                  | 1.2.840.113556.1.5.8                                                                                                                                                                                                                                                                                             |
| Default-Hiding-Value        | 0                                                                                                                                                                                                                                                                                                                |
| Rdn-Att-Id                  | [**Common-Name**](a-cn.md)<br/>                                                                                                                                                                                                                                                                           |
| Unterklasse von                 | [**Nach oben**](c-top.md)<br/>                                                                                                                                                                                                                                                                                  |
| Mögliche Vorgesetzte          | [**Domain-DNS**](c-domaindns.md)[**Organizational-Unit**](c-organizationalunit.md)[**Builtin-Domain Container**](c-builtindomain.md)[](c-container.md)[**ms-DS-Az-Admin-Manager**](c-msds-azadminmanager.md)[**ms-DS-Az-Application**](c-msds-azapplication.md)[**ms-DS-Az-Scope**](c-msds-azscope.md) |
| Zusätzlich           | [**posixGroup**](c-posixgroup.md)[**Security-Principal**](c-securityprincipal.md) (System)[**Mail-Recipient**](c-mailrecipient.md) (System)                                                                                                                                                                   |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                     |
| Standardsicherheitsdeskriptor | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;;; AU)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; AO)(A;; RPLCLORC;;; PS)(OA;; CR;ab721a55-1e2f-11d0-9819-00aa0040529b;; AU)(OA;; RP;46a9b11d-60ae-405a-b7e8-ff8a58d456d2;; S-1-5-32-560)                                                   |
| System-Flags                | 0x00000010                                                                                                                                                                                                                                                                                                       |



## <a name="windows-server-2012-attributes"></a>Windows Server 2012 Attribute

Diese Klasse enthält die folgenden Attribute für Windows Server 2012:



| attribute                                                                                    | Obligatorisch. | Abgeleitet von                                                                                                                       |
|----------------------------------------------------------------------------------------------|-----------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Account-Name-History**](a-accountnamehistory.md)                                         | Falsch     | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**Admin-Count**](a-admincount.md)                                                          | Falsch     | **Gruppe**                                                                                                                          |
| [**Admin-Description**](a-admindescription.md)                                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Administratoranzeigename**](a-admindisplayname.md)                                             | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Allowed-Attributes**](a-allowedattributes.md)                                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Alt-Sicherheitsidentitäten**](a-altsecurityidentities.md)                                   | Falsch     | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                                | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Kanonischer Name**](a-canonicalname.md)                                                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Kommentar**](a-info.md)                                                                    | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**Common-Name**](a-cn.md)                                                                  | Richtig      | [**Nach oben**](c-top.md)<br/> [**posixGroup**](c-posixgroup.md)<br/> [**E-Mail-Empfänger**](c-mailrecipient.md)<br/> |
| [**Control-Access-Rights**](a-controlaccessrights.md)                                       | Falsch     | **Gruppe**                                                                                                                          |
| [**Create-Time-Stamp**](a-createtimestamp.md)                                               | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Beschreibung**](a-description.md)                                                         | Falsch     | [**Nach oben**](c-top.md)<br/> [**posixGroup**](c-posixgroup.md)<br/>                                                      |
| [**Desktop-Profile**](a-desktopprofile.md)                                                  | Falsch     | **Gruppe**                                                                                                                          |
| [**Anzeigename**](a-displayname.md)                                                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Display-Name-Printable**](a-displaynameprintable.md)                                     | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**DSA-Signature**](a-dsasignature.md)                                                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**DS-Core-Propagierungsdaten**](a-dscorepropagationdata.md)                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**E-Mail-Adressen**](a-mail.md)                                                           | Falsch     | **Gruppe**                                                                                                                          |
| [**Extension-Name**](a-extensionname.md)                                                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Flaggen**](a-flags.md)                                                                     | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**From-Entry**](a-fromentry.md)                                                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)                                | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Garbage-Coll-Period**](a-garbagecollperiod.md)                                           | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**gidNumber**](a-gidnumber.md)                                                             | Falsch     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**Gruppenattribute**](a-groupattributes.md)                                                | Falsch     | **Gruppe**                                                                                                                          |
| [**Gruppenmitgliedschafts-SAM**](a-groupmembershipsam.md)                                         | Falsch     | **Gruppe**                                                                                                                          |
| [**Gruppentyp**](a-grouptype.md)                                                            | Richtig      | **Gruppe**                                                                                                                          |
| [**Instanztyp**](a-instancetype.md)                                                      | Richtig      | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                                | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Is-Deleted**](a-isdeleted.md)                                                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Is-Member-of-DL**](a-memberof.md)                                                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                                           | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Wird wiederverwendet**](a-isrecycled.md)                                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**labeledURI**](a-labeleduri.md)                                                           | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**Last-Known-Parent**](a-lastknownparent.md)                                               | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Legacy-Exchange-DN**](a-legacyexchangedn.md)                                             | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**Verwaltet von**](a-managedby.md)                                                            | Falsch     | **Gruppe**                                                                                                                          |
| [**Verwaltete Objekte**](a-managedobjects.md)                                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Mastered-By**](a-masteredby.md)                                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Member**](a-member.md)                                                                   | Falsch     | **Gruppe**                                                                                                                          |
| [**memberUid**](a-memberuid.md)                                                             | Falsch     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**Modify-Time-Stamp**](a-modifytimestamp.md)                                               | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md)                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md)               | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Az-Application-Data**](a-msds-azapplicationdata.md)                                | Falsch     | **Gruppe**                                                                                                                          |
| [**ms-DS-Az-Biz-Rule**](a-msds-azbizrule.md)                                                | Falsch     | **Gruppe**                                                                                                                          |
| [**ms-DS-Az-Biz-Rule-Language**](a-msds-azbizrulelanguage.md)                               | Falsch     | **Gruppe**                                                                                                                          |
| [**ms-DS-Az-Generic-Data**](a-msds-azgenericdata.md)                                        | Falsch     | **Gruppe**                                                                                                                          |
| [**ms-DS-Az-Last-Imported-Biz-Rule-Path**](a-msds-azlastimportedbizrulepath.md)             | Falsch     | **Gruppe**                                                                                                                          |
| [**ms-DS-Az-LDAP-Query**](a-msds-azldapquery.md)                                            | Falsch     | **Gruppe**                                                                                                                          |
| [**ms-DS-Az-Object-Guid**](a-msds-azobjectguid.md)                                          | Falsch     | **Gruppe**                                                                                                                          |
| [**ms-DS-Claim-Shares-Possible-Values-with-BL**](a-msds-claimsharespossiblevalueswithbl.md) | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Enabled-Feature-BL**](a-msds-enabledfeaturebl.md)                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-GeoCoordinates-Altitude**](a-msds-geocoordinatesaltitude.md)                       | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-DS-GeoCoordinates-Latitude**](a-msds-geocoordinateslatitude.md)                       | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-DS-GeoCoordinates-Longitude**](a-msds-geocoordinateslongitude.md)                     | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-DS-Host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Is-Domain-For**](a-msds-isdomainfor.md)                                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-is-full-replica-for**](a-msds-isfullreplicafor.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-is-partial-replica-for**](a-msds-ispartialreplicafor.md)                           | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Is-Primary-Computer-For**](a-msds-isprimarycomputerfor.md)                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-KeyVersionNumber**](a-msds-keyversionnumber.md)                                    | Falsch     | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-local-Effective-Deletion-Time**](a-msds-localeffectivedeletiontime.md)             | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-local-Effective-Recycle-Time**](a-msds-localeffectiverecycletime.md)               | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                                               | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Members-for-Az-Role-BL**](a-msds-membersforazrolebl.md)                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Members-of-Resource-Property-List-BL**](a-msds-membersofresourcepropertylistbl.md) | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)                     | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)                | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-Type**](a-msds-nctype.md)                                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Non-Members**](a-msds-nonmembers.md)                                               | Falsch     | **Gruppe**                                                                                                                          |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                                | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-OIDToGroup-Link-BL**](a-msds-oidtogrouplinkbl.md)                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Operations-for-Az-Role-BL**](a-msds-operationsforazrolebl.md)                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Phonetic-Display-Name**](a-msds-phoneticdisplayname.md)                            | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-DS-Primary-Computer**](a-msds-primarycomputer.md)                                     | Falsch     | **Gruppe**                                                                                                                          |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-PSO-Applied**](a-msds-psoapplied.md)                                               | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                               | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Revealed-DSAs**](a-msds-revealeddsas.md)                                           | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Revealed-List-BL**](a-msds-revealedlistbl.md)                                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)                                | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)                                | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-TDO-Egress-BL**](a-msds-tdoegressbl.md)                                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-TDO-Ingress-BL**](a-msds-tdoingressbl.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Value-Type-Reference-BL**](a-msds-valuetypereferencebl.md)                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**ms-Exch-Assistant-Name**](a-msexchassistantname.md)                                      | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-Exch-LabeledURI**](a-msexchlabeleduri.md)                                             | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**msSFU-30-Name**](a-mssfu30name.md)                                                       | Falsch     | **Gruppe**                                                                                                                          |
| [**msSFU-30-Nis-Domain**](a-mssfu30nisdomain.md)                                            | Falsch     | **Gruppe**                                                                                                                          |
| [**msSFU-30-Posix-Member**](a-mssfu30posixmember.md)                                        | Falsch     | **Gruppe**                                                                                                                          |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                                     | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Nicht-Sicherheitsmitglied**](a-nonsecuritymember.md)                                           | Falsch     | **Gruppe**                                                                                                                          |
| [**Non-Security-Member-BL**](a-nonsecuritymemberbl.md)                                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**NT-Group-Members**](a-ntgroupmembers.md)                                                 | Falsch     | **Gruppe**                                                                                                                          |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                                     | Richtig      | [**Nach oben**](c-top.md)<br/> [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/>                                       |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                                 | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Objektkategorie**](a-objectcategory.md)                                                  | Richtig      | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Object-Class**](a-objectclass.md)                                                        | Richtig      | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Objekt-GUID**](a-objectguid.md)                                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Object-Sid**](a-objectsid.md)                                                            | Richtig      | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**Object-Version**](a-objectversion.md)                                                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Operatoranzahl**](a-operatorcount.md)                                                    | Falsch     | **Gruppe**                                                                                                                          |
| [**Andere bekannte Objekte**](a-otherwellknownobjects.md)                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Mögliche 100000000000**](a-possibleinferiors.md)                                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Primary-Group-Token**](a-primarygrouptoken.md)                                           | Falsch     | **Gruppe**                                                                                                                          |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                                           | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Proxyadressen**](a-proxyaddresses.md)                                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Query-Policy-BL**](a-querypolicybl.md)                                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Rdn**](a-name.md)                                                                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                                    | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Berichte**](a-directreports.md)                                                           | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Reps-From**](a-repsfrom.md)                                                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Reps-To**](a-repsto.md)                                                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Revision**](a-revision.md)                                                               | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**los**](a-rid.md)                                                                         | Falsch     | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**SAM-Account-Name**](a-samaccountname.md)                                                 | Richtig      | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**SAM-Account-Type**](a-samaccounttype.md)                                                 | Falsch     | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                                           | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**secretary**](a-secretary.md)                                                             | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**Sicherheits-ID**](a-securityidentifier.md)                                          | Falsch     | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**Server-Reference-BL**](a-serverreferencebl.md)                                           | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Show-In-Address-Book**](a-showinaddressbook.md)                                          | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)                               | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**SID-Verlauf**](a-sidhistory.md)                                                          | Falsch     | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**Site-Object-BL**](a-siteobjectbl.md)                                                     | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Sub-Refs**](a-subrefs.md)                                                                | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                             | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Zusätzliche Anmeldeinformationen**](a-supplementalcredentials.md)                                | Falsch     | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**Systemflags**](a-systemflags.md)                                                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Telefonnummer**](a-telephonenumber.md)                                                | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**Textcodierte OR-Adresse**](a-textencodedoraddress.md)                                    | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**Tokengruppen**](a-tokengroups.md)                                                        | Falsch     | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**Tokengruppen –global und universell**](a-tokengroupsglobalanduniversal.md)                 | Falsch     | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**Tokengruppen-No-GC-Acceptable**](a-tokengroupsnogcacceptable.md)                         | Falsch     | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/>                                                                       |
| [**unixUserPassword**](a-unixuserpassword.md)                                               | Falsch     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**User-Cert**](a-usercert.md)                                                              | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**Benutzerkennwort**](a-userpassword.md)                                                      | Falsch     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**User-SMIME-Certificate**](a-usersmimecertificate.md)                                     | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |
| [**USN-Changed**](a-usnchanged.md)                                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**VON USN erstellt**](a-usncreated.md)                                                          | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**USN-Intersite**](a-usnintersite.md)                                                      | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                                  | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**USN-Quelle**](a-usnsource.md)                                                            | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Wbem-Path**](a-wbempath.md)                                                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Bekannte Objekte**](a-wellknownobjects.md)                                             | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Wenn geändert**](a-whenchanged.md)                                                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**Wenn erstellt**](a-whencreated.md)                                                        | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**WWW-Homepage**](a-wwwhomepage.md)                                                       | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**WWW-Page-Other**](a-url.md)                                                              | Falsch     | [**Nach oben**](c-top.md)<br/>                                                                                                    |
| [**X509-Cert**](a-usercertificate.md)                                                       | Falsch     | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/>                                                                               |



## <a name="windows-server-2012-extended-rights"></a>Windows Server 2012 Erweiterte Rechte

Diese Klasse enthält die folgenden erweiterten Rechte für Windows Server 2012:



| Allgemeiner Name                  |
|------------------------------|
| [**Senden an**](r-send-to.md) |



## <a name="windows-server-2012-validated-writes"></a>Windows Server 2012 Überprüfte Schreibvorgänge

Diese Klasse enthält die folgenden überprüften Schreibvorgänge für Windows Server 2012:



| Allgemeiner Name                                  |
|----------------------------------------------|
| [**Selbstmitgliedschaft**](r-self-membership.md) |



## <a name="windows-server-2012-property-sets"></a>Windows Server 2012 Eigenschaftensätze

Diese Klasse enthält die folgenden Eigenschaftensätze für Windows Server 2012:



| Allgemeiner Name                                      |
|--------------------------------------------------|
| [**E-Mail-Informationen**](r-email-information.md) |



 

 





