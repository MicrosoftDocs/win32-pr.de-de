---
title: TCM_GETCURFOCUS Meldung (kommstrg. h)
description: Gibt den Index des Elements zurück, das in einem Registerkarten-Steuerelement den Fokus besitzt. Sie können diese Nachricht explizit oder mithilfe des tabstrg \_ getcurrfocus-Makros senden.
ms.assetid: ae6ee159-c769-41d6-b0bb-2a9ade4c0e71
keywords:
- Windows-Steuerelemente für TCM_GETCURFOCUS Meldung
topic_type:
- apiref
api_name:
- TCM_GETCURFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0b0d0f3d2bbd4a7cf0ab2a63c5a988f60768eec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957040"
---
# <a name="tcm_getcurfocus-message"></a>TCM \_ getcurrfocus-Nachricht

Gibt den Index des Elements zurück, das in einem Registerkarten-Steuerelement den Fokus besitzt. Sie können diese Nachricht explizit oder mithilfe des [**tabstrg \_ getcurrfocus**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getcurfocus) -Makros senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Index des Registerkarten Elements zurück, das den Fokus besitzt.

## <a name="remarks"></a>Bemerkungen

Das Element, das den Fokus besitzt, kann sich von dem ausgewählten Element unterscheiden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





