---
title: Inapclientmanagement unregisterenforcementclient-Methode (napmanagement. h)
description: Hebt die Registrierung eines Erzwingungs Clients beim NAP-System auf.
ms.assetid: 549683de-7f2c-4da6-9616-862e0e99d21f
keywords:
- Unregisterenforcementclient-Methode NAP
- Unregisterenforcementclient-Methode NAP, inapclientmanagement-Schnittstelle
- Inapclientmanagement Interface NAP, unregisterenforcementclient-Methode
topic_type:
- apiref
api_name:
- INapClientManagement.UnregisterEnforcementClient
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea318cf632ac00d54451b11428907c88159809df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104691"
---
# <a name="inapclientmanagementunregisterenforcementclient-method"></a>Inapclientmanagement:: unregisterenforcementclient-Methode

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Durch die **unregisterenforcementclient** -Methode wird die Registrierung eines Erzwingungs Clients beim NAP-System aufgehoben.

## <a name="syntax"></a>Syntax


```C++
HRESULT UnregisterEnforcementClient(
  [in] EnforcementEntityId id
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ID* \[ in\]
</dt> <dd>

Ein [**enforcemententityid**](nap-datatypes.md) -Wert, der den Erzwingungs Client für die Aufhebung der Registrierung identifiziert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt einen HRESULT-Statuscode zurück, einschließlich, aber nicht beschränkt auf einen der folgenden.



| Rückgabecode                                                                                         | Beschreibung                                                                    |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                | Vorgang erfolgreich.<br/>                                               |
| <dl> <dt>**E \_ AccessDenied**</dt> </dl>      | Berechtigungs Fehler, Zugriff verweigert.<br/>                                   |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl>       | System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.<br/>             |
| <dl> <dt>**NAP \_ E \_ trotzdem \_ gebunden**</dt> </dl> | Die Registrierung des Erzwingungs Clients konnte nicht aufgehoben werden, und bleibt unverändert.<br/> |



 

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

 

 





