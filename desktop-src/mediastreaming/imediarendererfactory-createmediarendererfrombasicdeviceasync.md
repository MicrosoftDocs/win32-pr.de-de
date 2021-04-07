---
title: Imediarendererfactory-Methode "kreatemediarendererfrombasicdeviceasync"
description: Erstellt asynchron eine neue Instanz eines Objekts, das die imediarenderer-Schnittstelle mithilfe der angegebenen ibasicdevice-Schnittstelle implementiert.
ms.assetid: 14A83789-0F3C-467B-8EFD-3BB421C54217
keywords:
- Methode "kreatemediarendererfrombasicdeviceasync" Medien Streaming-API
- Methode "kreatemediarendererfrombasicdeviceasync" Media Streaming API, imediarendererfactory-Schnittstelle
- Imediarendererfactory-Schnittstelle Medien Streaming-API, Methode "kreatemediarendererfrombasicdeviceasync"
topic_type:
- apiref
api_name:
- IMediaRendererFactory.CreateMediaRendererFromBasicDeviceAsync
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7e4ee614cca9a03ca203ecde9203e019fab38ab4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038891"
---
# <a name="imediarendererfactorycreatemediarendererfrombasicdeviceasync-method"></a>Imediarendererfactory:: kreatemediarendererfrombasicdeviceasync-Methode

Erstellt asynchron eine neue Instanz eines Objekts, das die [**imediarenderer**](imediarenderer.md) -Schnittstelle mithilfe der angegebenen [**ibasicdevice**](ibasicdevice.md) -Schnittstelle implementiert.

## <a name="syntax"></a>Syntax


```C++
HRESULT CreateMediaRendererFromBasicDeviceAsync(
  [in]          IBasicDevice                 *basicDevice,
  [out, retval] CreateMediaRendererOperation **value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*basicdevice* \[ in\]
</dt> <dd>

Ein Zeiger auf eine [**ibasicdevice**](ibasicdevice.md) -Schnittstelle, die das Gerät darstellt, für das eine Instanz von [**imediarenderer**](imediarenderer.md) erstellt wird.

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

 

