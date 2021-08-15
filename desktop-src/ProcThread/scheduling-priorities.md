---
description: Die Ausführung von Threads wird basierend auf ihrer Planungspriorität geplant.
ms.assetid: 8710cd56-6bf3-4317-a1f6-1a159394ce2a
title: Zeitplanungsprioritäten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 359f86e6ef78ffe1e549045eebbe435674b50f25f25bd30598fce8581c06092a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117793312"
---
# <a name="scheduling-priorities"></a>Zeitplanungsprioritäten

Die Ausführung von Threads wird basierend auf ihrer *Planungspriorität geplant.* Jedem Thread wird eine Planungspriorität zugewiesen. Die Prioritätsstufen reichen von 0 (niedrigste Priorität) bis 31 (höchste Priorität). Nur der Nullseitenthread kann eine Priorität von 0 (null) haben. (Der Nullseitenthread ist ein Systemthread, der für das Nullen von freien Seiten verantwortlich ist, wenn keine anderen Threads ausgeführt werden müssen.)

Das System behandelt alle Threads mit der gleichen Priorität als gleich. Das System weist allen Threads mit der höchsten Priorität Zeitslices in Roundrobin-Weise zu. Wenn keiner dieser Threads ausgeführt werden kann, weist das System allen Threads mit der nächsten höchsten Priorität Roundrobin-Zeitslices zu. Wenn ein Thread mit höherer Priorität für die Ausführung verfügbar wird, beendet das System die Ausführung des Threads mit niedrigerer Priorität (ohne dass er die Verwendung seines Zeitslices beenden kann) und weist dem Thread mit höherer Priorität einen Zeitslice zu. Weitere Informationen finden Sie unter [Kontextwechsel.](context-switches.md)

Die Priorität der einzelnen Threads wird durch die folgenden Kriterien bestimmt:

-   Die Prioritätsklasse des Prozesses
-   Die Prioritätsebene des Threads innerhalb der Prioritätsklasse des Prozesses.

Die Prioritätsklasse und die Prioritätsebene werden kombiniert, um die *Basispriorität eines* Threads zu bilden. Informationen zur dynamischen Priorität eines Threads finden Sie unter [Priority Boosts](priority-boosts.md).

## <a name="priority-class"></a>Priority-Klasse

Jeder Prozess gehört zu einer der folgenden Prioritätsklassen:<dl> IDLE \_ \_ PRIORITY-KLASSE  
UNTERHALB \_ DER \_ NORMAL \_ PRIORITY-KLASSE  
NORMAL \_ \_ PRIORITY-KLASSE  
ÜBER \_ DER NORMAL \_ \_ PRIORITY-KLASSE  
HIGH \_ \_ PRIORITY-KLASSE  
REALTIME \_ \_ PRIORITY-KLASSE  
</dl>

Standardmäßig ist die Prioritätsklasse eines Prozesses NORMAL \_ PRIORITY \_ CLASS. Verwenden Sie [**die CreateProcess-Funktion,**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) um die Prioritätsklasse eines untergeordneten Prozesses anzugeben, wenn Sie ihn erstellen. Wenn der aufrufende Prozess IDLE \_ PRIORITY CLASS oder BELOW NORMAL PRIORITY CLASS \_ \_ \_ \_ ist, erbt der neue Prozess diese Klasse. Verwenden Sie [**die GetPriorityClass-Funktion,**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getpriorityclass) um die aktuelle Prioritätsklasse eines Prozesses zu bestimmen, und die [**SetPriorityClass-Funktion,**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setpriorityclass) um die Prioritätsklasse eines Prozesses zu ändern.

Prozesse, die das System überwachen, z. B. Bildschirmschoner oder Anwendungen, die eine Anzeige regelmäßig aktualisieren, sollten IDLE \_ PRIORITY \_ CLASS verwenden. Dadurch wird verhindert, dass threads dieses Prozesses, die keine hohe Priorität haben, Threads mit höherer Priorität stören.

Verwenden Sie HIGH \_ PRIORITY \_ CLASS mit Vorsicht. Wenn ein Thread für längere Zeiträume mit der höchsten Prioritätsebene ausgeführt wird, erhalten andere Threads im System keine Prozessorzeit. Wenn mehrere Threads gleichzeitig mit hoher Priorität festgelegt werden, verlieren die Threads ihre Effektivität. Die Klasse mit hoher Priorität sollte für Threads reserviert sein, die auf zeitkritische Ereignisse reagieren müssen. Wenn Ihre Anwendung eine Aufgabe ausführt, für die die Klasse mit hoher Priorität erforderlich ist, während die restlichen Aufgaben die normale Priorität haben, verwenden Sie [**SetPriorityClass,**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setpriorityclass) um die Prioritätsklasse der Anwendung vorübergehend zu erhöhen. Reduzieren Sie sie dann, nachdem die zeitkritische Aufgabe abgeschlossen wurde. Eine andere Strategie besteht in der Erstellung eines Prozesses mit hoher Priorität, bei dem alle Threads die meiste Zeit blockiert werden, und Threads nur dann zu erzeugen, wenn kritische Aufgaben benötigt werden. Der wichtigste Punkt ist, dass ein Thread mit hoher Priorität für einen kurzen Zeitraum ausgeführt werden sollte, und nur dann, wenn zeitkritische Aufgaben ausgeführt werden müssen.

