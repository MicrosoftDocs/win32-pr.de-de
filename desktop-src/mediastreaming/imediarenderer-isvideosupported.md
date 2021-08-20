---
title: IMediaRenderer IsVideoSupported-Methode
description: Ruft einen Wert ab, der angibt, ob die DMR Videoinhalte wiedergeben kann.
ms.assetid: AE9A14D0-A7A2-4A71-9454-06A05C7D85F9
keywords:
- 'IsVideoSupported-Methode: Medienstreaming-API'
- 'IsVideoSupported-Methode: Medienstreaming-API, IMediaRenderer-Schnittstelle'
- IMediaRenderer-Schnittstelle Medienstreaming-API , IsVideoSupported-Methode
topic_type:
- apiref
api_name:
- IMediaRenderer.IsVideoSupported
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0c1f6fa149c6c5025d3fd2c785dc2f4a8451fabed3906b559674d8038662c21d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972309"
---
# <a name="imediarendererisvideosupported-method"></a>IMediaRenderer::IsVideoSupported-Methode

Ruft einen Wert ab, der angibt, ob die DMR Videoinhalte wiedergeben kann.

## <a name="syntax"></a>Syntax


```C++
HRESULT IsVideoSupported(
  [out] boolean *value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wert* \[ out\]
</dt> <dd>

Ein boolescher Wert, der **True** ist, wenn die DMR Videoinhalte wiedergeben kann, und **FALSE,** wenn dies nicht der Fall ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMediaRenderer**](imediarenderer.md)
</dt> </dl>

 

 





