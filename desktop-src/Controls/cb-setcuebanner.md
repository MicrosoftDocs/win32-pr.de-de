---
title: CB_SETCUEBANNER Meldung (Winuser.h)
description: Legt den Text des Cue-Banners fest, der für das Bearbeitungssteuerelement eines Kombinationsfelds angezeigt wird.
ms.assetid: 4b2b5042-ba64-4e3f-adeb-9aea66773b0e
keywords:
- CB_SETCUEBANNER Windows-Steuerelementen
topic_type:
- apiref
api_name:
- CB_SETCUEBANNER
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb546b7113247f09d8929364984d5e73c3e28b6541d2ca04bd631405040bf6fb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089040"
---
# <a name="cb_setcuebanner-message"></a>CB \_ SETCUEBANNER-Nachricht

Legt den Text des Cue-Banners fest, der für das Bearbeitungssteuerelement eines Kombinationsfelds angezeigt wird.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Muss Null sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf einen mit NULL endenden Unicode-Zeichenfolgenpuffer, der den Text enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 1 zurück, andernfalls einen Fehlerwert.

## <a name="remarks"></a>Hinweise

Das Hinweisbanner ist Text, der im Bearbeitungssteuerelement eines Kombinationsfelds angezeigt wird, wenn keine Auswahl vorhanden ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>CommCtrl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Kombinationsfeldfeatures](combo-box-features.md)
</dt> </dl>

 

 





