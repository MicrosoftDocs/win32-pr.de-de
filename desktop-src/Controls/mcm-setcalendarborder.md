---
title: MCM_SETCALENDARBORDER Meldung (kommstrg. h)
description: Legt die Größe des Rahmens in Pixel fest. Sie können diese Nachricht explizit oder mit dem monthcal- \_ setcalendarborder-Makro senden.
ms.assetid: 2a64a08f-a1fb-47a8-8f09-725807e87a03
keywords:
- Windows-Steuerelemente für MCM_SETCALENDARBORDER Meldung
topic_type:
- apiref
api_name:
- MCM_SETCALENDARBORDER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09b870346e8d8b475833657dd83141ba1fe11715
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476626"
---
# <a name="mcm_setcalendarborder-message"></a>MCM \_ setcalendarborder-Meldung

Legt die Größe des Rahmens in Pixel fest. Sie können diese Nachricht explizit oder mit dem [**monthcal- \_ setcalendarborder**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcalendarborder) -Makro senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

**True** gibt an, dass die Rahmengröße auf die Anzahl der Pixel festgelegt wird, die *LPARAM* angibt. Wenn der Wert **false** ist, wird die Rahmengröße auf den Standardwert zurückgesetzt, der durch das Design angegeben wird, oder 0 (null), wenn keine Designs verwendet werden.

</dd> <dt>

*lParam* 
</dt> <dd>

Anzahl der Pixel der Rahmengröße.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Nicht verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





