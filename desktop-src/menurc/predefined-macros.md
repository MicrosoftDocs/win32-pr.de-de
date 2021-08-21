---
title: Vordefinierte Makros
description: RC unterstützt nicht die vordefinierten ANSI C-Makros ( \_ \_ DATE , FILE \_ \_ , \_ \_ LINE \_ \_ \_ \_ , \_ \_ \_ \_ STDC \_ \_ , TIME \_ \_ \_ \_ , \_ \_ TIMESTAMP \_ \_ ). Aus diesem Grund können Sie diese Makros nicht in Headerdateien hinzufügen, die Sie in Ihr Ressourcenskript hinzufügen.
ms.assetid: 2098d4a4-7c6f-4cdc-9c02-3d55907f8888
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f9e48b915fae430bf776b9eebab7ac795e7b69a3d79e06a7ce6422b6d6eab6e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971949"
---
# <a name="predefined-macros"></a>Vordefinierte Makros

RC unterstützt nicht die vordefinierten ANSI C-Makros (**\_ \_ DATE \_ \_**, **\_ \_ \_ \_ FILE**, **\_ \_ LINE \_ \_**, **\_ \_ STDC \_ \_**, **\_ \_ TIME \_ \_**, **\_ \_ TIMESTAMP \_ \_**). Aus diesem Grund können Sie diese Makros nicht in Headerdateien hinzufügen, die Sie in Ihr Ressourcenskript hinzufügen.

RC definiert RC INVOKED, wodurch Sie Teile Ihrer Headerdateien bedingt kompilieren können, je nachdem, ob der Compiler Ihr C-Compiler oder \_ der RC-Compiler ist. Dies ist wichtig, da der RC-Compiler nur eine Teilmenge der Anweisungen unterstützt, die ein C-Compiler unterstützen würde.

Um Ihren Code bedingt mit dem RC-Compiler zu kompilieren, umschließen Sie Code, der rc nicht mit \# ifndef RC \_ INVOKED und **\# endif kompilieren kann.**

Das folgende Beispiel ist aus den SDK-Beispielen entnommen. Es wird veranschaulicht, wie eine Headerdatei erstellt wird, die bedingt kompiliert werden kann.

``` syntax
#ifndef RC_INVOKED
#pragma message("Including CntrOutl.H from " __FILE__)
#endif
```

 

 




