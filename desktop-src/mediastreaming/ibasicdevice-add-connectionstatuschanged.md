---
title: IBasicDevice add_ConnectionStatusChanged-Methode
description: Registriert einen Ereignishandler für das ConnectionStatusChanged-Ereignis. | IBasicDevice add_ConnectionStatusChanged-Methode
ms.assetid: 1A4CCEFE-B6B6-4AFD-9296-EE923B9EF399
keywords:
- add_ConnectionStatusChanged Medienstreaming-API
- add_ConnectionStatusChanged Media Streaming-API, IBasicDevice-Schnittstelle
- IBasicDevice-Schnittstelle Medienstreaming-API , add_ConnectionStatusChanged-Methode
topic_type:
- apiref
api_name:
- IBasicDevice.add_ConnectionStatusChanged
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 55e90ea1f90ccd5b1e141b0e4071213abfe6f4a05a85d3c0d4ced505e1b0f164
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952660"
---
# <a name="ibasicdeviceadd_connectionstatuschanged-method"></a>IBasicDevice::add \_ ConnectionStatusChanged-Methode

Registriert einen Ereignishandler für das [**ConnectionStatusChanged-Ereignis.**](connectionstatuschanged.md)

## <a name="syntax"></a>Syntax


```C++
HRESULT add_ConnectionStatusChanged(
  [in]          ConnectionStatusHandler *handler,
  [out, retval] EventRegistrationToken  *token
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Handler* \[ In\]
</dt> <dd>

Eine [](/previous-versions/windows/desktop/legacy/hh828836(v=vs.85)) ConnectionStatusHandler-Ereignishandlerfunktion.

</dd> <dt>

*Token* \[ out, retval\]
</dt> <dd>

Verweis auf ein Token, mit dem die Registrierung des Ereignishandlers aufgehoben werden kann.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="remarks"></a>Hinweise

Um die Registrierung des Von dieser Methode registrierten Ereignishandlers aufzuheben, übergeben Sie den *Tokenwert* an die [**\_ remove ConnectionStatusChanged-Methode.**](ibasicdevice-remove-connectionstatuschanged.md)

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IBasicDevice**](ibasicdevice.md)
</dt> </dl>

 

