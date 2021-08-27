---
description: Einige Anwendungen stellen Features zur Verfügung, mit denen Objekte im Clientbereich gezeichnet werden.
ms.assetid: e5b82013-f6b9-460d-9f53-1b50dee2064f
title: Scheren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32edb9484fd8bb2a9da15220b0acf39fd5c44c50091551205022c6458b50d4e2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092630"
---
# <a name="shear"></a>Scheren

Einige Anwendungen stellen Features zur Verfügung, mit denen Objekte im Clientbereich gezeichnet werden. Anwendungen, die Shearfunktionen verwenden, verwenden die [**SetWorldTransform-Funktion,**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) um die entsprechenden Werte im Weltraum auf seitenbasierte Transformationen zu setzen. Diese Funktion empfängt einen Zeiger auf eine [**XFORM-Struktur,**](/windows/win32/api/wingdi/ns-wingdi-xform) die die entsprechenden Werte enthält. Die Elemente eM12 und eM21 von XFORM geben die horizontalen bzw. vertikalen Ziehkonstten an.

Es gibt zwei Komponenten der *Sheartransformation.* Die erste ändert die vertikalen Linien in einem -Objekt. Die zweite ändert die horizontalen Linien. Die folgende Abbildung zeigt ein Rechteck mit 20 by 20 Einheiten, das horizontal umgestrichen wird, wenn es aus dem Raum in den Seitenbereich kopiert wird.

![Abbildung, die ein Rechteck im Weltraum und ein Trape im Seitenbereich zeigt](images/cstrn-13.png)

Ein horizontales Shear kann durch den folgenden Algorithmus dargestellt werden:

``` syntax
x' = x + (Sx * y) 
```

Wobei x die ursprüngliche x-Koordinate, Sx die schwebige Konstante und x' das Ergebnis der Sheartransformation ist.

Ein vertikales Shear kann durch den folgenden Algorithmus dargestellt werden:

``` syntax
y' = y + (Sy * x) 
```

Wobei y die ursprüngliche y-Koordinate, Sy die y-Konstante und y' das Ergebnis der Bruchtransformation ist.

Die Horizontal-Shear- und Vertical-Shear-Transformationen können mithilfe einer 2-by-2-Matrix zu einem einzelnen Vorgang kombiniert werden.

``` syntax
|x' y'| == |x y| * |  1   Sx| 
                   | Sy    1| 
```

Die 2 by 2-Matrix, die den Strich erzeugt hat, enthält die folgenden Werte:

``` syntax
|1    1| 
|0    1| 
```

 

 



