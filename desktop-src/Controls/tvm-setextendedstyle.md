---
title: TVM_SETEXTENDEDSTYLE Meldung (kommstrg. h)
description: Teilt dem Strukturansicht-Steuerelement mit, dass erweiterte Stile festgelegt werden. Senden Sie diese Nachricht, oder verwenden Sie das Makro TreeView-Element "- \_ textendedstyle".
ms.assetid: 35cb6ac8-1c1e-4ecd-88b2-878d3f6ccaa5
keywords:
- Windows-Steuerelemente für TVM_SETEXTENDEDSTYLE Meldung
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
ms.openlocfilehash: 9c450f72f85e40514c35f08284428feec4f7caf9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517957"
---
# <a name="tvm_setextendedstyle-message"></a>TVM- \_ Meldung "abtextendedstyle"

Teilt dem Strukturansicht-Steuerelement mit, dass erweiterte Stile festgelegt werden. Senden Sie diese Nachricht, oder verwenden Sie das Makro TreeView-Element "- [**\_ textendedstyle**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setextendedstyle)".

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Maske, die verwendet wird, um die festzulegenden Stile auszuwählen.

</dd> <dt>

*lParam* 
</dt> <dd>

Der-Wert, der den erweiterten Stil angibt. Weitere Informationen zu Stilen finden Sie Unterstruktur [Ansicht-Steuerelement erweiterte Stile](tree-view-control-window-extended-styles.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Nachricht erfolgreich ist, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Die erweiterten Stile für ein Strukturansicht-Steuerelement haben nichts mit den erweiterten Stilen zu tun, die mit der Funktion " [**kreatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) " oder der Funktion " [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)" verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