Sie sollten fast nie REALTIME PRIORITY CLASS verwenden, da dies Systemthreads unterbricht, die Mauseingaben, Tastatureingaben und Hintergrunddatenträger \_ \_ leeren. Diese Klasse kann für Anwendungen geeignet sein, die direkt mit der Hardware "sprechen" oder kurze Aufgaben ausführen, die eingeschränkte Unterbrechungen haben sollten.

## <a name="priority-level"></a>Prioritätsebene

Im Folgenden finden Sie Prioritätsebenen innerhalb jeder Prioritätsklasse:<dl> \_THREADPRIORITÄT IM \_ LEERLAUF  
\_THREADPRIORITÄT \_ NIEDRIGSTE  
\_THREADPRIORITÄT \_ UNTER \_ NORMAL  
\_THREADPRIORITÄT \_ NORMAL  
\_THREADPRIORITÄT \_ ÜBER \_ NORMAL  
\_THREADPRIORITÄT \_ AM HÖCHSTEN  
\_ \_ THREADPRIORITÄTSZEIT \_ KRITISCH  
</dl>

Alle Threads werden mit THREAD \_ PRIORITY \_ NORMAL erstellt. Dies bedeutet, dass die Threadpriorität mit der Prozessprioritätsklasse identisch ist. Nachdem Sie einen Thread erstellt haben, verwenden Sie die [**SetThreadPriority-Funktion,**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadpriority) um die Priorität relativ zu anderen Threads im Prozess anzupassen.

Eine typische Strategie ist die Verwendung von THREAD PRIORITY ABOVE NORMAL oder THREAD PRIORITY HIGHEST für den Eingabethread des Prozesses, um sicherzustellen, dass die Anwendung \_ \_ auf den Benutzer \_ \_ \_ reagiert. Hintergrundthreads, insbesondere solche, die prozessorintensiv sind, können auf THREADPRIORITÄT UNTER NORMAL oder THREADPRIORITÄT NIEDRIGSTE festgelegt werden, um sicherzustellen, dass sie bei Bedarf \_ \_ \_ vorverlegt werden \_ \_ können. Wenn Sie jedoch einen Thread haben, der auf einen anderen Thread mit einer niedrigeren Priorität wartet, um eine Aufgabe auszuführen, stellen Sie sicher, dass Sie die Ausführung des wartenden Threads mit hoher Priorität blockieren. Verwenden Sie hierzu eine [Wartefunktion,](../sync/wait-functions.md) [einen](../sync/critical-section-objects.md)kritischen Abschnitt oder die [**Sleep-Funktion,**](/windows/win32/api/synchapi/nf-synchapi-sleep) [**SleepEx**](/windows/win32/api/synchapi/nf-synchapi-sleepex)oder [**SwitchToThread-Funktion.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-switchtothread) Dies ist dem Ausführen einer Schleife durch den Thread vorzuziehen. Andernfalls kann der Prozess zu einem Deadlock werden, da der Thread mit niedrigerer Priorität nie geplant wird.

Verwenden Sie die [**GetThreadPriority-Funktion,**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadpriority) um die aktuelle Prioritätsebene eines Threads zu bestimmen.

## <a name="base-priority"></a>Basispriorität

Die Prozessprioritätsklasse und threadprioritätsebene werden kombiniert, um die Basispriorität jedes Threads zu bilden.

Die folgende Tabelle zeigt die Basispriorität für Kombinationen von Prozessprioritätsklasse und Threadprioritätswert.


