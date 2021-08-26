---
title: TCM_GETROWCOUNT (Commctrl.h)
description: Ruft die aktuelle Anzahl von Zeilen von Registerkarten in einem Registerkarten-Steuerelement ab. Sie können diese Nachricht explizit oder mithilfe des TabCtrl \_ GetRowCount-Makros senden.
ms.assetid: ef104374-1030-46c3-876e-083df73854ab
keywords:
- TCM_GETROWCOUNT von Windows-Steuerelementen
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
ms.openlocfilehash: 9e67b2ac40834075b31ccf2415a52c96448b8143dde3d6bc67f9c515e1f601a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104870"
---
# <a name="tcm_getrowcount-message"></a>TCM \_ GETROWCOUNT-Nachricht

Ruft die aktuelle Anzahl von Zeilen von Registerkarten in einem Registerkarten-Steuerelement ab. Sie können diese Nachricht explizit oder mithilfe des [**TabCtrl \_ GetRowCount-Makros**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getrowcount) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die Anzahl der Zeilen von Registerkarten zurück.

## <a name="remarks"></a>Hinweise

Nur Registerkartensteuerelemente mit [**dem TCS \_ MULTILINE-Stil**](tab-control-styles.md) können mehrere Zeilen mit Registerkarten enthalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





