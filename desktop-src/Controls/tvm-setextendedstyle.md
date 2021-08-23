---
title: TVM_SETEXTENDEDSTYLE (Commctrl.h)
description: Informiert das Strukturansicht-Steuerelement über das Festlegen erweiterter Stile. Senden Sie diese Nachricht, oder verwenden Sie das Makro TreeView \_ SetExtendedStyle.
ms.assetid: 35cb6ac8-1c1e-4ecd-88b2-878d3f6ccaa5
keywords:
- TVM_SETEXTENDEDSTYLE von Windows-Steuerelementen
topic_type:
- apiref
api_name:
- TVM_SETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d13d99a2f7a27475c30867f007f45d7525118d3077ebdce235c6bd33e1f8aafe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119750960"
---
# <a name="tvm_setextendedstyle-message"></a>TVM \_ SETEXTENDEDSTYLE-Meldung

Informiert das Strukturansicht-Steuerelement über das Festlegen erweiterter Stile. Senden Sie diese Nachricht, oder verwenden Sie das [**Makro TreeView \_ SetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setextendedstyle).

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Maske zum Auswählen der stils, die festgelegt werden sollen.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Wert, der den erweiterten Stil angibt. Weitere Informationen zu Stilen finden Sie unter [Strukturansicht-Steuerelement Erweiterte Stile.](tree-view-control-window-extended-styles.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Meldung erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Die erweiterten Stile für ein Strukturansicht-Steuerelement haben nichts mit den erweiterten Stilen zu tun, die mit der [**CreateWindowEx-Funktion**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) oder der [**Funktion SetWindowLong verwendet werden.**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

