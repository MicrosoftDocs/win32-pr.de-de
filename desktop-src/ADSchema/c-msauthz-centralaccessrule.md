---
title: ms-Sollhz-Central-Access-Rule-Klasse
description: Eine Klasse, die zentrale Zugriffsregeln definiert, die zum Erstellen einer zentralen Zugriffsrichtlinie verwendet werden.
ms.assetid: 5831179c-c6ae-4980-b0f5-538faa190b60
ms.tgt_platform: multiple
keywords:
- ms-Sollhz-Central-Access-Rule-Klasse AD-Schema
- msAuthz-CentralAccessRule-Klasse AD-Schema
topic_type:
- apiref
api_name:
- ms-Authz-Central-Access-Rule
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bd7b0f7ca0d649d844de49ac61d86e22a4286d990907248c99112b797d81ef7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119323710"
---
# <a name="ms-authz-central-access-rule-class"></a>ms-Sollhz-Central-Access-Rule-Klasse

Eine Klasse, die zentrale Zugriffsregeln definiert, die zum Erstellen einer zentralen Zugriffsrichtlinie verwendet werden.



| Eingabe | Wert |
|-------------------|--------------------------------------|
| CN                | ms-Takthz-Central-Access-Rule         |
| Ldap-Anzeigename | msAuthz-CentralAccessRule            |
| Aktualisieren von Berechtigungen  | \-                                   |
| Updatehäufigkeit  | \-                                   |
| Schema-Id-Guid    | 5b4a06dc-251c-4edb-8813-0bdd71327226 |



## <a name="implementations"></a>Implementierungen

-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2012"></a>Windows Server 2012

-   [Attribute](#windows-server-2012-attributes)



| Eingabe | Wert |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | False                                                                                        |
| Object-Category             | 1                                                                                            |
| Default-Object-Category     | \-                                                                                           |
| Governs-Id                  | 1.2.840.113556.1.4.2163                                                                      |
| Default-Hiding-Value        | 0                                                                                            |
| Rdn-Att-Id                  | \-                                                                                           |
| Unterklasse von                 | [**Nach oben**](c-top.md)<br/>                                                              |
| Mögliche Vorgesetzte          | [**ms-Takthz-Central-Access-Rules**](c-msauthz-centralaccessrules.md)                        |
| Zusätzlich           | \-                                                                                           |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                 |
| Standardsicherheitsdeskriptor | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; EA)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;;; AU) |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2012-attributes"></a>Windows Server 2012 Attribute

Diese Klasse enthält die folgenden Attribute für Windows Server 2012:



