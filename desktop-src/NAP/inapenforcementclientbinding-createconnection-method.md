---
title: INapEnforcementClientBinding CreateConnection-Methode (NapEnforcementClient.h)
description: Wird von Erzwingern zum Erstellen von Verbindungsobjekten verwendet.
ms.assetid: 4d31928f-1a10-4168-a53c-256cbbf3e5c9
keywords:
- CreateConnection-Methode NAP
- CreateConnection-Methode NAP, INapEnforcementClientBinding-Schnittstelle
- INapEnforcementClientBinding-Schnittstelle NAP, CreateConnection-Methode
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.CreateConnection
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e72c8ef4760d611c45291f0de1039b915e9bc8fedde94c314bb1272e4b99b03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119891280"
---
# <a name="inapenforcementclientbindingcreateconnection-method"></a>INapEnforcementClientBinding::CreateConnection-Methode

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab dem Windows 10

 

Die **INapEnforcementClientBinding::CreateConnection-Factorymethode** wird von Erzwingern zum Erstellen von Verbindungsobjekten verwendet.

## <a name="syntax"></a>Syntax


```C++
HRESULT CreateConnection(
  [out] INapEnforcementClientConnection **connection
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Verbindung* \[ out\]
</dt> <dd>

Ein COM-Zeiger auf eine neue [**INapEnforcementClientConnection-Schnittstelle,**](inapenforcementclientconnection.md) die vom NAP-System zurückgegeben wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Es können auch andere COM-spezifische Fehlercodes zurückgegeben werden.



| Rückgabecode                                                                                     | Beschreibung                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Der Vorgang ist erfolgreich.<br/>                            |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Berechtigungsfehler, Zugriff verweigert.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Systemressourcenlimit, konnte den Vorgang nicht ausführen.<br/> |



 

## <a name="remarks"></a>Hinweise

Der Erzwingungsclient muss die [**INapEnforcementClientBinding::Initialize-Methode**](inapenforcementclientbinding-initialize-method.md) aufrufen, bevor er diese oder eine andere Methode der [**INapEnforcementClientBinding-Schnittstelle**](inapenforcementclientbinding.md) aufruft.

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


</dt> <dt>

[**INapEnforcementClientBinding**](inapenforcementclientbinding.md)
</dt> <dt>

[**INapEnforcementClientConnection**](inapenforcementclientconnection.md)
</dt> </dl>

 

 





