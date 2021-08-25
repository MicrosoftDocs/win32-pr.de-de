---
title: IBasicDevice ManufacturerName-Methode
description: Ruft den Herstellernamen des Geräts ab.
ms.assetid: F04400C9-02FC-4CB5-B355-A7E84BECD098
keywords:
- 'ManufacturerName-Methode: Medienstreaming-API'
- ManufacturerName-Methode Media Streaming-API, IBasicDevice-Schnittstelle
- IBasicDevice-Schnittstelle Medienstreaming-API , ManufacturerName-Methode
topic_type:
- apiref
api_name:
- IBasicDevice.ManufacturerName
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 453e11fc547998b6dc3e39017684c30cacd205c0c17b21846925d4de472f43a7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120011830"
---
# <a name="ibasicdevicemanufacturername-method"></a>IBasicDevice::ManufacturerName-Methode

Ruft den Herstellernamen des Geräts ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT ManufacturerName(
  [out] HSTRING *value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wert* \[ out\]
</dt> <dd>

Empfängt einen Zeiger auf den Herstellernamen des Geräts.

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

 

 





