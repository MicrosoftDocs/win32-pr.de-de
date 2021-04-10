---
title: Ibackgroundcopyjob setnoprogresstimeout-Methode (deliveryoptimization. h)
description: Legt die Zeitspanne fest, die die Übermittlungs Optimierung (Do) versucht, die Datei zu übertragen, nachdem ein vorübergehender Fehler aufgetreten ist. Bei einem Fortschritt wird der Timer zurückgesetzt.
ms.assetid: DC86F74F-8429-4D78-B425-CAF19867B05E
keywords:
- Setnoprogresstimeout-Methode
- Setnoprogresstimeout-Methode, ibackgroundcopyjob-Schnittstelle
- Ibackgroundcopyjob-Schnittstelle, setnoprogresstimeout-Methode
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.SetNoProgressTimeout
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 276c8c44d2b2b034543aae25361c5f5c94046f5d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040674"
---
# <a name="ibackgroundcopyjobsetnoprogresstimeout-method"></a>Ibackgroundcopyjob:: setnoprogresstimeout-Methode

Legt die Zeitspanne fest, die die Übermittlungs Optimierung (Do) versucht, die Datei zu übertragen, nachdem ein vorübergehender Fehler aufgetreten ist. Bei einem Fortschritt wird der Timer zurückgesetzt.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetNoProgressTimeout(
  [in] ULONG RetryPeriod
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*RetryPeriod* \[ in\]
</dt> <dd>

Die Zeitspanne in Sekunden, die versucht, die Datei zu übertragen, nachdem kein Fortschritt unternommen wurde. Der standardmäßige Wiederholungs Zeitraum für einen Auftrag mit hoher Priorität beträgt 3600 Sekunden (1 Stunde), und für einen Auftrag mit niedriger Priorität beträgt der Wert 86400 Sekunden (24 Stunden).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt sowohl die folgenden **HRESULT** -Werte als auch andere zurück.



| Rückgabecode                                                                                          | Beschreibung                                                                                          |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl>             | Der Wiederholungs Zeitraum wurde erfolgreich festgelegt.<br/>                                                            |
| <dl> <dt>**DO_E_INVALID_STATE**</dt> </dl> | Der Status des Auftrags kann nicht BG_JOB_STATE_CANCELLED oder BG_JOB_STATE_ACKNOWLEDGED sein.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Wenn der Vorgang während des Wiederholungs Zeitraums nicht fortgesetzt wird, wird der Status des Auftrags von BG_JOB_STATE_TRANSIENT_ERROR in BG_JOB_STATE_ERROR verschoben. Wenn Sie eine Fehler Benachrichtigung anfordern, wird Ihr [**joberror**](https://www.bing.com/search?q=**JobError**) -Rückruf aufgerufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1709, \[ nur Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, Version 1709, \[ nur Desktop-Apps\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Deliveryoptimization. idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyJob ist als 37668d37-507E-4160-9316-26306d150b12 definiert.<br/>               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IBackgroundCopyJob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**Ibackgroundcopyjob:: getnoprogresstimeout**](ibackgroundcopyjob-getnoprogresstimeout.md)
</dt> </dl>

 

 





