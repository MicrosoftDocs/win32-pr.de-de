---
description: Die TAPI LINE \_ REQUEST-Nachricht wird gesendet, um den Eingang einer neuen Anforderung von einer anderen Anwendung zu melden.
ms.assetid: d4dbba0d-8225-48d7-a66b-b189fdae70a8
title: LINE_REQUEST Meldung (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce3cd49b14aafabfdd4d7ab37c5f2beec1487a08a53385ae8a1439b7443d49cd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126230"
---
# <a name="line_request-message"></a>LINE \_ REQUEST-Nachricht

Die TAPI **LINE \_ REQUEST-Nachricht** wird gesendet, um den Eingang einer neuen Anforderung von einer anderen Anwendung zu melden.


```C++
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hDevice* 
</dt> <dd>

Wird nicht verwendet.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Die Registrierungsinstanz der Anwendung, die in [**lineRegisterRequestRecipient**](/windows/desktop/api/Tapi/nf-tapi-lineregisterrequestrecipient)angegeben ist.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Der Anforderungsmodus der neu ausstehenden Anforderung. Dieser Parameter verwendet die [**LINEREQUESTMODE-Konstanten \_**](linerequestmode--constants.md).

</dd> <dt>

*dwParam2* 
</dt> <dd>

Die Bedingungen für diesen Parameter sind: Wenn *dwParam1* auf LINEREQUESTMODE DROP festgelegt \_ ist, enthält *dwParam2* den *hWnd* der Anwendung, die den Drop anfordert. Andernfalls wird *dwParam2* nicht verwendet.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Wenn *dwParam1* auf LINEREQUESTMODE DROP festgelegt \_ ist, enthält das Wort mit niedriger Reihenfolge von *dwParam3* die *wRequestID,* wie von der Anwendung angegeben, die die Ablage angefordert hat. Andernfalls wird *dwParam3* nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

Die **LINE \_ REQUEST-Nachricht** wird an die Anwendung mit der höchsten Priorität gesendet, die für den entsprechenden Anforderungsmodus registriert wurde. Diese Meldung gibt an, dass eine gestützte Telefonieanforderung des angegebenen Anforderungsmodus eingetroffen ist. Wenn *dwParam1* LINEREQUESTMODE \_ MAKECALL ist, kann die Anwendung [**lineGetRequest**](/windows/desktop/api/Tapi/nf-tapi-linegetrequest) mit dem entsprechenden Anforderungsmodus aufrufen, um die Anforderung zu empfangen. Wenn *dwParam1* LINEREQUESTMODE \_ DROP ist, enthält die Nachricht alle Daten, die der Anforderungsempfänger zum Ausführen der Anforderung benötigt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2.0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**lineGetRequest**](/windows/desktop/api/Tapi/nf-tapi-linegetrequest)
</dt> <dt>

[**lineRegisterRequestRecipient**](/windows/desktop/api/Tapi/nf-tapi-lineregisterrequestrecipient)
</dt> <dt>

[**tapiRequestMakeCall**](/windows/desktop/api/Tapi/nf-tapi-tapirequestmakecall)
</dt> </dl>

 

 




