---
title: Definieren von Namen für den Präprozessor
description: Sie können die bedingte Kompilierung in einem Skript angeben, abhängig davon, ob ein Name in der RC-Befehlszeile mit der/d-Option oder in der Datei oder einer Includedatei mit der \ define-Direktive definiert ist.
ms.assetid: bc72911e-2aca-46a4-b6c1-60cc8ed7d82f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e64b339959ace5a70d83fa8ee8beb615f1bc5ce4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309427"
---
# <a name="defining-names-for-the-preprocessor"></a>Definieren von Namen für den Präprozessor

Sie können die bedingte Kompilierung in einem Skript angeben, abhängig davon, ob ein Name in der RC-Befehlszeile mit der **/d** -Option oder in der Datei oder einer Includedatei mit der [**\# define**](-define.md) -Direktive definiert ist.

Angenommen, die Anwendung verfügt über ein Popup Menü, das nur mit Debugversionen der Anwendung angezeigt werden sollte. Wenn Sie die Anwendung für die normale Verwendung kompilieren, ist das Menü nicht eingeschlossen. Das folgende Beispiel zeigt die-Anweisungen, die der Ressourcen Definitionsdatei hinzugefügt werden können, um ein debugmenü zu definieren:

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

Wenn Sie Ressourcen für eine Debugversion der Anwendung kompilieren, können Sie das Menü Debuggen mit dem folgenden Befehl einschließen:

**RC-d Debuggen MyApp. RC**

Verwenden Sie den folgenden Befehl, um Ressourcen für eine normale Version der Anwendung zu kompilieren? eine, die das Menü "Debuggen" nicht enthält?

**RC MyApp. RC**

 

 




