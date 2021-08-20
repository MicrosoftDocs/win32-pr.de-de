---
title: INapSystemHealthAgentCallback GetSoHRequest-Methode (NapSystemHealthAgent.h)
description: Wird vom NapAgent aufgerufen, um die SoH-Anforderung des Systemzustands-Agents abfragt.
ms.assetid: 4161a3e7-2f7a-40d1-b973-47f991bba5d0
keywords:
- GetSoHRequest-Methode NAP
- GetSoHRequest-Methode NAP, INapSystemHealthAgentCallback-Schnittstelle
- INapSystemHealthAgentCallback-Schnittstelle NAP, GetSoHRequest-Methode
topic_type:
- apiref
api_name:
- INapSystemHealthAgentCallback.GetSoHRequest
api_location:
- NapSystemHealthAgent.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6c9203a782be34be66e84fa8238a678647a4359df8cde3408aa8de99e73fcce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118133769"
---
# <a name="inapsystemhealthagentcallbackgetsohrequest-method"></a>INapSystemHealthAgentCallback::GetSoHRequest-Methode

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab dem Windows 10

 

Die **INapSystemHealthAgentCallback::GetSoHRequest-Methode** wird vom NapAgent aufgerufen, um die SoH-Anforderung des Systemzustands-Agents abfragt.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetSoHRequest(
  [in] INapSystemHealthAgentRequest *request
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Anforderung* \[ In\]
</dt> <dd>

Ein COM-Zeiger auf ein [**INapSystemHealthAgentRequest-Objekt,**](inapsystemhealthagentrequest.md) das das Anforderungsobjekt identifiziert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert



| Rückgabecode                                                                                                                      | Beschreibung                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                             | Gibt die erfolgreiche Ausführung an.<br/>                                                                                                                      |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32 \_ (RPC-SERVER NICHT \_ \_ VERFÜGBAR)**</dt> </dl> | Wenn dieser Code von Ihrer Implementierung zurückgegeben wird, entfernt der NapAgent den SHA aus der Bound-SHA-Liste und leert seinen Cacheeintrag.<br/> |



 

Wenn ein Rückgabewert (mit Ausnahme **von HRESULT \_ FROM \_ WIN32 (RPC \_ S SERVER \_ \_ UNAVAILABLE) )** von Ihrer Implementierung zurückgegeben wird, erstellt das NAP-System eine [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) und gibt sie an die entsprechende SHV mit den folgenden Attributtypen und Werten zurück:

-   [**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md)= <id>
-   [**sohAttributeTypeFailureCategory**](sohattributetype-enum.md) =  [ **failureCategoryClientComponent**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)
-   [**sohAttributeTypeErrorCodes**](sohattributetype-enum.md) = <fehlercode->

## <a name="remarks"></a>Hinweise

Diese Rückrufmethode wird vom NAP-System deklariert und muss vom SHA-Writer implementiert werden.

Diese Methode muss die Anforderung verarbeiten und sofort zurückgeben. Das Verzögern der Rückgabe dieser Methode wirkt sich negativ auf die Leistung und Reaktionsfähigkeit des Systems aus und kann dazu führen, dass für andere Teile des Betriebssystems ein Time out auftritt.

Die Überwachung des Integritätszustands sollte nicht im Rahmen dieses Aufrufs durchgeführt werden, insbesondere wenn sie rechenintensiv ist und lange dauert. Integritätszustandsüberwachung und SoH-Berechnung sollten in einem separaten Thread oder Dienst ausgeführt werden. Die einzige Funktion dieser Methode sollte sein, den SOH-Wert und die Rückgabe des SHA-Werts zu setzen.

Wenn es lange dauern wird, bis der SHA einen SoH generiert, sollte der zwischengespeicherte SoH an den NapAgent zurückgegeben werden. Wenn kein zwischengespeicherter SoH-Wert vorhanden ist, sollte der SHA sofort einen SoH mit den folgenden Attributtypen und Werten zurückgeben:

-   [**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md)= <id>
-   [**sohAttributeTypeFailureCategory**](sohattributetype-enum.md) =  [ **failureCategoryClientCommunication**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)
-   [**sohAttributeTypeErrorCodes**](sohattributetype-enum.md)  =  [ **NAP \_ E NO \_ \_ CACHED \_ SOH**](nap-error-constants.md)

Wenn der SoH generiert wurde, muss der SHA [**INapSystemHealthAgentBinding::NotifySoHChange**](inapsystemhealthagentbinding-notifysohchange-method.md) aufrufen, um napAgent über die Systemzustandsänderung zu benachrichtigen.

Der NapAgent ruft diese Methode auf, um soHRequest des System health-Agents abfragt. Der SHA kann das übergebene [**INapSystemHealthAgentRequest-Objekt**](inapsystemhealthagentrequest.md) nach Parametern abfragen, die zum Berechnen von SoHRequest benötigt werden. Der SHA muss die berechnete SoHRequest für das Anforderungsobjekt festlegen. Der SHA darf keine Verweise auf das Anforderungsobjekt besitzen, nachdem dieser Aufruf abgeschlossen wurde.

Wenn diese Methode aufgerufen wird und ein SoH im Cache des NapAgent vorhanden ist, wird sie für das Anforderungsobjekt festgelegt. Der SHA kann ihn mit **GetSoHRequest abfragen.** Wenn der SHA keinen neuen SoH-Wert festgelegt, wird der zwischengespeicherte soH verwendet.

Für ungebundene SHAs, die beim System registriert sind, erstellt und sendet das NAP-System eine SoHRequest mit den folgenden Attributtypen und Werten an die entsprechende SHV:

-   [**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md)= <id>
-   [**sohAttributeTypeFailureCategory**](sohattributetype-enum.md) =  [ **failureCategoryClientComponent**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)
-   [**sohAttributeTypeErrorCodes**](sohattributetype-enum.md)  =  [ **NAP \_ E NICHT \_ \_ INITIALISIERT**](nap-error-constants.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                |
| Header<br/>                   | <dl> <dt>NapSystemHealthAgent.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapSystemHealthAgent.idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**INapSystemHealthAgentCallback**](inapsystemhealthagentcallback.md)
</dt> </dl>

 

 





