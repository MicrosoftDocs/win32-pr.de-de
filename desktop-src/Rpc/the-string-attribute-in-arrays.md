---
title: Das Zeichenfolgenattribut in Arrays
description: Sie können das Attribut \string\ für eindimensionale Zeichenarrays, Breitzeichenarrays und Bytearrays verwenden, die Textzeichenfolgen darstellen.
ms.assetid: 96cebb84-6123-4bf8-b70b-a4f6d48cce52
keywords:
- Zeichenfolge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9d56099c9cc2be3638642b20f6d3572786ea0a93f47f8660c2e847c4c06dd3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120016660"
---
# <a name="the-string-attribute-in-arrays"></a>Das \[ \] Zeichenfolgenattribut in Arrays

Sie können das \[ [Zeichenfolgenattribut](/windows/desktop/Midl/string) für \] eindimensionale Zeichenarrays, Breitzeichenarrays und Bytearrays verwenden, die Textzeichenfolgen darstellen. Wenn Sie das **\[ Zeichenfolgenattribut \]** verwenden, verwendet der Clientstub die C-Bibliotheksfunktionen **strlen** oder **wstrlen,** um die Anzahl der Zeichen in der Zeichenfolge zu zählen. Um mögliche Inkonsistenzen zu vermeiden, lässt MIDL **\[ \]** nicht zu, dass Sie das Zeichenfolgenattribut zur gleichen Zeit wie das erste verwenden, das letzte ist , und die Größe \[ [ \_](/windows/desktop/Midl/first-is)ist \] \[ [ \_](/windows/desktop/Midl/last-is) \] \[ [ \_](/windows/desktop/Midl/size-is) \] Attribute.

Bei auf NULL endende Zeichenfolgen in C müssen Sie Platz für das NULL-Zeichen am Ende der Zeichenfolge zulassen. Wenn Sie beispielsweise eine Zeichenfolge deklarieren, die bis zu 80 Zeichen enthält, weisen Sie 81 Zeichen zu. Die folgende IDL-Beispieldatei veranschaulicht, wie Arrays mit dem **\[ Zeichenfolgenattribut \] deklariert** werden.

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(8.0)
]
interface arraytest
{
  void fArray8([in, out, string] char achArray[]);
}
```

 

 