---
title: INapServerCallback OnComplete-Methode (NapSystemHealthValidator.h)
description: Wird von SHVs zum Signalisieren des asynchronen Anforderungsabschlusses verwendet.
ms.assetid: 959ee4ac-7c29-4013-a174-24abc6a580c7
keywords:
- OnComplete-Methode NAP
- OnComplete-Methode NAP, INapServerCallback-Schnittstelle
- INapServerCallback-Schnittstelle NAP , OnComplete-Methode
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
ms.openlocfilehash: 16b0eb14663894eb1aac6911659eb452a1d50af59219b9c978215dc96de8a12f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012588"
---
# <a name="inapservercallbackoncomplete-method"></a>INapServerCallback::OnComplete-Methode

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **INapServerCallback::OnComplete-Methode** wird von SHVs verwendet, um den asynchronen Anforderungsabschluss zu signalisieren.

## <a name="syntax"></a>Syntax


```C++
HRESULT OnComplete(
  [in] INapSystemHealthValidationRequest *request,
  [in] HRESULT                           errorCode
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Anforderung* \[ In\]
</dt> <dd>

Ein Zeiger auf ein [**INapSystemHealthValidationRequest-Objekt,**](inapsystemhealthvalidationrequest.md) das eine Validierungsanforderung darstellt.

</dd> <dt>

*errorCode* \[ In\]
</dt> <dd>

Ein [**NAP-Fehlercode,**](nap-error-constants.md) der den Grund angibt, warum die Überprüfung nicht durchgeführt werden konnte.

> [!Note]  
> In der Regel wird der Rückgabewert der [**INapSystemHealthValidationRequest::SetSoHResponse-Methode**](inapsystemhealthvalidationrequest-setsohresponse-method.md) an diesen Parameter übergeben. Wenn **SetSoHResponse** jedoch aufgrund eines Fehlers bei der erneuten Verarbeitung nicht aufgerufen werden konnte, wird der vom fehlerhaften Befehl zurückgegebene Wert übergeben.

 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Andere COM-spezifische Fehlercodes können ebenfalls zurückgegeben werden.



| Rückgabecode                                                                                     | Beschreibung                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Vorgang erfolgreich.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Berechtigungsfehler, Zugriff verweigert.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Systemressourcenlimit, konnte den Vorgang nicht ausführen.<br/> |



 

## <a name="remarks"></a>Hinweise

Validierungsatoren müssen S \_ OK zurückgeben, wenn die [**SoHRequest-Überprüfung**](/windows/win32/api/naptypes/ns-naptypes-soh) abgeschlossen werden kann, unabhängig davon, ob die **SoHRequest** die Integritätsprüfung bestanden hat.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                    |
| Header<br/>                   | <dl> <dt>NapSystemHealthValidator.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapSystemHealthValidator.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qshvhost.dll</dt> </dl>                 |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>


</dt> <dt>

[**INapServerCallback**](inapservercallback.md)
</dt> <dt>

[**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





