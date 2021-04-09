---
description: 'Sie können einen frei Hand Sammler (InkCollector, InkOverlay oder InkPicture) verwenden, um direkt auf die standardmäßige Microsoft-Gestenerkennung zuzugreifen. So verwenden Sie einen Ink Collector für den Zugriff auf die Gestenerkennung: Legen Sie die CollectionMode-Eigenschaft des Ink Collector entweder auf den inkandgesten-oder den GestureOnly-Modus fest. InkOverlay. CollectionMode = CollectionMode. GestureOnly; Wählen Sie die Geste aus, die Sie unterstützen möchten. InkOverlay. SetGestureStatus (applicationgesten. allgesten, true); implementieren Sie einen Ereignishandler, der Gesten Benachrichtigungen empfängt. Im-Ereignishandler müssen Sie die Aktion implementieren, die den einzelnen empfangenen Ereignissen entspricht. Hinweis der gemischte Modus unterstützt nur Single-Stroke-Gesten. Der Gesten Modus unterstützt mehrere Strich Gesten. InkOverlay. Gesten + = New InkCollector gestureeventhandler (InkOverlay- \_ Geste); im inkandgesten-Modus wird jeder einzelne Strich an die Microsoft Gestenerkennung gesendet. Wenn Sie als Geste erkannt wird, die Sie aktiviert haben, wird eine Ereignis Benachrichtigung gesendet. Wenn die Anwendung die Ereignis Benachrichtigung annimmt, wird der Strich gelöscht. Wenn die Anwendung die Benachrichtigung nicht akzeptiert oder der Strich nicht als Geste erkannt wird, wird der Strich im Ink-Objekt gespeichert. Im GestureOnly-Modus werden die Striche durch Timeouts vor und nach den Strichen getrennt. Die im Timeout gesammelten Striche werden an die Erkennung gesendet. Wenn die Striche als Geste erkannt werden, die Sie aktiviert haben, wird eine Ereignis Benachrichtigung gesendet. Die Anwendung kann das Ereignis annehmen oder ablehnen, wobei die entsprechende Aktion wirksam wird oder nicht. Im Modus "nur Gesten" werden die Striche niemals im frei Hand Objekt gespeichert.'
ms.assetid: 3f5f00a3-1f2c-4fa2-9738-bc5fb56e2208
title: Nur die Gestenerkennung von Microsoft verwenden
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80504e8b32c0b9596936bb4f07d029cd4ea8ddbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862491"
---
# <a name="using-the-microsoft-gesture-recognizer-only"></a><span data-ttu-id="90f63-113">Nur die Gestenerkennung von Microsoft verwenden</span><span class="sxs-lookup"><span data-stu-id="90f63-113">Using the Microsoft Gesture Recognizer Only</span></span>

<span data-ttu-id="90f63-114">Sie können einen frei Hand Sammler ([**InkCollector**](inkcollector-class.md), [**InkOverlay**](inkoverlay-class.md)oder [InkPicture](inkpicture-control-reference.md)) verwenden, um direkt auf die standardmäßige Microsoft-Gestenerkennung zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="90f63-114">You can use an ink collector ([**InkCollector**](inkcollector-class.md), [**InkOverlay**](inkoverlay-class.md), or [InkPicture](inkpicture-control-reference.md)) to access the default Microsoft gesture recognizer directly.</span></span>

<span data-ttu-id="90f63-115">So verwenden Sie einen Ink Collector, um auf die Gestenerkennung zuzugreifen:</span><span class="sxs-lookup"><span data-stu-id="90f63-115">To use an ink collector to access the gesture recognizer:</span></span>

-   <span data-ttu-id="90f63-116">Legen Sie für die [**CollectionMode**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode) -Eigenschaft des Ink Collector entweder den **inkandgesten** -oder den **GestureOnly** -Modus fest.</span><span class="sxs-lookup"><span data-stu-id="90f63-116">Set the [**CollectionMode**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode) property of the ink collector to either **InkAndGesture** mode or **GestureOnly** mode.</span></span>

`inkOverlay.CollectionMode = CollectionMode.GestureOnly;`

-   <span data-ttu-id="90f63-117">Wählen Sie die Geste aus, die Sie unterstützen möchten.</span><span class="sxs-lookup"><span data-stu-id="90f63-117">Choose the gesture that you want to support.</span></span>

`inkOverlay.SetGestureStatus(ApplicationGesture.AllGestures, true);`

