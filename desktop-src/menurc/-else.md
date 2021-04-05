---
title: " else"
description: Die Direktive "\ Else" markiert eine optionale Klausel eines Blocks für die bedingte Kompilierung, der durch eine \ ifdef-, \ ifndef-oder \ if-Direktive definiert wird. Die \ Else-Direktive muss die letzte Direktive vor der \ endif-Direktive sein.
ms.assetid: 982466d9-ae77-4e1c-89f3-511335165da7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 086acd9e6323f7be11a65951a33b2b11b680ad46
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710913"
---
# <a name="else"></a>\#else

Die **\# else** -Direktive markiert eine optionale Klausel eines Blocks für die bedingte Kompilierung, der durch eine **\# ifdef**-, **\# ifndef**-oder **\# if** -Direktive definiert wird. Die **\# else** -Direktive muss die letzte Direktive vor der **\# EndIf** -Direktive sein.

``` syntax
#else
```

Diese Direktive hat keine Parameter.

## <a name="example"></a>Beispiel

In diesem Beispiel wird die zweite [**Bitmap**](bitmap-resource.md) -Anweisung nur dann kompiliert, wenn Debug nicht definiert ist:

``` syntax
#ifdef DEBUG
    BITMAP 1 errbox.bmp
#else
    BITMAP 1 userbox.bmp
#endif
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Präprozessordirektiven](preprocessor-directives.md)
</dt> </dl>

 

 




