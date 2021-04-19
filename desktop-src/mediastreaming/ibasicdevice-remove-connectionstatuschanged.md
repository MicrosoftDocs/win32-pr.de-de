---
title: Ibasicdevice-remove_ConnectionStatusChanged-Methode
description: Hebt die Registrierung eines Ereignis Handlers für das connectionstatuschge-Ereignis auf. | Ibasicdevice-remove_ConnectionStatusChanged-Methode
ms.assetid: 577D9C50-486D-441A-A9FE-AF79D1FC2B52
keywords:
- Medien Streaming-API für remove_ConnectionStatusChanged-Methode
- remove_ConnectionStatusChanged-Methode Medien Streaming-API, ibasicdevice-Schnittstelle
- Ibasicdevice-Schnittstelle Medien Streaming-API, remove_ConnectionStatusChanged-Methode
topic_type:
- apiref
api_name:
- IBasicDevice.remove_ConnectionStatusChanged
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 45c2bfa2886774ad637e66385a057c9d4e21efe0
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106361813"
---
# <a name="ibasicdeviceremove_connectionstatuschanged-method"></a>Ibasicdevice:: Remove \_ connectionstatuschangimethod

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

Ein Verweis auf ein Token, das von der [**Add \_ connectionstatuschangi-**](ibasicdevice-add-connectionstatuschanged.md) Methode abgerufen wurde, als der Ereignishandler registriert wurde.

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

 

 





