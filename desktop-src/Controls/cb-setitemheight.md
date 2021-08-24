---
title: CB_SETITEMHEIGHT (Winuser.h)
description: Eine Anwendung sendet eine CB SETITEMHEIGHT-Nachricht, um die Höhe von Listenelementen oder das Auswahlfeld \_ in einem Kombinationsfeld fest zu legen.
ms.assetid: 25a01170-5ffc-4d86-b696-706f5375570b
keywords:
- CB_SETITEMHEIGHT meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- CB_SETITEMHEIGHT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b97e83d13e66d0a8252fdc1974c775188f8009958a3f286916b0e46ea4f0e88c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119699440"
---
# <a name="cb_setitemheight-message"></a>CB \_ SETITEMHEIGHT-Nachricht

Eine Anwendung sendet eine **CB \_ SETITEMHEIGHT-Nachricht,** um die Höhe von Listenelementen oder das Auswahlfeld in einem Kombinationsfeld fest zu legen.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt die Komponente des Kombinationsfelds an, für das die Höhe festgelegt werden soll.

Dieser Parameter muss 1 sein, um die Höhe des Auswahlfelds festlegen zu können. Es muss 0 (null) sein, um die Höhe von Listenelementen festlegen zu können, es sei denn, das Kombinationsfeld hat den [**Stil CBS \_ OWNERDRAWVARIABLE.**](combo-box-styles.md) In diesem Fall ist der *wParam-Parameter* der nullbasierte Index eines bestimmten Listenelements.

</dd> <dt>

*lParam* 
</dt> <dd>

Gibt die Höhe der Kombinationsfeldkomponente in Pixel an, die von *wParam identifiziert wird.*

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn der Index oder die Höhe ungültig ist, ist der Rückgabewert CB \_ ERR.

## <a name="remarks"></a>Hinweise

Die Höhe des Auswahlfelds in einem Kombinationsfeld wird unabhängig von der Höhe der Listenelemente festgelegt. Eine Anwendung muss sicherstellen, dass die Höhe des Auswahlfelds nicht kleiner als die Höhe eines bestimmten Listenelements ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[**CB \_ GETITEMHEIGHT**](cb-getitemheight.md)
</dt> <dt>

[**WM \_ MEASUREITEM**](wm-measureitem.md)
</dt> </dl>

 

 





