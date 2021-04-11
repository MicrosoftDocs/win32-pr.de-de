---
title: Imediarendereraktioninformation-playbeschleunigt-Methode
description: Ruft die gesamte Liste der playspeed-Werte ab, die von der DMR akzeptiert werden.
ms.assetid: 0AB63E39-6A26-4199-9978-A10866A7C805
keywords:
- Playbeschleunigt-Methode Medien Streaming-API
- Playbeschleunigt-Methode Medien Streaming-API, imediarendereraktioninformation-Schnittstelle
- Imediarendereraktioninformation-Schnittstelle Medien Streaming-API, playbeschleunigt-Methode
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.PlaySpeeds
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 31089dd7616c035ebde4079c51988b94d1c27562
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314985"
---
# <a name="imediarendereractioninformationplayspeeds-method"></a>Imediarendereraktioninformation::P laybeschleunigt-Methode

Ruft die gesamte Liste der [**playspeed**](/previous-versions/windows/desktop/api/windows.media.streaming/ns-windows-media-streaming-playspeed) -Werte ab, die von der DMR akzeptiert werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT PlaySpeeds(
  [out] IVector< PlaySpeed > **value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Wert* \[ vorgenommen\]
</dt> <dd>

Empfängt einen Vektor von [**playspeed**](/previous-versions/windows/desktop/api/windows.media.streaming/ns-windows-media-streaming-playspeed) -Strukturen, der die gesamte Liste der von DMR akzeptierten **playspeed** -Werte angibt.

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

 

