---
description: ICE95 überprüft die Tabelle "Control" und "BBControl", um sicherzustellen, dass die Kontrollelemente in alle Würfe passen.
ms.assetid: 8ba73536-65a5-4658-846c-76356f16b81c
title: ICE95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8f0f7d44554385c33648036f314406971193afc079b5aa8e72cf595695797ef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119315260"
---
# <a name="ice95"></a>ICE95

ICE95 überprüft die [Tabelle "Control"](control-table.md) und ["BBControl",](bbcontrol-table.md) um sicherzustellen, dass die Kontrollelemente in alle Würfe passen.

## <a name="result"></a>Ergebnis

Wenn einer der folgenden Punkte zutrifft, passt ein Steuerelement nicht auf einen Automat. ICE95 gibt die folgenden Warnungen aus.



| ICE95-Warnung                                                                                                                                                                                                              | BESCHREIBUNG                                                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| Das BBControl-Element ' \[ 1 \] . \[ 2 \] ' in der BBControl-Tabelle passt nicht in alle Steuerelementsteuerelemente in der Control-Tabelle. Die X-Koordinate überschreitet die Grenze der Minimalbreite des Steuerelements %s.                   | Die X-Koordinate des Steuerelements liegt außerhalb der Breite des Gerüsts.                          |
| Das BBControl-Element ' \[ 1 \] . \[ 2 \] ' in der BBControl-Tabelle passt nicht in alle Steuerelementsteuerelemente in der Control-Tabelle. Die Y-Koordinate überschreitet die Grenze der minimalen Höhe der Steuerelementgröße %s.                  | Die Y-Koordinate des Steuerelements befindet sich unterhalb des unteren Rands des Strichs.                           |
| Das BBControl-Element ' \[ 1 \] . \[ 2 \] ' in der BBControl-Tabelle passt nicht in alle Steuerelementsteuerelemente in der Control-Tabelle. Die X-Koordinate und die Breite zusammen überschreiten die minimale Breite des Steuerelements %s.   | Die X-Koordinate des Steuerelements plus die Breite des Steuerelements liegt außerhalb der Breite des Steuerelements. |
| Das BBControl-Element ' \[ 1 \] . \[ 2 \] ' in der BBControl-Tabelle passt nicht in alle Steuerelementsteuerelemente in der Control-Tabelle. Die Y-Koordinate und die Höhe zusammen überschreiten die minimale Steuerhöhe %s. | Die Y-Koordinate des Steuerelements plus die Höhe des Steuerelements befindet sich unterhalb des unteren Rands des Strichs. |



 

## <a name="example"></a>Beispiel

ICE95 meldet die folgenden Warnungen für das Beispiel:

``` syntax
The BBControl item 'billboard1.bbcontrol1' in the BBControl table does not fit in all the billboard controls in the Control table. The X coordinate exceeds the boundary of the minimum billboard control width 100
The BBControl item 'billboard1.bbcontrol2' in the BBControl table does not fit in all the billboard controls in the Control table. The Y coordinate exceeds the boundary of the minimum billboard control height 100
The BBControl item 'billboard1.bbcontrol3' in the BBControl table does not fit in all the billboard controls in the Control table. The X coordinate and the width combined together exceeds the minimum billboard control width 100
The BBControl item 'billboard1.bbcontrol4' in the BBControl table does not fit in all the billboard controls in the Control table. The Y coordinate and the height combined together exceeds the minimum billboard control height 100
```

Steuertabelle (teilweise) (teilweise)



| Control  | type      | Breite | Höhe |
|----------|-----------|-------|--------|
| control1 | Billboard | 300   | 100    |
| Control2 | Billboard | 100   | 300    |



 

[BBControl-Tabelle](bbcontrol-table.md)



| Billboard\_ | BBControl  | X   | J   | Breite | Höhe |
|-------------|------------|-----|-----|-------|--------|
| 1  | bbcontrol1 | 200 | 0   | 100   | 100    |
| 1  | bbcontrol2 | 0   | 200 | 100   | 100    |
| 1  | bbcontrol3 | 50  | 0   | 100   | 50     |
| 1  | bbcontrol4 | 0   | 50  | 50    | 100    |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ICE-Referenz](ice-reference.md)
</dt> </dl>

 

 



