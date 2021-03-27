---
description: Einige Anwendungen stellen Funktionen bereit, die die im Client Bereich gezeichneten Objekte Scheren.
ms.assetid: e5b82013-f6b9-460d-9f53-1b50dee2064f
title: Scherz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c641ee0275828a7552251b0f8901c1ea41280b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217047"
---
# <a name="shear"></a>Scherz

Einige Anwendungen stellen Funktionen bereit, die die im Client Bereich gezeichneten Objekte Scheren. Anwendungen, die die Scheren-Funktionen verwenden, verwenden die [**setworldtransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) -Funktion, um geeignete Werte in der Transformation für den Welt Raum auf den Seiten Raum festzulegen. Diese Funktion empfängt einen Zeiger auf eine [**XForm**](/windows/win32/api/wingdi/ns-wingdi-xform) -Struktur, die die entsprechenden Werte enthält. Die eM12-und eM21-Member von XForm geben die horizontalen bzw. vertikalen Proportionalitäts Konstanten an.

Es gibt zwei Komponenten der schof- *Transformation*. Der erste ändert die vertikalen Linien in einem-Objekt. die zweite ändert die horizontalen Linien. In der folgenden Abbildung wird ein Rechteck mit 20 x 20 Einheiten angezeigt, das beim Kopieren aus dem Welt Raum in den Seitenbereich horizontal geschliffen wurde.

![Darstellung eines Rechtecks im Raum der Welt und eines trapeziod im Seitenbereich](images/cstrn-13.png)

Eine horizontale Schraffurart kann durch den folgenden Algorithmus dargestellt werden:

``` syntax
x' = x + (Sx * y) 
```

Dabei ist x die ursprüngliche x-Koordinate, SX ist die proportionationskonstante, und x ' ist das Ergebnis der scherungs Transformation.

Eine vertikale Schere kann durch den folgenden Algorithmus dargestellt werden:

``` syntax
y' = y + (Sy * x) 
```

bei y handelt es sich um die ursprüngliche y-Koordinate, sy ist die proportionationskonstante, und y ' ist das Ergebnis der schof-Transformation.

Die Transformationen mit horizontaler und vertikaler Schraffurart können mithilfe einer 2-x-2-Matrix zu einem einzelnen Vorgang kombiniert werden.

``` syntax
|x' y'| == |x y| * |  1   Sx| 
                   | Sy    1| 
```

Die 2 x 2-Matrix, die die Schere erzeugt hat, enthält die folgenden Werte:

``` syntax
|1    1| 
|0    1| 
```

 

 



