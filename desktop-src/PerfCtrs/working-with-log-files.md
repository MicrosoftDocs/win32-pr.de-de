---
description: Um eine Protokolldatei zum Lesen zu öffnen, rufen Sie PdhOpenQuery auf, und geben Sie einen Pfad zur Protokolldatei an.
ms.assetid: 1d8f8662-df1f-4f84-8b65-c152f79cc5c6
title: Arbeiten mit Protokolldateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82281694b72a2c28bb0e65ee4db16bd9ba33b8ed9c6e5e74dbf6c6cbf559507a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143743"
---
# <a name="working-with-log-files"></a>Arbeiten mit Protokolldateien

Um eine Protokolldatei zum Lesen zu öffnen, rufen [**Sie PdhOpenQuery**](/windows/desktop/api/Pdh/nf-pdh-pdhopenquerya) auf, und geben Sie einen Pfad zur Protokolldatei an. Um eine Protokolldatei zum Schreiben zu öffnen, müssen Sie [**PdhOpenLog aufrufen.**](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga) Um eine Protokolldatei zu schließen, rufen Sie [**entweder PdhCloseQuery**](/windows/desktop/api/Pdh/nf-pdh-pdhclosequery) oder [**PdhCloseLog**](/windows/desktop/api/Pdh/nf-pdh-pdhcloselog) auf, je nachdem, welche Funktion Sie zum Öffnen der Protokolldatei verwendet haben.

## <a name="reading-from-a-log-file"></a>Lesen aus einer Protokolldatei

Das Lesen von Leistungsdaten aus einer Protokolldatei ist identisch mit dem Lesen von Daten aus einer Echtzeitquelle. Sie öffnen eine Abfrage, fügen der Abfrage Leistungsindikatoren hinzu und rufen [**PdhCollectQueryData**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydata) auf, um ein Beispiel aus der Protokolldatei zu sammeln. **PdhCollectQueryData gibt** PDH NO MORE DATA zurück, wenn \_ Sie das Ende der \_ \_ Protokolldatei erreichen.

Jedes Beispiel in der Protokolldatei enthält einen Zeitstempel für den Zeitpunkt, zu dem es ursprünglich gesammelt und in die Protokolldatei geschrieben wurde. Um den Zeitstempel für das erste und letzte Beispiel in der Protokolldatei abzurufen, rufen Sie die [**PdhGetDataSourceTimeRange-Funktion**](/windows/desktop/api/Pdh/nf-pdh-pdhgetdatasourcetimerangea) auf. Wenn Sie die aus dem Protokoll gelesenen Beispiele auf einen bestimmten Zeitbereich beschränken möchten, finden Sie weitere Informationen unter Festlegen eines [Zeitbereichs für eine Abfrage.](setting-a-time-range-for-a-query.md)

Wenn Sie nicht wissen, welche Leistungsobjekte und Leistungsindikatoren in der Protokolldatei vorhanden sind, können Sie [**PdhEnumObjects**](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectsa) aufrufen, um die Liste der Objekte zu bestimmen. Bei einem Objekt können Sie [**entweder PdhEnumObjectItems**](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectitemsa) oder [**PdhExpandWildCardPath**](/windows/desktop/api/Pdh/nf-pdh-pdhexpandwildcardpatha) aufrufen, um eine Liste der Instanzen und Leistungsindikatoren des Objekts abzurufen, die in der Protokolldatei enthalten sind.

Wenn Sie [**PdhEnumObjectItems**](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectitemsa)aufrufen, verwenden Sie die Instanz- und Leistungsindikatorlisten, um einen Pfad für jede mögliche Kombination aus Instanz und Indikator zu erstellen. Wenn Sie [**PdhAddCounter**](/windows/desktop/api/Pdh/nf-pdh-pdhaddcountera) aufrufen, um den Zähler zur Abfrage hinzuzufügen, ist die Funktion nicht in der Angegebenen Kombination enthalten.

