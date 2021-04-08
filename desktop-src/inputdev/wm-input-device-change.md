---
title: WM_INPUT_DEVICE_CHANGE Meldung (Winuser. h)
description: Wird an das Fenster gesendet, das für den Empfang von roheingaben registriert ist. Ein Fenster empfängt diese Meldung über seine WindowProc-Funktion.
ms.assetid: 2f98d8ea-b47b-4dea-9c38-f9697b18053a
keywords:
- Tastatur-und Maus Eingaben für WM_INPUT_DEVICE_CHANGE Nachricht
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
ms.openlocfilehash: 0edb6dbfbcfa9e024ba85613e3b7671e5f416397
ms.sourcegitcommit: 47d1f3859035a69340571bf50c3d36e0abeb2126
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "104039783"
---
# <a name="wm_input_device_change-message"></a>WM_INPUT_DEVICE_CHANGE Meldung

## <a name="description"></a>BESCHREIBUNG

Wird an das Fenster gesendet, das für den Empfang von roheingaben registriert ist. 

Unformatierte Eingabe Benachrichtigungen sind erst verfügbar, nachdem die Anwendung [registerrawinputdevices](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices) mit [RIDEV_DEVNOTIFY](/windows/win32/api/winuser/ns-winuser-rawinputdevice) -Flag aufgerufen hat.

Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.

```C++
#define WM_INPUT_DEVICE_CHANGE          0x00FE
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam*

</dt> <dd>

Typ: **wParam**

Dieser Parameter kann einen der folgenden Werte annehmen.

| Wert                    | Bedeutung                                    |
|--------------------------|--------------------------------------------|
| **gidc- \_ Ankunft** </br>1 | Dem System wurde ein neues Gerät hinzugefügt. </br> Sie können " [getrawinputdeviceinfo](/windows/win32/api/winuser/nf-winuser-getrawinputdeviceinfoa) " anrufen, um weitere Informationen zum Gerät zu erhalten. |
| **Entfernen von gidc \_** </br>2 | Ein Gerät wurde aus dem System entfernt. |

</dd> <dt>

*lParam* 

</dt> <dd>

Typ: **LPARAM**

Das **handle** für das unformatierte Eingabegerät.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.

## <a name="see-also"></a>Siehe auch

**Licher**

[Rohdaten Eingabe](/windows/desktop/inputdev/raw-input)

**Verweis**

[Registerrawinputdevices](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices)

[RAWINPUTDEVICE-Struktur](/windows/win32/api/winuser/ns-winuser-rawinputdevice)
 

