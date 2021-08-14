---
title: TB_SETCOLORSCHEME (Commctrl.h)
description: Legt die Farbschemainformationen für das Symbolleisten-Steuerelement fest.
ms.assetid: 96cf6464-b760-46af-910f-984e41dbfca5
keywords:
- TB_SETCOLORSCHEME von Windows Steuerelementen
topic_type:
- apiref
api_name:
- TB_SETCOLORSCHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58c6a07c186fd3f5a521719ba0f75f8e468c3868d8ebfaa0595679d48b45089f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118167500"
---
# <a name="tb_setcolorscheme-message"></a>TB \_ SETCOLORSCHEME-Nachricht

Legt die Farbschemainformationen für das Symbolleisten-Steuerelement fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**COLORSCHEME-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-colorscheme) die die Farbschemainformationen enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert für diese Meldung wird nicht verwendet.

## <a name="remarks"></a>Hinweise

Das Symbolleisten-Steuerelement verwendet die Farbschemainformationen beim Zeichnen der 3D-Elemente im Steuerelement.

Wenn visuelle Stile aktiviert sind, hat diese Meldung keine Auswirkungen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**TB \_ GETCOLORSCHEME**](tb-getcolorscheme.md)
</dt> </dl>

 

 





