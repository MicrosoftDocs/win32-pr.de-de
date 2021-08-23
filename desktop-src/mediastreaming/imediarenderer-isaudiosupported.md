---
title: IMediaRenderer IsAudioSupported-Methode
description: Ruft einen Wert ab, der angibt, ob die DMR Audioinhalte wiedergibt.
ms.assetid: D5F0C4ED-5778-4388-A7BD-E3923145D663
keywords:
- 'IsAudioSupported-Methode: Media Streaming-API'
- 'IsAudioSupported-Methode: Media Streaming-API, IMediaRenderer-Schnittstelle'
- IMediaRenderer-Schnittstelle Media Streaming-API, IsAudioSupported-Methode
topic_type:
- apiref
api_name:
- IMediaRenderer.IsAudioSupported
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5abe42e65e451464a5f7f3a4d59679db62c3634e95e89e5e275919dd0ece869e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777010"
---
# <a name="imediarendererisaudiosupported-method"></a>IMediaRenderer::IsAudioSupported-Methode

Ruft einen Wert ab, der angibt, ob die DMR Audioinhalte wiedergibt.

## <a name="syntax"></a>Syntax


```C++
HRESULT IsAudioSupported(
  [out] boolean *value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*value* \[ out\]
</dt> <dd>

Ein boolescher Wert, der **True** ist, wenn die DMR Audioinhalte wiederveröffentlichen kann, und **False,** wenn dies nicht der Fall ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMediaRenderer**](imediarenderer.md)
</dt> </dl>

 

 





