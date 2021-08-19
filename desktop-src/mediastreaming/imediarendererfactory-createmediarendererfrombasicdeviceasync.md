---
title: IMediaRendererFactory CreateMediaRendererFromBasicDeviceAsync-Methode
description: Erstellt asynchron eine neue Instanz eines -Objekts, das die IMediaRenderer-Schnittstelle mithilfe der angegebenen IBasicDevice-Schnittstelle implementiert.
ms.assetid: 14A83789-0F3C-467B-8EFD-3BB421C54217
keywords:
- Media Streaming-API der CreateMediaRendererFromBasicDeviceAsync-Methode
- CreateMediaRendererFromBasicDeviceAsync-Methode Media Streaming-API, IMediaRendererFactory-Schnittstelle
- IMediaRendererFactory-Schnittstelle Media Streaming-API, CreateMediaRendererFromBasicDeviceAsync-Methode
topic_type:
- apiref
api_name:
- IMediaRendererFactory.CreateMediaRendererFromBasicDeviceAsync
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2b9ee80a4f681bb57d62f84d35cf3a254e38982a10f642a35e35187f6af9e48e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092290"
---
# <a name="imediarendererfactorycreatemediarendererfrombasicdeviceasync-method"></a>IMediaRendererFactory::CreateMediaRendererFromBasicDeviceAsync-Methode

Erstellt asynchron eine neue Instanz eines -Objekts, das die [**IMediaRenderer-Schnittstelle**](imediarenderer.md) mithilfe der angegebenen [**IBasicDevice-Schnittstelle**](ibasicdevice.md) implementiert.

## <a name="syntax"></a>Syntax


```C++
HRESULT CreateMediaRendererFromBasicDeviceAsync(
  [in]          IBasicDevice                 *basicDevice,
  [out, retval] CreateMediaRendererOperation **value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*basicDevice* \[ In\]
</dt> <dd>

Ein Zeiger auf eine [**IBasicDevice-Schnittstelle,**](ibasicdevice.md) die das Gerät darstellt, für das eine Instanz von [**IMediaRenderer**](imediarenderer.md) erstellt wird.

</dd> <dt>

*value* \[ out, retval\]
</dt> <dd>

Empfängt einen Verweis auf ein [**CreateMediaRendererOperation-Objekt,**](createmediarendereroperation.md) das verwendet wird, um Ergebnisse aus dem asynchronen Vorgang zu erhalten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMediaRendererFactory**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendererfactory)
</dt> </dl>

 

