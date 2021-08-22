---
title: INapServerManagement SetFailureCategoryMappings-Methode (NapServerManagement.h)
description: Dient zum Festlegen der Fehlerkategoriezuordnungen des SHV.
ms.assetid: be482f82-c79c-405c-b619-9bcb9b4dc349
keywords:
- SetFailureCategoryMappings-Methode NAP
- SetFailureCategoryMappings-Methode NAP, INapServerManagement-Schnittstelle
- INapServerManagement-Schnittstelle NAP, SetFailureCategoryMappings-Methode
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
ms.openlocfilehash: c22bc51edf887d26bf34f59932248c62bfca86199771a2b971a10e9c1b323eac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118939614"
---
# <a name="inapservermanagementsetfailurecategorymappings-method"></a>INapServerManagement::SetFailureCategoryMappings-Methode

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab dem Windows 10

 

Die **INapServerManagement::SetFailureCategoryMappings-Methode** wird verwendet, um die Fehlerkategoriezuordnungen der SHV zu festlegen.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetFailureCategoryMappings(
  [in]       SystemHealthEntityId   id,
  [in] const FailureCategoryMapping mapping
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*id* \[ in\]
</dt> <dd>

Eine [**SystemHealthEntityId,**](nap-type-constants.md) die den eindeutigen Bezeichner der SHV enthält.

</dd> <dt>

*Zuordnung* \[ In\]
</dt> <dd>

Eine [**FailureCategoryMapping-Struktur,**](/windows/win32/api/naptypes/ns-naptypes-failurecategorymapping) die die Zuordnungsdaten der Fehlerkategorie enthält.

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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**INapServerManagement**](inapservermanagement.md)
</dt> </dl>

 

 





