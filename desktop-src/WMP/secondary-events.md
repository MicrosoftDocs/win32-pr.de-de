---
title: Sekundäre Ereignisse
description: Sekundäre Ereignisse
ms.assetid: cc9eb382-82ca-4416-a04e-1572e4c69c90
keywords:
- Windows Media Player Skins, sekundäre Ereignisse
- Skins, sekundäre Ereignisse
- Ereignisse, Sekundär
- Schreiben von Code für Skins, sekundäre Ereignisse
- sekundäre Ereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e04785a7468353665083287ac1b74bce5cbf0f8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471596"
---
# <a name="secondary-events"></a>Sekundäre Ereignisse

Sie können bestimmen, welche anderen Ereignisse stattfinden, wenn ein bestimmtes Ereignis ausgelöst wird. Wenn z. b. auf eine Maustaste geklickt wird, möchten Sie möglicherweise wissen, ob die Alt-Taste gleichzeitig gedrückt war.

## <a name="event-attributes"></a>Ereignisattribute

Die folgenden Ereignis Attribute werden für Skins unterstützt:

-   **altKey**
-   **gedrückt**
-   **clientX**
-   **clientY**
-   **ctrlKey**
-   **fromelements**
-   **OffsetX**
-   **offität**
-   **screenX**
-   **Screeny**
-   **shiftKey**
-   **srcelements**
-   **"Element"**
-   **x**
-   **y**
-   **Keycode**

Weitere Informationen zu diesen Attributen finden Sie in der [Skin-Programmier Referenz](skin-programming-reference.md).

## <a name="using-secondary-events"></a>Verwenden sekundärer Ereignisse

Ereignis Attribute können nur in JScript-Code verarbeitet werden. Sie müssen die folgende Syntax verwenden:


```C++
event.eventattributename
```



*eventattributename* ist der Name des Ereignis Attributs. Wenn Sie z. b. ermitteln möchten, ob die Alt-Taste während eines Click-Ereignisses gedrückt wurde, können Sie die folgenden Zeilen in Ihrem JScript-Code verwenden:


```C++
wasAlt = event.altKey ;
if (wasAlt = true)
{
   // Do something here.
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Behandeln von Ereignissen**](handling-events.md)
</dt> </dl>

 

 




