---
title: MCIWNDM_PUT_SOURCE-Nachricht (Vfw.h)
description: Die MCIWNDM \_ PUT \_ SOURCE-Nachricht definiert die Koordinaten des Quellrechtecks neu, das zum Zuschneiden der Bilder einer AVI-Datei während der Wiedergabe verwendet wird. Sie können diese Nachricht explizit oder mithilfe des MCIWndPutSource-Makros senden.
ms.assetid: cff95139-0302-4db3-bf2e-559e75257e85
keywords:
- MCIWNDM_PUT_SOURCE nachricht Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_PUT_SOURCE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2c21e11142a1b47a8984712de664151b686cfa3c3cb9bf153dcbc2a23fa459c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807780"
---
# <a name="mciwndm_put_source-message"></a>MCIWNDM \_ PUT \_ SOURCE-Nachricht

Die **MCIWNDM \_ PUT \_ SOURCE-Nachricht** definiert die Koordinaten des Quellrechtecks neu, das zum Zuschneiden der Bilder einer AVI-Datei während der Wiedergabe verwendet wird. Sie können diese Nachricht explizit oder mithilfe des [**MCIWndPutSource-Makros**](/windows/desktop/api/Vfw/nf-vfw-mciwndputsource) senden.


```C++
MCIWNDM_PUT_SOURCE 
wParam = 0; 
lParam = (LPARAM) (LPRECT) prc; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="prc"></span><span id="PRC"></span>*Vr china*
</dt> <dd>

Zeiger auf eine [RECT-Struktur,](/previous-versions//ms536136(v=vs.85)) die die Koordinaten des Quellrechtecks enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn der Fehler erfolgreich war, oder andernfalls ein Fehler.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



 

