---
title: UDM_GETRANGE Meldung (Commctrl.h)
description: Ruft die minimalen und maximalen Positionen (Bereich) für ein Auf-Ab-Steuerelement ab.
ms.assetid: fd42538a-8d96-4a9c-a1db-07c3e9afef84
keywords:
- UDM_GETRANGE Windows-Steuerelemente für Nachrichten
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
ms.openlocfilehash: d13811f383886e0e4985eb3f2f5093eec53cb0745349a36ca133fa3de9656773
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118408100"
---
# <a name="udm_getrange-message"></a>UDM \_ GETRANGE-Nachricht

Ruft die minimalen und maximalen Positionen (Bereich) für ein Auf-Ab-Steuerelement ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist ein 32-Bit-Wert, der die minimalen und maximalen Positionen enthält. [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) ist die maximale Position für das Steuerelement, und [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) ist die Mindestposition.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

