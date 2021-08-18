---
description: Tritt ein, wenn die Antwortdaten abgeschlossen sind.
ms.assetid: 0df2031e-826f-436e-a689-201fa8b5c38f
title: IWinHttpRequestEvents::OnResponseFinished-Ereignis
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2114135c17f3e2eb2f9d60a7044f7441271f257fe099de31ea70c6030de769df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117744250"
---
# <a name="iwinhttprequesteventsonresponsefinished-event"></a>IWinHttpRequestEvents::OnResponseFinished-Ereignis

Das **OnResponseFinished-Ereignis** tritt auf, wenn die Antwortdaten abgeschlossen sind.

## <a name="syntax"></a>Syntax


```C++
void OnResponseFinished();
```



## <a name="parameters"></a>Parameter

Dieses Ereignis verfügt über keine Parameter.

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Dieses Ereignis signalisiert, dass alle Antwortdaten, die sich auf die letzte Anforderung beziehen, empfangen wurden. [**OnResponseDataAvailable**](iwinhttprequestevents-onresponsedataavailable.md) tritt erst bei der nächsten Anforderung erneut auf.

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

 

 




