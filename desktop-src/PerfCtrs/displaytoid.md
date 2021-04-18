---
description: Die displaytoid-Tabelle bezieht die vom System Monitor angezeigte benutzerfreundliche Zeichenfolge auf die GUID, die in den anderen Tabellen gespeichert ist.
ms.assetid: 414d16f1-ab6f-45f0-9287-154810543a6d
title: Display toid
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b71ae8c4ebaafc80d98580a13a83e3cc7cff815
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347367"
---
# <a name="displaytoid"></a>Display toid

Die **displaytoid** -Tabelle bezieht die vom System Monitor angezeigte benutzerfreundliche Zeichenfolge auf die GUID, die in den anderen Tabellen gespeichert ist.

Die Tabelle **displaytoid** definiert die folgenden Felder:

-   **GUID:** Eindeutiger Bezeichner, der für ein Protokoll generiert wurde. Dieses Feld ist der Primärschlüssel dieser Tabelle.
-   **RunId:** Reserviert für interne Verwendung.
-   **Display String:** Der Name der Protokolldatei, wie im System Monitor angezeigt.
-   **Logstarttime:** Zeitpunkt, zu dem der Protokollierungs Prozess im Format yyyy-mm-dd hh: mm: SS: nnn gestartet wurde.
-   **Logstoptime:** Zeitpunkt, zu dem der Protokollierungs Prozess im Format yyyy-mm-dd hh: mm: SS: nnn beendet wurde. Mehrere Protokolldateien mit demselben **DisplayString** -Wert können unterschieden werden, indem Sie den Wert in diesem und den **logstarttime** -Feldern verwenden. Mit den Werten in den Feldern **logstarttime** und **logstoptime** kann auch schnell auf die gesamte Sammlungszeit zugegriffen werden.
-   **Anzahl von Datensätzen:** Anzahl von Samplings, die in der Tabelle für jede Protokoll Sammlung gespeichert sind.
-   **Minutestoutc:** Der Wert, der verwendet wird, um die in UTC-Zeit gespeicherten Zeilendaten in die Ortszeit zu konvertieren.
-   **TimeZoneName:** Der Name der Zeitzone, in der die Daten erfasst wurden. Wenn Sie Daten aus einer Datei sammeln oder erneut protokolliert haben, die auf Systemen in ihrer eigenen Zeitzone gesammelt wurde, wird in diesem Feld der Speicherort angezeigt.

**Hinweis**  Vor Windows Vista wurden die Datensammler Sätze in der Registrierung unter gespeichert.

**HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ Services \\ SysmonLog- \\ Protokoll Abfragen**

. Die oben aufgeführten Felder entsprechen nicht den Werten in der Registrierung. Für Windows Vista werden die Datensammler Sätze nicht in der Registrierung gespeichert.

 

 



