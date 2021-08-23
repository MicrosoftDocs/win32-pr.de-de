---
title: INapEnforcementClientConnection2 SetIsolationInfoEx-Methode (NapEnforcementClient.h)
description: Wird vom NapAgent zum Festlegen der Isolationsinformationen für den Client verwendet.
ms.assetid: 1b1a41a1-73a6-4c81-8366-15d06c67e228
keywords:
- SetIsolationInfoEx-Methode NAP
- SetIsolationInfoEx-Methode NAP, INapEnforcementClientConnection2-Schnittstelle
- INapEnforcementClientConnection2-Schnittstelle NAP, SetIsolationInfoEx-Methode
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection2.SetIsolationInfoEx
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f86a678cce54a9872f8f3c059da3b3055f891160b042241769712b4424250690
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119626200"
---
# <a name="inapenforcementclientconnection2setisolationinfoex-method"></a>INapEnforcementClientConnection2::SetIsolationInfoEx-Methode

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab dem Windows 10

 

Die **INapEnforcementClientConnection2::SetIsolationInfoEx-Methode** wird vom NapAgent zum Festlegen der Isolationsinformationen für den Client verwendet.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetIsolationInfoEx(
  [in] const IsolationInfoEx *isolationInfo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*isolationInfo* \[ In\]
</dt> <dd>

Ein Zeiger auf eine [**IsolationInfoEx-Struktur,**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) die den Konnektivitätsstatus des Clients enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Es können auch andere COM-spezifische Fehlercodes zurückgegeben werden.



| Rückgabecode                                                                                     | Beschreibung                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Vorgang erfolgreich.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Berechtigungsfehler, Zugriff verweigert.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Systemressourcenlimit, konnte den Vorgang nicht ausführen.<br/> |



 

## <a name="remarks"></a>Hinweise

Diese Informationen werden von NapAgent nach der Verarbeitung einer [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) festgelegt und dürfen nicht vom Erzwinger festgelegt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                |
| Header<br/>                   | <dl> <dt>NapEnforcementClient.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapEnforcementClient.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**INapEnforcementClientConnection2**](inapenforcementclientconnection2.md)
</dt> </dl>

 

 





