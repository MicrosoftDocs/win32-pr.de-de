---
description: Der Arbeits Satz eines Prozesses ist der Satz von Seiten im virtuellen Adressraum des Prozesses, der sich derzeit im physischen Speicher befindet.
ms.assetid: ff05276a-1d40-4844-b649-10e32e3f1937
title: Arbeitssatz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f54ed26e9809ebffd01edb30f48f36d398689e88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351748"
---
# <a name="working-set"></a>Arbeitssatz

Der Arbeits Satz eines Prozesses ist der Satz von Seiten im virtuellen Adressraum des Prozesses, der sich derzeit im physischen Speicher befindet. Das Workingset enthält nur Speicher belegbare Speicher Belegungen. nicht Auslagerungs Bare Speicher Belegungen, wie z.b. [Address windowingextensions](address-windowing-extensions.md) (AWE) oder [große Seiten](large-page-support.md) Zuordnungen, sind nicht im Workingset enthalten.

Wenn ein Prozess auf einen speicherbaren Speicher verweist, der sich derzeit nicht in seinem Workingset befindet, tritt ein *Seiten Fehler* auf. Der Fehlerhandler der System Seite versucht, den Seiten Fehler aufzulösen. wenn er erfolgreich ist, wird die Seite dem Arbeits Satz hinzugefügt. (Der Zugriff auf AWE oder große Seiten Zuordnungen verursacht niemals einen Seiten Fehler, da diese Zuordnungen nicht Auslagerungs fähig sind.)

Ein *Hard-Page-Fehler* muss behoben werden, indem der Seiten Inhalt aus dem *Sicherungs Speicher* der Seite gelesen wird. dabei handelt es sich entweder um die Auslagerungs Datei des Systems oder um eine vom Prozess erstellte Speicher Abbild Datei. Ein *weicher Seiten Fehler* kann aufgelöst werden, ohne auf den Sicherungs Speicher zuzugreifen. Ein weicher Seiten Fehler tritt auf, wenn Folgendes zutrifft:

-   Die Seite befindet sich im Workingset eines anderen Prozesses, sodass Sie sich bereits im Arbeitsspeicher befindet.
-   Die Seite befindet sich im Übergangsstadium, weil Sie entweder aus den Arbeits Sätzen aller Prozesse entfernt wurde, die die Seite verwendet haben und noch nicht neu festgelegt wurden, oder Sie ist bereits als Ergebnis eines Vorabruf Vorgangs für den Speicher-Manager vorhanden.
-   Ein Prozess verweist zum ersten Mal auf eine zugeordnete virtuelle Seite (manchmal auch als *Fehler nach "Anforderung-NULL*" bezeichnet).

Seiten können aufgrund der folgenden Aktionen aus einem Prozess Arbeitssatz entfernt werden:

-   Der Prozess reduziert oder leert die Workingsets durch Aufrufen der [**SetProcessWorkingSetSize**](/windows/win32/api/winbase/nf-winbase-setprocessworkingsetsize)-, [**setprocessworkingsetsizeex**](/windows/win32/api/memoryapi/nf-memoryapi-setprocessworkingsetsizeex) -oder [**EmptyWorkingSet**](/windows/win32/api/psapi/nf-psapi-emptyworkingset) -Funktion.
-   Der Prozess ruft die [**virtualunlock**](/windows/win32/api/memoryapi/nf-memoryapi-virtualunlock) -Funktion für einen Speicherbereich auf, der nicht gesperrt ist.
-   Der Prozess entordnet eine zugeordnete Ansicht einer Datei mithilfe der [**UnmapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-unmapviewoffile) -Funktion.
-   Der Speicher-Manager schneidet Seiten aus dem Workingset, um mehr verfügbaren Arbeitsspeicher zu erstellen.
-   Der Speicher-Manager muss eine Seite aus dem Workingset entfernen, um Platz für eine neue Seite zu schaffen (z. b. weil der Workingset seine maximale Größe hat).

Wenn mehrere Prozesse eine Seite gemeinsam verwenden, wirkt sich das Entfernen der Seite aus dem Workingset eines Prozesses nicht auf andere Prozesse aus. Nachdem eine Seite aus den Arbeits Sätzen aller Prozesse entfernt wurde, die Sie verwendet haben, wird die Seite zu einer *Übergangs Seite*. Übergangs Seiten bleiben im Arbeitsspeicher zwischengespeichert, bis auf die Seite entweder von einem Prozess oder einem neuen Zweck verwiesen wird (z. b. mit Nullen gefüllt und an einen anderen Prozess übergeben). Wenn eine Übergangs Seite geändert wurde, seit Sie zuletzt auf den Datenträger geschrieben wurde (d. h., wenn die Seite "Dirty" ist), muss die Seite in den Sicherungs Speicher geschrieben werden, bevor Sie neu geschrieben werden kann. Das System beginnt möglicherweise damit, geänderte Übergangs Seiten in den Sicherungs Speicher zu schreiben, sobald diese Seiten verfügbar werden.

Jeder Prozess verfügt über eine minimale und maximale Workingsetgröße, die sich auf das Paging-Verhalten des virtuellen Speichers des Prozesses auswirkt. Um die aktuelle Größe des Workingsets eines angegebenen Prozesses zu erhalten, verwenden Sie die [**getprocessmemoryinfo**](/windows/win32/api/psapi/nf-psapi-getprocessmemoryinfo) -Funktion. Um die minimalen und maximalen workingsetgrößen zu erhalten oder zu ändern, verwenden Sie die Funktionen [**getprocessworkingsetsizeex**](/windows/win32/api/memoryapi/nf-memoryapi-getprocessworkingsetsizeex) und [**setprocessworkingsetsizeex**](/windows/win32/api/memoryapi/nf-memoryapi-setprocessworkingsetsizeex) .

Die Prozessstatus-Anwendungsprogrammierschnittstelle (PSAPI) bietet eine Reihe von Funktionen, die ausführliche Informationen über den Arbeits Satz eines Prozesses zurückgeben. Weitere Informationen finden Sie unter [Arbeits Satz Informationen](../psapi/working-set-information.md).

 

 
