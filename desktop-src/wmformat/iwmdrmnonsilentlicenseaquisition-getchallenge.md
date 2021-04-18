---
title: Iwmdrmnonsilentlicenseaquisition getchallenge-Methode (wmdrmsdk. h)
description: Die getchallenge-Methode ruft die Lizenz Herausforderung ab, die auf dem Lizenzserver gepostet werden soll.
ms.assetid: f2ff8484-8fe2-4c74-82c1-9bc14f8197e0
keywords:
- Getchallenge-Methode Windows Media-Format
- Getchallenge-Methode Windows Media-Format, iwmdrmnonsilentlicenseaquisition-Schnittstelle
- Iwmdrmnonsilentlicenseaquisition-Schnittstelle Windows Media-Format, getchallenge-Methode
topic_type:
- apiref
api_name:
- IWMDRMNonSilentLicenseAquisition.GetChallenge
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa0dc63c63e5d7a62c06cbe791d9a5e5e8d09c5d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357654"
---
# <a name="iwmdrmnonsilentlicenseaquisitiongetchallenge-method"></a>Iwmdrmnonsilentlicenseaquisition:: getchallenge-Methode

Die **getchallenge** -Methode ruft die Lizenz Herausforderung ab, die auf dem Lizenzserver gepostet werden soll.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetChallenge(
  [out] BSTR *pbstrChallenge
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pbstranchallenge* \[ vorgenommen\]
</dt> <dd>

Adresse einer Variablen, die die Lizenz Herausforderung empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Keine.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmdrmnonsilentlicenseaquisition-Schnittstelle**](iwmdrmnonsilentlicenseaquisition.md)
</dt> </dl>

 

 





