---
title: Imediarendereraktioninformation isstopavailable-Methode
description: Ruft einen Wert ab, der angibt, ob der DMR derzeit die stopasync-Methode annimmt.
ms.assetid: 6EE8F56D-2A5A-49B0-A9B2-0A7EE57D03FD
keywords:
- Isstopavailable-Methode Medien Streaming-API
- Isstopavailable-Methode Medien Streaming-API, imediarendereraktioninformation-Schnittstelle
- Imediarendereraktioninformation-Schnittstelle Medien Streaming-API, isstopavailable-Methode
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsStopAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5e0a031bafc9a755dfec2498f4e2a52cdd9ef5b1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101582"
---
# <a name="imediarendereractioninformationisstopavailable-method"></a>Imediarendereraktioninformation:: isstopavailable-Methode

Ruft einen Wert ab, der angibt, ob der DMR derzeit die [**stopasync**](imediarenderer-stopasync.md) -Methode annimmt.

## <a name="syntax"></a>Syntax


```C++
HRESULT IsStopAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Wert* \[ vorgenommen\]
</dt> <dd>

Ein boolescher Wert, der **true** ist, wenn der DMR derzeit die [**stopasync**](imediarenderer-stopasync.md) -Methode annimmt, andernfalls **false** .

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

 

