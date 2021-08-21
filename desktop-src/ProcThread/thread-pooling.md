---
description: Es gibt viele Anwendungen, die Threads erstellen, die viel Zeit im In-/Aus-Zustand auf ein Ereignis warten.
ms.assetid: a5e52080-35d4-47f5-9050-90889e3bf2f8
title: Pooling von Threads
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c581e416952e6bac14dbf12a8f87202925a5254879b7e220c7cb2d780699f9a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120081280"
---
# <a name="thread-pooling"></a>Pooling von Threads

Es gibt viele Anwendungen, die Threads erstellen, die viel Zeit im In-/Aus-Zustand auf ein Ereignis warten. Andere Threads können in den Zustand "In den Zustand "In den Zustand" wechseln, um in regelmäßigen Abständen nach Einer Änderungs- oder Aktualisierungsstatusinformationen zu fragen. *Mithilfe von Threadpooling* können Sie Threads effizienter verwenden, indem Sie ihrer Anwendung einen Pool von Arbeitsthreads bereitstellen, die vom System verwaltet werden. Mindestens ein Thread überwacht den Status aller Wartevorgänge, die sich in der Warteschlange des Threadpools befinden. Wenn ein Wartevorgang abgeschlossen ist, führt ein Arbeitsthread aus dem Threadpool die entsprechende Rückruffunktion aus.

In diesem Thema wird die ursprüngliche Threadpool-API beschrieben. Die in Windows Vista eingeführte Threadpool-API ist einfacher, zuverlässiger, bietet eine bessere Leistung und bietet Entwicklern mehr Flexibilität. Informationen zur aktuellen Threadpool-API finden Sie unter [Threadpools](thread-pools.md).

Sie können auch Arbeitselemente in die Warteschlange stellen, die nicht mit einem Wartevorgang im Threadpool verknüpft sind. Rufen Sie die [**QueueUserWorkItem-Funktion**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-queueuserworkitem) auf, um an fordern, dass ein Arbeitselement von einem Thread im Threadpool behandelt wird. Diese Funktion akzeptiert einen Parameter für die Funktion, die von dem aus dem Threadpool ausgewählten Thread aufgerufen wird. Es gibt keine Möglichkeit, ein Arbeitselement abzubricht, nachdem es in die Warteschlange gestellt wurde.

[Timerwarteschlangen-Timer und](../sync/timer-queues.md) [registrierte Wartevorgänge](../sync/wait-functions.md) verwenden ebenfalls den Threadpool. Ihre Rückruffunktionen werden in die Warteschlange des Threadpools gestellt. Sie können auch die [**BindIoCompletionCallback-Funktion**](/windows/desktop/api/WinBase/nf-winbase-bindiocompletioncallback) verwenden, um asynchrone E/A-Vorgänge zu veröffentlichen. Nach Abschluss der E/A wird der Rückruf von einem Threadpoolthread ausgeführt.

Der Threadpool wird erstellt, wenn [**Sie QueueUserWorkItem**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-queueuserworkitem) oder [**BindIoCompletionCallback**](/windows/desktop/api/WinBase/nf-winbase-bindiocompletioncallback)zum ersten Mal aufrufen oder wenn ein Timerwarteschlangen-Timer oder registrierter Wartevorgang eine Rückruffunktion in die Warteschlange einreiht. Standardmäßig beträgt die Anzahl der Threads, die im Threadpool erstellt werden können, etwa 500. Jeder Thread verwendet die Standardstapelgröße und wird mit der Standardpriorität ausgeführt.

Es gibt zwei Arten von Arbeitsthreads im Threadpool: E/A und Nicht-E/A. Ein *E/A-Arbeitsthread* ist ein Thread, der in einem wartbaren Wartezustand wartet. Arbeitselemente werden als asynchrone Prozeduraufrufe (APC) in E/A-Arbeitsthreads in die Warteschlange gestellt. Sie sollten ein Arbeitselement in die Warteschlange eines E/A-Arbeitsthreads stellen, wenn es in einem Thread ausgeführt werden soll, der in einem wartbaren Zustand wartet.

Ein *Nicht-E/A-Arbeitsthread* wartet auf E/A-Abschlussports. Die Verwendung von Nicht-E/A-Arbeitsthreads ist effizienter als die Verwendung von E/A-Arbeitsthreads. Daher sollten Sie nach Möglichkeit Nicht-E/A-Arbeitsthreads verwenden. E/A- und Nicht-E/A-Arbeitsthreads werden nicht beendet, wenn asynchrone E/A-Anforderungen ausstehen. Beide Threadtypen können von Arbeitselementen verwendet werden, die asynchrone E/A-Abschlussanforderungen initiieren. Vermeiden Sie es jedoch, asynchrone E/A-Abschlussanforderungen in Nicht-E/A-Arbeitsthreads zu veröffentlichen, wenn dies lange dauern kann.

Um Threadpooling zu verwenden, müssen die Arbeitselemente und alle funktionen, die sie aufrufen, threadpoolsicher sein. Eine sichere Funktion geht nicht davon aus, dass es sich bei dem Thread, der sie ausgeführt, um einen dedizierten oder persistenten Thread handelt. Im Allgemeinen sollten Sie die Verwendung des lokalen [Threadspeichers](thread-local-storage.md) oder einen asynchronen Aufruf vermeiden, der einen persistenten Thread erfordert, z. B. die [**RegNotifyChangeKeyValue-Funktion.**](/windows/win32/api/winreg/nf-winreg-regnotifychangekeyvalue) Solche Funktionen können jedoch für einen dedizierten Thread aufgerufen (von der Anwendung erstellt) oder in eine Warteschlange eines permanenten Arbeitsthreads gestellt werden (mit [**queueUserWorkItem**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-queueuserworkitem) mit der WT \_ EXECUTEINPERSISTENTTHREAD-Option).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Warnungsfähige E/A](../fileio/alertable-i-o.md)
</dt> <dt>

[Asynchrone Prozeduraufrufe](../sync/asynchronous-procedure-calls.md)
</dt> <dt>

[E/A-Abschlussports](../fileio/i-o-completion-ports.md)
</dt> <dt>

[Threadpools](thread-pools.md)
</dt> </dl>

 

 
