---
title: Ibackgroundcopycallback-joberror-Methode (deliveryoptimization. h)
description: Die Übermittlungs Optimierung (Do) ruft Ihre Implementierung der joberror-Methode auf, wenn sich der Status des Auftrags in "BG_JOB_STATE_ERROR" ändert.
ms.assetid: 121712A5-98EB-4B2F-A004-A3BDF9C1332B
keywords:
- Joberror-Methode
- Joberror-Methode, ibackgroundcopycallback-Schnittstelle
- Ibackgroundcopycallback-Schnittstelle, joberror-Methode
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
ms.openlocfilehash: 0122f5777303506be5fd81d0966b00f828bf2073
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391841"
---
# <a name="ibackgroundcopycallbackjoberror-method"></a>Ibackgroundcopycallback:: joberror-Methode

Die Übermittlungs Optimierung (Do) ruft Ihre Implementierung der [**joberror**](https://www.bing.com/search?q=**JobError**) -Methode auf, wenn sich der Status des Auftrags in "BG_JOB_STATE_ERROR" ändert.

## <a name="syntax"></a>Syntax


```C++
HRESULT JobError(
  [in] IBackgroundCopyJob   *pJob,
  [in] IBackgroundCopyError *pError
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pjob* \[ in\]
</dt> <dd>

Enthält auftragsbezogene Informationen, wie z. b. die Anzahl von Bytes und Dateien, die vor dem Auftreten des Fehlers übertragen wurden. Außerdem enthält es die Methoden zum fortsetzen und Abbrechen des Auftrags. *Pjob* nicht freigeben; Gibt die-Schnittstelle frei, wenn die [**joberror**](https://www.bing.com/search?q=**JobError**) -Methode zurückgibt.

</dd> <dt>

*perror* \[ in\]
</dt> <dd>

Enthält Fehlerinformationen, wie z. b. die Datei, die zu dem Zeitpunkt, zu dem ein schwerwiegender Fehler aufgetreten ist, und eine Beschreibung des Fehlers. Kein Release von *perror*; Gibt die-Schnittstelle frei, wenn die [**joberror**](https://www.bing.com/search?q=**JobError**) -Methode zurückgibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode sollte **S_OK** zurückgeben. Andernfalls wird diese Methode weiterhin aufgerufen, bis **S_OK** zurückgegeben wird. Aus Leistungsgründen sollten Sie begrenzen, wie oft ein anderer Wert als **S_OK** zurückgegeben werden soll. Als Alternative zum Zurückgeben eines Fehlercodes sollten Sie die Rückgabe von **S_OK** und die interne Behandlung des Fehlers in Erwägung gezogen. Das Intervall, in dem diese Methode aufgerufen wird, ist willkürlich.

## <a name="remarks"></a>Bemerkungen

Nachdem Sie die Ursache des Fehlers bestimmt haben, führen Sie eine der folgenden Optionen aus:

-   Um den Auftrag abzubrechen, rufen Sie die [**ibackgroundcopyjob:: Cancel**](ibackgroundcopyjob-cancel.md) -Methode auf.
-   Um den Teil des Auftrags zu akzeptieren, der vor dem Auftreten des Fehlers erfolgreich übertragen wurde, können Sie die [**ibackgroundcopyjob:: Complete**](ibackgroundcopyjob-complete.md) -Methode abrufen. Diese Option gilt nicht für Aufträge zum hochladen. ein Teil eines uploadauftrags kann nicht ausgeführt werden.
-   Beheben Sie das Problem, und führen Sie dann die [**ibackgroundcopyjob:: Resume**](ibackgroundcopyjob-resume.md) -Methode aus, um die Verarbeitung des Auftrags abzuschließen.

Vorübergehende Fehler generieren keine Aufrufe der [**joberror**](https://www.bing.com/search?q=**JobError**) -Methode.

Gibt BG_ERROR_CONTEXT_REMOTE_FILE zurück, wenn der Auftrag einen HTTP 403-Fehler ausgelöst hat, andernfalls BG_ERROR_CONTEXT_NONE.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1709, \[ nur Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, Version 1709, \[ nur Desktop-Apps\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Deliveryoptimization. idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyCallback ist als 97ea99c7-0186-4ad4-8df9-c5b4e0ed6b22 definiert.<br/>          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ibackgroundcopycallback**](ibackgroundcopycallback.md)
</dt> <dt>

[**Ibackgroundcopyerror**](ibackgroundcopyerror.md)
</dt> <dt>

[**IBackgroundCopyJob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**Ibackgroundcopyjob:: Cancel**](ibackgroundcopyjob-cancel.md)
</dt> <dt>

[**Ibackgroundcopyjob:: Resume**](ibackgroundcopyjob-resume.md)
</dt> </dl>

 

 





