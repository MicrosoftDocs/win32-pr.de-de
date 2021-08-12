---
title: ITransportParameters ActionInformation-Methode
description: Ruft eine IMediaRendererActionInformation-Schnittstelle ab, die Informationen darüber bereitstellt, welche Methoden derzeit für die DMR aufgerufen werden können.
ms.assetid: 3EEB94E1-B6BC-4111-AEF1-D5724BD0A2E7
keywords:
- 'ActionInformation-Methode : Medienstreaming-API'
- ActionInformation-Methode Medienstreaming-API , ITransportParameters-Schnittstelle
- ITransportParameters-Schnittstelle Medienstreaming-API , ActionInformation-Methode
topic_type:
- apiref
api_name:
- ITransportParameters.ActionInformation
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 551612fcaffb9379823efea15f29ed9feba1ff3d0c5af6e7271b61ad9d6036f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118235855"
---
# <a name="itransportparametersactioninformation-method"></a>ITransportParameters::ActionInformation-Methode

Ruft eine [**IMediaRendererActionInformation-Schnittstelle**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation) ab, die Informationen darüber bereitstellt, welche Methoden derzeit für die DMR aufgerufen werden können.

## <a name="syntax"></a>Syntax


```C++
HRESULT ActionInformation(
  [out, retval] IMediaRendererActionInformation **value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wert* \[ out, retval\]
</dt> <dd>

Empfängt einen Verweis auf eine [**IMediaRendererActionInformation-Schnittstelle.**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ITransportParameters**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-itransportparameters)
</dt> </dl>

 

