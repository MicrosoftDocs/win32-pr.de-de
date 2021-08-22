---
title: LVM_SETSELECTIONMARK Meldung (Commctrl.h)
description: Legt das Auswahlzeichen in einem Listenansicht-Steuerelement fest. Sie können diese Nachricht explizit senden oder das ListView \_ SetSelectionMark-Makro verwenden.
ms.assetid: 3218f1b3-b934-4083-aaaa-e10ef1dbb6bd
keywords:
- LVM_SETSELECTIONMARK Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- LVM_SETSELECTIONMARK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c80f1392b5bb8b8ae49eaefb639a60213b5d4a7deaf153b99262bf608a770e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119217360"
---
# <a name="lvm_setselectionmark-message"></a>LVM \_ SETSELECTIONMARK-Meldung

Legt das Auswahlzeichen in einem Listenansicht-Steuerelement fest. Sie können diese Nachricht explizit senden oder das [**ListView \_ SetSelectionMark-Makro**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setselectionmark) verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Nullbasierter Index der neuen Auswahlmarkierung. Wenn -1 festgelegt ist, wird das Auswahlzeichen entfernt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt das vorherige Auswahlzeichen oder -1 zurück, wenn kein vorheriges Auswahlzeichen vorhanden ist.

## <a name="remarks"></a>Hinweise

Das *Auswahlzeichen* ist der Elementindex, ab dem eine Mehrfachauswahl beginnt. Diese Meldung wirkt sich nicht auf den Auswahlzustand des Elements aus.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**LVM \_ GETSELECTIONMARK**](lvm-getselectionmark.md)
</dt> </dl>

 

 





