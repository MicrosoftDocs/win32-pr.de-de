---
description: Wird gesendet, wenn der VMR seinen renderingmechanismus ausgewählt hat.
ms.assetid: 815d1254-c6e3-4a6c-ba4a-bf3da7d35d1f
title: EC_VMR_RENDERDEVICE_SET (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9855b23e25a2c3b955c1499b9505efffcc5637e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355943"
---
# <a name="ec_vmr_renderdevice_set"></a>auf EC \_ VMR \_ renderdevice \_ festgelegt

Wird gesendet, wenn der VMR seinen renderingmechanismus ausgewählt hat.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Kann einen der folgenden Werte aufweisen:



| Wert                        | Bedeutung                                                  |
|------------------------------|----------------------------------------------------------|
| VMR- \_ Rendering- \_ Geräte \_ Überlagerung | Die VMR wird auf die Überlagerungs Oberfläche (nur VMR-7) renderren. |
| VMR- \_ Rendering- \_ Gerät \_ vidmem  | VMR wird in den Videospeicher Rendering.                     |
| VMR- \_ Rendering- \_ Geräte- \_ sysmem  | VMR wird in den Systemspeicher (nur VMR-7).       |



 

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Nicht verwendet.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Dieses Ereignis wird von VMR-7 und VMR-9 gesendet und an Anwendungen weitergeleitet. Beachten Sie, dass VMR-9 nur Videospeicher-Renderingziele unterstützt.

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

 

 




