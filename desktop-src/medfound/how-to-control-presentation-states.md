---
description: Steuern von Präsentations Zuständen
ms.assetid: 978373ef-b2a4-4035-b889-e28a037c0ab5
title: Steuern von Präsentations Zuständen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7a82fe0363a27b9c6f5c054b73ca409835a3dff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350516"
---
# <a name="how-to-control-presentation-states"></a><span data-ttu-id="1b8ed-103">Steuern von Präsentations Zuständen</span><span class="sxs-lookup"><span data-stu-id="1b8ed-103">How to Control Presentation States</span></span>

<span data-ttu-id="1b8ed-104">Die Medien Sitzung bietet Transport Steuerelemente, z. b. das Ändern von Präsentations Zuständen (wiedergeben, anhalten und stoppen in einem Wiedergabe Szenario mit Wiedergabelisten).</span><span class="sxs-lookup"><span data-stu-id="1b8ed-104">The Media Session provides transport control such as changing presentation states (Play, Pause, and Stop in a playlist-style playback scenario).</span></span> <span data-ttu-id="1b8ed-105">In diesem Thema werden die Methoden der Medien Sitzungen beschrieben, die eine Anwendung zum Ändern des Wiedergabe Zustands aufruft.</span><span class="sxs-lookup"><span data-stu-id="1b8ed-105">This topic describes Media Session methods that an application should call to change the playback state.</span></span>

<span data-ttu-id="1b8ed-106">In der folgenden Tabelle sind die gültigen Präsentations Zustandsübergänge aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="1b8ed-106">The following table shows the valid presentation state transitions.</span></span>



| <span data-ttu-id="1b8ed-107">Zustandsübergang</span><span class="sxs-lookup"><span data-stu-id="1b8ed-107">State transition</span></span> | <span data-ttu-id="1b8ed-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1b8ed-108">Description</span></span>                                                                                |
|------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b8ed-109">Wiedergabe > Pause</span><span class="sxs-lookup"><span data-stu-id="1b8ed-109">Play -> Pause</span></span> | <span data-ttu-id="1b8ed-110">Die Präsentations Uhr friert.</span><span class="sxs-lookup"><span data-stu-id="1b8ed-110">The presentation clock freezes.</span></span>                                                            |
| <span data-ttu-id="1b8ed-111">Wiedergabe > Beendigung</span><span class="sxs-lookup"><span data-stu-id="1b8ed-111">Play -> Stop</span></span>  | <span data-ttu-id="1b8ed-112">Die Präsentations Uhr wird zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="1b8ed-112">The presentation clock is reset.</span></span>                                                           |
| <span data-ttu-id="1b8ed-113">Pause > Wiedergabe</span><span class="sxs-lookup"><span data-stu-id="1b8ed-113">Pause -> Play</span></span> | <span data-ttu-id="1b8ed-114">Die Präsentations Uhr wird von der Zeit wieder aufgenommen, die während der Wiedergabe zum Anhalten des Übergangs gewechselt ist.</span><span class="sxs-lookup"><span data-stu-id="1b8ed-114">The presentation clock resumes from the time it froze during the Play to Pause transition.</span></span> |
| <span data-ttu-id="1b8ed-115">Anhalten-> anhalten</span><span class="sxs-lookup"><span data-stu-id="1b8ed-115">Pause -> Stop</span></span> | <span data-ttu-id="1b8ed-116">Die Präsentations Uhr wird zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="1b8ed-116">The presentation clock is reset.</span></span>                                                           |
| <span data-ttu-id="1b8ed-117">Wiedergabe ></span><span class="sxs-lookup"><span data-stu-id="1b8ed-117">Stop -> Play</span></span>  | <span data-ttu-id="1b8ed-118">Die Präsentations Uhr beginnt am Anfang der Präsentation.</span><span class="sxs-lookup"><span data-stu-id="1b8ed-118">The presentation clock starts from the beginning of the presentation.</span></span>                      |
| <span data-ttu-id="1b8ed-119">Anhalten-> anhalten</span><span class="sxs-lookup"><span data-stu-id="1b8ed-119">Stop -> Pause</span></span> | <span data-ttu-id="1b8ed-120">Nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="1b8ed-120">Not allowed.</span></span>                                                                               |



 

## <a name="to-change-presentation-states"></a><span data-ttu-id="1b8ed-121">So ändern Sie Darstellungs Zustände</span><span class="sxs-lookup"><span data-stu-id="1b8ed-121">To change presentation states</span></span>

