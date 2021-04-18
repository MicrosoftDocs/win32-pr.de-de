---
description: Eine Anwendung liest aus einer Datei und schreibt Sie mithilfe der Funktionen "Infofile", "infofileex", "Write file" und "Write fileex".
ms.assetid: 14ecb06c-3f80-47b8-9964-6a2c3b572300
title: Lesen aus und Schreiben in Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffd0e6518ce2430e18bbb11033023ee6dc274573
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352453"
---
# <a name="reading-from-and-writing-to-files"></a>Lesen aus und Schreiben in Dateien

Eine Anwendung liest aus einer Datei und schreibt Sie mithilfe der Funktionen " [**Infofile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile)", " [**infofileex**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex)", " [**Write File**](/windows/desktop/api/FileAPI/nf-fileapi-writefile)" und " [**Write fileex**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) ". Diese Funktionen erfordern ein Handle für eine Datei, die zum Lesen bzw. Schreiben geöffnet werden soll. Sie lesen und schreiben eine angegebene Anzahl von Bytes an dem Speicherort, der durch den Dateizeiger angegeben wird. Die Daten werden genau wie angegeben gelesen und geschrieben. die-Funktionen formatieren die Daten nicht.

Wenn der Dateizeiger das Ende einer Datei erreicht und die Anwendung versucht, aus der Datei zu lesen, tritt kein Fehler auf, aber es werden keine Bytes gelesen. Daher bedeutet das Lesen von 0 Bytes ohne Fehler, dass die Anwendung das Ende der Datei erreicht hat. Das Schreiben von 0 Bytes bewirkt nichts.

Weitere Informationen finden Sie in den nachfolgenden Themen.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                                                                           | BESCHREIBUNG                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [Positionieren eines Dateizeigers](positioning-a-file-pointer.md)<br/>                                                                         | Windows verwendet einen Dateizeiger, um die gelesenen oder geschriebenen Bytes nachzuverfolgen.<br/>                                                       |
| [Lesen aus oder schreiben in Dateien mit einem Scatter-Gather Schema](reading-from-or-writing-to-files-using-a-scatter-gather-scheme.md)<br/> | Beschreibt ein Scatter-Gather-Schema zum Lesen oder Schreiben von nicht zusammenhängenden Datenblöcken in einem Vorgang.<br/>                   |
| [Leeren von System-Buffered e/a-Daten auf den Datenträger](flushing-system-buffered-i-o-data-to-disk.md)<br/>                                           | Windows speichert die Daten in Datei Lese-und Schreibvorgängen in vom System verwalteten Daten Puffern, um die Datenträger Leistung zu optimieren.<br/> |
| [Abschneiden oder Erweitern von Dateien](truncating-or-extending-files.md)<br/>                                                                   | Eine Anwendung kann eine Datei durch Aufrufen von [**SetEndOfFile**](/windows/desktop/api/FileAPI/nf-fileapi-setendoffile)abschneiden oder erweitern.<br/>                             |



 

 

 




