---
title: WM_CAP_SET_SEQUENCE_SETUP Meldung (VFW. h)
description: Mit der Einstellung für die WM- \_ Cap- \_ Setup Sequenz wird festgelegt, welche \_ \_ Konfigurationsparameter mit der streamingerfassung Sie können diese Nachricht explizit oder mithilfe des capcapturesetsetup-Makros senden.
ms.assetid: ba9adb26-6627-469b-a836-f4f277ddb7c4
keywords:
- WM_CAP_SET_SEQUENCE_SETUP-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- WM_CAP_SET_SEQUENCE_SETUP
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54a2129021f31694d9e601ecd97503e2a5f5c925
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518953"
---
# <a name="wm_cap_set_sequence_setup-message"></a>\_ \_ \_ \_ Setup Nachricht für die WM-Cap-Einrichtung

Mit der Einstellung für die **WM- \_ Cap- \_ \_ \_ Setup Sequenz wird fest** gelegt, welche Konfigurationsparameter mit der streamingerfassung Sie können diese Nachricht explizit oder mithilfe des [**capcapturesetsetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) -Makros senden.


```C++
WM_CAP_SET_SEQUENCE_SETUP 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPCAPTUREPARMS) (psCapParms); 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wsize*
</dt> <dd>

Größe (in Bytes) der Struktur, auf die von **s** verwiesen wird.

</dd> <dt>

<span id="psCapParms"></span><span id="pscapparms"></span><span id="PSCAPPARMS"></span>*pscapparms*
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

 

 





