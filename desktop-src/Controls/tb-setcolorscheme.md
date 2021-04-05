---
title: TB_SETCOLORSCHEME Meldung (kommstrg. h)
description: Legt die Farbschema Informationen für das Symbolleisten-Steuerelement fest.
ms.assetid: 96cf6464-b760-46af-910f-984e41dbfca5
keywords:
- Windows-Steuerelemente für TB_SETCOLORSCHEME Meldung
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
ms.openlocfilehash: 0b4ed278ea31dfa156dcc8a64afdb98a2ae3b938
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859240"
---
# <a name="tb_setcolorscheme-message"></a>TB \_ SetColorScheme-Meldung

Legt die Farbschema Informationen für das Symbolleisten-Steuerelement fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**ColorScheme**](/windows/win32/api/commctrl/ns-commctrl-colorscheme) -Struktur, die die Farbschema Informationen enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert für diese Nachricht wird nicht verwendet.

## <a name="remarks"></a>Bemerkungen

Das Symbolleisten-Steuerelement verwendet beim Zeichnen der 3D-Elemente im-Steuerelement die Farbschema Informationen.

Wenn visuelle Stile aktiviert sind, hat diese Nachricht keine Auswirkung.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**TB \_ getcolorscheme**](tb-getcolorscheme.md)
</dt> </dl>

 

 





