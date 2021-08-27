---
title: CB_GETITEMHEIGHT Meldung (Winuser.h)
description: Bestimmt die Höhe von Listenelementen oder des Auswahlfelds in einem Kombinationsfeld.
ms.assetid: 72fba6ca-0a51-4801-bd45-5f5a7d5ebee2
keywords:
- CB_GETITEMHEIGHT Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- CB_GETITEMHEIGHT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6e3ad9636c32e40bfa95f1f3b2c209eab42023205e0a967cc91804ec314a103
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089190"
---
# <a name="cb_getitemheight-message"></a>CB \_ GETITEMHEIGHT-Nachricht

Bestimmt die Höhe von Listenelementen oder des Auswahlfelds in einem Kombinationsfeld.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Die Kombinationsfeldkomponente, deren Höhe abgerufen werden soll. Dieser Parameter muss -1 sein, um die Höhe des Auswahlfelds abzurufen. Es muss 0 (null) sein, um die Höhe von Listenelementen abzurufen, es sei denn, das Kombinationsfeld weist den [**CBS \_ OWNERDRAWVARIABLE-Stil**](combo-box-styles.md) auf. In diesem Fall ist der *wParam-Parameter* der nullbasierte Index eines bestimmten Listenelements.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist die Höhe der Listenelemente in einem Kombinationsfeld in Pixel. Wenn das Kombinationsfeld den [**CBS \_ OWNERDRAWVARIABLE-Stil**](combo-box-styles.md) auf hat, ist dies die Höhe des Elements, das durch den *wParam-Parameter* angegeben wird. Wenn *wParam* -1 ist, entspricht der Rückgabewert der Höhe des Bearbeitungssteuerelements (oder des statischen Texts) des Kombinationsfelds. Wenn ein Fehler auftritt, lautet der Rückgabewert CB \_ ERR.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[**CB \_ SETITEMHEIGHT**](cb-setitemheight.md)
</dt> <dt>

[**WM \_ MEASUREITEM**](wm-measureitem.md)
</dt> </dl>

 

 





