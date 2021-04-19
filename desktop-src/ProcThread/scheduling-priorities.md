---
description: Die Ausführung von Threads wird basierend auf Ihrer Planungs Priorität geplant.
ms.assetid: 8710cd56-6bf3-4317-a1f6-1a159394ce2a
title: Planen von Prioritäten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e80c8baf4ed066ec7034c97850248f81c298c65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356156"
---
# <a name="scheduling-priorities"></a>Planen von Prioritäten

Die Ausführung von Threads wird basierend auf Ihrer *Planungs Priorität* geplant. Jedem Thread wird eine Planungs Priorität zugewiesen. Die Prioritätsstufen liegen zwischen NULL (niedrigste Priorität) und 31 (höchste Priorität). Nur der Zero-page-Thread kann eine Priorität von 0 (null) haben. (Der Zero-page-Thread ist ein System Thread, der für das Nullen von freien Seiten zuständig ist, wenn keine anderen Threads ausgeführt werden müssen.)

Das System behandelt alle Threads mit der gleichen Priorität als gleich. Das System weist Zeit Scheiben in einer Roundrobin-Methode allen Threads mit der höchsten Priorität zu. Wenn keiner dieser Threads zur Laufzeit bereit ist, weist das Systemzeit Scheiben in einer Roundrobin-Methode allen Threads mit der nächsthöheren Priorität zu. Wenn ein Thread mit höherer Priorität für die Ausführung verfügbar ist, beendet das System die Ausführung des Threads mit niedrigerer Priorität (ohne die Beendigung seines Zeitabschnitts zuzulassen) und weist dem Thread mit höherer Priorität einen vollen Zeit Slice zu. Weitere Informationen finden Sie unter [Kontext](context-switches.md)Wechsel.

Die Priorität der einzelnen Threads wird durch die folgenden Kriterien bestimmt:

-   Die Prioritäts Klasse des Prozesses.
-   Die Prioritäts Ebene des Threads innerhalb der Prioritäts Klasse des Prozesses.

Die Prioritäts Klasse und die Prioritätsstufe werden kombiniert, um die *Basis Priorität* eines Threads zu bilden. Informationen zur dynamischen Priorität eines Threads finden Sie unter [Prioritäts Steigerungen](priority-boosts.md).

## <a name="priority-class"></a>Prioritäts Klasse

Jeder Prozess gehört zu einer der folgenden Prioritäts Klassen:<dl> inaktive \_ Prioritäts \_ Klasse  
unterhalb der \_ normalen \_ Prioritäts \_ Klasse  
Klasse der normalen \_ Priorität \_  
oberhalb der \_ normalen \_ Prioritäts \_ Klasse  
Klasse mit hoher \_ Priorität \_  
Realtime \_ priority- \_ Klasse  
</dl>

Standardmäßig ist die Prioritäts Klasse eines Prozesses normale \_ Prioritäts \_ Klasse. Verwenden Sie die Funktion "up- [**Process**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) ", um die Prioritäts Klasse eines untergeordneten Prozesses anzugeben, wenn Sie Sie erstellen. Wenn der aufrufende Prozess die \_ Prioritäts Klasse im Leerlauf \_ oder unter der \_ normalen \_ Prioritäts \_ Klasse ist, erbt der neue Prozess diese Klasse. Verwenden Sie die [**getpriorityclass**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getpriorityclass) -Funktion, um die aktuelle Prioritäts Klasse eines Prozesses zu bestimmen, und die [**setpriorityclass**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setpriorityclass) -Funktion, um die Prioritäts Klasse eines Prozesses zu ändern.

Prozesse, die das System überwachen, z. b. Bildschirmschoner oder Anwendungen, die in regelmäßigen Abständen eine Anzeige aktualisieren, sollten die Klasse mit der \_ Priorität " \_ Dadurch wird verhindert, dass die Threads dieses Prozesses, die keine hohe Priorität haben, von Threads mit höherer Priorität gestört werden.

