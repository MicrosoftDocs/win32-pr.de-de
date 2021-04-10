---
title: LB_GETCARETINDEX Meldung (Winuser. h)
description: Ruft den Index des Elements ab, das in einem Listenfeld mit Mehrfachauswahl den Fokus hat. Das Element ist möglicherweise nicht ausgewählt.
ms.assetid: vs|controls|~\controls\listboxes\listboxreference\listboxmessages\lb_getcaretindex.htm
keywords:
- Windows-Steuerelemente für LB_GETCARETINDEX Meldung
topic_type:
- apiref
api_name:
- LB_GETCARETINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b9e4b8b2c75d72cdec606942991e957d8109ac7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040954"
---
# <a name="lb_getcaretindex-message"></a>LB- \_ getcaretindex-Meldung

Ruft den Index des Elements ab, das in einem Listenfeld mit Mehrfachauswahl den Fokus hat. Das Element ist möglicherweise nicht ausgewählt.

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

Der Rückgabewert ist der null basierte Index des fokussierten Listenfeld Elements oder 0, wenn kein Element den Fokus besitzt.

## <a name="remarks"></a>Bemerkungen

Diese Meldung kann auch verwendet werden, um den Index des Elements zu erhalten, das derzeit in einem Listenfeld mit einer einzelnen Auswahl ausgewählt ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**LB- \_ setcaretindex**](lb-setcaretindex.md)
</dt> </dl>

 

 





