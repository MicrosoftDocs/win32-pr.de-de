---
title: Inapenforcementclientbinding notifyconnectionstatedown-Methode (napforcementclient. h)
description: Wird verwendet, um den NAPAgent darüber zu informieren, dass eine Verbindung zu einem Erzwingungs Client nicht mehr besteht.
ms.assetid: 504c61c1-c8f9-46b8-87cd-c1f04846f0b3
keywords:
- Notifyconnectionstatedown-Methode NAP
- Notifyconnectionstatedown-Methode NAP, inapenforcementclientbinding-Schnittstelle
- Inapenforcementclientbinding-Schnittstelle NAP, notifyconnectionstatedown-Methode
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
ms.openlocfilehash: 3129883342f493fd56a4cc81513910e8789ca4f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519279"
---
# <a name="inapenforcementclientbindingnotifyconnectionstatedown-method"></a>Inapenforcementclientbinding:: notifyconnectionstatedown-Methode

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **inapenforcementclientbinding:: notifyconnectionstatedown** -Methode wird verwendet, um den NAPAgent darüber zu informieren, dass eine Verbindung zu einem Erzwingungs Client nicht mehr besteht.

## <a name="syntax"></a>Syntax


```C++
HRESULT NotifyConnectionStateDown(
  [in] INapEnforcementClientConnection *downCxn
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*downcxn* \[ in\]
</dt> <dd>

Ein com-Zeiger auf die [**inapenforcementclientconnection**](inapenforcementclientconnection.md) -Schnittstelle der nach-unten-Verbindung.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.



| Rückgabecode                                                                                             | Beschreibung                                                        |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Der Vorgang ist erfolgreich.<br/>                            |
| <dl> <dt>**E \_ Access verweigert**</dt> </dl>         | Berechtigungs Fehler, Zugriff verweigert.<br/>                       |
| <dl> <dt>**E \_ Outo-Memory**</dt> </dl>          | System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.<br/> |
| <dl> <dt>**NAP \_ E \_ nicht \_ Initialisiert**</dt> </dl> | Der Enforcer wurde nicht bereits initialisiert.<br/>       |



 

## <a name="remarks"></a>Bemerkungen

Wenn eine der von einem Erzwingungs Client eingerichteten Verbindungen herunterfährt, sollte der Erzwingungs Client die Verbindung aus der aktiven Liste entfernen und den NAPAgent mithilfe dieser Methode informieren. Sobald dieser Rückruf zurückkehrt, kann das Verbindungs Objekt freigegeben und freigegeben werden. Der NAPAgent hält keine Verweise auf das Verbindungs Objekt.

Als Ergebnis dieser Benachrichtigung aktualisiert der NAPAgent den NAP-Status des Systems entsprechend.

Der Erzwingungs Client muss die [**inapenforcementclientbinding:: Initialize**](inapenforcementclientbinding-initialize-method.md) -Methode aufrufen, bevor diese oder eine andere Methode der [**inapenforcementclientbinding**](inapenforcementclientbinding.md) -Schnittstelle aufgerufen wird.

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


</dt> <dt>

[**Inapenforcementclientbinding**](inapenforcementclientbinding.md)
</dt> </dl>

 

 





