---
title: Kommentare (Menüs und andere Ressourcen)
description: RC unterstützt die Syntax im C-Stil sowohl für einzeilige Kommentare als auch für Block Kommentare. Einzeilige Kommentare beginnen mit zwei Schrägstrichen (//) und werden bis zum Ende der Zeile ausgeführt. Im folgenden finden Sie ein Beispiel für eine Ressourcen Anweisung, gefolgt von einem einzeiligen Kommentar.
ms.assetid: 045268fb-2d6e-446c-8b95-90e42baeb282
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5fda05690df9b7e7fff6974d75d8275a2842b68
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "103739625"
---
# <a name="comments-menus-and-other-resources"></a>Kommentare (Menüs und andere Ressourcen)

RC unterstützt die Syntax im C-Stil sowohl für einzeilige Kommentare als auch für Block Kommentare. Einzeilige Kommentare beginnen mit zwei Schrägstrichen (//) und werden bis zum Ende der Zeile ausgeführt. Im folgenden finden Sie ein Beispiel für eine Ressourcen Anweisung, gefolgt von einem einzeiligen Kommentar.

``` syntax
NewCursor  CURSOR  NEW.CUR  // a new cursor for the application.
```

Block Kommentare beginnen mit einem öffnenden Trennzeichen (/ \* ) und können bis zu einem schließenden Trennzeichen ( \* /) ausgeführt werden. Kommentare werden nicht geschachtelt. Im folgenden finden Sie ein Beispiel eines Block Kommentars am Anfang einer RC-Datei.

``` syntax
/* 
    Resources.Rc

    Contains the resource definitions for the application.
    Control identifiers are defined in Resources.h.
*/

#include "resources.h"
//...
```

 

 




