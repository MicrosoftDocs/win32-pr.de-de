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
# <a name="using-the-microsoft-gesture-recognizer-only"></a>Nur die Gestenerkennung von Microsoft verwenden

Sie können einen frei Hand Sammler ([**InkCollector**](inkcollector-class.md), [**InkOverlay**](inkoverlay-class.md)oder [InkPicture](inkpicture-control-reference.md)) verwenden, um direkt auf die standardmäßige Microsoft-Gestenerkennung zuzugreifen.

So verwenden Sie einen Ink Collector, um auf die Gestenerkennung zuzugreifen:

-   Legen Sie für die [**CollectionMode**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode) -Eigenschaft des Ink Collector entweder den **inkandgesten** -oder den **GestureOnly** -Modus fest.

`inkOverlay.CollectionMode = CollectionMode.GestureOnly;`

-   Wählen Sie die Geste aus, die Sie unterstützen möchten.

`inkOverlay.SetGestureStatus(ApplicationGesture.AllGestures, true);`

-   Implementieren Sie einen Ereignishandler, der Gesten Benachrichtigungen empfängt. Im-Ereignishandler müssen Sie die Aktion implementieren, die den einzelnen empfangenen Ereignissen entspricht.
    > [!Note]  
    > Der gemischte Modus unterstützt nur Bewegungen mit nur einem Strich. Der Gesten Modus unterstützt mehrere Strich Gesten.

     

`inkOverlay.Gesture += new InkCollectorGestureEventHandler(inkOverlay_Gesture);`

Im **inkandgesten** -Modus wird jeder einzelne Strich an die Microsoft Gestenerkennung gesendet. Wenn Sie als Geste erkannt wird, die Sie aktiviert haben, wird eine Ereignis Benachrichtigung gesendet. Wenn die Anwendung die Ereignis Benachrichtigung annimmt, wird der Strich gelöscht. Wenn die Anwendung die Benachrichtigung nicht akzeptiert oder der Strich nicht als Geste erkannt wird, wird der Strich im [**Ink**](inkdisp-class.md) -Objekt gespeichert.

Im **GestureOnly** -Modus werden die Striche durch Timeouts vor und nach den Strichen getrennt. Die im Timeout gesammelten Striche werden an die Erkennung gesendet. Wenn die Striche als Geste erkannt werden, die Sie aktiviert haben, wird eine Ereignis Benachrichtigung gesendet. Die Anwendung kann das Ereignis annehmen oder ablehnen, wobei die entsprechende Aktion wirksam wird oder nicht. Im Modus "nur Gesten" werden die Striche niemals im frei Hand [**Objekt gespeichert**](inkdisp-class.md) .

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Microsoft. Ink. InkCollector. CollectionMode](/previous-versions/ms836497(v=msdn.10))
</dt> <dt>

[Microsoft. Ink. InkOverlay. CollectionMode](/previous-versions/ms833092(v=msdn.10))
</dt> <dt>

[Microsoft. Ink. InkPicture. CollectionMode](/previous-versions/ms582182(v=vs.100))
</dt> </dl>

 

 
