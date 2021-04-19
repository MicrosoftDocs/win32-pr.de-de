---
description: Die TAPI-Telefon \_ Meldung "Schließen" wird gesendet, wenn ein geöffnetes Telefongerät im Rahmen der Ressourcenrückgewinnung zwangsweise geschlossen wurde. Das Geräte Handle ist nicht mehr gültig, nachdem diese Nachricht gesendet wurde.
ms.assetid: 84650abf-235e-4792-a67d-2f0f08b85a32
title: PHONE_CLOSE Meldung (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d9a7641b437a10098806fc7ad52aa64200ca015
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367079"
---
# <a name="phone_close-message"></a>\_Meldung zum Schließen des Telefons

Die TAPI-Telefon Meldung " **\_ Schließen** " wird gesendet, wenn ein geöffnetes Telefongerät im Rahmen der Ressourcenrückgewinnung zwangsweise geschlossen wurde. Das Geräte Handle ist nicht mehr gültig, nachdem diese Nachricht gesendet wurde.


```C++
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hphone* 
</dt> <dd>

Ein Handle für das geöffnete Telefongerät, das geschlossen wurde. Das Handle ist nicht mehr gültig, nachdem diese Nachricht gesendet wurde.

</dd> <dt>

*dwcallbackinstance* 
</dt> <dd>

Die Rückruf Instanz der Anwendung, die beim Öffnen des Telefon Geräts bereitgestellt wurde.

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

Die Meldung zum **\_ Schließen des Telefons** wird nur an eine Anwendung gesendet, nachdem ein geöffnetes Telefon zwangsweise geschlossen wurde. Dies kann durchgeführt werden, um zu verhindern, dass eine einzelne Anwendung das Telefongerät zu lange monopolisiert. Gibt an, ob das Telefon sofort nach einer erzwungenen Schließung wieder geöffnet werden kann.

Ein geöffnetes Telefongerät kann auch erzwungen werden, nachdem der Benutzer die Konfiguration dieses Telefons oder seines Treibers geändert hat. Wenn der Benutzer möchte, dass die Konfigurationsänderungen sofort wirksam werden (im Gegensatz zu nach dem nächsten Neustart des Systems), und sich diese Änderungen auf die aktuelle Ansicht des Geräts (z. b. eine Änderung der Gerätefunktionen) auswirken, kann ein Dienstanbieter das Telefongerät schließen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2,0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




