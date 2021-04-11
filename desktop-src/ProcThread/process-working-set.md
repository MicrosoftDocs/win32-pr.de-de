---
description: Das Workingset eines Programms ist eine Sammlung von Seiten im virtuellen Adressraum, auf die vor kurzem verwiesen wurde.
ms.assetid: 6017ef59-d2e9-4245-a406-8965024dbb35
title: Arbeits Satz verarbeiten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 900b5d8a19c756a9087a9b2c006259857691dc11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104216011"
---
# <a name="process-working-set"></a>Arbeits Satz verarbeiten

Das *Workingset* eines Programms ist eine Sammlung von Seiten im virtuellen Adressraum, auf die vor kurzem verwiesen wurde. Sie enthält sowohl freigegebene als auch private Daten. Die freigegebenen Daten enthalten Seiten, die alle von der Anwendung ausgeführten Anweisungen enthalten, einschließlich der in ihren DLLs und der System-DLLs. Wenn die Workingsetgröße zunimmt, steigt der Arbeitsspeicher Bedarf.

Einem Prozess sind minimale Workingsetgröße und maximale Workingsetgröße zugeordnet. Jedes Mal, wenn Sie " [**forateprocess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa)" aufrufen, wird die minimale Workingsetgröße für den Prozess reserviert. Der virtuelle Speicher-Manager versucht, genügend Arbeitsspeicher für den minimalen Workingset beizubehalten, wenn der Prozess aktiv ist, behält jedoch die maximale Größe bei.

Um die angeforderten minimalen und maximalen Größen der Workingsets für die Anwendung zu erhalten, müssen Sie die [**GetProcessWorkingSetSize**](/windows/desktop/api/WinBase/nf-winbase-getprocessworkingsetsize) -Funktion aufrufen.

Das System legt die standardmäßigen workingsetgrößen fest. Sie können die workingsetgrößen auch mithilfe der [**SetProcessWorkingSetSize**](/windows/desktop/api/WinBase/nf-winbase-setprocessworkingsetsize) -Funktion ändern. Das Festlegen dieser Werte ist keine Garantie dafür, dass der Arbeitsspeicher reserviert oder Residenten ist. Achten Sie darauf, eine zu große minimale oder maximale Workingsetgröße anzufordern, da dadurch die Systemleistung beeinträchtigt werden kann.

Verwenden Sie die [**getprocessmemoryinfo**](/windows/win32/api/psapi/nf-psapi-getprocessmemoryinfo) -Funktion, um die aktuelle oder maximale Größe des Workingsets für den Prozess zu erhalten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zur Speicherleistung](/previous-versions/windows/desktop/legacy/aa965225(v=vs.85))
</dt> <dt>

[Arbeitssatz](../memory/working-set.md)
</dt> </dl>

 

 
