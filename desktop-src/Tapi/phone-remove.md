---
description: Die TAPI-Telefon \_ Entfernungs Nachricht wird gesendet, um eine Anwendung über das Entfernen (Löschen vom System) eines Telefon Geräts zu informieren.
ms.assetid: 7c888976-65da-477a-b5a6-6e78d5f603b1
title: PHONE_REMOVE Meldung (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ab32ba8b8a8e003c5d87109dd2d0c9dbe98c236
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370688"
---
# <a name="phone_remove-message"></a>Meldung zum Entfernen des Telefons \_

Die TAPI- **Telefon \_ Entfernungs** Nachricht wird gesendet, um eine Anwendung über das Entfernen (Löschen vom System) eines Telefon Geräts zu informieren. Dies wird im Allgemeinen nicht für temporäre Entfernungen verwendet, wie z. b. das Extrahieren von PCMCIA-Geräten, sondern nur für permanente Entfernungen, bei denen das Gerät nicht mehr vom Dienstanbieter gemeldet wird, wenn TAPI erneut initialisiert wurde.


```C++
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hdevice* 
</dt> <dd>

Reserviert. Auf NULL festlegen.

</dd> <dt>

*dwcallbackinstance* 
</dt> <dd>

Reserviert. Auf NULL festlegen.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Der Bezeichner des entfernten Phone-Geräts.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Reserviert. Auf NULL festlegen.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Reserviert. Auf NULL festlegen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Anwendungen TAPI Version 2,0 oder höher wird eine Nachricht **zum \_ Entfernen per Telefon** gesendet. Dadurch werden Sie darüber informiert, dass das Gerät aus dem System entfernt wurde. Der **Telefon \_ Entfernungs** Meldung wird eine Telefonnachricht zum [**\_ Schließen**](phone-close.md) der Telefonnummer vorangestellt, wenn für die Anwendung das Telefon geöffnet war. Diese Nachricht wird an alle Anwendungen gesendet, die TAPI-Version 2,0 oder höher unterstützen, die " [**phoneinitializeex**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa)" genannt haben, einschließlich derjenigen, die keine Telefongeräte gleichzeitig geöffnet haben.

Älteren Anwendungen (die die TAPI-Version 1,4 oder früher ausgehandelt haben) wird eine [**Telefon \_ Zustands**](phone-state.md) Meldung gesendet \_ , in der phonestate entfernt wird, gefolgt von einer Meldung zum [**\_ Schließen des Telefons**](phone-close.md) . Anders als bei der **Telefon \_ Entfernungs** Nachricht können diese älteren Anwendungen diese Nachrichten jedoch nur empfangen, wenn Sie das Telefon geöffnet haben, wenn es entfernt wird. Wenn kein Telefon geöffnet ist, erhält der einzige Hinweis darauf, dass das Gerät entfernt wurde, \_ beim Versuch, auf das Gerät zuzugreifen, ein phoneerr-nodevice.

Nachdem ein Gerät entfernt wurde, führt jeder Versuch, über seine Gerätekennung auf das Gerät zuzugreifen, zu einem phoneerr- \_ nodevice-Fehler. Nachdem alle TAPI-Anwendungen heruntergefahren wurden, sodass TAPI neu gestartet werden kann, und wenn TAPI erneut initialisiert wird, belegt das entfernte Gerät keinen Geräte Bezeichner mehr.

> [!Note]  
> Implementierung: Dies ist TAPI, die diese phoneerr \_ nodevice-Nachricht zurückgibt, nachdem eine Telefon \_ Entfernungs Nachricht von einem Dienstanbieter empfangen wurde. es werden keine weiteren Aufrufe an den Dienstanbieter über diese Telefongeräte-ID gesendet.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2,0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Telefon \_ Schließen**](phone-close.md)
</dt> <dt>

[**Telefon \_ Status**](phone-state.md)
</dt> <dt>

[**phoneinitialize**](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize)
</dt> <dt>

[**phoneinitializeex**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa)
</dt> </dl>

 

 




