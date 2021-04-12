---
description: Die playabwärts-Methode startet die Rückwärts Wiedergabe von der aktuellen Position mit der angegebenen Geschwindigkeit.
ms.assetid: 7f8421e7-f835-4a10-a9c9-0e43de159e4f
title: Playrückwärts-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90b396c3829569d3f3ad25f0c0e8718dfd23f268
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104480595"
---
# <a name="playbackwards-method"></a>Playrückwärts-Methode

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die- `PlayBackwards` Methode startet die Rückwärts Wiedergabe von der aktuellen Position mit der angegebenen Geschwindigkeit.

``` syntax
MSWebDVD.PlayBackwards(nSpeed)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="nSpeed"></span><span id="nspeed"></span><span id="NSPEED"></span>*ngeschwindigkeit*
</dt> <dd>

Gibt die Geschwindigkeit an, mit der als Zahl abgespielt werden soll. Diese Zahl ist ein Multiplikator – 1.0 ist eine normale Wiedergabegeschwindigkeit. 2,0 ist eine doppelte Geschwindigkeit, 0,5 ist halb Geschwindigkeit usw. Wenn "**nspeed**" nicht gleich 1,0 ist, wird das audiobild stumm geschaltet, und das Teilbild ist deaktiviert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Playforward**](playforwards-method.md)
</dt> </dl>

 

 



