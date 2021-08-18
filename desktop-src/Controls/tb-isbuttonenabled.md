---
title: TB_ISBUTTONENABLED (Commctrl.h)
description: Bestimmt, ob die angegebene Schaltfläche in einer Symbolleiste aktiviert ist.
ms.assetid: 055ed89a-2f3a-4174-b249-c6e68afbad31
keywords:
- TB_ISBUTTONENABLED von Windows Steuerelementen
topic_type:
- apiref
api_name:
- TB_ISBUTTONENABLED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07ceb230edb693e065a7ef0455c1374b410a2dcd86995dc1a0ec8c2b354ae028
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119918460"
---
# <a name="tb_isbuttonenabled-message"></a>TB \_ ISBUTTONENABLED-Nachricht

Bestimmt, ob die angegebene Schaltfläche in einer Symbolleiste aktiviert ist.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Befehlsbezeichner der Schaltfläche.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen Wert ungleich 0 (null) zurück, wenn die Schaltfläche aktiviert ist, andernfalls 0 (null).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





