---
title: ms-DS-BIND-Proxy-Klasse
description: Hilfsklasse zur Darstellung eines Bindungs Proxys in AD/am.
ms.assetid: de837926-9d40-41f6-8c56-c4e436fd66b6
ms.tgt_platform: multiple
keywords:
- AD-Schema der ms-DS-BIND-Proxy Klasse
- AD-Schema der msDS-BindProxy-Klasse
topic_type:
- apiref
api_name:
- ms-DS-Bind-Proxy
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db4fbb48080c83c3ea82b72c598e2a5a06037562
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744097"
---
# <a name="ms-ds-bind-proxy-class"></a>ms-DS-BIND-Proxy-Klasse

Hilfsklasse zur Darstellung eines Bindungs Proxys in AD/am. Der Bindungs Proxy verweist mithilfe seines objectSID-Attributs auf einen Windows-Sicherheits Prinzipal. Wenn ein Benutzer eine einfache Bindung mit einem BIND-Proxy-Objekt ausführt, wird die Bindung an den entsprechenden Windows-Prinzipal umgeleitet.



| Eingabe | Wert |
|-------------------|--------------------------------------|
| CN                | ms-DS-BIND-Proxy                     |
| LDAP-Display-Name | msDS-BindProxy                       |
| Berechtigung aktualisieren  | \-                                   |
| Aktualisierungshäufigkeit  | \-                                   |
| Schema-ID-GUID    | 717532ab-66e9-684d-a62b-8af1e3985e2f |



## <a name="implementations"></a>Implementierungen

