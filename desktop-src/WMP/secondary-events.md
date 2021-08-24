---
title: Sekundäre Ereignisse
description: Sekundäre Ereignisse
ms.assetid: cc9eb382-82ca-4416-a04e-1572e4c69c90
keywords:
- Windows Media Player Skins,sekundäre Ereignisse
- Skins, sekundäre Ereignisse
- Ereignisse,sekundär
- Schreiben von Code für Skins, sekundäre Ereignisse
- Sekundäre Ereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35fd121330a99c73ed7a52def712bb53949113745a8af0f4c01ded8f9aeaea4a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119735780"
---
# <a name="secondary-events"></a>Sekundäre Ereignisse

Sie können bestimmen, welche anderen Ereignisse stattfinden, wenn ein bestimmtes Ereignis ausgelöst wird. Wenn Sie z. B. auf eine Maustaste klicken, möchten Sie möglicherweise wissen, ob die ALT-TASTE gleichzeitig gedrückt war.

## <a name="event-attributes"></a>Ereignisattribute

Die folgenden Ereignisattribute werden für Skins unterstützt:

-   **altKey**
-   **Schaltfläche**
-   **clientX**
-   **clientY**
-   **STRGKEY**
-   **fromElement**
-   **Offsetx**
-   **Offsety**
-   **screenX**
-   **Screeny**
-   **shiftKey**
-   **srcElement**
-   **toElement**
-   **x**
-   **y**
-   **Schlüsselcode**

Weitere Informationen zu diesen Attributen finden Sie in der [Referenz zur Skinprogrammierung.](skin-programming-reference.md)

## <a name="using-secondary-events"></a>Verwenden sekundärer Ereignisse

Ereignisattribute können nur im Code JScript werden. Sie müssen die folgende Syntax verwenden:


```C++
event.eventattributename
```



*eventattributename* ist der Name des Ereignisattributs. Um beispielsweise zu bestimmen, ob die ALT-TASTE während eines Klick-Ereignisses gedrückt wurde, können Sie die folgenden Zeilen in Ihrem JScript verwenden:


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

 

 




