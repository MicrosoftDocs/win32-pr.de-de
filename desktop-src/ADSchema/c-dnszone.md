---
title: Dns-Zone-Klasse
description: Der Container für DNS-Knoten. Enthält Zonenmetadaten.
ms.assetid: ea8e6799-df9c-4c17-a5a2-ea3e5016e3ec
ms.tgt_platform: multiple
keywords:
- Dns-Zone Ad-Schema der Klasse
- DNSZone-Klasse AD-Schema
topic_type:
- apiref
api_name:
- Dns-Zone
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9846c8a7553b3091e87dfc596f2d6abd0a2dc81c87c63078fb65712d609e7707
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119324770"
---
# <a name="dns-zone-class"></a>Dns-Zone-Klasse

Der Container für DNS-Knoten. Enthält Zonenmetadaten.



| Eingabe | Wert |
|-------------------|--------------------------------------|
| CN                | Dns-Zone                             |
| Ldap-Anzeigename | dnsZone                              |
| Aktualisieren von Berechtigungen  | \-                                   |
| Updatehäufigkeit  | \-                                   |
| Schema-ID-GUID    | e0fa1e8b-9b45-11d0-afdd-00c04fd930c9 |



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
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falsch                                                                                                                                        |
| Object-Category             | 1                                                                                                                                            |
| Default-Object-Category     | \-                                                                                                                                           |
| Governs-Id                  | 1.2.840.113556.1.5.85                                                                                                                        |
| Default-Hiding-Value        | 1                                                                                                                                            |
| Rdn-Att-Id                  | [**Domänenkomponente**](a-dc.md)<br/>                                                                                                  |
| Unterklasse von                 | [**Nach oben**](c-top.md)<br/>                                                                                                              |
| Mögliche Übergeordnete          | [**Container**](c-container.md)                                                                                                             |
| Zusätzlich           | \-                                                                                                                                           |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                                                                 |
| Standardsicherheitsdeskriptor | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; ED)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; CC;;; AU)(A;; RPLCLORC;;; WD) |
| System-Flags                | 0x00000010                                                                                                                                   |



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
| [**Kanonischer Name**](a-canonicalname.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Allgemeiner Name**](a-cn.md)                                               | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Erstellen eines Zeitstempels**](a-createtimestamp.md)                            | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Beschreibung**](a-description.md)                                      | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Anzeigename**](a-displayname.md)                                     | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Anzeigename– druckbar**](a-displaynameprintable.md)                  | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Dns-Allow-Dynamic**](a-dnsallowdynamic.md)                            | Falsch     | **Dns-Zone**                    |
| [**Dns-Allow-XFR**](a-dnsallowxfr.md)                                    | Falsch     | **DNS-Zone**                    |
| [**Dns-Notify-Secondaries**](a-dnsnotifysecondaries.md)                  | Falsch     | **DNS-Zone**                    |
| [**DNS-Eigenschaft**](a-dnsproperty.md)                                     | Falsch     | **DNS-Zone**                    |
| [**Dns-Secure-Secondaries**](a-dnssecuresecondaries.md)                  | Falsch     | **DNS-Zone**                    |
| [**Domänenkomponente**](a-dc.md)                                          | Richtig      | **DNS-Zone**                    |
| [**DSA-Signature**](a-dsasignature.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**DS-Core-Propagierungsdaten**](a-dscorepropagationdata.md)               | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Extension-Name**](a-extensionname.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Flaggen**](a-flags.md)                                                  | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**From-Entry**](a-fromentry.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)             | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                 | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Instanztyp**](a-instancetype.md)                                   | Richtig      | [**Nach oben**](c-top.md)<br/> |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)             | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Is-Deleted**](a-isdeleted.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Is-Member-of-DL**](a-memberof.md)                                     | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                        | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Letztes bekanntes übergeordnetes Element**](a-lastknownparent.md)                            | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Verwaltet von**](a-managedby.md)                                         | Falsch     | **DNS-Zone**                    |
| [**Verwaltete Objekte**](a-managedobjects.md)                               | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Mastered By**](a-masteredby.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/> |
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
| [**Andere bekannte Objekte**](a-otherwellknownobjects.md)               | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Teilattributlöschungsliste**](a-partialattributedeletionlist.md) | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Teilattributsatz**](a-partialattributeset.md)                    | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Mögliche Hindernisse**](a-possibleinferiors.md)                         | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                        | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Proxyadressen**](a-proxyaddresses.md)                               | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Query-Policy-BL**](a-querypolicybl.md)                                | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Rdn**](a-name.md)                                                     | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                 | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                      | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Berichte**](a-directreports.md)                                        | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Reps-From**](a-repsfrom.md)                                           | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Reps-To**](a-repsto.md)                                               | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Revision**](a-revision.md)                                            | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                        | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Server-Reference-BL**](a-serverreferencebl.md)                        | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Nur in erweiterter Ansicht anzeigen**](a-showinadvancedviewonly.md)            | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Site-Object-BL**](a-siteobjectbl.md)                                  | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Sub-Refs**](a-subrefs.md)                                             | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                          | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Systemflags**](a-systemflags.md)                                     | Falsch     | [**Nach oben**](c-top.md)<br/> |
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



