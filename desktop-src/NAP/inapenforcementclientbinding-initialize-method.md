---
title: Inapenforcementclientbinding Initialize-Methode (napforcementclient. h)
description: Startet den NAPAgent-Dienst automatisch.
ms.assetid: 6b51043d-a8e7-41e4-9da9-e7f18f9bd068
keywords:
- Methode "NAP initialisieren"
- Initialize-Methode NAP, inapenforcementclientbinding-Schnittstelle
- Inapenforcementclientbinding-Schnittstelle NAP, Initialize-Methode
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.Initialize
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee4d385e47bbbfe2e315d0a93d1f92542e8328e2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475999"
---
# <a name="inapenforcementclientbindinginitialize-method"></a>Inapenforcementclientbinding:: Initialize-Methode

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Mit der **inapenforcementclientbinding:: Initialize** -Methode wird der NAPAgent-Dienst automatisch gestartet.

## <a name="syntax"></a>Syntax


```C++
HRESULT Initialize(
  [in] EnforcementEntityId           id,
  [in] INapEnforcementClientCallback *callback
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ID* \[ in\]
</dt> <dd>

Eine [**enforcemententityid**](nap-datatypes.md) , die den Erzwingungs Client und seine Version identifiziert.

</dd> <dt>

*Rückruf* \[ in\]
</dt> <dd>

Ein com-Zeiger auf eine [**inapenforcementclientcallback**](inapenforcementclientcallback.md) -Schnittstelle, die vom NAPAgent verwendet wird, um die Erzwingungs Clients mit Benachrichtigen/verarbeiten zu Rückruf. Der NAPAgent enthält einen Verweis auf das Objekt, das dieser Schnittstelle zugeordnet ist, bis [**inapenforcementclientbinding:: Uninitialize**](inapenforcementclientbinding-uninitialize-method.md) aufgerufen wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.



| Rückgabecode                                                                                                         | Beschreibung                                                                              |
|---------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                               | Der Vorgang ist erfolgreich.<br/>                                                  |
| <dl> <dt>**E \_ Access verweigert**</dt> </dl>                     | Berechtigungs Fehler, Zugriff verweigert.<br/>                                             |
| <dl> <dt>**E \_ Outo-Memory**</dt> </dl>                      | System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.<br/>                       |
| <dl> <dt>**HRESULT (Fehler \_ bereits \_ initialisiert)**</dt> </dl> | Wenn der Enforcer zuvor initialisiert wurde, wird dieser Fehlercode zurückgegeben.<br/> |
| <dl> <dt>**NAP \_ E \_ nicht \_ registriert**</dt> </dl>              | Wenn der Enforcer nicht zuvor registriert wurde, wird dieser Fehlercode zurückgegeben.<br/>      |



 

## <a name="remarks"></a>Bemerkungen

Der Erzwingungs Client muss die **inapenforcementclientbinding:: Initialize** -Methode aufrufen, bevor eine andere Methode der [**inapenforcementclientbinding**](inapenforcementclientbinding.md) -Schnittstelle aufgerufen wird.

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
</dt> <dt>

[**Inapenforcementclientbinding:: Uninitialize**](inapenforcementclientbinding-uninitialize-method.md)
</dt> </dl>

 

 





