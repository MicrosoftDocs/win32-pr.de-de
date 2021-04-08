---
title: Die animationnames-Auflistung
description: Die animationnames-Auflistung
ms.assetid: 3b06e497-1d03-43be-8d33-e69ef2972237
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c9e0c2c1d42f51f9d50bafaee61b6ab51d5b85f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856168"
---
# <a name="the-animationnames-collection"></a>Die animationnames-Auflistung

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

Die [**animationnames**](https://www.bing.com/search?q=**AnimationNames**) -Auflistung ist eine spezielle Sammlung, die die Liste der für ein Zeichen kompilierten Animations Namen enthält. Sie können die Auflistung verwenden, um die Namen der Animationen für ein Zeichen aufzulisten. Beispielsweise können Sie in Visual Basic oder VBScript (2,0 oder höher) auf diese Namen mithilfe der **for each-... Nächste** Anweisungen:


```
   For Each Animation in Genie.AnimationNames
      Genie.Play Animation
   Next
```



Elemente in der Auflistung haben keine Eigenschaften, sodass auf einzelne Elemente nicht direkt zugegriffen werden kann.

Damit. ACF-Zeichen: die Auflistung gibt alle Animationen zurück, die für das Zeichen definiert wurden, nicht nur diejenigen, die mit der [**Get**](get-method.md) -Methode abgerufen wurden.

 

 




