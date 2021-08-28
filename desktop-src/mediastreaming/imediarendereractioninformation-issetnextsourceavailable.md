---
title: IMediaRendererActionInformation IsSetNextSourceAvailable-Methode
description: Ruft einen Wert ab, der angibt, ob die DMR derzeit die SetNextSourceFromUriAsync-Methode, die SetNextSourceFromStreamAsync-Methode oder die SetNextSourceFromMediaSourceAsync-Methode akzeptiert.
ms.assetid: 7588E992-4070-4E0F-8C4B-7DFC097A5076
keywords:
- IsSetNextSourceAvailable-Methode Medienstreaming-API
- IsSetNextSourceAvailable-Methode Media Streaming API , IMediaRendererActionInformation-Schnittstelle
- IMediaRendererActionInformation-Schnittstelle Medienstreaming-API , IsSetNextSourceAvailable-Methode
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsSetNextSourceAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ee18eadbc535dd2cd4b48ec6f77adb1d3dec2f5a0c1f5065cee009e27635eda9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092300"
---
# <a name="imediarendereractioninformationissetnextsourceavailable-method"></a>IMediaRendererActionInformation::IsSetNextSourceAvailable-Methode

Ruft einen Wert ab, der angibt, ob die DMR derzeit die [**SetNextSourceFromUriAsync-Methode,**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefromuriasync) die [**SetNextSourceFromStreamAsync-Methode**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefromstreamasync) oder die [**SetNextSourceFromMediaSourceAsync-Methode**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefrommediasourceasync) akzeptiert.

## <a name="syntax"></a>Syntax


```C++
HRESULT IsSetNextSourceAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wert* \[ out\]
</dt> <dd>

Ein boolescher Wert, der **True** ist, wenn die DMR derzeit die [**SetNextSourceFromUriAsync-Methode,**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefromuriasync) die [**SetNextSourceFromStreamAsync-Methode**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefromstreamasync) oder die [**SetNextSourceFromMediaSourceAsync-Methode**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefrommediasourceasync) akzeptiert, **andernfalls FALSE.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMediaRendererActionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)
</dt> </dl>

 

