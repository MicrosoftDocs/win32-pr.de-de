---
title: Mehrdimensionale Arrays
description: Array Attribute können auch mit mehrdimensionalen Arrays verwendet werden.
ms.assetid: a01b904c-fbe8-4af4-8393-6864f7ef7364
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6eb7bcf94d97e1f35fdd6ab432ea5869e47f79ed
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948959"
---
# <a name="multidimensional-arrays"></a>Mehrdimensionale Arrays

Array Attribute können auch mit mehrdimensionalen Arrays verwendet werden. Achten Sie jedoch darauf, sicherzustellen, dass jede Dimension des Arrays über ein entsprechendes-Attribut verfügt. Beispiel:

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(2.0)
]
interface multiarray
{
  void arr2d( [in] short        d1size,
              [in] short        d2len,
              [in, size_is( d1size, ), length_is ( , d2len) ] long array2d[*][30] ) ;
}
```

Das vorangehende Array ist ein konformes Array (der Größe d1size) von 30 Element Arrays (mit d2len-Elementen, die für jedes Element ausgeliefert werden). Das Komma in den Klammern des \[ [**size \_ is**](/windows/desktop/Midl/size-is) - \] Attributs gibt an, dass der Wert in d1size auf die erste Dimension des Arrays angewendet wird. Entsprechend gibt der-Befehl in den Klammern der \[ [**Länge \_**](/windows/desktop/Midl/length-is) \] Attribute an, dass der Wert in d2len auf die zweite Dimension des Arrays angewendet wird.

Der Compiler für die Mittel l 2,0 stellt zwei Methoden zum Mars Hallen von Parametern bereit: gemischter Modus (/**OS**) und vollständig interpretiert (/**OIF** oder/**Oicf**). Standardmäßig kompiliert der Mittell-Compiler Schnittstellen im gemischten Modus. Sie müssen nicht explizit den [**/OS**](/windows/desktop/Midl/-os) -Schalter angeben, um das Marshalling im gemischten Modus zu erhalten.

Die vollständig interpretierte Methode Marshalls Daten vollständig offline. Dadurch wird die Größe des stubcodes beträchtlich reduziert, dies führt jedoch auch zu einer geringeren Leistung. Beim Marshalling im gemischten Modus marshallt die stubweise einige Parameter online. Dies führt zwar zu einer größeren stubgröße, bietet aber auch eine höhere Leistung.

> [!Caution]  
> Bei der Kompilierung von IDL-Dateien in diesem Modus ist Vorsicht geboten. Die Verwendung von mehrdimensionalen Arrays im gemischten Modus kann zu Parametern führen, die nicht ordnungsgemäß gemarshallt werden. Der [**/Oicf**](/windows/desktop/Midl/-oi) -Befehls Zeilenschalter wird empfohlen, wenn Ihre Schnittstelle Parameter definiert, die mehrdimensionale Arrays sind.

 

Das \[ [**String**](/windows/desktop/Midl/string) - \] Attribut kann auch mit mehrdimensionalen Arrays verwendet werden. Das-Attribut gilt für die am wenigsten bedeutende Dimension, z. b. ein konformes Array von Zeichen folgen. Sie können auch mehrdimensionale Zeiger Attribute verwenden. Beispiel:

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(2.0)
]
interface multiarray
{
  void arr2d([in] short  d1len,
             [in] short  d2len,
             [in] size_is(d1len, d2len) ] long  ** ptr2d) ;
}
```

Im vorherigen Beispiel ist die Variable ptr2d ein Zeiger auf einen d1len-Zeiger, der jeweils auf d2len-Zeiger auf **Long** zeigt.

Mehrdimensionale Arrays entsprechen nicht den Arrays von Zeigern. Bei einem mehrdimensionalen Array handelt es sich um einen einzelnen großen Block von Daten im Arbeitsspeicher. Ein Array von Zeigern enthält nur einen Zeiger Block im Array. Die Daten, auf die die Zeiger zeigen, können sich an einer beliebigen Stelle im Speicher befinden. Außerdem ermöglicht die ANSI C-Syntax, dass nur die signifikanteste (äußteste) Array Dimension in einem mehrdimensionalen Array nicht angegeben wird. Daher ist Folgendes eine gültige-Anweisung:

`long a1[] [20]`

Vergleichen Sie dies mit der folgenden ungültigen Anweisung:

`long a1[20] []`

 

 