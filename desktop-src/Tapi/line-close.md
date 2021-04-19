---
description: Die TAPI-Zeilen \_ Schließen-Nachricht wird gesendet, wenn das angegebene Zeilen Gerät zwangsweise geschlossen wurde. Das Zeilen Geräte handle oder alle Aufruf Handles für Aufrufe in der Zeile sind nicht mehr gültig, nachdem diese Nachricht gesendet wurde.
ms.assetid: f254e331-d574-4fa7-8447-6e4535d3d773
title: LINE_CLOSE Meldung (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7f4fde53d1017b2dcd9fe4ea833803055d9f2dd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369673"
---
# <a name="line_close-message"></a>Zeilen Schluss \_ Nachricht

Die TAPI- **Zeilen \_ Schließen** -Nachricht wird gesendet, wenn das angegebene Zeilen Gerät zwangsweise geschlossen wurde. Das Zeilen Geräte handle oder alle Aufruf Handles für Aufrufe in der Zeile sind nicht mehr gültig, nachdem diese Nachricht gesendet wurde.


```C++
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hdevice* 
</dt> <dd>

Ein Handle für das Zeilen Gerät, das geschlossen wurde. Dieses Handle ist nicht mehr gültig.

</dd> <dt>

*dwcallbackinstance* 
</dt> <dd>

Die beim Öffnen der Zeile angegebene Rückruf Instanz.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Nicht verwendet.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Nicht verwendet.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Die Meldung zum **\_ Schließen der Zeile** wird nur an jede Anwendung gesendet, nachdem der TAPI-Dienstanbieter (TSP) das Schließen einer geöffneten Zeile erzwungen hat. Gibt an, ob die Zeile sofort nach einer erzwungenen Schließung wieder geöffnet werden kann.

Die Ursache kann eine bedeutende Zustandsänderung, ein Hardwarefehler, ein Verlust der Verbindung zu einem Server oder sogar potenziell verhindern, dass eine einzelne Anwendung ein Zeilen Gerät zu lange monopolisiert. Ein liniengerät kann auch erzwungen werden, nachdem der Benutzer die Konfiguration dieser Zeile oder seines Treibers geändert hat. Wenn der Benutzer möchte, dass die Konfigurationsänderungen sofort wirksam werden (im Gegensatz zu nach dem nächsten Neustart des Systems), und Sie sich auf die aktuelle Ansicht des Geräts der Anwendung auswirken (z. b. eine Änderung der Gerätefunktionen), kann ein Dienstanbieter zwangsweise das Zeilen Gerät schließen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2,0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




