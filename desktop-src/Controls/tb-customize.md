---
title: TB_CUSTOMIZE Meldung (kommstrg. h)
description: Zeigt das Dialogfeld Symbolleiste anpassen an.
ms.assetid: 45249467-d585-4ffd-8bbe-e39739059c40
keywords:
- Windows-Steuerelemente für TB_CUSTOMIZE Meldung
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
ms.openlocfilehash: dada0ef195e898b7a46487a2d775e46d6af854ed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345532"
---
# <a name="tb_customize-message"></a>TB anpassbare \_ Nachricht

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

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Die Symbolleiste muss die [TBN \_ queryinsert](tbn-queryinsert.md) -und [TBN \_ querydelete](tbn-querydelete.md) -Benachrichtigungen verarbeiten, damit das Dialogfeld **Symbolleiste anpassen** angezeigt wird. Wenn die Symbolleiste diese Benachrichtigungen nicht verarbeitet, hat die **\_ Anpassung von TB** keine Auswirkungen.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





