---
description: CPU-Sätze bieten APIs zum Deklarieren der Anwendungsaffinität auf "weiche" Weise, die mit der Energieverwaltung des Betriebssystems kompatibel ist.
ms.assetid: FF8BE790-19D9-473F-B184-C54FB392D61A
title: CPU-Sätze
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 092559fbf5646a0938696c953f4136f1fe1a9567e56e02a04c6c36510d03d729
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143123"
---
# <a name="cpu-sets"></a>CPU-Sätze

CPU-Sätze bieten APIs zum Deklarieren der Anwendungsaffinität auf "weiche" Weise, die mit der Energieverwaltung des Betriebssystems kompatibel ist. Darüber hinaus bietet die API Anwendungen die Möglichkeit, alle Hintergrundthreads im Prozess mithilfe des **Prozessstandardmechanismus** einer Teilmenge von Prozessoren neu zu affinisieren, um Störungen durch Betriebssystemthreads innerhalb des Prozesses zu vermeiden. Einige Versionen von Windows unterstützen Kernreservierungsrichtlinien, in denen eine Teilmenge der CPU-Sätze des Systems der exklusiven Verwendung einzelner Anwendungen und Workloads zur Verfügung stehen kann.

Die CPU-Set-API funktioniert mit CPU-Satz-IDs, die virtuellen Prozessoraffinitäten zugeordnet sind. Auf den meisten Systemen und unter den meisten Bedingungen wird jede CPU-Satz-ID direkt einem einzelnen logischen **Basisprozessor** zugeordnet. Ein Thread, der einer bestimmten CPU-Gruppe affin ist, wird in der Regel auf einem der Prozessoren in der Liste der ausgewählten CPU-Satz-IDs ausgeführt.

Reservierte CPU-Sätze können durch Überprüfen des **Flags Zugeordnet** in den SYSTEM CPU SET INFORMATION ermittelt \_ \_ \_ werden. Das System steuert den Zugriff auf reservierte CPU-Sätze, und die Zuweisung kann mithilfe des **AllocatedToTargetProcess-Flags** der SYSTEM \_ CPU SET \_ \_ INFORMATION-Struktur abgefragt werden. Wenn ein Prozess versucht, eine CPU-Mengenzuweisung zu verwenden, die ausschließlich anderen Prozessen zugeordnet ist, wird seine Anforderung ignoriert, und Threads, die unzulässigen CPU-Sätzen zugewiesen sind, werden an anderer Stelle geplant. CPU-Sätze können auf zwei Ebenen zugewiesen werden. Die CPU-Standardsätze des Prozesses werden allen Threads in einem Prozess zugewiesen, die auf der Ebene Threadauswahl keine Zuweisung aufweisen. Wenn für einen Thread oder Prozess eine restriktive Affinitätsmaske festgelegt ist, wird die Affinitätsmaske über jeder in Konflikt liegenden CPU-Satzzuweisung berücksichtigt. Auf Systemen mit mehreren Gruppen werden CPU-Zuweisungen ignoriert, wenn sie sich in Gruppen befinden, die nicht mit der Gruppe in der Affinitätsmaske des Threads übereinstimmen. Wenn ein Thread mehreren gültigen CPU-Sätzen zugewiesen ist, wird er auf einem der entsprechenden Prozessoren gemäß seinen Prioritäten und den Prioritäten konkurrierender Threads auf diesen Prozessoren ausgeführt.

**CPU Set Functions/Enumerations/Structures**

-   [**GetProcessDefaultCpuSets-Funktion**](getprocessdefaultcpusets.md)
-   [**GetSystemCpuSetInformation-Funktion**](getsystemcpusetinformation.md)
-   [**GetThreadSelectedCpuSets-Funktion**](getthreadselectedcpusets.md)
-   [**SetProcessDefaultCpuSets-Funktion**](setprocessdefaultcpusets.md)
-   [**SetThreadSelectedCpuSets-Funktion**](setthreadselectedcpusets.md)
-   [**CPU \_ SET \_ INFORMATION \_ TYPE-Enumeration**](cpu-set-information-type.md)
-   [**SYSTEM \_ CPU \_ SET \_ INFORMATION-Struktur**](/windows/desktop/api/winnt/ns-winnt-system_cpu_set_information)

 

 



