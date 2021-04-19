---
description: Mit den CPU-Sätzen werden APIs bereitgestellt, um die Anwendungs Affinität auf Weiche Weise zu deklarieren, die mit der Betriebssystem-Energie Verwaltung kompatibel
ms.assetid: FF8BE790-19D9-473F-B184-C54FB392D61A
title: CPU-Sätze
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 801474591751f04a5bffe570d6b8caff4974203f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353455"
---
# <a name="cpu-sets"></a>CPU-Sätze

Mit den CPU-Sätzen werden APIs bereitgestellt, um die Anwendungs Affinität auf Weiche Weise zu deklarieren, die mit der Betriebssystem-Energie Verwaltung kompatibel Außerdem bietet die API Anwendungen die Möglichkeit, alle Hintergrundthreads im Prozess mit einer Teilmenge von Prozessoren zu verbinden, indem der **ProzessStandard** Mechanismus verwendet wird, um Störungen von Betriebssystemthreads innerhalb des Prozesses zu vermeiden. Einige Versionen von Windows unterstützen grundlegende reservierungsrichtlinien, bei denen eine Teilmenge der CPU-Sets des Systems für die exklusive Verwendung einzelner Anwendungen und Arbeits Auslastungen verwendet werden kann.

Die CPU-Satz-API kann mit CPU-Satz-IDs verwendet werden, die mit virtuellen Prozessor Affinitäten verknüpft sind. Bei den meisten Systemen und unter den meisten Bedingungen wird jede CPU-Satz-ID direkt einem logischen Prozessor mit einem einzelnen **Home** zugeordnet. Ein Thread, der einem bestimmten CPU-Satz zugeordnet ist, wird in der Regel auf einem der Prozessoren in der Liste der ausgewählten CPU-Satz-IDs ausgeführt.

Reservierte CPU-Sätze können ermittelt werden, indem das **zugewiesene** Flag in den System- \_ CPU- \_ Satz Informationen überprüft wird \_ . Das System steuert den Zugriff auf reservierte CPU-Sätze, und die Zuweisung kann mit dem Flag " **Zuweisungs** Zuweisung" der System-CPU- \_ \_ Satz Informationsstruktur abgefragt werden \_ . Wenn ein Prozess versucht, eine CPU-Satz Zuweisung zu verwenden, die ausschließlich anderen Prozessen zugewiesen ist, wird die Anforderung ignoriert, und Threads, die unzulässigen CPU-Sätzen zugewiesen sind, werden an anderer Stelle geplant. CPU-Sätze können auf zwei Ebenen zugewiesen werden. Die Standard-CPU-Sätze des Prozesses werden allen Threads in einem Prozess zugewiesen, die keine Zuweisung auf der ausgewählten Thread Ebene aufweisen. Wenn für einen Thread oder Prozess eine restriktive Affinitäts Maske festgelegt ist, wird die Affinitäts Maske oberhalb der in Konflikt stehenden CPU-Satz Zuweisung berücksichtigt. Bei Systemen mit mehreren Gruppen werden CPU-Zuweisungen ignoriert, wenn Sie sich in Gruppen befinden, die nicht der Gruppe in der Affinitäts Maske des Threads entsprechen. Wenn ein Thread mehreren gültigen CPU-Sätzen zugewiesen ist, wird er auf einem der entsprechenden Prozessoren entsprechend seiner Prioritäten und der Prioritäten der konkurrierenden Threads auf diesen Prozessoren ausgeführt.

**CPU-Satz Funktionen/Enumerationen/Strukturen**

-   [**Getprocessdefaultcpusets**](getprocessdefaultcpusets.md) -Funktion
-   [**Getsystemcpusetinformation**](getsystemcpusetinformation.md) -Funktion
-   [**Getthreadselectedcpusets**](getthreadselectedcpusets.md) -Funktion
-   [**Setprocessdefaultcpusets**](setprocessdefaultcpusets.md) -Funktion
-   [**Setthreadselectedcpusets**](setthreadselectedcpusets.md) -Funktion
-   [**CPU \_ Enumeration des \_ Informations \_ Typs festlegen**](cpu-set-information-type.md)
-   [**System \_ Struktur der CPU- \_ Satz \_ Informationen**](/windows/desktop/api/winnt/ns-winnt-system_cpu_set_information)

 

 



