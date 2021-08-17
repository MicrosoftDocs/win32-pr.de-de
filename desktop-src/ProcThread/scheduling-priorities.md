---
description: Die Ausführung von Threads wird basierend auf ihrer Planungspriorität geplant.
ms.assetid: 8710cd56-6bf3-4317-a1f6-1a159394ce2a
title: Planungsprioritäten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 359f86e6ef78ffe1e549045eebbe435674b50f25f25bd30598fce8581c06092a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117793312"
---
# <a name="scheduling-priorities"></a>Planungsprioritäten

Die Ausführung von Threads wird basierend auf ihrer *Planungspriorität* geplant. Jedem Thread wird eine Planungspriorität zugewiesen. Die Prioritätsebenen reichen von 0 (niedrigste Priorität) bis 31 (höchste Priorität). Nur der Nullseitenthread kann die Priorität 0 (null) haben. (Der Nullseitenthread ist ein Systemthread, der dafür verantwortlich ist, alle freien Seiten auf null zu setzen, wenn keine anderen Threads ausgeführt werden müssen.)

Das System behandelt alle Threads mit der gleichen Priorität als gleich. Das System weist allen Threads mit der höchsten Priorität Zeitslices auf Roundrobin-Weise zu. Wenn keiner dieser Threads ausgeführt werden kann, weist das System allen Threads mit der nächstrangigen Priorität Roundrobin-Zeitslices zu. Wenn ein Thread mit höherer Priorität für die Ausführung verfügbar ist, beendet das System die Ausführung des Threads mit niedrigerer Priorität (ohne dass er die Verwendung seines Zeitslices beenden kann) und weist dem Thread mit höherer Priorität einen vollständigen Zeitslice zu. Weitere Informationen finden Sie unter [Kontextwechsel.](context-switches.md)

Die Priorität jedes Threads wird durch die folgenden Kriterien bestimmt:

-   Die Prioritätsklasse des Prozesses
-   Die Prioritätsebene des Threads innerhalb der Prioritätsklasse des Prozesses

Die Prioritätsklasse und die Prioritätsebene werden kombiniert, um die *Basispriorität* eines Threads zu bilden. Informationen zur dynamischen Priorität eines Threads finden Sie unter [Prioritätssteigerungen.](priority-boosts.md)

## <a name="priority-class"></a>Priority-Klasse

Jeder Prozess gehört zu einer der folgenden Prioritätsklassen:<dl> IDLE \_ \_ PRIORITY-KLASSE  
BELOW \_ NORMAL \_ PRIORITY \_ CLASS  
NORMAL \_ \_ PRIORITY-KLASSE  
OBERHALB \_ DER NORMALEN \_ \_ PRIORITÄTSKLASSE  
KLASSE MIT HOHER \_ PRIORITÄT \_  
REALTIME \_ PRIORITY \_ CLASS  
</dl>

Standardmäßig ist die Prioritätsklasse eines Prozesses NORMAL \_ PRIORITY \_ CLASS. Verwenden Sie die [**CreateProcess-Funktion,**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) um die Prioritätsklasse eines untergeordneten Prozesses anzugeben, wenn Sie ihn erstellen. Wenn der aufrufende Prozess IDLE \_ PRIORITY CLASS oder BELOW NORMAL PRIORITY CLASS \_ \_ \_ \_ ist, erbt der neue Prozess diese Klasse. Verwenden Sie die [**GetPriorityClass-Funktion,**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getpriorityclass) um die aktuelle Prioritätsklasse eines Prozesses zu bestimmen, und die [**SetPriorityClass-Funktion,**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setpriorityclass) um die Prioritätsklasse eines Prozesses zu ändern.

Prozesse, die das System überwachen, z. B. Bildschirmschoner oder Anwendungen, die regelmäßig eine Anzeige aktualisieren, sollten IDLE \_ PRIORITY \_ CLASS verwenden. Dadurch wird verhindert, dass die Threads dieses Prozesses, die keine hohe Priorität haben, Threads mit höherer Priorität beeinträchtigen.

