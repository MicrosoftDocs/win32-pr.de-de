---
title: Mehrdimensionale Arrays
description: Arrayattribute können auch mit mehrdimensionalen Arrays verwendet werden.
ms.assetid: a01b904c-fbe8-4af4-8393-6864f7ef7364
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52f7dac2b6d093fa56383ecaf976a83acf13fec9aa0c3820c1d608ccb69e9e9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118928081"
---
# <a name="multidimensional-arrays"></a>Mehrdimensionale Arrays

Arrayattribute können auch mit mehrdimensionalen Arrays verwendet werden. Achten Sie jedoch darauf, dass jede Dimension des Arrays über ein entsprechendes Attribut verfügt. Beispiel:

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

Das vorangehende Array ist ein konformes Array (der Größe d1size ) mit 30 Elementarrays (mit jeweils ausgelieferten d2len-Elementen). Das Komma in den Klammern der Größe ist attribut gibt an, dass der \[ [**\_**](/windows/desktop/Midl/size-is) Wert in d1size auf die erste Dimension des \] Arrays angewendet wird. Ebenso gibt der Befehl in den Klammern der Länge an, dass der Wert in d2len auf die zweite Dimension des \[ [**\_**](/windows/desktop/Midl/length-is) Arrays \] angewendet wird.

Der MIDL 2.0-Compiler bietet zwei Methoden zum Marshallen von Parametern: gemischter Modus (/**Os**) und vollständig interpretiert (/**Oif** oder /**Oicf**). Standardmäßig kompiliert der MIDL-Compiler Schnittstellen im gemischten Modus. Sie müssen den Schalter [**/Os**](/windows/desktop/Midl/-os) nicht explizit angeben, um Marshalling im gemischten Modus zu erhalten.

Die vollständig interpretierte Methode marshallt Daten vollständig offline. Dies reduziert die Größe des Stubcodes erheblich, führt aber auch zu einer verringerten Leistung. Beim Marshallen im gemischten Modus marshallen die Stubs einige Parameter online. Dies führt zwar zu einer größeren Stubgröße, bietet aber auch eine höhere Leistung.

> [!Caution]  
> Seien Sie vorsichtig, wenn Sie IDL-Dateien in diesem Modus kompilieren. Die Verwendung mehrdimensionaler Arrays im gemischten Modus kann zu Parametern führen, die nicht ordnungsgemäß gemarshallt werden. Der [**Befehlszeilenschalter /Oicf**](/windows/desktop/Midl/-oi) wird empfohlen, wenn die Schnittstelle Parameter definiert, die mehrdimensionale Arrays sind.

 

Das \[ [](/windows/desktop/Midl/string) \] Zeichenfolgenattribut kann auch mit mehrdimensionalen Arrays verwendet werden. Das -Attribut gilt für die Dimension mit der geringsten Bedeutung, z. B. ein konformes Array von Zeichenfolgen. Sie können auch mehrdimensionale Zeigerattribute verwenden. Beispiel:

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

Im vorherigen Beispiel ist die Variable ptr2d ein Zeiger auf einen Zeigerblock im Bereich d1len, der jeweils auf d2len-Zeiger auf **long** zeigt.

Mehrdimensionale Arrays entsprechen nicht Arrays von Zeigern. Ein mehrdimensionales Array ist ein einzelner, großer Datenblock im Arbeitsspeicher. Ein Array von Zeigern enthält nur einen Block von Zeigern im Array. Die Daten, auf die die Zeiger zeigen, können sich an einer beliebigen Stelle im Arbeitsspeicher finden. Außerdem lässt die ANSI C-Syntax zu, dass in einem mehrdimensionalen Array nur die signifikanteste Arraydimension (ganz links) nicht angegeben wird. Daher ist Folgendes eine gültige -Anweisung:

`long a1[] [20]`

Vergleichen Sie dies mit der folgenden ungültigen Anweisung:

`long a1[20] []`

 

 