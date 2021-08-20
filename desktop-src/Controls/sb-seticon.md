---
title: SB_SETICON (Commctrl.h)
description: Legt das Symbol für ein Teil in einer Statusleiste fest.
ms.assetid: d8528cd1-54d2-44ba-b0d6-29111f75616a
keywords:
- SB_SETICON von Windows-Steuerelementen
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
ms.openlocfilehash: d0e08b1c3b0ce1a453ca9050c20552a14169a594c8091708339b4a436f1fb1a3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540070"
---
# <a name="sb_seticon-message"></a>SB \_ SETICON-Nachricht

Legt das Symbol für ein Teil in einer Statusleiste fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Nullbasierter Index des Teils, der das Symbol erhält. Wenn dieser Parameter -1 ist, wird davon ausgegangen, dass es sich bei der Statusleiste um eine einfache Statusleiste handelt.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle für das symbol, das festgelegt werden soll. Wenn dieser Wert **NULL ist,** wird das Symbol aus dem Teil entfernt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg einen Wert ungleich 0 (null) oder andernfalls 0 (null) zurück.

## <a name="remarks"></a>Hinweise

Die Statusleiste zerstört das Symbol nicht. Es liegt in der Verantwortung der aufrufenden Anwendung, Symbole nachverfolgung und zu zerstören.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





