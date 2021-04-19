---
description: Die DVDTimeCode2bstr-Methode ruft eine Zeichenfolge ab, die die aktuelle Uhrzeit auf dem Laufwerk angibt.
ms.assetid: 0a477274-ac56-4f46-8461-53411362b33e
title: DVDTimeCode2bstr-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 042c6889fd2d5ee76aa42fc4e92f1c2754a5c95d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106346601"
---
# <a name="dvdtimecode2bstr-method"></a>DVDTimeCode2bstr-Methode

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die- `DVDTimeCode2bstr` Methode ruft eine Zeichenfolge ab, die die aktuelle Uhrzeit auf dem Laufwerk angibt.

``` syntax
[ sTimeCode = ] MSWebDVD.DVDTimeCode2bstr(nTimeCode)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="sTimeCode"></span><span id="stimecode"></span><span id="STIMECODE"></span>*stimecode*
</dt> <dd>

Gibt die aktuelle Uhrzeit auf der Festplatte relativ zum Anfang des Titels als Zahl an, die über das [**\_ \_ aktuelle \_ hmsf- \_ Zeit**](ec-dvd-current-hmsf-time.md) Ereignis der EC-DVD abgerufen wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt eine Zeichenfolge mit 11 Zeichen im Format "hh: mm: SS: FF" zurück, die die Stunden, Minuten, Sekunden und Frames darstellt, die die aktuelle Uhrzeit definieren.

## <a name="remarks"></a>Bemerkungen

Diese Methode ist schreibgeschützt.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Behandeln von DVD-Ereignis Benachrichtigungen](handling-dvd-event-notifications.md)
</dt> </dl>

 

 



