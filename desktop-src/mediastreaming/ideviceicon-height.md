---
title: IDeviceIcon Height-Methode
description: Ruft die Höhe des Symbols in Pixel ab.
ms.assetid: 06E1B3AD-FF49-4BC9-AC67-E2E00954475F
keywords:
- Height-Methode – Medienstreaming-API
- Height-Methode Media Streaming-API, IDeviceIcon-Schnittstelle
- IDeviceIcon-Schnittstelle Medienstreaming-API , Height-Methode
topic_type:
- apiref
api_name:
- IDeviceIcon.Height
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8d813c572b0fc9e562d40326d830c5ef3530857601811df78c3acd541314b402
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060290"
---
# <a name="ideviceiconheight-method"></a>IDeviceIcon::Height-Methode

Ruft die Höhe des Symbols in Pixel ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT Height(
  [out] UINT32 *value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wert* \[ out\]
</dt> <dd>

Empfängt einen Zeiger auf die Höhe des Symbols in Pixel.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IDeviceIcon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon)
</dt> </dl>

 

