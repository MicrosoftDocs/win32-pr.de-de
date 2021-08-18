---
description: Die Zoom-Methode zoomt die Videoanzeige ein- oder heraus, zentriert auf einem bestimmten Satz von Bildschirmkoordinaten.
ms.assetid: 050f1264-8fbe-4322-970c-184275d5b219
title: Zoommethode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb0c260e5a5404b65f4e0d0595a87ee78103c5acccedd32abf50fc5706c6b42f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119632699"
---
# <a name="zoom-method"></a>Zoommethode

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die `Zoom` -Methode zoomt die Videoanzeige ein- oder heraus, zentriert auf einem bestimmten Satz von Bildschirmkoordinaten.

``` syntax
MSWebDVD.Zoom(iXPos, iYPos, iZoomRatio)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="iXPos"></span><span id="ixpos"></span><span id="IXPOS"></span>*iXPos*
</dt> <dd>

Gibt die x-Koordinate in der Mitte des rechteckigen Zoombereichs als ganze Zahl an.

</dd> <dt>

<span id="iYPos"></span><span id="iypos"></span><span id="IYPOS"></span>*iYPos*
</dt> <dd>

Gibt die y-Koordinate in der Mitte des Rechtecks an, das als ganze Zahl vergrößert werden soll.

</dd> <dt>

<span id="iZoomRatio"></span><span id="izoomratio"></span><span id="IZOOMRATIO"></span>*iZoomRatio*
</dt> <dd>

Gibt den Vergrößerungsfaktor an, der auf den aktuellen Zoomwert als ganze Zahl angewendet wird. Der maximale Gesamtwert hängt davon ab, was die Hardwareüberlagerung unterstützen kann. Dies ist in der Regel ein Faktor von dem 32- bis 64-fachen der ursprünglichen Größe.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

Das neue Zoomverhältnis bleibt wirksam, bis es auf die ursprüngliche Größe wiederhergestellt oder erneut geändert wird. Anders ausgedrückt: Zwei Aufrufe dieser Methode, die ein *iZoomRatio* von zwei angeben, führen zu einem Zoomverhältnis, das viermal größer als die ursprüngliche Videogröße ist. Wenn der Benutzer versucht, zu vergrößern, was die Hardware unterstützen kann, ist diese Methode zwar erfolgreich, führt aber nichts aus.

Die [**SetClipVideoRect-Methode**](setclipvideorect-method.md) ist eine weitere Möglichkeit zum Vergrößern. Der einzige Unterschied zwischen den beiden Methoden besteht darin, wie das Zoomrechteck angegeben wird.

 

 



