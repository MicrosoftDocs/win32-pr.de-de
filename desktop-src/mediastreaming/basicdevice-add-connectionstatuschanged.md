---
title: BasicDevice.add_ConnectionStatusChanged-Methode
description: Registriert einen Ereignishandler für das ConnectionStatusChanged-Ereignis. | BasicDevice.add_ConnectionStatusChanged-Methode
ms.assetid: FFAA0981-508C-4300-9CA9-24C6AFC1183D
keywords:
- 'add_ConnectionStatusChanged-Methode: Medienstreaming-API'
- add_ConnectionStatusChanged Media Streaming-API, BasicDevice-Schnittstelle
- Media Streaming-API der BasicDevice-Schnittstelle , add_ConnectionStatusChanged-Methode
topic_type:
- apiref
api_name:
- BasicDevice.add_ConnectionStatusChanged
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a416770a0ea3a4d317a2308fc9f5c9d940e89900aabbc7651ceb93b789454338
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119462260"
---
# <a name="basicdeviceadd_connectionstatuschanged-method"></a>BasicDevice.add \_ ConnectionStatusChanged-Methode

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

Um die Registrierung des Von dieser Methode registrierten Ereignishandlers aufzuheben, übergeben Sie den *Tokenwert* an die [**\_ remove ConnectionStatusChanged-Methode.**](basicdevice-remove-connectionstatuschanged.md)

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**BasicDevice**](/previous-versions/windows/desktop/legacy/hh828813(v=vs.85))
</dt> </dl>

 

