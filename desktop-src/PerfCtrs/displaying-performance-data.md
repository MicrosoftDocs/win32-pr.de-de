---
description: Die meisten Leistungsindikatoren erfordern zwei Stichprobenwerte, um einen sichtbaren Wert zu berechnen.
ms.assetid: 75e45baf-51c5-400c-a31f-92bdab4ee492
title: Anzeigen von Leistungsdaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c56a2882485c0bf21db6f1f00788fb927442219f020b1241ab4cd64619c7ec56
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117794011"
---
# <a name="displaying-performance-data"></a>Anzeigen von Leistungsdaten

Die meisten Leistungsindikatoren erfordern zwei Stichprobenwerte, um einen sichtbaren Wert zu berechnen. Die Formel für jeden Leistungsindikator bestimmt, ob der Indikator zwei Stichproben erfordert. Eine Liste der Leistungsindikatoren und deren Formeln finden Sie im Abschnitt Indikatortypen des [Windows Server 2003 Deployment Kit.](/previous-versions/windows/it-pro/windows-server-2003/cc776490(v=ws.10))

[Das Sammeln von Leistungsdaten](collecting-performance-data.md) zeigt, wie Beispieldaten abgerufen werden. Sobald Sie über die Beispiele verfügen, rufen Sie in der Regel [**PdhGetFormattedCounterValue**](/windows/desktop/api/Pdh/nf-pdh-pdhgetformattedcountervalue) auf, um einen anzeigebaren Wert zu berechnen.

Wenn Sie den Indikatorwert hoch- oder herunterskalieren müssen, um den Wert anzuzeigen, rufen Sie die [**PdhSetCounterScaleFactor-Funktion**](/windows/desktop/api/Pdh/nf-pdh-pdhsetcounterscalefactor) auf, bevor [**Sie PdhGetFormattedCounterValue**](/windows/desktop/api/Pdh/nf-pdh-pdhgetformattedcountervalue)aufrufen. Indikatorwerte können mit einer Potenz von zehn von einem Faktor von -7 auf 7 skaliert werden.

Wenn der Indikatorpfad ein Platzhalterzeichen für den Instanznamen enthält, rufen Sie [**PdhGetFormattedCounterArray**](/windows/desktop/api/Pdh/nf-pdh-pdhgetformattedcounterarraya) auf, um ein Array formatierter Indikatorwerte für jede gesammelte Instanz abzurufen.

Sie können auch die Funktionen [**PdhCalculateCounterFromRawValue**](/windows/desktop/api/Pdh/nf-pdh-pdhcalculatecounterfromrawvalue) und [**PdhFormatFromRawValue**](/windows/desktop/api/Pdh/nf-pdh-pdhformatfromrawvalue) verwenden, um einen darstellbaren Wert zu berechnen. Um diese Funktionen verwenden zu können, müssen Sie das gesammelte Beispiel nach jedem [**PdhCollectQueryData-Aufruf**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydata) abrufen und das Beispiel selbst speichern. Rufen Sie zum Abrufen des Beispiels die [**PdhGetRawCounterValue-**](/windows/desktop/api/Pdh/nf-pdh-pdhgetrawcountervalue) oder [**PdhGetRawCounterArray-Funktion**](/windows/desktop/api/Pdh/nf-pdh-pdhgetrawcounterarraya) auf. Rufen Sie für zeitbasierte Indikatorwerte [**PdhGetCounterTimeBase**](/windows/desktop/api/Pdh/nf-pdh-pdhgetcountertimebase) vor **PdhFormatFromRawValue** auf, um die Zeitbasis des Indikators abzurufen.

Wenn Sie Berechnungen mithilfe der Rohdaten ausführen, überprüfen Sie immer den **CStatus-Member** der [**PDH \_ RAW \_ COUNTER-Struktur,**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter) bevor Sie das Beispiel verwenden. Das Beispiel ist ungültig, wenn der Wert von **CStatus** nicht PDH \_ CSTATUS \_ NEW DATA oder \_ PDH \_ CSTATUS VALID DATA \_ \_ ist.

## <a name="displaying-statistics-for-a-counter"></a>Anzeigen von Statistiken für einen Leistungsindikator

Wenn Sie die Minimal-, Höchst- und Mittelwerte eines Zählers berechnen möchten, rufen Sie die [**PdhComputeCounterStatistics-Funktion**](/windows/desktop/api/Pdh/nf-pdh-pdhcomputecounterstatistics) auf. Wenn Sie Beispiele sammeln, speichern Sie die [**PDH \_ RAW \_ COUNTER-Strukturen**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter) in einem Array, das Sie an **PdhComputeCounterStatistics** übergeben. Die Funktion gibt die statistischen Werte in einer [**PDH \_ STATISTICS-Struktur**](/windows/desktop/api/Pdh/ns-pdh-pdh_statistics) zurück.

Sie können diese Funktion auch verwenden, um eine Protokolldatei zu komprimieren. Lesen Sie beispielsweise zehn Datensätze aus einer Protokolldatei, rufen [**Sie PdhComputeCounterStatistics**](/windows/desktop/api/Pdh/nf-pdh-pdhcomputecounterstatistics) auf, um den Mittelwert zu berechnen, und schreiben Sie den Mittelwert dann in eine Ausgabeprotokolldatei.

 

 
