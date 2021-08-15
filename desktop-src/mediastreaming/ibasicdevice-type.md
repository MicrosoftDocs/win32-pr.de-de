---
title: IBasicDevice-Typmethode
description: Ruft einen Enumerationswert ab, der den Gerätetyp des DLNA-Geräts angibt.
ms.assetid: D9FB3A02-7796-4ACB-B7D3-D171D1D9B77F
keywords:
- Typmethode Medienstreaming-API
- Typmethode Media Streaming API , IBasicDevice-Schnittstelle
- IBasicDevice-Schnittstelle Medienstreaming-API , Type-Methode
topic_type:
- apiref
api_name:
- IBasicDevice.Type
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 433b255615a3fb57d59589b09a4a8b3e0f4cec5c02115bc737041d1fd94a197f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119100624"
---
# <a name="ibasicdevicetype-method"></a>IBasicDevice::Type-Methode

Ruft einen Enumerationswert ab, der den Gerätetyp des DLNA-Geräts angibt.

## <a name="syntax"></a>Syntax


```C++
HRESULT Type(
  [out] DeviceTypes *value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wert* \[ out\]
</dt> <dd>

Empfängt einen Zeiger auf einen [**DeviceTypes-Wert.**](devicetypes.md)

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

 

 





