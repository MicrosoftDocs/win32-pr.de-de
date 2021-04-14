---
title: WM_INPUT Meldung (Winuser. h)
description: Wird an das Fenster gesendet, das roheingaben erhält. Ein Fenster empfängt diese Meldung über seine WindowProc-Funktion.
ms.assetid: a014d68c-841c-4120-b752-4b3fac60e12d
keywords:
- Tastatur-und Maus Eingaben für WM_INPUT Nachricht
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
ms.openlocfilehash: ffe64a5ca79bbe886ddae31661c06dae695259a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391793"
---
# <a name="wm_input-message"></a>WM- \_ Eingabe Meldung

Wird an das Fenster gesendet, das roheingaben erhält.

Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.


```cpp
#define WM_INPUT 0x00FF
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam*

</dt> <dd>

Der Eingabecode. Verwenden Sie das Makro [**get \_ rawinput \_ Code \_ wParam**](/windows/win32/api/winuser/nf-winuser-get_rawinput_code_wparam) , um den Wert zu erhalten.

Folgenden Werte sind möglich:

| Wert | Bedeutung |
|---|---|
| <span id="RIM_INPUT"></span><span id="rim_input"></span><dl> <dt>**Rand \_ Eingabe**</dt> <dt>0</dt> </dl> | Die Eingabe ist aufgetreten, während sich die Anwendung im Vordergrund befand. </br> Die Anwendung muss [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) aufzurufen, damit das System eine Bereinigung durchführen kann. |
| <span id="RIM_INPUTSINK"></span><span id="rim_inputsink"></span><dl> <dt>**Rand \_ Inputsink**</dt> <dt>1</dt> </dl> | Die Eingabe ist aufgetreten, während sich die Anwendung nicht im Vordergrund befand. |

</dd> <dt>

*lParam* 

</dt> <dd>

Ein **hrawinput** -Handle für die [**rawinput**](/windows/win32/api/winuser/ns-winuser-rawinput) -Struktur, die die unformatierte Eingabe des Geräts enthält. Verwenden Sie zum Abrufen der Rohdaten dieses Handle im-Befehl von " [**getrawinputdata**](/windows/win32/api/winuser/nf-winuser-getrawinputdata)".

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.

## <a name="remarks"></a>Bemerkungen

Unformatierte Eingaben sind nur verfügbar, wenn die Anwendung [**registerrawinputdevices**](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices) mit gültigen Gerätespezifikationen aufruft.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|--------------------------|-------------------------------------------|
| Unterstützte Mindestversion (Client) | Nur Windows XP \[ -Desktop-Apps\] |
| Unterstützte Mindestversion (Server) | Nur Windows Server 2003 \[ -Desktop-Apps\] |
| Header | <dl> <dt>**Winuser. h (Windows. h einschließen)**</dt> </dl> |

## <a name="see-also"></a>Siehe auch

**Verweis**

[**Getrawinputdata**](/windows/win32/api/winuser/nf-winuser-getrawinputdata)

[**Registerrawinputdevices**](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices)

[**Rawinput**](/windows/win32/api/winuser/ns-winuser-rawinput)

[**GET \_ rawinput \_ Code \_ wParam**](/windows/win32/api/winuser/nf-winuser-get_rawinput_code_wparam)

**Licher**

[Rohdaten Eingabe](raw-input.md)
