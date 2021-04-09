---
title: 'Szenario 2: parserbeispiel mit etw-Ablauf Verfolgung'
description: Um einen etw-Ablauf Verfolgungs Bericht für die HTTP-Server-API-Komponente zu generieren, führen Sie die Schritte wie im Abschnitt \ 0034; Erstellen eines etw-Ablauf Verfolgungs Berichts \ 0034; Abschnitt des Beispiels "Szenario 1 http-Timeout" mit etw-Ablauf Verfolgung und Netsh-Befehlen, aber reproduzieren des Fehlers, der für dieses Szenario spezifisch ist.
ms.assetid: 2ccd2927-8a64-40a8-a29b-4b680a942f7f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 866c566973b660e4e665226fbf9b4a266b086b6b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104039002"
---
# <a name="scenario-2-parser-example-using-etw-tracing"></a>Szenario 2: parserbeispiel mit etw-Ablauf Verfolgung

Um einen etw-Ablauf Verfolgungs Bericht für die HTTP-Server-API-Komponente zu generieren, führen Sie die Schritte wie im Abschnitt "Generieren eines etw-Ablauf Verfolgungs Berichts" unter [Szenario 1: Beispiel für http-Timeout mit etw-Ablauf Verfolgung und Netsh-Befehlen](scenario-1--http-timeout-example-using-etw-tracing-and-netsh-commands.md)aus, aber reproduzieren Sie den für dieses Szenario spezifischen Fehler. In diesem Beispiel greifen Sie von einem Client Computer aus auf die Webanwendung zu, was dazu führt, dass die Meldung "400 Bad Request" auf dem Client angezeigt wird. Diese Schritte werden auf dem Server ausgeführt, da die Webanwendung gehostet wird.

## <a name="viewing-the-trace-and-diagnosing"></a>Anzeigen der Ablauf Verfolgung und Diagnose

Die resultierende CSV-Datei für Ablauf Verfolgungen kann in Excel oder einem beliebigen Tool angezeigt werden, das das CSV-Format unterstützt. Tabelle 2 unten zeigt Auszüge aus einer Beispieldatei für die Ablauf Verfolgung (httptrace.csv). Im Ablauf Verfolgungs Bericht wird in der Spalte "Ebene" ein Eintrag mit dem Wert "2" angezeigt, der einen Fehler darstellt. Wie bereits erwähnt, befolgt die HTTP-Server-API-Komponente die ETW-Ebenen, die im komplexen Typ des Artikels [leveltype komplexer Typen](../wes/eventmanifestschema-leveltype-complextype.md)definiert sind.

Die ETW-Ebenen umfassen: 1 kritisch; 2 Fehler 3 Warnung; 4 Informations Informationen; 5 ausführlich.

Mit diesem Fehler meldet der Ereignistyp (Typspalte) "parameterequestfailed". In den nachfolgenden Spalten für das Ereignis "parameterequestfailed" wird der Eintrag "invalidhost" angezeigt. Dieser Eintrag bedeutet, dass der identifizierte Host in der HTTP-Anforderung gemäß dem HTTP-Protokoll falsch ist. Beachten Sie, dass die Spalte mit dem Eintrag "invalidhost" aus Gründen der Übersichtlichkeit nicht in der Tabelle enthalten ist, und um zu vermeiden, dass nicht zusammenhängende Spalten durchsucht werden.

Um dieses Problem zu beheben, sollte der WebClient korrigiert werden, damit er mit der http-RFC kompatibel ist. 

| Ereignisname                    | type               | Ereignis-ID | Version | Channel | Ebene |
|-------------------------------|--------------------|----------|---------|---------|-------|
| EventTrace                    | Header             | 0        | 2       | 0       | 0     |
| Microsoft-Windows-HttpService | Addurl             | 31       | 0       | 16      | 4     |
| Microsoft-Windows-HttpService | Verbindung herstellen        | 21       | 0       | 16      | 4     |
| Microsoft-Windows-HttpService | "Config"        | 22       | 0       | 16      | 4     |
| Microsoft-Windows-HttpService | Recvreq            | 1        | 0       | 16      | 4     |
| Microsoft-Windows-HttpService | "Parameterequestfailed" | 52       | 0       | 16      | 2     |
| Microsoft-Windows-HttpService | Logfilewrite       | 51       | 0       | 16      | 4     |



 

Tabelle 2: Auszüge aus einem Beispiel für eine Ablauf Verfolgung für ein Verarbeitungs Problem

 

 