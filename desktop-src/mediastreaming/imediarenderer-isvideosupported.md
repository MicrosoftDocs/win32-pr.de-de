---
title: Imediarenderer isvideosupported-Methode
description: Ruft einen Wert ab, der angibt, ob der DMR Videoinhalte abspielen kann.
ms.assetid: AE9A14D0-A7A2-4A71-9454-06A05C7D85F9
keywords:
- Isvideosupported-Methode Medien Streaming-API
- Isvideosupported-Methode Medien Streaming-API, imediarenderer-Schnittstelle
- Imediarenderer-Schnittstelle Medien Streaming-API, isvideosupported-Methode
topic_type:
- apiref
api_name:
- IMediaRenderer.IsVideoSupported
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9808841bf60a384d6a4566e75f53248b0f86338c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104313001"
---
# <a name="imediarendererisvideosupported-method"></a>Imediarenderer:: isvideosupported-Methode

Ruft einen Wert ab, der angibt, ob der DMR Videoinhalte abspielen kann.

## <a name="syntax"></a>Syntax


```C++
HRESULT IsVideoSupported(
  [out] boolean *value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Wert* \[ vorgenommen\]
</dt> <dd>

Ein boolescher Wert, der **true** ist, wenn der DMR Videoinhalte abspielen kann, andernfalls **false** .

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Imediarenderer**](imediarenderer.md)
</dt> </dl>

 

 





