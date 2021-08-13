---
title: IEnumBackgroundCopyFiles GetCount-Methode (Deliveryoptimization.h)
description: Ruft die Anzahl der Dateien in der -Enumeration ab.
ms.assetid: EE27679D-3AC0-49DA-992F-8DEA10C21646
keywords:
- GetCount-Methode
- GetCount-Methode, IEnumBackgroundCopyFiles-Schnittstelle
- IEnumBackgroundCopyFiles-Schnittstelle, GetCount-Methode
topic_type:
- apiref
api_name:
- IEnumBackgroundCopyFiles.GetCount
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f67ee932079a7c67619fe769cbe5d1b6705261655853f1adccb14bf5d12eecf2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119409910"
---
# <a name="ienumbackgroundcopyfilesgetcount-method"></a>IEnumBackgroundCopyFiles::GetCount-Methode

Ruft die Anzahl der Dateien in der -Enumeration ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetCount(
  [out] ULONG *pCount
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pCount* \[ out\]
</dt> <dd>

Anzahl der Dateien in der Enumeration.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt **S_OK** bei Erfolg oder einen der COM **HRESULT-Standardwerte** bei Einem Fehler zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, nur Desktop-Apps der Version 1709 \[\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, nur Desktop-Apps der Version 1709 \[\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IEnumBackgroundCopyFiles ist als CA51E165-C365-424C-8D41-24AAA4FF3C40 definiert.<br/>         |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IEnumBackgroundCopyFiles**](ienumbackgroundcopyfiles-.md)
</dt> </dl>

 

 





