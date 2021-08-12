---
title: INapEnforcementClientConnection2 SetInstalledShvs-Methode (NapEnforcementClient.h)
description: Wird vom NAP-Agent verwendet, um die installierten System health Validators (SHVs) auf dem Client festzulegen.
ms.assetid: 38aa99b9-a15a-414d-91fc-128de8f5a654
keywords:
- NAP-Methode "SetInstalledShvs"
- SetInstalledShvs-Methode NAP, INapEnforcementClientConnection2-Schnittstelle
- INapEnforcementClientConnection2-Schnittstelle NAP, SetInstalledShvs-Methode
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
ms.openlocfilehash: 31a95f9ad491b0b5a6354bb5c44a7ff54f64b29ffa715762ab43a7752e3a3ac0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118621335"
---
# <a name="inapenforcementclientconnection2setinstalledshvs-method"></a>INapEnforcementClientConnection2::SetInstalledShvs-Methode

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **SetInstalledShvs-Methode** wird vom NAP-Agent verwendet, um die installierten SYSTEM HEALTH Validators (SHVs) auf dem Client festzulegen.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetInstalledShvs(
  [in] SystemHealthEntityCount count,
  [in] SystemHealthEntityId    *ids
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*count* \[ In\]
</dt> <dd>

Ein [SystemHealthEntityCount-Wert,](nap-datatypes.md) der die Anzahl der SHVs angibt, die in *IDs* installiert werden sollen.

</dd> <dt>

*ids* \[ In\]
</dt> <dd>

Ein Zeiger auf einen [SystemHealthEntityId-Wert,](nap-datatypes.md) der eine Liste der zu installierenden SHV-IDs enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Andere COM-spezifische Fehlercodes können ebenfalls zurückgegeben werden.



| Rückgabecode                                                                                  | Beschreibung                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>        | Die Methode war erfolgreich.<br/>          |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Der *count-Parameter* war 0 (null).<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                |
| Header<br/>                   | <dl> <dt>NapEnforcementClient.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapEnforcementClient.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**INapEnforcementClientConnection2**](inapenforcementclientconnection2.md)
</dt> </dl>

 

 





