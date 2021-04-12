---
description: ICE95 überprüft die Tabelle "Control Table" und die Tabelle "bbcontrol", um zu überprüfen, ob die Billboard-Steuerelemente auf alle
ms.assetid: 8ba73536-65a5-4658-846c-76356f16b81c
title: ICE95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14144c7739dfcc1f1b5e66d92d8e6c1c46ed49fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217649"
---
# <a name="ice95"></a>ICE95

ICE95 überprüft die Tabelle " [Control Table](control-table.md) " und die [Tabelle "bbcontrol](bbcontrol-table.md) ", um zu überprüfen, ob die Billboard-Steuerelemente auf alle

## <a name="result"></a>Ergebnis

Wenn einer der folgenden Punkte zutrifft, kann ein Billboard-Steuerelement nicht in ein Plakat eingefügt werden. ICE95 gibt die folgenden Warnungen aus.



| ICE95-Warnung                                                                                                                                                                                                              | BESCHREIBUNG                                                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| Das bbcontrol-Element ' \[ 1 \] . \[ 2 \] ' in der Tabelle ' bbcontrol ' ist nicht in alle Billboard-Steuerelemente in der Steuerelement Tabelle passt. Die X-Koordinate überschreitet die Grenze der Mindestbreite des Billboard-Steuer Elements% s.                   | Die X-Koordinate des Steuer Elements liegt außerhalb der Breite des Billboard.                          |
| Das bbcontrol-Element ' \[ 1 \] . \[ 2 \] ' in der Tabelle ' bbcontrol ' ist nicht in alle Billboard-Steuerelemente in der Steuerelement Tabelle passt. Die Y-Koordinate überschreitet die Grenze der minimalen Größe des Billboard-Steuer Elements% s.                  | Die Y-Koordinate des Steuer Elements befindet sich unter dem unteren Rand des Billboard.                           |
| Das bbcontrol-Element ' \[ 1 \] . \[ 2 \] ' in der Tabelle ' bbcontrol ' ist nicht in alle Billboard-Steuerelemente in der Steuerelement Tabelle passt. Die X-Koordinate und die zusammen kombinierte Breite überschreiten die Mindestbreite des Billboard-Steuer Elements% s.   | Die X-Koordinate des Steuer Elements und die Breite des Steuer Elements liegen außerhalb der Breite des Billboard. |
| Das bbcontrol-Element ' \[ 1 \] . \[ 2 \] ' in der Tabelle ' bbcontrol ' ist nicht in alle Billboard-Steuerelemente in der Steuerelement Tabelle passt. Die Y-Koordinate und die kombinierte Höhe überschreiten die minimale Größe des Billboard-Steuer Elements% s. | Die Y-Koordinate des Steuer Elements und die Höhe des Steuer Elements liegen unter dem unteren Rand des Billboard. |



 

## <a name="example"></a>Beispiel

ICE95 meldet die folgenden Warnungen für das Beispiel:

``` syntax
The BBControl item 'billboard1.bbcontrol1' in the BBControl table does not fit in all the billboard controls in the Control table. The X coordinate exceeds the boundary of the minimum billboard control width 100
The BBControl item 'billboard1.bbcontrol2' in the BBControl table does not fit in all the billboard controls in the Control table. The Y coordinate exceeds the boundary of the minimum billboard control height 100
The BBControl item 'billboard1.bbcontrol3' in the BBControl table does not fit in all the billboard controls in the Control table. The X coordinate and the width combined together exceeds the minimum billboard control width 100
The BBControl item 'billboard1.bbcontrol4' in the BBControl table does not fit in all the billboard controls in the Control table. The Y coordinate and the height combined together exceeds the minimum billboard control height 100
```

Control-Tabelle (partiell) (partiell)



| Control  | type      | Breite | Höhe |
|----------|-----------|-------|--------|
| control1 | Billboard | 300   | 100    |
| Control2 | Billboard | 100   | 300    |



 

[Bbcontrol-Tabelle](bbcontrol-table.md)



| Billboard\_ | Bbcontrol  | X   | J   | Breite | Höhe |
|-------------|------------|-----|-----|-------|--------|
| billboard1  | bbcontrol1 | 200 | 0   | 100   | 100    |
| billboard1  | bbcontrol2 | 0   | 200 | 100   | 100    |
| billboard1  | bbcontrol3 | 50  | 0   | 100   | 50     |
| billboard1  | bbcontrol4 | 0   | 50  | 50    | 100    |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ice-Referenz](ice-reference.md)
</dt> </dl>

 

 



