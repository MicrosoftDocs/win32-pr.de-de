---
description: Das DVDNotify-Ereignis benachrichtigt eine Anwendung über viele verschiedene DVD-Ereignisse und Datenträgeranweisungen.
ms.assetid: 8e7d85fb-95c0-472d-ab17-a82da303b68f
title: DVDNotify (Segment.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 988deaf53fb2b50555b4cf19a38684610aa0822a270dfba079defab92ce8aec0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119148703"
---
# <a name="dvdnotify"></a>DVDNotify

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Das Ereignis benachrichtigt eine Anwendung über viele verschiedene `DVDNotify` DVD-Ereignisse und Datenträgeranweisungen.

``` syntax
DVDNotify(EventCode, Param1, Param2)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="EventCode"></span><span id="eventcode"></span><span id="EVENTCODE"></span>*EventCode*
</dt> <dd>

Gibt den DVD-Ereignisbenachrichtigungscode an.

</dd> <dt>

<span id="Param1"></span><span id="param1"></span><span id="PARAM1"></span>*Param1*
</dt> <dd>

Kann zusätzliche Informationen im Zusammenhang mit dem Ereignis enthalten.

</dd> <dt>

<span id="Param2"></span><span id="param2"></span><span id="PARAM2"></span>*Param2*
</dt> <dd>

Kann zusätzliche Informationen im Zusammenhang mit dem Ereignis enthalten.

</dd> </dl>

## <a name="remarks"></a>Hinweise

[DVD-Ereignisbenachrichtigungscodes](dvd-notification-codes.md) enthalten eine vollständige Erläuterung aller DVD-Ereignisbenachrichtigungscodes und ihrer Parameter.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|--------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Segment.h</dt> </dl> |



 

 




