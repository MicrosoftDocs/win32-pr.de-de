---
title: IBasicDevice ManufacturerUrl-Methode
description: Ruft die Hersteller-URL des Geräts ab.
ms.assetid: E8372D15-D8B5-49E4-950A-96B4A88B0450
keywords:
- ManufacturerUrl-Methode Medienstreaming-API
- ManufacturerUrl-Methode Media Streaming-API, IBasicDevice-Schnittstelle
- IBasicDevice-Schnittstelle Media Streaming-API, ManufacturerUrl-Methode
topic_type:
- apiref
api_name:
- IBasicDevice.ManufacturerUrl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 306b4c194d7354b071d4daaf223a17f977b38b44243adaef856f9acffbf49c83
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972339"
---
# <a name="ibasicdevicemanufacturerurl-method"></a>IBasicDevice::ManufacturerUrl-Methode

Ruft die Hersteller-URL des Geräts ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT ManufacturerUrl(
  [out] HSTRING *value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*value* \[ out\]
</dt> <dd>

Empfängt einen Zeiger auf die Hersteller-URL des Geräts.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IBasicDevice**](ibasicdevice.md)
</dt> </dl>

 

 





