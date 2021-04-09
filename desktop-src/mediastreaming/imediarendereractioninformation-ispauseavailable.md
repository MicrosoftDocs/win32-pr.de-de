---
title: Imediarendereraktioninformation ispauseravailable-Methode
description: Ruft einen Wert ab, der angibt, ob der DMR derzeit die Methode "paugasync" annimmt.
ms.assetid: 095A664F-D974-410D-8741-87A171EDD071
keywords:
- Ispaugavailable-Methode Medien Streaming-API
- Ispauseravailable-Methode Medien Streaming-API, imediarendereraktioninformation-Schnittstelle
- Imediarendereraktioninformation-Schnittstelle Medien Streaming-API, ispauseravailable-Methode
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsPauseAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9eb0b750f5a04528aef830d87376c276bdaf6674
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103858227"
---
# <a name="imediarendereractioninformationispauseavailable-method"></a>Imediarendereraktioninformation:: ispauseravailable-Methode

Ruft einen Wert ab, der angibt, ob der DMR derzeit die Methode " [**paugasync**](imediarenderer-pauseasync.md) " annimmt.

## <a name="syntax"></a>Syntax


```C++
HRESULT IsPauseAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Wert* \[ vorgenommen\]
</dt> <dd>

Ein boolescher Wert, der **true** ist, wenn der DMR derzeit die Methode " [**pausiasync**](imediarenderer-pauseasync.md) " annimmt, andernfalls " **false** ".

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Imediarendereraktioninformation**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)
</dt> </dl>

 

