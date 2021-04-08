---
title: LVM_SETSELECTIONMARK Meldung (kommstrg. h)
description: Legt die Auswahl Markierung in einem Listenansicht-Steuerelement fest. Sie können diese Nachricht explizit senden oder das ListView \_ setselectionmark-Makro verwenden.
ms.assetid: 3218f1b3-b934-4083-aaaa-e10ef1dbb6bd
keywords:
- Windows-Steuerelemente für LVM_SETSELECTIONMARK Meldung
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
ms.openlocfilehash: 3efc01068f22585061cae5a6f2c5c0c841810f52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739936"
---
# <a name="lvm_setselectionmark-message"></a>LVM- \_ setselectionmark-Nachricht

Legt die Auswahl Markierung in einem Listenansicht-Steuerelement fest. Sie können diese Nachricht explizit senden oder das [**ListView \_ setselectionmark**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setselectionmark) -Makro verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

NULL basierter Index der neuen Auswahl Markierung. Wenn der Wert auf-1 festgelegt ist, wird das Auswahl Zeichen entfernt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die vorherige Auswahl Markierung oder-1 zurück, wenn keine vorherige Auswahl Markierung vorhanden ist.

## <a name="remarks"></a>Bemerkungen

Das *Auswahl Zeichen* ist der Element Index, von dem eine Mehrfachauswahl gestartet wird. Diese Meldung wirkt sich nicht auf den Auswahl Zustand des Elements aus.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**LVM \_ getselectionmark**](lvm-getselectionmark.md)
</dt> </dl>

 

 





