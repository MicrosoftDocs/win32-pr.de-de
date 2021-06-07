---
description: Der Arbeitssatz eines Prozesses ist der Satz von Seiten im virtuellen Adressraum des Prozesses, die sich derzeit im physischen Speicher befinden.
ms.assetid: ff05276a-1d40-4844-b649-10e32e3f1937
title: Arbeitssatz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4985e7eb526d5dda8469ccc2f46bfe6fd050c745
ms.sourcegitcommit: b01ad017c152c6756f3638623fe335877644d414
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/06/2021
ms.locfileid: "111549892"
---
# <a name="working-set"></a>Arbeitssatz

Der Arbeitssatz eines Prozesses ist der Satz von Seiten im virtuellen Adressraum des Prozesses, die sich derzeit im physischen Speicher befinden. Der Arbeitssatz enthält nur auslagerungsfähige Speicherbelegungen. Nicht auslagerungsfähige Speicherbelegungen wie [Adressfenstererweiterungen](address-windowing-extensions.md) (Address Windowing Extensions, AWE) oder [große Seitenbelegungen](large-page-support.md) sind nicht im Arbeitssatz enthalten.

Wenn ein Prozess auf auslagerungsfähigen Speicher verweist, der sich derzeit nicht im Arbeitssatz befindet, tritt ein *Seitenfehler* auf. Der Fehlerhandler der Systemseite versucht, den Seitenfehler zu beheben, und wenn er erfolgreich ist, wird die Seite dem Arbeitssatz hinzugefügt. (Der Zugriff auf AWE oder große Seitenzuordnungen verursacht nie einen Seitenfehler, da diese Zuordnungen nicht auslagerungsfähig sind.)

Ein *Hartseitenfehler* muss behoben werden, indem Seiteninhalte aus dem *Sicherungsspeicher* der Seite gelesen werden. Dabei handelt es sich entweder um die Auslagerungsdatei des Systems oder um eine vom Prozess erstellte Speicherzuordnungsdatei. Ein *Softpagefehler* kann behoben werden, ohne auf den Sicherungsspeicher zuzugreifen. Ein Softpagefehler tritt auf, wenn:

-   Die Seite befindet sich im Arbeitssatz eines anderen Prozesses, sodass sie sich bereits im Arbeitsspeicher befindet.
-   Die Seite befindet sich im Übergang, da sie entweder aus den Arbeitssätzen aller Prozesse entfernt wurde, die die Seite verwendet haben und noch nicht wiederverwendet wurden, oder weil sie aufgrund eines Vorabrufvorgangs des Speicher-Managers bereits vorhanden ist.
-   Ein Prozess verweist zum ersten Mal auf eine zugeordnete virtuelle Seite (manchmal auch als *Fehler ohne Anforderung* bezeichnet).

Seiten können aufgrund der folgenden Aktionen aus einem Prozessarbeitssatz entfernt werden:

-   Der Prozess reduziert oder leert das Arbeitssatz durch Aufrufen der [**SetProcessWorkingSetSize-,**](/windows/win32/api/memoryapi/nf-memoryapi-setprocessworkingsetsize) [**SetProcessWorkingSetSizeEx-**](/windows/win32/api/memoryapi/nf-memoryapi-setprocessworkingsetsizeex) oder [**EmptyWorkingSet-Funktion.**](/windows/win32/api/psapi/nf-psapi-emptyworkingset)
-   Der Prozess ruft die [**VirtualUnlock-Funktion**](/windows/win32/api/memoryapi/nf-memoryapi-virtualunlock) für einen Speicherbereich auf, der nicht gesperrt ist.
-   Der Prozess entpackt eine zugeordnete Ansicht einer Datei mithilfe der [**UnmapViewOfFile-Funktion.**](/windows/win32/api/memoryapi/nf-memoryapi-unmapviewoffile)
-   Der Speicher-Manager entfernt Seiten aus dem Arbeitssatz, um mehr verfügbaren Arbeitsspeicher zu erstellen.
-   Der Arbeitsspeicher-Manager muss eine Seite aus dem Arbeitssatz entfernen, um Platz für eine neue Seite zu schaffen (z. B. weil der Arbeitssatz die maximale Größe hat).

Wenn mehrere Prozesse eine Seite gemeinsam nutzen, wirkt sich das Entfernen der Seite aus dem Arbeitssatz eines Prozesses nicht auf andere Prozesse aus. Nachdem eine Seite aus den Arbeitssätzen aller Prozesse entfernt wurde, die sie verwendet haben, wird die Seite zu einer *Übergangsseite.* Übergangsseiten bleiben im RAM zwischengespeichert, bis von einem Prozess erneut auf die Seite verwiesen wird oder sie wiederverwendet werden (z. B. mit Nullen gefüllt und einem anderen Prozess übergeben). Wenn eine Übergangsseite geändert wurde, seit sie zuletzt auf den Datenträger geschrieben wurde (d. h. wenn die Seite "modifiziert" ist), muss die Seite in ihren Sicherungsspeicher geschrieben werden, bevor sie erneut verwendet werden kann. Das System kann beginnen, fehlerhafte Übergangsseiten in ihren Sicherungsspeicher zu schreiben, sobald diese Seiten verfügbar sind.

Jeder Prozess verfügt über eine minimale und maximale Arbeitssatzgröße, die sich auf das Auslagerungsverhalten des virtuellen Arbeitsspeichers des Prozesses auswirken. Verwenden Sie die [**GetProcessMemoryInfo-Funktion,**](/windows/win32/api/psapi/nf-psapi-getprocessmemoryinfo) um die aktuelle Größe des Arbeitssatzes eines angegebenen Prozesses abzurufen. Verwenden Sie die Funktionen [**GetProcessWorkingSetSizeEx**](/windows/win32/api/memoryapi/nf-memoryapi-getprocessworkingsetsizeex) und [**SetProcessWorkingSetSizeEx,**](/windows/win32/api/memoryapi/nf-memoryapi-setprocessworkingsetsizeex) um die minimalen und maximalen Arbeitssatzgrößen abzurufen oder zu ändern.

Die Prozessstatus-Anwendungsprogrammierschnittstelle (PSAPI) stellt eine Reihe von Funktionen bereit, die detaillierte Informationen zum Arbeitssatz eines Prozesses zurückgeben. Weitere Informationen finden Sie unter [Arbeitssatzinformationen.](../psapi/working-set-information.md)

 

 
