---
title: LVM_REDRAWITEMS Meldung (kommstrg. h)
description: Erzwingt, dass ein Listenansicht-Steuerelement einen Bereich von Elementen neu zeichnet. Sie können diese Nachricht explizit oder mithilfe des ListView \_ RedrawItems-Makros senden.
ms.assetid: a717b17f-6e0a-4804-96f9-da93392a19ec
keywords:
- Windows-Steuerelemente für LVM_REDRAWITEMS Meldung
topic_type:
- apiref
api_name:
- LVM_REDRAWITEMS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42568a9ab78361a28a99eee372674287a24d03cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040589"
---
# <a name="lvm_redrawitems-message"></a>LVM \_ RedrawItems-Nachricht

Erzwingt, dass ein Listenansicht-Steuerelement einen Bereich von Elementen neu zeichnet. Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ RedrawItems**](/windows/desktop/api/Commctrl/nf-commctrl-listview_redrawitems) -Makros senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Index des ersten Elements, das neu gezeichnet werden soll.

</dd> <dt>

*lParam* 
</dt> <dd>

Der Index des letzten Elements, das neu gezeichnet werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

## <a name="remarks"></a>Bemerkungen

Die angegebenen Elemente werden erst neu gezeichnet, wenn das Listen Ansichts Fenster eine WM-Zeichnungs Nachricht erhält, um Sie neu zu zeichnen. [**\_**](/windows/desktop/gdi/wm-paint) Um sofort neu zu zeichnen, müssen Sie die Funktion [**UpdateWindow**](/windows/desktop/api/winuser/nf-winuser-updatewindow) aufrufen, nachdem Sie dieses Makro verwendet haben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

