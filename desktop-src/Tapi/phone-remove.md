---
description: Die TAPI PHONE \_ REMOVE-Nachricht wird gesendet, um eine Anwendung über das Entfernen (Löschen aus dem System) eines Telefongeräts zu informieren.
ms.assetid: 7c888976-65da-477a-b5a6-6e78d5f603b1
title: PHONE_REMOVE Meldung (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a26be60c55b16d0126d0b3be107a95af17dd490c9329343bb27ac6496403d46d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119773900"
---
# <a name="phone_remove-message"></a>PHONE \_ REMOVE-Nachricht

Die TAPI **PHONE \_ REMOVE-Nachricht** wird gesendet, um eine Anwendung über das Entfernen (Löschen aus dem System) eines Telefongeräts zu informieren. Im Allgemeinen wird dies nicht für temporäre Entfernungen verwendet, z. B. für die Extraktion von PCMCIA-Geräten, sondern nur für dauerhafte Entfernungen, bei denen das Gerät nicht mehr vom Dienstanbieter gemeldet wird, wenn TAPI erneut initialisiert wird.


```C++
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hDevice* 
</dt> <dd>

Reserviert. Auf NULL festlegen.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Reserviert. Auf NULL festlegen.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Bezeichner des entfernten Telefongeräts.

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

## <a name="remarks"></a>Hinweise

Anwendungen tapi Version 2.0 oder höher wird eine **PHONE \_ REMOVE-Nachricht** gesendet. Dadurch werden sie darüber informiert, dass das Gerät aus dem System entfernt wurde. Der **PHONE \_ REMOVE-Nachricht** wird auf jedem Telefonhandle eine [**PHONE \_ CLOSE-Nachricht**](phone-close.md) vorangestellt, wenn die Anwendung das Telefon geöffnet hatte. Diese Nachricht wird an alle Anwendungen gesendet, die TAPI Version 2.0 oder höher unterstützen, die [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa)aufgerufen haben, einschließlich anwendungen, für die zu diesem Zeitpunkt keine Telefongeräte geöffnet sind.

Ältere Anwendungen (die TAPI Version 1.4 oder früher ausgehandelt haben) erhalten eine [**PHONE \_ STATE-Nachricht,**](phone-state.md) die PHONESTATE REMOVED angibt, \_ gefolgt von einer PHONE [**\_ CLOSE-Nachricht.**](phone-close.md) Im Gegensatz zur **PHONE \_ REMOVE-Nachricht** können diese älteren Anwendungen diese Nachrichten jedoch nur empfangen, wenn das Telefon beim Entfernen geöffnet ist. Wenn das Telefon nicht geöffnet ist, würde der einzige Hinweis darauf, dass das Gerät entfernt wurde, beim Versuch, auf das Gerät zuzugreifen, eine PHONEERR \_ NODEVICE empfangen.

Nachdem ein Gerät entfernt wurde, führt jeder Versuch, über seine Geräte-ID auf das Gerät zuzugreifen, zu einem PHONEERR \_ NODEVICE-Fehler. Nachdem alle TAPI-Anwendungen heruntergefahren wurden, sodass TAPI neu gestartet werden kann, und wenn TAPI erneut initialisiert wird, nimmt das entfernte Gerät keinen Gerätebezeichner mehr ein.

> [!Note]  
> Implementierung: TapI gibt diese PHONEERR \_ NODEVICE-Nachricht zurück, nachdem eine PHONE \_ REMOVE-Nachricht von einem Dienstanbieter empfangen wurde. Es werden keine weiteren Anrufe an diesen Dienstanbieter unter Verwendung dieses Telefongerätebezeichners durchgeführt.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2.0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**PHONE \_ CLOSE**](phone-close.md)
</dt> <dt>

[**\_TELEFONSTATUS**](phone-state.md)
</dt> <dt>

[**phoneInitialize**](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize)
</dt> <dt>

[**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa)
</dt> </dl>

 

 




