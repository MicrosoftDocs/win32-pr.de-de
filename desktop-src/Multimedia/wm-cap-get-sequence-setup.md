---
title: WM_CAP_GET_SEQUENCE_SETUP Meldung (VFW. h)
description: Die "WM \_ Cap \_ Get Sequence"- \_ \_ Setup Nachricht Ruft die aktuellen Einstellungen der streamingerfassungs Parameter ab. Sie können diese Nachricht explizit oder mithilfe des capcapturegetsetup-Makros senden.
ms.assetid: 2220c92a-1994-4f15-9730-1cf01972dda6
keywords:
- WM_CAP_GET_SEQUENCE_SETUP-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- WM_CAP_GET_SEQUENCE_SETUP
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5cd1585b165581f9c9646741b92c5dc841472ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949395"
---
# <a name="wm_cap_get_sequence_setup-message"></a>Meldung zum Einrichten der WM- \_ Cap- \_ \_ Sequenz \_

Die " **WM \_ Cap \_ get \_ Sequence \_** "-Setup Nachricht Ruft die aktuellen Einstellungen der streamingerfassungs Parameter ab. Sie können diese Nachricht explizit oder mithilfe des [**capcapturegetsetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) -Makros senden.


```C++
WM_CAP_GET_SEQUENCE_SETUP 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPCAPTUREPARMS) (s); 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wsize*
</dt> <dd>

Größe (in Bytes) der Struktur, auf die von **s** verwiesen wird.

</dd> <dt>

<span id="s"></span><span id="S"></span>*Hymnen*
</dt> <dd>

Zeiger auf eine [**captureparms**](/windows/win32/api/vfw/ns-vfw-captureparms) -Struktur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

## <a name="remarks"></a>Bemerkungen

Informationen zu den Parametern, die zum Steuern der streamingerfassung verwendet werden, finden Sie in der Struktur von [**captuprojektms**](/windows/win32/api/vfw/ns-vfw-captureparms) .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Video Erfassung](video-capture.md)
</dt> <dt>

[Video Erfassungs Meldungen](video-capture-messages.md)
</dt> </dl>

 

 





