---
title: SB_SETPARTS Meldung (kommstrg. h)
description: Legt die Anzahl der Teile in einem Statusfenster und die Koordinate des rechten Rands der einzelnen Teile fest.
ms.assetid: e29e8b09-c018-4ea4-8b47-6f3713113427
keywords:
- Windows-Steuerelemente für SB_SETPARTS Meldung
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
ms.openlocfilehash: 062058fa3778cd0394cadd9d76b363a0353ffb2e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518437"
---
# <a name="sb_setparts-message"></a>SB- \_ SetParts-Nachricht

Legt die Anzahl der Teile in einem Statusfenster und die Koordinate des rechten Rands der einzelnen Teile fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Anzahl der festzulegenden Teile (darf nicht größer als 256 sein).

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf ein ganzzahliges Array. Die Anzahl der Elemente wird in *wParam* angegeben. Jedes Element gibt die Position (in Client Koordinaten) des rechten Rands des entsprechenden Teils an. Wenn ein Element-1 ist, wird der Rechte Rand des entsprechenden Teils auf den Rahmen des Fensters erweitert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





