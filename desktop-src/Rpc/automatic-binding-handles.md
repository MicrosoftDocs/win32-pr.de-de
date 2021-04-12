---
title: Automatische Bindungs Handles
description: Automatische Bindungs Handles sind nützlich, wenn die Anwendung keinen bestimmten Server benötigt und keine Zustandsinformationen zwischen dem Client und dem Server beibehalten werden müssen.
ms.assetid: ba049369-6c8b-4313-a266-e0364a30056e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fe83d3f9029e0384c87e5e409583ff70f1e91ac
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316113"
---
# <a name="automatic-binding-handles"></a>Automatische Bindungs Handles

Automatische Bindungs Handles sind nützlich, wenn die Anwendung keinen bestimmten Server benötigt und keine Zustandsinformationen zwischen dem Client und dem Server beibehalten werden müssen. Wenn Sie ein automatisches Bindungs Handle verwenden, müssen Sie keinen Client Anwendungscode für die Behandlung von Bindungen und Handles schreiben – Sie geben einfach die Verwendung des automatischen Bindungs Handles in der Anwendungs Konfigurationsdatei (ACF) an. Der Stub definiert dann das Handle und verwaltet die Bindung.

Beispielsweise kann ein Zeitstempel Vorgang mithilfe eines automatischen Handles implementiert werden. Es gibt keinen Unterschied zur Client Anwendung, welcher Server den Zeitstempel bereitstellt, da er die Zeit von einem beliebigen verfügbaren Server annehmen kann.

> [!Note]  
> Automatische Handles werden für die Macintosh-Plattform nicht unterstützt.

 

Sie geben die Verwendung von automatischen Handles an, indem Sie das Attribut für \[ [**Automatisches \_ handle**](/windows/desktop/Midl/auto-handle) \] in der ACF einschließen. Im Zeitstempel Beispiel wird die folgende ACF verwendet:

``` syntax
/* ACF file */
[
  auto_handle
]
interface autoh
{
}
```

Wenn die ACF kein anderes handle-Attribut enthält, und wenn die Remote Prozeduren keine expliziten Handles verwenden, verwendet der mittlerer l-Compiler standardmäßig automatische Handles. Außerdem werden automatische Handles als Standard verwendet, wenn die ACF nicht vorhanden ist.

Die Remote Prozeduren werden in der IDL-Datei angegeben. Das automatische Handle darf nicht als Argument für die Remote Prozedur angezeigt werden. Beispiel:

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

Der Vorteil des automatischen Handles besteht darin, dass der Entwickler keinen Code zum Verwalten des Handles schreiben muss. die stusb verwalten die Bindung automatisch. Dies unterscheidet sich erheblich von dem [Hello, World-Beispiel](tutorial.md), bei dem der Client das implizite primitive Handle verwaltet, das in der ACF definiert ist, und mehrere Lauf Zeitfunktionen zum Einrichten des Bindungs Handles aufruft.

 

 