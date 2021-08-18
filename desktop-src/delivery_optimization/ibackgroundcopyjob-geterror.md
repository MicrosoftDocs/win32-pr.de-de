---
title: IBackgroundCopyJob GetError-Methode (Deliveryoptimization.h)
description: Ruft die Fehlerschnittstelle ab, nachdem ein Fehler aufgetreten ist.
ms.assetid: 66891557-C118-4C66-AEFC-D8FD70976B9A
keywords:
- GetError-Methode
- GetError-Methode, IBackgroundCopyJob-Schnittstelle
- IBackgroundCopyJob-Schnittstelle, GetError-Methode
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
ms.openlocfilehash: 016f11023d50d7ea1fa9024e270a7ebce0597e07d5c33a915facae47773759c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755510"
---
# <a name="ibackgroundcopyjobgeterror-method"></a>IBackgroundCopyJob::GetError-Methode

Ruft die Fehlerschnittstelle ab, nachdem ein Fehler aufgetreten ist.

Übermittlungsoptimierung (DO) generiert ein Fehlerobjekt, wenn der Status des Auftrags BG_JOB_STATE_ERROR oder BG_JOB_STATE_TRANSIENT_ERROR. Der Dienst erstellt kein Fehlerobjekt, wenn ein Aufruf einer **IBackgroundCopyXXXX-Schnittstellenmethode** fehlschlägt. Das Fehlerobjekt ist verfügbar, bis do mit der Übertragung von Daten beginnt (der Status des Auftrags ändert sich in BG_JOB_STATE_TRANSFERRING), oder bis Ihre Anwendung beendet wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetError(
  [out] IBackgroundCopyError **ppError
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppError* \[ out\]
</dt> <dd>

Fehlerschnittstelle, die den Fehlercode, eine Beschreibung des Fehlers und den Kontext enthält, in dem der Fehler aufgetreten ist. Dieser Parameter identifiziert auch die Datei, die zum Zeitpunkt des Fehlers übertragen wird. Geben Sie *ppError frei,* wenn Sie fertig sind.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt die folgenden **HRESULT-Werte** sowie andere zurück.



| Rückgabecode                                                                                                           | Beschreibung                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S_OK S_OK</dt> </dl>                              | Das Fehlerobjekt wurde erfolgreich generiert.<br/>                                                                                                                                                       |
| <dl> <dt>**DO_E_ERROR_INFORMATION_UNAVAILABLE**</dt> </dl> | Die Fehlerschnittstelle ist nur verfügbar, nachdem ein Fehler aufgetreten ist (BG_JOB_STATE_ERROR oder BG_JOB_STATE_TRANSIENT_ERROR) und bevor do mit der Übertragung von Daten beginnt (BG_JOB_STATE_TRANSFERRING).<br/> |



 

## <a name="remarks"></a>Hinweise

Der Auftrag wird bei schwerwiegenden Fehlern in einen Fehlerzustand gesetzt. Verwenden Sie eine der folgenden Optionen, um zu ermitteln, ob der Auftrag einen Fehler auft:

-   Um den Status des Auftrags zu erhalten, rufen Sie die [**IBackgroundCopyJob::GetState-Methode**](ibackgroundcopyjob-getstate.md) auf. Der Auftrag ist nicht fehlerfrei, wenn der Status BG_JOB_STATE_ERROR.
-   Um eine Benachrichtigung zu erhalten, wenn ein Fehler auftritt, implementieren Sie die [**IBackgroundCopyCallback-Schnittstelle**](ibackgroundcopycallback.md) (insbesondere die [**JobError-Methode).**](https://www.bing.com/search?q=**JobError**) Rufen Sie dann die [**IBackgroundCopyJob::SetNotifyInterface-Methode**](ibackgroundcopyjob-setnotifyinterface.md) auf, um den Rückruf zu registrieren, und die [**IBackgroundCopyJob::SetNotifyFlags-Methode,**](ibackgroundcopyjob-setnotifyflags.md) um das BG_NOTIFY_JOB_ERROR festlegen.

Die [**IBackgroundCopyError-Schnittstelle**](ibackgroundcopyerror.md) enthält Informationen, mit denen Sie die Ursache des Fehlers bestimmen und ob der Übertragungsprozess fortgesetzt werden kann. Nachdem Sie die Ursache des Fehlers ermittelt haben, führen Sie eine der folgenden Optionen aus:

-   Rufen Sie zum Abbrechen des Auftrags die [**IBackgroundCopyJob::Cancel-Methode**](ibackgroundcopyjob-cancel.md) auf.
-   Um die Dateien zu speichern, die vor dem Fehler erfolgreich übertragen wurden, rufen Sie die [**IBackgroundCopyJob::Complete-Methode**](ibackgroundcopyjob-complete.md) auf.
-   Beheben Sie das Problem, und rufen Sie dann die [**IBackgroundCopyJob::Resume-Methode**](ibackgroundcopyjob-resume.md) auf, um die Verarbeitung des Auftrags fertig zu stellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, version 1709 desktop apps only (Nur Desktop-Apps der Version 1709) \[\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, version 1709 desktop apps only (Nur \[ Desktop-Apps der Version 1709)\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyJob ist als 37668D37-507E-4160-9316-26306D150B12 definiert.<br/>               |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IBackgroundCopyJob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**IBackgroundCopyCallback::JobError**](ibackgroundcopycallback-joberror-method.md)
</dt> <dt>

[**IBackgroundCopyError**](ibackgroundcopyerror.md)
</dt> <dt>

[**IBackgroundCopyJob::GetState**](ibackgroundcopyjob-getstate.md)
</dt> </dl>

 

 





