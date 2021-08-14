---
title: INapEnforcementClientCallback GetConnections-Methode (NapEnforcementClient.h)
description: Wird vom NapAgent aufgerufen und vom Erzwingungsclient implementiert, um eine Reihe von Verbindungen zurück zu geben.
ms.assetid: 8f697217-5799-48e4-9f0b-715f516e48d9
keywords:
- GetConnections-Methode NAP
- GetConnections-Methode NAP, INapEnforcementClientCallback-Schnittstelle
- INapEnforcementClientCallback-Schnittstelle NAP, GetConnections-Methode
topic_type:
- apiref
api_name:
- INapEnforcementClientCallback.GetConnections
api_location:
- NapEnforcementClient.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4f6c6fdb4adc416cb25fa0e402c8fee2d8baf3270400f15a8de67966eff7a9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118134029"
---
# <a name="inapenforcementclientcallbackgetconnections-method"></a>INapEnforcementClientCallback::GetConnections-Methode

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab dem Windows 10

 

Die **INapEnforcementClientCallback::GetConnections-Rückrufmethode** wird vom NapAgent aufgerufen und vom Erzwingungsclient implementiert, um eine Reihe von Verbindungen zurück zu geben.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetConnections(
  [out] Connections **connections
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Verbindungen* \[ out\]
</dt> <dd>

Ein Zeiger auf den aktuellen Satz verwalteter [**Verbindungen.**](connections-struct.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Rückrufmethode muss einen der folgenden Fehlercodes zurückgeben.



| Rückgabecode                                                                                                | Beschreibung                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Gibt diesen Wert zurück, wenn der Vorgang erfolgreich war.<br/>                                                                                                                                                              |
| <dl> <dt>**\_ \_ RPC-S-SERVER \_ NICHT VERFÜGBAR**</dt> </dl> | Die Rückgabe dieses Werts bewirkt, dass der Erzwinger aus der Bound-SHA-Liste entfernt und der entsprechende NapAgent-Cacheeintrag geleert wird. Der fehlerhafte SHA kann sich dann mit dem NapAgent erneut initialisieren.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                |
| Header<br/>                   | <dl> <dt>NapEnforcementClient.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapEnforcementClient.idl</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**INapEnforcementClientCallback**](inapenforcementclientcallback.md)
</dt> </dl>

 

 





