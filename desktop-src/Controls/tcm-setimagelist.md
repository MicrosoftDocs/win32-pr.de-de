---
title: TCM_SETIMAGELIST Meldung (kommstrg. h)
description: Weist einem Registerkarten-Steuerelement eine Bildliste zu. Sie können diese Nachricht explizit oder mithilfe des tabstrg \_ SetImageList-Makros senden.
ms.assetid: b457c73c-4c38-4bc5-af5d-12bbd24504a6
keywords:
- Windows-Steuerelemente für TCM_SETIMAGELIST Meldung
topic_type:
- apiref
api_name:
- TCM_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59172c677998e816b295939c14effe45ff8aa961
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040086"
---
# <a name="tcm_setimagelist-message"></a>TCM \_ SetImageList-Meldung

Weist einem Registerkarten-Steuerelement eine Bildliste zu. Sie können diese Nachricht explizit oder mithilfe des [**tabstrg \_ SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setimagelist) -Makros senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Handle für die Bildliste, die dem Registerkarten-Steuerelement zugewiesen werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt das Handle für die vorherige Bildliste zurück, oder **null** , wenn keine vorherige Bildliste vorhanden ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





