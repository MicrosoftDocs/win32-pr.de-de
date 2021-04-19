---
description: Das Sperren einer Ressource bedeutet, den CPU-Zugriff auf den Speicher zu gewähren.
ms.assetid: b17d8262-e514-4b9c-9237-653a4258a14e
title: Sperren von Ressourcen (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70d66a7a420a33cb908d0974f9d942597019aded
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106342553"
---
# <a name="locking-resources-direct3d-9"></a><span data-ttu-id="3a47d-103">Sperren von Ressourcen (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="3a47d-103">Locking Resources (Direct3D 9)</span></span>

<span data-ttu-id="3a47d-104">Das Sperren einer Ressource bedeutet, den CPU-Zugriff auf den Speicher zu gewähren.</span><span class="sxs-lookup"><span data-stu-id="3a47d-104">Locking a resource means granting CPU access to its storage.</span></span> <span data-ttu-id="3a47d-105">Die folgenden Sperr Optionen sind für Ressourcen definiert:</span><span class="sxs-lookup"><span data-stu-id="3a47d-105">The following locking options are defined for resources:</span></span>

-   <span data-ttu-id="3a47d-106">D3DLOCK \_ verwerfen</span><span class="sxs-lookup"><span data-stu-id="3a47d-106">D3DLOCK\_DISCARD</span></span>
-   <span data-ttu-id="3a47d-107">D3DLOCK \_ schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3a47d-107">D3DLOCK\_READONLY</span></span>
-   <span data-ttu-id="3a47d-108">D3DLOCK \_ noüberschreibung</span><span class="sxs-lookup"><span data-stu-id="3a47d-108">D3DLOCK\_NOOVERWRITE</span></span>
-   <span data-ttu-id="3a47d-109">D3DLOCK \_ nosyslock</span><span class="sxs-lookup"><span data-stu-id="3a47d-109">D3DLOCK\_NOSYSLOCK</span></span>
-   <span data-ttu-id="3a47d-110">D3DLOCK \_ kein \_ Dirty \_ Update</span><span class="sxs-lookup"><span data-stu-id="3a47d-110">D3DLOCK\_NO\_DIRTY\_UPDATE</span></span>

<span data-ttu-id="3a47d-111">Ausführliche Informationen zu Sperr Flags und deren Beziehung zu bestimmten Ressourcen finden Sie auf den Referenzseiten zu den einzelnen Methoden zum Sperren von Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="3a47d-111">For details on locking flags and how they relate to specific resources, see the reference pages on the individual resource locking methods.</span></span> <span data-ttu-id="3a47d-112">Anwendungsentwickler sollten beachten, dass die \_ Flags D3DLOCK DISCARD, D3DLOCK Read \_ only und D3DLOCK \_ noüberschreibung nur Hinweise sind.</span><span class="sxs-lookup"><span data-stu-id="3a47d-112">Application developers should note that the D3DLOCK\_DISCARD, D3DLOCK\_READONLY, and D3DLOCK\_NOOVERWRITE flags are only hints.</span></span> <span data-ttu-id="3a47d-113">Die Laufzeit überprüft nicht, ob Anwendungen den von diesen Flags angegebenen Funktionen folgen.</span><span class="sxs-lookup"><span data-stu-id="3a47d-113">The run time does not check that applications are following the functionality specified by these flags.</span></span> <span data-ttu-id="3a47d-114">Eine Anwendung, die D3DLOCK-schreibgeschützt angibt, \_ aber dann in die Ressource schreibt, sollte nicht definierte Ergebnisse erwarten.</span><span class="sxs-lookup"><span data-stu-id="3a47d-114">An application that specifies D3DLOCK\_READONLY but then writes to the resource should expect undefined results.</span></span> <span data-ttu-id="3a47d-115">Im Allgemeinen ist es nicht gewährleistet, dass die Verwendung von Sperrflags, einschließlich der sperrnutzungsflags, in späteren Releases funktioniert und eine erhebliche Leistungs Einbuße verursachen kann.</span><span class="sxs-lookup"><span data-stu-id="3a47d-115">In general, working against locking flags, including the locking usage flags, is not guaranteed to work in later releases and may incur a significant performance penalty.</span></span>

<span data-ttu-id="3a47d-116">Auf einen Sperr Vorgang folgt ein Entsperrvorgang.</span><span class="sxs-lookup"><span data-stu-id="3a47d-116">A lock operation is followed by an unlock operation.</span></span> <span data-ttu-id="3a47d-117">Wenn z. b. eine Textur gesperrt ist, gibt die Anwendung den direkten Zugriff auf gesperrte Texturen aus, indem Sie sie entsperrt.</span><span class="sxs-lookup"><span data-stu-id="3a47d-117">For example, after locking a texture, the application subsequently relinquishes direct access to locked textures by unlocking them.</span></span> <span data-ttu-id="3a47d-118">Zusätzlich zum Gewähren von Prozessor Zugriff werden alle anderen Vorgänge, die diese Ressource betreffen, für die Dauer einer Sperre serialisiert.</span><span class="sxs-lookup"><span data-stu-id="3a47d-118">In addition to granting processor access, any other operations involving that resource are serialized for the duration of a lock.</span></span> <span data-ttu-id="3a47d-119">Nur eine einzige Sperre für eine Ressource ist zulässig, auch bei nicht überlappenden Regionen, und es können keine Zugriffstasten auf einer Oberfläche fortgeführt werden, während ein Sperr Vorgang auf dieser Oberfläche aussteht.</span><span class="sxs-lookup"><span data-stu-id="3a47d-119">Only a single lock for a resource is allowed, even for non-overlapping regions, and no accelerator operations on a surface can be ongoing while a lock operation is outstanding on that surface.</span></span>

<span data-ttu-id="3a47d-120">Jede Ressourcen Schnittstelle verfügt über Methoden zum Sperren der enthaltenen Puffer.</span><span class="sxs-lookup"><span data-stu-id="3a47d-120">Each resource interface has methods for locking the contained buffers.</span></span> <span data-ttu-id="3a47d-121">Jede Textur Ressource kann auch einen Teil Teil dieser Ressource sperren.</span><span class="sxs-lookup"><span data-stu-id="3a47d-121">Each texture resource can also lock a sub-portion of that resource.</span></span> <span data-ttu-id="3a47d-122">2D-Ressourcen (Oberflächen) ermöglichen das Sperren von unter Rechtecke, und volumeressourcen ermöglichen das Sperren von Subvolumes oder Feldern.</span><span class="sxs-lookup"><span data-stu-id="3a47d-122">2D resources (surfaces) allow the locking of sub-rectangles, and volume resources allow the locking of sub-volumes or boxes.</span></span> <span data-ttu-id="3a47d-123">Jede Lock-Methode gibt eine-Struktur zurück, die einen Zeiger auf den Speicher, der die Ressource unterstützt, und die Werte, die die Abstände zwischen Zeilen oder Daten Ebenen darstellen, abhängig vom Ressourcentyp enthält.</span><span class="sxs-lookup"><span data-stu-id="3a47d-123">Each lock method returns a structure that contains a pointer to the storage backing the resource and values representing the distances between rows or planes of data, depending on the resource type.</span></span> <span data-ttu-id="3a47d-124">Weitere Informationen finden Sie in den Methoden Listen für die Ressourcen Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="3a47d-124">For details, see the method lists for the resource interfaces.</span></span> <span data-ttu-id="3a47d-125">Der zurückgegebene Zeiger zeigt immer auf das linke obere Byte in den gesperrten Unterregionen.</span><span class="sxs-lookup"><span data-stu-id="3a47d-125">The returned pointer always points to the top-left byte in the locked sub-regions.</span></span>

<span data-ttu-id="3a47d-126">Wenn Sie mit Index-und Vertexpuffern arbeiten, können Sie mehrere Sperr Aufrufe durchführen. Sie müssen jedoch sicherstellen, dass die Anzahl der Sperr Aufrufe mit der Anzahl der entsperrungs Aufrufe übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="3a47d-126">When working with index and vertex buffers, you can make multiple lock calls; however, you must ensure that the number of lock calls matches the number of unlock calls.</span></span>

<span data-ttu-id="3a47d-127">DXTn speichert Pixel in codierten 4 x 4-Blöcken und kann nur für 4 x 4-Grenzen gesperrt werden.</span><span class="sxs-lookup"><span data-stu-id="3a47d-127">The DXTn store pixels in encoded 4x4 blocks, and can only be locked on 4x4 boundaries.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3a47d-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3a47d-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a47d-129">Direct3D-Ressourcen</span><span class="sxs-lookup"><span data-stu-id="3a47d-129">Direct3D Resources</span></span>](direct3d-resources.md)
</dt> </dl>

 

 



