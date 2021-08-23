---
title: IBasicDevice remove_ConnectionStatusChanged Methode
description: Aufheben der Registrierung eines Ereignishandlers für das ConnectionStatusChanged-Ereignis. | IBasicDevice remove_ConnectionStatusChanged Methode
ms.assetid: 577D9C50-486D-441A-A9FE-AF79D1FC2B52
keywords:
- remove_ConnectionStatusChanged Media Streaming-API
- remove_ConnectionStatusChanged Media Streaming-API, IBasicDevice-Schnittstelle
- IBasicDevice-Schnittstelle Media Streaming-API , remove_ConnectionStatusChanged-Methode
topic_type:
- apiref
api_name:
- IBasicDevice.remove_ConnectionStatusChanged
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 35b2f08b6df25f57d77f5c3677a4c6499370d9472202b6808073c5a75d1e2c34
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119599800"
---
# <a name="ibasicdeviceremove_connectionstatuschanged-method"></a>IBasicDevice::remove \_ ConnectionStatusChanged-Methode

Aufheben der Registrierung eines Ereignishandlers für das [**ConnectionStatusChanged-Ereignis.**](connectionstatuschanged.md)

## <a name="syntax"></a>Syntax


```C++
HRESULT remove_ConnectionStatusChanged(
  [in] EventRegistrationToken *token
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Token* \[ In\]
</dt> <dd>

Ein Verweis auf ein Token, das von der [**\_ Add ConnectionStatusChanged-Methode beim**](ibasicdevice-add-connectionstatuschanged.md) Registrieren des Ereignishandlers erhalten wurde.

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

 

 





