---
description: Mit der Zoom-Methode wird die Videoanzeige ein-oder ausgehend vergrößert, wobei eine bestimmte Gruppe von Bildschirm Koordinaten zentriert ist.
ms.assetid: 050f1264-8fbe-4322-970c-184275d5b219
title: Zoom-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2625e6c4facf006a0d904e49068853720e20c29e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485638"
---
# <a name="zoom-method"></a>Zoom-Methode

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Mit der- `Zoom` Methode wird die Videoanzeige ein-oder ausgehend vergrößert, wobei eine bestimmte Gruppe von Bildschirm Koordinaten zentriert ist.

``` syntax
MSWebDVD.Zoom(iXPos, iYPos, iZoomRatio)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="iXPos"></span><span id="ixpos"></span><span id="IXPOS"></span>*IXPOS*
</dt> <dd>

Gibt die x-Koordinate in der Mitte des rechteckigen Zoombereichs als ganze Zahl an.

</dd> <dt>

<span id="iYPos"></span><span id="iypos"></span><span id="IYPOS"></span>*iypos*
</dt> <dd>

Gibt die y-Koordinate in der Mitte des Rechtecks an, das als ganze Zahl vergrößert werden soll.

</dd> <dt>

<span id="iZoomRatio"></span><span id="izoomratio"></span><span id="IZOOMRATIO"></span>*izoomratio*
</dt> <dd>

Gibt den Vergrößerungsfaktor an, der auf den aktuellen Zoomwert als ganze Zahl angewendet wird. Der maximale Gesamtwert hängt davon ab, was vom Hardware Overlay unterstützt werden kann. Dies ist normalerweise ein Faktor von 32 bis 64 der ursprünglichen Größe.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Das neue Zoomverhältnis bleibt in Kraft, bis es in der ursprünglichen Größe wieder hergestellt oder erneut geändert wird. Mit anderen Worten: zwei Aufrufe dieser Methode, die ein *izoomratio* von zwei angeben, führen zu einem Zoomverhältnis, das viermal größer als die ursprüngliche Videogröße ist. Wenn der Benutzer versucht, die von der Hardware unterstützten Hardware zu vergrößern, ist diese Methode zwar erfolgreich, aber es wird keine Aktion ausgeführt.

Die [**setclipvideorect**](setclipvideorect-method.md) -Methode ist eine weitere Möglichkeit zum vergrößern. der einzige Unterschied zwischen den beiden Methoden ist die Art und Weise, in der das Zoom Rechteck angegeben wird.

 

 



