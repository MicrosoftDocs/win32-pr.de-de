---
title: INapEnforcementClientConnection2 setinstalledshvs-Methode (napforcementclient. h)
description: Wird vom NAP-Agent verwendet, um die installierten System Integritätsprüfungen (SHVs) auf dem Client festzulegen.
ms.assetid: 38aa99b9-a15a-414d-91fc-128de8f5a654
keywords:
- Setinstalledshvs-Methode NAP
- Setinstalledshvs-Methode NAP, INapEnforcementClientConnection2-Schnittstelle
- INapEnforcementClientConnection2 Interface NAP, setinstalledshvs-Methode
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection2.SetInstalledShvs
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6651cd5248094f82d9faa1862492f82648e94125
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106514"
---
# <a name="inapenforcementclientconnection2setinstalledshvs-method"></a>INapEnforcementClientConnection2:: setinstalledshvs-Methode

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **setinstalledshvs** -Methode wird vom NAP-Agent verwendet, um die installierten System Integritätsprüfungen (SHVs) auf dem Client festzulegen.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetInstalledShvs(
  [in] SystemHealthEntityCount count,
  [in] SystemHealthEntityId    *ids
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Anzahl* \[ in\]
</dt> <dd>

Ein [systemhealthentitycount](nap-datatypes.md) -Wert, der die Anzahl der SHVs angibt, die in *IDs* installiert werden sollen.

</dd> <dt>

*IDs* \[ in\]
</dt> <dd>

Ein Zeiger auf einen [systemhealthentityid](nap-datatypes.md) -Wert, der eine Liste der zu installierenden SHV-IDs enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.



| Rückgabecode                                                                                  | Beschreibung                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>        | Die Methode war erfolgreich.<br/>          |
| <dl> <dt>**E \_ invalidArg**</dt> </dl> | Der *count* -Parameter war 0 (null).<br/> |



 

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

 

 





