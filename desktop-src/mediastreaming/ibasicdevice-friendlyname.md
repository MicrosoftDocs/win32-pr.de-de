---
title: IBasicDevice FriendlyName-Methode
description: Ruft den Anzeigenamen des Geräts ab.
ms.assetid: 693806E1-CA66-457D-A25B-D79064776965
keywords:
- 'FriendlyName-Methode: Medienstreaming-API'
- FriendlyName-Methode Media Streaming-API, IBasicDevice-Schnittstelle
- IBasicDevice-Schnittstelle Medienstreaming-API , FriendlyName-Methode
topic_type:
- apiref
api_name:
- IBasicDevice.FriendlyName
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 35084fafb92b3716208aa6062f065cc4e25a45d2d1a412083076b9e355d2ce43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118735610"
---
# <a name="ibasicdevicefriendlyname-method"></a>IBasicDevice::FriendlyName-Methode

Ruft den Anzeigenamen des Geräts ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT FriendlyName(
  [out] HSTRING *value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wert* \[ out\]
</dt> <dd>

Empfängt einen Zeiger auf den Anzeigenamen des Geräts.

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

 

 





