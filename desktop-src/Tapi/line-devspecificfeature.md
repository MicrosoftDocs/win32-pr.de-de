---
description: Die TAPI-Linien- \_ devspecificfeature-Nachricht wird gesendet, um die Anwendung über gerätespezifische Ereignisse zu benachrichtigen, die in einer Zeile, Adresse oder einem Rückruf auftreten. Die Bedeutung der Nachricht und die Interpretation der Parameter sind gerätespezifisch.
ms.assetid: 5f1a4da2-1a2a-4a18-8a69-82d27ddca9cf
title: LINE_DEVSPECIFICFEATURE Meldung (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d45f91f4b3d45b52a345827e6535b054e9cf2c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360438"
---
# <a name="line_devspecificfeature-message"></a>LINE \_ devspecificfeature-Meldung

Die TAPI- **Linien- \_ devspecificfeature** -Nachricht wird gesendet, um die Anwendung über gerätespezifische Ereignisse zu benachrichtigen, die in einer Zeile, Adresse oder einem Rückruf auftreten. Die Bedeutung der Nachricht und die Interpretation der Parameter sind gerätespezifisch.


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

Die **Zeile \_ devspecificfeature** -Nachricht wird von einem Dienstanbieter in Verbindung mit der Funktion [**linedevspecificfeature**](/windows/desktop/api/Tapi/nf-tapi-linedevspecificfeature) verwendet. Seine Bedeutung ist gerätespezifisch.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2,0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




