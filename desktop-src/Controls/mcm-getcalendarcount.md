---
title: MCM_GETCALENDARCOUNT Meldung (kommstrg. h)
description: Ruft die Anzahl der Kalender ab, die momentan im Kalender Steuerelement angezeigt werden. Sie können diese Nachricht explizit oder mit dem monthcal \_ getcalendarcount-Makro senden.
ms.assetid: b9463f02-d37b-49b0-8387-0938020c23ee
keywords:
- Windows-Steuerelemente für MCM_GETCALENDARCOUNT Meldung
topic_type:
- apiref
api_name:
- MCM_GETCALENDARCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14a3be9e9bcc5db8c1aab32cacbcc2ded82727af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104805"
---
# <a name="mcm_getcalendarcount-message"></a>MCM \_ getcalendarcount-Meldung

Ruft die Anzahl der Kalender ab, die momentan im Kalender Steuerelement angezeigt werden. Sie können diese Nachricht explizit oder mit dem [**monthcal \_ getcalendarcount**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcalendarcount) -Makro senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Muss Null sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Muss Null sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Anzahl der derzeit im Kalender Steuerelement angezeigten Kalender. Die maximal zulässige Anzahl zulässiger Kalender ist 12.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





