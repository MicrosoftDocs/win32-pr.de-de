---
title: TCM_HITTEST Meldung (kommstrg. h)
description: Bestimmt, welche Registerkarte, falls vorhanden, an einer angegebenen Bildschirmposition ist. Sie können diese Nachricht explizit oder mithilfe des tabctrl \_ HitTest-Makros senden.
ms.assetid: 0334f616-8d39-4460-a7f8-692a9ffab012
keywords:
- Windows-Steuerelemente für TCM_HITTEST Meldung
topic_type:
- apiref
api_name:
- TCM_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04787662e417513d8c9c93e45cecd0d8bddc6cfa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340366"
---
# <a name="tcm_hittest-message"></a>TCM- \_ HitTest-Meldung

Bestimmt, welche Registerkarte, falls vorhanden, an einer angegebenen Bildschirmposition ist. Sie können diese Nachricht explizit oder mithilfe des [**tabctrl \_ HitTest**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_hittest) -Makros senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**tchittestinfo**](/windows/win32/api/commctrl/ns-commctrl-tchittestinfo) -Struktur, die die zu überprüfende Bildschirmposition angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Index der Registerkarte zurück, oder-1, wenn sich keine Registerkarte an der angegebenen Position befindet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





