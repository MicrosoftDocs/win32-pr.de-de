---
title: Imediarenderer isaudiosupported-Methode
description: Ruft einen Wert ab, der angibt, ob der DMR Audioinhalt abspielen kann.
ms.assetid: D5F0C4ED-5778-4388-A7BD-E3923145D663
keywords:
- Isaudiosupported-Methode Medien Streaming-API
- Isaudiosupported-Methode Medien Streaming-API, imediarenderer-Schnittstelle
- Imediarenderer-Schnittstelle Medien Streaming-API, isaudiosupported-Methode
topic_type:
- apiref
api_name:
- IMediaRenderer.IsAudioSupported
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4f7670d0a2818cf5518bee0b2586531caeea20fd
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "106340659"
---
# <a name="imediarendererisaudiosupported-method"></a>Imediarenderer:: isaudiosupported-Methode

Ruft einen Wert ab, der angibt, ob der DMR Audioinhalt abspielen kann.

## <a name="syntax"></a>Syntax


```C++
HRESULT IsAudioSupported(
  [out] boolean *value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Wert* \[ vorgenommen\]
</dt> <dd>

Ein boolescher Wert, der **true** ist, wenn der DMR Audioinhalt abspielen kann, andernfalls **false** .

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

 

 





