---
title: MCM_SETMONTHDELTA Meldung (kommstrg. h)
description: Legt die Bild Lauf Rate für ein Monatskalender-Steuerelement fest. Die Scrollrate entspricht der Anzahl von Monaten, die das Steuerelement seine Anzeige verschiebt, wenn der Benutzer auf eine Bild Lauf Schaltfläche klickt. Sie können diese Nachricht explizit oder mit dem monthcal- \_ setmonthdelta-Makro senden.
ms.assetid: 2d01b95f-3be8-4548-80b5-ac01d3e49e9f
keywords:
- Windows-Steuerelemente für MCM_SETMONTHDELTA Meldung
topic_type:
- apiref
api_name:
- MCM_SETMONTHDELTA
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 123eddb55a7ee8ddf8e3f6d8136e9ee57dfc8681
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340006"
---
# <a name="mcm_setmonthdelta-message"></a>MCM- \_ setmonthdelta-Meldung

Legt die Bild Lauf Rate für ein Monatskalender-Steuerelement fest. Die Scrollrate entspricht der Anzahl von Monaten, die das Steuerelement seine Anzeige verschiebt, wenn der Benutzer auf eine Bild Lauf Schaltfläche klickt. Sie können diese Nachricht explizit oder mit dem [**monthcal- \_ setmonthdelta**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setmonthdelta) -Makro senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Wert, der die Anzahl der Monate darstellt, die als Schiebe Rate des Steuer Elements festgelegt werden sollen. Wenn dieser Wert 0 (null) ist, wird der Monat Delta auf den Standardwert zurückgesetzt. Dies ist die Anzahl der Monate, die im Steuerelement angezeigt werden.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen int-Wert zurück, der die vorherige Scrollrate darstellt. Wenn die Scrollrate zuvor nicht festgelegt wurde, ist der Rückgabewert 0 (null).

## <a name="remarks"></a>Bemerkungen

Die Bild-auf-und Bild-ab-Taste, VK \_ vor und VK, \_ Ändern Sie den ausgewählten Monat um 1, unabhängig von der Anzahl der angezeigten Monate oder des durch **MCM \_ setmonthdelta** festgelegten Werts.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





