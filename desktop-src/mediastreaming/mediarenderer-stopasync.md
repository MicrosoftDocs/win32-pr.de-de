---
title: MediaRenderer.StopAsync-Methode
description: Weist die DMR asynchron an, die Wiedergabe des aktuellen Inhalts zu beenden. | MediaRenderer.StopAsync-Methode
ms.assetid: 04cf6d5a-8aa5-4821-8117-f250bfaf7ebd
keywords:
- 'StopAsync-Methode: Medienstreaming-API'
- 'StopAsync-Methode: Media Streaming-API, MediaRenderer-Schnittstelle'
- MediaRenderer-Schnittstelle Medienstreaming-API , StopAsync-Methode
topic_type:
- apiref
api_name:
- MediaRenderer.StopAsync
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4c13e69952261643f2ac74df1e3978fb10e846488ee2c4794ee3ecac17251469
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972139"
---
# <a name="mediarendererstopasync-method"></a>MediaRenderer.StopAsync-Methode

Weist die DMR asynchron an, die Wiedergabe des aktuellen Inhalts zu beenden.

## <a name="syntax"></a>Syntax


```C++
HRESULT StopAsync(
  [out] PlaybackOperation **value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wert* \[ out\]
</dt> <dd>

Empfängt einen Verweis auf ein [**PlaybackOperation-Objekt,**](playbackoperation.md) das zum Abrufen der Ergebnisse des asynchronen Vorgangs verwendet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MediaRenderer**](mediarenderer.md)
</dt> </dl>

 

 





