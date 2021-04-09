---
title: SB_SETICON Meldung (kommstrg. h)
description: Legt das Symbol für einen Teil in einer Statusleiste fest.
ms.assetid: d8528cd1-54d2-44ba-b0d6-29111f75616a
keywords:
- Windows-Steuerelemente für SB_SETICON Meldung
topic_type:
- apiref
api_name:
- SB_SETICON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f720c414238eb89cf98bf0556ebabffefceae4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859106"
---
# <a name="sb_seticon-message"></a>SB- \_ Nachricht

Legt das Symbol für einen Teil in einer Statusleiste fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

NULL basierter Index des Teils, der das Symbol empfängt. Wenn dieser Parameter-1 ist, wird angenommen, dass es sich bei der Statusleiste um eine einfache Statusleiste handelt.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle für das Symbol, das festgelegt werden soll. Wenn dieser Wert **null** ist, wird das Symbol aus dem Teil entfernt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg einen Wert ungleich 0 (null) zurück, andernfalls NULL.

## <a name="remarks"></a>Bemerkungen

Das Symbol wird in der Statusleiste nicht zerstört. Es ist die Aufgabe der aufrufenden Anwendung, beliebige Symbole nachzuverfolgen und zu zerstören.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





