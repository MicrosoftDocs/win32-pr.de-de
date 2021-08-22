---
description: Wird gesendet, wenn die VMR ihren Renderingmechanismus ausgewählt hat.
ms.assetid: 815d1254-c6e3-4a6c-ba4a-bf3da7d35d1f
title: EC_VMR_RENDERDEVICE_SET (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc2c8bef78156c4438e1e4e7aea45326562002ed8f4a3786377d7ee43a00a57c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015858"
---
# <a name="ec_vmr_renderdevice_set"></a>EC \_ VMR \_ RENDERDEVICE \_ SET

Wird gesendet, wenn die VMR ihren Renderingmechanismus ausgewählt hat.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Kann einer der folgenden Werte sein:



| Wert                        | Bedeutung                                                  |
|------------------------------|----------------------------------------------------------|
| VMR \_ RENDER \_ DEVICE \_ OVERLAY | Die VMR wird auf der Überlagerungsoberfläche gerendert (nur VMR-7). |
| VMR \_ RENDER \_ DEVICE \_ VIDMEM  | Die VMR wird in den Videospeicher gerendert.                     |
| \_VMR-RENDERGERÄT \_ \_ SYSMEM  | Die VMR wird in den Systemspeicher gerendert (nur VMR-7).       |



 

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Wird nicht verwendet.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Dieses Ereignis wird sowohl von VMR-7 als auch von VMR-9 gesendet und an Anwendungen weitergeleitet. Beachten Sie, dass VMR-9 nur Renderziele für den Videospeicher unterstützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Dshow.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Ereignisbenachrichtigungscodes](event-notification-codes.md)
</dt> <dt>

[Ereignisbenachrichtigung in DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




