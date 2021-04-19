---
description: Die Funktion "kreatetimerqueue" erstellt eine Warteschlange für Timer.
ms.assetid: ee85a6c3-3a1d-4f94-9112-cb8247b2a189
title: Timer-Warteschlangen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80ad2f94612c234b3ec0d1d75fa723c4e86e6fc0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363498"
---
# <a name="timer-queues"></a><span data-ttu-id="8ff86-103">Timer-Warteschlangen</span><span class="sxs-lookup"><span data-stu-id="8ff86-103">Timer Queues</span></span>

<span data-ttu-id="8ff86-104">Die Funktion " [**kreatetimerqueue**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueue) " erstellt eine Warteschlange für Timer.</span><span class="sxs-lookup"><span data-stu-id="8ff86-104">The [**CreateTimerQueue**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueue) function creates a queue for timers.</span></span> <span data-ttu-id="8ff86-105">Timer in dieser Warteschlange, die als *Timer-Queue-Timer* bezeichnet werden, sind Lightweight-Objekte, die es Ihnen ermöglichen, eine Rückruffunktion anzugeben, die aufgerufen wird, wenn die angegebene Fälligkeits Zeit erreicht wird.</span><span class="sxs-lookup"><span data-stu-id="8ff86-105">Timers in this queue, known as *timer-queue timers*, are lightweight objects that enable you to specify a callback function to be called when the specified due time arrives.</span></span> <span data-ttu-id="8ff86-106">Der Warte Vorgang wird von einem Thread im [Thread Pool](../procthread/thread-pooling.md)ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8ff86-106">The wait operation is performed by a thread in the [thread pool](../procthread/thread-pooling.md).</span></span>

<span data-ttu-id="8ff86-107">Um der Warteschlange einen Zeitgeber hinzuzufügen, müssen Sie [**die Funktion "**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) die Funktion" "" ".</span><span class="sxs-lookup"><span data-stu-id="8ff86-107">To add a timer to the queue, call the [**CreateTimerQueueTimer**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) function.</span></span> <span data-ttu-id="8ff86-108">Um einen Timer für Timer-Queue zu aktualisieren, nennen Sie die [**changetimerqueuetimer**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-changetimerqueuetimer) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="8ff86-108">To update a timer-queue timer, call the [**ChangeTimerQueueTimer**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-changetimerqueuetimer) function.</span></span> <span data-ttu-id="8ff86-109">Sie können eine Rückruffunktion angeben, die von einem Arbeits Thread aus dem Thread Pool ausgeführt wird, wenn der Zeitgeber abläuft.</span><span class="sxs-lookup"><span data-stu-id="8ff86-109">You can specify a callback function to be executed by a worker thread from the thread pool when the timer expires.</span></span>

<span data-ttu-id="8ff86-110">Um einen ausstehenden Timer abzubrechen, rufen Sie die [**deletetimerqueuetimer**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueuetimer) -Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="8ff86-110">To cancel a pending timer, call the [**DeleteTimerQueueTimer**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueuetimer) function.</span></span> <span data-ttu-id="8ff86-111">Wenn Sie mit der Warteschlange für Timer fertig sind, müssen Sie die [**deletetimerqueueex**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueueex) -Funktion aufrufen, um die Zeit Geber Warteschlange zu löschen.</span><span class="sxs-lookup"><span data-stu-id="8ff86-111">When you are finished with the queue of timers, call the [**DeleteTimerQueueEx**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueueex) function to delete the timer queue.</span></span> <span data-ttu-id="8ff86-112">Alle ausstehenden Timer in der Warteschlange werden abgebrochen und gelöscht.</span><span class="sxs-lookup"><span data-stu-id="8ff86-112">Any pending timers in the queue are canceled and deleted.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8ff86-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8ff86-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8ff86-114">Verwenden von Timer</span><span class="sxs-lookup"><span data-stu-id="8ff86-114">Using Timer Queues</span></span>](using-timer-queues.md)
</dt> </dl>

 

 
