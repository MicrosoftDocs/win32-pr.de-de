---
title: Imediarendererfactory-Methode "kreatemediarendererasync"
description: Erstellt asynchron eine neue Instanz eines Objekts, das die imediarenderer-Schnittstelle mit dem angegebenen eindeutigen Gerätenamen (User Name, udn) implementiert.
ms.assetid: FD1242F8-4C2E-4027-B1DE-5FD69557684C
keywords:
- Methode für die Media Streaming-API von "kreatemediarendererasync"
- Methode "Media Streaming API" der Methode "kreatemediarendererasync", imediarendererfactory-Schnittstelle
- Imediarendererfactory-Schnittstelle Medien Streaming-API, Methode "kreatemediarendererasync"
topic_type:
- apiref
api_name:
- IMediaRendererFactory.CreateMediaRendererAsync
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b152e5889ad83440a48e178be0b89a97d2a9f664
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725881"
---
# <a name="imediarendererfactorycreatemediarendererasync-method"></a>Imediarendererfactory:: kreatemediarendererasync-Methode

Erstellt asynchron eine neue Instanz eines Objekts, das die [**imediarenderer**](imediarenderer.md) -Schnittstelle mit dem angegebenen eindeutigen Gerätenamen (User Name, udn) implementiert.

## <a name="syntax"></a>Syntax


```C++
HRESULT CreateMediaRendererAsync(
  [in]          HSTRING                      deviceIdentifier,
  [out, retval] CreateMediaRendererOperation **value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

Geräte Bezeichner  \[ in\]
</dt> <dd>

Ein hstring-Wert, der einen udn enthält, der das DLNA-DMR-Gerät identifiziert, für das eine Instanz von [**imediarenderer**](imediarenderer.md) erstellt wird.

</dd> <dt>

*Wert* \[ Out, retval\]
</dt> <dd>

Empfängt einen Verweis auf ein Objekt vom Typ " [**kreatemediarendereroperation**](createmediarendereroperation.md) ", das verwendet wird, um Ergebnisse aus dem asynchronen Vorgang zu erhalten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Imediarendererfactory**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendererfactory)
</dt> </dl>

 

