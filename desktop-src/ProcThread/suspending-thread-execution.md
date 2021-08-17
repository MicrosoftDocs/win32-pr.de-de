---
description: Ein Thread kann die Ausführung eines anderen Threads an- und fortsetzen. Während ein Thread angehalten wird, ist er nicht für die Zeit auf dem Prozessor geplant.
ms.assetid: b76d7af7-e3ec-4663-a9e7-832c01733c8c
title: Angehaltene Threadausführung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcf3ecf2bee1f14ae8571cb7e7402e32a636f4a35ca5c182d32a2a636ed85dff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117793157"
---
# <a name="suspending-thread-execution"></a>Angehaltene Threadausführung

Ein Thread kann die Ausführung eines anderen Threads an- und fortsetzen. Während ein Thread angehalten wird, ist er nicht für die Zeit auf dem Prozessor geplant.

Wenn ein Thread in einem angehaltenen Zustand (mit dem [**CREATE \_ SUSPENDED-Flag)**](process-creation-flags.md) erstellt wird, wird er erst ausgeführt, wenn ein anderer Thread die [**ResumeThread-Funktion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread) mit einem Handle für den angehaltenen Thread aufruft. Dies kann nützlich sein, um den Zustand des Threads zu initialisieren, bevor er ausgeführt wird. Das Aussetzen eines Threads bei der Erstellung kann für die einmalige Synchronisierung nützlich sein, da dadurch sichergestellt wird, dass der angehaltene Thread beim Aufrufen von ResumeThread den Startpunkt seines Codes **ausricht.**

Die [**SuspendThread-Funktion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-suspendthread) ist nicht für die Threadsynchronisierung vorgesehen, da sie nicht den Punkt im Code kontrolliert, an dem die Ausführung des Threads angehalten wird. Diese Funktion ist in erster Linie für die Verwendung durch Debugger konzipiert.

Ein Thread kann seine Ausführung für ein [](/windows/win32/api/synchapi/nf-synchapi-sleep) angegebenes Intervall vorübergehend durch Aufrufen der Sleep- oder [**SleepEx-Funktionen**](/windows/win32/api/synchapi/nf-synchapi-sleepex) liefern. Dies ist insbesondere in Fällen nützlich, in denen der Thread auf Benutzerinteraktionen reagiert, da er die Ausführung lange genug verzögern kann, damit Benutzer die Ergebnisse ihrer Aktionen beobachten können. Während des Ruhezustands ist der Thread nicht für die Zeit auf dem Prozessor geplant.

Die [**SwitchToThread-Funktion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-switchtothread) [](/windows/win32/api/synchapi/nf-synchapi-sleep) ähnelt sleep und [**sleepEx,**](/windows/win32/api/synchapi/nf-synchapi-sleepex)mit der Ausnahme, dass Sie das Intervall nicht angeben können. **SwitchToThread ermöglicht** es dem Thread, seinen Zeitslice zu vererbn.

 

 
