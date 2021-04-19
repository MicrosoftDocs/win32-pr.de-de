---
title: Imediarenderer-Methode "pauabasync"
description: Weist den DMR asynchron an, die Wiedergabe des aktuellen Inhalts anzuhalten. | Imediarenderer-Methode "pauabasync"
ms.assetid: 2EADD9BE-2306-4CDA-AD5C-8342C06EAF1B
keywords:
- Methode für die Medien Streaming-API
- Pautsasync-Methode Medien Streaming-API, imediarenderer-Schnittstelle
- Imediarenderer-Schnittstelle Medien Streaming-API, pautsasync-Methode
topic_type:
- apiref
api_name:
- IMediaRenderer.PauseAsync
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8713fa4b2fe46a694024c2873cd50a0ec89ce898
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106353695"
---
# <a name="imediarendererpauseasync-method"></a>Imediarenderer::P autsasync-Methode

Weist den DMR asynchron an, die Wiedergabe des aktuellen Inhalts anzuhalten.

## <a name="syntax"></a>Syntax


```C++
HRESULT PauseAsync(
  [out] PlaybackOperation **value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Wert* \[ vorgenommen\]
</dt> <dd>

Empfängt einen Verweis auf ein [**playbackoperation**](playbackoperation.md) -Objekt, das verwendet wird, um Ergebnisse aus dem asynchronen Vorgang zu erhalten.

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

 

 