<table>
<tr>
<th colspan="2">Prozessprioritätsklasse</th>
<th>Threadprioritätsebene</th>
<th>Basispriorität</th>
</tr>
<tr>
<td rowspan="7" colspan="2">IDLE_PRIORITY_CLASS </td>
<td>THREAD_PRIORITY_IDLE</td>
<td>1</td>
</tr>
<tr>
<td>THREAD_PRIORITY_LOWEST</td>
<td>2</td>
</tr>
<tr>
<td>THREAD_PRIORITY_BELOW_NORMAL</td>
<td>3</td>
</tr>
<tr>
<td>THREAD_PRIORITY_NORMAL</td>
<td>4</td>
</tr>
<tr>
<td>THREAD_PRIORITY_ABOVE_NORMAL</td>
<td>5</td>
</tr>
<tr>
<td>THREAD_PRIORITY_HIGHEST</td>
<td>6</td>
</tr>
<tr>
<td>THREAD_PRIORITY_TIME_CRITICAL</td>
<td>15</td>
</tr>
<tr>
<td rowspan="7" colspan="2">BELOW_NORMAL_PRIORITY_CLASS </td>
<td>THREAD_PRIORITY_IDLE</td>
<td>1</td>
</tr>
<tr>
<td>THREAD_PRIORITY_LOWEST</td>
<td>4</td>
</tr>
<tr>
<td>THREAD_PRIORITY_BELOW_NORMAL</td>
<td>5</td>
</tr>
<tr>
<td>THREAD_PRIORITY_NORMAL</td>
<td>6</td>
</tr>
<tr>
<td>THREAD_PRIORITY_ABOVE_NORMAL</td>
<td>7</td>
</tr>
<tr>
<td>THREAD_PRIORITY_HIGHEST</td>
<td>8</td>
</tr>
<tr>
<td>THREAD_PRIORITY_TIME_CRITICAL</td>
<td>15</td>
</tr>
<tr>
<td rowspan="7" colspan="2">NORMAL_PRIORITY_CLASS </td>
<td>THREAD_PRIORITY_IDLE</td>
<td>1</td>
</tr>
<tr>
<td>THREAD_PRIORITY_LOWEST</td>
<td>6</td>
</tr>
<tr>
<td>THREAD_PRIORITY_BELOW_NORMAL</td>
<td>7</td>
</tr>
<tr>
<td>THREAD_PRIORITY_NORMAL</td>
<td>8</td>
</tr>
<tr>
<td>THREAD_PRIORITY_ABOVE_NORMAL</td>
<td>9</td>
</tr>
<tr>
<td>THREAD_PRIORITY_HIGHEST</td>
<td>10</td>
</tr>
<tr>
<td>THREAD_PRIORITY_TIME_CRITICAL</td>
<td>15</td>
</tr>
<tr>
<td rowspan="7" colspan="2">ABOVE_NORMAL_PRIORITY_CLASS </td>
<td>THREAD_PRIORITY_IDLE</td>
<td>1</td>
</tr>
<tr>
<td>THREAD_PRIORITY_LOWEST</td>
<td>8</td>
</tr>
<tr>
<td>THREAD_PRIORITY_BELOW_NORMAL</td>
<td>9</td>
</tr>
<tr>
<td>THREAD_PRIORITY_NORMAL</td>
<td>10</td>
</tr>
<tr>
<td>THREAD_PRIORITY_ABOVE_NORMAL</td>
<td>11</td>
</tr>
<tr>
<td>THREAD_PRIORITY_HIGHEST</td>
<td>12</td>
</tr>
<tr>
<td>THREAD_PRIORITY_TIME_CRITICAL</td>
<td>15</td>
</tr>
<tr>
<td rowspan="7" colspan="2">HIGH_PRIORITY_CLASS </td>
<td>THREAD_PRIORITY_IDLE</td>
<td>1</td>
</tr>
<tr>
<td>THREAD_PRIORITY_LOWEST</td>
<td>11</td>
</tr>
<tr>
<td>THREAD_PRIORITY_BELOW_NORMAL</td>
<td>12</td>
</tr>
<tr>
<td>THREAD_PRIORITY_NORMAL</td>
<td>13</td>
</tr>
<tr>
<td>THREAD_PRIORITY_ABOVE_NORMAL</td>
<td>14</td>
</tr>
<tr>
<td>THREAD_PRIORITY_HIGHEST</td>
<td>15</td>
</tr>
<tr>
<td>THREAD_PRIORITY_TIME_CRITICAL</td>
<td>15</td>
</tr>
<tr>
<td rowspan="7" colspan="2">REALTIME_PRIORITY_CLASS </td>
<td>THREAD_PRIORITY_IDLE</td>
<td>16</td>
</tr>
<tr>
<td>THREAD_PRIORITY_LOWEST</td>
<td>22</td>
</tr>
<tr>
<td>THREAD_PRIORITY_BELOW_NORMAL</td>
<td>23</td>
</tr>
<tr>
<td>THREAD_PRIORITY_NORMAL</td>
<td>24</td>
</tr>
<tr>
<td>THREAD_PRIORITY_ABOVE_NORMAL</td>
<td>25</td>
</tr>
<tr>
<td>THREAD_PRIORITY_HIGHEST</td>
<td>26</td>
</tr>
<tr>
<td>THREAD_PRIORITY_TIME_CRITICAL</td>
<td>31</td>
</tr>
</table>

 

 

 
