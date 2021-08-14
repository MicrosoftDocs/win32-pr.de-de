---
description: Tritt auf, wenn in der Anwendung ein Laufzeitfehler auftritt.
ms.assetid: d99400a4-3661-4162-bfd6-8c2a27e0f328
title: IWinHttpRequestEvents::OnError-Ereignis
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31127dcc3155b804bbda1c3ab94ee8a410c73f5a96c3ecfc6f787479ccd51539
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117744338"
---
# <a name="iwinhttprequesteventsonerror-event"></a>IWinHttpRequestEvents::OnError-Ereignis

Das **OnError-Ereignis** tritt auf, wenn in der Anwendung ein Laufzeitfehler auftritt.

## <a name="syntax"></a>Syntax


```C++
void OnError(
  [in] long ErrorNumber,
  [in] BSTR ErrorDescription
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ErrorNumber* \[ In\]
</dt> <dd>

Empfängt den numerischen Wert des Fehlers. Die unteren 16 Bits dieser Fehlernummer entsprechen einem der in [**Fehlermeldungen**](error-messages.md)aufgeführten Fehler.

</dd> <dt>

*ErrorDescription* \[ In\]
</dt> <dd>

Gibt eine kurze Beschreibung des aufgetretenen Fehlers an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

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

 

 




