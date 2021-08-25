---
title: ms-DS-Resource-Properties-Klasse
description: Ein Container dieser Klasse kann Ressourceneigenschaften enthalten.
ms.assetid: 4c29de10-8218-406e-8f5a-5e2edb341a85
ms.tgt_platform: multiple
keywords:
- MS-DS-Resource-Properties-Klasse AD-Schema
- msDS-ResourceProperties-Klasse AD-Schema
topic_type:
- apiref
api_name:
- ms-DS-Resource-Properties
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b38ea5c0c158e63635cedf4928385c437e4153d28cce61cf9f69168fb2c309d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119879900"
---
# <a name="ms-ds-resource-properties-class"></a>ms-DS-Resource-Properties-Klasse

Ein Container dieser Klasse kann Ressourceneigenschaften enthalten.



| Eingabe | Wert |
|-------------------|--------------------------------------|
| CN                | ms-DS-Resource-Properties            |
| Ldap-Anzeigename | msDS-ResourceProperties              |
| Aktualisieren von Berechtigungen  | \-                                   |
| Updatehäufigkeit  | \-                                   |
| Schema-ID-GUID    | 7a4a4584-b350-478f-acd6-b4b852d82cc0 |



## <a name="implementations"></a>Implementierungen

-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2012"></a>Windows Server 2012

-   [Attribute](#windows-server-2012-attributes)



| Eingabe | Wert |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Falsch                                                                                        |
| Object-Category             | 1                                                                                            |
| Default-Object-Category     | \-                                                                                           |
| Governs-Id                  | 1.2.840.113556.1.5.271                                                                       |
| Default-Hiding-Value        | 1                                                                                            |
| Rdn-Att-Id                  | [**Allgemeiner Name**](a-cn.md)<br/>                                                       |
| Unterklasse von                 | [**Nach oben**](c-top.md)<br/>                                                              |
| Mögliche Übergeordnete          | [**Container**](c-container.md)                                                             |
| Zusätzlich           | \-                                                                                           |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                 |
| Standardsicherheitsdeskriptor | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; EA)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;;; AU) |
| System-Flags                | 0x00000010                                                                                   |



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
| [**DSA-Signature**](a-dsasignature.md)                                                      | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**DS-Core-Propagierungsdaten**](a-dscorepropagationdata.md)                                  | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Erweiterungsname**](a-extensionname.md)                                                    | Falsch     | [**Nach oben**](c-top.md)<br/> |
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
| [**Last-Known-Parent**](a-lastknownparent.md)                                               | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Verwaltete Objekte**](a-managedobjects.md)                                                  | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Mastered-By**](a-masteredby.md)                                                          | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Modify-Time-Stamp**](a-modifytimestamp.md)                                               | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                                  | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                                  | Falsch     | [**Nach oben**](c-top.md)<br/> |
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
| [**Teilattributlöschungsliste**](a-partialattributedeletionlist.md)                    | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Teilattributsatz**](a-partialattributeset.md)                                       | Falsch     | [**Nach oben**](c-top.md)<br/> |
| [**Mögliche Hindernisse**](a-possibleinferiors.md)                                            | Falsch     | [**Nach oben**](c-top.md)<br/> |
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



 

 





