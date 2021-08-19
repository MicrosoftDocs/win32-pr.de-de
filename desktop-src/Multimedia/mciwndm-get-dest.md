---
title: MCIWNDM_GET_DEST (Vfw.h)
description: Die MCIWNDM GET DEST-Nachricht ruft die Koordinaten des Zielrechtecks ab, das zum Zoomen oder Strecken der Bilder einer AVI-Datei während der Wiedergabe \_ \_ verwendet wird. Sie können diese Nachricht explizit oder mithilfe des Makros MCIWndGetDest senden.
ms.assetid: d4d8a3eb-aad4-4435-a23b-7a9c55fc194d
keywords:
- MCIWNDM_GET_DEST von Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_GET_DEST
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4a6326485bece572b03ceeca687ca4468b6d866c25c738c32d13763fd0931a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117802904"
---
# <a name="mciwndm_get_dest-message"></a>MCIWNDM \_ GET \_ DEST-Nachricht

Die **MCIWNDM \_ GET \_ DEST-Nachricht** ruft die Koordinaten des Zielrechtecks ab, das zum Zoomen oder Strecken der Bilder einer AVI-Datei während der Wiedergabe verwendet wird. Sie können diese Nachricht explizit oder mithilfe des [**Makros MCIWndGetDest**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdest) senden.


```C++
MCIWNDM_GET_DEST 
wParam = 0; 
lParam = (LPARAM) (LPRECT) prc; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="prc"></span><span id="PRC"></span>*Vr china*
</dt> <dd>

Zeiger auf eine [**RECT-Struktur,**](/previous-versions//dd162897(v=vs.85)) um die Koordinaten des Zielrechtecks zurückgibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls ein Fehler.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MCIWndGetDest**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdest)
</dt> </dl>

 

