---
title: Inapenforcementclientcallback GetConnections-Methode (napforcementclient. h)
description: Wird von NAPAgent aufgerufen und vom Erzwingungs Client implementiert, um einen Satz von Verbindungen zurückzugeben.
ms.assetid: 8f697217-5799-48e4-9f0b-715f516e48d9
keywords:
- GetConnections-Methode NAP
- GetConnections-Methode NAP, inapenforcementclientcallback-Schnittstelle
- Inapenforcementclientcallback-Schnittstelle NAP, GetConnections-Methode
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
ms.openlocfilehash: 9acdc68dbc69cabe710414f3fa2501585f3e384e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859285"
---
# <a name="inapenforcementclientcallbackgetconnections-method"></a>Inapenforcementclientcallback:: GetConnections-Methode

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **inapenforcementclientcallback:: GetConnections** -Rückruf Methode wird von NAPAgent aufgerufen und vom Erzwingungs Client implementiert, um einen Satz von Verbindungen zurückzugeben.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetConnections(
  [out] Connections **connections
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Verbindungen* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf den aktuellen Satz von verwalteten [**Verbindungen**](connections-struct.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Rückruf Methode muss einen der folgenden Fehlercodes zurückgeben.



| Rückgabecode                                                                                                | Beschreibung                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Gibt diesen Wert zurück, wenn der Vorgang erfolgreich ausgeführt wurde.<br/>                                                                                                                                                              |
| <dl> <dt>**RPC \_ S- \_ Server nicht \_ verfügbar**</dt> </dl> | Durch das zurückgeben dieses Werts wird der Enforcer aus der gebundenen SHA-Liste entfernt, und der entsprechende NAPAgent-Cache Eintrag, der geleert werden soll. Der fehlerhafte SHA kann dann mit dem NAPAgent erneut initialisiert werden.<br/> |



 

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

 

 





