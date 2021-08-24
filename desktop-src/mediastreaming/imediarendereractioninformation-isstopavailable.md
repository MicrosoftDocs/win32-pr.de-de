---
title: IMediaRendererActionInformation IsStopAvailable-Methode
description: Ruft einen Wert ab, der angibt, ob die DMR derzeit die StopAsync-Methode akzeptiert.
ms.assetid: 6EE8F56D-2A5A-49B0-A9B2-0A7EE57D03FD
keywords:
- 'IsStopAvailable-Methode: Medienstreaming-API'
- IsStopAvailable-Methode Media Streaming API , IMediaRendererActionInformation-Schnittstelle
- IMediaRendererActionInformation-Schnittstelle Medienstreaming-API , IsStopAvailable-Methode
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsStopAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c177c46c62309525d9362f985075cec293105a80678b3b857eafa0524179d17e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119712890"
---
# <a name="imediarendereractioninformationisstopavailable-method"></a>IMediaRendererActionInformation::IsStopAvailable-Methode

Ruft einen Wert ab, der angibt, ob die DMR derzeit die [**StopAsync-Methode**](imediarenderer-stopasync.md) akzeptiert.

## <a name="syntax"></a>Syntax


```C++
HRESULT IsStopAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wert* \[ out\]
</dt> <dd>

Ein boolescher Wert, der **True** ist, wenn die DMR derzeit die [**StopAsync-Methode**](imediarenderer-stopasync.md) akzeptiert, und **False,** wenn dies nicht der Fall ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMediaRendererActionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)
</dt> </dl>

 

