---
description: Die TAPI-Zeilen \_ Anforderungs Nachricht wird gesendet, um den Eingang einer neuen Anforderung von einer anderen Anwendung zu melden.
ms.assetid: d4dbba0d-8225-48d7-a66b-b189fdae70a8
title: LINE_REQUEST Meldung (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23987e370d5ae9c8eeb579780c5659f8075ac865
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356410"
---
# <a name="line_request-message"></a>Zeilen \_ Anforderungs Nachricht

Die TAPI- **Zeilen \_ Anforderungs** Nachricht wird gesendet, um den Eingang einer neuen Anforderung von einer anderen Anwendung zu melden.


```C++
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hdevice* 
</dt> <dd>

Nicht verwendet.

</dd> <dt>

*dwcallbackinstance* 
</dt> <dd>

Die Registrierungs Instanz der Anwendung, die auf [**lineregisterrequestrecipient**](/windows/desktop/api/Tapi/nf-tapi-lineregisterrequestrecipient)angegeben ist.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Der Anforderungs Modus der neu ausstehenden Anforderung. Dieser Parameter verwendet die [**linerequestmode- \_ Konstanten**](linerequestmode--constants.md).

</dd> <dt>

*dwParam2* 
</dt> <dd>

Die Bedingungen für diesen Parameter lauten, wenn *dwParam1* auf linerequestmode Drop festgelegt ist \_ , *dwParam2* enthält das *HWND* der Anwendung, die den Löschvorgang anfordert. Andernfalls wird *dwParam2* nicht verwendet.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Wenn *dwParam1* auf linerequestmode Drop festgelegt ist \_ , enthält das nieder wertige Wort von *dwParam3* die *wrequestid* , wie von der Anwendung angegeben, die den Löschvorgang angefordert hat. Andernfalls wird *dwParam3* nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Die **Zeilen \_ Anforderungs** Nachricht wird an die Anwendung mit der höchsten Priorität gesendet, die sich für den entsprechenden Anforderungs Modus registriert hat. Diese Meldung gibt den Eingang einer unterstützten Telefonieanforderung im angegebenen Anforderungs Modus an. Wenn *dwParam1* linerequestmode \_ MakeCall ist, kann die Anwendung [**linegetrequest**](/windows/desktop/api/Tapi/nf-tapi-linegetrequest) mithilfe des entsprechenden Anforderungs Modus aufrufen, um die Anforderung zu empfangen. Wenn *dwParam1* auf linerequestmode \_ Drop gesetzt ist, enthält die Meldung alle Daten, die der Anforderungs Empfänger benötigt, um die Anforderung auszuführen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2,0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**linegetrequest**](/windows/desktop/api/Tapi/nf-tapi-linegetrequest)
</dt> <dt>

[**lineregisterrequestrecipient**](/windows/desktop/api/Tapi/nf-tapi-lineregisterrequestrecipient)
</dt> <dt>

[**tapirequestmakecall**](/windows/desktop/api/Tapi/nf-tapi-tapirequestmakecall)
</dt> </dl>

 

 