-   [**Adam**](#adam-attributes)

## <a name="adam"></a>Adam

-   [Attribute](#adam-attributes)



| Eingabe | Wert |
|-----------------------------|---------------------------------|
| System-Only                 | False                           |
| Object-Category             | 3                               |
| Default-Object-Category     | \-                              |
| Governs-Id                  | 1.2.840.113556.1.5.245          |
| Standard-ausblenden-Wert        | 1                               |
| RDN-ATT-ID                  | \-                              |
| Unterklasse von                 | [**Nach oben**](c-top.md)<br/> |
| Mögliche Vorgesetzten          | \-                              |
| Zusätzlich           | \-                              |
| NT-Security-Descriptor      | o:Bag: schlecht: S:                    |
| Standard Sicherheits Beschreibung | \-                              |
| System-Flags                | 0x00000010                      |



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
| [**Kanonischer Name**](a-canonicalname.md)                                   | False     | [**Nach oben**](c-top.md)<br/> |
| [**Gemeinsamer Name**](a-cn.md)                                                 | False     | [**Nach oben**](c-top.md)<br/> |
| [**Create-Zeitstempel**](a-createtimestamp.md)                              | False     | [**Nach oben**](c-top.md)<br/> |
| [**Beschreibung**](a-description.md)                                        | False     | [**Nach oben**](c-top.md)<br/> |
| [**Anzeige Name**](a-displayname.md)                                       | False     | [**Nach oben**](c-top.md)<br/> |
| [**DSA-Signatur**](a-dsasignature.md)                                     | False     | [**Nach oben**](c-top.md)<br/> |
| [**DS-Core-propagierungs Daten**](a-dscorepropagationdata.md)                 | False     | [**Nach oben**](c-top.md)<br/> |
| [**Aus-Eintrag**](a-fromentry.md)                                           | False     | [**Nach oben**](c-top.md)<br/> |
| [**"F"-Rollen Besitzer**](a-fsmoroleowner.md)                                  | False     | [**Nach oben**](c-top.md)<br/> |
| [**Instanztyp**](a-instancetype.md)                                     | Richtig      | [**Nach oben**](c-top.md)<br/> |
| [**Is-critical-System-Object**](a-iscriticalsystemobject.md)               | False     | [**Nach oben**](c-top.md)<br/> |
| [**Ist-gelöscht**](a-isdeleted.md)                                           | False     | [**Nach oben**](c-top.md)<br/> |
| [**Is-Member-of-DL**](a-memberof.md)                                       | False     | [**Nach oben**](c-top.md)<br/> |
| [**Letztes-bekannt/übergeordnetes Element**](a-lastknownparent.md)                              | False     | [**Nach oben**](c-top.md)<br/> |
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
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                        | False     | **ms-DS-BIND-Proxy**            |
| [**ms-DS-repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)      | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)              | False     | [**Nach oben**](c-top.md)<br/> |
| [**ms-DS-Service-Account-BL**](a-msds-serviceaccountbl.md)                 | False     | [**Nach oben**](c-top.md)<br/> |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                    | Richtig      | [**Nach oben**](c-top.md)<br/> |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                | False     | [**Nach oben**](c-top.md)<br/> |
| [**Objekt-Kategorie**](a-objectcategory.md)                                 | Richtig      | [**Nach oben**](c-top.md)<br/> |
| [**Object-Klasse**](a-objectclass.md)                                       | Richtig      | [**Nach oben**](c-top.md)<br/> |
| [**Objekt-GUID**](a-objectguid.md)                                         | False     | [**Nach oben**](c-top.md)<br/> |
| [**Objekt-sid**](a-objectsid.md)                                           | Richtig      | **ms-DS-BIND-Proxy**            |
| [**Objekt-Version**](a-objectversion.md)                                   | False     | [**Nach oben**](c-top.md)<br/> |
| [**Andere-bekannte Objekte**](a-otherwellknownobjects.md)                 | False     | [**Nach oben**](c-top.md)<br/> |
| [**Partial-Attribute-löschen-List**](a-partialattributedeletionlist.md)   | False     | [**Nach oben**](c-top.md)<br/> |
| [**Partiell-Attribut Satz**](a-partialattributeset.md)                      | False     | [**Nach oben**](c-top.md)<br/> |
| [**Mögliche-minderwertig**](a-possibleinferiors.md)                           | False     | [**Nach oben**](c-top.md)<br/> |
| [**Proxy-Objekt Name**](a-proxiedobjectname.md)                          | False     | [**Nach oben**](c-top.md)<br/> |
| [**Proxy Adressen**](a-proxyaddresses.md)                                 | False     | [**Nach oben**](c-top.md)<br/> |
| [**Abfrage-Richtlinie-BL**](a-querypolicybl.md)                                  | False     | [**Nach oben**](c-top.md)<br/> |
| [**RDN**](a-name.md)                                                       | False     | [**Nach oben**](c-top.md)<br/> |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                   | False     | [**Nach oben**](c-top.md)<br/> |
| [**REPL-Update-Vector**](a-repluptodatevector.md)                        | False     | [**Nach oben**](c-top.md)<br/> |
| [**Reps-from**](a-repsfrom.md)                                             | False     | [**Nach oben**](c-top.md)<br/> |
| [**Reps-to**](a-repsto.md)                                                 | False     | [**Nach oben**](c-top.md)<br/> |
| [**Novel**](a-revision.md)                                              | False     | [**Nach oben**](c-top.md)<br/> |
| [**SD-Rechte**](a-sdrightseffective.md)                          | False     | [**Nach oben**](c-top.md)<br/> |
| [**Server-Reference-BL**](a-serverreferencebl.md)                          | False     | [**Nach oben**](c-top.md)<br/> |
| [**Anzeigen-in-Advanced-nur anzeigen**](a-showinadvancedviewonly.md)              | False     | [**Nach oben**](c-top.md)<br/> |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | False     | [**Nach oben**](c-top.md)<br/> |
| [**Struktur-Objekt-Klasse**](a-structuralobjectclass.md)                  | False     | [**Nach oben**](c-top.md)<br/> |
| [**Sub-Refs**](a-subrefs.md)                                               | False     | [**Nach oben**](c-top.md)<br/> |
| [**Subschemasubentry**](a-subschemasubentry.md)                            | False     | [**Nach oben**](c-top.md)<br/> |
| [**SystemFlags**](a-systemflags.md)                                       | False     | [**Nach oben**](c-top.md)<br/> |
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



 

 





