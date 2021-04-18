---
description: Die TAPI Line \_ Create-Meldung wird gesendet, um die Anwendung über die Erstellung eines neuen Zeilen Geräts zu informieren.
ms.assetid: d4735eab-392f-49d9-a1d9-5895d9232624
title: LINE_CREATE Meldung (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd9973849c3942b5427dfb6b3fe7c47bc4d2a716
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357679"
---
# <a name="line_create-message"></a>Nachricht zum Erstellen von Zeilen \_

Die TAPI **line \_ Create** -Meldung wird gesendet, um die Anwendung über die Erstellung eines neuen Zeilen Geräts zu informieren.


```C++
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hdevice* 
</dt> <dd>

Nicht verwendet.

</dd> <dt>

*dwcallbackinstance* 
</dt> <dd>

Nicht verwendet.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Die *HDE viceid* des neu erstellten Geräts.

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

Ältere Anwendungen (die die TAPI-Version 1,3 aushandeln) werden an eine [**line- \_ linedevstate**](line-linedevstate.md) -Nachricht gesendet, die linedevstate \_ REIT angibt. Dies erfordert, dass Sie Ihre Verwendung der API Herunterfahren und [**lineinitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize) erneut aufrufen, um die neue Anzahl von Geräten zu erhalten. Im Gegensatz zu früheren Versionen von TAPI erfordert diese Version jedoch nicht, dass alle Anwendungen heruntergefahren werden, bevor Anwendungen erneut initialisiert werden können. die erneute Initialisierung kann sofort durchgeführt werden, wenn ein neues Gerät erstellt wird (das Herunterfahren ist nach wie vor erforderlich, wenn ein Dienstanbieter aus dem System entfernt wird).

Anwendungen, die TAPI-Version 1,4 oder höher unterstützen, werden als Nachricht zum **\_ Erstellen von Zeilen** gesendet Dadurch werden Sie darüber informiert, dass das neue Gerät und die neue Gerätekennung vorhanden sind. Die Anwendung kann dann auswählen, ob versucht werden soll, mit dem neuen Gerät zu arbeiten. Diese Nachricht wird an alle Anwendungen gesendet, die diese oder nachfolgende Versionen der API unterstützen, die [**lineinitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize) oder [**lineinitializeex**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa)aufgerufen haben, einschließlich derjenigen, die zu diesem Zeitpunkt keine Zeilen Geräte geöffnet haben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2,0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_linienlinedevstate**](line-linedevstate.md)
</dt> <dt>

[**lineinitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize)
</dt> <dt>

[**lineinitializeex**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa)
</dt> </dl>

 

 




