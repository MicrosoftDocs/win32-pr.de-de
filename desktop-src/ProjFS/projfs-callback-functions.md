---
title: ProjFS-Rückruffunktionen
description: Die folgenden Rückruffunktionen werden in projectedfslib.h deklariert.
ms.assetid: <GUID-GOES-HERE>
ms.date: 01/17/2020
ms.topic: article
ms.openlocfilehash: 595fac418ce57e1e6caff718d75b458390efd31c2e8727cd2feb8ee5a5d86eb3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031160"
---
# <a name="callback-functions"></a>Rückruffunktionen

Die folgenden Rückruffunktionen werden in projectedfslib.h deklariert.

## <a name="in-this-section"></a>In diesem Abschnitt

| Thema | BESCHREIBUNG |
|-|-|
| [**PRJ_CANCEL_COMMAND_CB**](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_cancel_command_cb) | Benachrichtigt den Anbieter, dass ein Vorgang durch einen früheren Aufruf eines Rückrufs abgebrochen werden soll. |
| [**PRJ_END_DIRECTORY_ENUMERATION_CB**](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_end_directory_enumeration_cb) | Informiert den Anbieter darüber, dass eine Verzeichnisenumeration beendet ist. |
| [**PRJ_GET_DIRECTORY_ENUMERATION_CB**](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_directory_enumeration_cb) | Fordert Informationen zur Verzeichnisenumeration vom Anbieter an.
| [**PRJ_GET_FILE_DATA_CB**](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_file_data_cb) | Fordert den Inhalt des primären Datenstroms einer Datei an.
| [**PRJ_GET_PLACEHOLDER_INFO_CB**](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_placeholder_info_cb) | Fordert Informationen für eine Datei oder ein Verzeichnis vom Anbieter an.
| [**PRJ_NOTIFICATION_CB**](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_notification_cb) | Übermittelt Benachrichtigungen zu Dateisystemvorgängen an den Anbieter.
| [**PRJ_QUERY_FILE_NAME_CB**](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_query_file_name_cb) | Bestimmt, ob ein angegebener Dateipfad im Hintergrundspeicher des Anbieters vorhanden ist.
| [**PRJ_START_DIRECTORY_ENUMERATION_CB**](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_start_directory_enumeration_cb) | Informiert den Anbieter darüber, dass eine Verzeichnisenumeration gestartet wird.