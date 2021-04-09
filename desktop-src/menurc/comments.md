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
# <a name="comments-menus-and-other-resources"></a><span data-ttu-id="22f16-105">Kommentare (Menüs und andere Ressourcen)</span><span class="sxs-lookup"><span data-stu-id="22f16-105">Comments (Menus and Other Resources)</span></span>

<span data-ttu-id="22f16-106">RC unterstützt die Syntax im C-Stil sowohl für einzeilige Kommentare als auch für Block Kommentare.</span><span class="sxs-lookup"><span data-stu-id="22f16-106">RC supports C-style syntax for both single-line comments and block comments.</span></span> <span data-ttu-id="22f16-107">Einzeilige Kommentare beginnen mit zwei Schrägstrichen (//) und werden bis zum Ende der Zeile ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="22f16-107">Single-line comments begin with two forward slashes (//) and run to the end of the line.</span></span> <span data-ttu-id="22f16-108">Im folgenden finden Sie ein Beispiel für eine Ressourcen Anweisung, gefolgt von einem einzeiligen Kommentar.</span><span class="sxs-lookup"><span data-stu-id="22f16-108">The following is an example of a resource statement followed by a single-line comment.</span></span>

``` syntax
NewCursor  CURSOR  NEW.CUR  // a new cursor for the application.
```

<span data-ttu-id="22f16-109">Block Kommentare beginnen mit einem öffnenden Trennzeichen (/ \* ) und können bis zu einem schließenden Trennzeichen ( \* /) ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="22f16-109">Block comments begin with an opening delimiter (/\*) and run to a closing delimiter (\*/).</span></span> <span data-ttu-id="22f16-110">Kommentare werden nicht geschachtelt.</span><span class="sxs-lookup"><span data-stu-id="22f16-110">Comments do not nest.</span></span> <span data-ttu-id="22f16-111">Im folgenden finden Sie ein Beispiel eines Block Kommentars am Anfang einer RC-Datei.</span><span class="sxs-lookup"><span data-stu-id="22f16-111">The following is an example of a block comment at the beginning of a .rc file.</span></span>

``` syntax
/* 
    Resources.Rc

    Contains the resource definitions for the application.
    Control identifiers are defined in Resources.h.
*/

#include "resources.h"
//...
```

 

 




