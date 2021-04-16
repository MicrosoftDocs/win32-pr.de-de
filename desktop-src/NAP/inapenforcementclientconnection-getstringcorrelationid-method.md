---
title: Inapenforcementclientconnection getstringcorrelationid-Methode (napforcementclient. h)
description: Ruft die Zeichen folgen Version der ID ab, die verwendet wird, um Anforderungen und Antworten zu korrelieren.
ms.assetid: d744fa4e-5e30-429e-810d-7326047bb3f8
keywords:
- Getstringcorrelationid-Methode NAP
- Getstringcorrelationid-Methode NAP, inapenforcementclientconnection-Schnittstelle
- Inapenforcementclientconnection-Schnittstelle NAP, getstringcorrelationid-Methode
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
ms.openlocfilehash: c6a01ca16bffb627f4ca5be38ef547980951c0ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517579"
---
# <a name="inapenforcementclientconnectiongetstringcorrelationid-method"></a>Inapenforcementclientconnection:: getstringcorrelationid-Methode

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **inapenforcementclientconnection:: getstringcorrelationid** -Methode ruft die Zeichen folgen Version der ID ab, die verwendet wird, um Anforderungen und Antworten zu korrelieren.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetStringCorrelationId(
  [out] CountedString **correlationId
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*correlationId* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine [**zählstring**](/windows/win32/api/naptypes/ns-naptypes-countedstring) -Struktur, die die Zeichen folgen Version der [**correlationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid)der Verbindung enthält.

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
| Header<br/>                   | <dl> <dt>Napforcementclient. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Napforcementclient. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Inapenforcementclientconnection**](inapenforcementclientconnection.md)
</dt> </dl>

 

 





