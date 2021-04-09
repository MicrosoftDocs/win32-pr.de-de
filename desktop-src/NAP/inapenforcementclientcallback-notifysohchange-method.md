---
title: Inapenforcementclientcallback notifysohchange-Methode (napforcementclient. h)
description: Wird von NAPAgent verwendet, um den Erzwingungs Client über SoH-Änderungen zu informieren.
ms.assetid: da8b9238-6371-4a6a-a9e7-ab791391ffc2
keywords:
- Notifysohchange-Methode NAP
- Notifysohchange-Methode NAP, inapenforcementclientcallback-Schnittstelle
- Inapenforcementclientcallback-Schnittstelle NAP, notifysohchange-Methode
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
ms.openlocfilehash: 6b405bca5ae27a68eea780dfcb922d1f986f475c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106431"
---
# <a name="inapenforcementclientcallbacknotifysohchange-method"></a>Inapenforcementclientcallback:: notifysohchange-Methode

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **inapenforcementclientcallback:: notifysohchange** -Rückruf Methode wird vom NAPAgent verwendet, um den Erzwingungs Client über SoH-Änderungen zu informieren.

## <a name="syntax"></a>Syntax


```C++
HRESULT NotifySoHChange();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Rückruf Methode muss einen der folgenden Fehlercodes zurückgeben.



| Rückgabecode                                                                                                | Beschreibung                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Gibt diesen Wert zurück, wenn der Vorgang erfolgreich ausgeführt wurde.<br/>                                                                                                                                                              |
| <dl> <dt>**RPC \_ S- \_ Server nicht \_ verfügbar**</dt> </dl> | Durch das zurückgeben dieses Werts wird der Enforcer aus der gebundenen SHA-Liste entfernt, und der entsprechende NAPAgent-Cache Eintrag, der geleert werden soll. Der fehlerhafte SHA kann dann mit dem NAPAgent erneut initialisiert werden.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Der Abschluss der systemfixinstallation ist ein System Integritäts Änderungs Ereignis. Dies bedeutet, dass Sie **notifysohchange** aufrufen müssen, wenn eine [**inapsystemhealthagentcallback:: getfixupinfo**](inapsystemhealthagentcallback-getfixupinfo-method.md) -Benachrichtigung anzeigt, dass der Client korrigiert wurde. Wenn ein Client korrigiert wird, hat der **Zustands** Member der [**fixupinfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) -Struktur, die von **getfixupinfo** zurückgegeben wurde, den Wert **fixupstaatuccess**.

Nach dem Aufrufen durch den NAPAgent über diesen Rückruf muss der Erzwingungs-Agent dann [**inapenforcementclientbinding:: getsohrequest**](inapenforcementclientbinding-getsohrequest-method.md) aufrufen, um die neue Anforderung abzurufen. Dieser Befehl kann im gleichen Thread wie **inapenforcementclientcallback:: notifysohchange** erfolgen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                      |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                |
| Header<br/>                   | <dl> <dt>Napforcementclient. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Napforcementclient. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Inapenforcementclientcallback**](inapenforcementclientcallback.md)
</dt> </dl>

 

 





