---
description: 'Sie können einen Ink-Collector (InkCollector, InkOverlay oder InkPicture) verwenden, um direkt auf die standardmäßige Microsoft-Gestenerkennung zu zugreifen. So verwenden Sie einen Ink-Collector für den Zugriff auf die Gestenerkennung: Legen Sie die CollectionMode-Eigenschaft des Ink-Collectors auf den InkAndGesture-Modus oder den GestureOnly-Modus.inkOverlay.CollectionMode = CollectionMode.GestureOnly fest. Wählen Sie die Geste aus, die Sie unterstützen möchten.inkOverlay.SetGestureStatus(ApplicationGesture.AllGestures, true);Implementieren Sie einen Ereignishandler, der Gestenbenachrichtigungen empfängt. Im Ereignishandler müssen Sie die Aktion implementieren, die jedem empfangenen Ereignis entspricht. Hinweis Der gemischte Modus unterstützt nur Gesten mit einem einzelnen Strich. Der Gestenmodus unterstützt mehrere Strichgesten. inkOverlay.Gesture += new InkCollectorGestureEventHandler(inkOverlay Gesture);Im InkAndGesture-Modus wird jeder einzelne Strich an die Microsoft-Gestenerkennung \_ gesendet. Wenn sie als aktivierte Geste erkannt wird, wird eine Ereignisbenachrichtigung gesendet. Wenn die Anwendung die Ereignisbenachrichtigung akzeptiert, wird der Strich gelöscht. Wenn die Anwendung die Benachrichtigung nicht akzeptiert oder der Strich nicht als Geste erkannt wird, wird der Strich im Ink-Objekt gespeichert. Im GestureOnly-Modus werden die Striche durch Timeouts vor und nach den Strichen getrennt. Die innerhalb des Timeouts erfassten Striche werden an die -Erkannte gesendet. Wenn die Striche als aktivierte Geste erkannt werden, wird eine Ereignisbenachrichtigung gesendet. Die Anwendung kann das Ereignis akzeptieren oder ablehnen, was die entsprechende Aktion zur Folge hat oder nicht. Im gestenbasierten Modus werden die Striche nie im Ink-Objekt gespeichert.'
ms.assetid: 3f5f00a3-1f2c-4fa2-9738-bc5fb56e2208
title: Ausschließliches Verwenden der Microsoft-Gestenerkennung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08d7b27ae30e0bba98ee2c9db57cc0da2d6491932d0137cc5cd4d2b6f86420ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118715177"
---
# <a name="using-the-microsoft-gesture-recognizer-only"></a>Ausschließliches Verwenden der Microsoft-Gestenerkennung

Sie können einen Ink-Collector ([**InkCollector**](inkcollector-class.md), [**InkOverlay**](inkoverlay-class.md)oder [InkPicture](inkpicture-control-reference.md)) verwenden, um direkt auf die standardmäßige Microsoft-Gestenerkennung zu zugreifen.

So verwenden Sie einen Ink-Collector für den Zugriff auf die Gestenerkennung:

-   Legen Sie [**die CollectionMode-Eigenschaft**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode) des Ink-Collectors entweder auf **den InkAndGesture-Modus** oder den **GestureOnly-Modus** fest.

`inkOverlay.CollectionMode = CollectionMode.GestureOnly;`

-   Wählen Sie die Geste aus, die Sie unterstützen möchten.

`inkOverlay.SetGestureStatus(ApplicationGesture.AllGestures, true);`

-   Implementieren Sie einen Ereignishandler, der Gestenbenachrichtigungen empfängt. Im Ereignishandler müssen Sie die Aktion implementieren, die jedem empfangenen Ereignis entspricht.
    > [!Note]  
    > Der gemischte Modus unterstützt nur Einzelstrichgesten. Der Gestenmodus unterstützt mehrere Strichgesten.

     

`inkOverlay.Gesture += new InkCollectorGestureEventHandler(inkOverlay_Gesture);`

Im **InkAndGesture-Modus** wird jeder einzelne Strich an die Gestenerkennung von Microsoft gesendet. Wenn sie als aktivierte Geste erkannt wird, wird eine Ereignisbenachrichtigung gesendet. Wenn die Anwendung die Ereignisbenachrichtigung akzeptiert, wird der Strich gelöscht. Wenn die Anwendung die Benachrichtigung nicht akzeptiert oder der Strich nicht als Geste erkannt wird, wird der Strich im [**Ink-Objekt**](inkdisp-class.md) gespeichert.

Im **GestureOnly-Modus** werden die Striche durch Timeouts vor und nach den Strichen getrennt. Die innerhalb des Timeouts erfassten Striche werden an die -Erkannte gesendet. Wenn die Striche als aktivierte Geste erkannt werden, wird eine Ereignisbenachrichtigung gesendet. Die Anwendung kann das Ereignis akzeptieren oder ablehnen, was die entsprechende Aktion zur Folge hat oder nicht. Im gestenbasierten Modus werden die Striche nie im [**Ink-Objekt**](inkdisp-class.md) gespeichert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Microsoft.Ink.InkCollector.CollectionMode](/previous-versions/ms836497(v=msdn.10))
</dt> <dt>

[Microsoft.Ink.InkOverlay.CollectionMode](/previous-versions/ms833092(v=msdn.10))
</dt> <dt>

[Microsoft.Ink.InkPicture.CollectionMode](/previous-versions/ms582182(v=vs.100))
</dt> </dl>

 

 
