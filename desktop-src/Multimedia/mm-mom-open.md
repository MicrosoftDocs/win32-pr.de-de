---
title: MM_MOM_OPEN Meldung (Mmsystem.h)
description: Die MM \_ MOM \_ OPEN-Nachricht wird an ein Fenster gesendet, wenn ein AUSGABEgerät geöffnet wird.
ms.assetid: 1374a07c-02fa-4b43-82df-cbd96302aec5
keywords:
- MM_MOM_OPEN Nachricht Windows Multimedia
topic_type:
- apiref
api_name:
- MM_MOM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 842eaeeb6e18e6623f8c88d8f5c65527db36ee8370c48a4cb26edca55f6d5f5b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065490"
---
# <a name="mm_mom_open-message"></a>MM \_ MOM \_ OPEN-Nachricht

Die **MM \_ MOM \_ OPEN-Nachricht** wird an ein Fenster gesendet, wenn ein AUSGABEgerät geöffnet wird.


```C++
MM_MOM_OPEN 
wParam = (WPARAM) hOutput 
lParam = reserved 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="hOutput"></span><span id="houtput"></span><span id="HOUTPUT"></span>*hOutput*
</dt> <dd>

Handle für das OUTPUT-Ausgabegerät.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Reserviert; nicht verwenden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Mmsystem.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[MELDUNGSMELDUNGEN](midi-messages.md)
</dt> </dl>

 

 





