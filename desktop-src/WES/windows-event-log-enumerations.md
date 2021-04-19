---
title: Windows-Ereignisprotokoll-Enumerationen
description: Das Windows-Ereignisprotokoll definiert die folgenden Enumerationen.
ms.assetid: 2dd0e9ef-057b-4d0a-8b21-e7f14e5ae6e3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c019a090d1a12e30948e5ed1f5672853caed848c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338207"
---
# <a name="windows-event-log-enumerations"></a>Windows-Ereignisprotokoll-Enumerationen

Das Windows-Ereignisprotokoll definiert die folgenden Enumerationen.



| Enumeration                                                                          | Beschreibung                                                                                                                        |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Typ der EVT- \_ \_ kanaluhr \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_channel_clock_type)                          | Definiert die Werte, die den Typ des Zeitstempels angeben, der beim Protokollieren des Ereignis Kanals verwendet werden soll.                                         |
| [**Eigenschaften-ID der EVT- \_ Kanal \_ Konfiguration \_ \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_channel_config_property_id)         | Definiert die Bezeichner, mit denen die Konfigurations Eigenschaften eines Kanals identifiziert werden.                                                   |
| [**EVT- \_ Kanal \_ Isolations \_ Typen**](/windows/desktop/api/WinEvt/ne-winevt-evt_channel_isolation_type)                  | Definiert die Standard Zugriffsberechtigungen, die auf den Kanal angewendet werden sollen.                                                                    |
| [**EVT \_ - \_ kanalverweisflags \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_channel_reference_flags)                | Definiert die Werte, die angeben, wie auf einen Kanal verwiesen wird.                                                                       |
| [**EVT- \_ Kanal- \_ sid- \_ Typ**](/windows/desktop/api/WinEvt/ne-winevt-evt_channel_sid_type)                              | Definiert die Werte, die bestimmen, ob das Ereignis die Sicherheits-ID (SID) des Prinzipals enthält, der das Ereignis protokolliert hat. |
| [**EVT \_ - \_ Kanaltyp**](/windows/desktop/api/WinEvt/ne-winevt-evt_channel_type)                                       | Definiert den Kanaltyp.                                                                                                     |
| [**Eigenschaften-ID der EVT- \_ Ereignis \_ Metadaten \_ \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_event_metadata_property_id)         | Definiert die Bezeichner, mit denen die Metadateneigenschaften einer Ereignis Definition identifiziert werden.                                              |
| [**EVT- \_ Ereignis \_ Eigenschaften- \_ ID**](/windows/desktop/api/WinEvt/ne-winevt-evt_event_property_id)               | Definiert die Werte, die die abzurufenden Abfrage Informationen bestimmen.                                                               |
| [**EVT- \_ \_ exportloggungsflags**](/windows/desktop/api/WinEvt/ne-winevt-evt_exportlog_flags)                                 | Definiert Werte, die angeben, ob die Ereignisse aus einer Kanal-oder Protokolldatei stammen.                                                   |
| [**EVT \_ - \_ \_ formatnachrichtenflags**](/windows/desktop/api/WinEvt/ne-winevt-evt_format_message_flags)                      | Definiert die Werte, die die Meldungs Zeichenfolge aus dem zu formatierenden Ereignis angeben.                                                       |
| [**EVT- \_ Protokoll \_ Eigenschaften- \_ ID**](/windows/desktop/api/WinEvt/ne-winevt-evt_log_property_id)                                | Definiert die Bezeichner, die die Protokolldatei-Metadateneigenschaften eines Kanals oder einer Protokolldatei identifizieren.                                   |
| [**EVT- \_ Anmelde \_ Klasse**](/windows/desktop/api/WinEvt/ne-winevt-evt_login_class)                                         | Definiert die Typen von Verbindungsmethoden, die Sie verwenden können, um eine Verbindung mit dem Remote Computer herzustellen.                                             |
| [**EVT \_ - \_ Protokoll- \_ Flags öffnen**](/windows/desktop/api/WinEvt/ne-winevt-evt_open_log_flags)                                  | Definiert die Werte, die angeben, ob ein Kanal oder eine exportierte Protokolldatei geöffnet werden soll.                                                    |
| [**ID der EVT- \_ Verleger- \_ \_ Metadateneigenschaft \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_publisher_metadata_property_id) | Definiert die Bezeichner, die die Metadateneigenschaften eines Anbieters identifizieren.                                                       |
| [**EVT \_ - \_ Abfrageflags**](/windows/desktop/api/WinEvt/ne-winevt-evt_query_flags)                                         | Definiert die Werte, die angeben, wie die Abfrageergebnisse zurückgegeben werden sollen, und ob Sie eine Abfrage für eine Kanal-oder Protokolldatei durchführen.           |
| [**EVT- \_ Abfrage \_ Eigenschaften- \_ ID**](/windows/desktop/api/WinEvt/ne-winevt-evt_query_property_id)                            | Definiert die Bezeichner, die die Abfrage Informationen identifizieren, die Sie abrufen können.                                                 |
| [**EVT- \_ Rendering-kontextflags \_ \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_render_context_flags)                      | Definiert die Werte, die den Typ der Informationen angeben, auf die vom Ereignis aus zugegriffen werden soll.                                                  |
| [**EVT- \_ Rendering- \_ Flags**](/windows/desktop/api/WinEvt/ne-winevt-evt_render_flags)                                       | Definiert die Werte, die angeben, was dargestellt werden soll.                                                                                    |
| [**EVT- \_ RPC- \_ Anmeldungs \_ Flags**](/windows/desktop/api/WinEvt/ne-winevt-evt_rpc_login_flags)                                | Definiert die Arten der Authentifizierung, die Sie zum Authentifizieren des Benutzers beim Herstellen einer Verbindung mit einem Remote Computer verwenden können.                |
| [**EVT \_ - \_ Suchflags**](/windows/desktop/api/WinEvt/ne-winevt-evt_seek_flags)                                           | Definiert die relative Position im Resultset, von dem gesucht werden soll.                                                                |
| [**EVT \_ - \_ abonnementflags**](/windows/desktop/api/WinEvt/ne-winevt-evt_subscribe_flags)                                 | Definiert die möglichen Werte, die angeben, wann mit dem Abonnieren von Ereignissen begonnen werden soll.                                                      |
| [**Benachrichtigung zum Abonnieren des EVT-Abonnements \_ \_ \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_subscribe_notify_action)                | Definiert die möglichen Datentypen, die der Abonnement Dienst an Ihren Rückruf übermitteln kann.                                     |
| [**EVT- \_ System \_ Eigenschaften- \_ ID**](/windows/desktop/api/WinEvt/ne-winevt-evt_system_property_id)                          | Definiert die Bezeichner, mit denen die System definierten Eigenschaften eines Ereignisses identifiziert werden.                                                   |
| [**EVT \_ - \_ Varianttyp**](/windows/desktop/api/WinEvt/ne-winevt-evt_variant_type)                                       | Definiert die möglichen Datentypen eines Variant-Datenelements.                                                                            |



 

 

 




