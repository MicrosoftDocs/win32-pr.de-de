---
title: ADSI-Enumerationen
description: Active Directory-Dienstschnittstellen (ADSI) definieren und verwenden die in der folgenden Tabelle aufgeführten Enumerationen.
ms.assetid: f0ad5ce5-742d-40dc-ac5a-31d779e40bfd
ms.tgt_platform: multiple
keywords:
- ADSI ADSI , Referenz, Enumerationen
- Enumerationen ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c10d5aed5688e7128a64a32dee2f83efa22ab5bf292231517026299ccb592886
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023908"
---
# <a name="adsi-enumerations"></a>ADSI-Enumerationen

Active Directory-Dienstschnittstellen (ADSI) definieren und verwenden die in der folgenden Tabelle aufgeführten Enumerationen.



| Enumeration                                                           | Beschreibung                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ADS \_ ACEFLAG \_ ENUM**](/windows/win32/api/iads/ne-iads-ads_aceflag_enum)                        | Gibt an, wie die Sicherheit für geerbte Zugriffssteuerungseinträge (ACEs) und Überwachungstypen für einen System-ACE weitergegeben wird.                                                                                                                                             |
| [**ADS \_ ACETYPE \_ ENUM**](/windows/win32/api/iads/ne-iads-ads_acetype_enum)                        | Gibt den ACE-Typ an.                                                                                                                                                                                                                                           |
| [**ADS \_ AUTHENTICATION \_ ENUM**](/windows/win32/api/iads/ne-iads-ads_authentication_enum)          | Gibt die Sicherheitsstufe an, die bei der Authentifizierung eines Clients verwendet wird.                                                                                                                                                                                                     |
| [**\_ \_ ADS-NACHVERFOLGUNGS-EMPFEHLUNGSENUMER \_**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum)       | Gibt das Verhalten der Verweisverfolge an.                                                                                                                                                                                                                       |
| [**ADS \_ DEREFENUM**](/windows/win32/api/iads/ne-iads-ads_derefenum)                               | Gibt das Verhalten der Aliasdereferenzierung an.                                                                                                                                                                                                                    |
| [**ADS \_ DISPLAY \_ ENUM**](/windows/win32/api/iads/ne-iads-ads_display_enum)                        | Gibt an, wie ein Pfad angezeigt wird.                                                                                                                                                                                                                                |
| [**ADS \_ ESCAPE \_ MODE \_ ENUM**](/windows/win32/api/iads/ne-iads-ads_escape_mode_enum)               | Gibt an, ob Sonderzeichen mit Escapezeichen, ohne Escapezeichen oder unverändert sind.                                                                                                                                                                                        |
| [**ADS \_ \_ FLAGTYPE-ENUMERATION**](/windows/win32/api/iads/ne-iads-ads_flagtype_enum)                      | Gibt das Vorhandensein der Felder **ObjectType** oder **InheritedObjectType** in einem ACE an.                                                                                                                                                                         |
| [**ADS \_ FORMAT \_ ENUM**](/windows/win32/api/iads/ne-iads-ads_format_enum)                          | Gibt den Typ der Werte in einem Pathname-Objekt an.                                                                                                                                                                                                                |
| [**ADS \_ GROUP \_ TYPE \_ ENUM**](/windows/win32/api/iads/ne-iads-ads_group_type_enum)                 | Gibt den Gruppentyp des Members an.                                                                                                                                                                                                                           |
| [**ADS \_ NAME \_ INITTYPE \_ ENUM**](/windows/win32/api/iads/ne-iads-ads_name_inittype_enum)           | Gibt den Typ der Initialisierung an, die für ein Name-Translate-Objekt ausgeführt werden soll.                                                                                                                                                                                  |
| [**ADS \_ NAME \_ TYPE \_ ENUM**](/windows/win32/api/iads/ne-iads-ads_name_type_enum)                   | Gibt das Format an, das zum Darstellen von Distinguished Names verwendet wird.                                                                                                                                                                                                       |
| [**ADS \_ OPTION \_ ENUM**](/windows/win32/api/iads/ne-iads-ads_option_enum)                          | Gibt die verfügbaren Optionen an, die die [**IADsObjectOptions-Schnittstelle**](/windows/desktop/api/Iads/nn-iads-iadsobjectoptions) zum Bearbeiten von Verzeichnisobjekten verwendet.                                                                                                                        |
| [**ADS \_ PASSWORD \_ ENCODING \_ ENUM**](/windows/win32/api/iads/ne-iads-ads_password_encoding_enum)   | Wird verwendet, um den Typ der Kennwortcodierung zu identifizieren, der mit der **ADS \_ OPTION PASSWORD \_ \_ METHOD-Option** in den Methoden [**IADsObjectOptions::GetOption**](/windows/desktop/api/Iads/nf-iads-iadsobjectoptions-getoption) und [**IADsObjectOptions::SetOption**](/windows/desktop/api/Iads/nf-iads-iadsobjectoptions-setoption) verwendet wird. |
| [**ADS \_ PATHTYPE \_ ENUM**](/windows/win32/api/iads/ne-iads-ads_pathtype_enum)                      | Gibt den Typ des Objekts an, für das der Sicherheitsdeskriptor geändert wird.                                                                                                                                                                                        |
| [**ADS \_ PREFERENCES \_ ENUM**](/windows/win32/api/iads/ne-iads-ads_preferences_enum)                | Gibt die Abfrageeinstellungen des OLE DB für ADSI an.                                                                                                                                                                                                           |
| [**ADS \_ PROPERTY \_ OPERATION \_ ENUM**](/windows/win32/api/iads/ne-iads-ads_property_operation_enum) | Gibt die Möglichkeiten zum Aktualisieren von Eigenschaftswerten im Eigenschaftencache an.                                                                                                                                                                                               |
| [**ADS \_ RIGHTS \_ ENUM**](/windows/win32/api/iads/ne-iads-ads_rights_enum)                          | Gibt die Zugriffsrechte für ein Verzeichnisdienstobjekt an.                                                                                                                                                                                                        |
| [**ADS \_ SCOPEENUM**](/windows/win32/api/iads/ne-iads-ads_scopeenum)                               | Gibt den Bereich einer Verzeichnissuche an.                                                                                                                                                                                                                        |
| [**ADS \_ SD \_ CONTROL \_ ENUM**](/windows/win32/api/iads/ne-iads-ads_sd_control_enum)                 | Gibt an, dass eine Zugriffssteuerungsliste (Access Control List, ACL) geschützt werden soll, wenn neue Berechtigungen rekursiv auf eine Verzeichnisstruktur angewendet werden.                                                                                                                                  |
| [**ADS \_ SD \_ FORMAT \_ ENUM**](/windows/win32/api/iads/ne-iads-ads_sd_format_enum)                   | Gibt das Format zum Konvertieren des Sicherheitsdeskriptors an.                                                                                                                                                                                                      |
| [**ADS \_ SD \_ REVISION \_ ENUM**](/windows/win32/api/iads/ne-iads-ads_sd_revision_enum)               | Gibt die Revisionsnummer eines ACE oder einer ACL an.                                                                                                                                                                                                                   |
| [**ADS \_ \_ SEARCHPREF-ENUMERATION**](/windows/win32/api/iads/ne-iads-ads_searchpref_enum)                  | Gibt die Einstellungen der Suche an.                                                                                                                                                                                                                              |
| [**ADS \_ SECURITY \_ INFO \_ ENUM**](/windows/win32/api/iads/ne-iads-ads_security_info_enum)           | Gibt die Optionen zum Untersuchen von Sicherheitsdaten an.                                                                                                                                                                                                                |
| [**ADS \_ SETTYPE \_ ENUM**](/windows/win32/api/iads/ne-iads-ads_settype_enum)                        | Gibt das Pfadformat in [**IADsPathname::Set an.**](/windows/desktop/api/Iads/nf-iads-iadspathname-set)                                                                                                                                                                                       |
| [**ADS \_ STATUSENUM**](/windows/win32/api/iads/ne-iads-ads_statusenum)                             | Gibt den Status der Sucheinstellungen an.                                                                                                                                                                                                                       |
| [**ADS \_ \_ SYSTEMFLAG-ENUMERATION**](/windows/win32/api/iads/ne-iads-ads_systemflag_enum)                  | Gibt die Typen von Attributen an, die durch ein **attributeSchema-Objekt** dargestellt werden.                                                                                                                                                                                   |
| [**ADS \_ USER \_ FLAG \_ ENUM**](/windows/win32/api/iads/ne-iads-ads_user_flag_enum)                   | Gibt Flags an, die zum Bearbeiten von Benutzereigenschaften verwendet werden.                                                                                                                                                                                                            |
| [**\_ \_ ADSI-DIALEKT-ENUMERATION**](/windows/win32/api/iads/ne-iads-adsi_dialect_enum)                      | Gibt verfügbare ADSI-Abfragedialekte an.                                                                                                                                                                                                                          |
| [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum)                                    | Gibt Datentypen an, die zum Interpretieren einer erweiterten ADSI-Syntaxzeichenfolge verwendet werden.                                                                                                                                                                                            |



 

## <a name="remarks"></a>Hinweise

Da Visual Basic Scripting Edition-Anwendungen keine Daten aus einer Typbibliothek lesen können, können VBScript-Anwendungen keine symbolischen Konstanten erkennen, wie in diesen Enumerationen definiert. Verwenden Sie stattdessen die numerischen Konstanten, um die entsprechenden Flags in vbscript-Anwendungen festzulegen. Um die symbolischen Konstanten als gute Programmieranwendung zu verwenden, schreiben Sie explizite Deklarationen solcher Konstanten, wie hier geschehen, in VBScript-Anwendungen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IADsObjectOptions**](/windows/desktop/api/Iads/nn-iads-iadsobjectoptions)
</dt> <dt>

[**IADsPathname::Set**](/windows/desktop/api/Iads/nf-iads-iadspathname-set)
</dt> </dl>

 

 




