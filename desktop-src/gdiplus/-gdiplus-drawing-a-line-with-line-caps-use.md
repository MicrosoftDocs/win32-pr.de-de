---
description: Sie können den Anfang oder das Ende einer Linie in einer von mehreren Formen zeichnen, die als Linien Caps bezeichnet werden. Windows GDI+ unterstützt mehrere Linien Kappen, z. b. Round, Square, Diamond und Arrowhead.
ms.assetid: c9d90114-3913-486c-a808-b08dd473d9a1
title: Zeichnen einer Linie mit Linien Deckeln
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50ee4dd12a3068fe5200e0f1ae786765170ccba7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104987688"
---
# <a name="drawing-a-line-with-line-caps"></a><span data-ttu-id="20807-104">Zeichnen einer Linie mit Linien Deckeln</span><span class="sxs-lookup"><span data-stu-id="20807-104">Drawing a Line with Line Caps</span></span>

<span data-ttu-id="20807-105">Sie können den Anfang oder das Ende einer Linie in einer von mehreren Formen zeichnen, die als Linien Caps bezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="20807-105">You can draw the start or end of a line in one of several shapes called line caps.</span></span> <span data-ttu-id="20807-106">Windows GDI+ unterstützt mehrere Linien Kappen, z. b. Round, Square, Diamond und Arrowhead.</span><span class="sxs-lookup"><span data-stu-id="20807-106">Windows GDI+ supports several line caps, such as round, square, diamond, and arrowhead.</span></span>

<span data-ttu-id="20807-107">Sie können für den Anfang einer Linie (Start-Obergrenze), das Ende einer Linie (Ende) oder die Bindestriche einer gestrichelten Linie (Bindestrich) Zeilenenden angeben.</span><span class="sxs-lookup"><span data-stu-id="20807-107">You can specify line caps for the start of a line (start cap), the end of a line (end cap), or the dashes of a dashed line (dash cap).</span></span>

<span data-ttu-id="20807-108">Im folgenden Beispiel wird eine Linie mit einem Pfeilspitzen an einem Ende und einem Rundenende am anderen Ende gezeichnet:</span><span class="sxs-lookup"><span data-stu-id="20807-108">The following example draws a line with an arrowhead at one end and a round cap at the other end:</span></span>


```
Pen pen(Color(255, 0, 0, 255), 8);
stat = pen.SetStartCap(LineCapArrowAnchor);
stat = pen.SetEndCap(LineCapRoundAnchor);
stat = graphics.DrawLine(&pen, 20, 175, 300, 175);
```



<span data-ttu-id="20807-109">Die folgende Abbildung zeigt die resultierende Zeile.</span><span class="sxs-lookup"><span data-stu-id="20807-109">The following illustration shows the resulting line.</span></span>

![Abbildung, die eine horizontale Linie mit einem Pfeil am linken Ende und einem Kreis am rechten Ende zeigt](images/pens4.png)

<span data-ttu-id="20807-111">**Linecaparrowanchor** und **linecaproundanchor** sind Elemente der [**LineCap**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-linecap) -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="20807-111">**LineCapArrowAnchor** and **LineCapRoundAnchor** are elements of the [**LineCap**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-linecap) enumeration.</span></span>

 

 



