---
title: IEnumBackgroundCopyFiles Next-Methode (Deliveryoptimization.h)
description: Ruft eine angegebene Anzahl von Elementen in der Enumerationsfolge ab. Wenn weniger Elemente als die angeforderte Anzahl von Elementen in der Sequenz übrig sind, werden die verbleibenden Elemente abgerufen.
ms.assetid: 31E603EC-2684-487D-AB37-4C6A6F661298
keywords:
- Nächste Methode
- Nächste Methode, IEnumBackgroundCopyFiles-Schnittstelle
- IEnumBackgroundCopyFiles-Schnittstelle, Next-Methode
topic_type:
- apiref
api_name:
- IEnumBackgroundCopyFiles.Next
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3dcf24c65b7f282b1a1e15d3109ce1af9ccfc0af6436c80c94760f0b4cd18069
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119461880"
---
# <a name="ienumbackgroundcopyfilesnext-method"></a>IEnumBackgroundCopyFiles::Next-Methode

Ruft eine angegebene Anzahl von Elementen in der Enumerationsfolge ab. Wenn weniger Elemente als die angeforderte Anzahl von Elementen in der Sequenz übrig sind, werden die verbleibenden Elemente abgerufen.

## <a name="syntax"></a>Syntax


```C++
HRESULT Next(
  [in]  ULONG               celt,
  [out] IBackgroundCopyFile **rgelt,
  [out] ULONG               *pceltFetched
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*celt* \[ In\]
</dt> <dd>

Anzahl der angeforderten Elemente.

</dd> <dt>

*rgelt* \[ out\]
</dt> <dd>

Array von [**IBackgroundCopyFile-Objekten.**](ibackgroundcopyfile.md) Wenn Sie fertig sind, müssen Sie jedes Objekt in *rgelt* wieder frei geben.

</dd> <dt>

*pceltFetched* \[ out\]
</dt> <dd>

Anzahl der in *rgelt zurückgegebenen Elemente.* Sie können *pceltFetched auf* **NULL festlegen,** *wenn celt* eins ist. Initialisieren Sie andernfalls den Wert *von pceltFetched auf* 0, bevor Sie diese Methode aufrufen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt die folgenden **HRESULT-Werte** sowie andere zurück.



| Rückgabecode                                                                              | Beschreibung                                                        |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>S_OK S_OK</dt> </dl> | Die Anzahl der angeforderten Elemente wurde erfolgreich zurückgegeben.<br/> |
| <dl> <dt>**S_FALSE**</dt> </dl>  | Wird kleiner als die Anzahl der angeforderten Elemente zurückgegeben.<br/>    |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10 Desktop-Apps, Version 1709 \[\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, version 1709 desktop apps only (Nur \[ Desktop-Apps der Version 1709)\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IEnumBackgroundCopyFiles ist als CA51E165-C365-424C-8D41-24AAA4FF3C40 definiert.<br/>         |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IEnumBackgroundCopyFiles**](ienumbackgroundcopyfiles-.md)
</dt> </dl>

 

 





