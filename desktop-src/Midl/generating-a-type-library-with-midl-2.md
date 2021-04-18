---
title: Erstellen einer Typbibliothek mit "Mittel l"
description: Das Element der obersten Ebene der ODL-Syntax ist die Library-Anweisung (Library-Block).
ms.assetid: e21a9e6e-4e10-4280-af8f-24534cb2ab90
keywords:
- Microsoft Interface Definition Language mittlerer l, Aufgaben, Erstellen einer Typbibliothek
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85f6e8f7ea6f65bc503c08872c9199ff3d5fd828
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106341519"
---
# <a name="generating-a-type-library-with-midl"></a>Erstellen einer Typbibliothek mit "Mittel l"

Das Element der obersten Ebene der ODL-Syntax ist die Library-Anweisung (Library-Block). Jede andere ODL-Anweisung, mit Ausnahme der Attribute, die auf die Library-Anweisung angewendet werden, muss innerhalb des Bibliotheks Blocks definiert werden. Wenn der mittlerer l-Compiler einen Bibliotheks Block sieht, generiert er eine Typbibliothek ähnlich wie MkTypLib. Mit einigen Ausnahmen, die [unter Unterschiede zwischen mittlerer l und MkTypLib](differences-between-midl-and-mktyplib.md)beschrieben werden, sollten die Anweisungen innerhalb des Bibliotheks Blocks dieselbe Syntax wie in der ODL-Sprache und MkTypLib befolgen.

> [!Note]  
> Das Mktyplib.exe Tool ist veraltet. Verwenden Sie stattdessen den Mittel l-Compiler.

 

Sie können odl-Attribute auf Elemente anwenden, die entweder innerhalb oder außerhalb des Bibliotheks Blocks definiert sind. Diese Attribute haben keine Auswirkung außerhalb des Bibliotheks Blocks, es sei denn, auf das Element, auf das Sie angewendet werden, wird im Bibliotheks Block verwiesen. Anweisungen innerhalb des Bibliotheks Blocks können auf ein außen Element verweisen, indem es entweder als Basistyp verwendet wird, von ihm geerbt wird, oder indem in einer Zeile wie gezeigt auf das Element verwiesen wird:

``` syntax
<some IDL definitions including definitions for interface IFace and struct bar>
[<some attributes>]
library a
{
    interface IFace;
    struct this_struct;
...
};
```

Wenn innerhalb des Bibliotheks Blocks auf ein Element verwiesen wird, das außerhalb des Bibliotheks Blocks definiert ist, wird seine Definition in die generierte Typbibliothek eingefügt. Der mittlerer l-Compiler behandelt die Anweisungen außerhalb eines Bibliotheks Blocks als eine typische IDL-Datei und analysiert diese Anweisungen, wie Sie dies immer getan haben. Normalerweise bedeutet dies, dass C-sprach-Stub für eine RPC-Anwendung erzeugt werden.

Weitere Informationen zur allgemeinen Syntax für eine ODL-Datei finden Sie unter [Syntax der ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-syntax).

 

 