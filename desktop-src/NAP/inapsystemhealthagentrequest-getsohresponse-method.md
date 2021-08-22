---
title: INapSystemHealthAgentRequest GetSoHResponse-Methode (NapSystemHealthAgent.h)
description: Wird vom Integritäts-Agent zum Abrufen des SoHResponse-Blobs verwendet, wenn der NapAgent INapSystemHealthAgentCallback ProcessSoHResponse aufruft.
ms.assetid: 60319256-d5c2-46cc-a59b-f81732e21a7f
keywords:
- GetSoHResponse-Methode NAP
- GetSoHResponse-Methode NAP, INapSystemHealthAgentRequest-Schnittstelle
- INapSystemHealthAgentRequest-Schnittstelle NAP , GetSoHResponse-Methode
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
ms.openlocfilehash: 1d78b67c38f54cfe1e7d342212be897ba1825b619324e6fc4cb5ab9ae4f5c4a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118621161"
---
# <a name="inapsystemhealthagentrequestgetsohresponse-method"></a>INapSystemHealthAgentRequest::GetSoHResponse-Methode

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **INapSystemHealthAgentRequest::GetSoHResponse-Methode** wird vom Integritäts-Agent zum Abrufen des SoHResponse-Blobs verwendet, wenn der NapAgent [**INapSystemHealthAgentCallback::P rocessSoHResponse**](inapsystemhealthagentcallback-processsohresponse-method.md)aufruft.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetSoHResponse(
  [out] SoHResponse **sohResponse,
  [out] UINT8       *flags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*sohResponse* \[ out\]
</dt> <dd>

Ein Zeiger auf einen Zeiger auf ein [**SoHResponse-Paket.**](/windows/win32/api/naptypes/ns-naptypes-soh)

</dd> <dt>

*Flags* \[ out\]
</dt> <dd>

Ein Zeiger auf ein Flag, das die Korrektur durch den SHA ermöglicht, wenn das [**shaFixup-Bit**](nap-type-constants.md) festgelegt ist, andernfalls ist die Korrektur deaktiviert.



| Mögliche Werte                                                                                                                                                          | Bedeutung                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="shaFixup"></span><span id="shafixup"></span><span id="SHAFIXUP"></span><dl> <dt>**shaFixup**</dt> </dl> | Es wird erwartet, dass der SHA den Fixup basierend auf der Antwort ausführt. Wenn dieses Flag nicht festgelegt ist, sollte der SHA keine Korrektur durchführen, obwohl [**die SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) angibt, dass es fehlerhaft ist.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Andere COM-spezifische Fehlercodes können ebenfalls zurückgegeben werden.



| Rückgabecode                                                                                     | Beschreibung                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Vorgang erfolgreich.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Berechtigungsfehler, Zugriff verweigert.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Systemressourcenlimit, konnte den Vorgang nicht ausführen.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                |
| Header<br/>                   | <dl> <dt>NapSystemHealthAgent.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapSystemHealthAgent.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagentrt.dll</dt> </dl>             |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md)
</dt> </dl>

 

 





