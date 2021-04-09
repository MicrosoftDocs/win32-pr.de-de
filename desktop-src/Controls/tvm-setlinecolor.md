---
title: TVM_SETLINECOLOR Meldung (kommstrg. h)
description: Die TVM- \_ setlinecolor-Meldung legt die aktuelle Linien Farbe fest.
ms.assetid: c5fc28af-5603-489f-aa6b-73e153f9aebc
keywords:
- Windows-Steuerelemente für TVM_SETLINECOLOR Meldung
topic_type:
- apiref
api_name:
- TVM_SETLINECOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d70340ea0d2339055faa3fb473269f3b244f335
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040719"
---
# <a name="tvm_setlinecolor-message"></a>TVM- \_ setlinecolor-Meldung

Die **TVM- \_ setlinecolor** -Meldung legt die aktuelle Linien Farbe fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Neue Zeilen Farbe. Verwenden Sie den CLR- \_ Standardwert, um die System Standardfarben wiederherzustellen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die vorherige Linien Farbe zurück.

## <a name="remarks"></a>Bemerkungen

Diese Meldung ändert nur die Linien Farben. Um die Farben von ' + ' und '-' innerhalb der Schaltflächen zu ändern, verwenden Sie die [**TVM \_ SetTextColor**](tvm-settextcolor.md) -Nachricht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**TVM \_ getLineColor**](tvm-getlinecolor.md)
</dt> </dl>

 

 





