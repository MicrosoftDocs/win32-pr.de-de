---
title: WM_CAP_GET_SEQUENCE_SETUP (Vfw.h)
description: Die MELDUNG WM \_ CAP GET SEQUENCE SETUP ruft die aktuellen Einstellungen der \_ \_ \_ Streamingerfassungsparameter ab. Sie können diese Nachricht explizit oder mithilfe des Makros capCaptureGetSetup senden.
ms.assetid: 2220c92a-1994-4f15-9730-1cf01972dda6
keywords:
- WM_CAP_GET_SEQUENCE_SETUP von Windows Multimedia
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
ms.openlocfilehash: 55122a98846f23c609eb371ab5698198729c39e967d7953295850b61764459af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118369538"
---
# <a name="wm_cap_get_sequence_setup-message"></a>WM \_ CAP GET SEQUENCE \_ \_ \_ SETUP-Meldung

Die **MELDUNG WM CAP GET SEQUENCE \_ \_ \_ \_ SETUP** ruft die aktuellen Einstellungen der Streamingerfassungsparameter ab. Sie können diese Nachricht explizit oder mithilfe des [**Makros capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) senden.


```C++
WM_CAP_GET_SEQUENCE_SETUP 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPCAPTUREPARMS) (s); 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*
</dt> <dd>

Größe der Struktur in Bytes, auf die von **s verwiesen wird.**

</dd> <dt>

<span id="s"></span><span id="S"></span>*s*
</dt> <dd>

Zeiger auf eine [**CAPTUREPARMS-Struktur.**](/windows/win32/api/vfw/ns-vfw-captureparms)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** wenn erfolgreich, **andernfalls FALSE.**

## <a name="remarks"></a>Hinweise

Informationen zu den Parametern, die zum Steuern der Streamingerfassung verwendet werden, finden Sie in der [**CAPTUREPARMS-Struktur.**](/windows/win32/api/vfw/ns-vfw-captureparms)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Videoaufnahme](video-capture.md)
</dt> <dt>

[Videoaufnahmenachrichten](video-capture-messages.md)
</dt> </dl>

 

 





