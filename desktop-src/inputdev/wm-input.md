---
title: WM_INPUT (Winuser.h)
description: Wird an das Fenster gesendet, in dem rohe Eingaben angezeigt werden. Ein Fenster empfängt diese Nachricht über seine WindowProc-Funktion.
ms.assetid: a014d68c-841c-4120-b752-4b3fac60e12d
keywords:
- WM_INPUT der Tastatur- und Mauseingabe
topic_type:
- apiref
api_name:
- WM_INPUT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 04/17/2020
ms.openlocfilehash: 5d317ba21c69b22ae9c6b7cb5be0be84cd15f561b34ec65f1f99e7335cd1badb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117884287"
---
# <a name="wm_input-message"></a>WM \_ INPUT-Meldung

Wird an das Fenster gesendet, in dem rohe Eingaben angezeigt werden.

Ein Fenster empfängt diese Nachricht über seine [**WindowProc-Funktion.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```cpp
#define WM_INPUT 0x00FF
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam*

</dt> <dd>

Der Eingabecode. Verwenden [**Sie das \_ \_ \_ WPARAM-Makro GET RAWINPUT CODE,**](/windows/win32/api/winuser/nf-winuser-get_rawinput_code_wparam) um den Wert zu erhalten.

Es kann sich um einen der folgenden Werte handeln:

| Wert | Bedeutung |
|---|---|
| <span id="RIM_INPUT"></span><span id="rim_input"></span><dl> <dt>**BESEN \_ EINGABE**</dt> <dt>0</dt> </dl> | Die Eingabe ist aufgetreten, während sich die Anwendung im Vordergrund befindet. </br> Die Anwendung muss [**DefWindowProc aufrufen,**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) damit das System eine Bereinigung durchführen kann. |
| <span id="RIM_INPUTSINK"></span><span id="rim_inputsink"></span><dl> <dt>**BESEN \_ INPUTSINK**</dt> <dt>1</dt> </dl> | Die Eingabe ist aufgetreten, während sich die Anwendung nicht im Vordergrund befindet. |

</dd> <dt>

*lParam* 

</dt> <dd>

Ein **HRAWINPUT-Handle** für die [**RAWINPUT-Struktur,**](/windows/win32/api/winuser/ns-winuser-rawinput) die die rohe Eingabe des Geräts enthält. Verwenden Sie dieses Handle im Aufruf von [**GetRawInputData,**](/windows/win32/api/winuser/nf-winuser-getrawinputdata)um die Rohdaten zu erhalten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, sollte sie 0 (null) zurückgeben.

## <a name="remarks"></a>Hinweise

Unformatierte Eingaben sind nur verfügbar, wenn die Anwendung [**RegisterRawInputDevices mit gültigen**](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices) Gerätespezifikationen aufruft.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|--------------------------|-------------------------------------------|
| Unterstützte Mindestversion (Client) | Windows Nur \[ XP-Desktop-Apps\] |
| Unterstützte Mindestversion (Server) | Windows Nur Server \[ 2003-Desktop-Apps\] |
| Header | <dl> <dt>**Winuser.h (include Windows.h)**</dt> </dl> |

## <a name="see-also"></a>Weitere Informationen

**Referenz**

[**GetRawInputData**](/windows/win32/api/winuser/nf-winuser-getrawinputdata)

[**RegisterRawInputDevices**](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices)

[**RAWINPUT**](/windows/win32/api/winuser/ns-winuser-rawinput)

[**GET \_ RAWINPUT \_ CODE \_ WPARAM**](/windows/win32/api/winuser/nf-winuser-get_rawinput_code_wparam)

**Konzeptionellen**

[Rohdateneingabe](raw-input.md)
