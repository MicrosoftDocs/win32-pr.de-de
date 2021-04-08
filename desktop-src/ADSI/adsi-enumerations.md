---
title: ADSI-Enumerationen
description: Active Directory Service Interfaces (ADSI) definieren und verwenden die in der folgenden Tabelle aufgeführten Enumerationen.
ms.assetid: f0ad5ce5-742d-40dc-ac5a-31d779e40bfd
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, Referenz, Enumerationen
- Enumerationen ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 459aa59bc0f7907f59a4cd5a7e5fcb4f1b2630d8
ms.sourcegitcommit: cb844c9ab17577ce171fd7b03add668645867bc7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/27/2020
ms.locfileid: "104038639"
---
# <a name="adsi-enumerations"></a>ADSI-Enumerationen

Active Directory Service Interfaces (ADSI) definieren und verwenden die in der folgenden Tabelle aufgeführten Enumerationen.



| Enumeration                                                           | Beschreibung                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ADS- \_ aceflag-Aufzählung \_**](/windows/win32/api/iads/ne-iads-ads_aceflag_enum)                        | Gibt an, wie die Sicherheit für geerbte Zugriffs Steuerungs Einträge (ACEs) und Überwachungs Typen für einen System-ACE weitergibt.                                                                                                                                             |
| [**ADS-AceType-Aufzählung \_ \_**](/windows/win32/api/iads/ne-iads-ads_acetype_enum)                        | Gibt den ACE-Typ an.                                                                                                                                                                                                                                           |
| [**ADS-Authentifizierungs-Aufzählung \_ \_**](/windows/win32/api/iads/ne-iads-ads_authentication_enum)          | Gibt die Sicherheitsstufe an, die zum Authentifizieren eines Clients verwendet wird.                                                                                                                                                                                                     |
| [**Werbung für Werbung- \_ \_ Verweigerungen \_**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum)       | Gibt das Verhalten der Verweis Verfolgung an.                                                                                                                                                                                                                       |
| [**ADS- \_ derefumum**](/windows/win32/api/iads/ne-iads-ads_derefenum)                               | Gibt das Verhalten der Alias Dereferenzierung an.                                                                                                                                                                                                                    |
| [**Anzeige Aufzählung anzeigen \_ \_**](/windows/win32/api/iads/ne-iads-ads_display_enum)                        | Gibt an, wie ein Pfad angezeigt wird.                                                                                                                                                                                                                                |
| [**ADS \_ - \_ escapesmodusenum \_**](/windows/win32/api/iads/ne-iads-ads_escape_mode_enum)               | Gibt an, ob Sonderzeichen mit Escapezeichen versehen, ohne Escapezeichen versehen werden.                                                                                                                                                                                        |
| [**ADS-FlagType-Aufzählung \_ \_**](/windows/win32/api/iads/ne-iads-ads_flagtype_enum)                      | Gibt an, dass die Felder " **ObjectType** " oder " **vereritedobjecttype** " in einem ACE vorhanden sind.                                                                                                                                                                         |
| [**ADS- \_ Format- \_ enum**](/windows/win32/api/iads/ne-iads-ads_format_enum)                          | Gibt den Typ der Werte in einem Pfadnamen-Objekt an.                                                                                                                                                                                                                |
| [**ADS \_ - \_ Gruppentyp- \_ enum**](/windows/win32/api/iads/ne-iads-ads_group_type_enum)                 | Gibt den Gruppentyp des Members an.                                                                                                                                                                                                                           |
| [**ADS \_ Name \_ inittype \_ enum**](/windows/win32/api/iads/ne-iads-ads_name_inittype_enum)           | Gibt den Typ der Initialisierung an, der für ein Name Translation-Objekt ausgeführt werden soll.                                                                                                                                                                                  |
| [**ADS \_ - \_ Namenstyp- \_ enum**](/windows/win32/api/iads/ne-iads-ads_name_type_enum)                   | Gibt das Format an, mit dem Distinguished Names dargestellt werden.                                                                                                                                                                                                       |
| [**ADS-Option-Aufzählung \_ \_**](/windows/win32/api/iads/ne-iads-ads_option_enum)                          | Gibt die verfügbaren Optionen an, die von der [**iadsobjectoptions**](/windows/desktop/api/Iads/nn-iads-iadsobjectoptions) -Schnittstelle zum Bearbeiten von Verzeichnis Objekten verwendet werden.                                                                                                                        |
| [**ADS \_ - \_ Codierungs-Aufzählung \_**](/windows/win32/api/iads/ne-iads-ads_password_encoding_enum)   | Wird verwendet, um den Typ der Kenn Wort Codierung zu identifizieren, die mit der Option " **ADS \_ Option \_ password \_ method** " in den [**iadsobjectoptions:: GetOption**](/windows/desktop/api/Iads/nf-iads-iadsobjectoptions-getoption) -und [**iadsobjectoptions:: SetOption**](/windows/desktop/api/Iads/nf-iads-iadsobjectoptions-setoption) -Methoden verwendet wird. |
| [**ADS-PathType-Aufzählung \_ \_**](/windows/win32/api/iads/ne-iads-ads_pathtype_enum)                      | Gibt den Objekttyp an, für den die Sicherheits Beschreibung geändert wird.                                                                                                                                                                                        |
| [**ADS-Voreinstellungs-Aufzählung \_ \_**](/windows/win32/api/iads/ne-iads-ads_preferences_enum)                | Gibt die Abfrage Einstellungen der OLE DB für ADSI an.                                                                                                                                                                                                           |
| [**Aufzählung der ADS- \_ Eigenschafts \_ Operation \_**](/windows/win32/api/iads/ne-iads-ads_property_operation_enum) | Gibt an, wie Eigenschaftswerte im Eigenschaften Cache aktualisiert werden.                                                                                                                                                                                               |
| [**ADS-Rechte Aufzählung \_ \_**](/windows/win32/api/iads/ne-iads-ads_rights_enum)                          | Gibt die Zugriffsrechte für ein Verzeichnisdienst Objekt an.                                                                                                                                                                                                        |
| [**ADS- \_ scopeumum**](/windows/win32/api/iads/ne-iads-ads_scopeenum)                               | Gibt den Bereich einer Verzeichnis Suche an.                                                                                                                                                                                                                        |
| [**ADS \_ SD- \_ Steuerelement \_ -Aufzählung**](/windows/win32/api/iads/ne-iads-ads_sd_control_enum)                 | Gibt an, dass eine Zugriffs Steuerungs Liste (Access Control List, ACL) geschützt werden soll, wenn neue Berechtigungen rekursiv auf eine Verzeichnisstruktur angewendet werden.                                                                                                                                  |
| [**ADS- \_ SD- \_ Format- \_ enum**](/windows/win32/api/iads/ne-iads-ads_sd_format_enum)                   | Gibt das Format für das Umstellen der Sicherheits Beschreibung an.                                                                                                                                                                                                      |
| [**ADS \_ SD \_ Revision-Aufzählung \_**](/windows/win32/api/iads/ne-iads-ads_sd_revision_enum)               | Gibt die Revisionsnummer eines ACE oder einer ACL an.                                                                                                                                                                                                                   |
| [**ADS \_ searchpref-Aufzählung \_**](/windows/win32/api/iads/ne-iads-ads_searchpref_enum)                  | Gibt Einstellungen für die Suche an.                                                                                                                                                                                                                              |
| [**ADS- \_ Sicherheits \_ Info- \_ Aufzählung**](/windows/win32/api/iads/ne-iads-ads_security_info_enum)           | Gibt die Optionen für die Untersuchung von Sicherheitsdaten an.                                                                                                                                                                                                                |
| [**ADS-settype-Aufzählung \_ \_**](/windows/win32/api/iads/ne-iads-ads_settype_enum)                        | Gibt das Pfad Format in [**iadspathname:: Set**](/windows/desktop/api/Iads/nf-iads-iadspathname-set)an.                                                                                                                                                                                       |
| [**Anzeigen von \_ Status usenum**](/windows/win32/api/iads/ne-iads-ads_statusenum)                             | Gibt den Status der Sucheinstellungen an.                                                                                                                                                                                                                       |
| [**ADS \_ Systemflag-Aufzählung \_**](/windows/win32/api/iads/ne-iads-ads_systemflag_enum)                  | Gibt die Typen von Attributen an, die durch ein **attributeSchema** -Objekt dargestellt werden.                                                                                                                                                                                   |
| [**ADS- \_ benutzerflag-Aufzählung \_ \_**](/windows/win32/api/iads/ne-iads-ads_user_flag_enum)                   | Gibt Flags zum Bearbeiten von Benutzereigenschaften an.                                                                                                                                                                                                            |
| [**ADSI-Dialekt-Aufzählung \_ \_**](/windows/win32/api/iads/ne-iads-adsi_dialect_enum)                      | Gibt verfügbare ADSI-Abfrage Dialekte an.                                                                                                                                                                                                                          |
| [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum)                                    | Gibt Datentypen an, die verwendet werden, um eine erweiterte ADSI-Syntax zu interpretieren.                                                                                                                                                                                            |



 

## <a name="remarks"></a>Bemerkungen

Da Visual Basic Scripting Edition Anwendungen keine Daten aus einer Typbibliothek lesen können, können VBScript-Anwendungen keine symbolischen Konstanten erkennen, wie Sie in diesen Enumerationen definiert sind. Verwenden Sie stattdessen die numerischen Konstanten, um die entsprechenden Flags in einer VBScript-Anwendung festzulegen. Schreiben Sie in VBScript-Anwendungen explizite Deklarationen dieser Konstanten, um die symbolischen Konstanten als gute Programmierpraxis zu verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IADsObjectOptions**](/windows/desktop/api/Iads/nn-iads-iadsobjectoptions)
</dt> <dt>

[**Iadspathname:: Set**](/windows/desktop/api/Iads/nf-iads-iadspathname-set)
</dt> </dl>

 

 




