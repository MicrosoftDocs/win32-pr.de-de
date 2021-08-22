---
description: Verwenden Sie die GetSystemInfo-Funktion, um die Größe einer Seite auf dem aktuellen Computer zu bestimmen.
ms.assetid: 953ddfc4-6126-41fb-81a3-0ce1f0fb223f
title: Arbeiten mit Pages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e47e8a352b13c12b38acca1a93f12886d83d24c4d43faa213a88cf5855b18c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067660"
---
# <a name="working-with-pages"></a>Arbeiten mit Pages

Verwenden Sie die [**GetSystemInfo-Funktion,**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) um die Größe einer Seite auf dem aktuellen Computer zu bestimmen.

Die Funktionen [**VirtualQuery**](/windows/win32/api/memoryapi/nf-memoryapi-virtualquery) und [**VirtualQueryEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualqueryex) geben Informationen zu einem Bereich aufeinanderfolgender Seiten zurück, die an einer angegebenen Adresse im Adressraum eines Prozesses beginnen. **VirtualQuery** gibt Informationen zum Arbeitsspeicher im aufrufenden Prozess zurück. **VirtualQueryEx** gibt Informationen zum Arbeitsspeicher in einem angegebenen Prozess zurück und wird verwendet, um Debugger zu unterstützen, die Informationen zu einem Prozess benötigen, der gedebuggt wird. Der Seitenbereich wird durch die angegebene Adresse begrenzt, die auf die nächste Seitengrenze gerundet wird. Sie wird durch alle nachfolgenden Seiten erweitert, wobei die folgenden Attribute gemeinsam sind:

-   Der Status aller Seiten ist identisch: commit, reserved oder free.
-   Wenn die anfängliche Seite nicht frei ist, sind alle Seiten in der Region Teil derselben anfänglichen Zuordnung von Seiten, die durch einen Aufruf von [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc)reserviert wurden.
-   Der Zugriffsschutz aller Seiten ist identisch (d.b. **PAGE \_ READONLY,** **PAGE \_ READWRITE** oder **PAGE \_ NOACCESS**).

Die [**VirtualLock-Funktion**](/windows/win32/api/memoryapi/nf-memoryapi-virtuallock) ermöglicht es einem Prozess, eine oder mehrere Seiten des arbeitsspeicherzusenden Arbeitsspeichers in den physischen Arbeitsspeicher (RAM) zu sperren, wodurch verhindert wird, dass das System die Seiten in die Auslagerungsdatei vertauscht. Sie kann verwendet werden, um sicherzustellen, dass auf wichtige Daten ohne Datenträgerzugriff zugegriffen werden kann. Das Sperren von Seiten im Arbeitsspeicher ist gefährlich, da dadurch die Fähigkeit des Systems zum Verwalten des Arbeitsspeichers eingeschränkt wird. Eine übermäßige Verwendung von **VirtualLock** kann die Systemleistung beeinträchtigen, da ausführbarer Code in die Auslagerungsdatei ausgetauscht wird. Die [**VirtualUnlock-Funktion**](/windows/win32/api/memoryapi/nf-memoryapi-virtualunlock) entsperrt den durch **VirtualLock** gesperrten Arbeitsspeicher.

Die [**VirtualProtect-Funktion**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotect) ermöglicht einem Prozess, den Zugriffsschutz einer beliebigen Seite, für die ein Commit ausgeführt wurde, im Adressraum eines Prozesses zu ändern. Beispielsweise kann ein Prozess Lese-/Schreibseiten zum Speichern vertraulicher Daten zuordnen und dann den Zugriff auf schreibgeschützten oder keinen Zugriff ändern, um vor versehentlichem Überschreiben zu schützen. **VirtualProtect** wird in der Regel mit Seiten verwendet, die von [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc)zugeordnet werden, funktioniert aber auch mit Seiten, für die von einer der anderen Zuordnungsfunktionen ein Commit ausgeführt wurde. **VirtualProtect** ändert jedoch den Schutz ganzer Seiten, und zeiger, die von den anderen Funktionen zurückgegeben werden, werden nicht notwendigerweise an Seitengrenzen ausgerichtet. Die [**VirtualProtectEx-Funktion**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotectex) ähnelt **VirtualProtect,** mit der Ausnahme, dass sie den Schutz des Arbeitsspeichers in einem angegebenen Prozess ändert. Das Ändern des Schutzes ist nützlich für Debugger beim Zugriff auf den Arbeitsspeicher eines Prozesses, der gedebuggt wird.

 

 
