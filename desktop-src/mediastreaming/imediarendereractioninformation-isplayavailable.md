---
title: Imediarendereraktioninformation isplayavailable-Methode
description: Ruft einen Wert ab, der angibt, ob der DMR derzeit akzeptiert, dass die playasync-Methode und die playatspeedasync-Methode akzeptiert werden.
ms.assetid: 969C55FA-872D-4063-B85C-573C8DA5593C
keywords:
- Isplayavailable-Methode Medien Streaming-API
- Isplayavailable-Methode Medien Streaming-API, imediarendereraktioninformation-Schnittstelle
- Imediarendereraktioninformation-Schnittstelle Medien Streaming-API, isplayavailable-Methode
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsPlayAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 87fa3a2005772a4d948bafe32d2a0e10cc5a6914
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390258"
---
# <a name="imediarendereractioninformationisplayavailable-method"></a>Imediarendereraktioninformation:: isplayavailable-Methode

Ruft einen Wert ab, der angibt, ob der DMR derzeit akzeptiert, dass die [**playasync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-playasync) -Methode und die [**playatspeedasync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-playatspeedasync) -Methode akzeptiert werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT IsPlayAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Wert* \[ vorgenommen\]
</dt> <dd>

Ein boolescher Wert, der **true** ist, wenn der DMR derzeit akzeptiert, dass die [**playasync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-playasync) -Methode und die [**playatspeedasync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-playatspeedasync) -Methode akzeptiert, andernfalls **false** .

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Imediarendereraktioninformation**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)
</dt> </dl>

 

