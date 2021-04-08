---
title: TVM_EDITLABEL Meldung (kommstrg. h)
description: Beginnt die direkte Bearbeitung des Texts des angegebenen Elements und ersetzt den Text des Elements durch ein einzeilige Bearbeitungs Steuerelement, das den Text enthält.
ms.assetid: ae844cbf-fa43-4f91-90cc-688f44bf77a5
keywords:
- Windows-Steuerelemente für TVM_EDITLABEL Meldung
topic_type:
- apiref
api_name:
- TVM_EDITLABEL
- TVM_EDITLABELA
- TVM_EDITLABELW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3608c3f959c45571d9bc085518b763cf505180ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949692"
---
# <a name="tvm_editlabel-message"></a>TVM \_ EditLabel-Meldung

Beginnt die direkte Bearbeitung des Texts des angegebenen Elements und ersetzt den Text des Elements durch ein einzeilige Bearbeitungs Steuerelement, das den Text enthält. Diese Meldung wählt das angegebene Element implizit aus und konzentriert dieses. Sie können diese Nachricht explizit oder mithilfe des [**TreeView \_ EditLabel**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_editlabel) -Makros senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Handle für das zu bearbeitende Element.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt das Handle für das Bearbeitungs Steuerelement zurück, mit dem der Element Text bei erfolgreicher Bearbeitung bearbeitet wird, andernfalls **null** .

## <a name="remarks"></a>Bemerkungen

Diese Meldung sendet einen [TVN \_ beginlabeledit](tvn-beginlabeledit.md) -Benachrichtigungs Code an das übergeordnete Element des Strukturansicht-Steuer Elements.

Wenn der Benutzer die Bearbeitung abschließt oder abbricht, wird das Bearbeitungs Steuerelement zerstört und das Handle ist nicht mehr gültig. Sie können das Bearbeitungs Steuerelement Unterklassen, aber nicht zerstören.

Vor dem Senden dieser Nachricht an das-Steuerelement muss das-Steuerelement den Fokus haben. Der Fokus kann mithilfe der [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) -Funktion festgelegt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **TVM \_ Editlabelw** (Unicode) und **TVM \_ editlabela** (ANSI)<br/>               |



 