-   <span data-ttu-id="90f63-118">Implementieren Sie einen Ereignishandler, der Gesten Benachrichtigungen empfängt.</span><span class="sxs-lookup"><span data-stu-id="90f63-118">Implement an event handler that receives gesture notifications.</span></span> <span data-ttu-id="90f63-119">Im-Ereignishandler müssen Sie die Aktion implementieren, die den einzelnen empfangenen Ereignissen entspricht.</span><span class="sxs-lookup"><span data-stu-id="90f63-119">In the event handler, you need to implement the action corresponding to each event received.</span></span>
    > [!Note]  
    > <span data-ttu-id="90f63-120">Der gemischte Modus unterstützt nur Bewegungen mit nur einem Strich.</span><span class="sxs-lookup"><span data-stu-id="90f63-120">Mixed mode supports only single-stroke gestures.</span></span> <span data-ttu-id="90f63-121">Der Gesten Modus unterstützt mehrere Strich Gesten.</span><span class="sxs-lookup"><span data-stu-id="90f63-121">Gesture mode supports multiple stroke gestures.</span></span>

     

`inkOverlay.Gesture += new InkCollectorGestureEventHandler(inkOverlay_Gesture);`

<span data-ttu-id="90f63-122">Im **inkandgesten** -Modus wird jeder einzelne Strich an die Microsoft Gestenerkennung gesendet.</span><span class="sxs-lookup"><span data-stu-id="90f63-122">In **InkAndGesture** mode, each individual stroke is sent to the Microsoft gesture recognizer.</span></span> <span data-ttu-id="90f63-123">Wenn Sie als Geste erkannt wird, die Sie aktiviert haben, wird eine Ereignis Benachrichtigung gesendet.</span><span class="sxs-lookup"><span data-stu-id="90f63-123">If it is recognized as a gesture that you have enabled, an event notification is sent.</span></span> <span data-ttu-id="90f63-124">Wenn die Anwendung die Ereignis Benachrichtigung annimmt, wird der Strich gelöscht.</span><span class="sxs-lookup"><span data-stu-id="90f63-124">If the application accepts the event notification, the stroke is erased.</span></span> <span data-ttu-id="90f63-125">Wenn die Anwendung die Benachrichtigung nicht akzeptiert oder der Strich nicht als Geste erkannt wird, wird der Strich im [**Ink**](inkdisp-class.md) -Objekt gespeichert.</span><span class="sxs-lookup"><span data-stu-id="90f63-125">If the application does not accept the notification or if the stroke is not recognized to be a gesture, the stroke is stored in the [**Ink**](inkdisp-class.md) object.</span></span>

<span data-ttu-id="90f63-126">Im **GestureOnly** -Modus werden die Striche durch Timeouts vor und nach den Strichen getrennt.</span><span class="sxs-lookup"><span data-stu-id="90f63-126">In **GestureOnly** mode, the strokes are delimited by timeouts before and after the strokes.</span></span> <span data-ttu-id="90f63-127">Die im Timeout gesammelten Striche werden an die Erkennung gesendet.</span><span class="sxs-lookup"><span data-stu-id="90f63-127">The strokes collected within the timeout are sent to the recognizer.</span></span> <span data-ttu-id="90f63-128">Wenn die Striche als Geste erkannt werden, die Sie aktiviert haben, wird eine Ereignis Benachrichtigung gesendet.</span><span class="sxs-lookup"><span data-stu-id="90f63-128">If the strokes are recognized as a gesture that you have enabled, an event notification is sent.</span></span> <span data-ttu-id="90f63-129">Die Anwendung kann das Ereignis annehmen oder ablehnen, wobei die entsprechende Aktion wirksam wird oder nicht.</span><span class="sxs-lookup"><span data-stu-id="90f63-129">The application may accept or reject the event, effecting the corresponding action or not.</span></span> <span data-ttu-id="90f63-130">Im Modus "nur Gesten" werden die Striche niemals im frei Hand [**Objekt gespeichert**](inkdisp-class.md) .</span><span class="sxs-lookup"><span data-stu-id="90f63-130">In gesture-only mode, the strokes are never saved in the [**Ink**](inkdisp-class.md) object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="90f63-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="90f63-131">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="90f63-132">[Microsoft. Ink. InkCollector. CollectionMode](/previous-versions/ms836497(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="90f63-132">[Microsoft.Ink.InkCollector.CollectionMode](/previous-versions/ms836497(v=msdn.10))</span></span>
</dt> <dt>

<span data-ttu-id="90f63-133">[Microsoft. Ink. InkOverlay. CollectionMode](/previous-versions/ms833092(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="90f63-133">[Microsoft.Ink.InkOverlay.CollectionMode](/previous-versions/ms833092(v=msdn.10))</span></span>
</dt> <dt>

<span data-ttu-id="90f63-134">[Microsoft. Ink. InkPicture. CollectionMode](/previous-versions/ms582182(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="90f63-134">[Microsoft.Ink.InkPicture.CollectionMode](/previous-versions/ms582182(v=vs.100))</span></span>
</dt> </dl>

 

 
