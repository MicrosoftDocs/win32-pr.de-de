---
title: LVM_GETNUMBEROFWORKAREAS (Commctrl.h)
description: Ruft die Anzahl der Arbeitsbereiche in einem Listenansicht-Steuerelement ab. Sie können diese Nachricht explizit senden oder das \_ ListView-Makro GetNumberOfWorkAreas verwenden.
ms.assetid: ce0bcccd-62a2-45a4-959e-9959c9ca0c46
keywords:
- LVM_GETNUMBEROFWORKAREAS von Windows-Steuerelementen
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
ms.openlocfilehash: 735dbb808755857df3dec4c5e8a021b9fe873e555607dc547bc77e67e123b948
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088880"
---
# <a name="lvm_getnumberofworkareas-message"></a>LVM \_ GETNUMBEROFWORKAREAS-Meldung

Ruft die Anzahl der Arbeitsbereiche in einem Listenansicht-Steuerelement ab. Sie können diese Nachricht explizit senden oder das [**\_ ListView-Makro GetNumberOfWorkAreas**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getnumberofworkareas) verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf einen UINT-Wert, der die Anzahl der Arbeitsbereiche im Listenansicht-Steuerelement empfängt. Wenn in dieser Variablen 0 (null) platziert wird, sind derzeit keine Arbeitsbereiche festgelegt. Dieser Wert darf nicht **NULL sein.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert für diese Meldung wird nicht verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Verwenden List-View-Steuerelementen](using-list-view-controls.md)
</dt> </dl>

 

 





