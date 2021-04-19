---
title: BasicDevice.add_ConnectionStatusChanged-Methode
description: Registriert einen Ereignishandler für das connectionstatuschangi-Ereignis. | BasicDevice.add_ConnectionStatusChanged-Methode
ms.assetid: FFAA0981-508C-4300-9CA9-24C6AFC1183D
keywords:
- Medien Streaming-API für add_ConnectionStatusChanged-Methode
- add_ConnectionStatusChanged-Methode Medien Streaming-API, basicdevice-Schnittstelle
- Basicdevice-Schnittstelle Medien Streaming-API, add_ConnectionStatusChanged-Methode
topic_type:
- apiref
api_name:
- BasicDevice.add_ConnectionStatusChanged
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 61a36e46d554a953ecd061ccf2396d33b0578d8f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106353659"
---
# <a name="basicdeviceadd_connectionstatuschanged-method"></a>Basicdevice. Add \_ connectionstatuschangimethod

Registriert einen Ereignishandler für das [**connectionstatuschangi-Ereignis**](connectionstatuschanged.md) .

## <a name="syntax"></a>Syntax


```C++
HRESULT add_ConnectionStatusChanged(
  [in]          ConnectionStatusHandler *handler,
  [out, retval] EventRegistrationToken  *token
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Handler* \[ in\]
</dt> <dd>

Eine [**connectionstatushandler-Ereignishandlerfunktion**](/previous-versions/windows/desktop/legacy/hh828836(v=vs.85)) .

</dd> <dt>

*Token* \[ Out, retval\]
</dt> <dd>

Verweis auf ein Token, das verwendet werden kann, um die Registrierung des Ereignis Handlers aufzuheben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Um die Registrierung des Ereignis Handlers aufzuheben, der durch diese Methode registriert wurde, übergeben Sie den *Tokenwert* an die [**Remove \_ connectionstatuschangi-**](basicdevice-remove-connectionstatuschanged.md) Methode.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Basicdevice**](/previous-versions/windows/desktop/legacy/hh828813(v=vs.85))
</dt> </dl>

 

