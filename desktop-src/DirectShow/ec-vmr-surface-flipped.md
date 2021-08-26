---
description: Wird gesendet, wenn der Zuweisungsbeteiliger von VMR-7 die DirectDraw Flip-Methode auf der dargestellten Oberfläche aufgerufen hat. Dadurch kann der VMR seine DirectXVA-Tabelle mit Oberflächen mit der Flippingkette von DirectDraw synchronisieren.
ms.assetid: e298857b-0579-48b4-add0-72320bc52d63
title: EC_VMR_SURFACE_FLIPPED (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02c352af01ee31728b41aa276d14ca64b7c3fa6770bb4c9328a8c4ee5e91bb07
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043350"
---
# <a name="ec_vmr_surface_flipped"></a>\_EC-VMR-OBERFLÄCHE \_ \_ GEKIPPT

Wird gesendet, wenn der Zuweisungsbeteiliger von VMR-7 die DirectDraw Flip-Methode auf der dargestellten Oberfläche aufgerufen hat. Dadurch kann der VMR seine DirectXVA-Tabelle mit Oberflächen mit der Flippingkette von DirectDraw synchronisieren.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**HRESULT**) Statuscode, der von der DirectDraw Flip-Methode zurückgegeben wird.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Wird nicht verwendet.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Benutzerdefinierte Allocator-Presenter für VMR-7 sollten dieses Ereignis senden. Dieses Ereignis wird nicht an Anwendungen weitergeleitet und nicht mit Allocator-Presentern für VMR-9 verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Dshow.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Ereignisbenachrichtigungscodes](event-notification-codes.md)
</dt> <dt>

[Ereignisbenachrichtigung in DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




