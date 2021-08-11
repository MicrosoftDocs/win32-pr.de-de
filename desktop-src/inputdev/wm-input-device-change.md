---
title: WM_INPUT_DEVICE_CHANGE Meldung (Winuser.h)
description: Wird an das Fenster gesendet, das für den Empfang unformatierten Eingaben registriert wurde. Ein Fenster empfängt diese Meldung über seine WindowProc-Funktion.
ms.assetid: 2f98d8ea-b47b-4dea-9c38-f9697b18053a
keywords:
- WM_INPUT_DEVICE_CHANGE Meldung Tastatur- und Mauseingabe
topic_type:
- apiref
api_name:
- WM_INPUT_DEVICE_CHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 823aeaf5655703802f07fb238d5c6c5dc479defa12ae4a416423b4519fd2b64f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118247886"
---
# <a name="wm_input_device_change-message"></a>WM_INPUT_DEVICE_CHANGE Meldung

## <a name="description"></a>BESCHREIBUNG

Wird an das Fenster gesendet, das für den Empfang unformatierten Eingaben registriert wurde. 

Unformatierte Eingabebenachrichtigungen sind erst verfügbar, nachdem die Anwendung [RegisterRawInputDevices](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices) mit [RIDEV_DEVNOTIFY-Flag](/windows/win32/api/winuser/ns-winuser-rawinputdevice) aufruft.

Ein Fenster empfängt diese Meldung über seine [**WindowProc-Funktion.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))

```C++
#define WM_INPUT_DEVICE_CHANGE          0x00FE
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam*

</dt> <dd>

Typ: **WPARAM**

Dieser Parameter kann einen der folgenden Werte annehmen.

| Wert                    | Bedeutung                                    |
|--------------------------|--------------------------------------------|
| **GIDC \_ ARRIVAL** </br>1 | Dem System wurde ein neues Gerät hinzugefügt. </br> Sie können [GetRawInputDeviceInfo](/windows/win32/api/winuser/nf-winuser-getrawinputdeviceinfoa) aufrufen, um weitere Informationen zum Gerät zu erhalten. |
| **ENTFERNEN VON GIDC \_** </br>2 | Ein Gerät wurde aus dem System entfernt. |

</dd> <dt>

*lParam* 

</dt> <dd>

Typ: **LPARAM**

Das **HANDLE** für das Unformatierte Eingabegerät.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, sollte sie 0 (null) zurückgeben.

## <a name="see-also"></a>Siehe auch

**Konzeptionellen**

[Rohdateneingabe](/windows/desktop/inputdev/raw-input)

**Referenz**

[RegisterRawInputDevices](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices)

[RAWINPUTDEVICE-Struktur](/windows/win32/api/winuser/ns-winuser-rawinputdevice)
 

