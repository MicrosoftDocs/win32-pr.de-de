---
description: Wird gesendet, wenn sich der Wert eines Systemparameterregisters (SPRM) ändert.
ms.assetid: 266b6de1-740d-4b3d-8487-5a9570d6c852
title: EC_DVD_SPRM_Change (Dvdevcode.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_SPRM_Change
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: e242fb17bfd80826b4bd165a2008789a2df7e478e5f526342bcbbe17ddf9d081
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119537020"
---
# <a name="ec_dvd_sprm_change"></a>EC \_ DVD \_ SPRM \_ Change

Wird gesendet, wenn sich der Wert eines Systemparameterregisters (SPRM) ändert.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Der nullbasierte Index des sprm-Werts, der geändert wurde.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Die unteren 16 Bits enthalten den neuen SPRM-Wert.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Dieses Ereignis ist standardmäßig deaktiviert. Um dieses Ereignis zu aktivieren, rufen [**Sie IDvdControl2::SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) auf, und legen Sie die **Option DVD \_ EnableLoggingEvents** auf **TRUE** fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Dvdevcode.h (include Dshow.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[DVD-Anwendungen](dvd-applications.md)
</dt> <dt>

[DVD-Ereignisbenachrichtigungscodes](dvd-notification-codes.md)
</dt> <dt>

[Ereignisbenachrichtigung in DirectShow](event-notification-in-directshow.md)
</dt> <dt>

[**IDvdInfo2::GetAllSPRMs**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getallsprms)
</dt> </dl>

 

 




