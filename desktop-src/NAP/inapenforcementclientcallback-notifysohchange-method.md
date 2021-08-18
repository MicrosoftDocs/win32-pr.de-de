---
title: INapEnforcementClientCallback NotifySoHChange-Methode (NapEnforcementClient.h)
description: Wird vom NapAgent verwendet, um den Erzwingungsclient über SoH-Änderungen zu informieren.
ms.assetid: da8b9238-6371-4a6a-a9e7-ab791391ffc2
keywords:
- NotifySoHChange-Methode NAP
- NotifySoHChange-Methode NAP, INapEnforcementClientCallback-Schnittstelle
- INapEnforcementClientCallback-Schnittstelle NAP , NotifySoHChange-Methode
topic_type:
- apiref
api_name:
- INapEnforcementClientCallback.NotifySoHChange
api_location:
- NapEnforcementClient.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9011db09b698f886bd10ad19298a104668d038cc2bb11136b6e4ac58035e3425
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118940134"
---
# <a name="inapenforcementclientcallbacknotifysohchange-method"></a>INapEnforcementClientCallback::NotifySoHChange-Methode

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **Rückrufmethode INapEnforcementClientCallback::NotifySoHChange** wird vom NapAgent verwendet, um den Erzwingungsclient über SoH-Änderungen zu informieren.

## <a name="syntax"></a>Syntax


```C++
HRESULT NotifySoHChange();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Rückrufmethode muss einen der folgenden Fehlercodes zurückgeben.



| Rückgabecode                                                                                                | Beschreibung                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Gibt diesen Wert zurück, wenn der Vorgang erfolgreich war.<br/>                                                                                                                                                              |
| <dl> <dt>**\_ \_ RPC-S-SERVER \_ NICHT VERFÜGBAR**</dt> </dl> | Die Rückgabe dieses Werts bewirkt, dass der Enforcer aus der Bound-SHA-Liste entfernt und der entsprechende NapAgent-Cacheeintrag geleert wird. Der fehlerhafte SHA kann sich dann mit dem NapAgent erneut initialisieren.<br/> |



 

## <a name="remarks"></a>Hinweise

Der Abschluss der Systemkorrektur ist ein Systemzustandsänderungsereignis. Das bedeutet, dass Sie **NotifySoHChange** aufrufen müssen, wenn eine [**INapSystemHealthAgentCallback::GetFixupInfo-Benachrichtigung**](inapsystemhealthagentcallback-getfixupinfo-method.md) angibt, dass der Client korrigiert wurde. Wenn ein Client korrigiert wird, weist der **Zustandsmember** der von **GetFixupInfo** zurückgegebenen [**FixupInfo-Struktur**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) den Wert **fixupStateSuccess auf.**

Nach dem Aufruf durch den NapAgent über diesen Rückruf muss der Erzwingungs-Agent dann [**INapEnforcementClientBinding::GetSoHRequest**](inapenforcementclientbinding-getsohrequest-method.md) aufrufen, um die neue Anforderung abzurufen. Dieser Aufruf kann im gleichen Thread wie **INapEnforcementClientCallback::NotifySoHChange** erfolgen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                |
| Header<br/>                   | <dl> <dt>NapEnforcementClient.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapEnforcementClient.idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**INapEnforcementClientCallback**](inapenforcementclientcallback.md)
</dt> </dl>

 

 





