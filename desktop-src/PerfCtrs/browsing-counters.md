---
description: Um ein Dialogfeld anzuzeigen, in dem die auf dem Computer definierten Leistungsobjekte und Leistungsindikatoren aufgeführt sind, rufen Sie die PdhBrowseCounters-Funktion auf.
ms.assetid: f2fac1d3-f643-43c9-a445-112015baecdd
title: Durchsuchen von Leistungsindikatoren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c63278e0a531ec882bad6e102c89f6db0e0946a0d2a0a14b8736e7ee3aef6a8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011408"
---
# <a name="browsing-counters"></a>Durchsuchen von Leistungsindikatoren

Um ein Dialogfeld anzuzeigen, in dem die auf dem Computer definierten Leistungsobjekte und Leistungsindikatoren aufgeführt sind, rufen Sie die [**PdhBrowseCounters-Funktion**](/windows/desktop/api/Pdh/nf-pdh-pdhbrowsecountersa) auf. Im Dialogfeld kann der Benutzer Leistungsindikatoren durchsuchen und auswählen. Sie verwenden die [**PDH \_ BROWSE \_ DLG \_ CONFIG-Struktur,**](/windows/win32/api/pdh/ns-pdh-pdh_browse_dlg_config_a) um die Konfiguration des Dialogfelds anzugeben. Beispielsweise können Sie das Dialogfeld so konfigurieren, dass eine Auswahl oder mehrfache Auswahl zurück angezeigt wird.

Bei der Eingabe enthält **das szReturnPathBuffer-Element** das Standardleistungsobjekt und den Leistungsindikator, die im Dialogfeld ausgewählt sind. Bei der Ausgabe enthält der Puffer das Leistungsobjekt und den Leistungsindikator, die der Benutzer ausgewählt hat. Sie können auch den **pCallBack-Member** verwenden, um eine Rückruffunktion anzugeben, um die vom Dialogfeld zurückgegebenen Indikatornamen zu verarbeiten.

Beachten Sie, dass dieses Dialogfeld PDH DIALOG CANCELLED zurückgeben kann, wenn \_ \_ **bSingleCounterPerDialog** **FALSE** ist und der Benutzer auf die Schaltfläche Schließen klickt, sodass die Fehlerbehandlung dies berücksichtigen muss.

Ein Beispiel, in dem die [**PdhBrowseCounters-Funktion verwendet**](/windows/desktop/api/Pdh/nf-pdh-pdhbrowsecountersa) wird, finden Sie unter [Durchsuchen von Leistungsindikatoren.](browsing-performance-counters.md)

Um eine Liste von Leistungsobjekten auf dem Computer abzurufen, können Sie auch die [**PdhEnumObjects-Funktion**](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectsa) aufrufen. Um eine Liste von Leistungsindikatoren und Instanzen für ein Leistungsobjekt abzurufen, rufen Sie die [**PdhEnumObjectItems-Funktion**](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectitemsa) auf. Sie können diese Funktionen auch verwenden, um die Leistungsobjekte und Leistungsindikatoren zu identifizieren, die in einer Protokolldatei enthalten sind. Wiederholte Aufrufe von **PdhEnumObjectItems** geben dieselbe Liste von Leistungsindikatoren und Instanzen zurück, bis **Sie PdhEnumObjects** aufrufen, um zuerst die Liste der Leistungsobjekte zu aktualisieren. Ein Beispiel, das Objekte und Leistungsindikatoren aufzählt, finden Sie unter [Aufzählen von Prozessobjekten.](enumerating-process-objects.md)

## <a name="selecting-the-data-source"></a>Auswählen der Datenquelle

Sie können [**PdhSelectDataSource**](/windows/desktop/api/Pdh/nf-pdh-pdhselectdatasourcea) in Verbindung mit [**PdhBrowseCounters**](/windows/desktop/api/Pdh/nf-pdh-pdhbrowsecountersa) verwenden, um den Benutzer aufzufordern, auszuwählen, ob sich die Datenquelle in Echtzeit oder aus einer Protokolldatei befindet, und, wenn es sich um eine Protokolldatei handelt, ihren Namen auszuwählen. Wenn das Datenquellendialogfeld nicht angezeigt werden soll, können Sie **PdhSelectDataSource** aufrufen, um nur den Dateibrowserkatalog anzuzeigen. Geben Sie hierzu PDH FLAGS FILE BROWSER ONLY als zweiten Parameter des Aufrufs von \_ \_ \_ \_ **PdhSelectDataSource an.**

 

 



