---
title: Imediarenderer stopasync-Methode
description: Weist den DMR asynchron an, die Wiedergabe des aktuellen Inhalts anzuhalten. | Imediarenderer stopasync-Methode
ms.assetid: B6B0F3F2-E95E-4A58-9CBD-CF4CB24FDAD0
keywords:
- Stopasync-Methode Medien Streaming-API
- Stopasync-Methode Medien Streaming-API, imediarenderer-Schnittstelle
- Imediarenderer-Schnittstelle Medien Streaming-API, stopasync-Methode
topic_type:
- apiref
api_name:
- IMediaRenderer.StopAsync
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a5f73d534fdd786038a242614a981f4915d92c13
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103870011"
---
# <a name="imediarendererstopasync-method"></a>Imediarenderer:: stopasync-Methode

Weist den DMR asynchron an, die Wiedergabe des aktuellen Inhalts anzuhalten.

## <a name="syntax"></a>Syntax


```C++
HRESULT StopAsync(
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

 

 





