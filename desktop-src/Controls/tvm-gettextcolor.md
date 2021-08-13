---
title: TVM_GETTEXTCOLOR Meldung (Commctrl.h)
description: Ruft die aktuelle Textfarbe des Steuerelements ab. Sie können diese Nachricht explizit oder mithilfe des TreeView \_ GetTextColor-Makros senden.
ms.assetid: fe1aa2e8-fdf2-48d1-936b-6d6bc8e589f4
keywords:
- TVM_GETTEXTCOLOR Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- TVM_GETTEXTCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65a578753b6f86d2ceaa6a664fe6e6e0ff88475dccfb953ae6c6f652bc2dffbc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118669711"
---
# <a name="tvm_gettextcolor-message"></a>TVM \_ GETTEXTCOLOR-Nachricht

Ruft die aktuelle Textfarbe des Steuerelements ab. Sie können diese Nachricht explizit oder mithilfe des [**TreeView \_ GetTextColor-Makros**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_gettextcolor) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen [**COLORREF-Wert**](/windows/desktop/gdi/colorref) zurück, der die aktuelle Textfarbe darstellt. Wenn dieser Wert -1 ist, verwendet das Steuerelement die Systemfarbe für die Textfarbe.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**TVM \_ SETTEXTCOLOR**](tvm-settextcolor.md)
</dt> </dl>

 

