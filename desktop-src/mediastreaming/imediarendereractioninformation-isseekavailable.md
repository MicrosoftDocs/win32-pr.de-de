---
title: IMediaRendererActionInformation IsSeekAvailable-Methode
description: Ruft einen Wert ab, der angibt, ob die DMR derzeit die SeekAsync-Methode akzeptiert.
ms.assetid: F0817184-70F2-43AC-A2BE-A15F4B195085
keywords:
- 'IsSeekAvailable-Methode: Medienstreaming-API'
- IsSeekAvailable-Methode Media Streaming API , IMediaRendererActionInformation-Schnittstelle
- IMediaRendererActionInformation-Schnittstelle Medienstreaming-API , IsSeekAvailable-Methode
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsSeekAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 32b5c7eef78dad4ebfeeebb40c323d7b13e540033eb54852f7da41942f5ec83e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118735513"
---
# <a name="imediarendereractioninformationisseekavailable-method"></a>IMediaRendererActionInformation::IsSeekAvailable-Methode

Ruft einen Wert ab, der angibt, ob die DMR derzeit die [**SeekAsync-Methode**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-seekasync) akzeptiert.

## <a name="syntax"></a>Syntax


```C++
HRESULT IsSeekAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wert* \[ out\]
</dt> <dd>

Ein boolescher Wert, der **True** ist, wenn die DMR derzeit die [**SeekAsync-Methode**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-seekasync) akzeptiert, und **False,** wenn dies nicht der Fall ist.

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

 

