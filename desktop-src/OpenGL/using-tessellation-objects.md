---
title: Verwenden von Mosaik Objekten
description: Wenn ein komplexes Polygon beschrieben und im Mosaik Prozess verwendet wird, werden zugeordnete Daten, wie z. b. die Scheitel Punkte, Kanten und Rückruf Funktionen, benötigt.
ms.assetid: b6102e25-280c-4d0d-9350-d0038d1a0306
keywords:
- OpenGL-Hilfsprogramm (GLU), Mosaik Objekte
- GLU (OpenGL-Hilfsprogramm), Mosaik Objekte
- Mosaik Objekte OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 590ab571e656fcd346da265bfa921cb965fdf540
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309639"
---
# <a name="using-tessellation-objects"></a><span data-ttu-id="81a1a-106">Verwenden von Mosaik Objekten</span><span class="sxs-lookup"><span data-stu-id="81a1a-106">Using Tessellation Objects</span></span>

<span data-ttu-id="81a1a-107">Wenn ein komplexes Polygon beschrieben und im Mosaik Prozess verwendet wird, werden zugeordnete Daten, wie z. b. die Scheitel Punkte, Kanten und Rückruf Funktionen, benötigt.</span><span class="sxs-lookup"><span data-stu-id="81a1a-107">As a complex polygon is being described and tessellated, it requires associated data, such as the vertices, edges, and callback functions.</span></span> <span data-ttu-id="81a1a-108">Alle diese Daten sind an ein einzelnes Mosaik Objekt gebunden.</span><span class="sxs-lookup"><span data-stu-id="81a1a-108">All this data is tied to a single tessellation object.</span></span> <span data-ttu-id="81a1a-109">Zum Mosaik eines Polygons verwenden Sie zunächst die [**glunewtess**](glunewtess.md) -Funktion, die ein neues Mosaik Objekt erstellt und einen Zeiger darauf zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="81a1a-109">To tessellate a polygon, you first use the [**gluNewTess**](glunewtess.md) function which creates a new tessellation object and returns a pointer to it.</span></span> <span data-ttu-id="81a1a-110">Wenn die Funktion fehlschlägt, wird ein NULL-Zeiger zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="81a1a-110">A null pointer is returned if the function fails.</span></span>

<span data-ttu-id="81a1a-111">Wenn Sie kein Mosaik Objekt mehr benötigen, können Sie es löschen und den gesamten zugeordneten Arbeitsspeicher mit " [**gludeletetess**](gludeletetess.md)" freigeben.</span><span class="sxs-lookup"><span data-stu-id="81a1a-111">If you no longer need a tessellation object, you can delete it and free all associated memory with [**gluDeleteTess**](gludeletetess.md).</span></span>

<span data-ttu-id="81a1a-112">Sie können ein einzelnes Mosaik Objekt für alle Mosaik Vorgänge wieder verwenden.</span><span class="sxs-lookup"><span data-stu-id="81a1a-112">You can reuse a single tessellation object for all your tessellations.</span></span> <span data-ttu-id="81a1a-113">Dieses Objekt ist nur erforderlich, da Bibliotheksfunktionen möglicherweise eigene Mosaik Vorgänge durchführen müssen, und Sie sollten dies tun können, ohne dass sich dies auf das von Ihrem Programm durch zuführte Mosaik beeinträchtigt.</span><span class="sxs-lookup"><span data-stu-id="81a1a-113">This object is required only because library functions may need to do their own tessellations, and they should be able to do so without interfering with any tessellation that your program is performing.</span></span> <span data-ttu-id="81a1a-114">Mehrere Mosaik Objekte sind ebenfalls nützlich, wenn Sie unterschiedliche Sätze von Rückrufen für verschiedene Mosaik Vorgänge verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="81a1a-114">Multiple tessellation objects are also useful if you want to use different sets of callbacks for different tessellations.</span></span> <span data-ttu-id="81a1a-115">In der Regel weisen Sie jedoch ein einzelnes Mosaik Objekt zu und verwenden es für alle Mosaik Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="81a1a-115">Typically, however, you allocate a single tessellation object and use it for all the tessellations.</span></span> <span data-ttu-id="81a1a-116">Es ist nicht erforderlich, es freizugeben, da es eine kleine Menge an Arbeitsspeicher verwendet.</span><span class="sxs-lookup"><span data-stu-id="81a1a-116">There's no real need to free it, because it uses a small amount of memory.</span></span> <span data-ttu-id="81a1a-117">Wenn Sie dagegen eine Bibliotheksfunktion schreiben, die das-Mosaik verwendet, achten Sie darauf, dass Sie alle erstellten Mosaik Objekte freigeben.</span><span class="sxs-lookup"><span data-stu-id="81a1a-117">On the other hand, if you're writing a library function that uses GLU tessellation, be careful to free any tessellation objects you create.</span></span>

 

 




