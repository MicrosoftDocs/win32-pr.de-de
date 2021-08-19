---
title: TB_CUSTOMIZE (Commctrl.h)
description: Zeigt das Dialogfeld Symbolleiste anpassen an.
ms.assetid: 45249467-d585-4ffd-8bbe-e39739059c40
keywords:
- TB_CUSTOMIZE von Windows-Steuerelementen
topic_type:
- apiref
api_name:
- TB_CUSTOMIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 765c4fe1cba535903ff1e60804ee6d4ec5743f5d3726212f9aca16742a40913b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957929"
---
# <a name="tb_customize-message"></a>TB \_ CUSTOMIZE-Nachricht

Zeigt das Dialogfeld **Symbolleiste anpassen** an.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Muss Null sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Muss Null sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Die Symbolleiste muss die [Benachrichtigungen TBN \_ QUERYINSERT](tbn-queryinsert.md) und [TBN \_ QUERYDELETE](tbn-querydelete.md) verarbeiten, damit **das** Dialogfeld Symbolleiste anpassen angezeigt wird. Wenn die Symbolleiste diese Benachrichtigungen nicht verarbeitet, **hat TB \_ CUSTOMIZE** keine Auswirkungen.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





