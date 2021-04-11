---
title: Inapsystemhealthagentrequest getsohresponse-Methode (napsystemhealthagent. h)
description: Wird vom Integritäts-Agent zum Abrufen des sohresponse-BLOBs verwendet, wenn der NAPAgent inapsystemhealthagentcallback processsohresponse aufruft.
ms.assetid: 60319256-d5c2-46cc-a59b-f81732e21a7f
keywords:
- Getsohresponse-Methode NAP
- Getsohresponse-Methode NAP, inapsystemhealthagentrequest-Schnittstelle
- Inapsystemhealthagentrequest-Schnittstelle NAP, getsohresponse-Methode
topic_type:
- apiref
api_name:
- INapSystemHealthAgentRequest.GetSoHResponse
api_location:
- qagentrt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d593ff897e69b86b554365561e43308adead5250
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103294"
---
# <a name="inapsystemhealthagentrequestgetsohresponse-method"></a>Inapsystemhealthagentrequest:: getsohresponse-Methode

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **inapsystemhealthagentrequest:: getsohresponse** -Methode wird vom Health-Agent zum Abrufen ihres sohresponse-BLOBs verwendet, wenn der NAPAgent [**inapsystemhealthagentcallback::P rocesssohresponse**](inapsystemhealthagentcallback-processsohresponse-method.md)aufruft.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetSoHResponse(
  [out] SoHResponse **sohResponse,
  [out] UINT8       *flags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*sohresponse* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen Zeiger auf ein [**sohresponse**](/windows/win32/api/naptypes/ns-naptypes-soh) -Paket.

</dd> <dt>

*Flags* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf ein Flag, das eine Korrektur durch SHA ermöglicht, wenn das [**shafixupbit**](nap-type-constants.md) festgelegt ist, andernfalls ist die Behebung deaktiviert.



| Mögliche Werte                                                                                                                                                          | Bedeutung                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="shaFixup"></span><span id="shafixup"></span><span id="SHAFIXUP"></span><dl> <dt>**shafixup**</dt> </dl> | Der SHA wird erwartet, dass das Fixup basierend auf der Antwort ausgeführt wird. Wenn dieses Flag nicht festgelegt ist, sollte das SHA keine Korrektur durchführen, auch wenn die [**sohresponse**](/windows/win32/api/naptypes/ns-naptypes-soh) angibt, dass Sie fehlerhaft ist.<br/> |



 

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
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                      |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                |
| Header<br/>                   | <dl> <dt>Napsystemhealthagent. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Napsystemhealthagent. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagentrt.dll</dt> </dl>             |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Inapsystemhealthagentrequest**](inapsystemhealthagentrequest.md)
</dt> </dl>

 

 





