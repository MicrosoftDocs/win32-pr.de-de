---
title: Methode "ibackgroundcopyjob Complete" (deliveryoptimization. h)
description: Beendet den Auftrag und speichert die übertragenen Dateien auf dem Client.
ms.assetid: A3706DBA-C44E-4F7A-A787-62FB436706FC
keywords:
- Complete-Methode
- Complete-Methode, ibackgroundcopyjob-Schnittstelle
- Ibackgroundcopyjob-Schnittstelle, Complete-Methode
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.Complete
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 72383bb235d31043f781998324891b6df134e6ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103658"
---
# <a name="ibackgroundcopyjobcomplete-method"></a>Ibackgroundcopyjob:: Complete-Methode

Beendet den Auftrag und speichert die übertragenen Dateien auf dem Client.

## <a name="syntax"></a>Syntax


```C++
HRESULT Complete();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt die folgenden **HRESULT** -Werte zurück. Die-Methode kann auch Fehler im Zusammenhang mit dem Umbenennen der temporären Kopien der übertragenen Dateien in Ihre angegebenen Namen zurückgeben.



| Rückgabecode                                                                                          | Beschreibung                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl>             | Alle Dateien wurden erfolgreich übertragen.<br/>                                                                                                                                                         |
| <dl> <dt>**DO_E_INVALID_STATE**</dt> </dl> | Für Downloads kann der Status des Auftrags nicht BG_JOB_STATE_CANCELLED oder BG_JOB_STATE_ACKNOWLEDGED sein. <br/> Für Uploads muss der Status des Auftrags BG_JOB_STATE_TRANSFERRED sein.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Alle Dateien wurden erfolgreich übertragen, wenn der Status des Auftrags **BG_JOB_STATE_TRANSFERRED** ist. Um den Status des Auftrags zu überprüfen, müssen Sie die [**ibackgroundcopyjob:: GetState**](ibackgroundcopyjob-getstate.md) -Methode aufrufen. Sie können auch die [**ibackgroundcopycallback**](ibackgroundcopycallback.md) -Schnittstelle implementieren, um eine Benachrichtigung zu erhalten, wenn alle Dateien an den Client übertragen wurden.

Behält Aufträge bei, die weniger als 30 Tage sind. Alle älteren Aufträge werden entfernt. Die Gruppenrichtlinie " [jobinactivitytimeout](https://www.bing.com/search?q=JobInactivityTimeout) " wird von nicht unterstützt.

Für Download Aufträge können Sie während des Übertragungs Vorgangs jederzeit die **Complete** -Methode abrufen. Allerdings werden nur Dateien gespeichert, die vor dem Aufruf dieser Methode erfolgreich an den Client übertragen wurden. Wenn Sie z. b. die **Complete** -Methode aufzurufen, während die dritte von fünf Dateien verarbeitet, werden nur die ersten beiden Dateien gespeichert. Um zu ermitteln, welche Dateien übertragen wurden, müssen Sie die [**ibackgroundcopyfile:: GetProgress**](ibackgroundcopyfile-getprogress-method.md) -Methode aufrufen und den **bytesTransferred** -Member mit dem **bytesTotal** -Member der [**BG_FILE_PROGRESS**](bg-file-progress.md) Struktur vergleichen.

Bei Uploadaufträgen können Sie die **Complete** -Methode nur dann aufzurufen, wenn der Status des Auftrags **BG_JOB_STATE_TRANSFERRED** ist.

Der Besitzer der Datei ist der Benutzer, der den-Befehl durchgeführt hat. Wenn ein Administrator beispielsweise den Auftrag eines anderen Benutzers abschließt, ist der Administrator nicht der Besitzer des Auftrags, der die Datei besitzt.

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

[**Ibackgroundcopyjob:: Cancel**](ibackgroundcopyjob-cancel.md)
</dt> <dt>

[**Ibackgroundcopyjob:: GetState**](ibackgroundcopyjob-getstate.md)
</dt> </dl>

 

 





