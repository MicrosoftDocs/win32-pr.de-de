---
title: INapEnforcementClientConnection GetIsolationInfo-Methode (NapEnforcementClient.h)
description: Wird verwendet, um die Isolationsinformationen des Clients abzurufen.
ms.assetid: 33040554-dcbe-4563-b047-fc7e28bac55c
keywords:
- Nap-Methode "GetIsolationInfo"
- GetIsolationInfo-Methode NAP, INapEnforcementClientConnection-Schnittstelle
- INapEnforcementClientConnection-Schnittstelle NAP , GetIsolationInfo-Methode
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetIsolationInfo
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81f9fffc3f31b22e791b8f5dcff67bfc4b75c998f35158f99d5c558004a51f5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118939958"
---
# <a name="inapenforcementclientconnectiongetisolationinfo-method"></a>INapEnforcementClientConnection::GetIsolationInfo-Methode

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **INapEnforcementClientConnection::GetIsolationInfo-Methode** wird verwendet, um die Isolationsinformationen des Clients abzurufen.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetIsolationInfo(
  [out] IsolationInfo **isolationInfo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*isolationInfo* \[ out\]
</dt> <dd>

Ein Zeiger auf einen Zeiger auf eine [**IsolationInfo-Struktur,**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo) die den Konnektivitätsstatus des Clients enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Andere COM-spezifische Fehlercodes können ebenfalls zurückgegeben werden.



| Rückgabecode                                                                                     | Beschreibung                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Vorgang erfolgreich.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Berechtigungsfehler, Zugriff verweigert.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Systemressourcenlimit, konnte den Vorgang nicht ausführen.<br/> |



 

## <a name="remarks"></a>Hinweise

Diese Informationen werden vom NapAgent nach der Verarbeitung einer [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) festgelegt und dürfen nicht vom Erzwingenden festgelegt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                |
| Header<br/>                   | <dl> <dt>NapEnforcementClient.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapEnforcementClient.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**INapEnforcementClientConnection**](inapenforcementclientconnection.md)
</dt> </dl>

 

 





