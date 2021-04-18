---
description: Funktionen, die verwendet werden, um Dateien zu erstellen, zu löschen und zu verwalten.
ms.assetid: b9cf0ddf-efda-4997-bcc3-3056026c1264
title: Erstellen, löschen und warten von Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 921388e84ac44a42e0c24880b1b56971ba84c12b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352309"
---
# <a name="creating-deleting-and-maintaining-files"></a>Erstellen, löschen und warten von Dateien

In den folgenden Themen wird beschrieben, wie Dateien erstellt, gelöscht und gewartet werden.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                   | BESCHREIBUNG                                                                                                                                                                                                                                                                 |
|-------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Benennen von Dateien, Pfaden und Namespaces](naming-a-file.md)<br/>     | Regeln, Konventionen und Einschränkungen von Namen für Dateien und Verzeichnisse, einschließlich Benennungs Konventionen, kurzen Dateinamen im Vergleich zu langen Dateinamen, voll qualifizierten Pfaden im Vergleich zu relativen Pfaden, Einschränkung der maximalen Pfad Länge, 8,3-Dateinamen und Namespaces.<br/>            |
| [Erstellen und Öffnen von Dateien](creating-and-opening-files.md)<br/> | Überlegungen zum Erstellen oder öffnen [**einer Datei mithilfe der Funktion**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) "Funktion".<br/>                                                                                                                                                            |
| [Verschieben und Ersetzen von Dateien](moving-and-replacing-files.md)<br/> | Überlegungen zum Verschieben und Ersetzen von Dateien mithilfe der CopyFileEx-, der-Funktion, der ReplaceFile-Funktion und der-Funktion von "muvefileex".<br/>                                                                                                                                        |
| [Schließen und Löschen von Dateien](closing-and-deleting-files.md)<br/> | Um Betriebssystemressourcen effizient zu verwenden, sollte eine Anwendung Dateien schließen, wenn Sie nicht mehr benötigt werden, indem Sie die [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) -Funktion verwenden. Wenn eine Datei geöffnet ist, wenn eine Anwendung beendet wird, wird Sie vom System automatisch geschlossen.<br/> |
| [Defragmentieren von Dateien](defragmenting-files.md)<br/>               | *Defragmentierung* ist der Prozess, bei dem Teile von Dateien auf einem Datenträger verschoben werden, um Dateien zu defragmentieren, d. h. der Prozess des Verschiebens von Datei Clustern auf einem Datenträger, um Sie zusammenhängend zu machen.<br/>                                                                               |



 

 

