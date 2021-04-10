---
description: Ein Thread kann die Ausführung eines anderen Threads aussetzen und fortsetzen. Während ein Thread angehalten wird, ist er für den Prozessor nicht zeitlich geplant.
ms.assetid: b76d7af7-e3ec-4663-a9e7-832c01733c8c
title: Anhalten der Thread Ausführung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3688b0327ecf5fd21f07e9be6be6ecab17d64617
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959728"
---
# <a name="suspending-thread-execution"></a>Anhalten der Thread Ausführung

Ein Thread kann die Ausführung eines anderen Threads aussetzen und fortsetzen. Während ein Thread angehalten wird, ist er für den Prozessor nicht zeitlich geplant.

Wenn ein Thread in einem angehaltenen Zustand (mit dem [**Flag \_ "Create**](process-creation-flags.md) angehalten") erstellt wird, wird er erst ausgeführt, wenn ein anderer Thread die [**ResumeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread) -Funktion mit einem Handle für den angehaltenen Thread aufruft. Dies kann nützlich sein, um den Thread Zustand zu initialisieren, bevor er mit der Ausführung beginnt. Das Anhalten eines Threads bei der Erstellung kann für die einmalige Synchronisierung nützlich sein, da dadurch sichergestellt wird, dass der angehaltene Thread den Anfangspunkt seines Codes ausführt, wenn Sie **ResumeThread** aufzurufen.

Die [**SuspendThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-suspendthread) -Funktion ist nicht für die Thread Synchronisierung vorgesehen, da Sie den Punkt im Code nicht steuert, an dem die Ausführung des Threads angehalten wird. Diese Funktion ist hauptsächlich für die Verwendung durch-Debug konzipiert.

Ein Thread kann seine Ausführung für ein angegebenes Intervall vorübergehend durch Aufrufen der Funktionen [**Sleep**](/windows/win32/api/synchapi/nf-synchapi-sleep) oder [**sleepex**](/windows/win32/api/synchapi/nf-synchapi-sleepex) erzielen. Dies ist besonders in Fällen hilfreich, in denen der Thread auf Benutzerinteraktionen reagiert, da er die Ausführung lange genug verzögern kann, damit Benutzer die Ergebnisse ihrer Aktionen beobachten können. Während des standbyintervalls ist der Thread für den Prozessor nicht geplant.

Die [**switchdethread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-switchtothread) -Funktion ähnelt dem [**Sleep**](/windows/win32/api/synchapi/nf-synchapi-sleep) -und [**sleepex**](/windows/win32/api/synchapi/nf-synchapi-sleepex)-Wert, mit dem Unterschied, dass Sie das Intervall nicht angeben können. **Switchper Thread** ermöglicht dem Thread, seinen Zeit Slice zu übergeben.

 

 
