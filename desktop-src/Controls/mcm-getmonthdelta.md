---
title: MCM_GETMONTHDELTA Meldung (kommstrg. h)
description: Ruft die Bild Lauf Rate für ein Monatskalender-Steuerelement ab. Die Scrollrate entspricht der Anzahl von Monaten, die das Steuerelement seine Anzeige verschiebt, wenn der Benutzer auf eine Bild Lauf Schaltfläche klickt. Sie können diese Nachricht explizit oder mit dem monthcal \_ getmonthdelta-Makro senden.
ms.assetid: 6db02993-b22c-430f-8928-8bd5768b2151
keywords:
- Windows-Steuerelemente für MCM_GETMONTHDELTA Meldung
topic_type:
- apiref
api_name:
- MCM_GETMONTHDELTA
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01eaa40b930e6317cc2be6b674f0cea58115ae40
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106659"
---
# <a name="mcm_getmonthdelta-message"></a>MCM \_ getmonthdelta-Meldung

Ruft die Bild Lauf Rate für ein Monatskalender-Steuerelement ab. Die Scrollrate entspricht der Anzahl von Monaten, die das Steuerelement seine Anzeige verschiebt, wenn der Benutzer auf eine Bild Lauf Schaltfläche klickt. Sie können diese Nachricht explizit oder mit dem [**monthcal \_ getmonthdelta**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmonthdelta) -Makro senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn der Monat Delta zuvor mithilfe der [**MCM- \_ setmonthdelta**](mcm-setmonthdelta.md) -Nachricht festgelegt wurde, gibt einen int-Wert zurück, der die aktuelle Scrollrate des Monats Kalenders darstellt. Wenn das Delta für den Monat nicht zuvor mithilfe der **MCM- \_ setmonthdelta** -Nachricht festgelegt wurde, oder wenn der Monat Delta auf den Standardwert zurückgesetzt wurde, gibt einen int-Wert zurück, der die aktuelle Anzahl der sichtbaren Monate darstellt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





