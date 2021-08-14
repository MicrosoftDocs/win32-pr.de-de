---
title: TVM_EDITLABEL Nachricht (Commctrl.h)
description: Beginnt die direkte Bearbeitung des Texts des angegebenen Elements und ersetzt den Text des Elements durch ein einzeiliges Bearbeitungssteuerelement, das den Text enthält.
ms.assetid: ae844cbf-fa43-4f91-90cc-688f44bf77a5
keywords:
- TVM_EDITLABEL Windows-Steuerelemente für Nachrichten
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
ms.openlocfilehash: 87ba9f9d0af4d6afb3c454f5e5477ccd67728bdec7f378b0f0a04adc901ba322
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118408587"
---
# <a name="tvm_editlabel-message"></a>TVM \_ EDITLABEL-Nachricht

Beginnt die direkte Bearbeitung des Texts des angegebenen Elements und ersetzt den Text des Elements durch ein einzeiliges Bearbeitungssteuerelement, das den Text enthält. Diese Meldung wählt implizit das angegebene Element aus und konzentriert es. Sie können diese Nachricht explizit oder mithilfe des [**TreeView \_ EditLabel-Makros**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_editlabel) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Handle für das zu bearbeitende Element.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt das Handle für das Bearbeitungssteuerelement zurück, das verwendet wird, um den Elementtext bei Erfolg zu bearbeiten, oder **andernfalls NULL.**

## <a name="remarks"></a>Hinweise

Diese Nachricht sendet einen [TVN \_ BEGINLABELEDIT-Benachrichtigungscode](tvn-beginlabeledit.md) an das übergeordnete Element des Strukturansichtssteuerelements.

Wenn der Benutzer die Bearbeitung abschließt oder abbricht, wird das Bearbeitungssteuerelement zerstört, und das Handle ist nicht mehr gültig. Sie können das Bearbeitungssteuerelement untergliedern, aber nicht zerstören.

Das Steuerelement muss den Fokus haben, bevor Sie diese Nachricht an das Steuerelement senden. Der Fokus kann mithilfe der [**SetFocus-Funktion**](/windows/desktop/api/winuser/nf-winuser-setfocus) festgelegt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **TVM \_ EDITLABELW** (Unicode) und **TVM \_ EDITLABELA** (ANSI)<br/>               |



 

