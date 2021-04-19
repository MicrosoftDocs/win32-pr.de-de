---
description: Die Richtlinien \_ -DevSpecific-Nachricht wird gesendet, um die Anwendung über gerätespezifische Ereignisse zu benachrichtigen, die in einer Zeile, Adresse oder einem Rückruf auftreten. Die Bedeutung der Nachricht und die Interpretation der Parameter sind gerätespezifisch.
ms.assetid: 6a58e77b-6ee2-4d2d-aca2-71b239f6a1dc
title: LINE_DEVSPECIFIC Meldung (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91907b10c0176258648fa165bbeb922a61a402ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359671"
---
# <a name="line_devspecific-message"></a>Zeilen- \_ DevSpecific-Nachricht

Die Richt **Linien- \_ DevSpecific** -Nachricht wird gesendet, um die Anwendung über gerätespezifische Ereignisse zu benachrichtigen, die in einer Zeile, Adresse oder einem Rückruf auftreten. Die Bedeutung der Nachricht und die Interpretation der Parameter sind gerätespezifisch.


```C++
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hdevice* 
</dt> <dd>

Ein Handle für ein Zeilen Gerät oder einen-Befehl. Dies ist gerätespezifisch.

</dd> <dt>

*dwcallbackinstance* 
</dt> <dd>

Die beim Öffnen der Zeile angegebene Rückruf Instanz.

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

## <a name="remarks"></a>Bemerkungen

Die **\_ DevSpecific-Zeilen** Meldung wird von einem Dienstanbieter in Verbindung mit der [**linedevspecific**](/windows/desktop/api/Tapi/nf-tapi-linedevspecific) -Funktion verwendet. Seine Bedeutung ist gerätespezifisch.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2,0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




