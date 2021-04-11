---
title: SB_GETBORDERS Meldung (kommstrg. h)
description: Ruft die aktuelle Breite der horizontalen und vertikalen Rahmen eines Status Fensters ab.
ms.assetid: 120c1e0d-6f42-424e-94e0-a080d216d39d
keywords:
- Windows-Steuerelemente für SB_GETBORDERS Meldung
topic_type:
- apiref
api_name:
- SB_GETBORDERS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 854df2cd367a852a2e6a0e638b470187efabe58c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105081"
---
# <a name="sb_getborders-message"></a>SB \_ getborders-Nachricht

Ruft die aktuelle Breite der horizontalen und vertikalen Rahmen eines Status Fensters ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf ein ganzzahliges Array, das über drei Elemente verfügt. Das erste Element empfängt die Breite des horizontalen Rahmens, das zweite empfängt die Breite des vertikalen Rahmens, und das dritte empfängt die Breite des Rahmens zwischen Rechtecke.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

## <a name="remarks"></a>Bemerkungen

Die Rahmen bestimmen den Abstand zwischen dem äußeren Rand des Fensters und den Rechtecke innerhalb des Fensters, die Text enthalten. Die Rahmen bestimmen auch den Abstand zwischen Rechtecke.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





