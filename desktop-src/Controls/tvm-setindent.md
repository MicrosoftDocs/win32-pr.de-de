---
title: TVM_SETINDENT Meldung (Commctrl.h)
description: Legt die Breite des Einzugs für ein Strukturansicht-Steuerelement fest und zeichnet das Steuerelement neu, um die neue Breite widerzuspiegeln. Sie können diese Nachricht explizit oder mithilfe des TreeView \_ SetIndent-Makros senden.
ms.assetid: 377da8fe-c8e6-479b-a283-f1811cbc3e58
keywords:
- TVM_SETINDENT Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- TVM_SETINDENT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 538a89439909afe346ae8776d31a2104c7f6014664a33bdd3864bf43b0387e80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118669665"
---
# <a name="tvm_setindent-message"></a>TVM \_ SETINDENT-Nachricht

Legt die Breite des Einzugs für ein Strukturansicht-Steuerelement fest und zeichnet das Steuerelement neu, um die neue Breite widerzuspiegeln. Sie können diese Nachricht explizit oder mithilfe des [**TreeView \_ SetIndent-Makros**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setindent) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Breite des Einzugs in Pixel. Wenn dieser Parameter kleiner als die systemdefinierte Mindestbreite ist, wird die neue Breite auf den vom System definierten Mindestwert festgelegt.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

Der systemdefinierte Mindesteinzugswert beträgt in der Regel fünf Pixel, ist aber nicht fixiert. Um den genauen Wert des minimalen Einzugs auf einem bestimmten System abzurufen, senden Sie eine **TVM \_ SETINDENT-Nachricht,** wobei *wParam* auf 0 (null) festgelegt ist. Senden Sie dann eine [**TVM \_ GETINDENT-Nachricht,**](tvm-getindent.md) um den minimalen Einzugswert abzurufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**TreeView \_ SetIndent**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setindent)
</dt> </dl>

 

 





