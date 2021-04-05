---
title: TCM_GETROWCOUNT Meldung (kommstrg. h)
description: Ruft die aktuelle Anzahl der Zeilen von Registerkarten in einem Registerkarten-Steuerelement ab. Sie können diese Nachricht explizit oder mithilfe des tabctrl \_ GetRowCount-Makros senden.
ms.assetid: ef104374-1030-46c3-876e-083df73854ab
keywords:
- Windows-Steuerelemente für TCM_GETROWCOUNT Meldung
topic_type:
- apiref
api_name:
- TCM_GETROWCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9bc3d9985591a08b96be2f21d55b8a6cade9b7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859197"
---
# <a name="tcm_getrowcount-message"></a>TCM \_ GetRowCount-Nachricht

Ruft die aktuelle Anzahl der Zeilen von Registerkarten in einem Registerkarten-Steuerelement ab. Sie können diese Nachricht explizit oder mithilfe des [**tabctrl \_ GetRowCount**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getrowcount) -Makros senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die Anzahl der Zeilen von Registerkarten zurück.

## <a name="remarks"></a>Bemerkungen

Nur Registerkarten-Steuerelemente, die den [**\_ mehrzeiligen TCS**](tab-control-styles.md) -Stil aufweisen, können mehrere Zeilen mit Registerkarten aufweisen

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





