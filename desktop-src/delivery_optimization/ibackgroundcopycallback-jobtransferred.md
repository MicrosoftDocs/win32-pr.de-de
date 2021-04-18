---
title: Ibackgroundcopycallback-jobtransfer-Methode (deliveryoptimization. h)
description: Die Übermittlungs Optimierung (Do) ruft Ihre Implementierung der jobübertragene Methode auf, wenn alle Dateien im Auftrag erfolgreich übertragen wurden.
ms.assetid: D3088279-2D26-4707-9BA2-19D2758EA1CC
keywords:
- Jobübertragene Methode
- Jobtransfer-Methode, ibackgroundcopycallback-Schnittstelle
- Ibackgroundcopycallback-Schnittstelle, jobtransfer-Methode
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
ms.openlocfilehash: 6c5c358978da1731152ca6f7de8c3f7a92a1da86
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103514"
---
# <a name="ibackgroundcopycallbackjobtransferred-method"></a>Ibackgroundcopycallback:: jobtransfer-Methode

Die Übermittlungs Optimierung (Do) ruft Ihre Implementierung der **jobübertragene** Methode auf, wenn alle Dateien im Auftrag erfolgreich übertragen wurden.

## <a name="syntax"></a>Syntax


```C++
HRESULT JobTransferred(
  [in] IBackgroundCopyJob *pJob
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pjob* \[ in\]
</dt> <dd>

Enthält auftragsbezogene Informationen, wie z. b. den Zeitpunkt, zu dem der Auftrag abgeschlossen wurde, die Anzahl der übertragenen Bytes und die Anzahl der übertragenen Dateien. *Pjob* nicht freigeben; Gibt die-Schnittstelle frei, wenn die-Methode zurückgibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode sollte S_OK zurückgeben.

## <a name="remarks"></a>Bemerkungen

In der Regel sollte Ihre Implementierung die [**ibackgroundcopyjob:: Complete**](ibackgroundcopyjob-complete.md) -Methode anrufen, um zu bestätigen, dass die Dateien erfolgreich übertragen wurden. Download Dateien und die Antwortdatei sind auf dem Client erst verfügbar, wenn Sie die **Complete** -Methode aufgerufen haben.

Wenn Sie die [**Complete**](ibackgroundcopyjob-complete.md) -Methode oder die [**ibackgroundcopyjob:: Cancel**](ibackgroundcopyjob-cancel.md) -Methode nicht aufzurufen, wird der Auftrag nach 30 Tagen abgebrochen, und die unvollständigen Dateien werden gelöscht.

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

[**IBackgroundCopyJob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**Ibackgroundcopyjob:: Complete**](ibackgroundcopyjob-complete.md)
</dt> <dt>

[**Ibackgroundcopyjob:: Cancel**](ibackgroundcopyjob-cancel.md)
</dt> </dl>

 

 





