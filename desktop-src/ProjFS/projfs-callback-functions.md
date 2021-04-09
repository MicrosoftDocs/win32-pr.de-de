---
title: Projfs-Rückruf Funktionen
description: Die folgenden Rückruf Funktionen werden in projectedfslib. h deklariert.
ms.assetid: <GUID-GOES-HERE>
ms.date: 01/17/2020
ms.topic: article
ms.openlocfilehash: 1412fc4b406b668ad6651d69835f8cdea56857c5
ms.sourcegitcommit: 62e758931c610782807c7c9fad284921a6c56232
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/22/2020
ms.locfileid: "103857940"
---
# <a name="callback-functions"></a>Rückruf Funktionen

Die folgenden Rückruf Funktionen werden in projectedfslib. h deklariert.

## <a name="in-this-section"></a>In diesem Abschnitt

| Thema | BESCHREIBUNG |
|-|-|
| [**PRJ_CANCEL_COMMAND_CB**](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_cancel_command_cb) | Benachrichtigt den Anbieter, dass ein Vorgang eines früheren Aufrufs eines Rückrufs abgebrochen werden soll. |
| [**PRJ_END_DIRECTORY_ENUMERATION_CB**](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_end_directory_enumeration_cb) | Informiert den Anbieter darüber, dass sich eine verzeichnisenumeration befindet. |
| [**PRJ_GET_DIRECTORY_ENUMERATION_CB**](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_directory_enumeration_cb) | Fordert verzeichnisenumerationsinformationen vom Anbieter an.
| [**PRJ_GET_FILE_DATA_CB**](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_file_data_cb) | Fordert den Inhalt des primären Datenstroms einer Datei an.
| [**PRJ_GET_PLACEHOLDER_INFO_CB**](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_placeholder_info_cb) | Fordert Informationen für eine Datei oder ein Verzeichnis vom Anbieter an.
| [**PRJ_NOTIFICATION_CB**](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_notification_cb) | Übermittelt Benachrichtigungen an den Anbieter zu Dateisystem Vorgängen.
| [**PRJ_QUERY_FILE_NAME_CB**](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_query_file_name_cb) | Bestimmt, ob ein angegebener Dateipfad im Sicherungs Speicher des Anbieters vorhanden ist.
| [**PRJ_START_DIRECTORY_ENUMERATION_CB**](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_start_directory_enumeration_cb) | Informiert den Anbieter darüber, dass eine verzeichnisenumeration gestartet wird.