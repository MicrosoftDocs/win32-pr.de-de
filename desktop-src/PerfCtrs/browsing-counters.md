---
description: Um ein Dialogfeld anzuzeigen, in dem die auf dem Computer definierten Leistungs Objekte und-Indikatoren aufgelistet sind, können Sie die pdhbrowsecounters-Funktion aufrufen.
ms.assetid: f2fac1d3-f643-43c9-a445-112015baecdd
title: Leistungsindikatoren durchsuchen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd4bae5ce5ae7a21ae247cf66515f7386b8d0265
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357759"
---
# <a name="browsing-counters"></a>Leistungsindikatoren durchsuchen

Um ein Dialogfeld anzuzeigen, in dem die auf dem Computer definierten Leistungs Objekte und-Indikatoren aufgelistet sind, können Sie die [**pdhbrowsecounters**](/windows/desktop/api/Pdh/nf-pdh-pdhbrowsecountersa) -Funktion aufrufen. Das Dialogfeld ermöglicht dem Benutzer das Durchsuchen und Auswählen von Leistungsindikatoren. Sie verwenden die Struktur [**PDH- \_ Durchsuchen \_ DLG \_ config**](/windows/win32/api/pdh/ns-pdh-pdh_browse_dlg_config_a) , um die Konfiguration des Dialog Felds anzugeben. Beispielsweise können Sie das Dialogfeld so konfigurieren, dass eine Auswahl oder eine Mehrfachauswahl zurückgegeben wird.

Bei der Eingabe enthält das Element **szreturnpathbuffer** das Standard Leistungs Objekt und den Leistungswert, der im Dialogfeld ausgewählt ist. Bei der Ausgabe enthält der Puffer das Leistungs Objekt und den Leistungs Bewert, den der Benutzer ausgewählt hat. Sie können auch das **pCallback** -Member verwenden, um eine Rückruffunktion anzugeben, mit der die vom Dialogfeld zurückgegebenen Namen von Zählern verarbeitet werden.

Beachten Sie, dass dieses Dialogfeld das PDH-Dialogfeld zurückgeben kann \_ \_ , das abgebrochen wird, wenn **bsinglecounterperdialog** **false** ist und der Benutzer auf die Schaltfläche Schließen klickt, damit die Fehlerbehandlung dies berücksichtigen muss.

Ein Beispiel, in dem die [**pdhbrowscounters**](/windows/desktop/api/Pdh/nf-pdh-pdhbrowsecountersa) -Funktion verwendet wird, finden Sie unter durch [Suchen von Leistungsindikatoren](browsing-performance-counters.md).

Zum Abrufen einer Liste von Leistungs Objekten auf dem Computer können Sie auch die [**pdhenumubjects**](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectsa) -Funktion aufrufen. Rufen Sie zum Abrufen einer Liste von Leistungsindikatoren und Instanzen für ein Leistungs Objekt die [**pdhenumubjectitems**](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectitemsa) -Funktion auf. Sie können diese Funktionen auch verwenden, um die Leistungs Objekte und-Indikatoren zu identifizieren, die in einer Protokolldatei enthalten sind. Bei wiederholten Aufrufen von **pdhenumubjectitems** wird die gleiche Liste von Leistungsindikatoren und Instanzen zurückgegeben, bis Sie **pdhenumubjects** aufrufen, um die Liste der Leistungs Objekte zuerst zu aktualisieren. Ein Beispiel für das Auflisten von Objekten und Leistungsindikatoren finden Sie unter Auflisten von [Prozess Objekten](enumerating-process-objects.md).

## <a name="selecting-the-data-source"></a>Auswählen der Datenquelle

Mit [**pdhselectdatasource**](/windows/desktop/api/Pdh/nf-pdh-pdhselectdatasourcea) können Sie zusammen mit [**pdhbrowscounters**](/windows/desktop/api/Pdh/nf-pdh-pdhbrowsecountersa) den Benutzer auffordern, auszuwählen, ob sich die Datenquelle in Echtzeit oder aus einer Protokolldatei befindet, und ob es sich um eine Protokolldatei handelt. Wenn Sie nicht möchten, dass das Dialogfeld Datenquelle angezeigt wird, können Sie **pdhselectdatasource** aufrufen, um nur den Katalog des Datei Browsers anzuzeigen. Geben Sie hierzu \_ den Datei Browser PDH-Flags \_ \_ \_ nur als zweiten Parameter des Aufrufens von **pdhselectdatasource** an.

 

 



