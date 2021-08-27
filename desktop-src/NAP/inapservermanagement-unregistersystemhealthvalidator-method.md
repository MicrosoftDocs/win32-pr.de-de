---
title: INapServerManagement UnregisterSystemHealthValidator-Methode (NapServerManagement.h)
description: Wird zum Aufheben der Registrierung einer SHV beim NAP-Server verwendet.
ms.assetid: f4148df1-a230-4845-ac8b-9e04be9e0d6c
keywords:
- UnregisterSystemHealthValidator-Methode NAP
- UnregisterSystemHealthValidator-Methode NAP, INapServerManagement-Schnittstelle
- INapServerManagement-Schnittstelle NAP, UnregisterSystemHealthValidator-Methode
topic_type:
- apiref
api_name:
- INapServerManagement.UnregisterSystemHealthValidator
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 116bcf2d2eec17389cf230bf0a1ad24ba386d2a6e35872570efda092e5992869
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037830"
---
# <a name="inapservermanagementunregistersystemhealthvalidator-method"></a>INapServerManagement::UnregisterSystemHealthValidator-Methode

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab dem Windows 10

 

Mit **der INapServerManagement::UnregisterSystemHealthValidator-Methode** wird die Registrierung einer SHV beim NAP-Server aufgehoben.

## <a name="syntax"></a>Syntax


```C++
HRESULT UnregisterSystemHealthValidator(
  [in] SystemHealthEntityId id
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*id* \[ in\]
</dt> <dd>

Eine [**SystemHealthEntityId,**](nap-type-constants.md) die den eindeutigen Bezeichner der SHV enthält, deren Registrierung aufgehoben werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Es können auch andere COM-spezifische Fehlercodes zurückgegeben werden.



| Rückgabecode                                                                                     | Beschreibung                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Vorgang erfolgreich.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Berechtigungsfehler, Zugriff verweigert.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Systemressourcenlimit, konnte den Vorgang nicht ausführen.<br/> |



 

## <a name="remarks"></a>Hinweise

Wenn asynchrone Aufrufe für die SHV ausstehen, werden sie zu einem späteren Zeitpunkt abgeschlossen und verworfen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                               |
| Header<br/>                   | <dl> <dt>NapServerManagement.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapServerManagement.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qsvrmgmt.dll</dt> </dl>            |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**INapServerManagement**](inapservermanagement.md)
</dt> </dl>

 

 





