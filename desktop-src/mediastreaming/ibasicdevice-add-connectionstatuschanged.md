---
title: Ibasicdevice-add_ConnectionStatusChanged-Methode
description: Registriert einen Ereignishandler für das connectionstatuschangi-Ereignis. | Ibasicdevice-add_ConnectionStatusChanged-Methode
ms.assetid: 1A4CCEFE-B6B6-4AFD-9296-EE923B9EF399
keywords:
- Medien Streaming-API für add_ConnectionStatusChanged-Methode
- add_ConnectionStatusChanged-Methode Medien Streaming-API, ibasicdevice-Schnittstelle
- Ibasicdevice-Schnittstelle Medien Streaming-API, add_ConnectionStatusChanged-Methode
topic_type:
- apiref
api_name:
- IBasicDevice.add_ConnectionStatusChanged
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0028e6f3dad1670974178b0f07a59f74dffdc06f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106366602"
---
# <a name="ibasicdeviceadd_connectionstatuschanged-method"></a>Ibasicdevice:: Add \_ connectionstatuschangi-Methode

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

Um die Registrierung des Ereignis Handlers aufzuheben, der durch diese Methode registriert wurde, übergeben Sie den *Tokenwert* an die [**Remove \_ connectionstatuschangi-**](ibasicdevice-remove-connectionstatuschanged.md) Methode.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ibasicdevice**](ibasicdevice.md)
</dt> </dl>

 

