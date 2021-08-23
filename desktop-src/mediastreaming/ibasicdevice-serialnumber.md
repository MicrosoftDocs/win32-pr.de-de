---
title: IBasicDevice SerialNumber-Methode
description: Ruft die Seriennummer des Geräts ab.
ms.assetid: 238A5999-0E8B-4462-AFCF-790DB58CFCB4
keywords:
- 'SerialNumber-Methode: Medienstreaming-API'
- 'SerialNumber-Methode: Medienstreaming-API, IBasicDevice-Schnittstelle'
- IBasicDevice-Schnittstelle Medienstreaming-API, SerialNumber-Methode
topic_type:
- apiref
api_name:
- IBasicDevice.SerialNumber
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 37a4985754982b8b64246d8d0d0fac0d2c37f4a37f159d2e5087497442c97a75
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119712940"
---
# <a name="ibasicdeviceserialnumber-method"></a>IBasicDevice::SerialNumber-Methode

Ruft die Seriennummer des Geräts ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT SerialNumber(
  [out] HSTRING *value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*value* \[ out\]
</dt> <dd>

Empfängt einen Zeiger auf die Seriennummer des Geräts.

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

 

 