Verwenden Sie HIGH \_ PRIORITY \_ CLASS mit Vorsicht. Wenn ein Thread über längere Zeiträume mit der höchsten Prioritätsstufe ausgeführt wird, erhalten andere Threads im System keine Prozessorzeit. Wenn mehrere Threads gleichzeitig mit hoher Priorität festgelegt werden, verlieren die Threads ihre Effektivität. Die Klasse mit hoher Priorität sollte für Threads reserviert werden, die auf zeitkritische Ereignisse reagieren müssen. Wenn Ihre Anwendung eine Aufgabe ausführt, die die Klasse mit hoher Priorität erfordert, während die restlichen Aufgaben eine normale Priorität haben, verwenden [**Sie SetPriorityClass,**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setpriorityclass) um die Prioritätsklasse der Anwendung vorübergehend zu erhöhen. reduzieren Sie sie dann, nachdem die zeitkritische Aufgabe abgeschlossen wurde. Eine weitere Strategie besteht darin, einen Prozess mit hoher Priorität zu erstellen, bei dem die meiste Zeit alle Threads blockiert sind, und Threads nur dann wieder ins Laufen zu bringen, wenn wichtige Aufgaben erforderlich sind. Der wichtige Punkt ist, dass ein Thread mit hoher Priorität für einen kurzen Zeitraum und nur dann ausgeführt werden soll, wenn zeitkritische Aufgaben ausgeführt werden müssen.

Sie sollten REALTIME PRIORITY CLASS fast nie \_ \_ verwenden, da dadurch Systemthreads unterbrochen werden, die Mauseingaben, Tastatureingaben und das Leeren von Hintergrunddatenträgern verwalten. Diese Klasse kann für Anwendungen geeignet sein, die direkt mit Hardware kommunizieren oder kurze Aufgaben ausführen, die begrenzte Unterbrechungen aufweisen sollten.

## <a name="priority-level"></a>Prioritätsstufe

Im Folgenden sind Die Prioritätsebenen innerhalb jeder Prioritätsklasse:<dl> \_ \_ THREADPRIORITÄT IM LEERLAUF  
\_ \_ THREADPRIORITÄT NIEDRIGSTE  
\_THREADPRIORITÄT \_ UNTER \_ NORMAL  
\_THREADPRIORITÄT \_ NORMAL  
\_ \_ THREADPRIORITÄT ÜBER \_ NORMAL  
\_HÖCHSTE \_ THREADPRIORITÄT  
\_ZEITKRITISCH FÜR THREADPRIORITÄT \_ \_  
</dl>

Alle Threads werden mit THREAD \_ PRIORITY \_ NORMAL erstellt. Dies bedeutet, dass die Threadpriorität mit der Prozessprioritätsklasse identisch ist. Nachdem Sie einen Thread erstellt haben, verwenden Sie die [**SetThreadPriority-Funktion,**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadpriority) um ihre Priorität relativ zu anderen Threads im Prozess anzupassen.

Eine typische Strategie ist die Verwendung von THREAD \_ PRIORITY ABOVE NORMAL oder THREAD PRIORITY HIGHEST für den \_ \_ \_ \_ Eingabethread des Prozesses, um sicherzustellen, dass die Anwendung auf den Benutzer reagiert. Hintergrundthreads, insbesondere solche, die prozessorintensiv sind, können auf THREAD PRIORITY BELOW NORMAL oder THREAD PRIORITY LOWEST festgelegt \_ \_ \_ \_ \_ werden, um sicherzustellen, dass sie bei Bedarf vorzeitig beendet werden können. Wenn Sie jedoch einen Thread haben, der auf einen anderen Thread mit einer niedrigeren Priorität wartet, um eine Aufgabe abzuschließen, stellen Sie sicher, dass Sie die Ausführung des wartenden Threads mit hoher Priorität blockieren. Verwenden Sie hierzu eine [Wait-Funktion,](../sync/wait-functions.md)einen [kritischen Abschnitt](../sync/critical-section-objects.md)oder die [**Sleep-Funktion,**](/windows/win32/api/synchapi/nf-synchapi-sleep) [**SleepEx**](/windows/win32/api/synchapi/nf-synchapi-sleepex)oder die [**SwitchToThread-Funktion.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-switchtothread) Dies ist dem Ausführen einer Schleife durch den Thread vorzuziehen. Andernfalls kann der Prozess zu einem Deadlock führen, da der Thread mit niedrigerer Priorität nie geplant ist.

Verwenden Sie die [**GetThreadPriority-Funktion,**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadpriority) um die aktuelle Prioritätsebene eines Threads zu bestimmen.

## <a name="base-priority"></a>Basispriorität

Die Prozessprioritätsklasse und die Threadprioritätsebene werden kombiniert, um die Basispriorität jedes Threads zu bilden.

Die folgende Tabelle zeigt die Basispriorität für Kombinationen aus Prozessprioritätsklasse und Threadprioritätswert.


<table>
<tr>
<th colspan="2">Prozessprioritätsklasse</th>
<th>Threadprioritätsstufe</th>
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

 

 

 
