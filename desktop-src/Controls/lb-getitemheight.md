---
title: LB_GETITEMHEIGHT (Winuser.h)
description: Ruft die Höhe von Elementen in einem Listenfeld ab.
ms.assetid: ee96fce6-babd-4581-ac0e-2eb955fe543b
keywords:
- LB_GETITEMHEIGHT message Windows Controls
topic_type:
- apiref
api_name:
- LB_GETITEMHEIGHT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29c232c172f14774db9dd7c783e18a10f0888190708432b9336208570f0d5031
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119434330"
---
# <a name="lb_getitemheight-message"></a>LB \_ GETITEMHEIGHT-Nachricht

Ruft die Höhe von Elementen in einem Listenfeld ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der nullbasierte Index des Listenfeldelements. Dieser Index wird nur verwendet, wenn das Listenfeld über den [**LBS \_ OWNERDRAWVARIABLE-Stil**](list-box-styles.md) verfügt, andernfalls muss er 0 (null) sein.

Windows 95/Windows 98/Windows Edition (Windows Me): Der *wParam-Parameter* ist auf 16-Bit-Werte beschränkt. Dies bedeutet, dass Listenfelder nicht mehr als 32.767 Elemente enthalten dürfen. Obwohl die Anzahl der Elemente eingeschränkt ist, ist die Gesamtgröße der Elemente in einem Listenfeld in Bytes nur durch den verfügbaren Arbeitsspeicher beschränkt.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist die Höhe der einzelnen Elemente im Listenfeld in Pixel. Der Rückgabewert ist die Höhe des Elements, das durch den *wParam-Parameter* angegeben wird, wenn das Listenfeld über das [**FORMAT LBS \_ OWNERDRAWVARIABLE verfügt.**](list-box-styles.md) Der Rückgabewert ist LB \_ ERR, wenn ein Fehler auftritt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**LB \_ SETITEMHEIGHT**](lb-setitemheight.md)
</dt> </dl>

 

 





