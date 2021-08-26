---
title: TB_GETHOTITEM Meldung (Commctrl.h)
description: Ruft den Index des heißen Elements in einer Symbolleiste ab.
ms.assetid: a87dbfc3-c6be-4a0a-9b6a-301b900d7929
keywords:
- TB_GETHOTITEM Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- TB_GETHOTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c22f33566a586ceaa524f720a9d688897f132ee227950f1f786093150955eafa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119918830"
---
# <a name="tb_gethotitem-message"></a>TB \_ GETHOTITEM-Nachricht

Ruft den Index des heißen Elements in einer Symbolleiste ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Index des heißen Elements oder -1 zurück, wenn kein heißes Element festgelegt ist. Symbolleistensteuerelemente, die nicht über den [**TBSTYLE \_ FLAT-Stil**](toolbar-control-and-button-styles.md) verfügen, verfügen nicht über heiße Elemente.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





