---
title: STM_GETICON Meldung (Winuser. h)
description: Eine Anwendung sendet die STM \_ GetIcon-Nachricht, um ein Handle für das Symbol abzurufen, das einem statischen Steuerelement mit dem SS-Symbolstil zugeordnet ist \_ .
ms.assetid: e6b0a006-696b-401d-b894-b1db697c8939
keywords:
- Windows-Steuerelemente für STM_GETICON Meldung
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
ms.openlocfilehash: f64f55d2a2f8315b99526e51a69891f6f0056e8b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103126"
---
# <a name="stm_geticon-message"></a>STM- \_ GetIcon-Nachricht

Eine Anwendung sendet die **STM \_ GetIcon** -Nachricht, um ein Handle für das Symbol abzurufen, das einem statischen Steuerelement mit dem SS-Symbolstil zugeordnet ist \_ .

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

Der Rückgabewert ist ein Handle für das Symbol, oder **null** , wenn entweder das statische Steuerelement kein zugeordnetes Symbol aufweist oder wenn ein Fehler aufgetreten ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**STM \_ -Ziel**](stm-seticon.md)
</dt> </dl>

 

 





