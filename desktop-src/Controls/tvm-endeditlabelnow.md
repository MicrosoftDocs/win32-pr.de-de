---
title: TVM_ENDEDITLABELNOW Meldung (kommstrg. h)
description: Beendet die Bearbeitung der Bezeichnung eines Struktur Ansichts Elements. Sie können diese Nachricht explizit oder mithilfe des TreeView- \_ Makros "tdeditlabelnow" senden.
ms.assetid: 68de2020-9311-4958-859a-de55f5e41fcf
keywords:
- Windows-Steuerelemente für TVM_ENDEDITLABELNOW Meldung
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
ms.openlocfilehash: 4f059be20560adeb8cbcb0c63a2555283f6b7051
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517588"
---
# <a name="tvm_endeditlabelnow-message"></a>TVM- \_ Meldung "tdeditlabelnow"

Beendet die Bearbeitung der Bezeichnung eines Struktur Ansichts Elements. Sie können diese Nachricht explizit oder mithilfe des [**TreeView-Makros " \_ tdeditlabelnow**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_endeditlabelnow) " senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Eine Variable, die angibt, ob die Bearbeitung abgebrochen wird, ohne dass Sie in der Bezeichnung gespeichert wird. Wenn dieser Parameter **true** ist, bricht das System die Bearbeitung ab, ohne die Änderungen zu speichern. Andernfalls speichert das System die Änderungen an der Bezeichnung.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

## <a name="remarks"></a>Bemerkungen

Diese Meldung bewirkt, dass der [TVN \_ endlabeledit](tvn-endlabeledit.md) -Benachrichtigungs Code an das übergeordnete Fenster des Strukturansicht-Steuer Elements gesendet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





