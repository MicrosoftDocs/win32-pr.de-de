---
title: BasicDevice.remove_ConnectionStatusChanged-Methode
description: Aufheben der Registrierung eines Ereignishandlers für das ConnectionStatusChanged-Ereignis. | BasicDevice.remove_ConnectionStatusChanged-Methode
ms.assetid: 537CA8FE-D2E1-4CC7-BB80-FBE36A2D4A1E
keywords:
- remove_ConnectionStatusChanged Media Streaming-API
- remove_ConnectionStatusChanged Media Streaming-API, BasicDevice-Schnittstelle
- BasicDevice-Schnittstelle Media Streaming-API , remove_ConnectionStatusChanged-Methode
topic_type:
- apiref
api_name:
- BasicDevice.remove_ConnectionStatusChanged
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 89057195c23aa917c7338a8abb740817bb6af7896261cf1d31bcb37d5d5d5ab8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972499"
---
# <a name="basicdeviceremove_connectionstatuschanged-method"></a>BasicDevice.remove \_ ConnectionStatusChanged-Methode

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

Ein Verweis auf ein Token, das von der [**\_ Add ConnectionStatusChanged-Methode beim**](basicdevice-add-connectionstatuschanged.md) Registrieren des Ereignishandlers erhalten wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**BasicDevice**](/previous-versions/windows/desktop/legacy/hh828813(v=vs.85))
</dt> </dl>

 

