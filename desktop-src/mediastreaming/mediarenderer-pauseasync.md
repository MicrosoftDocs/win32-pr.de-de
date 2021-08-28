---
title: MediaRenderer.PauseAsync-Methode
description: Weist die DMR asynchron an, die Wiedergabe des aktuellen Inhalts anzuhalten. | MediaRenderer.PauseAsync-Methode
ms.assetid: 1bd36349-0551-44e8-9550-3fd80900de9a
keywords:
- Medienstreaming-API der PauseAsync-Methode
- 'PauseAsync-Methode: Medienstreaming-API, MediaRenderer-Schnittstelle'
- MediaRenderer-Schnittstelle Medienstreaming-API , PauseAsync-Methode
topic_type:
- apiref
api_name:
- MediaRenderer.PauseAsync
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5dcb4474f7a7843f2812cf64e0119912eca8ae320b29b9acb0131a65bbbffa19
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060250"
---
# <a name="mediarendererpauseasync-method"></a>MediaRenderer.PauseAsync-Methode

Weist die DMR asynchron an, die Wiedergabe des aktuellen Inhalts anzuhalten.

## <a name="syntax"></a>Syntax


```C++
HRESULT PauseAsync(
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

 

 





