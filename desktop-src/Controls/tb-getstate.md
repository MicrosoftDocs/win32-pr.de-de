---
title: TB_GETSTATE Meldung (kommstrg. h)
description: Ruft Informationen zum Zustand der angegebenen Schaltfläche in einer Symbolleiste ab, z. b. ob Sie aktiviert, gedrückt oder aktiviert ist.
ms.assetid: e8a9e1ff-506f-413b-8f8c-986c25bce736
keywords:
- Windows-Steuerelemente für TB_GETSTATE Meldung
topic_type:
- apiref
api_name:
- TB_GETSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3b5c50978da78218be7f3d47208c0ea430ff36c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858731"
---
# <a name="tb_getstate-message"></a>TB \_ GetState-Nachricht

Ruft Informationen zum Zustand der angegebenen Schaltfläche in einer Symbolleiste ab, z. b. ob Sie aktiviert, gedrückt oder aktiviert ist.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Befehls Bezeichner der Schaltfläche, für die Informationen abgerufen werden sollen.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die Schaltflächen Zustandsinformationen zurück, wenn erfolgreich, andernfalls-1. Die Schaltflächen Zustandsinformationen können eine Kombination der Werte sein, die in den Symbolleisten- [**Schaltflächen Zuständen**](toolbar-button-states.md)aufgeführt sind

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





