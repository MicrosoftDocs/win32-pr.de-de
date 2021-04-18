---
title: WM_TOUCH Meldung (Winuser. h)
description: Benachrichtigt das Fenster, wenn ein oder mehrere Berührungspunkte, z. b. ein Finger oder Stift, eine berührungsempfindliche Digitalisierungs Oberfläche berührt.
ms.assetid: 5dee8bab-34fa-4dd9-a65b-35883757ec80
keywords:
- Windows-Fingereingabe für WM_TOUCH Meldung
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
ms.openlocfilehash: 6b6242d43b661240d946d2883237640d1bc92b3f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392051"
---
# <a name="wm_touch-message"></a>WM-Fingereingabe \_ Nachricht

Benachrichtigt das Fenster, wenn ein oder mehrere Berührungspunkte, z. b. ein Finger oder Stift, eine berührungsempfindliche Digitalisierungs Oberfläche berührt.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Das nieder wertige Wort enthält die Anzahl der der Nachricht zugeordneten Berührungspunkte. Das höchst wertige Wort ist für die zukünftige Verwendung reserviert.

</dd> <dt>

*lParam* 
</dt> <dd>

Enthält ein Fingereingabe handle, das in einem Aufrufen von [**GetTouchInputInfo**](/windows/desktop/api/winuser/nf-winuser-gettouchinputinfo) verwendet werden kann, um ausführliche Informationen zu den mit dieser Meldung verknüpften Berührungspunkten abzurufen.

Dieses Handle ist nur innerhalb des aktuellen Prozesses gültig und sollte nicht Prozess übergreifend übermittelt werden, außer als **LPARAM** in einem **SendMessage** -oder **PostMessage** -Befehl.

Wenn die Anwendung dieses Handle nicht mehr benötigt, muss die Anwendung **closetouchinputhandle** aufrufen, um den mit diesem Handle verknüpften Prozess Speicher freizugeben. Wenn dies nicht der Fall ist, kann dies zu einem Anwendungs Arbeitsspeicher-Fehler führen.

Beachten Sie, dass das Berührungs Eingabe Handle in diesem Parameter nicht mehr gültig ist, nachdem die Nachricht an [defwindowproc](/windows/win32/api/winuser/nf-winuser-defwindowproca)übergeben wurde. Mit [defwindowproc](/windows/win32/api/winuser/nf-winuser-defwindowproca) wird dieses Handle geschlossen und ungültig.

Beachten Sie auch, dass das Fingereingabe Handle in diesem Parameter nicht mehr gültig ist, nachdem die Nachricht mithilfe von [**Post Message**](sendmessage--postmessage--and-related-functions.md), **SendMessage** oder einer ihrer Varianten weitergeleitet wurde. Diese Funktionen werden dieses Handle schließen und für ungültig erklären.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.

Wenn die Anwendung die Nachricht nicht verarbeitet, muss Sie [defwindowproc](/windows/win32/api/winuser/nf-winuser-defwindowproca)aufgerufen werden. Wenn Sie dies nicht tun, wird der Arbeitsspeicher nicht durch die Anwendung getrennt, da der Fingereingabe Handle nicht geschlossen und zugeordneter Prozess Speicher nicht freigegeben wird.

## <a name="remarks"></a>Bemerkungen

**WM \_** Die Fingereingabe-Nachrichten berücksichtigen keine " **httransparent** "-Fensterbereiche. Wenn ein Fenster als Antwort auf eine **WM- \_ nchittest** -Nachricht " **httransparent** " zurückgibt, werden die Maus Meldungen an das übergeordnete Element gesendet, und **WM \_** -Finger Eingaben werden direkt an das Fenster gesendet.

## <a name="examples"></a>Beispiele

Der folgende Code ist ein Beispiel für das Abrufen detaillierter Fingereingabe Informationen, die dieser Nachricht zugeordnet sind.


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
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                                                  |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Meldungen](messages.md)
</dt> <dt>

[Programmier Handbuch zu Manipulationen und Trägheit](manipulation-and-inertia.md)
</dt> <dt>

[Leitfaden zur Eingabe der Windows-Eingabe Eingabe](guide-multi-touch-input.md)
</dt> </dl>

 

