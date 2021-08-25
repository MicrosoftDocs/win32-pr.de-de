---
description: Die PlayForwards-Methode startet die Wiedergabe von der aktuellen Position mit der angegebenen Geschwindigkeit.
ms.assetid: 4f1a3e74-b343-413d-8df7-6c4bea39c62d
title: PlayForwards-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81e607779147ba057b9cfd747ebfe827a25e294e2b04cdfa7e61a0691ecf293c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119830630"
---
# <a name="playforwards-method"></a>PlayForwards-Methode

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die `PlayForwards` -Methode startet die Wiedergabe von der aktuellen Position mit der angegebenen Geschwindigkeit.

``` syntax
MSWebDVD.PlayForwards(nSpeed)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="nSpeed"></span><span id="nspeed"></span><span id="NSPEED"></span>*nSpeed*
</dt> <dd>

Gibt die Geschwindigkeit an, mit der als Ganzzahlwert wiedergegeben werden soll. Dieser Wert ist ein Multiplikator– 1,0 ist die normale Wiedergabegeschwindigkeit. 2,0 ist die doppelte Geschwindigkeit, 0,5 ist halb schnell usw. Wenn **nSpeed** ungleich 1,0 ist, wird die Audiodatei stummgeschaltet, und die Bildunterdrückung wird deaktiviert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**PlayBackwards**](playbackwards-method.md)
</dt> </dl>

 

 



