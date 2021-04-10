---
description: Informationen zur Medien Sitzung
ms.assetid: 09f50b11-0e0a-42b6-a7bf-bb0135343351
title: Informationen zur Medien Sitzung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc490e63f623fb3c2d5efde5a80f1988566f9345
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "103961094"
---
# <a name="about-the-media-session"></a><span data-ttu-id="e4cbd-103">Informationen zur Medien Sitzung</span><span class="sxs-lookup"><span data-stu-id="e4cbd-103">About the Media Session</span></span>

<span data-ttu-id="e4cbd-104">Die Medien Sitzung macht die [**imfmediasession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) -Schnittstelle verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e4cbd-104">The Media Session exposes the [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) interface.</span></span> <span data-ttu-id="e4cbd-105">Es gibt zwei Möglichkeiten, die Medien Sitzung zu erstellen, je nachdem, ob Ihre Anwendung geschützte Inhalte unterstützt:</span><span class="sxs-lookup"><span data-stu-id="e4cbd-105">There are two ways to create the Media Session, depending on whether your application will support protected content:</span></span>

-   <span data-ttu-id="e4cbd-106">Wenn Ihre Anwendung geschützte Inhalte nicht unterstützt, können Sie die Medien Sitzung erstellen, indem Sie die [**mfcreatemediasession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="e4cbd-106">If your application does not support protected content, you can create the Media Session by calling the [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession).</span></span> <span data-ttu-id="e4cbd-107">Diese Funktion erstellt die Medien Sitzung innerhalb des Anwendungsprozesses.</span><span class="sxs-lookup"><span data-stu-id="e4cbd-107">This function creates the Media Session inside the application process.</span></span>
-   <span data-ttu-id="e4cbd-108">Um geschützte Inhalte zu unterstützen, erstellen Sie die Medien Sitzung, indem Sie [**mfcreatepmpmediasession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="e4cbd-108">To support protected content, create the Media Session by calling [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession).</span></span> <span data-ttu-id="e4cbd-109">Diese Funktion erstellt die Medien Sitzung innerhalb des PMP-Prozesses (Protected Media Path).</span><span class="sxs-lookup"><span data-stu-id="e4cbd-109">This function creates the Media Session inside the Protected Media Path (PMP) process.</span></span> <span data-ttu-id="e4cbd-110">Die Anwendung empfängt einen Zeiger auf ein Proxy Objekt, das Methodenaufrufe über die Prozess Grenze hinweg marshallen.</span><span class="sxs-lookup"><span data-stu-id="e4cbd-110">The application receives a pointer to a proxy object that marshals method calls across the process boundary.</span></span> <span data-ttu-id="e4cbd-111">Beachten Sie, dass die PMP-Medien Sitzung verwendet werden kann, um Klartext und geschützte Inhalte wiederzugeben.</span><span class="sxs-lookup"><span data-stu-id="e4cbd-111">Note that the PMP Media Session can be used to play clear content, as well as protected content.</span></span>

<span data-ttu-id="e4cbd-112">Jede Anwendung, die die Medien Sitzung verwendet, führt die folgenden allgemeinen Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="e4cbd-112">Any application that uses the Media Session will follow these general steps:</span></span>

1.  <span data-ttu-id="e4cbd-113">Erstellen Sie eine Topologie.</span><span class="sxs-lookup"><span data-stu-id="e4cbd-113">Create a topology.</span></span>
2.  <span data-ttu-id="e4cbd-114">Stellen Sie die Topologie in der Medien Sitzung durch Aufrufen von [**imfmediasession:: settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology)in die Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="e4cbd-114">Queue the topology on the Media Session by calling [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).</span></span>
3.  <span data-ttu-id="e4cbd-115">Steuern Sie den Datenfluss durch Aufrufen von [**imfmediasession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start), [**imfmediasession::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause)oder [**imfmediasession:: Beendigung**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop).</span><span class="sxs-lookup"><span data-stu-id="e4cbd-115">Control the flow of data by calling [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start), [**IMFMediaSession::Pause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause), or [**IMFMediaSession::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop).</span></span>
4.  <span data-ttu-id="e4cbd-116">Bevor die Anwendung beendet wird, wird [**imfmediasession:: Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) aufgerufen, um die Medien Sitzung zu schließen.</span><span class="sxs-lookup"><span data-stu-id="e4cbd-116">Before the application exits, call [**IMFMediaSession::Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) to close the Media Session.</span></span>
5.  <span data-ttu-id="e4cbd-117">Beenden Sie alle Medienquellen, die von der Anwendung erstellt wurden, durch Aufrufen von [**imfmediasource:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown).</span><span class="sxs-lookup"><span data-stu-id="e4cbd-117">Shut down any media sources that the application created, by calling [**IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown).</span></span>
6.  <span data-ttu-id="e4cbd-118">Beenden Sie die Medien Sitzung, indem Sie [**imfmediasession:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="e4cbd-118">Shut down the Media Session by calling [**IMFMediaSession::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown).</span></span>

<span data-ttu-id="e4cbd-119">Wenn Sie die Medien Sitzung verwenden, sollte die Anwendung die Medienquelle nicht direkt starten, anhalten oder beenden.</span><span class="sxs-lookup"><span data-stu-id="e4cbd-119">When using the Media Session, the application should not directly start, pause, or stop the media source.</span></span> <span data-ttu-id="e4cbd-120">Alle Zustandsänderungen müssen durch Aufrufen von [**imfmediasession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) -Methoden initiiert werden.</span><span class="sxs-lookup"><span data-stu-id="e4cbd-120">All state changes must be initiated by calling [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) methods.</span></span> <span data-ttu-id="e4cbd-121">Zustandsänderungen in der Medienquelle werden von der Medien Sitzung behandelt.</span><span class="sxs-lookup"><span data-stu-id="e4cbd-121">State changes in the media source are handled by the Media Session.</span></span>

<span data-ttu-id="e4cbd-122">Viele weitere Details hängen von der spezifischen Funktionalität Ihrer Anwendung ab.</span><span class="sxs-lookup"><span data-stu-id="e4cbd-122">Many other details will depend on the specific functionality of your application.</span></span>

## <a name="protected-content"></a><span data-ttu-id="e4cbd-123">Geschützter Inhalt</span><span class="sxs-lookup"><span data-stu-id="e4cbd-123">Protected Content</span></span>

<span data-ttu-id="e4cbd-124">Um geschützte Inhalte wiederzugeben, müssen Sie die Medien Sitzung im geschützten Medien Pfad (PMP) erstellen, indem Sie [**mfcreatepmpmediasession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="e4cbd-124">To play protected content, you must create the Media Session inside the protected media path (PMP), by calling [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession).</span></span> <span data-ttu-id="e4cbd-125">Diese Funktion erstellt eine Instanz der Medien Sitzung innerhalb des PMP und gibt einen Zeiger auf ein Proxy Objekt zurück, das Schnittstellen über die Prozess Grenze hinweg marshunkt.</span><span class="sxs-lookup"><span data-stu-id="e4cbd-125">This function creates an instance of the Media Session inside the PMP and returns a pointer to a proxy object that marshals interfaces across the process boundary.</span></span>

<span data-ttu-id="e4cbd-126">In den meisten Fällen ist die Verwendung der Medien Sitzung innerhalb des PMP für die Anwendung transparent.</span><span class="sxs-lookup"><span data-stu-id="e4cbd-126">In most respects, using the Media Session inside the PMP is transparent to the application.</span></span> <span data-ttu-id="e4cbd-127">Allerdings muss die Anwendung möglicherweise bestimmte Aktionen aufrufen, die dem Benutzer die Wiedergabe des Inhalts ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="e4cbd-127">However, the application might need to invoke certain actions that enable the user to play the content.</span></span> <span data-ttu-id="e4cbd-128">Beispielsweise muss der Benutzer möglicherweise eine DRM-Lizenz erwerben.</span><span class="sxs-lookup"><span data-stu-id="e4cbd-128">For example, the user might need to obtain a DRM license.</span></span> <span data-ttu-id="e4cbd-129">Media Foundation definiert einen generischen Mechanismus für diese Aktionen mithilfe der [**IMF contentenabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="e4cbd-129">Media Foundation defines a generic mechanism for these actions using the [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) interface.</span></span>

<span data-ttu-id="e4cbd-130">Weitere Informationen finden Sie unter den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="e4cbd-130">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="e4cbd-131">Geschützter Medien Pfad</span><span class="sxs-lookup"><span data-stu-id="e4cbd-131">Protected Media Path</span></span>](protected-media-path.md)
-   [<span data-ttu-id="e4cbd-132">Wiedergeben geschützter Mediendateien</span><span class="sxs-lookup"><span data-stu-id="e4cbd-132">How to Play Protected Media Files</span></span>](how-to-play-protected-media-files.md)

## <a name="presentation-clock"></a><span data-ttu-id="e4cbd-133">Präsentations Uhr</span><span class="sxs-lookup"><span data-stu-id="e4cbd-133">Presentation Clock</span></span>

<span data-ttu-id="e4cbd-134">In der Medien Sitzung werden alle Aspekte der Präsentations Uhr verwaltet:</span><span class="sxs-lookup"><span data-stu-id="e4cbd-134">The Media Session manages all aspects of the presentation clock:</span></span>

-   <span data-ttu-id="e4cbd-135">Erstellen der Präsentations Uhr.</span><span class="sxs-lookup"><span data-stu-id="e4cbd-135">Creating the presentation clock.</span></span>

-   <span data-ttu-id="e4cbd-136">Die Zeit Quelle wird ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="e4cbd-136">Selecting the time source.</span></span>

-   <span data-ttu-id="e4cbd-137">Benachrichtigen der Medien senken über die Uhr</span><span class="sxs-lookup"><span data-stu-id="e4cbd-137">Notifying the media sinks about the clock</span></span>

-   <span data-ttu-id="e4cbd-138">Starten, beenden und Anhalten der Uhr nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="e4cbd-138">Starting, stopping, and pausing the clock as necessary.</span></span>

-   <span data-ttu-id="e4cbd-139">Die Uhr wird heruntergefahren.</span><span class="sxs-lookup"><span data-stu-id="e4cbd-139">Shutting down the clock.</span></span>

<span data-ttu-id="e4cbd-140">Um einen Zeiger auf die Präsentations Uhr zu erhalten, nennen Sie [**imfmediasession:: getclock**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getclock) für die Medien Sitzung.</span><span class="sxs-lookup"><span data-stu-id="e4cbd-140">To get a pointer to the presentation clock, call [**IMFMediaSession::GetClock**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getclock) on the Media Session.</span></span> <span data-ttu-id="e4cbd-141">Die Präsentations Uhr gibt keine gültige Zeit zurück, bis die Medien Sitzung das [mesessiontopologystatus](mesessiontopologystatus.md) -Ereignis mit dem MF- \_ Flag "topostatusready" sendet \_ .</span><span class="sxs-lookup"><span data-stu-id="e4cbd-141">The presentation clock does not return a valid time until the Media Session sends the [MESessionTopologyStatus](mesessiontopologystatus.md) event with the MF\_TOPOSTATUS\_READY flag.</span></span> <span data-ttu-id="e4cbd-142">Bis zu diesem Zeitpunkt gibt **getclock** die "MF \_ E \_ Clock \_ No Time"- \_ Quelle zurück \_ .</span><span class="sxs-lookup"><span data-stu-id="e4cbd-142">Until then, **GetClock** returns MF\_E\_CLOCK\_NO\_TIME\_SOURCE.</span></span>

<span data-ttu-id="e4cbd-143">Eine Anwendung, die die Medien Sitzung verwendet, sollte die Präsentations Uhr nie starten, beenden oder anhalten. Ändern Sie die Taktrate. oder beenden Sie die Uhr.</span><span class="sxs-lookup"><span data-stu-id="e4cbd-143">An application that uses the Media Session should never start, stop, or pause the presentation clock; change the clock rate; or shut down the clock.</span></span>

<span data-ttu-id="e4cbd-144">Wenn die Anwendung [**imfmediasession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start)aufruft, startet die Medien Sitzung die Präsentations Uhr mit einer Startzeit, die der Anfangsposition entspricht, die in der **Start** -Methode angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="e4cbd-144">When the application calls [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start), the Media Session starts the presentation clock with a starting time equal to the starting position specified in the **Start** method.</span></span> <span data-ttu-id="e4cbd-145">Weitere Informationen zur Medien Sitzung finden Sie unter [Medien Sitzung](media-session.md).</span><span class="sxs-lookup"><span data-stu-id="e4cbd-145">For more information about the Media Session, see [Media Session](media-session.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e4cbd-146">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e4cbd-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e4cbd-147">Medien Sitzung</span><span class="sxs-lookup"><span data-stu-id="e4cbd-147">Media Session</span></span>](media-session.md)
</dt> </dl>

 

 



