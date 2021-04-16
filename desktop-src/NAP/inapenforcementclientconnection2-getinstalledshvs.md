---
title: INapEnforcementClientConnection2 getinstalledshvs-Methode (napforcementclient. h)
description: Wird vom NAP-Agent verwendet, um die installierten System Integritätsprüfungen (SHVs) auf dem Client abzufragen.
ms.assetid: b2e3ab29-90bf-4117-bc2e-2ff2827ee15c
keywords:
- Getinstalledshvs-Methode NAP
- Getinstalledshvs-Methode NAP, INapEnforcementClientConnection2-Schnittstelle
- INapEnforcementClientConnection2 Interface NAP, getinstalledshvs-Methode
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
ms.openlocfilehash: fa54d09a0c3d3c524262231982f662c497920a0b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479356"
---
# <a name="inapenforcementclientconnection2getinstalledshvs-method"></a>INapEnforcementClientConnection2:: getinstalledshvs-Methode

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **getinstalledshvs** -Methode wird vom NAP-Agent verwendet, um die installierten System Integritätsprüfungen (SHVs) auf dem Client abzufragen.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetInstalledShvs(
  [out] SystemHealthEntityCount *count,
  [out] SystemHealthEntityId    **ids
) const;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Anzahl* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen [systemhealthentitycount](nap-datatypes.md) -Wert, der die Anzahl der installierten SHVs in *IDs* angibt.

</dd> <dt>

*IDs* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf ein Array von [systemhealthentityid](nap-datatypes.md) -Werten, die die installierten SHV-IDs enthalten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.



| Rückgabecode                                                                                   | Beschreibung                                              |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Vorgang erfolgreich.<br/>                          |
| <dl> <dt>**E \_ InvalidArg**</dt> </dl> | Ein ungültiges Argument wurde an die-Methode übermittelt.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                      |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                |
| Header<br/>                   | <dl> <dt>Napforcementclient. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Napforcementclient. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**INapEnforcementClientConnection2**](inapenforcementclientconnection2.md)
</dt> </dl>

 

 





