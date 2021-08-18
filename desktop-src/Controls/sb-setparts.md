---
title: SB_SETPARTS (Commctrl.h)
description: Legt die Anzahl der Teile in einem Statusfenster und die Koordinate des rechten Rands jedes Teils fest.
ms.assetid: e29e8b09-c018-4ea4-8b47-6f3713113427
keywords:
- SB_SETPARTS meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- SB_SETPARTS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a63694ba40eb77cd887454b634ba8cdd2bff2c6ee7bb75beb9a7230eb3d1e1d0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119637030"
---
# <a name="sb_setparts-message"></a>SB \_ SETPARTS-Nachricht

Legt die Anzahl der Teile in einem Statusfenster und die Koordinate des rechten Rands jedes Teils fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Anzahl der zu setzenden Teile (darf nicht größer als 256 sein).

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf ein Ganzzahlarray. Die Anzahl der Elemente wird in *wParam angegeben.* Jedes Element gibt die Position des rechten Rands des entsprechenden Teils in Clientkoordinaten an. Wenn ein Element -1 ist, wird der rechte Rand des entsprechenden Teils bis zum Rahmen des Fensters erweitert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** wenn erfolgreich, andernfalls **FALSE.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





