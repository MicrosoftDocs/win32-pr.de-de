---
title: MCM_GETCALID Meldung (kommstrg. h)
description: Ruft die Kalender-ID für das angegebene Kalender Steuerelement ab. Sie können diese Nachricht explizit oder mit dem monthcal \_ getcalid-Makro senden.
ms.assetid: ecfab4f3-a5af-445d-8b90-243b646524a6
keywords:
- Windows-Steuerelemente für MCM_GETCALID Meldung
topic_type:
- apiref
api_name:
- MCM_GETCALID
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb4a780d5107a7761d7dcac9b27a7cb01f3de744
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104037"
---
# <a name="mcm_getcalid-message"></a>MCM \_ getcalid-Meldung

Ruft die Kalender-ID für das angegebene Kalender Steuerelement ab. Sie können diese Nachricht explizit oder mit dem [**monthcal \_ getcalid-**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcalid) Makro senden.

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

ID des aktuellen Kalenders. Eine der-Konstanten des [Kalender Bezeichner](/windows/desktop/Intl/calendar-identifiers) .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

