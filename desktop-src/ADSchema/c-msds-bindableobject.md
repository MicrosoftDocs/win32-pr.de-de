---
title: ms-DS-Bindable-Object-Klasse
description: Eine Hilfsklasse, die ein bindbares Objekt darstellt. Jede benutzerdefinierte Klasse, die eine Entität darstellt, die zum Binden an das Verzeichnis (d. h. ein Benutzer) verwendet werden kann, sollte diese Hilfsklasse einschließen.
ms.assetid: 181b3e2b-9442-4f11-9af7-4697491115f3
ms.tgt_platform: multiple
keywords:
- ms-DS-Bindable-Objektklasse AD-Schema
- AD-Schema der msDS-bindableobject-Klasse
topic_type:
- apiref
api_name:
- ms-DS-Bindable-Object
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: feb69036ad9cd33b8f0a60f5356192acbea8dd71
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103859528"
---
# <a name="ms-ds-bindable-object-class"></a>ms-DS-Bindable-Object-Klasse

Eine Hilfsklasse, die ein bindbares Objekt darstellt. Jede benutzerdefinierte Klasse, die eine Entität darstellt, die zum Binden an das Verzeichnis (d. h. ein Benutzer) verwendet werden kann, sollte diese Hilfsklasse einschließen.



| Eingabe | Wert |
|-------------------|--------------------------------------|
| CN                | ms-DS-Bindable-Objekt                |
| LDAP-Display-Name | msDS-bindableobject                  |
| Berechtigung aktualisieren  | \-                                   |
| Aktualisierungshäufigkeit  | \-                                   |
| Schema-ID-GUID    | 89f4a69f-4416-6b49-821d-6e3c4a0ff802 |



## <a name="implementations"></a>Implementierungen

