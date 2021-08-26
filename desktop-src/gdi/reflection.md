---
description: Einige Anwendungen bieten Features, die im Clientbereich gezeichnete Objekte widerspiegeln (oder spiegeln).
ms.assetid: 2205dc3c-ca4b-4a0a-be3e-0332ce8467a0
title: Spiegelung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f03d872273e7d0b9f23d9ffb31c6304c8b59b59eda80c7181802120f89c0d764
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092700"
---
# <a name="reflection"></a>Spiegelung

Einige Anwendungen bieten Features, die im Clientbereich gezeichnete Objekte widerspiegeln (oder spiegeln). Anwendungen, die Reflektionsfunktionen enthalten, verwenden die [**SetWorldTransform-Funktion,**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) um die entsprechenden Werte im Weltraum auf die Transformation im Seitenbereich festzulegen. Diese Funktion empfängt einen Zeiger auf eine [**XFORM-Struktur,**](/windows/win32/api/wingdi/ns-wingdi-xform) die die entsprechenden Werte enthält. Die Elemente eM11 und eM22 von XFORM geben die horizontalen bzw. vertikalen Reflektionskomponenten an.

Die *Reflektionstransformation* erstellt ein Spiegelbild eines Objekts in Bezug auf die x- oder y-Achse. Kurz gesagt: Reflektion ist nur eine negative Skalierung. Um eine horizontale Reflektion zu erzeugen, werden x-Koordinaten mit 1 multipliziert. Um eine vertikale Reflektion zu erzeugen, werden y-Koordinaten mit 1 multipliziert.

Horizontale Reflektion kann durch den folgenden Algorithmus dargestellt werden:

``` syntax
x' = -x 
```

wobei x die x-Koordinate und x' das Ergebnis der Reflektion ist.

Die 2-by-2-Matrix, die horizontale Reflektion erzeugt hat, enthält die folgenden Werte:

``` syntax
|-1    0| 
|0     1| 
```

Die vertikale Reflektion kann durch den folgenden Algorithmus dargestellt werden:

``` syntax
y' = -y 
```

wobei y die y-Koordinate und y' das Ergebnis der Reflektion ist.

Die 2-by-2-Matrix, die vertikale Reflektion erzeugt hat, enthält die folgenden Werte:

``` syntax
|1    0| 
|0   -1| 
```

Die horizontalen und vertikalen Reflektionsvorgänge können mithilfe der folgenden 2-mal-2-Matrix zu einem einzelnen Vorgang kombiniert werden:

``` syntax
|-1    0| 
|0    -1| 
```

 

 



