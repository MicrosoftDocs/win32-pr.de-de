---
title: LVM_GETSELECTIONMARK Meldung (kommstrg. h)
description: Ruft die Auswahl Markierung von einem Listenansicht-Steuerelement ab. Sie können diese Nachricht explizit senden oder das ListView \_ getselectionmark-Makro verwenden.
ms.assetid: 21daf7d7-1217-4608-93f9-c390546f1591
keywords:
- Windows-Steuerelemente für LVM_GETSELECTIONMARK Meldung
topic_type:
- apiref
api_name:
- LVM_GETSELECTIONMARK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 076aff15ff69c4b442c74022ed5a7c02b92a8c52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342468"
---
# <a name="lvm_getselectionmark-message"></a>LVM \_ getselectionmark-Nachricht

Ruft die Auswahl Markierung von einem Listenansicht-Steuerelement ab. Sie können diese Nachricht explizit senden oder das [**ListView \_ getselectionmark**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getselectionmark) -Makro verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt das null basierte Auswahl Zeichen oder-1 zurück, wenn kein Auswahl Zeichen vorhanden ist.

## <a name="remarks"></a>Bemerkungen

Das *Auswahl Zeichen* ist der Element Index, von dem eine Mehrfachauswahl gestartet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**LVM \_ setselectionmark**](lvm-setselectionmark.md)
</dt> </dl>

 

 





