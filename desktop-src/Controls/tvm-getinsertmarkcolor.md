---
title: TVM_GETINSERTMARKCOLOR Meldung (kommstrg. h)
description: Ruft die Farbe ab, die verwendet wird, um die Einfügemarke für die Strukturansicht zu zeichnen. Sie können diese Nachricht explizit oder mithilfe des TreeView \_ getinsertmarkcolor-Makros senden.
ms.assetid: d1fba4bb-1bdb-44e0-8083-b564cdafc055
keywords:
- Windows-Steuerelemente für TVM_GETINSERTMARKCOLOR Meldung
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
ms.openlocfilehash: 61416a428fed88ece8f50ca640dd9a05ec131614
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957095"
---
# <a name="tvm_getinsertmarkcolor-message"></a>TVM \_ getinsertmarkcolor-Meldung

Ruft die Farbe ab, die verwendet wird, um die Einfügemarke für die Strukturansicht zu zeichnen. Sie können diese Nachricht explizit oder mithilfe des [**TreeView \_ getinsertmarkcolor**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getinsertmarkcolor) -Makros senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen [**COLORREF**](/windows/desktop/gdi/colorref) -Wert zurück, der die Farbe der aktuellen Einfügemarke enthält.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**TVM-Wert für "". \_**](tvm-setinsertmarkcolor.md)
</dt> </dl>

 

