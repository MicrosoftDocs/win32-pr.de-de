---
title: Inapclientmanagement registerenforcementclient-Methode (napmanagement. h)
description: Registriert einen Erzwingungs Client beim NAP-System.
ms.assetid: 26ea45ea-a366-4162-91dc-06bcd0261c56
keywords:
- Registerenforcementclient-Methode NAP
- Registerenforcementclient-Methode NAP, inapclientmanagement-Schnittstelle
- Inapclientmanagement Interface NAP, registerenforcementclient-Methode
topic_type:
- apiref
api_name:
- INapClientManagement.RegisterEnforcementClient
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc8ed4b5fe5a97d60b764341f21f25628c3c3434
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104696"
---
# <a name="inapclientmanagementregisterenforcementclient-method"></a>Inapclientmanagement:: registerenforcementclient-Methode

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Mit der **registerenforcementclient** -Methode wird ein Erzwingungs Client beim NAP-System registriert.

## <a name="syntax"></a>Syntax


```C++
HRESULT RegisterEnforcementClient(
  [in] const NapComponentRegistrationInfo *enforcer
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Enforcer* \[ in\]
</dt> <dd>

Ein Zeiger auf eine [**napcomponentregistrationinfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) -Datenstruktur, die die dem Erzwingungs Client zugeordneten Registrierungsinformationen enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt einen HRESULT-Statuscode zurück, einschließlich, aber nicht beschränkt auf einen der folgenden.



| Rückgabecode                                                                                            | Beschreibung                                                                       |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Vorgang erfolgreich.<br/>                                                  |
| <dl> <dt>**E \_ AccessDenied**</dt> </dl>         | Berechtigungs Fehler, Zugriff verweigert.<br/>                                      |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl>          | System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.<br/>                |
| <dl> <dt>**in \_ \_ Konflikt stehende \_ ID für NAP**</dt> </dl> | Ein Erzwingungs-Agent mit dem angegebenen Bezeichner ist bereits registriert.<br/> |



 

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

 

 





