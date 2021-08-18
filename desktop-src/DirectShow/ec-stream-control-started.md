---
description: Ein Startbefehl für das Streamsteuersteuersystem ist wirksam.
ms.assetid: e2f8d9a2-c96c-457c-8a88-7c86d4405928
title: EC_STREAM_CONTROL_STARTED (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73af8d39c3dae0447600a23dcb00483f4e0da6b81bc7ba6ab4a7e8b5f7afa42d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119997890"
---
# <a name="ec_stream_control_started"></a>EC \_ STREAM CONTROL STARTED \_ (EC STREAM-STEUERELEMENT \_ GESTARTET)

Ein Startbefehl für das Streamsteuersteuersystem ist wirksam.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="pSender"></span><span id="psender"></span><span id="PSENDER"></span>*pSender*
</dt> <dd>

(**IUnknown** \* ) Zeiger auf die [**IPin-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ipin) des Pins, der den Stream gestartet hat.

</dd> <dt>

<span id="dwCookie"></span><span id="dwcookie"></span><span id="DWCOOKIE"></span>*dwCookie*
</dt> <dd>

(**DWORD**) Benutzerdefinierter Wert.

</dd> </dl>

## <a name="default-action"></a>Standardaktion

Keine.

## <a name="remarks"></a>Hinweise

Filter senden dieses Ereignis als Antwort auf die [**IAMStreamControl::StartAt-Methode.**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat) Diese Methode gibt eine Bezugszeit an, zu der ein Pin mit dem Streaming beginnt. Wenn das Streaming beginnt, sendet der Filter dieses Ereignis.

Der *pSender-Parameter* gibt den Pin an, der den Startbefehl ausgibt. Je nach Implementierung ist es möglicherweise nicht der Pin, der den [**StartAt-Aufruf empfangen**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat) hat.

Der *dwCookie-Parameter* wird von der Anwendung in der [**StartAt-Methode**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat) angegeben. Mit diesem Parameter kann die Anwendung mehrere Aufrufe der -Methode nachverfolgen.

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

 

 