-   [**Adam**](#adam-attributes)

## <a name="adam"></a>Adam

-   [Attribute](#adam-attributes)



| Eingabe | Wert |
|-----------------------------|--------------------------------------------------------------|
| System-Only                 | False                                                        |
| Object-Category             | 3                                                            |
| Default-Object-Category     | \-                                                           |
| Governs-Id                  | 1.2.840.113556.1.5.244                                       |
| Standard-ausblenden-Wert        | 1                                                            |
| RDN-ATT-ID                  | \-                                                           |
| Unterklasse von                 | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/> |
| Mögliche Vorgesetzten          | \-                                                           |
| Zusätzlich           | \-                                                           |
| NT-Security-Descriptor      | o:Bag: schlecht: S:                                                 |
| Standard Sicherheits Beschreibung | \-                                                           |
| System-Flags                | 0x00000010                                                   |



## <a name="adam-attributes"></a>Adam-Attribute

Diese Klasse enthält die folgenden Attribute für Adam:



| Attribut                                                                                      | Obligatorisch. | Abgeleitet von                                                                                 |
|------------------------------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------|
| [**Konto: läuft ab**](a-accountexpires.md)                                                    | False     | **ms-DS-Bindable-Objekt**                                                                    |
| [**Administrator: Beschreibung**](a-admindescription.md)                                                | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Administrator-Anzeige Name**](a-admindisplayname.md)                                               | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Zulässige Attribute**](a-allowedattributes.md)                                              | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Zulässige Attribute-gültig**](a-allowedattributeseffective.md)                           | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Zulässige, untergeordnete Klassen**](a-allowedchildclasses.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Zulässig-untergeordnete Klassen-gültig**](a-allowedchildclasseseffective.md)                      | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Ungültige Kenn Wort Zeit**](a-badpasswordtime.md)                                                 | False     | **ms-DS-Bindable-Objekt**                                                                    |
| [**Falsch-pwd-Anzahl**](a-badpwdcount.md)                                                         | False     | **ms-DS-Bindable-Objekt**                                                                    |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                                  | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Kanonischer Name**](a-canonicalname.md)                                                      | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Gemeinsamer Name**](a-cn.md)                                                                    | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Create-Zeitstempel**](a-createtimestamp.md)                                                 | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Beschreibung**](a-description.md)                                                           | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Anzeige Name**](a-displayname.md)                                                          | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**DSA-Signatur**](a-dsasignature.md)                                                        | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**DS-Core-propagierungs Daten**](a-dscorepropagationdata.md)                                    | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Aus-Eintrag**](a-fromentry.md)                                                              | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**"F"-Rollen Besitzer**](a-fsmoroleowner.md)                                                     | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Instanztyp**](a-instancetype.md)                                                        | Richtig      | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Is-critical-System-Object**](a-iscriticalsystemobject.md)                                  | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Ist-gelöscht**](a-isdeleted.md)                                                              | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Is-Member-of-DL**](a-memberof.md)                                                          | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Letztes-bekannt/übergeordnetes Element**](a-lastknownparent.md)                                                 | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Zeitstempel der letzten Anmeldung**](a-lastlogontimestamp.md)                                           | False     | **ms-DS-Bindable-Objekt**                                                                    |
| [**Sperr Zeit**](a-lockouttime.md)                                                          | False     | **ms-DS-Bindable-Objekt**                                                                    |
| [**Verwaltete Objekte**](a-managedobjects.md)                                                    | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Verwaltet von**](a-masteredby.md)                                                            | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Modify-Zeitstempel**](a-modifytimestamp.md)                                                 | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**ms-DS-ca-immed-untergeordnete Elemente**](a-msds-approx-immed-subordinates.md)                    | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**MS-DS-Konsistenz-untergeordnet-Anzahl**](a-ms-ds-consistencychildcount.md)                         | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**ms-DS-deaktivieren-für-Instanzen-BL**](a-msds-disableforinstancesbl.md)                         | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**ms-DS-gemastert von**](a-msds-masteredby.md)                                                 | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**ms-DS-NC-repl-Cursor**](a-msds-ncreplcursors.md)                                          | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**ms-DS-NC-repl-Inbound-Nachbarn**](a-msds-ncreplinboundneighbors.md)                       | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**ms-DS-NC-repl-Outbound-Nachbarn**](a-msds-ncreploutboundneighbors.md)                     | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**ms-DS-repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)                         | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**ms-DS-repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**ms-DS-Service-Account-BL**](a-msds-serviceaccountbl.md)                                    | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**ms-DS-Benutzer-Konto-automatisch gesperrt**](a-ms-ds-useraccountautolocked.md)                        | False     | **ms-DS-Bindable-Objekt**                                                                    |
| [**ms-DS-User-Account-Control-berechnet**](a-msds-user-account-control-computed.md)            | False     | **ms-DS-Bindable-Objekt**                                                                    |
| [**ms-DS-Benutzer-Konto-deaktiviert**](a-msds-useraccountdisabled.md)                              | False     | **ms-DS-Bindable-Objekt**                                                                    |
| [**ms-DS-User-nicht-ablaufen-Kennwort**](a-msds-userdontexpirepassword.md)                       | False     | **ms-DS-Bindable-Objekt**                                                                    |
| [**ms-DS-Benutzer-verschlüsselt-Text-Kennwort zulässig**](a-ms-ds-userencryptedtextpasswordallowed.md) | False     | **ms-DS-Bindable-Objekt**                                                                    |
| [**ms-DS-User-Password-abgelaufen**](a-msds-userpasswordexpired.md)                              | False     | **ms-DS-Bindable-Objekt**                                                                    |
| [**ms-DS-User-Password-nicht erforderlich**](a-ms-ds-userpasswordnotrequired.md)                    | False     | **ms-DS-Bindable-Objekt**                                                                    |
| [**NT-pwd-Verlauf**](a-ntpwdhistory.md)                                                       | False     | **ms-DS-Bindable-Objekt**                                                                    |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                                       | Richtig      | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/> [**Nach oben**](c-top.md)<br/> |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                                   | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Objekt-Kategorie**](a-objectcategory.md)                                                    | Richtig      | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Object-Klasse**](a-objectclass.md)                                                          | Richtig      | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Objekt-GUID**](a-objectguid.md)                                                            | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Objekt-sid**](a-objectsid.md)                                                              | Richtig      | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/>                                 |
| [**Objekt-Version**](a-objectversion.md)                                                      | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Andere-bekannte Objekte**](a-otherwellknownobjects.md)                                    | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Partial-Attribute-löschen-List**](a-partialattributedeletionlist.md)                      | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Partiell-Attribut Satz**](a-partialattributeset.md)                                         | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Mögliche-minderwertig**](a-possibleinferiors.md)                                              | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Proxy-Objekt Name**](a-proxiedobjectname.md)                                             | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Proxy Adressen**](a-proxyaddresses.md)                                                    | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**PWD-letztes Set**](a-pwdlastset.md)                                                           | False     | **ms-DS-Bindable-Objekt**                                                                    |
| [**Abfrage-Richtlinie-BL**](a-querypolicybl.md)                                                     | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**RDN**](a-name.md)                                                                          | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                                      | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**REPL-Update-Vector**](a-repluptodatevector.md)                                           | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Reps-from**](a-repsfrom.md)                                                                | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Reps-to**](a-repsto.md)                                                                    | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Novel**](a-revision.md)                                                                 | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**SD-Rechte**](a-sdrightseffective.md)                                             | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Server-Reference-BL**](a-serverreferencebl.md)                                             | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Anzeigen-in-Advanced-nur anzeigen**](a-showinadvancedviewonly.md)                                 | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Site-Object-BL**](a-siteobjectbl.md)                                                       | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Struktur-Objekt-Klasse**](a-structuralobjectclass.md)                                     | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Sub-Refs**](a-subrefs.md)                                                                  | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Subschemasubentry**](a-subschemasubentry.md)                                               | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Ergänzende Anmelde Informationen**](a-supplementalcredentials.md)                                  | False     | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/>                                 |
| [**SystemFlags**](a-systemflags.md)                                                          | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Tokengruppen**](a-tokengroups.md)                                                          | False     | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/>                                 |
| [**Unicode-pwd**](a-unicodepwd.md)                                                            | False     | **ms-DS-Bindable-Objekt**                                                                    |
| [**Die Anwendung wurde geändert.**](a-usnchanged.md)                                                            | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Von der Anwendung erstellte**](a-usncreated.md)                                                            | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**USA-DSA-letzte-obj-entfernt**](a-usndsalastobjremoved.md)                                     | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Standort-und standortübergreifende standortübergreifende**](a-usnintersite.md)                                                        | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**"An-Last-obj-REM"**](a-usnlastobjrem.md)                                                    | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Quell Code Quelle**](a-usnsource.md)                                                              | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**WBEM-Pfad**](a-wbempath.md)                                                                | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Bekannte Objekte**](a-wellknownobjects.md)                                               | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Bei Änderung**](a-whenchanged.md)                                                          | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**Bei Erstellung**](a-whencreated.md)                                                          | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**WWW-Homepage**](a-wwwhomepage.md)                                                         | False     | [**Nach oben**](c-top.md)<br/>                                                              |
| [**WWW-Page-other**](a-url.md)                                                                | False     | [**Nach oben**](c-top.md)<br/>                                                              |



 

 





