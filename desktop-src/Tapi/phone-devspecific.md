---
description: TAPI sendet die PHONE \_ DEVSPECIFIC-Nachricht an eine Anwendung, um die Anwendung über gerätespezifische Ereignisse auf dem Telefon zu benachrichtigen. Die Bedeutung der Nachricht und die Interpretation der Parameter ist implementierungsdefiniert.
ms.assetid: e3e803dd-b041-48b7-9acf-a89989370204
title: PHONE_DEVSPECIFIC Meldung (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 578ba0960963f85ff597d9a6bc87ff3369a6c837ed58367bd82d62a13341e988
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072900"
---
# <a name="phone_devspecific-message"></a>PHONE \_ DEVSPECIFIC-Nachricht

TAPI sendet die **PHONE \_ DEVSPECIFIC-Nachricht** an eine Anwendung, um die Anwendung über gerätespezifische Ereignisse auf dem Telefon zu benachrichtigen. Die Bedeutung der Nachricht und die Interpretation der Parameter ist implementierungsdefiniert.


```C++
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hPhone* 
</dt> <dd>

Ein Handle für das Telefongerät.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Die Rückrufinstanz der Anwendung, die beim Öffnen des Telefongeräts bereitgestellt wird.

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
| TAPI-Version<br/> | Erfordert TAPI 2.0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




