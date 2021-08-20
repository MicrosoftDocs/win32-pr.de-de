---
title: Generieren einer Typbibliothek mit MIDL
description: Das Element der obersten Ebene der ODL-Syntax ist die Bibliotheks-Anweisung (Bibliotheksblock).
ms.assetid: e21a9e6e-4e10-4280-af8f-24534cb2ab90
keywords:
- Microsoft Interface Definition Language MIDL , Tasks, Generieren einer Typbibliothek
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8d9084631dc30eb1cff7f61f6f3f090f95bb92cff357b3902cb0959f2c4142f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013848"
---
# <a name="generating-a-type-library-with-midl"></a>Generieren einer Typbibliothek mit MIDL

Das Element der obersten Ebene der ODL-Syntax ist die Bibliotheks-Anweisung (Bibliotheksblock). Jede andere ODL-Anweisung, mit Ausnahme der Attribute, die auf die Bibliotheks-Anweisung angewendet werden, muss innerhalb des Bibliotheksblocks definiert werden. Wenn der MIDL-Compiler einen Bibliotheksblock sieht, generiert er eine Typbibliothek auf ähnliche Weise wie MkTypLib. Mit einigen Ausnahmen, die unter [Unterschiede zwischen MIDL und MKTYPLIB](differences-between-midl-and-mktyplib.md)beschrieben werden, sollten die Anweisungen im Bibliotheksblock der gleichen Syntax folgen wie in der ODL-Sprache und MkTypLib.

> [!Note]  
> Das Mktyplib.exe Tool ist veraltet. Verwenden Sie stattdessen den MIDL-Compiler.

 

Sie können ODL-Attribute auf Elemente anwenden, die innerhalb oder außerhalb des Bibliotheksblocks definiert sind. Diese Attribute haben außerhalb des Bibliotheksblocks keine Auswirkungen, es sei denn, auf das Element, auf das sie angewendet werden, wird innerhalb des Bibliotheksblocks verwiesen. Anweisungen innerhalb des Bibliotheksblocks können auf ein externes Element verweisen, indem sie es entweder als Basistyp verwenden, von ihm erben oder wie gezeigt in einer Zeile darauf verweisen:

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

Wenn innerhalb des Bibliotheksblocks auf ein außerhalb des Bibliotheksblocks definiertes Element verwiesen wird, wird seine Definition in die generierte Typbibliothek aufgenommen. Der MIDL-Compiler behandelt die Anweisungen außerhalb eines Bibliotheksblocks als typische IDL-Datei und analysiert diese Anweisungen wie immer. Normalerweise bedeutet dies das Generieren von C-Sprachstubs für eine RPC-Anwendung.

Weitere Informationen zur allgemeinen Syntax für eine ODL-Datei finden Sie unter [ODL-Dateisyntax.](/previous-versions/windows/desktop/automat/odl-file-syntax)

 

 