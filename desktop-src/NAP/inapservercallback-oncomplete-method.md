---
title: Inapservercallback OnComplete-Methode (napsystemhealthvalidator. h)
description: Wird von SHVs verwendet, um den Abschluss einer asynchronen Anforderung zu signalisieren.
ms.assetid: 959ee4ac-7c29-4013-a174-24abc6a580c7
keywords:
- OnComplete-Methode, NAP
- OnComplete-Methode, NAP, inapservercallback-Schnittstelle
- Inapservercallback-Schnittstelle NAP, OnComplete-Methode
topic_type:
- apiref
api_name:
- INapServerCallback.OnComplete
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ef846d3d9dc2d6618f0eca9f097d74222606eb4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479344"
---
# <a name="inapservercallbackoncomplete-method"></a>Inapservercallback:: OnComplete-Methode

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **inapservercallback:: OnComplete** -Methode wird von SHVs verwendet, um den Abschluss einer asynchronen Anforderung zu signalisieren.

## <a name="syntax"></a>Syntax


```C++
HRESULT OnComplete(
  [in] INapSystemHealthValidationRequest *request,
  [in] HRESULT                           errorCode
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Anforderung* \[ in\]
</dt> <dd>

Ein Zeiger auf ein [**inapsystemhealthvalidationrequest**](inapsystemhealthvalidationrequest.md) -Objekt, das eine Validierungs Anforderung darstellt.

</dd> <dt>

*errorCode* \[ in\]
</dt> <dd>

Ein [**NAP-Fehlercode**](nap-error-constants.md) , der den Grund angibt, warum die Überprüfung nicht ausgeführt werden konnte.

> [!Note]  
> In der Regel wird der Rückgabewert der Methode [**inapsystemhealthvalidationrequest:: setsohresponse**](inapsystemhealthvalidationrequest-setsohresponse-method.md) an diesen Parameter übergeben. Wenn **setsohresponse** jedoch aufgrund eines erneuten Verarbeitungs Fehlers nicht aufgerufen werden konnte, wird der Wert, der vom fehlerhaften Befehl zurückgegeben wurde, übermittelt.

 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.



| Rückgabecode                                                                                     | Beschreibung                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Vorgang erfolgreich.<br/>                                    |
| <dl> <dt>**E \_ Access verweigert**</dt> </dl> | Berechtigungs Fehler, Zugriff verweigert.<br/>                       |
| <dl> <dt>**E \_ Outo-Memory**</dt> </dl>  | System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Validators müssen S OK zurückgeben \_ , wenn die [**sohrequest**](/windows/win32/api/naptypes/ns-naptypes-soh) -Überprüfung abgeschlossen werden konnte, unabhängig davon, ob der **sohrequest** die Integritätsprüfung bestanden hat.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                    |
| Header<br/>                   | <dl> <dt>Napsystemhealthvalidator. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Napsystemhealthvalidator. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qshvhost.dll</dt> </dl>                 |



## <a name="see-also"></a>Siehe auch

<dl> <dt>


</dt> <dt>

[**Inapservercallback**](inapservercallback.md)
</dt> <dt>

[**Inapsystemhealthvalidationrequest**](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





