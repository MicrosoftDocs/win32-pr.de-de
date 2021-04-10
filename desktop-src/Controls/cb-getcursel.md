---
title: CB_GETCURSEL Meldung (Winuser. h)
description: Eine Anwendung sendet eine CB \_ getcurrsel-Nachricht, um den Index des derzeit ausgewählten Elements (sofern vorhanden) im Listenfeld eines Kombinations Felds abzurufen.
ms.assetid: 47bf87f6-637f-48e9-849e-b2acbe5a6a7b
keywords:
- Windows-Steuerelemente für CB_GETCURSEL Meldung
topic_type:
- apiref
api_name:
- CB_GETCURSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fbc9aa1785738fb061696fbad64598747168269
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859357"
---
# <a name="cb_getcursel-message"></a>CB \_ getcurrsel-Meldung

Eine Anwendung sendet eine **CB \_ getcurrsel** -Nachricht, um den Index des derzeit ausgewählten Elements (sofern vorhanden) im Listenfeld eines Kombinations Felds abzurufen.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Nicht verwendet; muss 0 (null) sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Nicht verwendet; muss 0 (null) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist der null basierte Index des aktuell ausgewählten Elements. Wenn kein Element ausgewählt ist, ist es CB \_ Err.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**CB- \_ SelectString**](cb-selectstring.md)
</dt> <dt>

[**CB \_ setcurrsel**](cb-setcursel.md)
</dt> </dl>

 

 





