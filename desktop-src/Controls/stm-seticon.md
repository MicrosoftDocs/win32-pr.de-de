---
title: STM_SETICON Meldung (Winuser.h)
description: Eine Anwendung sendet die STM \_ SETICON-Nachricht, um ein Symbol einem Symbolsteuerelement zuzuordnen.
ms.assetid: 105b0667-8e23-47ed-9fb1-0792a22d7100
keywords:
- STM_SETICON Windows-Steuerelementen
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
ms.openlocfilehash: 55ff1cbaa6a1083751b3619392fbb0d3b60695e829907c2dfe27fdb41170e167
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119281420"
---
# <a name="stm_seticon-message"></a>STM \_ SETICON-Meldung

Eine Anwendung sendet die **STM \_ SETICON-Nachricht,** um ein Symbol einem Symbolsteuerelement zuzuordnen.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Handle für das Symbol, das dem Symbolsteuerelement zugeordnet werden soll.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist ein Handle für das Symbol, das zuvor dem Symbolsteuerelement zugeordnet war, oder 0 (null), wenn ein Fehler auftritt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Referenz**
</dt> <dt>

[**STM \_ GETICON**](stm-geticon.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**LoadIcon**](/windows/desktop/api/winuser/nf-winuser-loadicona)
</dt> </dl>

 

