---
title: IBasicDevice IpAddresses-Methode
description: Gibt einen Vektor von IP-Adressen zurück.
ms.assetid: F48B91DC-3AE2-462F-835B-292BF86904B3
keywords:
- 'IpAddresses-Methode: Medienstreaming-API'
- IpAddresses-Methode Media Streaming API , IBasicDevice-Schnittstelle
- IBasicDevice-Schnittstelle Medienstreaming-API , IpAddresses-Methode
topic_type:
- apiref
api_name:
- IBasicDevice.IpAddresses
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dc997abb24c007e9e3e4d5c8028762daaca20e434ca4e3ab22fb278f567f998c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847680"
---
# <a name="ibasicdeviceipaddresses-method"></a>IBasicDevice::IpAddresses-Methode

Gibt einen Vektor von IP-Adressen zurück.

## <a name="syntax"></a>Syntax


```C++
HRESULT IpAddresses(
  [out] IVector< HSTRING > **value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wert* \[ out\]
</dt> <dd>

Empfängt eine aufzählbare Auflistung von Zeigern auf IP-Adressen.

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

 

 





