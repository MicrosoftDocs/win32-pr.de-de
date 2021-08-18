---
title: IBasicDevice Description-Methode
description: Ruft eine Beschreibung des Geräts ab.
ms.assetid: 9973AC46-E6BA-4931-BDEB-E64B147AB291
keywords:
- Beschreibungsmethode Media Streaming-API
- 'Beschreibungsmethode: Media Streaming-API, IBasicDevice-Schnittstelle'
- IBasicDevice-Schnittstelle Media Streaming-API, Beschreibungsmethode
topic_type:
- apiref
api_name:
- IBasicDevice.Description
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cfaf3ba8ca9c74d094aa8cdc15f4c190d6e5141fb11ff255b6e7682b667846d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972349"
---
# <a name="ibasicdevicedescription-method"></a>IBasicDevice::D escription-Methode

Ruft eine Beschreibung des Geräts ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT Description(
  [out] HSTRING *value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*value* \[ out\]
</dt> <dd>

Empfängt einen Zeiger auf die Beschreibung des Geräts.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IBasicDevice**](ibasicdevice.md)
</dt> </dl>

 

 





