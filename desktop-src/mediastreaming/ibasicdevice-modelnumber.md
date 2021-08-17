---
title: IBasicDevice ModelNumber-Methode
description: Ruft die Modellnummer des Geräts ab.
ms.assetid: C4199135-0C6C-4427-8152-224D7D29C270
keywords:
- ModelNumber-Methode – Medienstreaming-API
- 'ModelNumber-Methode: Medienstreaming-API, IBasicDevice-Schnittstelle'
- IBasicDevice-Schnittstelle Medienstreaming-API, ModelNumber-Methode
topic_type:
- apiref
api_name:
- IBasicDevice.ModelNumber
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a2793a67e6dee60c20c613b32b96bb2dda76907b13bd5e7a9c71add86d2c35a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119461900"
---
# <a name="ibasicdevicemodelnumber-method"></a>IBasicDevice::ModelNumber-Methode

Ruft die Modellnummer des Geräts ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT ModelNumber(
  [out] HSTRING *value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*value* \[ out\]
</dt> <dd>

Empfängt einen Zeiger auf die Modellnummer des Geräts.

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

 

 





