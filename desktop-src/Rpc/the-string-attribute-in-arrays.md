---
title: Das Zeichen folgen Attribut in Arrays
description: Sie können das Attribut \ String \ für eindimensionale Zeichen Arrays, breit Zeichen Arrays und Byte Arrays verwenden, die Text Zeichenfolgen darstellen.
ms.assetid: 96cebb84-6123-4bf8-b70b-a4f6d48cce52
keywords:
- Zeichenfolge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e8bd2f7234b2713b6a7df05cfb5d6ae4c08b2d8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102003"
---
# <a name="the-string-attribute-in-arrays"></a>Das \[ Zeichen folgen \] Attribut in Arrays

Sie können das \[ [String](/windows/desktop/Midl/string) - \] Attribut für eindimensionale Zeichen Arrays, breit Zeichen Arrays und Byte Arrays verwenden, die Text Zeichenfolgen darstellen. Wenn Sie das **\[ \] Zeichen** folgen Attribut verwenden, verwendet der Clientstub die C-Bibliotheksfunktionen von " **straulen** " oder " **wstrinlen** ", um die Anzahl der Zeichen in der Zeichenfolge zu zählen. Um mögliche Inkonsistenzen zu vermeiden, können Sie das **\[ Zeichen \]** folgen Attribut nicht zur gleichen Zeit wie die \[ [erste \_ is](/windows/desktop/Midl/first-is) \] -, \[ [Last \_](/windows/desktop/Midl/last-is) \] -und \[ [size \_](/windows/desktop/Midl/size-is) - \] Attribute verwenden.

Bei null-terminierten Zeichen folgen in C müssen Sie Leerzeichen für das NULL Zeichen am Ende der Zeichenfolge zulassen. Wenn Sie z. b. eine Zeichenfolge mit bis zu 80 Zeichen deklarieren, müssen Sie 81 Zeichen zuordnen. Die folgende Beispiel-IDL-Datei veranschaulicht das Deklarieren von Arrays mit dem **\[ Zeichen \]** folgen Attribut.

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

 

 