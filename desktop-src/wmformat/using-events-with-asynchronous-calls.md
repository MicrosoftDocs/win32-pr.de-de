---
title: Verwenden von Ereignissen mit asynchronen Aufrufen
description: Verwenden von Ereignissen mit asynchronen Aufrufen
ms.assetid: 98c24176-a632-400e-b23b-5e13f1bd9a27
keywords:
- Windows Media-Format-SDK, Ereignisse mit asynchronen Aufrufen
- Windows Media-Format-SDK, asynchrone Ereignis Aufrufe
- Ereignisse, asynchrone Aufrufe
- asynchrone Aufrufe von Ereignissen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1729108cae5b73ec96be208709c1360e9401ac0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388635"
---
# <a name="using-events-with-asynchronous-calls"></a><span data-ttu-id="daf78-107">Verwenden von Ereignissen mit asynchronen Aufrufen</span><span class="sxs-lookup"><span data-stu-id="daf78-107">Using Events with Asynchronous Calls</span></span>

<span data-ttu-id="daf78-108">Häufig können Sie bei der Verwendung von Methoden, die asynchron aufgerufen werden, die weitere Verarbeitung der Anwendung anhalten, bis die-Methode die Verarbeitung abgeschlossen hat.</span><span class="sxs-lookup"><span data-stu-id="daf78-108">Frequently, when using methods that are called asynchronously, you will want to halt further processing of your application until after the method completes processing.</span></span> <span data-ttu-id="daf78-109">Sie können jedes Verfahren implementieren, das Sie für diese Situation ausführen möchten.</span><span class="sxs-lookup"><span data-stu-id="daf78-109">You can implement any technique you like to handle this situation.</span></span> <span data-ttu-id="daf78-110">In diesem Abschnitt wird beschrieben, wie Sie mit einem Ereignis auf asynchrone Aufrufe im aufrufenden Thread warten.</span><span class="sxs-lookup"><span data-stu-id="daf78-110">This section describes using an event to wait for asynchronous calls in the calling thread.</span></span> <span data-ttu-id="daf78-111">Dieses Verfahren wird häufig mit dem SDK für den Windows Media-Format verwendet und wird in einigen der Beispielanwendungen veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="daf78-111">This technique is frequently used with the Windows Media Format SDK, and is demonstrated in some of the sample applications.</span></span>

<span data-ttu-id="daf78-112">In der folgenden Liste wird die Verwendung von Ereignissen für das warten auf asynchrone Aufrufe zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="daf78-112">The following list summarizes the use of events to wait for asynchronous calls.</span></span>

1.  <span data-ttu-id="daf78-113">Erstellen Sie ein Ereignis für die Verwendung mit Ihrer Anwendung, indem Sie die **CreateEvent** -Funktion des Platform SDK aufrufen.</span><span class="sxs-lookup"><span data-stu-id="daf78-113">Create an event for use with your application by calling the **CreateEvent** function of the Platform SDK.</span></span>
2.  <span data-ttu-id="daf78-114">Wenn Sie die entsprechenden Rückrufe für die Anwendung implementieren, fangen Sie die Nachrichten ab, die Sie warten müssen.</span><span class="sxs-lookup"><span data-stu-id="daf78-114">When implementing the appropriate callbacks for your application, trap the messages for which you need to wait.</span></span> <span data-ttu-id="daf78-115">Signalisieren Sie in der Meldungs Behandlungs Logik für die gewünschten Nachrichten das Ereignis, indem Sie die Funktion " **settevent** " des Platform SDK aufrufen.</span><span class="sxs-lookup"><span data-stu-id="daf78-115">In the message handling logic for the desired messages, signal the event by calling the **SetEvent** function of the Platform SDK.</span></span>
3.  <span data-ttu-id="daf78-116">Nachdem Aufrufe von asynchronen Ereignissen in der Anwendung vorgenommen wurden, warten Sie, bis das Ereignis signalisiert, indem Sie die **WaitForSingleObject** -Funktion des Platform SDK aufrufen.</span><span class="sxs-lookup"><span data-stu-id="daf78-116">After calls to asynchronous events are made in your application, wait for the event to signal by calling the **WaitForSingleObject** function of the Platform SDK.</span></span> <span data-ttu-id="daf78-117">Wenn Sie eine Windows-Anwendung entwerfen, sollten Sie eine Schleife zum Überprüfen auf Windows-Meldungen erstellen und einen Aufruf von **WaitForSingleObject** in der Schleife mit einer kurzen Wartezeit einschließen.</span><span class="sxs-lookup"><span data-stu-id="daf78-117">If you are designing a Windows application, you should create a loop to check for Windows messages and include a call to **WaitForSingleObject** in the loop with a short wait time.</span></span>

## <a name="related-topics"></a><span data-ttu-id="daf78-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="daf78-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="daf78-119">**Verwenden der Rückruf Methoden**</span><span class="sxs-lookup"><span data-stu-id="daf78-119">**Using the Callback Methods**</span></span>](using-the-callback-methods.md)
</dt> </dl>

 

 




