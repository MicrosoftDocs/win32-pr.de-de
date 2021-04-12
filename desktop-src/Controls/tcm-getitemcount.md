---
title: TCM_GETITEMCOUNT Meldung (kommstrg. h)
description: Ruft die Anzahl der Registerkarten im Registerkarten-Steuerelement ab. Sie können diese Nachricht explizit oder mithilfe des tabctrl \_ GetItemCount-Makros senden.
ms.assetid: a8ec7d66-fe44-45ca-8f6c-4e75752ebe95
keywords:
- Windows-Steuerelemente für TCM_GETITEMCOUNT Meldung
topic_type:
- apiref
api_name:
- TCM_GETITEMCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d638a9be81581605b978695c8504f538967c77f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105741"
---
# <a name="tcm_getitemcount-message"></a>TCM \_ GetItemCount-Nachricht

Ruft die Anzahl der Registerkarten im Registerkarten-Steuerelement ab. Sie können diese Nachricht explizit oder mithilfe des [**tabctrl \_ GetItemCount**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getitemcount) -Makros senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die Anzahl der Elemente zurück, wenn erfolgreich, andernfalls 0 (null).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





