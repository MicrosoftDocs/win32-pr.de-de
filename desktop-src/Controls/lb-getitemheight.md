---
title: LB_GETITEMHEIGHT Meldung (Winuser. h)
description: Ruft die Höhe der Elemente in einem Listenfeld ab.
ms.assetid: ee96fce6-babd-4581-ac0e-2eb955fe543b
keywords:
- Windows-Steuerelemente für LB_GETITEMHEIGHT Meldung
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
ms.openlocfilehash: f44aa9e9b6d52c082a5f33a10280837a33372245
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858824"
---
# <a name="lb_getitemheight-message"></a>LB- \_ GetItemHeight-Nachricht

Ruft die Höhe der Elemente in einem Listenfeld ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der null basierte Index des Listenfeld Elements. Dieser Index wird nur verwendet, wenn das Listenfeld den Wert der lbs-Besitzer [**\_ drawvariable**](list-box-styles.md) aufweist, andernfalls muss er 0 (null) sein.

Windows 95/Windows 98/Windows Millennium Edition (Windows Me): der *wParam* -Parameter ist auf 16-Bit-Werte beschränkt. Dies bedeutet, dass Listenfelder nicht mehr als 32.767 Elemente enthalten dürfen. Obwohl die Anzahl der Elemente eingeschränkt ist, wird die Gesamtgröße der Elemente in einem Listenfeld in Bytes nur durch den verfügbaren Arbeitsspeicher beschränkt.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist die Höhe jedes Elements im Listenfeld in Pixel. Der Rückgabewert ist die Höhe des Elements, das durch den *wParam* -Parameter angegeben wird, wenn das Listenfeld den Wert der lbs-Besitzer [**\_ drawvariable**](list-box-styles.md) aufweist. Der Rückgabewert ist "lb err", \_ Wenn ein Fehler auftritt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**LB- \_ Größe**](lb-setitemheight.md)
</dt> </dl>

 

 





