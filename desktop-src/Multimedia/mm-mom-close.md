---
title: MM_MOM_CLOSE (Mmsystem.h)
description: Die MM \_ MOM \_ CLOSE-Nachricht wird an ein Fenster gesendet, wenn ein SCHLIEßEN-Ausgabegerät geschlossen wird.
ms.assetid: 4829bbe5-5103-4354-88a7-37def22e926e
keywords:
- MM_MOM_CLOSE von Windows Multimedia
topic_type:
- apiref
api_name:
- MM_MOM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8e8c9af8f6a5fb454a2f7759b5e64804e82c568b15549d01f7478a3d7c6041d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807150"
---
# <a name="mm_mom_close-message"></a>MM \_ MOM \_ CLOSE-Nachricht

Die **MM \_ MOM \_ CLOSE-Nachricht** wird an ein Fenster gesendet, wenn ein SCHLIEßEN-Ausgabegerät geschlossen wird.


```C++
MM_MOM_CLOSE 
wParam = (WPARAM) hOutput 
lParam = reserved 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="hOutput"></span><span id="houtput"></span><span id="HOUTPUT"></span>*hOutput*
</dt> <dd>

Handle für das OUTPUT-Gerät des 2016-Geräts

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Reserviert; nicht verwenden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Das Gerätehandy ist nach dem Senden dieser Nachricht nicht mehr gültig.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Mmsystem.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[MESSAGES-Meldungen](midi-messages.md)
</dt> </dl>

 

 





