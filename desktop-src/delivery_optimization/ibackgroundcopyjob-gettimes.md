---
title: Ibackgroundcopyjob gettimes-Methode (deliveryoptimization. h)
description: Ruft auftragsbezogene Zeitstempel ab, z. b. den Zeitpunkt, zu dem der Auftrag erstellt oder zuletzt geändert wurde.
ms.assetid: 9002FB8D-08CB-4878-980F-15FE0DC952A6
keywords:
- Gettimes-Methode
- Gettimes-Methode, ibackgroundcopyjob-Schnittstelle
- Ibackgroundcopyjob-Schnittstelle, gettimes-Methode
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetTimes
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 04e779b59e0976e77b287bc575f3b08f8d39340a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477031"
---
# <a name="ibackgroundcopyjobgettimes-method"></a>Ibackgroundcopyjob:: gettimes-Methode

Ruft auftragsbezogene Zeitstempel ab, z. b. den Zeitpunkt, zu dem der Auftrag erstellt oder zuletzt geändert wurde.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetTimes(
  [out] BG_JOB_TIMES *pTimes
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ptimes* \[ vorgenommen\]
</dt> <dd>

Enthält auftragsbezogene Zeitstempel. Informationen zu verfügbaren Zeitstempeln finden Sie in der [**BG_JOB_TIMES**](bg-job-times.md) -Struktur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt sowohl die folgenden **HRESULT** -Werte als auch andere zurück.



| Rückgabecode                                                                              | Beschreibung                                         |
|------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl> | Die Zeitstempel konnten erfolgreich abgerufen werden.<br/> |



 

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

[**BG_JOB_TIMES**](bg-job-times.md)
</dt> </dl>

 

 





