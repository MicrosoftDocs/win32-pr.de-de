---
title: MediaRenderer. pautsasync-Methode
description: Weist den DMR asynchron an, die Wiedergabe des aktuellen Inhalts anzuhalten. | MediaRenderer. pautsasync-Methode
ms.assetid: 1bd36349-0551-44e8-9550-3fd80900de9a
keywords:
- Methode für die Medien Streaming-API
- Pautsasync-Methode Medien Streaming-API, MediaRenderer-Schnittstelle
- MediaRenderer Interface Media Streaming API, pautsasync-Methode
topic_type:
- apiref
api_name:
- MediaRenderer.PauseAsync
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2bbbc55931c7cc7fc5e2e5ec39ba63fe7a064478
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106361831"
---
# <a name="mediarendererpauseasync-method"></a>MediaRenderer. pautsasync-Methode

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

[**MediaRenderer**](mediarenderer.md)
</dt> </dl>

 

 





