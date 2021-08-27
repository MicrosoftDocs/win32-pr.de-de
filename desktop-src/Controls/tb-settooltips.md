---
title: TB_SETTOOLTIPS (Commctrl.h)
description: Ordnet einer Symbolleiste ein QuickInfo-Steuerelement zu.
ms.assetid: a645f1f2-9333-4e25-985a-107cffb9b97f
keywords:
- TB_SETTOOLTIPS von Windows-Steuerelementen
topic_type:
- apiref
api_name:
- TB_SETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a75827df49eeaf8b6175cd14180ebb26ddbb642588ee77d625c701eee457baaf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061230"
---
# <a name="tb_settooltips-message"></a>TB \_ SETTOOLTIPS-Nachricht

Ordnet einer Symbolleiste ein QuickInfo-Steuerelement zu.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Handle für das QuickInfo-Steuerelement.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

Schaltflächen, die vor dem Senden der **\_ TB-SETTOOLTIPS-Nachricht** zu einer Symbolleiste hinzugefügt werden, werden nicht beim QuickInfo-Steuerelement registriert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





