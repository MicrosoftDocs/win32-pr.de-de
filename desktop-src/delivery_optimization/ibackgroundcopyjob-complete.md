---
title: IBackgroundCopyJob Complete-Methode (Deliveryoptimization.h)
description: Beendet den Auftrag und speichert die übertragenen Dateien auf dem Client.
ms.assetid: A3706DBA-C44E-4F7A-A787-62FB436706FC
keywords:
- Complete-Methode
- Complete-Methode, IBackgroundCopyJob-Schnittstelle
- IBackgroundCopyJob-Schnittstelle, Complete-Methode
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
ms.openlocfilehash: 72ace8890e724e529e96c5292a439042f13bc2bfad77e6d990a6dbb2fa18f5d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736225"
---
# <a name="ibackgroundcopyjobcomplete-method"></a>IBackgroundCopyJob::Complete-Methode

Beendet den Auftrag und speichert die übertragenen Dateien auf dem Client.

## <a name="syntax"></a>Syntax


```C++
HRESULT Complete();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt die folgenden **HRESULT-Werte** zurück. Die -Methode kann auch Fehler im Zusammenhang mit dem Umbenennen der temporären Kopien der übertragenen Dateien in ihre Vornamen zurückgeben.



| Rückgabecode                                                                                          | Beschreibung                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S_OK</dt> </dl>             | Alle Dateien wurden erfolgreich übertragen.<br/>                                                                                                                                                         |
| <dl> <dt>**DO_E_INVALID_STATE**</dt> </dl> | Bei Downloads kann der Status des Auftrags nicht BG_JOB_STATE_CANCELLED oder BG_JOB_STATE_ACKNOWLEDGED werden. <br/> Bei Uploads muss der Status des Auftrags BG_JOB_STATE_TRANSFERRED sein.<br/> |



 

## <a name="remarks"></a>Hinweise

Alle Dateien wurden erfolgreich übertragen, wenn der Status des Auftrags **BG_JOB_STATE_TRANSFERRED** ist. Rufen Sie die [**IBackgroundCopyJob::GetState-Methode auf,**](ibackgroundcopyjob-getstate.md) um den Status des Auftrags zu überprüfen. Sie können auch die [**IBackgroundCopyCallback-Schnittstelle**](ibackgroundcopycallback.md) implementieren, um Benachrichtigungen zu erhalten, wenn alle Dateien an den Client übertragen wurden.

Do behält Aufträge bei, die weniger als 30 Tage dauern. Alle älteren Aufträge werden entfernt. Do unterstützt die [JobInactivityTimeout-Gruppenrichtlinie](https://www.bing.com/search?q=JobInactivityTimeout) nicht.

Für Downloadaufträge können Sie die **Complete-Methode** jederzeit während des Übertragungsvorgangs aufrufen. Allerdings werden nur Dateien gespeichert, die erfolgreich an den Client übertragen wurden, bevor diese Methode aufgerufen wurde. Wenn Sie beispielsweise die **Complete-Methode** aufrufen, während DO die dritte von fünf Dateien verarbeitet, werden nur die ersten beiden Dateien gespeichert. Um zu ermitteln, welche Dateien übertragen wurden, rufen Sie die [**IBackgroundCopyFile::GetProgress-Methode**](ibackgroundcopyfile-getprogress-method.md) auf, und vergleichen Sie den **BytesTransferred-Member** mit dem **BytesTotal-Member** der [**BG_FILE_PROGRESS-Struktur.**](bg-file-progress.md)

Bei Uploadaufträgen können Sie die **Complete-Methode** nur aufrufen, wenn der Status des Auftrags **BG_JOB_STATE_TRANSFERRED** ist.

Der Besitzer der Datei ist der Benutzer, der den Anruf getätigt hat. Wenn beispielsweise ein Administrator den Auftrag einer anderen Person abschließt, besitzt der Administrator nicht der Besitzer des Auftrags die Datei.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, nur Desktop-Apps der Version 1709 \[\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, nur Desktop-Apps der Version 1709 \[\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyJob ist als 37668D37-507E-4160-9316-26306D150B12 definiert.<br/>               |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IBackgroundCopyJob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**IBackgroundCopyJob::Cancel**](ibackgroundcopyjob-cancel.md)
</dt> <dt>

[**IBackgroundCopyJob::GetState**](ibackgroundcopyjob-getstate.md)
</dt> </dl>

 

 





