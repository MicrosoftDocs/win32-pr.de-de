---
description: Der Arbeitssatz eines Programms ist eine Auflistung der Seiten im virtuellen Adressraum, auf die kürzlich verwiesen wurde.
ms.assetid: 6017ef59-d2e9-4245-a406-8965024dbb35
title: Prozessarbeitssatz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a345df46f4d36e8400112c54492d7844c7a46b5d5ae125a3d9103db9cbcc18c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117793508"
---
# <a name="process-working-set"></a>Prozessarbeitssatz

Der *Arbeitssatz eines* Programms ist eine Auflistung der Seiten im virtuellen Adressraum, auf die kürzlich verwiesen wurde. Sie umfasst sowohl freigegebene als auch private Daten. Die freigegebenen Daten enthalten Seiten, die alle Anweisungen enthalten, die Ihre Anwendung ausgeführt, einschließlich der in Ihren DLLs und den System-DLLs. Wenn die Arbeitssatzgröße zunimmt, steigt der Arbeitsspeicherbedarf.

Ein Prozess verfügt über eine zugeordnete minimale Arbeitssatzgröße und maximale Arbeitssatzgröße. Jedes Mal, wenn [**Sie CreateProcess aufrufen,**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa)wird die minimale Arbeitssatzgröße für den Prozess reserviert. Der Virtuelle Arbeitsspeicher-Manager versucht, genügend Arbeitsspeicher für den minimalen Arbeitssatz zu behalten, der sich befindet, wenn der Prozess aktiv ist, behält jedoch nicht mehr als die maximale Größe bei.

Rufen Sie die [**GetProcessWorkingSetSize-Funktion**](/windows/desktop/api/memoryapi/nf-memoryapi-getprocessworkingsetsize) auf, um die angeforderten Mindest- und Höchstgrößen des Arbeitssets für Ihre Anwendung zu erhalten.

Das System legt die Standardarbeitssatzgrößen fest. Sie können die Arbeitssatzgrößen auch mithilfe der [**SetProcessWorkingSetSize-Funktion**](/windows/desktop/api/memoryapi/nf-memoryapi-setprocessworkingsetsize) ändern. Das Festlegen dieser Werte ist keine Garantie dafür, dass der Arbeitsspeicher reserviert oder resident ist. Seien Sie vorsichtig, wenn Sie eine zu große minimale oder maximale Arbeitssatzgröße anfordern, da dies die Systemleistung beeinträchtigen kann.

Verwenden Sie die [**GetProcessMemoryInfo-Funktion,**](/windows/win32/api/psapi/nf-psapi-getprocessmemoryinfo) um die aktuelle oder Spitzengröße des Arbeitssets für Ihren Prozess zu erhalten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Arbeitsspeicherleistungsinformationen](/previous-versions/windows/desktop/legacy/aa965225(v=vs.85))
</dt> <dt>

[Arbeitssatz](../memory/working-set.md)
</dt> </dl>

 

 
