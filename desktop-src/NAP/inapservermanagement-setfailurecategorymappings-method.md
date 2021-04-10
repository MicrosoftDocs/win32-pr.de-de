---
title: Inapservermanagement setfailurecategorymappings-Methode (napservermanagement. h)
description: Wird verwendet, um die Fehler Kategoriezuordnungen von SHV festzulegen.
ms.assetid: be482f82-c79c-405c-b619-9bcb9b4dc349
keywords:
- Setfailurecategorymappings-Methode NAP
- Setfailurecategorymappings-Methode NAP, inapservermanagement-Schnittstelle
- Inapservermanagement-Schnittstelle NAP, setfailurecategorymappings-Methode
topic_type:
- apiref
api_name:
- INapServerManagement.SetFailureCategoryMappings
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a220d6603ef5bbb49377ac0e212d5d98afa4bdd0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956768"
---
# <a name="inapservermanagementsetfailurecategorymappings-method"></a>Inapservermanagement:: setfailurecategorymappings-Methode

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **inapservermanagement:: setfailurecategorymappings** -Methode wird verwendet, um die SHV-Zuordnungen für die Fehler Kategorie festzulegen.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetFailureCategoryMappings(
  [in]       SystemHealthEntityId   id,
  [in] const FailureCategoryMapping mapping
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ID* \[ in\]
</dt> <dd>

Eine [**systemhealthentityid**](nap-type-constants.md) , die den eindeutigen Bezeichner des SHV enthält.

</dd> <dt>

*Zuordnung* \[ in\]
</dt> <dd>

Eine [**failurecategorymapping**](/windows/win32/api/naptypes/ns-naptypes-failurecategorymapping) -Struktur, die die Fehler Kategorie-Mapping-Daten enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.



| Rückgabecode                                                                                     | Beschreibung                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Vorgang erfolgreich.<br/>                                    |
| <dl> <dt>**E \_ Access verweigert**</dt> </dl> | Berechtigungs Fehler, Zugriff verweigert.<br/>                       |
| <dl> <dt>**E \_ Outo-Memory**</dt> </dl>  | System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.<br/> |



 

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

 

 





