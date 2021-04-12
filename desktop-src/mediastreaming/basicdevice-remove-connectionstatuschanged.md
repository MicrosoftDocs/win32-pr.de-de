---
title: BasicDevice.remove_ConnectionStatusChanged-Methode
description: Hebt die Registrierung eines Ereignis Handlers für das connectionstatuschge-Ereignis auf. | BasicDevice.remove_ConnectionStatusChanged-Methode
ms.assetid: 537CA8FE-D2E1-4CC7-BB80-FBE36A2D4A1E
keywords:
- Medien Streaming-API für remove_ConnectionStatusChanged-Methode
- remove_ConnectionStatusChanged-Methode Medien Streaming-API, basicdevice-Schnittstelle
- Basicdevice-Schnittstelle Medien Streaming-API, remove_ConnectionStatusChanged-Methode
topic_type:
- apiref
api_name:
- BasicDevice.remove_ConnectionStatusChanged
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fdd39309774a61c4fd115ff09e16428101439a0b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104219300"
---
# <a name="basicdeviceremove_connectionstatuschanged-method"></a>Basicdevice. Remove \_ connectionstatuschangimethod

Hebt die Registrierung eines Ereignis Handlers für das [**connectionstatuschge**](connectionstatuschanged.md) -Ereignis auf.

## <a name="syntax"></a>Syntax


```C++
HRESULT remove_ConnectionStatusChanged(
  [in] EventRegistrationToken *token
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Token* \[ in\]
</dt> <dd>

Ein Verweis auf ein Token, das von der [**Add \_ connectionstatuschangi-**](basicdevice-add-connectionstatuschanged.md) Methode abgerufen wurde, als der Ereignishandler registriert wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Basicdevice**](/previous-versions/windows/desktop/legacy/hh828813(v=vs.85))
</dt> </dl>

 

