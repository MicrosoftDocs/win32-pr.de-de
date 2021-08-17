---
title: INapEnforcementClientConnection2 GetInstalledShvs-Methode (NapEnforcementClient.h)
description: Wird vom NAP-Agent verwendet, um die installierten System health Validators (SHVs) auf dem Client abfragt.
ms.assetid: b2e3ab29-90bf-4117-bc2e-2ff2827ee15c
keywords:
- GetInstalledShvs-Methode NAP
- GetInstalledShvs-Methode NAP, INapEnforcementClientConnection2-Schnittstelle
- INapEnforcementClientConnection2-Schnittstelle NAP, GetInstalledShvs-Methode
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection2.GetInstalledShvs
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40cb18f749adc9a1b7003a777cc821fb5e003b83322a7d54c2efda4b8e5739f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118939641"
---
# <a name="inapenforcementclientconnection2getinstalledshvs-method"></a>INapEnforcementClientConnection2::GetInstalledShvs-Methode

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab dem Windows 10

 

Die **GetInstalledShvs-Methode** wird vom NAP-Agent verwendet, um die installierten System health Validators (SHVs) auf dem Client abfragt.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetInstalledShvs(
  [out] SystemHealthEntityCount *count,
  [out] SystemHealthEntityId    **ids
) const;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*count* \[ out\]
</dt> <dd>

Ein Zeiger auf einen [SystemHealthEntityCount-Wert,](nap-datatypes.md) der die Anzahl der installierten SHVs in *ids angibt.*

</dd> <dt>

*ids* \[ out\]
</dt> <dd>

Ein Zeiger auf ein Array von [SystemHealthEntityId-Werten,](nap-datatypes.md) die die installierten SHV-IDs enthalten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Es können auch andere COM-spezifische Fehlercodes zurückgegeben werden.



| Rückgabecode                                                                                   | Beschreibung                                              |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Vorgang erfolgreich.<br/>                          |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Ein ungültiges Argument wurde an die -Methode übergeben.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                |
| Header<br/>                   | <dl> <dt>NapEnforcementClient.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapEnforcementClient.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**INapEnforcementClientConnection2**](inapenforcementclientconnection2.md)
</dt> </dl>

 

 





