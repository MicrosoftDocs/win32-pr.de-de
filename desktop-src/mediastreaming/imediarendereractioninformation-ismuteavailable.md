---
title: IMediaRendererActionInformation IsMuteAvailable-Methode
description: Ruft einen Wert ab, der angibt, ob die DMR die Audiodaten stummschalten kann.
ms.assetid: F744C2D7-5518-4A9F-A71E-60CF0B312177
keywords:
- 'IsMuteAvailable-Methode: Medienstreaming-API'
- 'IsMuteAvailable-Methode: Media Streaming-API, IMediaRendererActionInformation-Schnittstelle'
- IMediaRendererActionInformation-Schnittstelle Media Streaming-API, IsMuteAvailable-Methode
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsMuteAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 331e2831ff18656f23a3d7067b8ab472835bf4a25760f6e86a92302621048a48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117871067"
---
# <a name="imediarendereractioninformationismuteavailable-method"></a>IMediaRendererActionInformation::IsMuteAvailable-Methode

Ruft einen Wert ab, der angibt, ob die DMR die Audiodaten stummschalten kann.

## <a name="syntax"></a>Syntax


```C++
HRESULT IsMuteAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*value* \[ out\]
</dt> <dd>

Ein boolescher Wert, der **True ist,** wenn die DMR die Audiodaten stummschalten kann, und **False,** wenn dies nicht der Fall ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IMediaRendererActionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)
</dt> </dl>

 

