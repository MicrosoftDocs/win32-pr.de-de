---
title: IDeviceIcon Width-Methode
description: Ruft die Breite des Symbols in Pixel ab.
ms.assetid: 28ADA921-6808-43B8-966E-BA42B1B52931
keywords:
- Breitenmethode Medienstreaming-API
- Width-Methode Media Streaming-API, IDeviceIcon-Schnittstelle
- IDeviceIcon-Schnittstelle Medienstreaming-API , Width-Methode
topic_type:
- apiref
api_name:
- IDeviceIcon.Width
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cc76fcd7915c350e04cbacfe756e424d31b0d27d5ced38b0ccf8664805fc9bb5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118473462"
---
# <a name="ideviceiconwidth-method"></a>IDeviceIcon::Width-Methode

Ruft die Breite des Symbols in Pixel ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT Width(
  [out] UINT32 *value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wert* \[ out\]
</dt> <dd>

Empfängt einen Zeiger auf die Breite des Symbols in Pixel.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IDeviceIcon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon)
</dt> </dl>

 

