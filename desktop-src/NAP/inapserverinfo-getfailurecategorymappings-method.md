---
title: Inapserverinfo getfailurecategorymappings-Methode (napservermanagement. h)
description: Ruft die Zuordnungen der Fehlerkategorien für einen angegebenen SHA-oder SHV-Knoten ab.
ms.assetid: 89b89003-40b3-4763-aec8-01cd0c307649
keywords:
- Getfailurecategorymappings-Methode NAP
- Getfailurecategorymappings-Methode NAP, inapserverinfo-Schnittstelle
- Inapserverinfo-Schnittstelle NAP, getfailurecategorymappings-Methode
topic_type:
- apiref
api_name:
- INapServerInfo.GetFailureCategoryMappings
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7ba830dd8a35a2c60b14c4feec14846125223e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479341"
---
# <a name="inapserverinfogetfailurecategorymappings-method"></a>Inapserverinfo:: getfailurecategorymappings-Methode

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **inapserverinfo:: getfailurecategorymappings** -Methode ruft die Zuordnungen der Fehlerkategorien für einen angegebenen SHA oder SHV ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetFailureCategoryMappings(
  [in]  SystemHealthEntityId   id,
  [out] FailureCategoryMapping *mapping
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ID* \[ in\]
</dt> <dd>

Eine [**systemhealthentityid**](nap-type-constants.md) , die den eindeutigen Bezeichner von SHA oder SHV enthält.

</dd> <dt>

*Zuordnung* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf ein [**failurecategorymapping**](/windows/win32/api/naptypes/ns-naptypes-failurecategorymapping) , das die Mapping-Daten enthält.

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

[**Inapserverinfo**](inapserverinfo.md)
</dt> </dl>

 

 