## <a name="windows-server-2003"></a>Windows Server 2003

-   [Attribute](#windows-server-2003-attributes)



| Eingabe | Wert |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falsch                                                                                                                                                                            |
| Object-Category             | 1                                                                                                                                                                                |
| Default-Object-Category     | \-                                                                                                                                                                               |
| Governs-Id                  | 1.2.840.113556.1.5.85                                                                                                                                                            |
| Default-Hiding-Value        | 1                                                                                                                                                                                |
| Rdn-Att-Id                  | [**Domänenkomponente**](a-dc.md)<br/>                                                                                                                                      |
| Unterklasse von                 | [**Nach oben**](c-top.md)<br/>                                                                                                                                                  |
| Mögliche Vorgesetzte          | [**Container**](c-container.md)                                                                                                                                                 |
| Zusätzlich           | \-                                                                                                                                                                               |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                                                                                                     |
| Standardsicherheitsdeskriptor | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; ED)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; CC;;;; AU)(A;; RPLCLORC;;; WD)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; CO) |
| System-Flags                | 0x00000010                                                                                                                                                                       |



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
| [**Kanonischer Name**](a-canonicalname.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Common-Name**](a-cn.md)                                                 | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Create-Time-Stamp**](a-createtimestamp.md)                              | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Beschreibung**](a-description.md)                                        | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Anzeigename**](a-displayname.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Display-Name-Printable**](a-displaynameprintable.md)                    | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Dns-Allow-Dynamic**](a-dnsallowdynamic.md)                              | Falsch     | **DNS-Zone**                    |
| [**Dns-Allow-XFR**](a-dnsallowxfr.md)                                      | Falsch     | **DNS-Zone**                    |
| [**Dns-Notify-Secondaries**](a-dnsnotifysecondaries.md)                    | Falsch     | **DNS-Zone**                    |
| [**DNS-Eigenschaft**](a-dnsproperty.md)                                       | Falsch     | **DNS-Zone**                    |
| [**Dns-Secure-Secondaries**](a-dnssecuresecondaries.md)                    | Falsch     | **DNS-Zone**                    |
| [**Domänenkomponente**](a-dc.md)                                            | Richtig      | **DNS-Zone**                    |
| [**DSA-Signature**](a-dsasignature.md)                                     | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**DS-Core-Propagierungsdaten**](a-dscorepropagationdata.md)                 | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Extension-Name**](a-extensionname.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Flaggen**](a-flags.md)                                                    | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**From-Entry**](a-fromentry.md)                                           | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)               | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                   | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                  | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Instanztyp**](a-instancetype.md)                                     | Richtig      | [**Nach oben**](c-top.md)<br/> |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)               | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Is-Deleted**](a-isdeleted.md)                                           | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Is-Member-of-DL**](a-memberof.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                          | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Letztes bekanntes übergeordnetes Element**](a-lastknownparent.md)                              | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Verwaltet von**](a-managedby.md)                                           | Falsch     | **DNS-Zone**                    |
| [**Verwaltete Objekte**](a-managedobjects.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Mastered By**](a-masteredby.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Modify-Time-Stamp**](a-modifytimestamp.md)                              | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                 | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md) | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)      | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                              | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Members-For-Az-Role-BL**](a-msds-membersforazrolebl.md)           | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                       | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)    | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)  | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                         | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)               | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)     | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)     | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)      | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)              | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)               | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)               | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                    | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Non-Security-Member-BL**](a-nonsecuritymemberbl.md)                     | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                    | Richtig      | [**Nach oben**](c-top.md)<br/> |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Objektkategorie**](a-objectcategory.md)                                 | Richtig      | [**Nach oben**](c-top.md)<br/> |
| [**Objektklasse**](a-objectclass.md)                                       | Richtig      | [**Nach oben**](c-top.md)<br/> |
| [**Objekt-GUID**](a-objectguid.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Objektversion**](a-objectversion.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Andere bekannte Objekte**](a-otherwellknownobjects.md)                 | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Teilattributlöschungsliste**](a-partialattributedeletionlist.md)   | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Teilattributsatz**](a-partialattributeset.md)                      | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Mögliche Hindernisse**](a-possibleinferiors.md)                           | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                          | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Proxyadressen**](a-proxyaddresses.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Query-Policy-BL**](a-querypolicybl.md)                                  | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Rdn**](a-name.md)                                                       | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                   | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                        | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Berichte**](a-directreports.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Reps-From**](a-repsfrom.md)                                             | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Reps-To**](a-repsto.md)                                                 | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Revision**](a-revision.md)                                              | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                          | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Server-Reference-BL**](a-serverreferencebl.md)                          | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Nur in erweiterter Ansicht anzeigen**](a-showinadvancedviewonly.md)              | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                  | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Sub-Refs**](a-subrefs.md)                                               | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Systemflags**](a-systemflags.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/> |
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



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2

-   [Attribute](#windows-server-2003-r2-attributes)



| Eingabe | Wert |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falsch                                                                                                                                                                            |
| Object-Category             | 1                                                                                                                                                                                |
| Default-Object-Category     | \-                                                                                                                                                                               |
| Governs-Id                  | 1.2.840.113556.1.5.85                                                                                                                                                            |
| Default-Hiding-Value        | 1                                                                                                                                                                                |
| Rdn-Att-Id                  | [**Domänenkomponente**](a-dc.md)<br/>                                                                                                                                      |
| Unterklasse von                 | [**Nach oben**](c-top.md)<br/>                                                                                                                                                  |
| Mögliche Übergeordnete          | [**Container**](c-container.md)                                                                                                                                                 |
| Zusätzlich           | \-                                                                                                                                                                               |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                                                                                                     |
| Standardsicherheitsdeskriptor | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; ED)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; CC;;; AU)(A;; RPLCLORC;;; WD)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; CO) |
| System-Flags                | 0x00000010                                                                                                                                                                       |



