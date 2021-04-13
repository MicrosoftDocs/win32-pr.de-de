---
description: Einige Anwendungen stellen Funktionen bereit, die im Client Bereich gezeichnete Objekte widerspiegeln (oder Spiegeln).
ms.assetid: 2205dc3c-ca4b-4a0a-be3e-0332ce8467a0
title: Spiegelung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d8e327af098a4e232e2a6734b37a17a1ac85f19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978353"
---
# <a name="reflection"></a>Spiegelung

Einige Anwendungen stellen Funktionen bereit, die im Client Bereich gezeichnete Objekte widerspiegeln (oder Spiegeln). Anwendungen, die Reflektionsfunktionen enthalten, verwenden die [**setworldtransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) -Funktion, um die entsprechenden Werte in der Welt Raum Transformation auf die Seiten Raum Transformation festzulegen. Diese Funktion empfängt einen Zeiger auf eine [**XForm**](/windows/win32/api/wingdi/ns-wingdi-xform) -Struktur, die die entsprechenden Werte enthält. Die eM11-und eM22-Member von XForm geben die horizontalen bzw. vertikalen reflektionskomponenten an.

Die *reflektionstransformation* erstellt ein Spiegelbild eines Objekts in Bezug auf die x-oder y-Achse. Kurz gesagt, die Reflektion ist nur eine negative Skalierung. Um eine horizontale Reflektion zu schaffen, werden x-Koordinaten mit 1 multipliziert. Um eine vertikale Reflektion zu schaffen, werden y-Koordinaten mit 1 multipliziert.

Die horizontale Reflektion kann durch den folgenden Algorithmus dargestellt werden:

``` syntax
x' = -x 
```

Dabei ist x die x-Koordinate, und x ' ist das Ergebnis der Reflektion.

Die 2 x 2-Matrix, die die horizontale Reflektion erzeugt hat, enthält die folgenden Werte:

``` syntax
|-1    0| 
|0     1| 
```

Die vertikale Reflektion kann durch den folgenden Algorithmus dargestellt werden:

``` syntax
y' = -y 
```

Dabei ist y die y-Koordinate, und y ' ist das Ergebnis der Reflektion.

Die 2 x 2-Matrix, die die vertikale Reflektion erzeugt hat, enthält die folgenden Werte:

``` syntax
|1    0| 
|0   -1| 
```

Die Vorgänge für die horizontale Reflektion und die vertikale Reflektion können mithilfe der folgenden 2-bis-2-Matrix in einem einzelnen Vorgang kombiniert werden:

``` syntax
|-1    0| 
|0    -1| 
```

 

 



