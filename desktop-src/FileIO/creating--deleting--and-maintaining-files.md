---
description: Funktionen zum Erstellen, Löschen und Verwalten von Dateien.
ms.assetid: b9cf0ddf-efda-4997-bcc3-3056026c1264
title: Erstellen, Löschen und Verwalten von Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff20362e2ff5f1d8b01b515c7cbbb9fae250d930b2610c49c5e8aaeeabe7b401
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982120"
---
# <a name="creating-deleting-and-maintaining-files"></a>Erstellen, Löschen und Verwalten von Dateien

In den folgenden Themen wird beschrieben, wie Sie Dateien erstellen, löschen und verwalten.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                   | Beschreibung                                                                                                                                                                                                                                                                 |
|-------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Benennen von Dateien, Pfaden und Namespaces](naming-a-file.md)<br/>     | Regeln, Konventionen und Einschränkungen von Namen für Dateien und Verzeichnisse, einschließlich Namenskonventionen, kurzen Dateinamen im Vergleich zu langen Dateinamen, vollqualifizierten Pfaden im Vergleich zu relativen Pfaden, Beschränkung der maximalen Pfadlänge, 8.3 Dateinamen und Namespaces.<br/>            |
| [Erstellen und Öffnen von Dateien](creating-and-opening-files.md)<br/> | Überlegungen zum Erstellen oder Öffnen einer Datei mithilfe der [**CreateFile-Funktion.**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)<br/>                                                                                                                                                            |
| [Verschieben und Ersetzen von Dateien](moving-and-replacing-files.md)<br/> | Überlegungen zum Verschieben und Ersetzen von Dateien mithilfe der Funktionen CopyFileEx, CreateFile, Replacefile und MoveFileEx.<br/>                                                                                                                                        |
| [Schließen und Löschen von Dateien](closing-and-deleting-files.md)<br/> | Um Betriebssystemressourcen effizient zu verwenden, sollte eine Anwendung Dateien schließen, wenn sie nicht mehr benötigt werden, indem die [**CloseHandle-Funktion**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) verwendet wird. Wenn eine Datei geöffnet ist, wenn eine Anwendung beendet wird, schließt das System sie automatisch.<br/> |
| [Defragmentieren von Dateien](defragmenting-files.md)<br/>               | *Defragmentierung* ist der Prozess, bei dem Teile von Dateien auf einem Datenträger verschoben werden, um Dateien zu defragmentieren, d.h. Dateicluster auf einem Datenträger zu verschieben, um sie zusammenhängend zu machen.<br/>                                                                               |



 

 

