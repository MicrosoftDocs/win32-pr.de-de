---
title: Ibackgroundcopyjob GetError-Methode (deliveryoptimization. h)
description: Ruft die Fehler Schnittstelle ab, nachdem ein Fehler aufgetreten ist.
ms.assetid: 66891557-C118-4C66-AEFC-D8FD70976B9A
keywords:
- GetError-Methode
- GetError-Methode, ibackgroundcopyjob-Schnittstelle
- Ibackgroundcopyjob-Schnittstelle, GetError-Methode
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetError
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1f2da994da83a786b89adb5ae63104dbaa6e2ef9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391912"
---
# <a name="ibackgroundcopyjobgeterror-method"></a>Ibackgroundcopyjob:: GetError-Methode

Ruft die Fehler Schnittstelle ab, nachdem ein Fehler aufgetreten ist.

Die Übermittlungs Optimierung (Do) generiert ein Fehler Objekt, wenn der Status des Auftrags BG_JOB_STATE_ERROR oder BG_JOB_STATE_TRANSIENT_ERROR ist. Der Dienst erstellt kein Fehler Objekt, wenn ein-Rückruf für eine **ibackgroundcopyxxxx** -Schnittstellen Methode fehlschlägt. Das Error-Objekt ist verfügbar, bis die Daten übertragen werden (der Status des Auftrags ändert sich in BG_JOB_STATE_TRANSFERRING), oder bis die Anwendung beendet wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetError(
  [out] IBackgroundCopyError **ppError
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pperror* \[ vorgenommen\]
</dt> <dd>

Fehler Schnittstelle, die den Fehlercode, eine Beschreibung des Fehlers und den Kontext bereitstellt, in dem der Fehler aufgetreten ist. Dieser Parameter identifiziert außerdem die Datei, die zum Zeitpunkt des Auftretens des Fehlers übertragen wird. Release *pperror* , wenn dies erledigt ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt sowohl die folgenden **HRESULT** -Werte als auch andere zurück.



| Rückgabecode                                                                                                           | Beschreibung                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl>                              | Das Fehler Objekt wurde erfolgreich generiert.<br/>                                                                                                                                                       |
| <dl> <dt>**DO_E_ERROR_INFORMATION_UNAVAILABLE**</dt> </dl> | Die Fehler Schnittstelle ist nur verfügbar, wenn ein Fehler auftritt (BG_JOB_STATE_ERROR oder BG_JOB_STATE_TRANSIENT_ERROR) und bevor mit dem Übertragen von Daten begonnen wird (BG_JOB_STATE_TRANSFERRING).<br/> |



 

## <a name="remarks"></a>Bemerkungen

Der Auftrag wird bei schwerwiegenden Fehlern in einen Fehlerzustand versetzt. Verwenden Sie eine der folgenden Optionen, um zu bestimmen, ob der Auftrag fehlerhaft ist:

-   Rufen Sie die [**ibackgroundcopyjob:: GetState**](ibackgroundcopyjob-getstate.md) -Methode auf, um den Status des Auftrags abzurufen. Der Auftrag ist fehlerhaft, wenn der Status BG_JOB_STATE_ERROR ist.
-   Um Benachrichtigungen zu erhalten, wenn ein Fehler auftritt, implementieren Sie die [**ibackgroundcopycallback**](ibackgroundcopycallback.md) -Schnittstelle (insbesondere die [**joberror**](https://www.bing.com/search?q=**JobError**) -Methode). Rufen Sie dann die [**ibackgroundcopyjob:: setnotifyinterface**](ibackgroundcopyjob-setnotifyinterface.md) -Methode auf, um den Rückruf zu registrieren, und die [**ibackgroundcopyjob:: setnotifyflags**](ibackgroundcopyjob-setnotifyflags.md) -Methode, um das BG_NOTIFY_JOB_ERROR-Flag festzulegen.

Die [**ibackgroundcopyerror**](ibackgroundcopyerror.md) -Schnittstelle enthält Informationen, die Sie verwenden, um die Ursache des Fehlers zu ermitteln, und, wenn der Übertragungsprozess fortgesetzt werden kann. Nachdem Sie die Ursache des Fehlers bestimmt haben, führen Sie eine der folgenden Optionen aus:

-   Um den Auftrag abzubrechen, rufen Sie die [**ibackgroundcopyjob:: Cancel**](ibackgroundcopyjob-cancel.md) -Methode auf.
-   Um die Dateien zu speichern, die vor dem Auftreten des Fehlers erfolgreich übertragen wurden, müssen Sie die [**ibackgroundcopyjob:: Complete**](ibackgroundcopyjob-complete.md) -Methode abrufen.
-   Beheben Sie das Problem, und führen Sie dann die [**ibackgroundcopyjob:: Resume**](ibackgroundcopyjob-resume.md) -Methode aus, um die Verarbeitung des Auftrags abzuschließen.

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

[**Ibackgroundcopycallback:: joberror**](ibackgroundcopycallback-joberror-method.md)
</dt> <dt>

[**Ibackgroundcopyerror**](ibackgroundcopyerror.md)
</dt> <dt>

[**Ibackgroundcopyjob:: GetState**](ibackgroundcopyjob-getstate.md)
</dt> </dl>

 

 





