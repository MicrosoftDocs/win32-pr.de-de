---
title: INapEnforcementClientBinding NotifyConnectionStateDown-Methode (NapEnforcementClient.h)
description: Wird verwendet, um napAgent darüber zu informieren, dass eine Verbindung mit einem Erzwingungsclient beendet wurde.
ms.assetid: 504c61c1-c8f9-46b8-87cd-c1f04846f0b3
keywords:
- NotifyConnectionStateDown-Methode NAP
- NotifyConnectionStateDown-Methode NAP, INapEnforcementClientBinding-Schnittstelle
- INapEnforcementClientBinding-Schnittstelle NAP , NotifyConnectionStateDown-Methode
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.NotifyConnectionStateDown
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e0e40d3b46e8c970287f49d983d89733d4858e38671ac93fb75d482c0259a73
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119803050"
---
# <a name="inapenforcementclientbindingnotifyconnectionstatedown-method"></a>INapEnforcementClientBinding::NotifyConnectionStateDown-Methode

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **INapEnforcementClientBinding::NotifyConnectionStateDown-Methode** wird verwendet, um napAgent darüber zu informieren, dass eine Verbindung mit einem Erzwingungsclient getrennt wurde.

## <a name="syntax"></a>Syntax


```C++
HRESULT NotifyConnectionStateDown(
  [in] INapEnforcementClientConnection *downCxn
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*downCxn* \[ In\]
</dt> <dd>

Ein COM-Zeiger auf die [**INapEnforcementClientConnection-Schnittstelle**](inapenforcementclientconnection.md) der down-Verbindung.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Andere COM-spezifische Fehlercodes können ebenfalls zurückgegeben werden.



| Rückgabecode                                                                                             | Beschreibung                                                        |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Der Vorgang ist erfolgreich.<br/>                            |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>         | Berechtigungsfehler, Zugriff verweigert.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>          | Systemressourcenlimit, konnte den Vorgang nicht ausführen.<br/> |
| <dl> <dt>**NAP \_ E \_ NICHT \_ INITIALISIERT**</dt> </dl> | Der Enforcer wurde zuvor nicht initialisiert.<br/>       |



 

## <a name="remarks"></a>Hinweise

Wenn eine der von einem Erzwingungsclient hergestellten Verbindungen ausgeschaltet wird, sollte der Erzwingungsclient die Verbindung aus der aktiven Liste entfernen und napAgent mit dieser Methode informieren. Sobald dieser Aufruf zurückgegeben wird, kann das Verbindungsobjekt freigegeben und freigegeben werden. NapAgent enthält keine Verweise auf das Verbindungsobjekt.

Aufgrund dieser Benachrichtigung aktualisiert NapAgent den NAP-Systemstatus nach Bedarf.

Der Erzwingungsclient muss die [**INapEnforcementClientBinding::Initialize-Methode**](inapenforcementclientbinding-initialize-method.md) aufrufen, bevor er diese oder eine andere Methode der [**INapEnforcementClientBinding-Schnittstelle aufruft.**](inapenforcementclientbinding.md)

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


</dt> <dt>

[**INapEnforcementClientBinding**](inapenforcementclientbinding.md)
</dt> </dl>

 

 





