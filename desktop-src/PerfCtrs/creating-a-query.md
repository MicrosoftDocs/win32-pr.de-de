---
description: Um eine neue Abfrage zu erstellen, die Leistungsdaten aus einer Echtzeitquelle oder Protokolldatei sammelt, rufen Sie die PdhOpenQuery-Funktion auf. Die Funktion gibt ein Handle für die Abfrage zurück, die Sie in nachfolgenden PDH-Funktionsaufrufen verwenden.
ms.assetid: 6fd4716e-b163-47a3-b0cb-5f9599f8681f
title: Erstellen einer Abfrage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1175c491ac1336458ed73d375d963f8a68b874bf3fecbb32000730a475d52714
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119775660"
---
# <a name="creating-a-query"></a>Erstellen einer Abfrage

Um eine neue Abfrage zu erstellen, die Leistungsdaten aus einer Echtzeitquelle oder Protokolldatei sammelt, rufen Sie die [**PdhOpenQuery-Funktion**](/windows/desktop/api/Pdh/nf-pdh-pdhopenquerya) auf. Die Funktion gibt ein Handle für die Abfrage zurück, die Sie in nachfolgenden PDH-Funktionsaufrufen verwenden.

Rufen Sie nach dem Erstellen der Abfrage die [**PdhAddCounter-Funktion**](/windows/desktop/api/Pdh/nf-pdh-pdhaddcountera) für jeden Leistungsindikator auf, den Sie der Abfrage hinzufügen möchten. Sie können eine der folgenden Methoden verwenden, um den vollqualifizierten Indikatorpfad bereitzustellen.

-   Definieren Sie den Indikatorpfad als statische Zeichenfolge. Verwenden Sie diese Methode, wenn Sie immer denselben Indikator überwachen und mit der richtigen Syntax eines Indikatorpfads vertraut sind. Informationen zur richtigen Syntax, die zum Angeben eines Leistungsindikators verwendet wird, finden Sie unter [Angeben eines Indikatorpfads.](specifying-a-counter-path.md)
-   Initialisieren Sie eine [**PDH \_ COUNTER PATH \_ \_ ELEMENTS-Struktur**](/windows/desktop/api/Pdh/ns-pdh-pdh_counter_path_elements_a) mit den Namen von Computer, Objekt, Indikator und Instanz. Übergeben Sie diese Struktur an [**PdhMakeCounterPath,**](/windows/desktop/api/Pdh/nf-pdh-pdhmakecounterpatha) wodurch ein Indikatorpfad für die angegebenen Elemente zurückgegeben wird.
-   Geben Sie einen Indikatorpfad an, der Platzhalterzeichen enthält, und rufen Sie [**PdhExpandWildCardPath**](/windows/desktop/api/Pdh/nf-pdh-pdhexpandwildcardpatha) auf, um eine Liste der Indikatornamen abzurufen, die mit den Platzhalterzeichen im Pfad übereinstimmen. Durchsuchen Sie die Liste der Indikatornamen, und fügen Sie der Abfrage die Leistungsindikatoren hinzu, die Sie aus dieser Liste wünschen.
-   Rufen Sie die [**PdhBrowseCounters-Funktion**](/windows/desktop/api/Pdh/nf-pdh-pdhbrowsecountersa) auf, um ein Dialogfeld anzuzeigen, in dem der Benutzer Leistungsindikatoren durchsuchen und auswählen kann. Weitere Informationen finden Sie unter [Durchsuchen von Leistungsindikatoren.](browsing-counters.md)

Beachten Sie, dass [**PdhAddCounter**](/windows/desktop/api/Pdh/nf-pdh-pdhaddcountera) keine Fehlerbedingung meldet, wenn eine Zählerinstanz angegeben wird, die nicht vorhanden ist. Stattdessen wird ERROR \_ SUCCESS zurückgegeben. Der Grund für dieses Verhalten ist, dass es nicht bekannt ist, ob eine nicht vorhandene Indikatorinstanz angegeben wurde oder eine vorhanden ist, aber noch nicht erstellt wurde.

Die fehlende Indikatorinstanz wird entweder von [**PdhCollectQueryData,**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydata) [**PdhGetRawCounterValue**](/windows/desktop/api/Pdh/nf-pdh-pdhgetrawcountervalue)oder [**PdhGetFormattedCounterValue**](/windows/desktop/api/Pdh/nf-pdh-pdhgetformattedcountervalue)gemeldet. Wenn **PdhCollectQueryData** nur für eine Indikatorinstanz aufgerufen wird und die Indikatorinstanz immer noch nicht vorhanden ist, wird davon ausgegangen, dass die Indikatorinstanz nicht vorhanden ist und die Funktion PDH \_ NO DATA zurückgibt. \_ Wenn jedoch mehrere Leistungsindikatoren abgefragt werden, gibt **PdhCollectQueryData** möglicherweise trotzdem ERROR \_ SUCCESS zurück, auch wenn eine der Indikatorinstanzen noch nicht vorhanden ist. Rufen Sie in diesem Fall **PdhGetRawCounterValue** oder **PdhGetFormattedCounterValue** für jede der Zählerinstanzen auf, die von Interesse sind. Wenn die Instanz beim Aufrufen von **PdhGetRawCounterValue** nicht vorhanden ist, gibt die Funktion ERROR SUCCESS zurück \_ und legt den **CStatus-Member** von [**PDH RAW \_ \_ COUNTER**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter) auf PDH \_ STATUS NO INSTANCE \_ \_ fest. Wenn die Instanz beim Aufrufen von **PdhGetFormattedCounterValue** nicht vorhanden ist, gibt die Funktion PDH INVALID DATA zurück \_ und legt den \_ **CStatus-Member** des [**PDH \_ FMT \_ COUNTERVALUE**](/windows/desktop/api/Pdh/ns-pdh-pdh_fmt_countervalue) auf PDH \_ CSTATUS NO INSTANCE \_ \_ fest.

Beachten Sie, dass der in der [**PdhAddCounter-Funktion**](/windows/desktop/api/Pdh/nf-pdh-pdhaddcountera) angegebene Indikatorpfad lokalisiert werden muss. Die [**PdhAddEnglishCounter-Funktion**](/windows/desktop/api/Pdh/nf-pdh-pdhaddenglishcountera) bietet eine gebietsschemaneutrale Möglichkeit, der Abfrage Leistungsindikatoren hinzuzufügen. Diese Funktion ist die empfohlene Methode zum Hinzufügen gebietsschemaneutraler Leistungsindikatoren zu einer Abfrage.

Um einen Indikator aus einer Abfrage zu entfernen, rufen Sie die [**PdhRemoveCounter-Funktion**](/windows/desktop/api/Pdh/nf-pdh-pdhremovecounter) auf.

Nachdem Sie das Sammeln von Daten für eine Abfrage abgeschlossen haben, rufen Sie die [**PdhCloseQuery-Funktion**](/windows/desktop/api/Pdh/nf-pdh-pdhclosequery) auf, um die Abfrage zu schließen und alle zugeordneten Systemressourcen freizugeben. **PdhCloseQuery** schließt alle Indikatorhandles, die der Abfrage zugeordnet sind.

 

 



