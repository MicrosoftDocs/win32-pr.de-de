---
title: INapServerManagement RegisterSystemHealthValidator-Methode (NapServerManagement.h)
description: Registriert eine SHV.
ms.assetid: 23f147d5-3c4e-48ca-940a-c4350ad6ecb3
keywords:
- RegisterSystemHealthValidator-Methode NAP
- RegisterSystemHealthValidator-Methode NAP, INapServerManagement-Schnittstelle
- INapServerManagement-Schnittstelle NAP , RegisterSystemHealthValidator-Methode
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
ms.openlocfilehash: bdb5dc93c5bb927ffb25df20f37e5b2c30560153efb006f3c91bf7e97efec360
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012568"
---
# <a name="inapservermanagementregistersystemhealthvalidator-method"></a>INapServerManagement::RegisterSystemHealthValidator-Methode

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **INapServerManagement::RegisterSystemHealthValidator-Methode** registriert eine SHV.

## <a name="syntax"></a>Syntax


```C++
HRESULT RegisterSystemHealthValidator(
  [in] const NapComponentRegistrationInfo *validator,
  [in] const CLSID                        *validatorClsid
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Validierungszeichen* \[ In\]
</dt> <dd>

Ein Zeiger auf eine [**NapComponentRegistrationInfo-Struktur,**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) die die SHV-Registrierungsinformationen enthält.

</dd> <dt>

*validatorClsid* \[ In\]
</dt> <dd>

Ein Zeiger auf die CLSID der COM-Klasse, die die [**INapSystemHealthValidator-Schnittstelle**](inapsystemhealthvalidator.md) implementiert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Andere COM-spezifische Fehlercodes können ebenfalls zurückgegeben werden.



| Rückgabecode                                                                                            | Beschreibung                                                        |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Vorgang erfolgreich.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>        | Berechtigungsfehler, Zugriff verweigert.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>         | Systemressourcenlimit, konnte den Vorgang nicht ausführen.<br/> |
| <dl> <dt>**IN \_ \_ KONFLIKTSTEHENDE \_ NAP E-ID**</dt> </dl> | Die SHV-ID ist bereits registriert.<br/>                           |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                               |
| Header<br/>                   | <dl> <dt>NapServerManagement.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapServerManagement.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qsvrmgmt.dll</dt> </dl>            |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**INapServerManagement**](inapservermanagement.md)
</dt> </dl>

 

 





