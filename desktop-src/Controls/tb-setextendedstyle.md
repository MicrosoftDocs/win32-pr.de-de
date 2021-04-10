---
title: TB_SETEXTENDEDSTYLE Meldung (kommstrg. h)
description: Legt die erweiterten Stile für ein Symbolleisten-Steuerelement fest.
ms.assetid: aec64bc7-74b4-4efc-9864-2c8a9fbd35c2
keywords:
- Windows-Steuerelemente für TB_SETEXTENDEDSTYLE Meldung
topic_type:
- apiref
api_name:
- TB_SETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9a540aaeff61bd81b649f0509e064a29282f598
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105039"
---
# <a name="tb_setextendedstyle-message"></a>TB- \_ /textendedstyle-Nachricht

Legt die erweiterten Stile für ein Symbolleisten-Steuerelement fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Ein-Wert, der die neuen erweiterten Stile angibt. Dieser Parameter kann eine Kombination aus [erweiterten Stilen](toolbar-extended-styles.md)sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt ein **DWORD** zurück, das die vorherigen erweiterten Stile darstellt. Bei diesem Wert kann es sich um eine Kombination [erweiterter Stile](toolbar-extended-styles.md)handeln.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**TB \_ getextendecodstyle**](tb-getextendedstyle.md)
</dt> </dl>

 

 