-   <span data-ttu-id="1b8ed-122">Wenden Sie die [**imfmediasession::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause) -Methode an, um die Wiedergabe anzuhalten.</span><span class="sxs-lookup"><span data-stu-id="1b8ed-122">Call the [**IMFMediaSession::Pause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause) method to pause playback.</span></span>

    ```C++
    hr = pMediaSession->Pause();
    ```

    

    <span data-ttu-id="1b8ed-123">Vor dem Aufrufen dieser Methode muss die Anwendung die [**imfmediasession:: gezessionfunktionalitäten**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getsessioncapabilities) -Methode aufrufen, um zu ermitteln, ob die Medienquelle den anhaltezustand unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1b8ed-123">Before calling this method, the application must call the [**IMFMediaSession::GetSessionCapabilities**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getsessioncapabilities) method to discover whether the media source supports the Pause state.</span></span> <span data-ttu-id="1b8ed-124">Wenn dies der Fall ist, gibt diese Methode " **mfsessioncap \_ Pause** " im *pdwcaps* -Parameter zurück.</span><span class="sxs-lookup"><span data-stu-id="1b8ed-124">If it does, this method returns **MFSESSIONCAP\_PAUSE** in the *pdwCaps* parameter.</span></span>

    <span data-ttu-id="1b8ed-125">Anhalten beendet vorübergehend die Medien Sitzung, die Präsentations Uhr und die streamsenke für die aktuelle Präsentation.</span><span class="sxs-lookup"><span data-stu-id="1b8ed-125">Pause temporarily stops the Media Session, the presentation clock, and the stream sink for the current presentation.</span></span> <span data-ttu-id="1b8ed-126">Nachdem der-Vorgang erfolgreich abgeschlossen wurde, empfängt die Anwendung ein [mesessionangeh Ed](mesessionpaused.md) -Ereignis.</span><span class="sxs-lookup"><span data-stu-id="1b8ed-126">After the call completes successfully, the application receives a [MESessionPaused](mesessionpaused.md) event.</span></span>

-   <span data-ttu-id="1b8ed-127">Wenden Sie die [**imfmediasession:: stopmethode**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop) an, um die Wiedergabe zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="1b8ed-127">Call the [**IMFMediaSession::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop) method to stop playback.</span></span>

    ```C++
    hr = pMediaSession->Stop();
    ```

    

    <span data-ttu-id="1b8ed-128">Diese Methode beendet die Medien Sitzung durch Beenden der Medienquelle, der entsprechenden Uhren und der streamsenken.</span><span class="sxs-lookup"><span data-stu-id="1b8ed-128">This method stops the Media Session by stopping the media source, the corresponding clocks, and stream sinks.</span></span> <span data-ttu-id="1b8ed-129">Wenn die Medien Sitzung die [Sequencer-Quelle](sequencer-source.md)steuert, werden die zugrunde liegenden systemeigenen Quellen von der Sequencer-Quelle beendet.</span><span class="sxs-lookup"><span data-stu-id="1b8ed-129">If the Media Session is controlling the [Sequencer Source](sequencer-source.md), the underlying native sources are stopped by the sequencer source.</span></span> <span data-ttu-id="1b8ed-130">Nachdem die Medien Sitzung beendet wurde, empfängt die Anwendung ein [mesessionbeendete](mesessionstopped.md) -Ereignis.</span><span class="sxs-lookup"><span data-stu-id="1b8ed-130">After the Media Session is stopped, the application receives a [MESessionStopped](mesessionstopped.md) event.</span></span>

-   <span data-ttu-id="1b8ed-131">Wenden Sie die [**imfmediasession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) -Methode an, um die Wiedergabe zu starten oder eine neue Position zu suchen.</span><span class="sxs-lookup"><span data-stu-id="1b8ed-131">Call the [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) method to start playback or seek to a new position.</span></span>

    ```C++
    hr = pMediaSession->Start(NULL, &var);
    ```

    

    <span data-ttu-id="1b8ed-132">Diese Methode startet die Medien Sitzung über den Status anhalten und anhalten.</span><span class="sxs-lookup"><span data-stu-id="1b8ed-132">This method starts the Media Session from Pause and Stop states.</span></span> <span data-ttu-id="1b8ed-133">Die Medien Sitzung ist für das Einrichten des Datenflusses in der Pipeline zuständig.</span><span class="sxs-lookup"><span data-stu-id="1b8ed-133">The Media Session is responsible for setting up the data flow in the pipeline.</span></span> <span data-ttu-id="1b8ed-134">Diese Methode weist die Medien Sitzung an, die Präsentations Uhr zu starten.</span><span class="sxs-lookup"><span data-stu-id="1b8ed-134">This method instructs the Media Session to start the presentation clock.</span></span> <span data-ttu-id="1b8ed-135">Nach diesem-Befehl sendet die Medien Sitzung ein [mesessionstarted](mesessionstarted.md) -Ereignis an die Anwendung.</span><span class="sxs-lookup"><span data-stu-id="1b8ed-135">After this call, Media Session sends a [MESessionStarted](mesessionstarted.md) event to the application.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1b8ed-136">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1b8ed-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1b8ed-137">Medien Sitzung</span><span class="sxs-lookup"><span data-stu-id="1b8ed-137">Media Session</span></span>](media-session.md)
</dt> </dl>

 

 



