---
description: Die Tabelle DisplayToID bezieht die benutzerfreundlichen Zeichenfolgen, die vom Systemmonitor angezeigt werden, mit der GUID in den anderen Tabellen in Zusammenhang.
ms.assetid: 414d16f1-ab6f-45f0-9287-154810543a6d
title: DisplayToID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 485eab24a2c758b36e190e035a9442a032ebd683f3f5ea052bd37992ad14c85f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033910"
---
# <a name="displaytoid"></a>DisplayToID

Die **Tabelle DisplayToID** bezieht die benutzerfreundlichen Zeichenfolgen, die vom Systemmonitor angezeigt werden, mit der GUID in den anderen Tabellen in Zusammenhang.

Die **Tabelle DisplayToID** definiert die folgenden Felder:

-   **GUID:** Eindeutiger Bezeichner, der für ein Protokoll generiert wird. Dieses Feld ist der Primärschlüssel dieser Tabelle.
-   **RunID:** Für die interne Verwendung reserviert.
-   **DisplayString:** Der Name der Protokolldatei, wie er im Systemmonitor angezeigt wird.
-   **LogStartTime:** Zeitpunkt, zu dem der Protokollierungsprozess im Format yyyy-mm-dd hh:mm:ss:nnn gestartet wurde.
-   **LogStopTime:** Uhrzeit, zu der der Protokollierungsprozess im Format yyyy-mm-dd hh:mm:ss:nnn beendet wurde. Mehrere Protokolldateien mit dem gleichen **DisplayString-Wert** können mithilfe des Werts in diesem und den **LogStartTime-Feldern unterschieden** werden. Die Werte in den **Feldern LogStartTime** und **LogStopTime** ermöglichen auch den schnellen Zugriff auf die gesamte Sammlungszeit.
-   **NumberOfRecords:** Anzahl der in der Tabelle gespeicherten Beispiele für jede Protokollsammlung.
-   **MinutesToUTC:** Der Wert, der verwendet wird, um die in UTC-Zeit gespeicherten Zeilendaten in die Ortszeit zu konvertieren.
-   **TimeZoneName:** Name der Zeitzone, in der die Daten gesammelt wurden. Wenn Sie Daten aus einer Datei sammeln oder erneut aus einer Datei gespeichert haben, die auf Systemen in Ihrer eigenen Zeitzone gesammelt wurde, wird in diesem Feld der Speicherort angezeigt.

**Hinweis:**  Vor der Windows Vista wurden die Datensammlersätze in der Registrierung unter gespeichert.

**HKEY \_ LOCAL MACHINE SYSTEM \_ \\ \\ CurrentControlSet \\ Services \\ SysmonLog-Protokollabfragen \\**

. Die oben aufgeführten Felder entsprechen nicht den Werten in der Registrierung. Für Windows Vista werden die Datensammlersätze nicht in der Registrierung gespeichert.

 

 



