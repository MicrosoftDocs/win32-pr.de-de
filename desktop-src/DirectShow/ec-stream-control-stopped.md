---
description: Ein Befehl zum Beenden der Streamsteuerung ist wirksam.
ms.assetid: a2f7a959-fafd-47ff-9b3d-1a898fdb1f81
title: EC_STREAM_CONTROL_STOPPED (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69884ecc573b2bb775092529cb81e1b33a1514d4799af9f55c7bcebb5ebd2b24
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928420"
---
# <a name="ec_stream_control_stopped"></a>EC \_ STREAM \_ CONTROL \_ STOPPED

Ein Befehl zum Beenden der Streamsteuerung ist wirksam.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="pSender"></span><span id="psender"></span><span id="PSENDER"></span>*pSender*
</dt> <dd>

(**IUnknown** \* ) Zeiger auf die [**IPin-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ipin) des Pins, der den Stream beendet hat.

</dd> <dt>

<span id="dwCookie"></span><span id="dwcookie"></span><span id="DWCOOKIE"></span>*dwCookie*
</dt> <dd>

(**DWORD**) Benutzerdefinierter Wert.

</dd> </dl>

## <a name="default-action"></a>Standardaktion

Keine.

## <a name="remarks"></a>Hinweise

Filter senden dieses Ereignis als Antwort auf die [**IAMStreamControl::StopAt-Methode.**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-stopat) Die **StopAt-Methode** gibt eine Referenzzeit für einen Pin an, um das Streaming zu beenden. Wenn das Streaming nicht mehr funktioniert, sendet der Filter dieses Ereignis.

Der *pSender-Parameter* gibt den Pin an, der den Stop-Befehl ausgibt. Je nach Implementierung ist es möglicherweise nicht der Pin, der den [**StopAt-Aufruf empfangen**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-stopat) hat.

Der *dwCookie-Parameter* wird von der Anwendung in der [**StopAt-Methode**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-stopat) angegeben. Mit diesem Parameter kann die Anwendung mehrere Aufrufe der -Methode nachverfolgen.

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

 

 




