---
title: IBasicDevice UniqueDeviceName-Methode
description: Ruft den eindeutigen Gerätenamen (UDN) des Geräts ab.
ms.assetid: 393EFF96-69E1-4081-905D-D8CC47B5FC4A
keywords:
- UniqueDeviceName-Methode Media Streaming-API
- UniqueDeviceName-Methode Media Streaming API , IBasicDevice-Schnittstelle
- IBasicDevice-Schnittstelle Medienstreaming-API , UniqueDeviceName-Methode
topic_type:
- apiref
api_name:
- IBasicDevice.UniqueDeviceName
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7b70fbc2021cf717cdb49d8a222aa33ad4e9213f297364b81af065c3bbeaed99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972319"
---
# <a name="ibasicdeviceuniquedevicename-method"></a>IBasicDevice::UniqueDeviceName-Methode

Ruft den eindeutigen Gerätenamen (UDN) des Geräts ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT UniqueDeviceName(
  [out] HSTRING *value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wert* \[ out\]
</dt> <dd>

Empfängt einen Zeiger auf den Modell-UDN des Geräts.

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

 

 





