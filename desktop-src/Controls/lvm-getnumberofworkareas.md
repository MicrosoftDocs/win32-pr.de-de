---
title: LVM_GETNUMBEROFWORKAREAS Meldung (kommstrg. h)
description: Ruft die Anzahl der Arbeitsbereiche in einem Listenansicht-Steuerelement ab. Sie können diese Nachricht explizit senden oder das ListView \_ getnumofworkareas-Makro verwenden.
ms.assetid: ce0bcccd-62a2-45a4-959e-9959c9ca0c46
keywords:
- Windows-Steuerelemente für LVM_GETNUMBEROFWORKAREAS Meldung
topic_type:
- apiref
api_name:
- LVM_GETNUMBEROFWORKAREAS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a73c62b7184ba60b979356a98a93d2579c8f74a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956987"
---
# <a name="lvm_getnumberofworkareas-message"></a>LVM \_ getnumofworkareas-Meldung

Ruft die Anzahl der Arbeitsbereiche in einem Listenansicht-Steuerelement ab. Sie können diese Nachricht explizit senden oder das [**ListView \_ getnumofworkareas**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getnumberofworkareas) -Makro verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf einen uint-Wert, der die Anzahl der Arbeitsbereiche im Listenansicht-Steuerelement empfängt. Wenn NULL in diese Variable eingefügt wird, sind derzeit keine Arbeitsbereiche festgelegt. Dieser Wert darf nicht **null** sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert für diese Nachricht wird nicht verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Verwenden von List-View Steuerelementen](using-list-view-controls.md)
</dt> </dl>

 

 





