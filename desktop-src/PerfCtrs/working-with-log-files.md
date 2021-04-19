---
description: Um eine Protokolldatei zum Lesen zu öffnen, nennen Sie pdhopesquery, und geben Sie einen Pfad zur Protokolldatei an.
ms.assetid: 1d8f8662-df1f-4f84-8b65-c152f79cc5c6
title: Arbeiten mit Protokolldateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba2032b90036f8f58c07d8c7e80e7e7ac2b2701c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357750"
---
# <a name="working-with-log-files"></a>Arbeiten mit Protokolldateien

Um eine Protokolldatei zum Lesen zu öffnen, nennen Sie [**pdhopesquery**](/windows/desktop/api/Pdh/nf-pdh-pdhopenquerya) , und geben Sie einen Pfad zur Protokolldatei an. Um eine Protokolldatei zum Schreiben zu öffnen, müssen Sie [**pdhoptolog**](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga)abrufen. Um eine Protokolldatei zu schließen, müssen Sie je nach Funktion, die Sie zum Öffnen der Protokolldatei verwendet haben, entweder [**pdhclosequery**](/windows/desktop/api/Pdh/nf-pdh-pdhclosequery) oder [**pdhcloselog**](/windows/desktop/api/Pdh/nf-pdh-pdhcloselog) abrufen.

## <a name="reading-from-a-log-file"></a>Lesen aus einer Protokolldatei

Das Lesen von Leistungsdaten aus einer Protokolldatei ist identisch mit dem Lesen von Daten aus einer echt Zeit Quelle – Sie öffnen eine Abfrage, fügen der Abfrage Leistungsindikatoren hinzu und nennen [**pdhcollectquerydata**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydata) , um ein Beispiel aus der Protokolldatei zu erfassen. **Pdhcollectquerydata** gibt PDH \_ keine \_ weiteren \_ Daten zurück, wenn Sie das Ende der Protokolldatei erreichen.

Jedes Beispiel in der Protokolldatei enthält einen Zeitstempel für den Zeitpunkt, zu dem es ursprünglich gesammelt und in die Protokolldatei geschrieben wurde. Um den Zeitstempel für das erste und letzte Beispiel in der Protokolldatei abzurufen, rufen Sie die [**pdhgetdatasourcetimerange**](/windows/desktop/api/Pdh/nf-pdh-pdhgetdatasourcetimerangea) -Funktion auf. Wenn Sie die aus dem Protokoll gelesenen Beispiele auf einen bestimmten Zeitraum beschränken möchten, finden Sie weitere Informationen unter [Festlegen eines Zeit Bereichs für eine Abfrage](setting-a-time-range-for-a-query.md).

Wenn Sie nicht wissen, welche Leistungs Objekte und-Indikatoren in der Protokolldatei vorhanden sind, können Sie [**pdhenumubjects**](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectsa) zum Ermitteln der Liste der Objekte abrufen. Bei einem Objekt können Sie entweder [**pdhenumubjectitems**](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectitemsa) oder [**PdhExpandWildCardPath**](/windows/desktop/api/Pdh/nf-pdh-pdhexpandwildcardpatha) aufrufen, um eine Liste der Instanzen und Indikatoren des Objekts abzurufen, die in der Protokolldatei enthalten sind.

Wenn Sie [**pdhenumubjectitems**](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectitemsa)aufrufen, verwenden Sie die Instanz-und die Counter-Listen, um einen Pfad für jede mögliche Kombination von Instanz und Counter zu erstellen. Wenn Sie [**pdhaddcounter**](/windows/desktop/api/Pdh/nf-pdh-pdhaddcountera) zum Hinzufügen des Zählers zur Abfrage abrufen, schlägt die Funktion fehl, wenn die Protokolldatei die angegebene Kombination nicht enthält.

