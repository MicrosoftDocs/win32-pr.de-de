---
title: INapEnforcementClientConnection Initialize-Methode (NapEnforcementClient.h)
description: Initialisiert die Clientverbindung.
ms.assetid: da72bfc3-9551-4fb0-b9a5-2931c14f618f
keywords:
- Initialisieren der NAP-Methode
- Initialisieren der NAP-Methode, INapEnforcementClientConnection-Schnittstelle
- INapEnforcementClientConnection-Schnittstelle NAP, Initialize-Methode
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.Initialize
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 034fd83ac9337f6b2529b4035e6daa1b9bd06c3022ed30dbce0af74e5f6ef6cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118939661"
---
# <a name="inapenforcementclientconnectioninitialize-method"></a>INapEnforcementClientConnection::Initialize-Methode

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab dem Windows 10

 

Die **INapEnforcementClientConnection::Initialize-Methode** initialisiert die Clientverbindung.

## <a name="syntax"></a>Syntax


```C++
HRESULT Initialize(
  [in] EnforcementEntityId id
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*id* \[ in\]
</dt> <dd>

Ein Zeiger auf eine [**EnforementEntityId,**](nap-datatypes.md) die den Erzwingungsclient identifiziert, der die Verbindung an fordert. Dieser Wert wird während der Verbindungserstellung vom NapAgent festgelegt.

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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**INapEnforcementClientConnection**](inapenforcementclientconnection.md)
</dt> </dl>

 

 





