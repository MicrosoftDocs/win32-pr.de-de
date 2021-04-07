---
title: Ibasicdevice-Symbol Methode
description: Gibt einen Vektor von ideviceicon-Schnittstellen zurück.
ms.assetid: 0C083AF3-FE22-4A8E-87B7-0FFA7B65ADBD
keywords:
- Symbol Methode Medien Streaming-API
- Symbol Methode Medien Streaming-API, ibasicdevice-Schnittstelle
- Ibasicdevice-Schnittstelle Medien Streaming-API, Symbol-Methode
topic_type:
- apiref
api_name:
- IBasicDevice.Icons
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3fb6e4b708b4e38ffb39f152308cec7b885a772f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103724985"
---
# <a name="ibasicdeviceicons-method"></a>Ibasicdevice:: Icons-Methode

Gibt einen Vektor von [**ideviceicon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon) -Schnittstellen zurück.

## <a name="syntax"></a>Syntax


```C++
HRESULT Icons(
  [out] IVector< IDeviceIcon > **value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Wert* \[ vorgenommen\]
</dt> <dd>

Empfängt eine Aufzähl Bare Auflistung von [**ideviceicon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon) -Schnittstellen Zeigern.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ibasicdevice**](ibasicdevice.md)
</dt> </dl>

 

