---
title: MediaRenderer. stopasync-Methode
description: Weist den DMR asynchron an, die Wiedergabe des aktuellen Inhalts anzuhalten. | MediaRenderer. stopasync-Methode
ms.assetid: 04cf6d5a-8aa5-4821-8117-f250bfaf7ebd
keywords:
- Stopasync-Methode Medien Streaming-API
- Stopasync-Methode Medien Streaming-API, MediaRenderer-Schnittstelle
- MediaRenderer Interface Medien Streaming-API, stopasync-Methode
topic_type:
- apiref
api_name:
- MediaRenderer.StopAsync
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 205c69a83572539974c1b8ad2cf45159c45335cb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104132261"
---
# <a name="mediarendererstopasync-method"></a>MediaRenderer. stopasync-Methode

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

[**MediaRenderer**](mediarenderer.md)
</dt> </dl>

 

 





