---
description: Wird von VMR-7 und VMR-9 gesendet, wenn eine Änderungsanforderung des dynamischen Formats vom Upstreamdecoder nicht akzeptiert werden konnte.
ms.assetid: 0c865853-2484-4833-9c92-3d6452b655f1
title: EC_VMR_RECONNECTION_FAILED (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4dae6b2735d1ae21576591055aff9dc007f447660f5c96cf13239e5f420f81f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117819960"
---
# <a name="ec_vmr_reconnection_failed"></a>\_FEHLER BEI DER WIEDERHERSTELLUNG DER EC-VMR-VERBINDUNG \_ \_

Wird von VMR-7 und VMR-9 gesendet, wenn eine Änderungsanforderung des dynamischen Formats vom Upstreamdecoder nicht akzeptiert werden konnte.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**HRESULT**) Statuscode, der von [**IPin::ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) für den Eingabepin der VMR zurückgegeben wird, bei dem die erneute Verbindung nicht hergestellt werden konnte.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Wird nicht verwendet.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Dieses Ereignis wird an Anwendungen weitergeleitet.

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

 

 




