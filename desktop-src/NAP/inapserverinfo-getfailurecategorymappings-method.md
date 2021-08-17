---
title: INapServerInfo GetFailureCategoryMappings-Methode (NapServerManagement.h)
description: Ruft die Fehlerkategoriezuordnungen für einen angegebenen SHA- oder SHV-Wert ab.
ms.assetid: 89b89003-40b3-4763-aec8-01cd0c307649
keywords:
- GetFailureCategoryMappings-Methode NAP
- GetFailureCategoryMappings-Methode NAP, INapServerInfo-Schnittstelle
- INapServerInfo-Schnittstelle NAP, GetFailureCategoryMappings-Methode
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
ms.openlocfilehash: 13fcd87105eace269d3b8f395392c8a0ba275a135c212863ef69e45e597eb752
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144383"
---
# <a name="inapserverinfogetfailurecategorymappings-method"></a>INapServerInfo::GetFailureCategoryMappings-Methode

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab dem Windows 10

 

Die **INapServerInfo::GetFailureCategoryMappings-Methode** ruft die Fehlerkategoriezuordnungen für einen angegebenen SHA- oder SHV-Wert ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetFailureCategoryMappings(
  [in]  SystemHealthEntityId   id,
  [out] FailureCategoryMapping *mapping
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*id* \[ in\]
</dt> <dd>

Eine [**SystemHealthEntityId,**](nap-type-constants.md) die den eindeutigen Bezeichner des SHA oder der SHV enthält.

</dd> <dt>

*Zuordnung* \[ out\]
</dt> <dd>

Ein Zeiger auf eine [**FailureCategoryMapping-Datei,**](/windows/win32/api/naptypes/ns-naptypes-failurecategorymapping) die die Zuordnungsdaten enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Es können auch andere COM-spezifische Fehlercodes zurückgegeben werden.



| Rückgabecode                                                                                     | Beschreibung                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Vorgang erfolgreich.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Berechtigungsfehler, Zugriff verweigert.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Systemressourcenlimit, konnte den Vorgang nicht ausführen.<br/> |



 

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

[**INapServerInfo**](inapserverinfo.md)
</dt> </dl>

 

 





