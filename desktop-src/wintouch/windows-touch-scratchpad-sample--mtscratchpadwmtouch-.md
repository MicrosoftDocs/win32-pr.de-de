---
title: Windows touchscratchpad-Beispiel (C++)
description: Das Windows touchscratchpad-Beispiel zeigt, wie Sie Windows-touchnachrichten verwenden, um Ablauf Verfolgungen der Touchpoints zu einem Fenster zu zeichnen.
ms.assetid: 6c4b4595-1e95-499c-b045-b5ae01aa5a6e
keywords:
- Windows-Fingereingabe, Codebeispiele
- Windows-Fingereingabe, Beispielcode
- Windows Toucheingabe, Scratchpad-Beispiele
- Scratchpad-Beispiele
ms.topic: article
ms.date: 02/18/2020
ms.openlocfilehash: afdd39e886d97671942b4ff67a74c0da75924fbb
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2020
ms.locfileid: "104039808"
---
# <a name="windows-touch-scratchpad-sample-c"></a>Windows touchscratchpad-Beispiel (C++)

Das [Windows touchscratchpad-Beispiel](https://github.com/MicrosoftDocs/win32-pr/blob/master/desktop-src/wintouch/windows-touch-scratchpad-sample--mtscratchpadwmtouch-.md) zeigt, wie Sie Windows-touchnachrichten verwenden, um Ablauf Verfolgungen der Touchpoints zu einem Fenster zu zeichnen. Die Ablauf Verfolgung des primären Fingers, die zuerst auf dem Digitalisierer abgelegt wurde, wird schwarz gezeichnet. Sekundäre Finger werden in sechs anderen Farben gezeichnet: rot, grün, blau, Cyan, Magenta und gelb. Die folgende Abbildung zeigt, wie die Anwendung während der Ausführung aussehen könnte.

![Screenshot mit dem Windows-touchscratchpad mit roten und schwarzen Wellenlinien auf dem Bildschirm](images/mtscratchpadwmtouch.png)

Für diese Anwendung wird das Fenster als touchfenster registriert, touchnachrichten werden zum Hinzufügen von touchpunkten zu Stroke-Objekten interpretiert, und Hand Striche werden auf dem Bildschirm im **WM_PAINT** Meldungs Handler gerendert.

Der folgende Code zeigt, wie das Fenster als Berührungs Fenster registriert wird.

```C++
    // Register application window for receiving multitouch input. Use default settings.
    if(!RegisterTouchWindow(hWnd, 0))
    {
        MessageBox(hWnd, L"Cannot register application window for multitouch input", L"Error", MB_OK);
        return FALSE;
    }
```

Der folgende Code zeigt, wie Finger Eingaben zum Hinzufügen von Berührungspunkten zu Hand Strichen verwendet werden.

```C++
        // WM_TOUCH message handlers
        case WM_TOUCH:
            {
                // WM_TOUCH message can contain several messages from different contacts
                // packed together.
                // Message parameters need to be decoded:
                unsigned int numInputs = (unsigned int) wParam; // Number of actual per-contact messages
                TOUCHINPUT* ti = new TOUCHINPUT[numInputs]; // Allocate the storage for the parameters of the per-contact messages
                if(ti == NULL)
                {
                    break;
                }
                // Unpack message parameters into the array of TOUCHINPUT structures, each
                // representing a message for one single contact.
                if(GetTouchInputInfo((HTOUCHINPUT)lParam, numInputs, ti, sizeof(TOUCHINPUT)))
                {
                    // For each contact, dispatch the message to the appropriate message
                    // handler.
                    for(unsigned int i=0; i<numInputs; ++i)
                    {
                        if(ti[i].dwFlags & TOUCHEVENTF_DOWN)
                        {
                            OnTouchDownHandler(hWnd, ti[i]);
                        }
                        else if(ti[i].dwFlags & TOUCHEVENTF_MOVE)
                        {
                            OnTouchMoveHandler(hWnd, ti[i]);
                        }
                        else if(ti[i].dwFlags & TOUCHEVENTF_UP)
                        {
                            OnTouchUpHandler(hWnd, ti[i]);
                        }
                    }
                }
                CloseTouchInputHandle((HTOUCHINPUT)lParam);
                delete [] ti;
            }
            break;
```

Der folgende Code zeigt, wie die Handschlag Striche im **WM_PAINT** Meldungs Handler auf dem Bildschirm gezeichnet werden.

```C++
        case WM_PAINT:
            hdc = BeginPaint(hWnd, &ps);
            // Full redraw: draw complete collection of finished strokes and
            // also all the strokes that are currently in drawing.
            g_StrkColFinished.Draw(hdc);
            g_StrkColDrawing.Draw(hdc);
            EndPaint(hWnd, &ps);
            break;
```

Der folgende Code zeigt, wie das Stroke-Objekt auf dem Bildschirm Striche rendert.

```C++
void CStroke::Draw(HDC hDC) const
{
    if(m_nCount < 2)
    {
        return;
    }

    HPEN hPen = CreatePen(PS_SOLID, 3, m_clr);
    HGDIOBJ hOldPen = SelectObject(hDC, hPen);
    Polyline(hDC, m_arrData, m_nCount);
    SelectObject(hDC, hOldPen);
    DeleteObject(hPen);
}
```

## <a name="related-topics"></a>Zugehörige Themen

[Windows Touch Scratchpad-Beispiel (c#)](windows-touch-scratchpad-sample-in-c---mtscratchpadwmtouchcs-.md), [Multitouch Scratchpad-Anwendung (WM_TOUCH/c #)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadWMTouch/CS), [Multitouch Scratchpad-Anwendung (WM_TOUCH/c + +)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadWMTouch/cpp), [Windows Touch-Beispiele](windows-touch-samples.md)
