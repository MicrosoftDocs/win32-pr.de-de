---
title: INapEnforcementClientConnection GetStringCorrelationId-Methode (NapEnforcementClient.h)
description: Ruft die Zeichenfolgenversion der ID ab, die zum Korrelieren von Anforderungen und Antworten verwendet wird.
ms.assetid: d744fa4e-5e30-429e-810d-7326047bb3f8
keywords:
- GetStringCorrelationId-Methode NAP
- GetStringCorrelationId-Methode NAP, INapEnforcementClientConnection-Schnittstelle
- INapEnforcementClientConnection-Schnittstelle NAP, GetStringCorrelationId-Methode
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetStringCorrelationId
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c7a7729873958d830e40a1979abb5fbcb3135ec4f08ae75af8396244ef35537
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119781010"
---
# <a name="inapenforcementclientconnectiongetstringcorrelationid-method"></a>INapEnforcementClientConnection::GetStringCorrelationId-Methode

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab dem Windows 10

 

Die **INapEnforcementClientConnection::GetStringCorrelationId-Methode** ruft die Zeichenfolgenversion der ID ab, die zum Korrelieren von Anforderungen und Antworten verwendet wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetStringCorrelationId(
  [out] CountedString **correlationId
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*correlationId* \[ out\]
</dt> <dd>

Ein Zeiger auf eine [**CountedString-Struktur,**](/windows/win32/api/naptypes/ns-naptypes-countedstring) die die Zeichenfolgenversion der CorrelationId der [**Verbindung enthält.**](/windows/win32/api/naptypes/ns-naptypes-correlationid)

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
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                |
| Header<br/>                   | <dl> <dt>NapEnforcementClient.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapEnforcementClient.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**INapEnforcementClientConnection**](inapenforcementclientconnection.md)
</dt> </dl>

 

 





