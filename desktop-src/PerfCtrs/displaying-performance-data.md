---
description: Die meisten Leistungsindikatoren erfordern zwei Beispiel Werte, um einen anzeigbaren Wert zu berechnen.
ms.assetid: 75e45baf-51c5-400c-a31f-92bdab4ee492
title: Anzeigen von Leistungsdaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22d913474b794585dd557fae2b1fc232336b637d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106358898"
---
# <a name="displaying-performance-data"></a>Anzeigen von Leistungsdaten

Die meisten Leistungsindikatoren erfordern zwei Beispiel Werte, um einen anzeigbaren Wert zu berechnen. Die Formel für jeden gegen Wert bestimmt, ob der-Wert zwei Beispiele erfordert. Eine Liste der Indikatoren und deren Formeln finden Sie im Abschnitt "Indikator Typen" im [Windows Server 2003 Deployment Kit](/previous-versions/windows/it-pro/windows-server-2003/cc776490(v=ws.10)).

[Sammeln von Leistungsdaten](collecting-performance-data.md) zeigt, wie Beispiel Daten abgerufen werden. Sobald Sie über die Beispiele verfügen, rufen Sie in der Regel [**pdhgetformattedcountervalue**](/windows/desktop/api/Pdh/nf-pdh-pdhgetformattedcountervalue) auf, um einen anzeigbaren Wert zu berechnen.

Wenn Sie den Wert des Indikators nach oben oder unten skalieren müssen, um den Wert anzuzeigen, rufen Sie die [**pdhsetcounterscalefactor**](/windows/desktop/api/Pdh/nf-pdh-pdhsetcounterscalefactor) -Funktion vor dem Aufruf von " [**pdhgetformattedcountervalue**](/windows/desktop/api/Pdh/nf-pdh-pdhgetformattedcountervalue)" auf. Leistungswerte können mit einer Leistungsstärke von 10 von einem Faktor von-7 bis 7 skaliert werden.

Wenn der Indikator Pfad ein Platzhalter Zeichen für den Instanznamen enthält, rufen Sie [**pdhgetformattedcounterarray**](/windows/desktop/api/Pdh/nf-pdh-pdhgetformattedcounterarraya) auf, um ein Array von formatierten Indikator Werten für jede erfasste Instanz abzurufen.

Sie können auch die Funktionen [**pdhcalculatecounterfromrawvalue**](/windows/desktop/api/Pdh/nf-pdh-pdhcalculatecounterfromrawvalue) und [**pdhformatfromrawvalue**](/windows/desktop/api/Pdh/nf-pdh-pdhformatfromrawvalue) verwenden, um einen anzeigbaren Wert zu berechnen. Um diese Funktionen zu verwenden, müssen Sie das gesammelte Beispiel nach jedem [**pdhcollectquerydata**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydata) -Befehl Abrufen und das Beispiel selbst speichern. Um das Beispiel abzurufen, rufen Sie die [**pdhgetrawcountervalue**](/windows/desktop/api/Pdh/nf-pdh-pdhgetrawcountervalue) -oder [**pdhgetrawcounterarray**](/windows/desktop/api/Pdh/nf-pdh-pdhgetrawcounterarraya) -Funktion auf. Rufen Sie für zeitbasierte Indikatorwerte [**pdhgetcountertimebase**](/windows/desktop/api/Pdh/nf-pdh-pdhgetcountertimebase) vor **pdhformatfromrawvalue** auf, um die Zeitbasis des Indikators abzurufen.

Wenn Sie Berechnungen mithilfe der Rohdaten durchführen, überprüfen Sie vor der Verwendung des Beispiels immer das **cstatus** -Element der [**PDH- \_ rohleistungs- \_ Counter**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter) -Struktur. Das Beispiel ist ungültig, wenn der Wert von **cstatus** nicht PDH \_ cstatus \_ neue \_ Daten oder PDH \_ cstatus \_ gültige Daten ist \_ .

## <a name="displaying-statistics-for-a-counter"></a>Anzeigen von Statistiken für einen Counter

Wenn Sie die Mindest-, höchst-und Mittelwerte eines Indikators berechnen möchten, können Sie die [**pdhcomputecounterstatistics**](/windows/desktop/api/Pdh/nf-pdh-pdhcomputecounterstatistics) -Funktion abrufen. Wenn Sie Beispiele sammeln, speichern Sie die [**PDH- \_ rohindikator \_**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter) Strukturen in einem Array, das Sie an **pdhcomputecounterstatistics** übergeben. Die-Funktion gibt die statistischen Werte in einer [**PDH- \_ Statistik**](/windows/desktop/api/Pdh/ns-pdh-pdh_statistics) Struktur zurück.

Sie können diese Funktion auch verwenden, um eine Protokolldatei zu komprimieren. Lesen Sie z. b. zehn Datensätze aus einer Protokolldatei, und nennen Sie [**pdhcomputecounterstatistics**](/windows/desktop/api/Pdh/nf-pdh-pdhcomputecounterstatistics) , um den Mittelwert zu berechnen und dann den Mittelwert in eine Ausgabeprotokoll Datei zu schreiben.

 

 
