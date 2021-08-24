---
title: WM_TOUCH (Winuser.h)
description: Benachrichtigt das Fenster, wenn ein oder mehrere Berührungspunkte, z. B. ein Finger oder Stift, eine berührungsempfindliche Digitizeroberfläche berühren.
ms.assetid: 5dee8bab-34fa-4dd9-a65b-35883757ec80
keywords:
- WM_TOUCH-Nachricht Windows Touch
topic_type:
- apiref
api_name:
- WM_TOUCH
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec1034a229dbb1f3895726fcb3c1551e2dd0f390be0fd7bc2eb81d8331e582eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810100"
---
# <a name="wm_touch-message"></a>WM \_ TOUCH-Nachricht

Benachrichtigt das Fenster, wenn ein oder mehrere Berührungspunkte, z. B. ein Finger oder Stift, eine berührungsempfindliche Digitizeroberfläche berühren.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Das Wort in niedriger Reihenfolge enthält die Anzahl von Berührungspunkten, die dieser Nachricht zugeordnet sind. Das obere Wort ist für die zukünftige Verwendung reserviert.

</dd> <dt>

*lParam* 
</dt> <dd>

Enthält ein Toucheingabehand handle, das in einem Aufruf von [**GetTouchInputInfo verwendet werden**](/windows/desktop/api/winuser/nf-winuser-gettouchinputinfo) kann, um ausführliche Informationen zu den Touchpunkten abzurufen, die dieser Nachricht zugeordnet sind.

Dieses Handle ist nur innerhalb des aktuellen Prozesses gültig und sollte nur als **LPARAM** in einem **SendMessage-** oder **PostMessage-Aufruf prozessübergreifend übergeben** werden.

Wenn die Anwendung dieses Handle nicht mehr benötigt, muss die Anwendung **CloseTouchInputHandle** aufrufen, um den diesem Handle zugeordneten Prozessspeicher frei zu geben. Andernicht kann dies zu einem Speicherverlust der Anwendung führen.

Beachten Sie, dass das Toucheingabehand handle in diesem Parameter nicht mehr gültig ist, nachdem die Nachricht an [DefWindowProc übergeben wurde.](/windows/win32/api/winuser/nf-winuser-defwindowproca) [DefWindowProc schließt](/windows/win32/api/winuser/nf-winuser-defwindowproca) dieses Handle und macht es ungültig.

Beachten Sie auch, dass das Toucheingabehand handle in diesem Parameter nicht mehr gültig ist, nachdem die Nachricht mitHilfe von [**PostMessage,**](sendmessage--postmessage--and-related-functions.md) **SendMessage** oder einer ihrer Varianten weitergeleitet wurde. Diese Funktionen schließen dieses Handle und machen es ungültig.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, sollte sie 0 (null) zurückgeben.

Wenn die Anwendung die Nachricht nicht verarbeiten kann, muss sie [DefWindowProc aufrufen.](/windows/win32/api/winuser/nf-winuser-defwindowproca) Wenn dies nicht erfolgt, gibt die Anwendung Arbeitsspeicher frei, da das Toucheingabehand handle nicht geschlossen und der zugeordnete Prozessspeicher nicht frei wird.

## <a name="remarks"></a>Hinweise

**WM \_ TOUCH-Nachrichten** achten nicht **auf HTTRANSPARENT-Fensterregionen.** Wenn ein Fenster **HTTRANSPARENT** als Antwort auf eine **WM \_ NCHITTEST-Nachricht** zurückgibt, werden Mausnachrichten an das übergeordnete Element gesendet, und **WM \_ TOUCH-Nachrichten** werden direkt an das Fenster gesendet.

## <a name="examples"></a>Beispiele

Der folgende Code ist ein Beispiel für das Abrufen detaillierter Toucheingabeinformationen, die dieser Nachricht zugeordnet sind.


```C++
UINT cInputs = LOWORD(wParam);
PTOUCHINPUT pInputs = new TOUCHINPUT[cInputs];
if (NULL != pInputs)
{
    if (GetTouchInputInfo((HTOUCHINPUT)lParam,
                          cInputs,
                          pInputs,
                          sizeof(TOUCHINPUT)))
    {
        // process pInputs
        if (!CloseTouchInputHandle((HTOUCHINPUT)lParam))
        {
            // error handling
        }
    }
    else
    {
        // GetLastError() and error handling
    }
    delete [] pInputs;
}
else
{
    // error handling, presumably out of memory
}
return DefWindowProc(hWnd, message, wParam, lParam);
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                                                  |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Meldungen](messages.md)
</dt> <dt>

[Programmierhandbuch zu Manipulationen und Trägheit](manipulation-and-inertia.md)
</dt> <dt>

[Windows Programmierhandbuch für Toucheingaben](guide-multi-touch-input.md)
</dt> </dl>

 

