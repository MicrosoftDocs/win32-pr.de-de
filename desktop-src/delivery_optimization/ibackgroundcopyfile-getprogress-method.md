---
title: Ibackgroundcopyfile GetProgress-Methode (deliveryoptimization. h)
description: Ruft Informationen zum Fortschritt der Dateiübertragung ab.
ms.assetid: 3D8AFD65-AF34-4000-A4A9-8A187427E85C
keywords:
- GetProgress-Methode
- GetProgress-Methode, ibackgroundcopyfile-Schnittstelle
- Ibackgroundcopyfile-Schnittstelle, GetProgress-Methode
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
ms.openlocfilehash: f0828105822700f9d34cd180c8877634bc3a6013
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476374"
---
# <a name="ibackgroundcopyfilegetprogress-method"></a>Ibackgroundcopyfile:: GetProgress-Methode

Ruft Informationen zum Fortschritt der Dateiübertragung ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetProgress(
  [out] BG_FILE_PROGRESS *pProgress
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pprogress* \[ vorgenommen\]
</dt> <dd>

-Struktur, deren Elemente den Fortschritt der Dateiübertragung angeben. Ausführliche Informationen zu den verfügbaren Fortschrittsinformationen finden Sie in der [**BG_FILE_PROGRESS**](bg-file-progress.md) -Struktur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt **S_OK** bei Erfolg oder einen der standardmäßigen com **HRESULT** -Werte bei einem Fehler zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1709, \[ nur Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, Version 1709, \[ nur Desktop-Apps\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Deliveryoptimization. idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyFile ist als 01b7bd23-B88-4a77-8490-5891d3e4653a definiert.<br/>              |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**BG_FILE_PROGRESS**](bg-file-progress.md)
</dt> <dt>

[**Ibackgroundcopyfile**](ibackgroundcopyfile.md)
</dt> <dt>

[**Ibackgroundcopyjob:: GetProgress**](ibackgroundcopyjob-getprogress.md)
</dt> </dl>

 

 





