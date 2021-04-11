---
title: Vordefinierte Makros
description: RC unterstützt die vordefinierten ANSI C-Makros ( \_ \_ Date \_ \_ , \_ \_ file \_ \_ , \_ \_ line \_ \_ , \_ \_ stdc \_ \_ , \_ \_ time \_ \_ , \_ \_ timestamp \_ \_ ) nicht. Daher können Sie diese Makros nicht in Header Dateien einschließen, die Sie in Ihr Ressourcen Skript einschließen.
ms.assetid: 2098d4a4-7c6f-4cdc-9c02-3d55907f8888
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 351674bc86ab56753bb49dba9e65edd97a7b1a04
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100683"
---
# <a name="predefined-macros"></a>Vordefinierte Makros

RC unterstützt die vordefinierten ANSI C-Makros (**\_ \_ Date \_ \_**, **\_ \_ file \_ \_**, **\_ \_ line \_ \_**, **\_ \_ \_ stdc \_**, **\_ \_ time \_ , \_** **\_ \_ timestamp \_ ) \_** nicht. Daher können Sie diese Makros nicht in Header Dateien einschließen, die Sie in Ihr Ressourcen Skript einschließen.

RC definiert RC- \_ aufgerufen, sodass Sie Teile der Header Dateien bedingt kompilieren können, je nachdem, ob der Compiler der C-Compiler oder der RC-Compiler ist. Dies ist wichtig, da der RC-Compiler nur eine Teilmenge der Anweisungen unterstützt, die von einem C-Compiler unterstützt werden.

Um den Code bedingt mit dem RC-Compiler zu kompilieren, müssen Sie den Code umschließen, den RC nicht mit den Aufrufen \# \_ und **\# EndIf** von ifndef RC kompilieren kann

Das folgende Beispiel stammt aus den SDK-Beispielen. Es wird veranschaulicht, wie eine Header Datei erstellt wird, die bedingt kompiliert werden kann.

``` syntax
#ifndef RC_INVOKED
#pragma message("Including CntrOutl.H from " __FILE__)
#endif
```

 

 




