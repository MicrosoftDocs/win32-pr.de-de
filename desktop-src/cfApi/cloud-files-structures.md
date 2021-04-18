---
description: Die folgenden Strukturen werden zum Erstellen und Verwalten von Platzhalter Dateien und Verzeichnissen verwendet.
ms.assetid: 50CCA8F5-7118-48E8-ADBF-337798FAF549
title: Cloudfilterstrukturen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eebe6623ad3d9d348d624f8ab8da3427416d4742
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344010"
---
# <a name="cloud-filter-structures"></a>Cloudfilterstrukturen

Die folgenden Strukturen werden zum Erstellen und Verwalten von Platzhalter Dateien und Verzeichnissen verwendet.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                   | BESCHREIBUNG                                                                                                                               |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [**CF- \_ Rückruf \_ Informationen**](/windows/desktop/api/cfapi/ns-cfapi-cf_callback_info)<br/>                          | Enthält allgemeine Rückruf Informationen.<br/>                                                                                          |
| [**CF- \_ Rückruf \_ Parameter**](/windows/desktop/api/cfapi/ns-cfapi-cf_callback_parameters)<br/>              | Enthält Rückruf spezifische Parameter, wie z. b. Dateioffset, Länge, Flags usw.<br/>                                                 |
| [**CF- \_ Rückruf \_ Registrierung**](/windows/desktop/api/cfapi/ns-cfapi-cf_callback_registration)<br/>          | Die Rückrufe, die vom Synchronisierungs Anbieter registriert werden sollen.<br/>                                                                           |
| [**CF- \_ Datei \_ Bereich**](/windows/desktop/api/cfapi/ns-cfapi-cf_file_range)<br/>                                | Gibt einen Datenbereich in einer Platzhalter Datei an.<br/>                                                                               |
| [**CF- \_ Datei \_ Bereichs \_ Puffer**](/previous-versions/windows/desktop/legacy/mt844616(v=vs.85))<br/>                | Eine-Struktur, um den Speicherort und den Datenbereich in einer Datei zu beschreiben.<br/>                                                              |
| [**CF \_ FS- \_ Metadaten**](/windows/desktop/api/cfapi/ns-cfapi-cf_fs_metadata)<br/>                              | Platzhalter Datei-oder Verzeichnis Metadaten.<br/>                                                                                        |
| [**CF-Aktivierungs \_ \_ Richtlinie**](/windows/desktop/api/cfapi/ns-cfapi-cf_hydration_policy)<br/>                    | Gibt die primäre Aktivierungs Richtlinie und deren Modifizierer an.<br/>                                                                       |
| [**CF- \_ Vorgangs \_ Informationen**](/windows/desktop/api/cfapi/ns-cfapi-cf_operation_info)<br/>                        | Informationen zu einem Vorgang für eine Platzhalter Datei oder einen Platzhalter Ordner.<br/>                                                                |
| [**CF- \_ Vorgangs \_ Parameter**](/windows/desktop/api/cfapi/ns-cfapi-cf_operation_parameters)<br/>            | Parameter eines Vorgangs für eine Platzhalter Datei oder einen Platzhalter Ordner.<br/>                                                                    |
| [**\_ \_ grundlegende \_ Informationen zum CF-Platzhalter**](/windows/desktop/api/cfapi/ns-cfapi-cf_placeholder_basic_info)<br/>       | Grundlegende Platzhalter Informationen.<br/>                                                                                                 |
| [**Informationen zum Erstellen von CF- \_ Platzhaltern \_ \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_placeholder_create_info)<br/>     | Enthält Platzhalter Informationen zum Erstellen neuer Platzhalter Dateien oder Verzeichnisse. <br/>                                           |
| [**CF- \_ Platzhalter- \_ Standard \_ Informationen**](/windows/desktop/api/cfapi/ns-cfapi-cf_placeholder_standard_info)<br/> | Standard Platzhalter Informationen.<br/>                                                                                              |
| [**CF- \_ Platt Form \_ Informationen**](/windows/desktop/api/cfapi/ns-cfapi-cf_platform_info)<br/>                          | Gibt Informationen für die Cloud Files-Plattform zurück. Dies ist für Synchronisierungs Anbieter vorgesehen, die unter mehreren Versionen von Windows ausgeführt werden.<br/> |
| [**CF \_ Population- \_ Richtlinie**](/windows/desktop/api/cfapi/ns-cfapi-cf_population_policy)<br/>                  | Gibt die primäre auffüllungs Richtlinie und ihren Modifizierer an.<br/>                                                                      |
| [**CF- \_ Prozess \_ Informationen**](/windows/desktop/api/cfapi/ns-cfapi-cf_process_info)<br/>                            | Enthält Informationen zu einem Benutzer Prozess.<br/>                                                                                     |
| [**CF- \_ Synchronisierungs \_ Richtlinien**](/windows/desktop/api/cfapi/ns-cfapi-cf_sync_policies)<br/>                          | Definiert die Synchronisierungs Richtlinien, die von einem Synchronisierungs Stamm verwendet werden.<br/>                                                                                 |
| [**CF- \_ Synchronisierungs \_ Registrierung**](/windows/desktop/api/cfapi/ns-cfapi-cf_sync_registration)<br/>                  | Die Details des Synchronisierungs Anbieters und der Synchronisierungs Stamm, die registriert werden sollen.<br/>                                                               |
| [**\_ \_ \_ grundlegende \_ Informationen zum Stammverzeichnis von CF**](/windows/desktop/api/cfapi/ns-cfapi-cf_sync_root_basic_info)<br/>          | Grundlegende Informationen zur Synchronisierungs Stamm.<br/>                                                                                                   |
| [**CF- \_ Synchronisierungs Stamm \_ Anbieter- \_ \_ Informationen**](/windows/desktop/api/cfapi/ns-cfapi-cf_sync_root_provider_info)<br/>    | Informationen zu Stamm Anbietern synchronisieren.<br/>                                                                                                |
| [**CF \_ Sync \_ root \_ Standard \_ Info**](/windows/desktop/api/cfapi/ns-cfapi-cf_sync_root_standard_info)<br/>    | Standard-Synchronisierungs Stamm Informationen.<br/>                                                                                                |
| [**CF- \_ Synchronisierungs \_ Status**](/windows/desktop/api/cfapi/ns-cfapi-cf_sync_status)<br/>                              | Wird in einer [**CF- \_ Vorgangs \_ Info**](/windows/desktop/api/cfapi/ns-cfapi-cf_operation_info) Struktur verwendet, um den Status eines angegebenen Synchronisierungs Stamms zu beschreiben.<br/>     |



 

 

