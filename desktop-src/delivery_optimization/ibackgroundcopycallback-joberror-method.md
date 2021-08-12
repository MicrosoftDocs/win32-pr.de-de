---
title: IBackgroundCopyCallback JobError-Methode (Deliveryoptimization.h)
description: Übermittlungsoptimierung (DO) ruft Ihre Implementierung der JobError-Methode auf, wenn sich der Status des Auftrags in BG_JOB_STATE_ERROR.
ms.assetid: 121712A5-98EB-4B2F-A004-A3BDF9C1332B
keywords:
- JobError-Methode
- JobError-Methode, IBackgroundCopyCallback-Schnittstelle
- IBackgroundCopyCallback-Schnittstelle, JobError-Methode
topic_type:
- apiref
api_name:
- IBackgroundCopyCallback.JobError
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 307ab18a0f956e5a2f4f14e9782f90b8ec6bff723da04aa9866566d95c53dca7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118543132"
---
# <a name="ibackgroundcopycallbackjoberror-method"></a>IBackgroundCopyCallback::JobError-Methode

Übermittlungsoptimierung (DO) ruft Ihre Implementierung der [**JobError-Methode**](https://www.bing.com/search?q=**JobError**) auf, wenn sich der Status des Auftrags in BG_JOB_STATE_ERROR.

## <a name="syntax"></a>Syntax


```C++
HRESULT JobError(
  [in] IBackgroundCopyJob   *pJob,
  [in] IBackgroundCopyError *pError
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pJob* \[ In\]
</dt> <dd>

Enthält auftragsbezogene Informationen, z. B. die Anzahl der Bytes und Dateien, die vor dem Fehler übertragen wurden. Sie enthält auch die Methoden zum Fortsetzen und Abbrechen des Auftrags. Geben Sie *pJob nicht frei.* DO gibt die Schnittstelle frei, wenn die [**JobError-Methode**](https://www.bing.com/search?q=**JobError**) zurückgegeben wird.

</dd> <dt>

*pError* \[ In\]
</dt> <dd>

Enthält Fehlerinformationen, z. B. die Datei, die zum Zeitpunkt des schwerwiegenden Fehlers verarbeitet wird, und eine Beschreibung des Fehlers. Geben Sie *pError nicht frei.* DO gibt die Schnittstelle frei, wenn die [**JobError-Methode**](https://www.bing.com/search?q=**JobError**) zurückgegeben wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode sollte **S_OK.** Andernfalls wird diese Methode von DO weiterhin verwendet, **bis S_OK** zurückgegeben wird. Aus Leistungsgründen sollten Sie die Anzahl der Rückgaben eines anderen Werts als S_OK auf **einige** Male beschränken. Als Alternative zur Rückgabe eines Fehlercodes  sollten Sie in Betracht ziehen, immer S_OK und den Fehler intern zu behandeln. Das Intervall, in dem diese Methode aufgerufen wird, ist beliebig.

## <a name="remarks"></a>Hinweise

Nachdem Sie die Ursache des Fehlers ermittelt haben, führen Sie eine der folgenden Optionen aus:

-   Rufen Sie zum Abbrechen des Auftrags die [**IBackgroundCopyJob::Cancel-Methode**](ibackgroundcopyjob-cancel.md) auf.
-   Um den Teil des Auftrags zu akzeptieren, der vor dem Fehler erfolgreich übertragen wurde, rufen Sie die [**IBackgroundCopyJob::Complete-Methode**](ibackgroundcopyjob-complete.md) auf. Diese Option gilt nicht für Uploadaufträge. Sie können einen Teil eines Uploadauftrags nicht abschließen.
-   Beheben Sie das Problem, und rufen Sie dann die [**IBackgroundCopyJob::Resume-Methode**](ibackgroundcopyjob-resume.md) auf, um die Verarbeitung des Auftrags fertig zu stellen.

Vorübergehende Fehler generieren keine Aufrufe der [**JobError-Methode.**](https://www.bing.com/search?q=**JobError**)

DO gibt BG_ERROR_CONTEXT_REMOTE_FILE zurück, wenn für den Auftrag ein HTTP 403-Fehler aufgetreten ist, BG_ERROR_CONTEXT_NONE andernfalls .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10 Desktop-Apps, Version 1709 \[\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, version 1709 desktop apps only (Nur \[ Desktop-Apps der Version 1709)\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyCallback ist als 97EA99C7-0186-4AD4-8DF9-C5B4E0ED6B22 definiert.<br/>          |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**IBackgroundCopyCallback**](ibackgroundcopycallback.md)
</dt> <dt>

[**IBackgroundCopyError**](ibackgroundcopyerror.md)
</dt> <dt>

[**IBackgroundCopyJob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**IBackgroundCopyJob::Cancel**](ibackgroundcopyjob-cancel.md)
</dt> <dt>

[**IBackgroundCopyJob::Resume**](ibackgroundcopyjob-resume.md)
</dt> </dl>

 

 





