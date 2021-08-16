---
description: Verwenden des Fenstermodus
ms.assetid: 09ee4568-348b-4cf9-bb38-dada291cdef9
title: Verwenden des Fenstermodus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd5f71bfa58e46ade8c779e562278f908c8b8fd593989ed4007e6b98cb7916da
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119633090"
---
# <a name="using-windowed-mode"></a>Verwenden des Fenstermodus

> [!Note]  
> Der [Legacy-Videorendererfilter](video-renderer-filter.md) verwendet immer den Fenstermodus. Die Filter VMR-7 und VMR-9 verwenden standardmäßig den Fenstermodus, unterstützen aber auch den fensterlosen Modus.

 

Im Fenstermodus erstellt der Videorenderer ein eigenes Fenster, in dem er die Videoframes zeichnet. Sofern nicht anders angegeben, ist dieses Fenster ein Fenster der obersten Ebene mit eigenen Rahmen und titelleisten. In den meisten Jahren fügen Sie das Videofenster jedoch an ein Anwendungsfenster an, damit das Video in Ihre Anwendungsbenutzeroberfläche integriert wird. Gehen Sie dazu folgendermaßen vor:

1.  Abfrage für **IVideoWindow**.
2.  Legen Sie das übergeordnete Fenster fest.
3.  Legen Sie neue Fensterstile fest.
4.  Positionieren Sie das Videofenster im Besitzerfenster.
5.  Benachrichtigen Sie das Videofenster über WM \_ MOVE-Meldungen.

**Abfrage für IVideoWindow**

Fragen Sie vor dem Starten der Wiedergabe den Filter Graph Manager für die **IVideoWindow-Schnittstelle** ab:


```C++
IVideoWindow *pVidWin = NULL;
pGraph->QueryInterface(IID_IVideoWindow, (void **)&pVidWin);
```



**Festlegen des übergeordneten Fensters**

Um das übergeordnete Fenster festzulegen, rufen Sie die [**IVideoWindow::p ut \_ Owner-Methode**](/windows/desktop/api/Control/nf-control-ivideowindow-put_owner) mit einem Handle für Ihr Anwendungsfenster auf. Diese Methode nimmt eine Variable vom Typ [**OAHWND**](oahwnd.md)an, also wandeln Sie das Handle in diesen Typ um:


```C++
pVidWin->put_Owner((OAHWND)hwnd);
```



**Festlegen neuer Fensterstile**

Ändern Sie den Stil des Videofensters, indem Sie die [**IVideoWindow::p ut \_ WindowStyle-Methode**](/windows/desktop/api/Control/nf-control-ivideowindow-put_windowstyle) aufrufen:


```C++
pVidWin->put_WindowStyle(WS_CHILD | WS_CLIPSIBLINGS);
```



Das WS \_ CHILD-Flag legt das Fenster als untergeordnetes Fenster fest, und das WS \_ CLIPSIBLINGS-Flag verhindert, dass das Fenster im Clientbereich eines anderen untergeordneten Fensters gezeichnet wird.

**Positionieren des Videofensters**

Um die Position des Videos relativ zum Clientbereich des Anwendungsfensters festzulegen, rufen Sie die [**IVideoWindow::SetWindowPosition-Methode**](/windows/desktop/api/Control/nf-control-ivideowindow-setwindowposition) auf. Diese Methode verwendet ein Rechteck, das den linken Rand, den oberen Rand, die Breite und die Höhe des Videofensters angibt. Mit dem folgenden Code wird beispielsweise das Videofenster so gestreckt, dass es dem gesamten Clientbereich des übergeordneten Fensters entspricht:


```C++
RECT rc;
GetClientRect(hwnd, &rc);
pVidWin->SetWindowPosition(0, 0, rc.right, rc.bottom);
```



Um die native Größe des Videos abzurufen, rufen Sie die [**IBasicVideo::GetVideoSize-Methode**](/windows/desktop/api/Control/nf-control-ibasicvideo-getvideosize) im Filter Graph Manager auf. Sie können diese Informationen verwenden, um das Video zu skalieren und das richtige Seitenverhältnis beizubehalten.

**Reagieren auf WM \_ MOVE-Nachrichten**

Um eine optimale Leistung zu erzielen, sollten Sie den Videorenderer benachrichtigen, wenn sich das Fenster bewegt, während das Diagramm angehalten wird. Rufen Sie die [**IVideoWindow::NotifyOwnerMessage-Methode**](/windows/desktop/api/Control/nf-control-ivideowindow-notifyownermessage) auf, um die WM \_ MOVE-Nachricht weiterzuleiten:


```C++
// (Inside your WindowProc)
case WM_MOVE:
    pVidWin->NotifyOwnerMessage((OAHWND)hWnd, msg, wParam, lParam);
    break;
```



Wenn der Renderer eine Hardwareüberlagerung verwendet, bewirkt diese Benachrichtigung, dass der Renderer die Überlagerungsposition aktualisiert. (Die VMR-9 verwendet keine Überlagerungen, daher müssen Sie diese Methode nicht aufrufen, wenn Sie VMR-9 verwenden.)

**Bereinigen**

Bevor die Anwendung beendet wird, beenden Sie das Diagramm, und setzen Sie den Besitzer des Videofensters auf **NULL** zurück. Andernfalls können Fenstermeldungen an das falsche Fenster gesendet werden, was wahrscheinlich Fehler verursacht. Blenden Sie auch das Videofenster aus, oder sie sehen, dass ein Videobild kurzzeitig auf dem Bildschirm flackert:


```C++
pControl->Stop(); 
pVidWin->put_Visible(OAFALSE);
pVidWin->put_Owner(NULL);  
```



> [!Note]  
> Wenn das übergeordnete Element des Videofensters ein untergeordnetes Element Ihres Hauptanwendungsfensters ist (d. h. wenn das Videofenster ein untergeordnetes Element eines untergeordneten Elements ist), sollten Sie das Videofenster mit **CoCreateInstance** erstellen und dem Diagramm hinzufügen, anstatt dem Filter Graph Manager den Videorenderer während intelligent [Verbinden](intelligent-connect.md)hinzufügen zu lassen. Dadurch wird sichergestellt, dass das Videofenster und ihr untergeordnetes Fenster gleichzeitig neu maliert werden. Andernfalls kann das untergeordnete Fenster das Videofenster übermalen.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Videorendering](video-rendering.md)
</dt> </dl>

 

 



