---
title: Inapclientmanagement registersystemhealthagent-Methode (napmanagement. h)
description: Registriert einen SHA beim NAP-System.
ms.assetid: 37acfd11-8282-42ba-ae02-9a45c4509b8b
keywords:
- Registersystemhealthagent-Methode NAP
- Registersystemhealthagent-Methode NAP, inapclientmanagement-Schnittstelle
- Inapclientmanagement Interface NAP, registersystemhealthagent-Methode
topic_type:
- apiref
api_name:
- INapClientManagement.RegisterSystemHealthAgent
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 581c49a117a2b8aaa2c4dda2c6573e4a6327b688
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477817"
---
# <a name="inapclientmanagementregistersystemhealthagent-method"></a>Inapclientmanagement:: registersystemhealthagent-Methode

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Mit der **registersystemhealthagent** -Methode wird ein SHA beim NAP-System registriert.

## <a name="syntax"></a>Syntax


```C++
HRESULT RegisterSystemHealthAgent(
  [in] const NapComponentRegistrationInfo *agent
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Agent* \[ in\]
</dt> <dd>

Ein Zeiger auf eine [**napcomponentregistrationinfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) -Struktur, die die Registrierungsinformationen für den SHA enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt einen HRESULT-Statuscode zurück, einschließlich, aber nicht beschränkt auf einen der folgenden.



| Rückgabecode                                                                                            | Beschreibung                                                        |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Vorgang erfolgreich.<br/>                                   |
| <dl> <dt>**E \_ AccessDenied**</dt> </dl>         | Berechtigungs Fehler, Zugriff verweigert.<br/>                       |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl>          | System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.<br/> |
| <dl> <dt>**in \_ \_ Konflikt stehende \_ ID für NAP**</dt> </dl> | Ein SHA, der diese ID verwendet, ist bereits registriert.<br/>         |



 

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

 

 





