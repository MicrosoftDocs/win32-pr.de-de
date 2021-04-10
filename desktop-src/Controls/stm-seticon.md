---
title: STM_SETICON Meldung (Winuser. h)
description: Eine Anwendung sendet die STM \_ SetIcon-Nachricht, um ein Symbol einem Symbol Steuerelement zuzuordnen.
ms.assetid: 105b0667-8e23-47ed-9fb1-0792a22d7100
keywords:
- Windows-Steuerelemente für STM_SETICON Meldung
topic_type:
- apiref
api_name:
- STM_SETICON
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb9c7e2a007c1f866a1c73b3a1c1a55b157add47
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040160"
---
# <a name="stm_seticon-message"></a>STM- \_ Nachricht

Eine Anwendung sendet die **STM \_ SetIcon** -Nachricht, um ein Symbol einem Symbol Steuerelement zuzuordnen.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Handle für das Symbol, das mit dem Symbol Steuerelement verknüpft werden soll.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist ein Handle für das Symbol, das zuvor dem Symbol Steuerelement zugeordnet wurde, oder 0 (null), wenn ein Fehler auftritt.

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

[**STM- \_ getIcon**](stm-geticon.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**LoadIcon**](/windows/desktop/api/winuser/nf-winuser-loadicona)
</dt> </dl>

 

