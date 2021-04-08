---
title: MCIWNDM_PUT_SOURCE Meldung (VFW. h)
description: Die mciwndm \_ Put- \_ Quell Nachricht definiert die Koordinaten des Quell Rechtecks neu, das zum Zuschneiden der Bilder einer AVI-Datei während der Wiedergabe verwendet wird. Sie können diese Nachricht explizit oder mithilfe des mciwndputsource-Makros senden.
ms.assetid: cff95139-0302-4db3-bf2e-559e75257e85
keywords:
- MCIWNDM_PUT_SOURCE-Nachricht (Multimedia)
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
ms.openlocfilehash: 5407f420b8def6dda9795e87eb68943c9373b143
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739816"
---
# <a name="mciwndm_put_source-message"></a>Mciwndm \_ Put- \_ Quell Nachricht

Die **mciwndm \_ Put- \_ Quell** Nachricht definiert die Koordinaten des Quell Rechtecks neu, das zum Zuschneiden der Bilder einer AVI-Datei während der Wiedergabe verwendet wird. Sie können diese Nachricht explizit oder mithilfe des [**mciwndputsource**](/windows/desktop/api/Vfw/nf-vfw-mciwndputsource) -Makros senden.


```C++
MCIWNDM_PUT_SOURCE 
wParam = 0; 
lParam = (LPARAM) (LPRECT) prc; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="prc"></span><span id="PRC"></span>*PRC*
</dt> <dd>

Ein Zeiger auf eine [Rect](/previous-versions//ms536136(v=vs.85)) -Struktur, die die Koordinaten des Quell Rechtecks enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



 