Verwenden Sie \_ die \_ Klasse mit hoher Priorität mit Bedacht. Wenn ein Thread für erweiterte Zeiträume mit der höchsten Prioritätsstufe ausgeführt wird, erhalten andere Threads im System keine Prozessorzeit. Wenn mehrere Threads gleichzeitig mit hoher Priorität festgelegt werden, verlieren die Threads ihre Wirksamkeit. Die Klasse mit hoher Priorität sollte für Threads reserviert werden, die auf zeitkritische Ereignisse reagieren müssen. Wenn Ihre Anwendung eine Aufgabe ausführt, die die Klasse mit hoher Priorität erfordert, während die restlichen Aufgaben eine normale Priorität haben, verwenden Sie [**setpriorityclass**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setpriorityclass) , um die Prioritäts Klasse der Anwendung vorübergehend zu erhöhen. verringern Sie Sie anschließend, nachdem die zeitkritische Aufgabe abgeschlossen wurde. Eine andere Strategie besteht darin, einen Prozess mit hoher Priorität zu erstellen, bei dem alle Threads in den meisten Fällen blockiert werden, sodass Threads nur dann wiedererweckt werden, wenn wichtige Aufgaben benötigt werden. Der wichtigste Punkt ist, dass ein Thread mit hoher Priorität für einen kurzen Zeitraum ausgeführt werden sollte und nur wenn er zeitkritische Aufgaben ausführen muss.

Sie sollten fast nie die Echtzeit- \_ Prioritäts \_ Klasse verwenden, da dadurch Systemthreads unterbrochen werden, die Maus Eingaben, Tastatureingaben und das Leeren von Hintergrund Datenträger verwalten. Diese Klasse eignet sich für Anwendungen, die direkt mit der Hardware kommunizieren oder kurze Aufgaben ausführen, die begrenzte Unterbrechungen aufweisen sollten.

## <a name="priority-level"></a>Prioritätsstufe

Die folgenden Prioritätsstufen sind in jeder Prioritäts Klasse aufgeführt:<dl> Thread \_ Priorität im \_ Leerlauf  
Thread \_ Priorität \_ niedrigste  
Thread \_ Priorität \_ unterhalb von \_ Normal  
Thread \_ Priorität \_ Normal  
Thread \_ Priorität \_ oberhalb des \_ normalen  
Thread \_ Priorität \_ höchste  
Thread \_ Prioritäts \_ Zeit \_ kritisch  
</dl>

Alle Threads werden mithilfe der Thread \_ Priorität \_ Normal erstellt. Dies bedeutet, dass die Thread Priorität mit der Prozess Prioritäts Klasse identisch ist. Nachdem Sie einen Thread erstellt haben, verwenden Sie die [**SetThreadPriority**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadpriority) -Funktion, um die Priorität relativ zu anderen Threads im Prozess anzupassen.

Eine typische Strategie besteht darin, die Thread \_ Priorität \_ oberhalb \_ der normalen oder Thread \_ Priorität \_ für den Eingabe Thread des Prozesses zu verwenden, um sicherzustellen, dass die Anwendung auf den Benutzer reagiert. Hintergrundthreads, insbesondere prozessorintensive, können auf die Thread \_ Priorität \_ unterhalb \_ der normalen oder Thread Priorität niedrigste festgelegt werden \_ \_ , um sicherzustellen, dass Sie bei Bedarf vorzeitig entfernt werden können. Wenn Sie jedoch einen Thread haben, der darauf wartet, dass ein anderer Thread mit niedrigerer Priorität einen Task abschließt, müssen Sie die Ausführung des wartenden Threads mit hoher Priorität blockieren. Verwenden Sie hierzu eine Wait- [Funktion](../sync/wait-functions.md), einen [kritischen Abschnitt](../sync/critical-section-objects.md) [**oder die Funktion**](/windows/win32/api/synchapi/nf-synchapi-sleep) "Standby", " [**sleepex**](/windows/win32/api/synchapi/nf-synchapi-sleepex)" oder " [**SwitchTo Thread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-switchtothread) ". Dies ist vorzuziehen, wenn der Thread eine Schleife ausführt. Andernfalls kann der Prozess blockiert werden, da der Thread mit niedrigerer Priorität nie geplant wird.

Verwenden Sie die [**getthreadpriority**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadpriority) -Funktion, um die aktuelle Prioritätsstufe eines Threads zu bestimmen.

## <a name="base-priority"></a>Basispriorität

Die Prozess Prioritäts Klasse und die Thread Prioritätsstufe werden kombiniert, um die Basis Priorität der einzelnen Threads zu bilden.

In der folgenden Tabelle wird die Basis Priorität für Kombinationen aus der Prozess Prioritäts Klasse und dem Thread Prioritätswert angezeigt.


<table>
<tr>
<th colspan="2">Prozess Prioritäts Klasse</th>
<th>Thread Prioritätsstufe</th>
<th>Basis Priorität</th>
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

 

 

 
