---
title: IBasicDevice ModelUrl-Methode
description: Ruft die Modell-URL des Geräts ab.
ms.assetid: 093D306B-5DFC-4A68-803D-3DDE195A8B85
keywords:
- Media Streaming-API der ModelUrl-Methode
- 'ModelUrl-Methode: Medienstreaming-API, IBasicDevice-Schnittstelle'
- IBasicDevice-Schnittstelle Medienstreaming-API , ModelUrl-Methode
topic_type:
- apiref
api_name:
- IBasicDevice.ModelUrl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2e7595af295b0d0bc565d79bf5450ee6c5c16b0da4f3baa4fcf636e4e5386920
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847650"
---
# <a name="ibasicdevicemodelurl-method"></a>IBasicDevice::ModelUrl-Methode

Ruft die Modell-URL des Geräts ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT ModelUrl(
  [out] HSTRING *value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wert* \[ out\]
</dt> <dd>

Empfängt einen Zeiger auf die Modell-URL des Geräts.

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

 

 





