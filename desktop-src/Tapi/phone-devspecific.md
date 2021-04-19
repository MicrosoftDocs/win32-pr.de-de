---
description: TAPI sendet die Phone \_ DevSpecific-Nachricht an eine Anwendung, um die Anwendung über gerätespezifische Ereignisse zu benachrichtigen, die auf dem Telefon auftreten. Die Bedeutung der Nachricht und die Interpretation der Parameter sind Implementierungs definiert.
ms.assetid: e3e803dd-b041-48b7-9acf-a89989370204
title: PHONE_DEVSPECIFIC Meldung (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c817f273a49fdcda36995cec335811fb06c8a917
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373569"
---
# <a name="phone_devspecific-message"></a>\_DevSpecific-Telefonnachricht

TAPI sendet die **Phone \_ DevSpecific** -Nachricht an eine Anwendung, um die Anwendung über gerätespezifische Ereignisse zu benachrichtigen, die auf dem Telefon auftreten. Die Bedeutung der Nachricht und die Interpretation der Parameter sind Implementierungs definiert.


```C++
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hphone* 
</dt> <dd>

Ein Handle für das Telefongerät.

</dd> <dt>

*dwcallbackinstance* 
</dt> <dd>

Die Rückruf Instanz der Anwendung, die beim Öffnen des Telefon Geräts bereitgestellt wird.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Gerätespezifisch.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Gerätespezifisch.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Gerätespezifisch.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2,0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




