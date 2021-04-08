---
title: Ibasicdevice-Methode canwakedevices
description: Ruft einen Wert ab, der angibt, ob das Gerät aktiviert werden kann.
ms.assetid: AAD0597C-AD33-40EE-A5DA-27AC66375D38
keywords:
- Canwakedevices-Methode Medien Streaming-API
- Canwakedevices-Methode Medien Streaming-API, ibasicdevice-Schnittstelle
- Ibasicdevice-Schnittstelle Medien Streaming-API, canwakedevices-Methode
topic_type:
- apiref
api_name:
- IBasicDevice.CanWakeDevices
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 08a893ac880a426f604f2dc1c73173585e507cc0
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104038056"
---
# <a name="ibasicdevicecanwakedevices-method"></a>Ibasicdevice:: canwakedevices-Methode

Ruft einen Wert ab, der angibt, ob das Gerät aktiviert werden kann.

## <a name="syntax"></a>Syntax


```C++
HRESULT CanWakeDevices(
  [out] boolean *value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Wert* \[ vorgenommen\]
</dt> <dd>

Empfängt einen Zeiger auf einen booleschen Wert, der **true** ist, wenn das Gerät aktiviert werden kann.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ibasicdevice**](ibasicdevice.md)
</dt> </dl>

 

 





