---
title: TB_SETEXTENDEDSTYLE (Commctrl.h)
description: Legt die erweiterten Stile für ein Symbolleisten-Steuerelement fest.
ms.assetid: aec64bc7-74b4-4efc-9864-2c8a9fbd35c2
keywords:
- TB_SETEXTENDEDSTYLE meldungssteuerelemente Windows
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
ms.openlocfilehash: 600e5904637215eeb052c85ec0203c9b86c75ed6b179be643dc9a213156b3afd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119318880"
---
# <a name="tb_setextendedstyle-message"></a>TB \_ SETEXTENDEDSTYLE-Meldung

Legt die erweiterten Stile für ein Symbolleisten-Steuerelement fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Wert, der die neuen erweiterten Stile an gibt. Dieser Parameter kann eine Kombination aus erweiterten [Stilen sein.](toolbar-extended-styles.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt ein **DWORD zurück,** das die vorherigen erweiterten Stile darstellt. Dieser Wert kann eine Kombination aus erweiterten [Stilen sein.](toolbar-extended-styles.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**TB \_ GETEXTENDEDSTYLE**](tb-getextendedstyle.md)
</dt> </dl>

 

 





