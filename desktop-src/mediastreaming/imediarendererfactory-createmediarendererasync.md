---
title: IMediaRendererFactory CreateMediaRendererAsync-Methode
description: Erstellt asynchron eine neue Instanz eines Objekts, das die IMediaRenderer-Schnittstelle mit dem angegebenen eindeutigen Gerätenamen (Unique Device Name, UDN) implementiert.
ms.assetid: FD1242F8-4C2E-4027-B1DE-5FD69557684C
keywords:
- 'CreateMediaRendererAsync-Methode: Medienstreaming-API'
- CreateMediaRendererAsync-Methode Media Streaming-API, IMediaRendererFactory-Schnittstelle
- IMediaRendererFactory-Schnittstelle Medienstreaming-API , CreateMediaRendererAsync-Methode
topic_type:
- apiref
api_name:
- IMediaRendererFactory.CreateMediaRendererAsync
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3e459324d96f031ab3433f0d8bfe8ba5de562d76c95f51affd7b72d130655fab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118735487"
---
# <a name="imediarendererfactorycreatemediarendererasync-method"></a>IMediaRendererFactory::CreateMediaRendererAsync-Methode

Erstellt asynchron eine neue Instanz eines Objekts, das die [**IMediaRenderer-Schnittstelle**](imediarenderer.md) mit dem angegebenen eindeutigen Gerätenamen (Unique Device Name, UDN) implementiert.

## <a name="syntax"></a>Syntax


```C++
HRESULT CreateMediaRendererAsync(
  [in]          HSTRING                      deviceIdentifier,
  [out, retval] CreateMediaRendererOperation **value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*deviceIdentifier* \[ In\]
</dt> <dd>

Ein HSTRING mit einem UDN, der das DLNA DMR-Gerät identifiziert, für das eine Instanz von [**IMediaRenderer**](imediarenderer.md) erstellt wird.

</dd> <dt>

*wert* \[ out, retval\]
</dt> <dd>

Empfängt einen Verweis auf ein [**CreateMediaRendererOperation-Objekt,**](createmediarendereroperation.md) das zum Abrufen der Ergebnisse des asynchronen Vorgangs verwendet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IMediaRendererFactory**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendererfactory)
</dt> </dl>

 

