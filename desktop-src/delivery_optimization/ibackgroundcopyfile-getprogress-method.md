---
title: IBackgroundCopyFile GetProgress-Methode (Deliveryoptimization.h)
description: Ruft Informationen zum Fortschritt der Dateiübertragung ab.
ms.assetid: 3D8AFD65-AF34-4000-A4A9-8A187427E85C
keywords:
- GetProgress-Methode
- GetProgress-Methode, IBackgroundCopyFile-Schnittstelle
- IBackgroundCopyFile-Schnittstelle, GetProgress-Methode
topic_type:
- apiref
api_name:
- IBackgroundCopyFile.GetProgress
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a7c5fe4a9fcfac86403fd7f4c330d437156e57179b3bf692f53bf3777399b9bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119610500"
---
# <a name="ibackgroundcopyfilegetprogress-method"></a>IBackgroundCopyFile::GetProgress-Methode

Ruft Informationen zum Fortschritt der Dateiübertragung ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetProgress(
  [out] BG_FILE_PROGRESS *pProgress
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pProgress* \[ out\]
</dt> <dd>

Struktur, deren Member den Status der Dateiübertragung angeben. Weitere Informationen zum Typ der verfügbaren Statusinformationen finden Sie in der [**BG_FILE_PROGRESS**](bg-file-progress.md) Struktur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt **S_OK** bei Erfolg oder einen der STANDARDMÄßIGEN COM **HRESULT-Werte** bei einem Fehler zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, version 1709 desktop apps only (Nur Desktop-Apps der Version 1709) \[\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, version 1709 desktop apps only (Nur \[ Desktop-Apps der Version 1709)\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyFile ist als 01B7BD23-FB88-4A77-8490-5891D3E4653A definiert.<br/>              |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**BG_FILE_PROGRESS**](bg-file-progress.md)
</dt> <dt>

[**IBackgroundCopyFile**](ibackgroundcopyfile.md)
</dt> <dt>

[**IBackgroundCopyJob::GetProgress**](ibackgroundcopyjob-getprogress.md)
</dt> </dl>

 

 





