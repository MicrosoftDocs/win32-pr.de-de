---
description: Die PlayAtTimeInTitle-Methode startet die Wiedergabe zum angegebenen Zeitpunkt innerhalb des angegebenen Titels.
ms.assetid: 82726885-8393-409b-b8a1-29a8e9e9ac65
title: PlayAtTimeInTitle-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a33640733f7333395a4affc4dedc0ae8db3e3558bf066584cb603dfc5f906f73
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119291269"
---
# <a name="playattimeintitle-method"></a>PlayAtTimeInTitle-Methode

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die `PlayAtTimeInTitle` -Methode startet die Wiedergabe zum angegebenen Zeitpunkt innerhalb des angegebenen Titels.

``` syntax
MSWebDVD.PlayAtTimeInTitle(sTime, iTitle)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="sTime"></span><span id="stime"></span><span id="STIME"></span>*sTime*
</dt> <dd>

Gibt den Zeitpunkt an, zu dem die Wiedergabe als Zeichenfolge gestartet werden soll. Die Zeichenfolge muss das Format "hh:mm:ss:ff" aufweisen (mit Angabe von Stunden, Minuten, Sekunden, Frames).

</dd> <dt>

<span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*
</dt> <dd>

Gibt den Index des Titels als ganze Zahl an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CurrentTitle**](currenttitle-property.md)
</dt> <dt>

[**PlayAtTime**](playattime-method.md)
</dt> <dt>

[**TitlesAvailable**](titlesavailable-property.md)
</dt> </dl>

 

 



