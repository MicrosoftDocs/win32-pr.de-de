---
title: Windows Touch Scratchpad-Beispiel (C++)
description: Das Windows Touch Scratchpad-Beispiel zeigt, wie sie Windows Touch-Nachrichten verwenden, um Ablaufverfolgungen der Berührungspunkte in einem Fenster zu zeichnen.
ms.assetid: 6c4b4595-1e95-499c-b045-b5ae01aa5a6e
keywords:
- Windows Toucheingabe, Codebeispiele
- Windows Toucheingabe, Beispielcode
- Windows Touch,Scratchpad-Beispiele
- Scratchpad-Beispiele
ms.topic: article
ms.date: 02/18/2020
ms.openlocfilehash: 7f3be8c120a935bc1a8d65dfdd8c7ab9894e0360d3415e8c645e5b3afae87012
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119086250"
---
# <a name="windows-touch-scratchpad-sample-c"></a>Windows Touch Scratchpad-Beispiel (C++)

Das [Windows Touch Scratchpad-Beispiel](https://github.com/MicrosoftDocs/win32-pr/blob/master/desktop-src/wintouch/windows-touch-scratchpad-sample--mtscratchpadwmtouch-.md) zeigt, wie sie Windows Touch-Nachrichten verwenden, um Ablaufverfolgungen der Berührungspunkte in einem Fenster zu zeichnen. Die Ablaufverfolgung des primären Fingers, der zuerst auf den Digitizer gesetzt wurde, wird schwarz gezeichnet. Sekundäre Finger werden in sechs anderen Farben gezeichnet: Rot, Grün, Blau, Cyan, Magenta und Gelb. Die folgende Abbildung zeigt, wie die Anwendung aussehen könnte, während sie ausgeführt wird.

![Screenshot des Windows-Touch-Scratchpads mit roten und schwarzenQuiken auf dem Bildschirm](images/mtscratchpadwmtouch.png)

Für diese Anwendung wird das Fenster als Touchfenster registriert, Touchnachrichten werden interpretiert, um Strichobjekten Berührungspunkte hinzuzufügen, und Ink-Striche werden auf dem Bildschirm im **WM_PAINT** Meldungshandler gerendert.

Der folgende Code zeigt, wie das Fenster als Touchfenster registriert wird.

```C++
    // Register application window for receiving multitouch input. Use default settings.
    if(!RegisterTouchWindow(hWnd, 0))
    {
        MessageBox(hWnd, L"Cannot register application window for multitouch input", L"Error", MB_OK);
        return FALSE;
    }
```

Der folgende Code zeigt, wie Touchnachrichten verwendet werden, um Berührungspunkte zu Ink-Strichen hinzuzufügen.

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

Der folgende Code zeigt, wie die Ink-Striche im **WM_PAINT** Meldungshandler auf den Bildschirm gezeichnet werden.

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

Der folgende Code zeigt, wie das Strichobjekt Striche auf dem Bildschirm rendert.

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

[Windows Touch Scratchpad Sample (C#),](windows-touch-scratchpad-sample-in-c---mtscratchpadwmtouchcs-.md) [Multi-touch Scratchpad Application (WM_TOUCH/C#)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadWMTouch/CS), [Multi-touch Scratchpad Application (WM_TOUCH/C++)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadWMTouch/cpp) [, Windows Touch Samples](windows-touch-samples.md)
