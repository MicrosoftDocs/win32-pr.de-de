---
title: SB_GETICON Meldung (kommstrg. h)
description: Ruft das Symbol für einen Teil in einer Statusleiste ab.
ms.assetid: f99508e3-afa8-48fd-b87a-fce41c4410ff
keywords:
- Windows-Steuerelemente für SB_GETICON Meldung
topic_type:
- apiref
api_name:
- SB_GETICON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab86809df54d796b8e83f05f2a2b9041450ce2fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859109"
---
# <a name="sb_geticon-message"></a>SB- \_ GetIcon-Nachricht

Ruft das Symbol für einen Teil in einer Statusleiste ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

NULL basierter Index des Teils, der das abzurufende Symbol enthält. Wenn dieser Parameter-1 ist, wird angenommen, dass es sich bei der Statusleiste um eine Statusleiste im [einfachen Modus](status-bars.md) handelt.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt das Handle für das Symbol zurück, wenn erfolgreich, andernfalls **null** .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





