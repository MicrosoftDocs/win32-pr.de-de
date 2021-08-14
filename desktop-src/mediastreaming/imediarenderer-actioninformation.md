---
title: IMediaRenderer ActionInformation-Methode
description: Ruft Informationen darüber ab, welche Methoden derzeit für die DMR aufgerufen werden können.
ms.assetid: 7681FF92-DD13-4BBC-B860-E2BDFDA74FB9
keywords:
- 'ActionInformation-Methode : Medienstreaming-API'
- ActionInformation-Methode Media Streaming API , IMediaRenderer-Schnittstelle
- IMediaRenderer-Schnittstelle Media Streaming API , ActionInformation-Methode
topic_type:
- apiref
api_name:
- IMediaRenderer.ActionInformation
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3caf251c080f218b99861d4a81920cd5c95c1f0e53bc6b006c84536f33f7f29c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118735523"
---
# <a name="imediarendereractioninformation-method"></a>IMediaRenderer::ActionInformation-Methode

Ruft Informationen darüber ab, welche Methoden derzeit für die DMR aufgerufen werden können.

## <a name="syntax"></a>Syntax


```C++
HRESULT ActionInformation(
  [out] IMediaRendererActionInformation **value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wert* \[ out\]
</dt> <dd>

Empfängt einen Verweis auf eine [**IMediaRendererActionInformation-Schnittstelle.**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IMediaRenderer**](imediarenderer.md)
</dt> </dl>

 

