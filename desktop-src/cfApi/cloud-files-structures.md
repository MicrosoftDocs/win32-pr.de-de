---
description: Die folgenden Strukturen werden zum Erstellen und Verwalten von Platzhalterdateien und Verzeichnissen verwendet.
ms.assetid: 50CCA8F5-7118-48E8-ADBF-337798FAF549
title: Cloudfilterstrukturen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6da8cf5e512c6e65e88d17c5904fca264c28829dd0a0e842227da4b069aa82d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130222"
---
# <a name="cloud-filter-structures"></a>Cloudfilterstrukturen

Die folgenden Strukturen werden zum Erstellen und Verwalten von Platzhalterdateien und Verzeichnissen verwendet.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                   | Beschreibung                                                                                                                               |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [**CF \_ CALLBACK \_ INFO**](/windows/desktop/api/cfapi/ns-cfapi-cf_callback_info)<br/>                          | Enthält allgemeine Rückrufinformationen.<br/>                                                                                          |
| [**\_ \_ CF-RÜCKRUFPARAMETER**](/windows/desktop/api/cfapi/ns-cfapi-cf_callback_parameters)<br/>              | Enthält rückrufspezifische Parameter wie Dateioffset, Länge, Flags usw.<br/>                                                 |
| [**CF \_ CALLBACK \_ REGISTRATION**](/windows/desktop/api/cfapi/ns-cfapi-cf_callback_registration)<br/>          | Die Rückrufe, die vom Synchronisierungsanbieter registriert werden sollen.<br/>                                                                           |
| [**\_ \_ CF-DATEIBEREICH**](/windows/desktop/api/cfapi/ns-cfapi-cf_file_range)<br/>                                | Gibt einen Datenbereich in einer Platzhalterdatei an.<br/>                                                                               |
| [**\_ \_ \_ CF-DATEIBEREICHSPUFFER**](/previous-versions/windows/desktop/legacy/mt844616(v=vs.85))<br/>                | Eine -Struktur, die den Speicherort und den Datenbereich in einer Datei beschreibt.<br/>                                                              |
| [**CF \_ \_ FS-METADATEN**](/windows/desktop/api/cfapi/ns-cfapi-cf_fs_metadata)<br/>                              | Platzhalterdatei oder Verzeichnismetadaten.<br/>                                                                                        |
| [**CF \_ \_ HYDRATION-RICHTLINIE**](/windows/desktop/api/cfapi/ns-cfapi-cf_hydration_policy)<br/>                    | Gibt die primäre Hydrationsrichtlinie und deren Modifizierer an.<br/>                                                                       |
| [**\_CF-VORGANGSINFORMATIONEN \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_operation_info)<br/>                        | Informationen zu einem Vorgang für eine Platzhalterdatei oder einen Platzhalterordner.<br/>                                                                |
| [**\_CF-VORGANGSPARAMETER \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_operation_parameters)<br/>            | Parameter eines Vorgangs für eine Platzhalterdatei oder einen Platzhalterordner.<br/>                                                                    |
| [**GRUNDLEGENDE INFORMATIONEN ZUM \_ CF-PLATZHALTER \_ \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_placeholder_basic_info)<br/>       | Grundlegende Platzhalterinformationen.<br/>                                                                                                 |
| [**CF \_ PLACEHOLDER \_ CREATE \_ INFO**](/windows/desktop/api/cfapi/ns-cfapi-cf_placeholder_create_info)<br/>     | Enthält Platzhalterinformationen zum Erstellen neuer Platzhalterdateien oder -verzeichnisse. <br/>                                           |
| [**\_ \_ CF-PLATZHALTERSTANDARDINFORMATIONEN \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_placeholder_standard_info)<br/> | Standardplatzhalterinformationen.<br/>                                                                                              |
| [**INFORMATIONEN \_ ZUR CF-PLATTFORM \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_platform_info)<br/>                          | Gibt Informationen für die Clouddateiplattform zurück. Dies ist für Synchronisierungsanbieter vorgesehen, die in mehreren Versionen von Windows ausgeführt werden.<br/> |
| [**CF \_ POPULATION \_ POLICY**](/windows/desktop/api/cfapi/ns-cfapi-cf_population_policy)<br/>                  | Gibt die primäre Auffüllungsrichtlinie und deren Modifizierer an.<br/>                                                                      |
| [**\_ \_ CF-PROZESSINFORMATIONEN**](/windows/desktop/api/cfapi/ns-cfapi-cf_process_info)<br/>                            | Enthält Informationen zu einem Benutzerprozess.<br/>                                                                                     |
| [**\_CF-SYNCHRONISIERUNGSRICHTLINIEN \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_sync_policies)<br/>                          | Definiert die Synchronisierungsrichtlinien, die von einem Synchronisierungsstamm verwendet werden.<br/>                                                                                 |
| [**CF \_ \_ SYNC-REGISTRIERUNG**](/windows/desktop/api/cfapi/ns-cfapi-cf_sync_registration)<br/>                  | Die Details des zu registrierenden Synchronisierungsanbieters und Synchronisierungsstamms.<br/>                                                               |
| [**GRUNDLEGENDE INFORMATIONEN ZUM CF \_ \_ SYNC-STAMM \_ \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_sync_root_basic_info)<br/>          | Grundlegende Synchronisierungsstamminformationen.<br/>                                                                                                   |
| [**INFORMATIONEN ZUM CF \_ \_ SYNC-STAMMANBIETER \_ \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_sync_root_provider_info)<br/>    | Synchronisieren von Stammanbieterinformationen.<br/>                                                                                                |
| [**CF \_ SYNC \_ ROOT \_ STANDARD \_ INFO**](/windows/desktop/api/cfapi/ns-cfapi-cf_sync_root_standard_info)<br/>    | Standard-Synchronisierungsstamminformationen.<br/>                                                                                                |
| [**CF \_ SYNC \_ STATUS**](/windows/desktop/api/cfapi/ns-cfapi-cf_sync_status)<br/>                              | Wird in einer [**CF \_ OPERATION \_ INFO-Struktur**](/windows/desktop/api/cfapi/ns-cfapi-cf_operation_info) verwendet, um den Status eines angegebenen Synchronisierungsstamms zu beschreiben.<br/>     |



 

 

