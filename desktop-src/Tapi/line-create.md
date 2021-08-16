---
description: Die TAPI LINE \_ CREATE-Meldung wird gesendet, um die Anwendung über die Erstellung eines neuen Liniengeräts zu informieren.
ms.assetid: d4735eab-392f-49d9-a1d9-5895d9232624
title: LINE_CREATE (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ab18245dc151f074588216d272c305c3a4cbd6aaa85c650ec9854710f5b9eac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117762274"
---
# <a name="line_create-message"></a>LINE \_ CREATE-Nachricht

Die TAPI **LINE \_ CREATE-Meldung** wird gesendet, um die Anwendung über die Erstellung eines neuen Liniengeräts zu informieren.


```C++
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hDevice* 
</dt> <dd>

Nicht verwendet.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Nicht verwendet.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Die *hDeviceID* des neu erstellten Geräts.

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

## <a name="remarks"></a>Hinweise

Ältere Anwendungen (die TAPI Version 1.3 ausgehandelt haben) erhalten eine [**LINE \_ LINEDEVSTATE-Nachricht,**](line-linedevstate.md) die LINEDEVSTATE REINIT anfordert. Daher müssen sie ihre Verwendung der API beenden und \_ [**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize) erneut aufrufen, um die neue Anzahl von Geräten zu erhalten. Im Gegensatz zu früheren Versionen von TAPI erfordert diese Version jedoch nicht, dass alle Anwendungen heruntergefahren werden, bevor anwendungen erneut initialisiert werden können. Die Neuinialisierung kann sofort stattfinden, wenn ein neues Gerät erstellt wird (ein vollständiges Herunterfahren ist immer noch erforderlich, wenn ein Dienstanbieter aus dem System entfernt wird).

Anwendungen, die TAPI Version 1.4 oder höher unterstützen, erhalten eine **LINE \_ CREATE-Nachricht.** Dadurch werden sie über das Vorhandensein des neuen Geräts und seine neue Geräte-ID informiert. Die Anwendung kann dann auswählen, ob sie versucht, mit dem neuen Gerät zu arbeiten. Diese Meldung wird an alle Anwendungen gesendet, die diese oder nachfolgende Versionen der API unterstützen, die [**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize) oder [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa)aufgerufen haben, einschließlich der Anwendungen, für die zu diesem Zeitpunkt keine Liniengeräte geöffnet sind.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2.0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**LINE \_ LINEDEVSTATE**](line-linedevstate.md)
</dt> <dt>

[**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize)
</dt> <dt>

[**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa)
</dt> </dl>

 

 




