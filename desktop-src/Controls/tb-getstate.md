---
title: TB_GETSTATE Meldung (Commctrl.h)
description: Ruft Informationen zum Status der angegebenen Schaltfläche auf einer Symbolleiste ab, z. B. ob sie aktiviert, gedrückt oder aktiviert ist.
ms.assetid: e8a9e1ff-506f-413b-8f8c-986c25bce736
keywords:
- TB_GETSTATE Windows-Steuerelementen
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
ms.openlocfilehash: de1757cfd71427904dc7060cc0084c64b82f143e1a8db666e40fe9e08c64c7ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118168236"
---
# <a name="tb_getstate-message"></a>TB \_ GETSTATE-Nachricht

Ruft Informationen zum Status der angegebenen Schaltfläche auf einer Symbolleiste ab, z. B. ob sie aktiviert, gedrückt oder aktiviert ist.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Befehlsbezeichner der Schaltfläche, für die Informationen abgerufen werden sollen.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg die Zustandsinformationen der Schaltfläche zurück, andernfalls -1. Die Zustandsinformationen der Schaltfläche können eine Kombination der Werte sein, die unter [**Symbolleistenschaltflächenstatus**](toolbar-button-states.md)aufgeführt sind.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





