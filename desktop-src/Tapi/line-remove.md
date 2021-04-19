---
description: Die TAPI-Zeilen \_ Entfernungs Nachricht wird gesendet, um eine Anwendung über das Entfernen (Löschen vom System) eines Zeilen Geräts zu informieren.
ms.assetid: 21b912d6-34aa-4ac0-b019-be3c851cc96d
title: LINE_REMOVE Meldung (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 567ead3ad2941845dd22405f0d8706eca74bfbd8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361958"
---
# <a name="line_remove-message"></a>Zeilen \_ Entfernungs Meldung

Die TAPI- **Zeilen \_ Entfernungs** Nachricht wird gesendet, um eine Anwendung über das Entfernen (Löschen vom System) eines Zeilen Geräts zu informieren. Dies wird im Allgemeinen nicht für temporäre Entfernungen verwendet, wie z. b. das Extrahieren von PCMCIA-Geräten, sondern nur für permanente Entfernungen, bei denen das Gerät nicht mehr vom Dienstanbieter gemeldet wird, wenn TAPI erneut initialisiert wurde.


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

Der Bezeichner des entfernten Zeilen Geräts.

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

Anwendungen, die TAPI-Version 2,0 oder höher unterstützen, werden als **Zeilen \_ Entfernungs** Nachricht gesendet. Dadurch werden Sie darüber informiert, dass das Gerät aus dem System entfernt wurde. Der **Zeilen \_ Entfernungs** Nachricht wird eine [**Zeilen Schluss \_**](line-close.md) Nachricht für jedes Zeilen handle vorangestellt, wenn die Zeile in der Anwendung geöffnet war. Diese Nachricht wird an alle Anwendungen gesendet, die TAPI-Version 2,0 oder höher unterstützen, die [**lineinitializeex**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa)aufgerufen haben, einschließlich derjenigen, die zu diesem Zeitpunkt keine Zeilen Geräte geöffnet haben.

Älteren Anwendungen wird eine [**\_ linienlinedevstate**](line-linedevstate.md) -Nachricht gesendet, in der linedevstate \_ entfernt wird, gefolgt von einer Zeilen Schluss \_ Nachricht. Anders als bei der **Zeilen \_ Entfernungs** Nachricht können diese älteren Anwendungen diese Nachrichten jedoch nur empfangen, wenn die Zeile beim Entfernen geöffnet ist. Wenn die Zeile nicht geöffnet ist, erhalten Sie lediglich den Hinweis, dass das Gerät entfernt wurde, \_ Wenn Sie versuchen, auf das Gerät zuzugreifen.

Nachdem ein Gerät entfernt wurde, führt jeder Versuch, über seine Gerätekennung auf das Gerät zuzugreifen, zu einem lineerr- \_ nodevice-Fehler. Nachdem alle TAPI-Anwendungen heruntergefahren wurden, sodass TAPI neu gestartet werden kann, und wenn TAPI erneut initialisiert wird, belegt das entfernte Gerät keinen Geräte Bezeichner mehr.

> [!Note]  
> Implementierung: Es ist TAPI, die dieses lineerr- \_ nodevice zurückgibt, nachdem eine **Zeile zum \_ Entfernen von Zeilen** von einem Dienstanbieter empfangen wurde. es werden keine weiteren Aufrufe an den Dienstanbieter über diese Geräte-Geräte-ID gesendet.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2,0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Zeilen \_ Schließen**](line-close.md)
</dt> <dt>

[**\_linienlinedevstate**](line-linedevstate.md)
</dt> <dt>

[**lineinitializeex**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa)
</dt> </dl>

 

 




