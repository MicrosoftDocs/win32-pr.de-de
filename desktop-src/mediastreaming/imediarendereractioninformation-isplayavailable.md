---
title: IMediaRendererActionInformation IsPlayAvailable-Methode
description: Ruft einen Wert ab, der angibt, ob die DMR derzeit die PlayAsync- und PlayAtSpeedAsync-Methoden akzeptiert.
ms.assetid: 969C55FA-872D-4063-B85C-573C8DA5593C
keywords:
- 'IsPlayAvailable-Methode: Medienstreaming-API'
- 'IsPlayAvailable-Methode: Media Streaming-API, IMediaRendererActionInformation-Schnittstelle'
- IMediaRendererActionInformation-Schnittstelle Media Streaming-API, IsPlayAvailable-Methode
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsPlayAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 912e5478ef1d9bd7114d198a9671d38ba7b721c9dbd82d2a8080b5a7876e76cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118235845"
---
# <a name="imediarendereractioninformationisplayavailable-method"></a>IMediaRendererActionInformation::IsPlayAvailable-Methode

Ruft einen Wert ab, der angibt, ob die DMR derzeit die [**PlayAsync-**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-playasync) und [**PlayAtSpeedAsync-Methoden**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-playatspeedasync) akzeptiert.

## <a name="syntax"></a>Syntax


```C++
HRESULT IsPlayAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*value* \[ out\]
</dt> <dd>

Ein boolescher Wert, der **True** ist, wenn die DMR derzeit die [**PlayAsync-**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-playasync) und  [**PlayAtSpeedAsync-Methode**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-playatspeedasync) akzeptiert, ander denn, false.

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

 

