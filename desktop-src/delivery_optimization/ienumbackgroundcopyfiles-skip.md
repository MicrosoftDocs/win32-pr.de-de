---
title: Ienumbackgroundcopyfiles Skip-Methode (deliveryoptimization. h)
description: Überspringt die nächste angegebene Anzahl von Elementen in der enumerationssequenz. Wenn in der Sequenz weniger Elemente als die angeforderte Anzahl der zu über springenden Elemente vorhanden sind, wird das letzte Element in der Sequenz übersprungen.
ms.assetid: B01D4292-6BA5-4171-928B-AB2C555E2C2A
keywords:
- Skip-Methode
- Skip-Methode, ienumbackgroundcopyfiles-Schnittstelle
- Ienumbackgroundcopyfiles-Schnittstelle, Skip-Methode
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
ms.openlocfilehash: 5d88a7d971ab93b90c844fc8d9d92d7f154c0ebf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040252"
---
# <a name="ienumbackgroundcopyfilesskip-method"></a>Ienumbackgroundcopyfiles:: Skip-Methode

Überspringt die nächste angegebene Anzahl von Elementen in der enumerationssequenz. Wenn in der Sequenz weniger Elemente als die angeforderte Anzahl der zu über springenden Elemente vorhanden sind, wird das letzte Element in der Sequenz übersprungen.

## <a name="syntax"></a>Syntax


```C++
HRESULT Skip(
  [in] ULONG celt
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*celt* \[ in\]
</dt> <dd>

Anzahl der zu überspringenden Elemente.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt sowohl die folgenden **HRESULT** -Werte als auch andere zurück.



| Rückgabecode                                                                              | Beschreibung                                                       |
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl> | Die Anzahl der angeforderten Elemente wurde erfolgreich übersprungen.<br/> |
| <dl> <dt>**S_FALSE**</dt> </dl>  | Wird kleiner als die Anzahl der angeforderten Elemente übersprungen.<br/>    |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1709, \[ nur Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, Version 1709, \[ nur Desktop-Apps\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Deliveryoptimization. idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IEnumBackgroundCopyFiles ist als CA51E165-C365-424C-8D41-24AAA4FF3C40 definiert.<br/>         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ienumbackgroundcopyfiles**](ienumbackgroundcopyfiles-.md)
</dt> </dl>

 

 





