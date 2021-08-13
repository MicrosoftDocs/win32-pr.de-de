---
title: TVM_ENDEDITLABELNOW Meldung (Commctrl.h)
description: Beendet die Bearbeitung der Bezeichnung eines Strukturansichtselements. Sie können diese Nachricht explizit oder mithilfe des \_ TreeView-Makros EndEditLabelNow senden.
ms.assetid: 68de2020-9311-4958-859a-de55f5e41fcf
keywords:
- TVM_ENDEDITLABELNOW Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- TVM_ENDEDITLABELNOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18355edc8efb18ea56a39e60c68361a7ef8d72e39af644707d6d102738fd60c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119387260"
---
# <a name="tvm_endeditlabelnow-message"></a>TVM \_ ENDEDITLABELNOW-Nachricht

Beendet die Bearbeitung der Bezeichnung eines Strukturansichtselements. Sie können diese Nachricht explizit oder mithilfe des [**\_ TreeView-Makros EndEditLabelNow**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_endeditlabelnow) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Variable, die angibt, ob die Bearbeitung abgebrochen wird, ohne in der Bezeichnung gespeichert zu werden. Wenn dieser Parameter **TRUE** ist, bricht das System die Bearbeitung ab, ohne die Änderungen zu speichern. Andernfalls speichert das System die Änderungen an der Bezeichnung.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn erfolgreich, **andernfalls FALSE.**

## <a name="remarks"></a>Hinweise

Diese Meldung bewirkt, dass der [TVN \_ ENDLABELEDIT-Benachrichtigungscode](tvn-endlabeledit.md) an das übergeordnete Fenster des Strukturansichtssteuerelements gesendet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