Wenn Sie [**PdhExpandWildCardPath**](/windows/desktop/api/Pdh/nf-pdh-pdhexpandwildcardpatha)verwenden, können Sie einen Pfad erstellen, der einen Platzhalter für den Instanznamen und-Wert enthält, z \\ . b. Object ( \* ) \\ \* . Die Funktion gibt einen ungültigen PDH-Pfad zurück, \_ \_ Wenn das Objekt keine Instanz enthält. Nennen Sie in diesem Fall **PdhExpandWildCardPath** mithilfe eines Platzhalters nur für Counter (z \\ . b. Object) \\ \* .

Neuere Betriebssysteme können Protokolldateien lesen, die auf älteren Betriebssystemen generiert wurden. Protokolldateien, die unter Windows Vista und späteren Betriebssystemen erstellt wurden, können jedoch nicht unter früheren Betriebssystemen gelesen werden.

Ein Beispiel für das Lesen von Daten aus einer Protokolldatei finden Sie unter [Lesen von Leistungsdaten aus einer Protokolldatei](reading-performance-data-from-a-log-file.md).

## <a name="reading-from-multiple-log-files"></a>Lesen aus mehreren Protokolldateien

Wenn Sie eine Abfrage erstellen müssen, die aus mehreren Protokolldateien liest, rufen Sie [**pdhbindinputdatasource**](/windows/desktop/api/Pdh/nf-pdh-pdhbindinputdatasourcea) auf, um die Protokolldateien zu binden. Sie müssen dann PDH-Funktionen verwenden, die mit "H" enden, z. b. " [**pdhopenqueryh**](/windows/desktop/api/Pdh/nf-pdh-pdhopenqueryh)".

## <a name="writing-to-a-log-file"></a>Schreiben in eine Protokolldatei

Rufen Sie vor dem Schreiben in eine Protokolldatei [**pdhopenquery**](/windows/desktop/api/Pdh/nf-pdh-pdhopenquerya) auf, um eine Abfrage zu erstellen, und geben Sie die Quelle der Leistungsdaten an (entweder Echtzeitdaten oder eine Protokolldatei). Fügen Sie dann die Leistungsindikatoren hinzu, die Sie Abfragen möchten.

Um die Zieldatei zu öffnen, nennen Sie [**pdhoptolog**](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga). Geben Sie die Abfrage an, wenn Sie die Protokolldatei öffnen. Um die Leistungsdaten zu erfassen und in die Protokolldatei zu schreiben, nennen Sie [**pdhupdatelog**](/windows/desktop/api/Pdh/nf-pdh-pdhupdateloga).

Wenn die gegen Daten in eine durch Trennzeichen getrennte (. CSV) oder durch Tabstopps getrennte (. TSV) Protokolldatei geschrieben werden und der Pfad eine Platzhalter Instanz enthält, wird der Pfad erweitert, und nur die Instanzen, die zum Zeitpunkt der Erweiterung des Pfads vorhanden sind, sind in der Protokolldatei enthalten. Bei Binärdateien (. blg) oder SQL-Protokolldateien wird der Platzhalter jedoch nicht erweitert, sodass die Protokolldatei-Instanzen enthält, die während der Protokollierung erstellt werden.

Ein Beispiel für das Schreiben von Daten in eine Protokolldatei finden Sie unter [Schreiben von Leistungsdaten in eine Protokolldatei](writing-performance-data-to-a-log-file.md).

## <a name="compressing-a-log-file"></a>Komprimieren einer Protokolldatei

Sie können die [**pdhcomputecounterstatistics**](/windows/desktop/api/Pdh/nf-pdh-pdhcomputecounterstatistics) -Funktion verwenden, um eine Protokolldatei zu komprimieren. Lesen Sie z. b. zehn Datensätze aus einer Protokolldatei, und nennen Sie **pdhcomputecounterstatistics** , um den Mittelwert zu berechnen und dann den Mittelwert in eine Ausgabeprotokoll Datei zu schreiben.

Das folgende Thema enthält zusätzliche Informationen zur Verwendung einer Protokolldatei.

-   [Die Größe einer Protokolldatei wird erhalten.](getting-the-size-of-a-log-file.md)

 

 