## <a name="windows-server-2003-r2-attributes"></a>Windows Server 2003 R2-Attribute

Diese Klasse enthält die folgenden Attribute für Windows Server 2003 R2:



| attribute                                                                   | Obligatorisch. | Abgeleitet von                    |
|-----------------------------------------------------------------------------|-----------|---------------------------------|
| [**Administratorbeschreibung**](a-admindescription.md)                             | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Admin-Display-Name**](a-admindisplayname.md)                            | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Allowed-Attributes**](a-allowedattributes.md)                           | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)        | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                      | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)   | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)               | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Kanonischer Name**](a-canonicalname.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Allgemeiner Name**](a-cn.md)                                                 | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Erstellen eines Zeitstempels**](a-createtimestamp.md)                              | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Beschreibung**](a-description.md)                                        | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Anzeigename**](a-displayname.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Anzeigename– druckbar**](a-displaynameprintable.md)                    | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Dns-Allow-Dynamic**](a-dnsallowdynamic.md)                              | Falsch     | **Dns-Zone**                    |
| [**Dns-Allow-XFR**](a-dnsallowxfr.md)                                      | Falsch     | **Dns-Zone**                    |
| [**Dns-Notify-Secondaries**](a-dnsnotifysecondaries.md)                    | Falsch     | **Dns-Zone**                    |
| [**DNS-Eigenschaft**](a-dnsproperty.md)                                       | Falsch     | **Dns-Zone**                    |
| [**Dns-Secure-Secondaries**](a-dnssecuresecondaries.md)                    | Falsch     | **Dns-Zone**                    |
| [**Domänenkomponente**](a-dc.md)                                            | Richtig      | **Dns-Zone**                    |
| [**DSA-Signature**](a-dsasignature.md)                                     | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**DS-Core-Propagierungsdaten**](a-dscorepropagationdata.md)                 | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Erweiterungsname**](a-extensionname.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Flaggen**](a-flags.md)                                                    | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**From-Entry**](a-fromentry.md)                                           | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)               | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                   | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                  | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Instanztyp**](a-instancetype.md)                                     | Richtig      | [**Nach oben**](c-top.md)<br/> |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)               | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Is-Deleted**](a-isdeleted.md)                                           | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Is-Member-of-DL**](a-memberof.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                          | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Last-Known-Parent**](a-lastknownparent.md)                              | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Verwaltet von**](a-managedby.md)                                           | Falsch     | **Dns-Zone**                    |
| [**Verwaltete Objekte**](a-managedobjects.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Mastered-By**](a-masteredby.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Modify-Time-Stamp**](a-modifytimestamp.md)                              | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                 | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/> |
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
| [**Andere bekannte Objekte**](a-otherwellknownobjects.md)                 | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Teilattributlöschungsliste**](a-partialattributedeletionlist.md)   | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Teilattributsatz**](a-partialattributeset.md)                      | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Mögliche Hindernisse**](a-possibleinferiors.md)                           | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                          | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Proxyadressen**](a-proxyaddresses.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Query-Policy-BL**](a-querypolicybl.md)                                  | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Rdn**](a-name.md)                                                       | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                   | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                        | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Berichte**](a-directreports.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Reps-From**](a-repsfrom.md)                                             | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Reps-To**](a-repsto.md)                                                 | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Revision**](a-revision.md)                                              | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                          | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Server-Reference-BL**](a-serverreferencebl.md)                          | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)              | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                  | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Sub-Refs**](a-subrefs.md)                                               | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Systemflags**](a-systemflags.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**USN-Changed**](a-usnchanged.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**VON USN erstellt**](a-usncreated.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                  | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**USN-Intersite**](a-usnintersite.md)                                     | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**USN-Quelle**](a-usnsource.md)                                           | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Wbem-Path**](a-wbempath.md)                                             | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Bekannte Objekte**](a-wellknownobjects.md)                            | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Wenn geändert**](a-whenchanged.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Wenn erstellt**](a-whencreated.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**WWW-Homepage**](a-wwwhomepage.md)                                      | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**WWW-Page-Other**](a-url.md)                                             | Falsch     | [**Nach oben**](c-top.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008

-   [Attribute](#windows-server-2008-attributes)



| Eingabe | Wert |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falsch                                                                                                                                                                            |
| Object-Category             | 1                                                                                                                                                                                |
| Default-Object-Category     | \-                                                                                                                                                                               |
| Governs-Id                  | 1.2.840.113556.1.5.85                                                                                                                                                            |
| Default-Hiding-Value        | 1                                                                                                                                                                                |
| Rdn-Att-Id                  | [**Domänenkomponente**](a-dc.md)<br/>                                                                                                                                      |
| Unterklasse von                 | [**Nach oben**](c-top.md)<br/>                                                                                                                                                  |
| Mögliche Vorgesetzte          | [**Container**](c-container.md)                                                                                                                                                 |
| Zusätzlich           | \-                                                                                                                                                                               |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                                                                                                     |
| Standardsicherheitsdeskriptor | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; ED)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; CC;;;; AU)(A;; RPLCLORC;;; WD)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; CO) |
| System-Flags                | 0x00000010                                                                                                                                                                       |



