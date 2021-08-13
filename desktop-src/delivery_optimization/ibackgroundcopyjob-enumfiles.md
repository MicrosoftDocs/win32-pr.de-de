---
title: IBackgroundCopyJob EnumFiles-Methode (Deliveryoptimization.h)
description: Ruft einen IEnumBackgroundCopyFiles-Schnittstellenzeiger ab, den Sie zum Aufzählen der Dateien in einem Auftrag verwenden.
ms.assetid: 94FA5D7B-08C1-497E-9813-571D35AE3BCF
keywords:
- EnumFiles-Methode
- EnumFiles-Methode, IBackgroundCopyJob-Schnittstelle
- IBackgroundCopyJob-Schnittstelle, EnumFiles-Methode
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.EnumFiles
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4ecd27e1de8dfaa16d7f5d2dc3218d3c993148a0878976e329b4953cefdc4c29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118543016"
---
# <a name="ibackgroundcopyjobenumfiles-method"></a>IBackgroundCopyJob::EnumFiles-Methode

Ruft einen [**IEnumBackgroundCopyFiles-Schnittstellenzeiger**](ienumbackgroundcopyfiles-.md) ab, den Sie zum Aufzählen der Dateien in einem Auftrag verwenden.

## <a name="syntax"></a>Syntax


```C++
HRESULT EnumFiles(
  [out] IEnumBackgroundCopyFiles **ppEnumFiles
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppEnumFiles* \[ out\]
</dt> <dd>

[**IEnumBackgroundCopyFiles-Schnittstellenzeiger,**](ienumbackgroundcopyfiles-.md) den Sie zum Aufzählen der Dateien im Auftrag verwenden. Geben *Sie ppEnumFiles frei,* wenn Sie fertig sind.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt **S_OK** bei Erfolg oder einen der STANDARDMÄßIGEN COM **HRESULT-Werte** bei einem Fehler zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10 Desktop-Apps, Version 1709 \[\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, version 1709 desktop apps only (Nur \[ Desktop-Apps der Version 1709)\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyJob ist als 37668D37-507E-4160-9316-26306D150B12 definiert.<br/>               |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**IBackgroundCopyJob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**IEnumBackgroundCopyFiles**](ienumbackgroundcopyfiles-.md)
</dt> </dl>

 

 





