---
title: LVM_GETSELECTIONMARK-Nachricht (Commctrl.h)
description: Ruft das Auswahlzeichen aus einem Listenansichtssteuerelement ab. Sie können diese Nachricht explizit senden oder das ListView \_ GetSelectionMark-Makro verwenden.
ms.assetid: 21daf7d7-1217-4608-93f9-c390546f1591
keywords:
- LVM_GETSELECTIONMARK Windows-Steuerelementen
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
ms.openlocfilehash: ed2675550ebc4cf456b439a2e5869068e983f46c82bf6fdde99d8b92806e6cac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118670978"
---
# <a name="lvm_getselectionmark-message"></a>LVM \_ GETSELECTIONMARK-Nachricht

Ruft das Auswahlzeichen aus einem Listenansichtssteuerelement ab. Sie können diese Nachricht explizit senden oder das [**ListView \_ GetSelectionMark-Makro**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getselectionmark) verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt das nullbasierte Auswahlzeichen oder -1 zurück, wenn kein Auswahlzeichen vorhanden ist.

## <a name="remarks"></a>Hinweise

Das *Auswahlzeichen* ist der Elementindex, ab dem eine Mehrfachauswahl beginnt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**LVM \_ SETSELECTIONMARK**](lvm-setselectionmark.md)
</dt> </dl>

 

 