| attribute                                                                                    | Obligatorisch. | Abgeleitet von                     |
|----------------------------------------------------------------------------------------------|-----------|----------------------------------|
| [**Admin-Description**](a-admindescription.md)                                              | False     | [**Nach oben**](c-top.md)<br/>  |
| [**Administratoranzeigename**](a-admindisplayname.md)                                             | False     | [**Nach oben**](c-top.md)<br/>  |
| [**Allowed-Attributes**](a-allowedattributes.md)                                            | False     | [**Nach oben**](c-top.md)<br/>  |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)                         | False     | [**Nach oben**](c-top.md)<br/>  |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                                       | False     | [**Nach oben**](c-top.md)<br/>  |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)                    | False     | [**Nach oben**](c-top.md)<br/>  |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                                | False     | [**Nach oben**](c-top.md)<br/>  |
| [**Kanonischer Name**](a-canonicalname.md)                                                    | False     | [**Nach oben**](c-top.md)<br/>  |
| [**Common-Name**](a-cn.md)                                                                  | False     | [**Nach oben**](c-top.md)<br/>  |
| [**Create-Time-Stamp**](a-createtimestamp.md)                                               | False     | [**Nach oben**](c-top.md)<br/>  |
| [**Beschreibung**](a-description.md)                                                         | False     | [**Nach oben**](c-top.md)<br/>  |
| [**Anzeigename**](a-displayname.md)                                                        | False     | [**Nach oben**](c-top.md)<br/>  |
| [**Display-Name-Printable**](a-displaynameprintable.md)                                     | False     | [**Nach oben**](c-top.md)<br/>  |
| [**DSA-Signature**](a-dsasignature.md)                                                      | False     | [**Nach oben**](c-top.md)<br/>  |
| [**DS-Core-Propagierungsdaten**](a-dscorepropagationdata.md)                                  | False     | [**Nach oben**](c-top.md)<br/>  |
| [**Aktiviert**](a-enabled.md)                                                                 | False     | **ms-Authz-Central-Access-Rule** |
| [**Erweiterungsname**](a-extensionname.md)                                                    | False     | [**Nach oben**](c-top.md)<br/>  |
| [**Flaggen**](a-flags.md)                                                                     | False     | [**Nach oben**](c-top.md)<br/>  |
| [**From-Entry**](a-fromentry.md)                                                            | False     | [**Nach oben**](c-top.md)<br/>  |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)                                | False     | [**Nach oben**](c-top.md)<br/>  |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                                    | False     | [**Nach oben**](c-top.md)<br/>  |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                                   | False     | [**Nach oben**](c-top.md)<br/>  |
| [**Instanztyp**](a-instancetype.md)                                                      | True      | [**Nach oben**](c-top.md)<br/>  |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                                | False     | [**Nach oben**](c-top.md)<br/>  |
| [**Is-Deleted**](a-isdeleted.md)                                                            | False     | [**Nach oben**](c-top.md)<br/>  |
| [**Is-Member-of-DL**](a-memberof.md)                                                        | False     | [**Nach oben**](c-top.md)<br/>  |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                                           | False     | [**Nach oben**](c-top.md)<br/>  |
| [**Wird wiederverwendet**](a-isrecycled.md)                                                          | False     | [**Nach oben**](c-top.md)<br/>  |
| [**Last-Known-Parent**](a-lastknownparent.md)                                               | False     | [**Nach oben**](c-top.md)<br/>  |
| [**Verwaltete Objekte**](a-managedobjects.md)                                                  | False     | [**Nach oben**](c-top.md)<br/>  |
| [**Mastered-By**](a-masteredby.md)                                                          | False     | [**Nach oben**](c-top.md)<br/>  |
| [**Modify-Time-Stamp**](a-modifytimestamp.md)                                               | False     | [**Nach oben**](c-top.md)<br/>  |
| [**ms-Authz-Effective-Security-Policy**](a-msauthz-effectivesecuritypolicy.md)              | False     | **ms-Authz-Central-Access-Rule** |
| [**ms-Autorehz-Last-Effective-Security-Policy**](a-msauthz-lasteffectivesecuritypolicy.md)     | False     | **ms-Authz-Central-Access-Rule** |
| [**ms-Authz-Proposed-Security-Policy**](a-msauthz-proposedsecuritypolicy.md)                | False     | **ms-Authz-Central-Access-Rule** |
| [**ms-Authz-Resource-Condition**](a-msauthz-resourcecondition.md)                           | False     | **ms-Authz-Central-Access-Rule** |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                                  | False     | [**Nach oben**](c-top.md)<br/>  |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                                  | False     | [**Nach oben**](c-top.md)<br/>  |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)                          | False     | [**Nach oben**](c-top.md)<br/>  |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                              | False     | [**Nach oben**](c-top.md)<br/>  |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md)                  | False     | [**Nach oben**](c-top.md)<br/>  |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md)               | False     | [**Nach oben**](c-top.md)<br/>  |
| [**ms-DS-Claim-Shares-Possible-Values-with-BL**](a-msds-claimsharespossiblevalueswithbl.md) | False     | [**Nach oben**](c-top.md)<br/>  |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)                       | False     | [**Nach oben**](c-top.md)<br/>  |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                                    | False     | [**Nach oben**](c-top.md)<br/>  |
| [**ms-DS-Enabled-Feature-BL**](a-msds-enabledfeaturebl.md)                                  | False     | [**Nach oben**](c-top.md)<br/>  |
| [**ms-DS-Host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)                         | False     | [**Nach oben**](c-top.md)<br/>  |
| [**ms-DS-Is-Domain-For**](a-msds-isdomainfor.md)                                            | False     | [**Nach oben**](c-top.md)<br/>  |
| [**ms-DS-is-full-replica-for**](a-msds-isfullreplicafor.md)                                 | False     | [**Nach oben**](c-top.md)<br/>  |
| [**ms-DS-is-partial-replica-for**](a-msds-ispartialreplicafor.md)                           | False     | [**Nach oben**](c-top.md)<br/>  |
| [**ms-DS-Is-Primary-Computer-For**](a-msds-isprimarycomputerfor.md)                         | False     | [**Nach oben**](c-top.md)<br/>  |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                                          | False     | [**Nach oben**](c-top.md)<br/>  |
| [**ms-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                                          | False     | [**Nach oben**](c-top.md)<br/>  |
| [**ms-DS-local-Effective-Deletion-Time**](a-msds-localeffectivedeletiontime.md)             | False     | [**Nach oben**](c-top.md)<br/>  |
| [**ms-DS-local-Effective-Recycle-Time**](a-msds-localeffectiverecycletime.md)               | False     | [**Nach oben**](c-top.md)<br/>  |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                                               | False     | [**Nach oben**](c-top.md)<br/>  |
| [**ms-DS-Members-for-Az-Role-BL**](a-msds-membersforazrolebl.md)                            | False     | [**Nach oben**](c-top.md)<br/>  |
| [**ms-DS-Members-of-Resource-Property-List-BL**](a-msds-membersofresourcepropertylistbl.md) | False     | [**Nach oben**](c-top.md)<br/>  |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                                        | False     | [**Nach oben**](c-top.md)<br/>  |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)                     | False     | [**Nach oben**](c-top.md)<br/>  |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)                   | False     | [**Nach oben**](c-top.md)<br/>  |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)                | False     | [**Nach oben**](c-top.md)<br/>  |
| [**ms-DS-NC-Type**](a-msds-nctype.md)                                                       | False     | [**Nach oben**](c-top.md)<br/>  |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                                          | False     | [**Nach oben**](c-top.md)<br/>  |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                                | False     | [**Nach oben**](c-top.md)<br/>  |
| [**ms-DS-OIDToGroup-Link-BL**](a-msds-oidtogrouplinkbl.md)                                  | False     | [**Nach oben**](c-top.md)<br/>  |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)                      | False     | [**Nach oben**](c-top.md)<br/>  |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)                      | False     | [**Nach oben**](c-top.md)<br/>  |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                                         | False     | [**Nach oben**](c-top.md)<br/>  |
| [**ms-DS-PSO-Applied**](a-msds-psoapplied.md)                                               | False     | [**Nach oben**](c-top.md)<br/>  |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)                       | False     | [**Nach oben**](c-top.md)<br/>  |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                               | False     | [**Nach oben**](c-top.md)<br/>  |
| [**ms-DS-Revealed-DSAs**](a-msds-revealeddsas.md)                                           | False     | [**Nach oben**](c-top.md)<br/>  |
| [**ms-DS-Revealed-List-BL**](a-msds-revealedlistbl.md)                                      | False     | [**Nach oben**](c-top.md)<br/>  |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)                                | False     | [**Nach oben**](c-top.md)<br/>  |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)                                | False     | [**Nach oben**](c-top.md)<br/>  |
| [**ms-DS-TDO-Egress-BL**](a-msds-tdoegressbl.md)                                            | False     | [**Nach oben**](c-top.md)<br/>  |
| [**ms-DS-TDO-Ingress-BL**](a-msds-tdoingressbl.md)                                          | False     | [**Nach oben**](c-top.md)<br/>  |
| [**ms-DS-Value-Type-Reference-BL**](a-msds-valuetypereferencebl.md)                         | False     | [**Nach oben**](c-top.md)<br/>  |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                                        | False     | [**Nach oben**](c-top.md)<br/>  |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                                   | False     | [**Nach oben**](c-top.md)<br/>  |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                                     | False     | [**Nach oben**](c-top.md)<br/>  |
| [**Non-Security-Member-BL**](a-nonsecuritymemberbl.md)                                      | False     | [**Nach oben**](c-top.md)<br/>  |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                                     | True      | [**Nach oben**](c-top.md)<br/>  |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                                 | False     | [**Nach oben**](c-top.md)<br/>  |
| [**Objektkategorie**](a-objectcategory.md)                                                  | True      | [**Nach oben**](c-top.md)<br/>  |
| [**Objektklasse**](a-objectclass.md)                                                        | True      | [**Nach oben**](c-top.md)<br/>  |
| [**Objekt-GUID**](a-objectguid.md)                                                          | False     | [**Nach oben**](c-top.md)<br/>  |
| [**Objektversion**](a-objectversion.md)                                                    | False     | [**Nach oben**](c-top.md)<br/>  |
| [**Andere bekannte Objekte**](a-otherwellknownobjects.md)                                  | False     | [**Nach oben**](c-top.md)<br/>  |
| [**Teilattributlöschungsliste**](a-partialattributedeletionlist.md)                    | False     | [**Nach oben**](c-top.md)<br/>  |
| [**Teilattributsatz**](a-partialattributeset.md)                                       | False     | [**Nach oben**](c-top.md)<br/>  |
| [**Mögliche Hindernisse**](a-possibleinferiors.md)                                            | False     | [**Nach oben**](c-top.md)<br/>  |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                                           | False     | [**Nach oben**](c-top.md)<br/>  |
| [**Proxyadressen**](a-proxyaddresses.md)                                                  | False     | [**Nach oben**](c-top.md)<br/>  |
| [**Query-Policy-BL**](a-querypolicybl.md)                                                   | False     | [**Nach oben**](c-top.md)<br/>  |
| [**Rdn**](a-name.md)                                                                        | False     | [**Nach oben**](c-top.md)<br/>  |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                                    | False     | [**Nach oben**](c-top.md)<br/>  |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                                         | False     | [**Nach oben**](c-top.md)<br/>  |
| [**Berichte**](a-directreports.md)                                                           | False     | [**Nach oben**](c-top.md)<br/>  |
| [**Reps-From**](a-repsfrom.md)                                                              | False     | [**Nach oben**](c-top.md)<br/>  |
| [**Reps-To**](a-repsto.md)                                                                  | False     | [**Nach oben**](c-top.md)<br/>  |
| [**Revision**](a-revision.md)                                                               | False     | [**Nach oben**](c-top.md)<br/>  |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                                           | False     | [**Nach oben**](c-top.md)<br/>  |
| [**Server-Reference-BL**](a-serverreferencebl.md)                                           | False     | [**Nach oben**](c-top.md)<br/>  |
| [**Nur in erweiterter Ansicht anzeigen**](a-showinadvancedviewonly.md)                               | False     | [**Nach oben**](c-top.md)<br/>  |
| [**Site-Object-BL**](a-siteobjectbl.md)                                                     | False     | [**Nach oben**](c-top.md)<br/>  |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                                   | False     | [**Nach oben**](c-top.md)<br/>  |
| [**Sub-Refs**](a-subrefs.md)                                                                | False     | [**Nach oben**](c-top.md)<br/>  |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                             | False     | [**Nach oben**](c-top.md)<br/>  |
| [**Systemflags**](a-systemflags.md)                                                        | False     | [**Nach oben**](c-top.md)<br/>  |
| [**USN geändert**](a-usnchanged.md)                                                          | False     | [**Nach oben**](c-top.md)<br/>  |
| [**USN-erstellt**](a-usncreated.md)                                                          | False     | [**Nach oben**](c-top.md)<br/>  |
| [**USN-DSA-last-obj-removed**](a-usndsalastobjremoved.md)                                   | False     | [**Nach oben**](c-top.md)<br/>  |
| [**USN-Intersite**](a-usnintersite.md)                                                      | False     | [**Nach oben**](c-top.md)<br/>  |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                                  | False     | [**Nach oben**](c-top.md)<br/>  |
| [**USN-Quelle**](a-usnsource.md)                                                            | False     | [**Nach oben**](c-top.md)<br/>  |
| [**Wbem-Pfad**](a-wbempath.md)                                                              | False     | [**Nach oben**](c-top.md)<br/>  |
| [**Bekannte Objekte**](a-wellknownobjects.md)                                             | False     | [**Nach oben**](c-top.md)<br/>  |
| [**Wenn geändert**](a-whenchanged.md)                                                        | False     | [**Nach oben**](c-top.md)<br/>  |
| [**Wenn erstellt**](a-whencreated.md)                                                        | False     | [**Nach oben**](c-top.md)<br/>  |
| [**WWW-Homepage**](a-wwwhomepage.md)                                                       | False     | [**Nach oben**](c-top.md)<br/>  |
| [**WWW-Page-Other**](a-url.md)                                                              | False     | [**Nach oben**](c-top.md)<br/>  |



 

 