## <a name="windows-server-2008-attributes"></a>Windows Server 2008-Attribute

Diese Klasse enthält die folgenden Attribute für Windows Server 2008:



| attribute                                                                      | Obligatorisch. | Abgeleitet von                    |
|--------------------------------------------------------------------------------|-----------|---------------------------------|
| [**Admin-Description**](a-admindescription.md)                                | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Administratoranzeigename**](a-admindisplayname.md)                               | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Allowed-Attributes**](a-allowedattributes.md)                              | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)           | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                         | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)      | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                  | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Kanonischer Name**](a-canonicalname.md)                                      | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Allgemeiner Name**](a-cn.md)                                                    | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Erstellen eines Zeitstempels**](a-createtimestamp.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Beschreibung**](a-description.md)                                           | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Anzeigename**](a-displayname.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Anzeigename– druckbar**](a-displaynameprintable.md)                       | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Dns-Allow-Dynamic**](a-dnsallowdynamic.md)                                 | Falsch     | **Dns-Zone**                    |
| [**Dns-Allow-XFR**](a-dnsallowxfr.md)                                         | Falsch     | **Dns-Zone**                    |
| [**Dns-Notify-Secondaries**](a-dnsnotifysecondaries.md)                       | Falsch     | **Dns-Zone**                    |
| [**DNS-Eigenschaft**](a-dnsproperty.md)                                          | Falsch     | **Dns-Zone**                    |
| [**Dns-Secure-Secondaries**](a-dnssecuresecondaries.md)                       | Falsch     | **Dns-Zone**                    |
| [**Domänenkomponente**](a-dc.md)                                               | Richtig      | **Dns-Zone**                    |
| [**DSA-Signature**](a-dsasignature.md)                                        | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**DS-Core-Propagierungsdaten**](a-dscorepropagationdata.md)                    | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Erweiterungsname**](a-extensionname.md)                                      | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Flaggen**](a-flags.md)                                                       | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**From-Entry**](a-fromentry.md)                                              | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)                  | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                      | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                     | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Instanztyp**](a-instancetype.md)                                        | Richtig      | [**Nach oben**](c-top.md)<br/> |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                  | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Is-Deleted**](a-isdeleted.md)                                              | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Is-Member-of-DL**](a-memberof.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                             | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Last-Known-Parent**](a-lastknownparent.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Verwaltet von**](a-managedby.md)                                              | Falsch     | **Dns-Zone**                    |
| [**Verwaltete Objekte**](a-managedobjects.md)                                    | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Mastered-By**](a-masteredby.md)                                            | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Modify-Time-Stamp**](a-modifytimestamp.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                    | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                    | Falsch     | [**Nach oben**](c-top.md)<br/> |
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
| [**Andere bekannte Objekte**](a-otherwellknownobjects.md)                    | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)      | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                         | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Mögliche 100000000000**](a-possibleinferiors.md)                              | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                             | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Proxyadressen**](a-proxyaddresses.md)                                    | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Query-Policy-BL**](a-querypolicybl.md)                                     | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Rdn**](a-name.md)                                                          | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                      | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                           | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Berichte**](a-directreports.md)                                             | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Reps-From**](a-repsfrom.md)                                                | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Reps-To**](a-repsto.md)                                                    | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Revision**](a-revision.md)                                                 | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                             | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Server-Reference-BL**](a-serverreferencebl.md)                             | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)                 | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Site-Object-BL**](a-siteobjectbl.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                     | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Sub-Refs**](a-subrefs.md)                                                  | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                               | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Systemflags**](a-systemflags.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**USN-Changed**](a-usnchanged.md)                                            | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**VON USN erstellt**](a-usncreated.md)                                            | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                     | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**USN-Intersite**](a-usnintersite.md)                                        | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                    | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**USN-Quelle**](a-usnsource.md)                                              | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Wbem-Path**](a-wbempath.md)                                                | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Bekannte Objekte**](a-wellknownobjects.md)                               | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Wenn geändert**](a-whenchanged.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Wenn erstellt**](a-whencreated.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**WWW-Homepage**](a-wwwhomepage.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**WWW-Page-Other**](a-url.md)                                                | Falsch     | [**Nach oben**](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2

-   [Attribute](#windows-server-2008-r2-attributes)



| Eingabe | Wert |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falsch                                                                                                                                                                            |
| Object-Category             | 1                                                                                                                                                                                |
| Default-Object-Category     | \-                                                                                                                                                                               |
| Governs-Id                  | 1.2.840.113556.1.5.85                                                                                                                                                            |
| Default-Hiding-Value        | 1                                                                                                                                                                                |
| Rdn-Att-Id                  | [**Domänenkomponente**](a-dc.md)<br/>                                                                                                                                      |
| Unterklasse von                 | [**Nach oben**](c-top.md)<br/>                                                                                                                                                  |
| Mögliche Vorgesetzte          | [**Container**](c-container.md)                                                                                                                                                 |
| Zusätzlich           | \-                                                                                                                                                                               |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                                                                                                     |
| Standardsicherheitsdeskriptor | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; ED)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; CC;;;; AU)(A;; RPLCLORC;;; WD)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; CO) |
| System-Flags                | 0x00000010                                                                                                                                                                       |



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
| [**Kanonischer Name**](a-canonicalname.md)                                        | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Common-Name**](a-cn.md)                                                      | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Create-Time-Stamp**](a-createtimestamp.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Beschreibung**](a-description.md)                                             | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Anzeigename**](a-displayname.md)                                            | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Display-Name-Printable**](a-displaynameprintable.md)                         | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Dns-Allow-Dynamic**](a-dnsallowdynamic.md)                                   | Falsch     | **DNS-Zone**                    |
| [**Dns-Allow-XFR**](a-dnsallowxfr.md)                                           | Falsch     | **DNS-Zone**                    |
| [**Dns-Notify-Secondaries**](a-dnsnotifysecondaries.md)                         | Falsch     | **DNS-Zone**                    |
| [**DNS-Eigenschaft**](a-dnsproperty.md)                                            | Falsch     | **DNS-Zone**                    |
| [**Dns-Secure-Secondaries**](a-dnssecuresecondaries.md)                         | Falsch     | **DNS-Zone**                    |
| [**Domänenkomponente**](a-dc.md)                                                 | Richtig      | **DNS-Zone**                    |
| [**DSA-Signature**](a-dsasignature.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**DS-Core-Propagierungsdaten**](a-dscorepropagationdata.md)                      | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Extension-Name**](a-extensionname.md)                                        | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Flaggen**](a-flags.md)                                                         | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**From-Entry**](a-fromentry.md)                                                | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)                    | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                        | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Instanztyp**](a-instancetype.md)                                          | Richtig      | [**Nach oben**](c-top.md)<br/> |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                    | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Is-Deleted**](a-isdeleted.md)                                                | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Is-Member-of-DL**](a-memberof.md)                                            | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                               | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Wird wiederverwendet**](a-isrecycled.md)                                              | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Letztes bekanntes übergeordnetes Element**](a-lastknownparent.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Verwaltet von**](a-managedby.md)                                                | Falsch     | **DNS-Zone**                    |
| [**Verwaltete Objekte**](a-managedobjects.md)                                      | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Mastered By**](a-masteredby.md)                                              | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Modify-Time-Stamp**](a-modifytimestamp.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                      | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                      | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)              | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                  | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md)      | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md)   | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)           | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                        | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Enabled-Feature-BL**](a-msds-enabledfeaturebl.md)                      | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)             | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-is-Domain-for**](a-msds-isdomainfor.md)                                | Falsch     | [**Nach oben**](c-top.md)<br/> |
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
| [**ms-DS-Operations-for-Az-Role-BL**](a-msds-operationsforazrolebl.md)          | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Operations-for-Az-Task-BL**](a-msds-operationsforaztaskbl.md)          | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                             | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-PSO-Applied**](a-msds-psoapplied.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)           | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                   | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Revealed-DSAs**](a-msds-revealeddsas.md)                               | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Revealed-List-BL**](a-msds-revealedlistbl.md)                          | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Tasks-for-Az-Role-BL**](a-msds-tasksforazrolebl.md)                    | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Tasks-for-Az-Task-BL**](a-msds-tasksforaztaskbl.md)                    | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                            | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                       | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Non-Security-Member-BL**](a-nonsecuritymemberbl.md)                          | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                         | Richtig      | [**Nach oben**](c-top.md)<br/> |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                     | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Objektkategorie**](a-objectcategory.md)                                      | Richtig      | [**Nach oben**](c-top.md)<br/> |
| [**Objektklasse**](a-objectclass.md)                                            | Richtig      | [**Nach oben**](c-top.md)<br/> |
| [**Objekt-GUID**](a-objectguid.md)                                              | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Object-Version**](a-objectversion.md)                                        | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Andere bekannte Objekte**](a-otherwellknownobjects.md)                      | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)        | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                           | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Mögliche 100000000000**](a-possibleinferiors.md)                                | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                               | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Proxyadressen**](a-proxyaddresses.md)                                      | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Query-Policy-BL**](a-querypolicybl.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Rdn**](a-name.md)                                                            | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                        | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                             | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Berichte**](a-directreports.md)                                               | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Reps-From**](a-repsfrom.md)                                                  | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Reps-To**](a-repsto.md)                                                      | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Revision**](a-revision.md)                                                   | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                               | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Server-Reference-BL**](a-serverreferencebl.md)                               | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)                   | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Site-Object-BL**](a-siteobjectbl.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                       | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Sub-Refs**](a-subrefs.md)                                                    | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Systemflags**](a-systemflags.md)                                            | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**USN-Changed**](a-usnchanged.md)                                              | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**VON USN erstellt**](a-usncreated.md)                                              | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                       | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**USN-Intersite**](a-usnintersite.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                      | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**USN-Quelle**](a-usnsource.md)                                                | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Wbem-Path**](a-wbempath.md)                                                  | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Bekannte Objekte**](a-wellknownobjects.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Wenn geändert**](a-whenchanged.md)                                            | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Bei der Erstellung**](a-whencreated.md)                                            | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**WWW-Startseite**](a-wwwhomepage.md)                                           | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**WWW-Page-Other**](a-url.md)                                                  | Falsch     | [**Nach oben**](c-top.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012

-   [Attribute](#windows-server-2012-attributes)



| Eingabe | Wert |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falsch                                                                                                                                                                            |
| Object-Category             | 1                                                                                                                                                                                |
| Default-Object-Category     | \-                                                                                                                                                                               |
| Governs-Id                  | 1.2.840.113556.1.5.85                                                                                                                                                            |
| Default-Hiding-Value        | 1                                                                                                                                                                                |
| Rdn-Att-Id                  | [**Domänenkomponente**](a-dc.md)<br/>                                                                                                                                      |
| Unterklasse von                 | [**Nach oben**](c-top.md)<br/>                                                                                                                                                  |
| Mögliche Übergeordnete          | [**Container**](c-container.md)                                                                                                                                                 |
| Zusätzlich           | \-                                                                                                                                                                               |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                                                                                                     |
| Standardsicherheitsdeskriptor | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; ED)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; CC;;; AU)(A;; RPLCLORC;;; WD)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; CO) |
| System-Flags                | 0x00000010                                                                                                                                                                       |



