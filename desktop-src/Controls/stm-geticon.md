---
title: STM_GETICON Meldung (Winuser.h)
description: Eine Anwendung sendet die STM \_ GETICON-Nachricht, um ein Handle für das Symbol abzurufen, das einem statischen Steuerelement zugeordnet ist, das über das \_ SS-SYMBOLformat verfügt.
ms.assetid: e6b0a006-696b-401d-b894-b1db697c8939
keywords:
- STM_GETICON Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- STM_GETICON
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d33aab01e668f4b77e36a0a62b8eab75f3ee5db82188416c295c04cdf9bcb078
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084950"
---
# <a name="stm_geticon-message"></a>STM \_ GETICON-Nachricht

Eine Anwendung sendet die **STM \_ GETICON-Nachricht,** um ein Handle für das Symbol abzurufen, das einem statischen Steuerelement zugeordnet ist, das über das SS-SYMBOLformat \_ verfügt.

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

Der Rückgabewert ist ein Handle für das Symbol oder **NULL,** wenn dem statischen Steuerelement kein Symbol zugeordnet ist oder ein Fehler aufgetreten ist.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**STM \_ SETICON**](stm-seticon.md)
</dt> </dl>

 

 





