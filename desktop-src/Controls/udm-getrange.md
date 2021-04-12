---
title: UDM_GETRANGE Meldung (kommstrg. h)
description: Ruft die minimalen und maximalen Positionen (Bereich) für ein auf-ab-Steuerelement ab.
ms.assetid: fd42538a-8d96-4a9c-a1db-07c3e9afef84
keywords:
- Windows-Steuerelemente für UDM_GETRANGE Meldung
topic_type:
- apiref
api_name:
- UDM_GETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6fd8467ad4494bea92a4c1f9a68d675ef1471f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104213750"
---
# <a name="udm_getrange-message"></a>UDM- \_ GetRange-Nachricht

Ruft die minimalen und maximalen Positionen (Bereich) für ein auf-ab-Steuerelement ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist ein 32-Bit-Wert, der die Mindest-und höchst Position enthält. Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) ist die maximale Position für das Steuerelement, und das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) ist die minimale Position.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

