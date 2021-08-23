---
title: IWMDRMNonSilentLicenseAquisition GetChallenge-Methode (Wmdrmsdk.h)
description: Die GetChallenge-Methode ruft die Lizenzausforderung ab, die an den Lizenzserver gesendet werden soll.
ms.assetid: f2ff8484-8fe2-4c74-82c1-9bc14f8197e0
keywords:
- 'GetChallenge-Methode : Windows Media Format'
- GetCkatge-Methode windows Media Format, IWMDRMNonSilentLicenseAquisition-Schnittstelle
- IWMDRMNonSilentLicenseAquisition-Schnittstelle Windows Media Format , GetC gemäß der Methode
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
ms.openlocfilehash: cf495652033bdb5201f2b4e5bd9dc1d6a222cc3ebdf4ec6438fe391ed06fac85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027518"
---
# <a name="iwmdrmnonsilentlicenseaquisitiongetchallenge-method"></a>IWMDRMNonSilentLicenseAquisition::GetCwiedergabege-Methode

Die **GetChallenge-Methode** ruft die Lizenzausforderung ab, die an den Lizenzserver gesendet werden soll.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetChallenge(
  [out] BSTR *pbstrChallenge
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pbstrC wiege* \[ out\]
</dt> <dd>

Adresse einer Variablen, die die Lizenzausforderung empfängt.

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

 

 





