---
description: Tritt ein, wenn die Antwortdaten empfangen werden.
ms.assetid: 7245725b-40dd-4282-b681-f0b2c191db94
title: IWinHttpRequestEvents::OnResponseStart-Ereignis
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cb08273bfbab92e957b932f463ce4b91ee53e3663dcd886f5e02b73698fff3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117744223"
---
# <a name="iwinhttprequesteventsonresponsestart-event"></a>IWinHttpRequestEvents::OnResponseStart-Ereignis

Das **OnResponseStart-Ereignis** tritt auf, wenn die Antwortdaten empfangen werden.

## <a name="syntax"></a>Syntax


```C++
void OnResponseStart(
  [in] long Status,
  [in] BSTR ContentType
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Status* \[ In\]
</dt> <dd>

Empfängt den Standardstatuscode, der mit den Antwortdaten zurückgegeben wird. Statuscodes werden in [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt)definiert.

</dd> <dt>

*ContentType* \[ In\]
</dt> <dd>

Gibt den Typ des empfangenen Inhalts an, z. B. "text/html" oder "image/gif".

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Verwenden Sie für dieses Ereignis [**Öffnen,**](iwinhttprequest-open.md) um eine HTTP-Verbindung im asynchronen Modus zu senden, und [**verwenden Sie Senden,**](iwinhttprequest-send.md) um eine Datenanforderung an einen Internetserver zu senden.

Dies ist das erste WinHTTP-Ereignis, das nach dem [**Senden**](iwinhttprequest-send.md)von auftritt.

> [!Note]  
> Informationen zu Windows XP und Windows 2000 finden Sie im Abschnitt [Laufzeitanforderungen](winhttp-start-page.md) der WinHTTP-Startseite.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows XP, Windows 2000 Professional nur mit \[ SP3-Desktop-Apps\]<br/>            |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003, Windows 2000 Server nur mit \[ SP3-Desktop-Apps\]<br/>         |
| Verteilbare Komponente<br/>          | WinHTTP 5.0 und Internet Explorer 5.01 oder höher auf Windows XP und Windows 2000.<br/> |
| Idl<br/>                      | <dl> <dt>HttpRequest.idl</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IWinHttpRequestEvents**](iwinhttprequestevents-interface.md)
</dt> <dt>

[**WinHttpRequest**](winhttprequest.md)
</dt> <dt>

[WinHTTP-Versionen](winhttp-versions.md)
</dt> </dl>

 

 




