---
title: Itransportparameters-Methode "aktioninformation"
description: Ruft eine imediarendereraktioninformation-Schnittstelle ab, die Informationen darüber bereitstellt, welche Methoden aktuell für die DMR aufgerufen werden können.
ms.assetid: 3EEB94E1-B6BC-4111-AEF1-D5724BD0A2E7
keywords:
- Aktioninformation-Methode Medien Streaming-API
- Aktions Information-Methode Medien Streaming-API, itransportparameters-Schnittstelle
- Itransportparameters-Schnittstelle Medien Streaming-API, aktioninformation-Methode
topic_type:
- apiref
api_name:
- ITransportParameters.ActionInformation
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b194da50e71402b6af69eb4cc9d67902e8ae89a0
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038890"
---
# <a name="itransportparametersactioninformation-method"></a>Itransportparameters:: aktioninformation-Methode

Ruft eine [**imediarendereraktioninformation**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation) -Schnittstelle ab, die Informationen darüber bereitstellt, welche Methoden aktuell für die DMR aufgerufen werden können.

## <a name="syntax"></a>Syntax


```C++
HRESULT ActionInformation(
  [out, retval] IMediaRendererActionInformation **value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Wert* \[ Out, retval\]
</dt> <dd>

Empfängt einen Verweis auf eine [**imediarendereraktioninformation**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation) -Schnittstelle.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Itransportparameters**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-itransportparameters)
</dt> </dl>

 

