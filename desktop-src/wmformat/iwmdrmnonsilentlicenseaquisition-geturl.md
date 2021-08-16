---
title: IWMDRMNonSilentLicenseAquisition GetURL-Methode (Wmdrmsdk.h)
description: Die GetURL-Methode ruft die URL ab, an die die Lizenzaufforderung gesendet werden soll.
ms.assetid: f65f1984-74bc-4cd0-957e-930aa6a6f6a5
keywords:
- GetURL-Methode windows Media Format
- GetURL-Methodenfenster Media Format , IWMDRMNonSilentLicenseAquisition-Schnittstelle
- IWMDRMNonSilentLicenseAquisition-Schnittstelle windows Media Format , GetURL-Methode
topic_type:
- apiref
api_name:
- IWMDRMNonSilentLicenseAquisition.GetURL
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7979d82363b21b58563a606c31a99d069a60a3bc5b2da162a7339513c2867bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119084707"
---
# <a name="iwmdrmnonsilentlicenseaquisitiongeturl-method"></a>IWMDRMNonSilentLicenseAquisition::GetURL-Methode

Die **GetURL-Methode** ruft die URL ab, an die die Lizenzaufforderung gesendet werden soll.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetURL(
  [out] BSTR *pbstrURL
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pbstrURL* \[ out\]
</dt> <dd>

Adresse einer Variablen, die die URL empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Keine.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wmdrmsdk.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>Wmdrmsdk.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IWMDRMNonSilentLicenseAquisition-Schnittstelle**](iwmdrmnonsilentlicenseaquisition.md)
</dt> </dl>

 

 





