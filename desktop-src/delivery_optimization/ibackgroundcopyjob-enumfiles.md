---
title: Ibackgroundcopyjob-EnumFiles-Methode (deliveryoptimization. h)
description: Ruft einen ienumbackgroundcopyfiles-Schnittstellen Zeiger ab, mit dem Sie die Dateien in einem Auftrag aufzählen.
ms.assetid: 94FA5D7B-08C1-497E-9813-571D35AE3BCF
keywords:
- EnumFiles-Methode
- EnumFiles-Methode, ibackgroundcopyjob-Schnittstelle
- Ibackgroundcopyjob-Schnittstelle, EnumFiles-Methode
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
ms.openlocfilehash: a4b0315f98594357d67fd5dbfed3bf2561f41f71
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104073"
---
# <a name="ibackgroundcopyjobenumfiles-method"></a>Ibackgroundcopyjob:: EnumFiles-Methode

Ruft einen [**ienumbackgroundcopyfiles**](ienumbackgroundcopyfiles-.md) -Schnittstellen Zeiger ab, mit dem Sie die Dateien in einem Auftrag aufzählen.

## <a name="syntax"></a>Syntax


```C++
HRESULT EnumFiles(
  [out] IEnumBackgroundCopyFiles **ppEnumFiles
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

" *ppumschlag files* \[ " vorgenommen\]
</dt> <dd>

[**Ienumbackgroundcopyfiles**](ienumbackgroundcopyfiles-.md) -Schnittstellen Zeiger, mit dem die Dateien im Auftrag aufgelistet werden. Geben Sie nach Abschluss " *ppumschlag files* " frei.

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
| IID<br/>                      | IID_IBackgroundCopyJob ist als 37668d37-507E-4160-9316-26306d150b12 definiert.<br/>               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IBackgroundCopyJob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**Ienumbackgroundcopyfiles**](ienumbackgroundcopyfiles-.md)
</dt> </dl>

 

 





