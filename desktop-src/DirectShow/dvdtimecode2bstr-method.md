---
description: Die DVDTimeCode2bstr-Methode ruft eine Zeichenfolge ab, die die aktuelle Zeit auf dem Datenträger angibt.
ms.assetid: 0a477274-ac56-4f46-8461-53411362b33e
title: DVDTimeCode2bstr-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90bda68bafa462af5d425c62368b51f8b4b08ce2dfc310276e8f26b7c4601fa1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119148603"
---
# <a name="dvdtimecode2bstr-method"></a>DVDTimeCode2bstr-Methode

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die `DVDTimeCode2bstr` -Methode ruft eine Zeichenfolge ab, die die aktuelle Zeit auf dem Datenträger angibt.

``` syntax
[ sTimeCode = ] MSWebDVD.DVDTimeCode2bstr(nTimeCode)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="sTimeCode"></span><span id="stimecode"></span><span id="STIMECODE"></span>*sTimeCode*
</dt> <dd>

Gibt die aktuelle Zeit auf dem Datenträger relativ zum Anfang des Titels als Zahl an, die über das [**EC \_ DVD CURRENT \_ \_ HMSF \_ TIME-Ereignis**](ec-dvd-current-hmsf-time.md) abgerufen wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt eine Zeichenfolge mit 11 Zeichen im Format "hh:mm:ss:ff" zurück, die die Stunden, Minuten, Sekunden und Frames darstellt, die die aktuelle Zeit definieren.

## <a name="remarks"></a>Hinweise

Diese Methode ist schreibgeschützter.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Behandeln von DVD-Ereignisbenachrichtigungen](handling-dvd-event-notifications.md)
</dt> </dl>

 

 



