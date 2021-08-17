---
title: IMediaRendererActionInformation PlaySpeeds-Methode
description: Ruft die vollständige Liste der PlaySpeed-Werte ab, die von der DMR akzeptiert werden.
ms.assetid: 0AB63E39-6A26-4199-9978-A10866A7C805
keywords:
- 'PlaySpeeds-Methode: Media Streaming-API'
- 'PlaySpeeds-Methode: Media Streaming-API, IMediaRendererActionInformation-Schnittstelle'
- IMediaRendererActionInformation-Schnittstelle Media Streaming-API, PlaySpeeds-Methode
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.PlaySpeeds
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 573fe9da4e71f9c16a9850da352e866ddbb0f77abc8c30861f2aa29647065fff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972199"
---
# <a name="imediarendereractioninformationplayspeeds-method"></a>IMediaRendererActionInformation::P laySpeeds-Methode

Ruft die vollständige Liste der [**PlaySpeed-Werte**](/previous-versions/windows/desktop/api/windows.media.streaming/ns-windows-media-streaming-playspeed) ab, die von der DMR akzeptiert werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT PlaySpeeds(
  [out] IVector< PlaySpeed > **value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*value* \[ out\]
</dt> <dd>

Empfängt einen Vektor von [**PlaySpeed-Strukturen,**](/previous-versions/windows/desktop/api/windows.media.streaming/ns-windows-media-streaming-playspeed) die die vollständige Liste der **PlaySpeed-Werte** angeben, die von der DMR akzeptiert werden.

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

 

