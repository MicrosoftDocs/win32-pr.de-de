---
title: RB_MAXIMIZEBAND (Commctrl.h)
description: Ändern der Größe eines Bands in einem Rebar-Steuerelement in seine ideale oder größte Größe.
ms.assetid: 79fff6d0-01f2-4308-b916-38dc06dad894
keywords:
- RB_MAXIMIZEBAND von Windows-Steuerelementen
topic_type:
- apiref
api_name:
- RB_MAXIMIZEBAND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13ef02fbe9611c09d1932907c8218ffd169d3e18d10e0b07faa2b63d50058af1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119770090"
---
# <a name="rb_maximizeband-message"></a>RB \_ MAXIMIZEBAND-Meldung

Ändern der Größe eines Bands in einem Rebar-Steuerelement in seine ideale oder größte Größe.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Nullbasierter Index des zu maximierenden Bands.

</dd> <dt>

*lParam* 
</dt> <dd>

Gibt an, ob die ideale Breite des Bandes verwendet werden soll, wenn das Band maximiert ist. Wenn dieser Wert ungleich 0 (null) ist, wird die ideale Breite verwendet. Wenn dieser Wert 0 (null) ist, wird das Band so groß wie möglich.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird nicht verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Referenz**
</dt> <dt>

[**RB \_ SETBANDINFO**](rb-setbandinfo.md)
</dt> </dl>

 

 





