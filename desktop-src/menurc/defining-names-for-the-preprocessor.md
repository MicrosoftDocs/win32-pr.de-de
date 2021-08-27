---
title: Definieren von Namen für den Präprozessor
description: Sie können die bedingte Kompilierung in einem Skript basierend darauf angeben, ob ein Name in der RC-Befehlszeile mit der Option /d oder in der Datei oder in einer Includedatei mit der \define-Direktive definiert ist.
ms.assetid: bc72911e-2aca-46a4-b6c1-60cc8ed7d82f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3bcf9c02b5a4da4487b0c82de8d8b0223662cb30f9529e82204fc66a3de91cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972109"
---
# <a name="defining-names-for-the-preprocessor"></a>Definieren von Namen für den Präprozessor

Sie können die bedingte Kompilierung in einem Skript basierend darauf angeben, ob ein Name in der RC-Befehlszeile mit der **Option /d** oder in der Datei oder in einer Includedatei mit der [**\# define-Direktive definiert**](-define.md) ist.

Angenommen, Ihre Anwendung verfügt über ein Popupmenü, das nur mit Debugversionen der Anwendung angezeigt werden soll. Wenn Sie die Anwendung für die normale Verwendung kompilieren, ist das Menü nicht enthalten. Das folgende Beispiel zeigt die Anweisungen, die der Ressourcendefinitionsdatei hinzugefügt werden können, um ein Debugmenü zu definieren:

``` syntax
#include <windows.h>

MainMenu MENU
{
    //. . .
#ifdef DEBUG
    POPUP "&Debug"
    {
        MENUITEM "&Memory usage", ID_MEMORY
        MENUITEM "&Walk data heap", ID_WALK_HEAP
    }
#endif
}
```

Beim Kompilieren von Ressourcen für eine Debugversion der Anwendung können Sie das Menü Debuggen mithilfe des folgenden Befehls verwenden:

**rc -d DEBUG myapp.rc**

Um Ressourcen für eine normale Version der Anwendung zu kompilieren, die nicht das Menü Debuggen enthält? können Sie den folgenden Befehl verwenden:

**rc myapp.rc**

 

 




