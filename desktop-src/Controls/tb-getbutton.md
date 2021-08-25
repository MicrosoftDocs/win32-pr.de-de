---
title: TB_GETBUTTON-Nachricht (Commctrl.h)
description: Ruft Informationen über die angegebene Schaltfläche in einer Symbolleiste ab.
ms.assetid: d90d053c-0daf-4a5a-b7ca-b9b4472c65a3
keywords:
- TB_GETBUTTON Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- TB_GETBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e36d8cd4e382570884b0cb30f7c95615e2342544cab0970e9864e9fde7882f0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919030"
---
# <a name="tb_getbutton-message"></a>TB \_ GETBUTTON-Nachricht

Ruft Informationen über die angegebene Schaltfläche in einer Symbolleiste ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Nullbasierter Index der Schaltfläche, für die Informationen abgerufen werden sollen.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf die [**TBBUTTON-Struktur,**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) die die Schaltflächeninformationen empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn erfolgreich, **andernfalls FALSE.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





