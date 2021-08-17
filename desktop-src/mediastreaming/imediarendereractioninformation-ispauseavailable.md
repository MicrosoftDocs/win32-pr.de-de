---
title: IMediaRendererActionInformation IsPauseAvailable-Methode
description: Ruft einen Wert ab, der angibt, ob die DMR derzeit die PauseAsync-Methode akzeptiert.
ms.assetid: 095A664F-D974-410D-8741-87A171EDD071
keywords:
- 'IsPauseAvailable-Methode: Medienstreaming-API'
- 'IsPauseAvailable-Methode: Media Streaming-API, IMediaRendererActionInformation-Schnittstelle'
- IMediaRendererActionInformation-Schnittstelle Media Streaming-API, IsPauseAvailable-Methode
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsPauseAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fad69863306a8a937771f16c2ab9a83a2622c571d2cd5ee5658a279bf7564132
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117870847"
---
# <a name="imediarendereractioninformationispauseavailable-method"></a>IMediaRendererActionInformation::IsPauseAvailable-Methode

Ruft einen Wert ab, der angibt, ob die DMR derzeit die [**PauseAsync-Methode**](imediarenderer-pauseasync.md) akzeptiert.

## <a name="syntax"></a>Syntax


```C++
HRESULT IsPauseAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*value* \[ out\]
</dt> <dd>

Ein boolescher Wert, der **True** ist, wenn die DMR derzeit die [**PauseAsync-Methode**](imediarenderer-pauseasync.md) akzeptiert, ander denn, false. 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IMediaRendererActionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)
</dt> </dl>

 

