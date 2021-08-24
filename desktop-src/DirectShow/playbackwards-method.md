---
description: Die PlayBackwards-Methode startet die Rückwärtswiedergabe von der aktuellen Position mit der angegebenen Geschwindigkeit.
ms.assetid: 7f8421e7-f835-4a10-a9c9-0e43de159e4f
title: PlayBackwards-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7236c225858d9508da0074ea64d104a50632b772302f42362dae373a987c352
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748360"
---
# <a name="playbackwards-method"></a>PlayBackwards-Methode

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die `PlayBackwards` Methode startet die Rückwärtswiedergabe von der aktuellen Position mit der angegebenen Geschwindigkeit.

``` syntax
MSWebDVD.PlayBackwards(nSpeed)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="nSpeed"></span><span id="nspeed"></span><span id="NSPEED"></span>*nSpeed*
</dt> <dd>

Gibt die Geschwindigkeit an, mit der als Zahl wiedergegeben werden soll. Diese Zahl ist ein Multiplikator– 1,0 ist die normale Wiedergabegeschwindigkeit. 2,0 ist die doppelte Geschwindigkeit, 0,5 ist halb schnell usw. Wenn **nSpeed** ungleich 1,0 ist, wird die Audiodatei stummgeschaltet, und die Bildunterdrückung wird deaktiviert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**PlayForwards**](playforwards-method.md)
</dt> </dl>

 

 



