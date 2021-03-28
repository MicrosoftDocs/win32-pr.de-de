---
description: Wie bei einem Clippingbereich ist ein Clip Pfad ein weiteres Grafik Objekt, das von einer Anwendung in einen Gerätekontext ausgewählt werden kann.
ms.assetid: 35c4052b-3f11-40bc-9cc9-6f999326a656
title: Clip Pfade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dc4a93b0047110a6adb2f68d413e89cb1e97fbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978769"
---
# <a name="clip-paths"></a><span data-ttu-id="39713-103">Clip Pfade</span><span class="sxs-lookup"><span data-stu-id="39713-103">Clip Paths</span></span>

<span data-ttu-id="39713-104">Wie bei einem Clippingbereich ist ein Clip Pfad ein weiteres Grafik Objekt, das von einer Anwendung in einen Gerätekontext ausgewählt werden kann.</span><span class="sxs-lookup"><span data-stu-id="39713-104">Like a clipping region, a clip path is another graphics object that an application can select into a device context.</span></span> <span data-ttu-id="39713-105">Anders als bei einem Clippingbereich wird ein Clip Pfad immer von einer Anwendung erstellt und für das Clipping auf eine oder mehrere unregelmäßige Formen verwendet.</span><span class="sxs-lookup"><span data-stu-id="39713-105">Unlike a clipping region, a clip path is always created by an application and it is used for clipping to one or more irregular shapes.</span></span> <span data-ttu-id="39713-106">Beispielsweise kann eine Anwendung die Linien und Kurven verwenden, die die Darstellung von Zeichen in einer Text Zeichenfolge bilden, um einen Clip Pfad zu definieren.</span><span class="sxs-lookup"><span data-stu-id="39713-106">For example, an application can use the lines and curves that form the outlines of characters in a string of text to define a clip path.</span></span>

<span data-ttu-id="39713-107">Zum Erstellen eines Clip Pfades muss zunächst ein Pfad erstellt werden, der die erforderliche unregelmäßige Form beschreibt.</span><span class="sxs-lookup"><span data-stu-id="39713-107">To create a clip path, it's first necessary to create a path that describes the required irregular shape.</span></span> <span data-ttu-id="39713-108">Pfade werden erstellt, indem nach dem Aufrufen der [**beginpath**](/windows/desktop/api/Wingdi/nf-wingdi-beginpath) -Funktion und vor dem Aufrufen der [**endpath**](/windows/desktop/api/Wingdi/nf-wingdi-endpath) -Funktion die entsprechenden GDI-Zeichnungsfunktionen (Graphics Device Interface) aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="39713-108">Paths are created by calling the appropriate graphics device interface (GDI) drawing functions after calling the [**BeginPath**](/windows/desktop/api/Wingdi/nf-wingdi-beginpath) function and before calling the [**EndPath**](/windows/desktop/api/Wingdi/nf-wingdi-endpath) function.</span></span> <span data-ttu-id="39713-109">Diese Auflistung von Funktionen wird als Pfad Klammer bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="39713-109">This collection of functions is called a path bracket.</span></span> <span data-ttu-id="39713-110">Weitere Informationen zu Pfaden und Pfad Klammern finden Sie unter [Pfade](paths.md).</span><span class="sxs-lookup"><span data-stu-id="39713-110">For more information about paths and path brackets, see [Paths](paths.md).</span></span>

<span data-ttu-id="39713-111">Nachdem der Pfad erstellt wurde, kann er in einen Clip Pfad konvertiert werden, indem die [**selectclippath**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath) -Funktion aufgerufen, ein Gerätekontext identifiziert und ein Verwendungs Modus angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="39713-111">After the path is created, it can be converted to a clip path by calling the [**SelectClipPath**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath) function, identifying a device context, and specifying a usage mode.</span></span> <span data-ttu-id="39713-112">Der Verwendungs Modus bestimmt, wie das System den neuen Clip Pfad mit dem ursprünglichen Clippingbereich des Geräte Kontexts kombiniert.</span><span class="sxs-lookup"><span data-stu-id="39713-112">The usage mode determines how the system combines the new clip path with the device context's original clipping region.</span></span> <span data-ttu-id="39713-113">In der folgenden Tabelle werden die Verwendungs Modi beschrieben.</span><span class="sxs-lookup"><span data-stu-id="39713-113">The following table describes the usage modes.</span></span>



| <span data-ttu-id="39713-114">Mode</span><span class="sxs-lookup"><span data-stu-id="39713-114">Mode</span></span>      | <span data-ttu-id="39713-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="39713-115">Description</span></span>                                                                                                                  |
|-----------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39713-116">RGN \_ und</span><span class="sxs-lookup"><span data-stu-id="39713-116">RGN\_AND</span></span>  | <span data-ttu-id="39713-117">Der Clip Pfad enthält die Schnittmenge (überlappende Bereiche) des Clippingbereichs des Geräte Kontexts und den aktuellen Pfad.</span><span class="sxs-lookup"><span data-stu-id="39713-117">The clip path includes the intersection (overlapping areas) of the device context's clipping region and the current path.</span></span>    |
| <span data-ttu-id="39713-118">RGN- \_ Kopie</span><span class="sxs-lookup"><span data-stu-id="39713-118">RGN\_COPY</span></span> | <span data-ttu-id="39713-119">Der Clip Pfad ist der aktuelle Pfad.</span><span class="sxs-lookup"><span data-stu-id="39713-119">The clip path is the current path.</span></span>                                                                                           |
| <span data-ttu-id="39713-120">RGN- \_ diff</span><span class="sxs-lookup"><span data-stu-id="39713-120">RGN\_DIFF</span></span> | <span data-ttu-id="39713-121">Der Clip Pfad schließt den Clippingbereich des Geräte Kontexts ein, der überschneidende Teile des aktuellen Pfads ausgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="39713-121">The clip path includes the device context's clipping region with any intersecting parts of the current path excluded.</span></span>        |
| <span data-ttu-id="39713-122">RGN \_ oder</span><span class="sxs-lookup"><span data-stu-id="39713-122">RGN\_OR</span></span>   | <span data-ttu-id="39713-123">Der Clip Pfad enthält die Union (kombinierte Bereiche) des Clippingbereichs des Geräte Kontexts und den aktuellen Pfad.</span><span class="sxs-lookup"><span data-stu-id="39713-123">The clip path includes the union (combined areas) of the device context's clipping region and the current path.</span></span>              |
| <span data-ttu-id="39713-124">RGN- \_ Xor</span><span class="sxs-lookup"><span data-stu-id="39713-124">RGN\_XOR</span></span>  | <span data-ttu-id="39713-125">Der Clip Pfad umfasst die Vereinigung des Clippingbereichs des Geräte Kontexts und des aktuellen Pfads, schließt jedoch die Schnittmenge aus.</span><span class="sxs-lookup"><span data-stu-id="39713-125">The clip path includes the union of the device context's clipping region and the current path but excludes the intersection.</span></span> |



 

 

 



