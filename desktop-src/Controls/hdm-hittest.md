---
title: HDM_HITTEST Meldung (kommstrg. h)
description: Testet einen Punkt, um zu bestimmen, welches Header Element, sofern vorhanden, sich am angegebenen Punkt befindet.
ms.assetid: ff866bd1-9f2a-457c-921d-549610ab9088
keywords:
- Windows-Steuerelemente für HDM_HITTEST Meldung
topic_type:
- apiref
api_name:
- HDM_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8b6634396dbd5ecd4510a4f7341fc6380dbb0ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104481"
---
# <a name="hdm_hittest-message"></a>HDM- \_ HitTest-Meldung

Testet einen Punkt, um zu bestimmen, welches Header Element, sofern vorhanden, sich am angegebenen Punkt befindet.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**hdhittestinfo**](/windows/win32/api/commctrl/ns-commctrl-hdhittestinfo) -Struktur, die die zu testende Position enthält und Informationen über die Ergebnisse des Tests empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Index des Elements an der angegebenen Position zurück, sofern vorhanden, oder andernfalls 1.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





