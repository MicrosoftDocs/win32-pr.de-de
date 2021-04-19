---
description: Ein Befehl zum Abbrechen der Stream-Steuerung wurde wirksam.
ms.assetid: a2f7a959-fafd-47ff-9b3d-1a898fdb1f81
title: EC_STREAM_CONTROL_STOPPED (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8c5488ba400d90623955c3e9adcba0dde07e04a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356430"
---
# <a name="ec_stream_control_stopped"></a>EC- \_ Stream- \_ Steuerelement \_ beendet

Ein Befehl zum Abbrechen der Stream-Steuerung wurde wirksam.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="pSender"></span><span id="psender"></span><span id="PSENDER"></span>*psender*
</dt> <dd>

(**IUnknown** \* ) Ein Zeiger auf die [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) -Schnittstelle der PIN, die den Stream beendet hat.

</dd> <dt>

<span id="dwCookie"></span><span id="dwcookie"></span><span id="DWCOOKIE"></span>*dwCookie*
</dt> <dd>

(**DWORD**) Benutzerdefinierter Wert.

</dd> </dl>

## <a name="default-action"></a>Standardaktion

Keine.

## <a name="remarks"></a>Bemerkungen

Filter Senden dieses Ereignis als Antwort auf die [**iamstreamcontrol:: STOPAT**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-stopat) -Methode. Die **STOPAT** -Methode gibt eine Bezugszeit für eine PIN zum Beenden des Streamings an. Wenn das Streaming angehalten wird, sendet der Filter dieses Ereignis.

Der *psender* -Parameter gibt die PIN an, mit der der Befehl zum Abbrechen ausgeführt wird. Abhängig von der Implementierung ist es möglicherweise nicht die PIN, die den [**Stop at**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-stopat) -Befehl empfangen hat.

Der *dwCookie* -Parameter wird von der Anwendung in der [**STOPAT**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-stopat) -Methode angegeben. Dieser Parameter ermöglicht der Anwendung die Nachverfolgung mehrerer Aufrufe der-Methode.

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

 

 




