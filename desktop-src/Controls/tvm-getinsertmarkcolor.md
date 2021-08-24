---
title: TVM_GETINSERTMARKCOLOR Nachricht (Commctrl.h)
description: Ruft die Farbe ab, die zum Zeichnen der Einfügemarke für die Strukturansicht verwendet wird. Sie können diese Nachricht explizit oder mithilfe des TreeView \_ GetInsertMarkColor-Makros senden.
ms.assetid: d1fba4bb-1bdb-44e0-8083-b564cdafc055
keywords:
- TVM_GETINSERTMARKCOLOR Windows-Steuerelementen
topic_type:
- apiref
api_name:
- TVM_GETINSERTMARKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38c784f6b3c363d68472270f0f52cb97cea7c13b6eb709d1aba4975d3cd97bca
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119834150"
---
# <a name="tvm_getinsertmarkcolor-message"></a>TVM \_ GETINSERTMARKCOLOR-Nachricht

Ruft die Farbe ab, die zum Zeichnen der Einfügemarke für die Strukturansicht verwendet wird. Sie können diese Nachricht explizit oder mithilfe des [**TreeView \_ GetInsertMarkColor-Makros**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getinsertmarkcolor) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen [**COLORREF-Wert**](/windows/desktop/gdi/colorref) zurück, der die aktuelle Einfügemarkierungsfarbe enthält.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**TVM \_ SETINSERTMARKCOLOR**](tvm-setinsertmarkcolor.md)
</dt> </dl>

 

