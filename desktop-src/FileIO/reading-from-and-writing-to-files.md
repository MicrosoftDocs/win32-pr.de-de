---
description: Eine Anwendung liest aus einer Datei und schreibt sie mithilfe der Funktionen ReadFile, ReadFileEx, WriteFile und WriteFileEx in eine Datei.
ms.assetid: 14ecb06c-3f80-47b8-9964-6a2c3b572300
title: Lesen aus und Schreiben in Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b88de3510a681839a9592bed4755de6249f79db117d94985ddb00320381b92c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119533320"
---
# <a name="reading-from-and-writing-to-files"></a>Lesen aus und Schreiben in Dateien

Eine Anwendung liest mithilfe der Funktionen [**ReadFile,**](/windows/desktop/api/FileAPI/nf-fileapi-readfile) [**ReadFileEx,**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile)und [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) aus einer Datei und schreibt sie in diese. Diese Funktionen erfordern ein Handle für eine Datei, die zum Lesen bzw. Schreiben geöffnet werden muss. Sie lesen und schreiben eine angegebene Anzahl von Bytes an der vom Dateizeiger angegebenen Position. Die Daten werden genau wie angegeben gelesen und geschrieben. die Funktionen formatieren die Daten nicht.

Wenn der Dateizeiger das Ende einer Datei erreicht und die Anwendung versucht, aus der Datei zu lesen, tritt kein Fehler auf, aber es werden keine Bytes gelesen. Daher bedeutet das Lesen von null Bytes ohne Fehler, dass die Anwendung das Ende der Datei erreicht hat. Das Schreiben von 0 Bytes führt zu nichts.

Weitere Informationen finden Sie in den folgenden Themen.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                                                                           | Beschreibung                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [Positionieren eines Dateizeigers](positioning-a-file-pointer.md)<br/>                                                                         | Windows verwendet einen Dateizeiger, um gelesene oder geschriebene Bytes nachzuverfolgen.<br/>                                                       |
| [Lesen aus oder Schreiben in Dateien mithilfe eines Scatter-Gather Schemas](reading-from-or-writing-to-files-using-a-scatter-gather-scheme.md)<br/> | Beschreibt ein Punktdiagrammschema zum Lesen oder Schreiben nicht zusammenhängender Datenblöcke in einem Vorgang.<br/>                   |
| [Leeren System-Buffered E/A-Daten auf den Datenträger](flushing-system-buffered-i-o-data-to-disk.md)<br/>                                           | Windows speichert die Daten in Dateilese- und Schreibvorgängen in vom System verwalteten Datenpuffern, um die Datenträgerleistung zu optimieren.<br/> |
| [Abschneiden oder Erweitern von Dateien](truncating-or-extending-files.md)<br/>                                                                   | Eine Anwendung kann eine Datei durch Aufrufen von [**SetEndOfFile**](/windows/desktop/api/FileAPI/nf-fileapi-setendoffile)abschneiden oder erweitern.<br/>                             |



 

 

 




