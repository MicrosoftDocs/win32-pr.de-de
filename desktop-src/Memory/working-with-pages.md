---
description: Verwenden Sie die GetSystemInfo-Funktion, um die Größe einer Seite auf dem aktuellen Computer zu ermitteln.
ms.assetid: 953ddfc4-6126-41fb-81a3-0ce1f0fb223f
title: Arbeiten mit Seiten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66c12c99ada03dca1e17c72c2a5f0d5360b6a98d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527263"
---
# <a name="working-with-pages"></a>Arbeiten mit Seiten

Verwenden Sie die [**GetSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) -Funktion, um die Größe einer Seite auf dem aktuellen Computer zu ermitteln.

Die Funktionen [**VirtualQuery**](/windows/win32/api/memoryapi/nf-memoryapi-virtualquery) und [**virtualqueryex**](/windows/win32/api/memoryapi/nf-memoryapi-virtualqueryex) geben Informationen zu einem Bereich von aufeinander folgenden Seiten zurück, beginnend bei einer angegebenen Adresse im Adressraum eines Prozesses. **VirtualQuery** gibt Informationen zum Arbeitsspeicher im aufrufenden Prozess zurück. **Virtualqueryex** gibt Informationen zum Arbeitsspeicher in einem angegebenen Prozess zurück und wird verwendet, um Debugger zu unterstützen, die Informationen zu einem debuggten Prozess benötigen. Der Bereich der Seiten wird durch die angegebene Adresse gebunden, die auf die nächste Seitenbegrenzung gerundet wird. Es erweitert alle nachfolgenden Seiten mit den folgenden Attributen gemeinsam:

-   Der Status aller Seiten ist identisch: entweder zugesichert, reserviert oder kostenlos.
-   Wenn die anfängliche Seite nicht frei ist, sind alle Seiten in der Region Teil derselben anfänglichen Zuordnung von Seiten, die durch einen [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc)-Aufrufe reserviert wurden.
-   Der Zugriffsschutz für alle Seiten ist identisch (d. h. **Seiten \_** schreibgeschützt, **Seiten- \_ /Schreibzugriff** oder **Seiten- \_ NoAccess**).

Die [**virtubelegungsfunktion**](/windows/win32/api/memoryapi/nf-memoryapi-virtuallock) ermöglicht einem Prozess, eine oder mehrere Seiten des zugeteilten Speichers in den physischen Speicher (RAM) zu sperren, sodass das System nicht mehr in die Auslagerungs Datei wechseln kann. Sie kann verwendet werden, um sicherzustellen, dass auf wichtige Daten ohne Datenträger Zugriff zugegriffen werden kann. Das Sperren von Seiten im Arbeitsspeicher ist gefährlich, da dadurch die Fähigkeit des Systems, Arbeitsspeicher zu verwalten, eingeschränkt wird Eine übermäßige Verwendung von **virtuzuweisung** kann die Systemleistung beeinträchtigen, indem der ausführbare Code in die Auslagerungs Datei ausgelagert wird. Die [**virtualunlock**](/windows/win32/api/memoryapi/nf-memoryapi-virtualunlock) -Funktion entsperrt den von **virtuzuweisung** gesperrten Arbeitsspeicher.

Die [**VirtualProtect**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotect) -Funktion ermöglicht es einem Prozess, den Zugriffsschutz für jede zugesicherte Seite im Adressraum eines Prozesses zu ändern. So kann ein Prozess z. b. Lese-/Schreibseiten zuordnen, um sensible Daten zu speichern. Anschließend kann er den Zugriff auf "schreibgeschützt" oder "kein Zugriff" zum Schutz vor versehentlichem überschreiben ändern. **VirtualProtect** wird in der Regel mit Seiten verwendet, die von [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc)zugeordnet werden, aber es funktioniert auch mit Seiten, die durch eine der anderen Zuordnungs Funktionen committet wurden. **VirtualProtect** ändert jedoch den Schutz ganzer Seiten, und Zeiger, die von den anderen Funktionen zurückgegeben werden, werden nicht notwendigerweise an Seiten Grenzen ausgerichtet. Die [**virtualprotectex**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotectex) -Funktion ähnelt **VirtualProtect**, mit dem Unterschied, dass der Arbeitsspeicher in einem angegebenen Prozess geändert wird. Das Ändern des Schutzes ist hilfreich, um zu Debuggern beim Zugriff auf den Arbeitsspeicher eines gedebuggten Prozesses zu wechseln.

 

 
