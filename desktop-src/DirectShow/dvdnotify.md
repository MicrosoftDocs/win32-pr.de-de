---
description: Das dvdnotify-Ereignis benachrichtigt eine Anwendung über viele verschiedene DVD-Ereignisse und Disk-Anweisungen.
ms.assetid: 8e7d85fb-95c0-472d-ab17-a82da303b68f
title: Dvdnotify (Segment. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b31a2974bec428cb8ffe290edc9a384445e42070
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371600"
---
# <a name="dvdnotify"></a>Dvdnotify

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Das `DVDNotify` Ereignis benachrichtigt eine Anwendung über viele verschiedene DVD-Ereignisse und Disk-Anweisungen.

``` syntax
DVDNotify(EventCode, Param1, Param2)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="EventCode"></span><span id="eventcode"></span><span id="EVENTCODE"></span>*EventCode*
</dt> <dd>

Gibt den DVD-Ereignis Benachrichtigungs Code an.

</dd> <dt>

<span id="Param1"></span><span id="param1"></span><span id="PARAM1"></span>*Param1*
</dt> <dd>

Kann zusätzliche Informationen enthalten, die sich auf das Ereignis beziehen.

</dd> <dt>

<span id="Param2"></span><span id="param2"></span><span id="PARAM2"></span>*Param2*
</dt> <dd>

Kann zusätzliche Informationen enthalten, die sich auf das Ereignis beziehen.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Mit [DVD-Ereignis Benachrichtigungs Codes](dvd-notification-codes.md) erhalten Sie eine vollständige Erläuterung aller DVD-Ereignis Benachrichtigungs Codes und ihrer Parameter.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|--------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Segment. h</dt> </dl> |



 

 




