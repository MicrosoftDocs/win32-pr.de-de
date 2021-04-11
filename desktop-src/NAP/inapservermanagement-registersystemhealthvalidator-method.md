---
title: Inapservermanagement registersystemhealthvalidator-Methode (napservermanagement. h)
description: Registriert einen SHV.
ms.assetid: 23f147d5-3c4e-48ca-940a-c4350ad6ecb3
keywords:
- Registersystemhealthvalidator-Methode NAP
- Registersystemhealthvalidator-Methode NAP, inapservermanagement-Schnittstelle
- Inapservermanagement-Schnittstelle NAP, registersystemhealthvalidator-Methode
topic_type:
- apiref
api_name:
- INapServerManagement.RegisterSystemHealthValidator
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2abd8d42da196caa804a8919c6425fda9fcb950c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104213753"
---
# <a name="inapservermanagementregistersystemhealthvalidator-method"></a>Inapservermanagement:: registersystemhealthvalidator-Methode

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **inapservermanagement:: registersystemhealthvalidator** -Methode registriert einen SHV.

## <a name="syntax"></a>Syntax


```C++
HRESULT RegisterSystemHealthValidator(
  [in] const NapComponentRegistrationInfo *validator,
  [in] const CLSID                        *validatorClsid
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Validierungs Steuerelement* \[ in\]
</dt> <dd>

Ein Zeiger auf eine [**napcomponentregistrationinfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) -Struktur, die die SHV-Registrierungsinformationen enthält.

</dd> <dt>

*validatorclsid* \[ in\]
</dt> <dd>

Ein Zeiger auf die CLSID der com-Klasse, die die [**inapsystemhealthvalidator**](inapsystemhealthvalidator.md) -Schnittstelle implementiert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.



| Rückgabecode                                                                                            | Beschreibung                                                        |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Vorgang erfolgreich.<br/>                                    |
| <dl> <dt>**E \_ Access verweigert**</dt> </dl>        | Berechtigungs Fehler, Zugriff verweigert.<br/>                       |
| <dl> <dt>**E \_ Outo-Memory**</dt> </dl>         | System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.<br/> |
| <dl> <dt>**in \_ \_ Konflikt stehende \_ ID für NAP**</dt> </dl> | Die SHV-ID ist bereits registriert.<br/>                           |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                               |
| Header<br/>                   | <dl> <dt>Napservermanagement. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Napservermanagement. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qsvrmgmt.dll</dt> </dl>            |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Inapservermanagement**](inapservermanagement.md)
</dt> </dl>

 

 





