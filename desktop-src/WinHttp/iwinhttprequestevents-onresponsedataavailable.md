---
description: Tritt ein, wenn Daten aus der Antwort verfügbar sind.
ms.assetid: 62d02e3b-466a-4d3d-994b-0a1ae12049e1
title: IWinHttpRequestEvents::OnResponseDataAvailable-Ereignis
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12b55f87584164a47b47920caf961f02f0bd9cc6596c4c90f76f381027af545e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118114244"
---
# <a name="iwinhttprequesteventsonresponsedataavailable-event"></a>IWinHttpRequestEvents::OnResponseDataAvailable-Ereignis

Das **OnResponseDataAvailable-Ereignis** tritt auf, wenn Daten aus der Antwort verfügbar sind.

## <a name="syntax"></a>Syntax


```C++
void OnResponseDataAvailable(
  [in] SAFEARRAY(unsigned char) *Data
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Daten* \[ In\]
</dt> <dd>

Ein nullbasiertes Bytearray, das die von Microsoft Windows HTTP Services (WinHTTP) empfangenen Antwortdaten bis zu dem Punkt empfängt, an dem dieses Ereignis auftritt. Dies ist eine **VARIANT** vom Typ VT \_ ARRAY \| VT \_ UI1.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Da Daten in Bytes sind, müssen sie in Breitzeichen konvertiert werden, wenn sie in einer Unicode-Zeichenfolge (Breitzeichen) platziert werden.

> [!Note]  
> Informationen zu Windows XP und Windows 2000 finden Sie im Abschnitt [Laufzeitanforderungen](winhttp-start-page.md) der WinHTTP-Startseite.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows XP, Windows 2000 Professional nur mit \[ SP3-Desktop-Apps\]<br/>            |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003, Windows 2000 Server nur mit \[ SP3-Desktop-Apps\]<br/>         |
| Verteilbare Komponente<br/>          | WinHTTP 5.0 und Internet Explorer 5.01 oder höher auf Windows XP und Windows 2000.<br/> |
| Idl<br/>                      | <dl> <dt>HttpRequest.idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IWinHttpRequestEvents**](iwinhttprequestevents-interface.md)
</dt> <dt>

[**WinHttpRequest**](winhttprequest.md)
</dt> <dt>

[WinHTTP-Versionen](winhttp-versions.md)
</dt> </dl>

 

 




