---
title: TCM_HIGHLIGHTITEM Meldung (kommstrg. h)
description: Legt den Hervorhebungs Zustand eines Registerkarten Elements fest. Sie können diese Nachricht explizit oder mithilfe des tabstrg \_ highlightitem-Makros senden.
ms.assetid: b0d0850a-62d9-46a1-8846-81f67a886ea8
keywords:
- Windows-Steuerelemente für TCM_HIGHLIGHTITEM Meldung
topic_type:
- apiref
api_name:
- TCM_HIGHLIGHTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55664aeeeefadfcb5205b9a5bde4fee1aafdfef3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859194"
---
# <a name="tcm_highlightitem-message"></a>TCM \_ highlightitem-Meldung

Legt den Hervorhebungs Zustand eines Registerkarten Elements fest. Sie können diese Nachricht explizit oder mithilfe des [**tabstrg \_ highlightitem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_highlightitem) -Makros senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein **int** -Wert, der den NULL basierten Index eines Registerkarten-Steuer Elements angibt.

</dd> <dt>

*lParam* 
</dt> <dd>

Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) ist ein **boolescher** Wert, der den festzulegenden Hervorhebungs Zustand angibt. Wenn dieser Wert **true** ist, wird die Registerkarte hervorgehoben. Wenn der Wert **false** ist, wird die Registerkarte auf den Standardzustand festgelegt. Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) muss NULL sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg einen Wert ungleich 0 (null) zurück, andernfalls NULL.

## <a name="remarks"></a>Bemerkungen

In Comctl32.dll Version 6,0 hat diese Nachricht keine sichtbare Auswirkung, wenn ein Design aktiv ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

