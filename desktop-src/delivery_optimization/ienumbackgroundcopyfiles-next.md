---
title: Ienumbackgroundcopyfiles Next-Methode (deliveryoptimization. h)
description: Ruft eine angegebene Anzahl von Elementen in der Enumerationsfolge ab. Wenn weniger als die angeforderte Anzahl von Elementen in der Sequenz vorhanden sind, werden die restlichen Elemente abgerufen.
ms.assetid: 31E603EC-2684-487D-AB37-4C6A6F661298
keywords:
- Nächste Methode
- Next-Methode, ienumbackgroundcopyfiles-Schnittstelle
- Ienumbackgroundcopyfiles-Schnittstelle, Next-Methode
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
ms.openlocfilehash: 504b9083f4bdb1651496b4ab2d3b937740596243
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956945"
---
# <a name="ienumbackgroundcopyfilesnext-method"></a>Ienumbackgroundcopyfiles:: Next-Methode

Ruft eine angegebene Anzahl von Elementen in der Enumerationsfolge ab. Wenn weniger als die angeforderte Anzahl von Elementen in der Sequenz vorhanden sind, werden die restlichen Elemente abgerufen.

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

*celt* \[ in\]
</dt> <dd>

Anzahl der angeforderten Elemente.

</dd> <dt>

*rgelt* \[ vorgenommen\]
</dt> <dd>

Array von [**ibackgroundcopyfile**](ibackgroundcopyfile.md) -Objekten. Sie müssen jedes Objekt in *rgelt* freigeben, wenn Sie dies erledigt haben.

</dd> <dt>

*pceltfetch* \[ vorgenommen\]
</dt> <dd>

Anzahl der Elemente, die in *rgelt* zurückgegeben werden. Sie können *pceltfetch* auf **null** festlegen, wenn es sich um ein *celt* handelt. Initialisieren Sie andernfalls den Wert von *pceltfetch* auf 0, bevor Sie diese Methode aufrufen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt sowohl die folgenden **HRESULT** -Werte als auch andere zurück.



| Rückgabecode                                                                              | Beschreibung                                                        |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl> | Die Anzahl der angeforderten Elemente wurde erfolgreich zurückgegeben.<br/> |
| <dl> <dt>**S_FALSE**</dt> </dl>  | Wird kleiner als die Anzahl der angeforderten Elemente zurückgegeben.<br/>    |



 

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

 

 





