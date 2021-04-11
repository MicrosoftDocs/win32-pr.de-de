---
description: Rufen Sie die pdhopenquery-Funktion auf, um eine neue Abfrage zu erstellen, die Leistungsdaten aus einer echt Zeit Quelle oder einer Protokolldatei sammelt. Die-Funktion gibt ein Handle für die Abfrage zurück, die Sie in nachfolgenden PDH-Funktionsaufrufen verwenden.
ms.assetid: 6fd4716e-b163-47a3-b0cb-5f9599f8681f
title: Erstellen einer Abfrage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a9d50ec52966529a3476a6d375606ba3d0b538b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131681"
---
# <a name="creating-a-query"></a>Erstellen einer Abfrage

Rufen Sie die [**pdhopenquery**](/windows/desktop/api/Pdh/nf-pdh-pdhopenquerya) -Funktion auf, um eine neue Abfrage zu erstellen, die Leistungsdaten aus einer echt Zeit Quelle oder einer Protokolldatei sammelt. Die-Funktion gibt ein Handle für die Abfrage zurück, die Sie in nachfolgenden PDH-Funktionsaufrufen verwenden.

Nachdem Sie die Abfrage erstellt haben, nennen Sie die [**pdhaddcounter**](/windows/desktop/api/Pdh/nf-pdh-pdhaddcountera) -Funktion für jeden Zählers, den Sie der Abfrage hinzufügen möchten. Sie können eine der folgenden Methoden verwenden, um den voll qualifizierten Counter-Pfad bereitzustellen.

-   Definieren Sie den Counter-Pfad als statische Zeichenfolge. Verwenden Sie diese Methode, wenn Sie den gleichen Wert immer überwachen und wenn Sie mit der korrekten Syntax eines Counter-Pfads vertraut sind. Informationen zur korrekten Syntax, die zum Angeben eines Zählers verwendet wird, finden Sie unter [Angeben eines Counter-Pfads](specifying-a-counter-path.md).
-   Initialisieren Sie eine [**PDH-Objekt \_ \_ Pfad \_ Element**](/windows/desktop/api/Pdh/ns-pdh-pdh_counter_path_elements_a) -Struktur mit den Namen des Computers, des Objekts, des Zählers und der Instanz. Übergeben Sie diese Struktur an [**pdhmakecounterpath**](/windows/desktop/api/Pdh/nf-pdh-pdhmakecounterpatha) , wodurch ein Indikator Pfad für die angegebenen Elemente zurückgegeben wird.
-   Geben Sie einen Counter-Pfad an, der Platzhalter Zeichen enthält, und nennen Sie [**PdhExpandWildCardPath**](/windows/desktop/api/Pdh/nf-pdh-pdhexpandwildcardpatha) , um eine Liste der Namen von Zählern abzurufen, die den Platzhalter Zeichen im Pfad entsprechen. Durchsuchen Sie die Liste der Zähler Namen, und fügen Sie der Abfrage die gewünschten Indikatoren aus der Liste hinzu.
-   Rufen Sie die [**pdhbrowscounters**](/windows/desktop/api/Pdh/nf-pdh-pdhbrowsecountersa) -Funktion auf, um ein Dialogfeld anzuzeigen, mit dem der Benutzer Leistungsindikatoren durchsuchen und auswählen kann. Weitere Informationen finden Sie unter durch [Suchen](browsing-counters.md)von Leistungsindikatoren.

Beachten Sie, dass " [**pdhaddcounter**](/windows/desktop/api/Pdh/nf-pdh-pdhaddcountera) " keine Fehlerbedingung meldet, wenn eine Instanz angegeben ist, die nicht vorhanden ist. Stattdessen wird ein Fehler erfolgreich zurückgegeben \_ . Der Grund für dieses Verhalten ist, dass Sie nicht bekannt ist, wenn eine nicht vorhandene Instanz des Zählers angegeben wurde oder eine vorhanden ist, die zwar vorhanden ist, aber noch nicht erstellt wurde.

Die fehlende Indikator Instanz wird entweder von [**pdhcollectquerydata**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydata), [**pdhgetrawcountervalue**](/windows/desktop/api/Pdh/nf-pdh-pdhgetrawcountervalue)oder [**pdhgetformattedcountervalue**](/windows/desktop/api/Pdh/nf-pdh-pdhgetformattedcountervalue)gemeldet. Wenn Sie **pdhcollectquerydata** nur für eine Objektinstanz aufrufen und die Objektinstanz immer noch nicht vorhanden ist, wird davon ausgegangen, dass die Instanz des Zählers nicht vorhanden ist, und die Funktion gibt PDH \_ keine \_ Daten zurück. Wenn jedoch mehr als ein-Counter abgefragt wird, gibt **pdhcollectquerydata** möglicherweise trotzdem einen Fehler Erfolg zurück, \_ auch wenn eine der-Objektinstanzen noch nicht vorhanden ist. Rufen Sie in diesem Fall " **pdhgetrawcountervalue** " oder " **pdhgetformattedcountervalue** " für jede der relevanten Leistungsindikator Instanzen auf. Wenn die Instanz beim Aufrufen von **pdhgetrawcountervalue** nicht vorhanden ist, gibt die Funktion den Fehler \_ Erfolg zurück und legt den **cstatus** -Member des [**PDH- \_ \_ rohindikators**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter) auf PDH- \_ Status \_ keine \_ Instanz fest. Wenn die Instanz beim Aufrufen von **pdhgetformattedcountervalue** nicht vorhanden ist, gibt die Funktion \_ ungültige PDH \_ -Daten zurück und legt den **cstatus** -Member des [**PDH- \_ fmt- \_ CounterValue**](/windows/desktop/api/Pdh/ns-pdh-pdh_fmt_countervalue) auf PDH \_ cstatus \_ No \_ instance fest.

Beachten Sie, dass der in der [**pdhaddcounter**](/windows/desktop/api/Pdh/nf-pdh-pdhaddcountera) -Funktion angegebene Counter-Pfad lokalisiert werden muss. Die [**pdhaddenglishcounter**](/windows/desktop/api/Pdh/nf-pdh-pdhaddenglishcountera) -Funktion stellt eine Gebiets Schema neutrale Methode zum Hinzufügen von Leistungsindikatoren zur Abfrage bereit. Diese Funktion ist die empfohlene Methode zum Hinzufügen von Gebiets Schema neutralen Leistungsindikatoren zu einer Abfrage.

Um einen Counter aus einer Abfrage zu entfernen, nennen Sie die [**PdhRemoveCounter**](/windows/desktop/api/Pdh/nf-pdh-pdhremovecounter) -Funktion.

Nachdem Sie die Datensammlung für eine Abfrage abgeschlossen haben, können Sie die [**pdhclosequery**](/windows/desktop/api/Pdh/nf-pdh-pdhclosequery) -Funktion zum Schließen der Abfrage und zum Freigeben aller zugeordneten Systemressourcen abrufen. **Pdhclosequery** schließt alle gegen Handles, die der Abfrage zugeordnet sind.

 

 



