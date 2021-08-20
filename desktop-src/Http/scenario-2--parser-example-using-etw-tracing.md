---
title: 'Szenario 2: Parserbeispiel mit ETW-Ablaufverfolgung'
description: Um einen ETW-Ablaufverfolgungsbericht für die HTTP Server-API-Komponente zu generieren, führen Sie die Schritte aus, wie in \ 0034 gezeigt. Generieren eines ETW-Ablaufverfolgungsberichts \ 0034; Abschnitt des HTTP-Timeoutbeispiels für Szenario 1 mit ETW-Ablaufverfolgung und Netsh-Befehlen, aber reproduzieren Sie den für dieses Szenario spezifischen Fehler.
ms.assetid: 2ccd2927-8a64-40a8-a29b-4b680a942f7f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62ec0448801334dddb1f964473a925ff18183af992157a55c0d90d7b259f1159
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117996198"
---
# <a name="scenario-2-parser-example-using-etw-tracing"></a>Szenario 2: Parserbeispiel mit ETW-Ablaufverfolgung

Um einen ETW-Ablaufverfolgungsbericht für die HTTP Server-API-Komponente zu generieren, führen Sie die Schritte aus, wie im Abschnitt "Generieren eines ETW-Ablaufverfolgungsberichts" von Szenario [1: HTTP-Timeoutbeispiel](scenario-1--http-timeout-example-using-etw-tracing-and-netsh-commands.md)mit ETW-Ablaufverfolgung und Netsh-Befehlen gezeigt, aber reproduzieren Sie den für dieses Szenario spezifischen Fehler. In diesem Beispiel greifen Sie von einem Clientcomputer aus auf die Webanwendung zu, was dazu führt, dass die Meldung "400 bad request" (400 fehlerhafte Anforderung) auf dem Client angezeigt wird. Diese Schritte werden auf dem Server ausgeführt, da er die Webanwendung hosten wird.

## <a name="viewing-the-trace-and-diagnosing"></a>Anzeigen der Ablaufverfolgung und Diagnose

Die resultierende CSV-Datei für Ablaufverfolgungen kann in einem Excel tool angezeigt werden, das das CSV-Format unterstützt. Tabelle 2 unten zeigt Ausschnitte aus einer Beispiel-Ablaufverfolgungsdatei (httptrace.csv). Im Ablaufverfolgungsbericht zeigt die Spalte "Level" einen Eintrag mit dem Wert "2" an, der einen Fehler darstellt. Wie bereits erwähnt, folgt die HTTP-Server-API-Komponente den ETW-Ebenen, die im Artikel Komplexer Typ des [komplexen Typs LevelType definiert sind.](../wes/eventmanifestschema-leveltype-complextype.md)

Die ETW-Ebenen umfassen: 1 Kritisch; 2 Fehler; 3 Warnung; 4 Information; 5 Ausführlich.

Bei diesem Fehler meldet der Ereignistyp (Spalte Typ) "ParseRequestFailed". In den nachfolgenden Spalten für das ParseRequestFailed-Ereignis wird der Eintrag "InvalidHost" angezeigt. Dieser Eintrag bedeutet, dass der identifizierte Host in der HTTP-Anforderung gemäß dem HTTP-Protokoll falsch ist. Beachten Sie, dass die Spalte mit dem Eintrag "InvalidHost" aus Gründen der Kürze und zur Vermeidung des Auszugs nicht zusammenhängender Spalten nicht in der Tabelle enthalten ist.

Um dieses Analyseproblem zu beheben, sollte der Webclient korrigiert werden, damit er mit HTTP RFC kompatibel ist. 

| Ereignisname                    | Typ               | Ereignis-ID | Version | Kanal | Ebene |
|-------------------------------|--------------------|----------|---------|---------|-------|
| EventTrace                    | Header             | 0        | 2       | 0       | 0     |
| Microsoft-Windows-HttpService | AddUrl             | 31       | 0       | 16      | 4     |
| Microsoft-Windows-HttpService | ConnConnect        | 21       | 0       | 16      | 4     |
| Microsoft-Windows-HttpService | ConnIdAssgn        | 22       | 0       | 16      | 4     |
| Microsoft-Windows-HttpService | RecvReq            | 1        | 0       | 16      | 4     |
| Microsoft-Windows-HttpService | ParseRequestFailed | 52       | 0       | 16      | 2     |
| Microsoft-Windows-HttpService | LogFileWrite       | 51       | 0       | 16      | 4     |



 

Tabelle 2: Auszüge aus einem Beispiel-Ablaufverfolgungsbericht für ein Analyseproblem

 

 