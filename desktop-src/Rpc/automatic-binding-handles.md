---
title: Automatische Bindungshandles
description: Automatische Bindungshandles sind nützlich, wenn die Anwendung keinen bestimmten Server benötigt und keine Zustandsinformationen zwischen Client und Server verwalten muss.
ms.assetid: ba049369-6c8b-4313-a266-e0364a30056e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b619b17e44e79e623bcffa84f4938d1278a7d146d6de90547cd833e1bf091167
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120023440"
---
# <a name="automatic-binding-handles"></a>Automatische Bindungshandles

Automatische Bindungshandles sind nützlich, wenn die Anwendung keinen bestimmten Server benötigt und keine Zustandsinformationen zwischen Client und Server verwalten muss. Wenn Sie ein automatisches Bindungshandles verwenden, müssen Sie keinen Clientanwendungscode schreiben, um Bindungen und Handles zu verarbeiten. Sie geben einfach die Verwendung des automatischen Bindungshandles in der Anwendungskonfigurationsdatei (Application Configuration File, ACF) an. Der Stub definiert dann das Handle und verwaltet die Bindung.

Beispielsweise kann ein Zeitstempelvorgang mithilfe eines automatischen Handles implementiert werden. Es macht keinen Unterschied für die Clientanwendung, welcher Server ihr den Zeitstempel zur Verfügung stellt, da sie die Zeit von jedem verfügbaren Server akzeptieren kann.

> [!Note]  
> Automatische Handles werden für die Macintosh-Plattform nicht unterstützt.

 

Sie geben die Verwendung von automatischen Handles an, indem Sie das \[ [**\_ AutoHandlesattribut**](/windows/desktop/Midl/auto-handle) \] in ACF angeben. Im Beispiel für den Zeitstempel wird der folgende ACF verwendet:

``` syntax
/* ACF file */
[
  auto_handle
]
interface autoh
{
}
```

Wenn der ACF kein anderes Handleattribut enthält und die Remoteverfahren keine expliziten Handles verwenden, verwendet der MIDL-Compiler standardmäßig automatische Handles. Außerdem werden automatische Handles als Standard verwendet, wenn der ACF nicht vorhanden ist.

Die Remoteverfahren werden in der IDL-Datei angegeben. Das automatische Handle darf nicht als Argument für die Remoteprozedur angezeigt werden. Beispiel:

``` syntax
/* IDL file */
[ 
  uuid (6B29FC40-CA47-1067-B31D-00DD010662DA),
  version(1.0),
  pointer_default(unique)
]
interface autoh
{
  void GetTime([out] long * time);
  void Shutdown(void);
}
```

Der Vorteil des automatischen Handles ist, dass der Entwickler keinen Code schreiben muss, um das Handle zu verwalten. die Stubs verwalten die Bindung automatisch. Dies weht erheblich von dem Beispiel [Hello, World ab,](tutorial.md)bei dem der Client das implizite primitive Handle verwaltet, das im ACF definiert ist, und mehrere Laufzeitfunktionen aufrufen muss, um das Bindungshand handle zu erstellen.

 

 