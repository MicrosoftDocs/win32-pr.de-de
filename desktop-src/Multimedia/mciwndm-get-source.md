---
title: MCIWNDM_GET_SOURCE Meldung (Vfw.h)
description: Die MCIWNDM \_ GET \_ SOURCE-Nachricht ruft die Koordinaten des Quellrechtecks ab, das zum Zuschneiden der Bilder einer AVI-Datei während der Wiedergabe verwendet wird. Sie können diese Nachricht explizit oder mithilfe des MCIWndGetSource-Makros senden.
ms.assetid: d5f25926-5a3d-412e-8248-fbf307583757
keywords:
- MCIWNDM_GET_SOURCE nachricht Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_GET_SOURCE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ef8bcbaf0909adeae5345448769c68e726456a4bbf4375f08d874e3502ab6a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119429400"
---
# <a name="mciwndm_get_source-message"></a>MCIWNDM \_ GET \_ SOURCE-Nachricht

Die **MCIWNDM \_ GET \_ SOURCE-Nachricht** ruft die Koordinaten des Quellrechtecks ab, das zum Zuschneiden der Bilder einer AVI-Datei während der Wiedergabe verwendet wird. Sie können diese Nachricht explizit oder mithilfe des [**MCIWndGetSource-Makros**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetsource) senden.


```C++
MCIWNDM_GET_SOURCE 
wParam = 0; 
lParam = (LPARAM) (LPRECT) prc; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="prc"></span><span id="PRC"></span>*Vr china*
</dt> <dd>

Zeiger auf eine [**RECT-Struktur,**](/previous-versions//dd162897(v=vs.85)) die die Koordinaten des Quellrechtecks enthalten soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn der Fehler erfolgreich war, oder andernfalls ein Fehler.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**MCIWndGetSource**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetsource)
</dt> </dl>

 

