---
title: IBackgroundCopyCallback JobTransferred-Methode (Deliveryoptimization.h)
description: Übermittlungsoptimierung (DO) ruft Ihre Implementierung der JobTransferred-Methode auf, wenn alle Dateien im Auftrag erfolgreich übertragen wurden.
ms.assetid: D3088279-2D26-4707-9BA2-19D2758EA1CC
keywords:
- JobTransferred-Methode
- JobTransferred-Methode, IBackgroundCopyCallback-Schnittstelle
- IBackgroundCopyCallback-Schnittstelle, JobTransferred-Methode
topic_type:
- apiref
api_name:
- IBackgroundCopyCallback.JobTransferred
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 69cf1a739e15bc7341769bdc01549ad439a1c93877f653f0689e686eb8bac1f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047098"
---
# <a name="ibackgroundcopycallbackjobtransferred-method"></a>IBackgroundCopyCallback::JobTransferred-Methode

Übermittlungsoptimierung (DO) ruft Ihre Implementierung der **JobTransferred-Methode** auf, wenn alle Dateien im Auftrag erfolgreich übertragen wurden.

## <a name="syntax"></a>Syntax


```C++
HRESULT JobTransferred(
  [in] IBackgroundCopyJob *pJob
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pJob* \[ In\]
</dt> <dd>

Enthält auftragsbezogene Informationen, z. B. die Zeit, zu der der Auftrag abgeschlossen wurde, die Anzahl der übertragenen Bytes und die Anzahl der übertragenen Dateien. Geben Sie *pJob nicht frei.* DO gibt die Schnittstelle frei, wenn die Methode zurückgegeben wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode sollte die S_OK.

## <a name="remarks"></a>Hinweise

In der Regel sollte Ihre Implementierung die [**IBackgroundCopyJob::Complete-Methode**](ibackgroundcopyjob-complete.md) aufrufen, um zu bestätigen, dass DO die Dateien erfolgreich übertragen hat. Downloaddateien und die Antwortdatei sind erst auf dem Client verfügbar, wenn Sie die **Complete-Methode** aufrufen.

Wenn Sie die [**Complete-Methode**](ibackgroundcopyjob-complete.md) oder [**die IBackgroundCopyJob::Cancel-Methode**](ibackgroundcopyjob-cancel.md) nicht aufrufen, bricht DO den Auftrag nach 30 Tagen ab und löscht die unvollständigen Dateien.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, version 1709 desktop apps only (Nur \[ Desktop-Apps der Version 1709)\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, version 1709 desktop apps only (Nur \[ Desktop-Apps der Version 1709)\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyCallback ist als 97EA99C7-0186-4AD4-8DF9-C5B4E0ED6B22 definiert.<br/>          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IBackgroundCopyCallback**](ibackgroundcopycallback.md)
</dt> <dt>

[**IBackgroundCopyJob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**IBackgroundCopyJob::Complete**](ibackgroundcopyjob-complete.md)
</dt> <dt>

[**IBackgroundCopyJob::Cancel**](ibackgroundcopyjob-cancel.md)
</dt> </dl>

 

 