## <a name="windows-server-2012-attributes"></a>Windows Server 2012 Attribute

Diese Klasse enthält die folgenden Attribute für Windows Server 2012:



| attribute                                                                                    | Obligatorisch. | Abgeleitet von                    |
|----------------------------------------------------------------------------------------------|-----------|---------------------------------|
| [**Administratorbeschreibung**](a-admindescription.md)                                              | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Admin-Display-Name**](a-admindisplayname.md)                                             | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Allowed-Attributes**](a-allowedattributes.md)                                            | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)                         | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)                    | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                                | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Kanonischer Name**](a-canonicalname.md)                                                    | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Allgemeiner Name**](a-cn.md)                                                                  | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Erstellen eines Zeitstempels**](a-createtimestamp.md)                                               | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Beschreibung**](a-description.md)                                                         | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Anzeigename**](a-displayname.md)                                                        | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Anzeigename– druckbar**](a-displaynameprintable.md)                                     | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Dns-Allow-Dynamic**](a-dnsallowdynamic.md)                                               | Falsch     | **Dns-Zone**                    |
| [**Dns-Allow-XFR**](a-dnsallowxfr.md)                                                       | Falsch     | **Dns-Zone**                    |
| [**Dns-Notify-Secondaries**](a-dnsnotifysecondaries.md)                                     | Falsch     | **Dns-Zone**                    |
| [**DNS-Eigenschaft**](a-dnsproperty.md)                                                        | Falsch     | **Dns-Zone**                    |
| [**Dns-Secure-Secondaries**](a-dnssecuresecondaries.md)                                     | Falsch     | **Dns-Zone**                    |
| [**Domänenkomponente**](a-dc.md)                                                             | Richtig      | **Dns-Zone**                    |
| [**DSA-Signature**](a-dsasignature.md)                                                      | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**DS-Core-Propagierungsdaten**](a-dscorepropagationdata.md)                                  | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Extension-Name**](a-extensionname.md)                                                    | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Flaggen**](a-flags.md)                                                                     | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**From-Entry**](a-fromentry.md)                                                            | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)                                | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                                    | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                                   | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Instanztyp**](a-instancetype.md)                                                      | Richtig      | [**Nach oben**](c-top.md)<br/> |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                                | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Is-Deleted**](a-isdeleted.md)                                                            | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Is-Member-of-DL**](a-memberof.md)                                                        | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                                           | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Wird wiederverwendet**](a-isrecycled.md)                                                          | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Letztes bekanntes übergeordnetes Element**](a-lastknownparent.md)                                               | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Verwaltet von**](a-managedby.md)                                                            | Falsch     | **DNS-Zone**                    |
| [**Verwaltete Objekte**](a-managedobjects.md)                                                  | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Mastered By**](a-masteredby.md)                                                          | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Modify-Time-Stamp**](a-modifytimestamp.md)                                               | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                                  | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                                  | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)                          | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                              | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DNS-DNSKEY-Records**](a-msdns-dnskeyrecords.md)                                       | Falsch     | **DNS-Zone**                    |
| [**ms-DNS-DNSKEY-Record-Set-TTL**](a-msdns-dnskeyrecordsetttl.md)                           | Falsch     | **DNS-Zone**                    |
| [**ms-DNS-DS-Record-Algorithms**](a-msdns-dsrecordalgorithms.md)                            | Falsch     | **DNS-Zone**                    |
| [**ms-DNS-DS-Record-Set-TTL**](a-msdns-dsrecordsetttl.md)                                   | Falsch     | **DNS-Zone**                    |
| [**ms-DNS-Is-Signed**](a-msdns-issigned.md)                                                 | Falsch     | **DNS-Zone**                    |
| [**ms-DNS-Maintain-Trust-Anchor**](a-msdns-maintaintrustanchor.md)                          | Falsch     | **DNS-Zone**                    |
| [**ms-DNS-NSEC3-Current-Salt**](a-msdns-nsec3currentsalt.md)                                | Falsch     | **DNS-Zone**                    |
| [**ms-DNS-NSEC3-Hash-Algorithm**](a-msdns-nsec3hashalgorithm.md)                            | Falsch     | **DNS-Zone**                    |
| [**ms-DNS-NSEC3-Iterations**](a-msdns-nsec3iterations.md)                                   | Falsch     | **DNS-Zone**                    |
| [**ms-DNS-NSEC3-OptOut**](a-msdns-nsec3optout.md)                                           | Falsch     | **DNS-Zone**                    |
| [**ms-DNS-NSEC3-Random-Salt-Length**](a-msdns-nsec3randomsaltlength.md)                     | Falsch     | **DNS-Zone**                    |
| [**ms-DNS-NSEC3-User-Salt**](a-msdns-nsec3usersalt.md)                                      | Falsch     | **DNS-Zone**                    |
| [**ms-DNS-Parent-Has-Secure-Delegation**](a-msdns-parenthassecuredelegation.md)             | Falsch     | **DNS-Zone**                    |
| [**ms-DNS-Propagation-Time**](a-msdns-propagationtime.md)                                   | Falsch     | **DNS-Zone**                    |
| [**ms-DNS-RFC5011-Key-Rollovers**](a-msdns-rfc5011keyrollovers.md)                          | Falsch     | **DNS-Zone**                    |
| [**ms-DNS-Secure-Delegation-Polling-Period**](a-msdns-securedelegationpollingperiod.md)     | Falsch     | **DNS-Zone**                    |
| [**ms-DNS-Signature-Inception-Offset**](a-msdns-signatureinceptionoffset.md)                | Falsch     | **DNS-Zone**                    |
| [**ms-DNS-Signing-Key-Descriptors**](a-msdns-signingkeydescriptors.md)                      | Falsch     | **DNS-Zone**                    |
| [**ms-DNS-Signing-Keys**](a-msdns-signingkeys.md)                                           | Falsch     | **DNS-Zone**                    |
| [**ms-DNS-Sign-With-NSEC3**](a-msdns-signwithnsec3.md)                                      | Falsch     | **DNS-Zone**                    |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md)                  | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md)               | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Claim-Shares-Possible-Values-With-BL**](a-msds-claimsharespossiblevalueswithbl.md) | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)                       | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                                    | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Enabled-Feature-BL**](a-msds-enabledfeaturebl.md)                                  | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)                         | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-is-Domain-for**](a-msds-isdomainfor.md)                                            | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-is-full-replica-for**](a-msds-isfullreplicafor.md)                                 | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-is-partial-replica-for**](a-msds-ispartialreplicafor.md)                           | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Is-Primary-Computer-for**](a-msds-isprimarycomputerfor.md)                         | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                                          | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-local-Effective-Deletion-Time**](a-msds-localeffectivedeletiontime.md)             | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-local-Effective-Recycle-Time**](a-msds-localeffectiverecycletime.md)               | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                                               | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Members-For-Az-Role-BL**](a-msds-membersforazrolebl.md)                            | Falsch     | [**Nach oben**](c-top.md)<br/> |
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
| [**Andere bekannte Objekte**](a-otherwellknownobjects.md)                                  | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)                    | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Mögliche 100000000000**](a-possibleinferiors.md)                                            | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                                           | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Proxyadressen**](a-proxyaddresses.md)                                                  | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Query-Policy-BL**](a-querypolicybl.md)                                                   | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Rdn**](a-name.md)                                                                        | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                                    | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                                         | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Berichte**](a-directreports.md)                                                           | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Reps-From**](a-repsfrom.md)                                                              | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Reps-To**](a-repsto.md)                                                                  | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Revision**](a-revision.md)                                                               | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                                           | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Server-Reference-BL**](a-serverreferencebl.md)                                           | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Nur in erweiterter Ansicht anzeigen**](a-showinadvancedviewonly.md)                               | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Site-Object-BL**](a-siteobjectbl.md)                                                     | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Sub-Refs**](a-subrefs.md)                                                                | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                             | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Systemflags**](a-systemflags.md)                                                        | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**USN geändert**](a-usnchanged.md)                                                          | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**USN-erstellt**](a-usncreated.md)                                                          | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**USN-DSA-last-obj-removed**](a-usndsalastobjremoved.md)                                   | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**USN-Intersite**](a-usnintersite.md)                                                      | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                                  | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**USN-Quelle**](a-usnsource.md)                                                            | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Wbem-Pfad**](a-wbempath.md)                                                              | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Bekannte Objekte**](a-wellknownobjects.md)                                             | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Bei Änderung**](a-whenchanged.md)                                                        | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Bei der Erstellung**](a-whencreated.md)                                                        | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**WWW-Startseite**](a-wwwhomepage.md)                                                       | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**WWW-Page-Other**](a-url.md)                                                              | Falsch     | [**Nach oben**](c-top.md)<br/> |



 

 





