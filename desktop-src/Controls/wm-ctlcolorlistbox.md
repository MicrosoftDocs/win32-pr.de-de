---
title: WM_CTLCOLORLISTBOX Meldung (Winuser. h)
description: Wird an das übergeordnete Fenster eines Listen Felds gesendet, bevor das System das Listenfeld zeichnet. Wenn Sie auf diese Meldung reagieren, kann das übergeordnete Fenster die Text-und Hintergrundfarben des Listen Felds mit dem angegebenen Kontext Handle für den Anzeigegerät festlegen.
ms.assetid: e128e77f-e966-44c4-9f0e-efcf421b6c82
keywords:
- Windows-Steuerelemente für WM_CTLCOLORLISTBOX Meldung
topic_type:
- apiref
api_name:
- WM_CTLCOLORLISTBOX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e949af76bd05aa9ad3a3e720c89be33cfe76ed8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103547"
---
# <a name="wm_ctlcolorlistbox-message"></a>\_Ctlcolorlistbox-Nachricht für WM

Wird an das übergeordnete Fenster eines Listen Felds gesendet, bevor das System das Listenfeld zeichnet. Wenn Sie auf diese Meldung reagieren, kann das übergeordnete Fenster die Text-und Hintergrundfarben des Listen Felds mit dem angegebenen Kontext Handle für den Anzeigegerät festlegen.


```C++
WM_CTLCOLORLISTBOX

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Handle für den Gerätekontext für das Listenfeld.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle für das Listenfeld.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, muss Sie ein Handle für einen Pinsel zurückgeben. Das System verwendet den Pinsel zum Zeichnen des Hintergrunds des Listen Felds.

## <a name="remarks"></a>Bemerkungen

Standardmäßig wählt die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion die Standardsystem Farben für das Listenfeld aus.

Die " **WM \_ ctlcolorlistbox** "-Meldung wird nie zwischen Threads gesendet. Sie wird nur innerhalb eines Threads gesendet.

Wenn eine Dialogfeld Prozedur diese Nachricht behandelt, sollte Sie den gewünschten Rückgabewert in ein **int- \_ ptr** umwandeln und den Wert direkt zurückgeben. Wenn die Dialogfeld Prozedur **false** zurückgibt, wird die standardmäßige Nachrichtenverarbeitung ausgeführt. Der von der [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) -Funktion festgelegte **DWL- \_ msgresult** -Wert wird ignoriert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Andere Ressourcen**
</dt> <dt>

[**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[**SelectPalette**](/windows/desktop/api/wingdi/nf-wingdi-selectpalette)
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> </dl>

 