Wenn Sie [**PdhExpandWildCardPath**](/windows/desktop/api/Pdh/nf-pdh-pdhexpandwildcardpatha)verwenden, können Sie einen Pfad erstellen, der einen Platzhalter für den Instanznamen und den Leistungsindikator enthält, z. B. \\ object( \* ) \\ \* . Die Funktion gibt PDH \_ INVALID \_ PATH zurück, wenn das Objekt keine -Instanz enthält. Rufen Sie in diesem Fall **PdhExpandWildCardPath** mithilfe eines Platzhalters nur für den Indikator auf, z. B. \\ objekt \\ \* .

Neuere Betriebssysteme können Protokolldateien lesen, die unter älteren Betriebssystemen generiert wurden. Protokolldateien, die unter den Betriebssystemen Windows Vista und höher erstellt wurden, können jedoch unter früheren Betriebssystemen nicht gelesen werden.

Ein Beispiel zum Lesen von Daten aus einer Protokolldatei finden Sie unter [Lesen von Leistungsdaten aus einer Protokolldatei.](reading-performance-data-from-a-log-file.md)

## <a name="reading-from-multiple-log-files"></a>Lesen aus mehreren Protokolldateien

Wenn Sie eine Abfrage erstellen müssen, die aus mehreren Protokolldateien liest, rufen Sie [**PdhBindInputDataSource**](/windows/desktop/api/Pdh/nf-pdh-pdhbindinputdatasourcea) auf, um die Protokolldateien zu binden. Anschließend müssen Sie PDH-Funktionen verwenden, die auf "H" enden, z. B. [**PdhOpenQueryH.**](/windows/desktop/api/Pdh/nf-pdh-pdhopenqueryh)

## <a name="writing-to-a-log-file"></a>Schreiben in eine Protokolldatei

Rufen Sie vor dem Schreiben in eine Protokolldatei [**PdhOpenQuery**](/windows/desktop/api/Pdh/nf-pdh-pdhopenquerya) auf, um eine Abfrage zu erstellen und die Quelle der Leistungsdaten anzugeben, entweder Echtzeitdaten oder eine Protokolldatei. Fügen Sie dann die Leistungsindikatoren hinzu, die Sie abfragen möchten.

Um die Zieldatei zu öffnen, rufen Sie [**PdhOpenLog auf.**](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga) Geben Sie die Abfrage an, wenn Sie die Protokolldatei öffnen. Rufen Sie [**PdhUpdateLog**](/windows/desktop/api/Pdh/nf-pdh-pdhupdateloga)auf, um die Leistungsdaten zu sammeln und in die Protokolldatei zu schreiben.

Wenn die Indikatordaten in eine durch Trennzeichen getrennte (.csv) oder tabstoppgetrennte Protokolldatei (TSV) geschrieben werden und der Pfad eine Platzhalterinstanz enthält, wird der Pfad erweitert, und nur die Instanzen, die zum Zeitpunkt der Erweiterung des Pfads vorhanden sind, werden in die Protokolldatei aufgenommen. Für binäre (BLG)- oder SQL-Protokolldateien wird der Platzhalter jedoch nicht erweitert, sodass die Protokolldatei Instanzen enthält, die während der Protokollierung erstellt werden.

Ein Beispiel zum Schreiben von Daten in eine Protokolldatei finden Sie unter [Schreiben von Leistungsdaten in eine Protokolldatei.](writing-performance-data-to-a-log-file.md)

## <a name="compressing-a-log-file"></a>Komprimieren einer Protokolldatei

Sie können die [**PdhComputeCounterStatistics-Funktion**](/windows/desktop/api/Pdh/nf-pdh-pdhcomputecounterstatistics) verwenden, um eine Protokolldatei zu komprimieren. Lesen Sie beispielsweise zehn Datensätze aus einer Protokolldatei, rufen **Sie PdhComputeCounterStatistics** auf, um den Mittelwert zu berechnen, und schreiben Sie dann den Mittelwert in eine Ausgabeprotokolldatei.

Das folgende Thema enthält zusätzliche Informationen zur Verwendung einer Protokolldatei.

-   [Abrufen der Größe einer Protokolldatei](getting-the-size-of-a-log-file.md)

 

 



