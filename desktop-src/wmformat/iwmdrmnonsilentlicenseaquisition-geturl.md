---
title: Iwmdrmnonsilentlicenseaquisition getURL-Methode (wmdrmsdk. h)
description: Die getURL-Methode ruft die URL ab, an die die Lizenz Herausforderung gesendet werden soll.
ms.assetid: f65f1984-74bc-4cd0-957e-930aa6a6f6a5
keywords:
- GetURL-Methode Windows Media-Format
- GetURL-Methode Windows Media-Format, iwmdrmnonsilentlicenseaquisition-Schnittstelle
- Iwmdrmnonsilentlicenseaquisition-Schnittstelle Windows Media-Format, getURL-Methode
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
ms.openlocfilehash: 79212d19d7dbf4a66e2b72dcbdeba9262a9aeddd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364604"
---
# <a name="iwmdrmnonsilentlicenseaquisitiongeturl-method"></a>Iwmdrmnonsilentlicenseaquisition:: getURL-Methode

Die **getURL** -Methode ruft die URL ab, an die die Lizenz Herausforderung gesendet werden soll.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetURL(
  [out] BSTR *pbstrURL
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pbstrinurl* \[ vorgenommen\]
</dt> <dd>

Adresse einer Variablen, die die URL empfängt.

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

 

 





