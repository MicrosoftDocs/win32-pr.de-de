---
description: Es gibt viele Anwendungen, mit denen Threads erstellt werden, die sehr viel Zeit für den Ruhezustand aufwenden, der auf das Eintreten eines Ereignisses wartet.
ms.assetid: a5e52080-35d4-47f5-9050-90889e3bf2f8
title: Pooling von Threads
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcf3565401dc57b077e333043861d42b683e810c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865048"
---
# <a name="thread-pooling"></a>Pooling von Threads

Es gibt viele Anwendungen, mit denen Threads erstellt werden, die sehr viel Zeit für den Ruhezustand aufwenden, der auf das Eintreten eines Ereignisses wartet. Andere Threads können nur dann in den Ruhezustand versetzt werden, dass Sie regelmäßig zum Abrufen von Änderungs-oder Update Statusinformationen aktiviert werden. *Thread Pooling* ermöglicht es Ihnen, Threads effizienter zu verwenden, indem Sie der Anwendung einen Pool von Arbeitsthreads bereitstellen, die vom System verwaltet werden. Mindestens ein Thread überwacht den Status aller warte Vorgänge, die in die Warteschlange des Thread Pools eingereiht wurden. Wenn ein warte Vorgang abgeschlossen ist, führt ein Arbeits Thread aus dem Thread Pool die entsprechende Rückruffunktion aus.

In diesem Thema wird die ursprüngliche Thread Pool-API beschrieben. Die in Windows Vista eingeführte Thread Pool-API ist einfacher und zuverlässiger, bietet eine bessere Leistung und bietet Entwicklern mehr Flexibilität. Informationen zur aktuellen Thread Pool-API finden Sie unter [Thread Pools](thread-pools.md).

Sie können auch Arbeitselemente in die Warteschlange stellen, die nicht mit einem warte Vorgang im Thread Pool verknüpft sind. Um anzufordern, dass ein Arbeits Element von einem Thread im Thread Pool behandelt werden soll, müssen Sie die [**QueueUserWorkItem**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-queueuserworkitem) -Funktion aufzurufen. Diese Funktion nimmt einen Parameter für die Funktion an, die von dem aus dem Thread Pool ausgewählten Thread aufgerufen wird. Es gibt keine Möglichkeit, ein Arbeits Element abzubrechen, nachdem es in die Warteschlange eingereiht wurde.

[Timer-Queue-Timer](../sync/timer-queues.md) und [registrierte warte Vorgänge](../sync/wait-functions.md) verwenden ebenfalls den Thread Pool. Die Rückruf Funktionen werden in die Warteschlange des Thread Pools eingereiht. Sie können auch die [**bindiocompletioncallback**](/windows/desktop/api/WinBase/nf-winbase-bindiocompletioncallback) -Funktion verwenden, um asynchrone e/a-Vorgänge zu veröffentlichen. Nach Abschluss des e/a-Vorgängen wird der Rückruf von einem Thread Pool Thread ausgeführt.

Der Thread Pool wird beim ersten Aufruf von [**QueueUserWorkItem**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-queueuserworkitem) oder [**bindiocompletioncallback**](/windows/desktop/api/WinBase/nf-winbase-bindiocompletioncallback)erstellt, oder wenn eine Rückruffunktion von einem Timer oder einem registrierten Warteschlangen-Timer in eine Warteschlange eingereiht wird. Standardmäßig beträgt die Anzahl der Threads, die im Thread Pool erstellt werden können, ungefähr 500. Jeder Thread verwendet die Standard Stapelgröße und wird mit der Standardpriorität ausgeführt.

Der Thread Pool enthält zwei Arten von Arbeitsthreads: e/a-Vorgänge und nicht-e/a-Vorgänge. Ein e */a-Arbeits Thread* ist ein Thread, der in einem wartewarnbaren Wartestatus wartet. Arbeitselemente werden in e/a-Arbeitsthreads als asynchrone Prozedur Aufrufe (APC) in die Warteschlange eingereiht. Sie sollten eine Arbeitsaufgabe in die Warteschlange eines e/a-Arbeits Thread einreihen, wenn Sie in einem Thread ausgeführt werden soll, der auf einen Warn baren Zustand wartet.

Ein *nicht-e/a-Arbeits Thread* wartet auf e/a-Abschlussports. Die Verwendung von nicht-e/a-Arbeitsthreads ist effizienter als die Verwendung von e/a-Arbeitsthreads. Daher sollten Sie, wenn möglich, nicht-e/a-Arbeitsthreads verwenden. Sowohl e/a-als auch nicht-e/a-Arbeitsthreads werden nicht beendet, wenn ausstehende asynchrone e/a-Anforderungen vorliegen. Beide Arten von Threads können von Arbeits Elementen verwendet werden, die asynchrone e/a-Abschluss Anforderungen initiieren. Vermeiden Sie jedoch das Veröffentlichen von asynchronen e/a-Abschluss Anforderungen in nicht-e/a-Arbeitsthreads, wenn die Ausführung lange dauern könnte.

Um das Thread Pooling verwenden zu können, müssen die Arbeitselemente und alle Funktionen, die Sie aufzurufen, Thread Pool sicher sein. Eine sichere Funktion geht davon aus, dass es sich bei dem ausgeführten Thread um einen dedizierten oder persistenten Thread handelt. Im Allgemeinen sollten Sie die Verwendung von [Thread lokalem Speicher](thread-local-storage.md) oder das Ausführen eines asynchronen Aufrufes vermeiden, der einen persistenten Thread benötigt, z. b. die [**RegNotifyChangeKeyValue**](/windows/win32/api/winreg/nf-winreg-regnotifychangekeyvalue) -Funktion. Diese Funktionen können jedoch in einem dedizierten (von der Anwendung erstellten) Thread oder in eine Warteschlange für einen persistenten Arbeits Thread (mithilfe von [**QueueUserWorkItem**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-queueuserworkitem) mit der WT \_ executeinpersistentthread-Option) aufgerufen werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Warn Bare e/a](../fileio/alertable-i-o.md)
</dt> <dt>

[Asynchrone Prozedur Aufrufe](../sync/asynchronous-procedure-calls.md)
</dt> <dt>

[E/a-Abschlussports](../fileio/i-o-completion-ports.md)
</dt> <dt>

[Thread Pools](thread-pools.md)
</dt> </dl>

 

 
