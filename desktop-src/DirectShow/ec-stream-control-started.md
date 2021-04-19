---
description: Der Startbefehl für die Stream-Steuerung wurde wirksam.
ms.assetid: e2f8d9a2-c96c-457c-8a88-7c86d4405928
title: EC_STREAM_CONTROL_STARTED (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 984562fde9001de14067e5865d5583636b264852
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365982"
---
# <a name="ec_stream_control_started"></a>EC- \_ Stream- \_ Steuerelement \_

Der Startbefehl für die Stream-Steuerung wurde wirksam.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="pSender"></span><span id="psender"></span><span id="PSENDER"></span>*psender*
</dt> <dd>

(**IUnknown** \* ) Ein Zeiger auf die [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) -Schnittstelle der PIN, die den Stream gestartet hat.

</dd> <dt>

<span id="dwCookie"></span><span id="dwcookie"></span><span id="DWCOOKIE"></span>*dwCookie*
</dt> <dd>

(**DWORD**) Benutzerdefinierter Wert.

</dd> </dl>

## <a name="default-action"></a>Standardaktion

Keine.

## <a name="remarks"></a>Bemerkungen

Filter Senden dieses Ereignis als Antwort auf die [**iamstreamcontrol:: startat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat) -Methode. Diese Methode gibt eine Bezugszeit für eine PIN an, um mit dem Streaming zu beginnen. Wenn das Streaming beginnt, sendet der Filter dieses Ereignis.

Der *psender* -Parameter gibt die PIN an, die den Startbefehl ausführt. Abhängig von der Implementierung ist es möglicherweise nicht die PIN, die den [**startat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat) -Befehl empfangen hat.

Der *dwCookie* -Parameter wird von der Anwendung in der [**startat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat) -Methode angegeben. Dieser Parameter ermöglicht der Anwendung die Nachverfolgung mehrerer Aufrufe der-Methode.

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

 

 




