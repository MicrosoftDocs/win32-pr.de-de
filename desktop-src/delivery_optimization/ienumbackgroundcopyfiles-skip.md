---
title: IEnumBackgroundCopyFiles Skip-Methode (Deliveryoptimization.h)
description: Überspringt die nächste angegebene Anzahl von Elementen in der Enumerationssequenz. Wenn in der Sequenz weniger Elemente vorhanden sind als die angeforderte Anzahl von zu überspringenden Elementen, überspringt sie das letzte Element in der Sequenz.
ms.assetid: B01D4292-6BA5-4171-928B-AB2C555E2C2A
keywords:
- Skip-Methode
- Skip-Methode, IEnumBackgroundCopyFiles-Schnittstelle
- IEnumBackgroundCopyFiles-Schnittstelle, Skip-Methode
topic_type:
- apiref
api_name:
- IEnumBackgroundCopyFiles.Skip
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 174b8ac3e0286a4d2a19e211773969d408c7f7762e8b2dd4fe743f0b4b2aabeb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119567360"
---
# <a name="ienumbackgroundcopyfilesskip-method"></a>IEnumBackgroundCopyFiles::Skip-Methode

Überspringt die nächste angegebene Anzahl von Elementen in der Enumerationssequenz. Wenn in der Sequenz weniger Elemente vorhanden sind als die angeforderte Anzahl von zu überspringenden Elementen, überspringt sie das letzte Element in der Sequenz.

## <a name="syntax"></a>Syntax


```C++
HRESULT Skip(
  [in] ULONG celt
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*celt* \[ In\]
</dt> <dd>

Anzahl der zu überspringenden Elemente.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt die folgenden **HRESULT-Werte** sowie andere zurück.



| Rückgabecode                                                                              | Beschreibung                                                       |
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <dt>S_OK</dt> </dl> | Die Anzahl der angeforderten Elemente wurde erfolgreich übersprungen.<br/> |
| <dl> <dt>**S_FALSE**</dt> </dl>  | Kleiner als die Anzahl der angeforderten Elemente übersprungen.<br/>    |



 

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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IEnumBackgroundCopyFiles**](ienumbackgroundcopyfiles-.md)
</dt> </dl>

 

 





