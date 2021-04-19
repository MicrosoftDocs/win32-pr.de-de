---
description: Verwenden des Fenstermodus
ms.assetid: 09ee4568-348b-4cf9-bb38-dada291cdef9
title: Verwenden des Fenstermodus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95309f5546ce4f00a8dde029390b2edf48544f1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368855"
---
# <a name="using-windowed-mode"></a>Verwenden des Fenstermodus

> [!Note]  
> Der Legacy- [Videorenderer-Filter](video-renderer-filter.md) verwendet immer den Fenstermodus. Der VMR-7-und der VMR-9-Filter verwenden standardmäßig den Fenstermodus, unterstützen aber auch den fensterlosen Modus.

 

Im Fenstermodus erstellt der Videorenderer ein eigenes Fenster, in dem die Video Frames gezeichnet werden. Wenn Sie nicht anders angeben, ist dieses Fenster ein Fenster der obersten Ebene mit seinen eigenen Rahmen und Titelleiste. In den meisten Fällen fügen Sie jedoch das Videofenster an ein Anwendungsfenster an, damit das Video in die Benutzeroberfläche der Anwendung integriert ist. Gehen Sie dazu folgendermaßen vor:

1.  Abfrage für **IVideoWindow**.
2.  Legen Sie das übergeordnete Fenster fest.
3.  Legen Sie neue Fenster Stile fest.
4.  Positionieren Sie das Videofenster im Fenster Besitzer.
5.  Benachrichtigen Sie das Videofenster über das \_ Verschieben von Nachrichten von WM.

**Abfrage für IVideoWindow**

Fragen Sie vor der Wiedergabe den Filter Graph-Manager nach der **IVideoWindow** -Schnittstelle ab:


```C++
IVideoWindow *pVidWin = NULL;
pGraph->QueryInterface(IID_IVideoWindow, (void **)&pVidWin);
```



**Übergeordnetes Fenster festlegen**

Um das übergeordnete Fenster festzulegen, müssen Sie die [**:p UT- \_ Besitzer**](/windows/desktop/api/Control/nf-control-ivideowindow-put_owner) Methode mit einem Handle für das Anwendungsfenster aufzurufen. Diese Methode nimmt eine Variable vom Typ [**oahwnd**](oahwnd.md)auf, deshalb wandeln Sie den Handle in diesen Typ um:


```C++
pVidWin->put_Owner((OAHWND)hwnd);
```



**Neue Fenster Stile festlegen**

Ändern Sie den Stil des Videofensters, indem Sie die Methode [**IVideoWindow::p UT \_ WindowStyle**](/windows/desktop/api/Control/nf-control-ivideowindow-put_windowstyle) aufrufen:


```C++
pVidWin->put_WindowStyle(WS_CHILD | WS_CLIPSIBLINGS);
```



Mit dem untergeordneten WS \_ -Flag wird das Fenster als untergeordnetes Fenster festgelegt, und das WS \_ clipneben-Flag verhindert, dass das Fenster innerhalb des Client Bereichs eines anderen untergeordneten Fensters gezeichnet wird.

**Positionieren des Video Fensters**

Um die Position des Videos relativ zum Client Bereich des Anwendungsfensters festzulegen, müssen Sie die [**IVideoWindow:: SetWindowPosition**](/windows/desktop/api/Control/nf-control-ivideowindow-setwindowposition) -Methode aufrufen. Diese Methode nimmt ein Rechteck an, das den linken Rand, den oberen Rand, die Breite und die Höhe des Videofensters angibt. Mit dem folgenden Code wird z. b. das Videofenster so gestreckt, dass es dem gesamten Client Bereich des übergeordneten Fensters entspricht:


```C++
RECT rc;
GetClientRect(hwnd, &rc);
pVidWin->SetWindowPosition(0, 0, rc.right, rc.bottom);
```



Um die systemeigene Größe des Videos abzurufen, müssen Sie die [**ibasicvideo:: getvideosize**](/windows/desktop/api/Control/nf-control-ibasicvideo-getvideosize) -Methode für den Filter Graph-Manager aufrufen. Sie können diese Informationen verwenden, um das Video zu skalieren und das richtige Seitenverhältnis beizubehalten.

**Antworten auf WM-Verschiebungs \_ Meldungen**

Um die optimale Leistung zu erzielen, sollten Sie den Videorenderer Benachrichtigen, wenn das Fenster bewegt wird, während das Diagramm angehalten wird. Um die WM-Verschiebungs Nachricht weiterzuleiten, wenden Sie die [**IVideoWindow:: notifyownermessage**](/windows/desktop/api/Control/nf-control-ivideowindow-notifyownermessage) -Methode an \_ :


```C++
// (Inside your WindowProc)
case WM_MOVE:
    pVidWin->NotifyOwnerMessage((OAHWND)hWnd, msg, wParam, lParam);
    break;
```



Wenn der Renderer eine Hardware Überlagerung verwendet, bewirkt diese Benachrichtigung, dass der Renderer die Überlagerungs Position aktualisiert. (VMR-9 verwendet keine Überlagerungen, daher müssen Sie diese Methode nicht aufzurufen, wenn Sie VMR-9 verwenden.)

**Bereinigen**

Bevor die Anwendung beendet wird, beenden Sie das Diagramm, und setzen Sie den Besitzer des Videofensters auf **null** zurück. Andernfalls werden möglicherweise Fenster Meldungen an das falsche Fenster gesendet, was wahrscheinlich zu Fehlern führt. Außerdem können Sie das Videofenster ausblenden, oder Sie sehen, dass auf dem Bildschirm vorübergehend ein Video Bild flimmern angezeigt wird:


```C++
pControl->Stop(); 
pVidWin->put_Visible(OAFALSE);
pVidWin->put_Owner(NULL);  
```



> [!Note]  
> Wenn das übergeordnete Element des Videofensters ein untergeordnetes Element des Haupt Anwendungsfensters ist (d. h., wenn das Videofenster einem untergeordneten Element untergeordnet ist), sollten Sie das Videofenster mithilfe von **cokreateinstance** erstellen und dem Diagramm hinzufügen, anstatt den Filter Diagramm-Manager bei [intelligenter Verbindung](intelligent-connect.md)hinzufügen zu lassen. Dadurch wird sichergestellt, dass das Videofenster und das untergeordnete Fenster gleichzeitig neu gezeichnet werden. Andernfalls wird das untergeordnete Fenster möglicherweise über das Videofenster gezeichnet.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Videorendering](video-rendering.md)
</dt> </dl>

 

 



