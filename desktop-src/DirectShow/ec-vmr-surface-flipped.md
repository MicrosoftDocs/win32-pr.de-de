---
description: Wird gesendet, wenn der zuordnerpräsentator von VMR-7Die DirectDraw-Flip-Methode auf der dargestellten Oberfläche aufgerufen hat. Dadurch kann der VMR seine directxva-Tabelle der Oberflächen mit der DirectDraw-flippingkette synchronisieren.
ms.assetid: e298857b-0579-48b4-add0-72320bc52d63
title: EC_VMR_SURFACE_FLIPPED (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1feafaa58f0cacdafde04591d494dbb9a9eb258e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373826"
---
# <a name="ec_vmr_surface_flipped"></a>EC- \_ VMR- \_ Oberfläche \_ gekippt

Wird gesendet, wenn der zuordnerpräsentator von VMR-7Die DirectDraw-Flip-Methode auf der dargestellten Oberfläche aufgerufen hat. Dadurch kann der VMR seine directxva-Tabelle der Oberflächen mit der DirectDraw-flippingkette synchronisieren.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**HRESULT**) Der von der DirectDraw-Flip-Methode zurückgegebene Status Code.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Nicht verwendet.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Benutzerdefinierte Zuweisung: Presenter für VMR-7 sollte dieses Ereignis senden. Dieses Ereignis wird nicht an Anwendungen weitergeleitet und wird nicht mit "zuordcator-Presenter" für VMR-9 verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Ereignis Benachrichtigungs Codes](event-notification-codes.md)
</dt> <dt>

[Ereignis Benachrichtigung in DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




