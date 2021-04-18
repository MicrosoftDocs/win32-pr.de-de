---
title: Inapclientmanagement unregistersystemhealthagent-Methode (napmanagement. h)
description: Hebt die Registrierung eines SHA beim NAP-System auf.
ms.assetid: c3ad6f2a-c39a-4590-8487-24c802433845
keywords:
- Unregistersystemhealthagent-Methode NAP
- Unregistersystemhealthagent-Methode NAP, inapclientmanagement-Schnittstelle
- Inapclientmanagement Interface NAP, unregistersystemhealthagent-Methode
topic_type:
- apiref
api_name:
- INapClientManagement.UnregisterSystemHealthAgent
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbff7af1c279090d12883d2a4e06ee9bcc364438
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340351"
---
# <a name="inapclientmanagementunregistersystemhealthagent-method"></a>Inapclientmanagement:: unregistersystemhealthagent-Methode

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **unregistersystemhealthagent** -Methode hebt die Registrierung eines SHA beim NAP-System auf.

## <a name="syntax"></a>Syntax


```C++
HRESULT UnregisterSystemHealthAgent(
  [in] SystemHealthEntityId id
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ID* \[ in\]
</dt> <dd>

Eine [**systemhealthentityid**](nap-datatypes.md) , die den Systemintegritäts-Agent identifiziert, dessen Registrierung aufgehoben werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt einen HRESULT-Statuscode zurück, einschließlich, aber nicht beschränkt auf einen der folgenden.



| Rückgabecode                                                                                         | Beschreibung                                                        |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                | Vorgang erfolgreich.<br/>                                   |
| <dl> <dt>**E \_ AccessDenied**</dt> </dl>      | Berechtigungs Fehler, Zugriff verweigert.<br/>                       |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl>       | System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.<br/> |
| <dl> <dt>**NAP \_ E \_ trotzdem \_ gebunden**</dt> </dl> | Der SHA bleibt gebunden, und die Registrierung konnte nicht aufgehoben werden.<br/>    |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                         |
| Header<br/>                   | <dl> <dt>Napmanagement. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Napmanagement. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>        |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Inapclientmanagement**](inapclientmanagement.md)
</dt> </dl>

 

 





