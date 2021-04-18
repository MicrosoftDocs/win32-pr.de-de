---
title: TCM_GETCURSEL Meldung (kommstrg. h)
description: Bestimmt die derzeit ausgewählte Registerkarte in einem Registerkarten-Steuerelement. Sie können diese Nachricht explizit oder mithilfe des tabstrg \_ getcurrsel-Makros senden.
ms.assetid: 1caa7fad-da5a-4b26-8e78-12110c126691
keywords:
- Windows-Steuerelemente für TCM_GETCURSEL Meldung
topic_type:
- apiref
api_name:
- TCM_GETCURSEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3103931e29d150412192a745f8dde7681cff0e94
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338785"
---
# <a name="tcm_getcursel-message"></a>TCM \_ getcurrsel-Nachricht

Bestimmt die derzeit ausgewählte Registerkarte in einem Registerkarten-Steuerelement. Sie können diese Nachricht explizit oder mithilfe des [**tabstrg \_ getcurrsel**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getcursel) -Makros senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Index der ausgewählten Registerkarte zurück, wenn erfolgreich, oder-1, wenn keine Registerkarte ausgewählt ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





