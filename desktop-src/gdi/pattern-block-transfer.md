---
description: Der Name der patblt-Funktion (eine Abkürzung für die Musterblock Übertragung) impliziert, dass diese Funktion einfach den Pinsel (oder das Muster) repliziert, bis Sie ein angegebenes Rechteck füllt.
ms.assetid: 601e1e79-a328-4e63-958a-ca26129e03f8
title: Muster Block Übertragung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54424348c28b83d1d0d1075072e80b18049546ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104993934"
---
# <a name="pattern-block-transfer"></a><span data-ttu-id="f0c9b-103">Muster Block Übertragung</span><span class="sxs-lookup"><span data-stu-id="f0c9b-103">Pattern Block Transfer</span></span>

<span data-ttu-id="f0c9b-104">Der Name der [**patblt**](/windows/desktop/api/Wingdi/nf-wingdi-patblt) -Funktion (eine Abkürzung für die Musterblock Übertragung) impliziert, dass diese Funktion einfach den Pinsel (oder das Muster) repliziert, bis Sie ein angegebenes Rechteck füllt.</span><span class="sxs-lookup"><span data-stu-id="f0c9b-104">The name of the [**PatBlt**](/windows/desktop/api/Wingdi/nf-wingdi-patblt) function (an abbreviation for pattern block transfer) implies that this function simply replicates the brush (or pattern) until it fills a specified rectangle.</span></span> <span data-ttu-id="f0c9b-105">Allerdings ist die-Funktion tatsächlich viel leistungsfähiger.</span><span class="sxs-lookup"><span data-stu-id="f0c9b-105">However, the function is actually much more powerful.</span></span> <span data-ttu-id="f0c9b-106">Vor dem Replizieren des Pinsels werden die Farbdaten für das Muster mit den Farbdaten für die vorhandenen Pixel in der Videoanzeige mithilfe eines Raster Vorgangs (ROP) kombiniert.</span><span class="sxs-lookup"><span data-stu-id="f0c9b-106">Before replicating the brush, it combines the color data for the pattern with the color data for the existing pixels on the video display by using a raster operation (ROP).</span></span> <span data-ttu-id="f0c9b-107">Ein ROP ist eine bitweise Operation, die auf die Bits der Farbdaten für den replizierten Pinsel und die Bits der Farbdaten für das Ziel Rechteck auf dem Anzeigegerät angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="f0c9b-107">An ROP is a bitwise operation that is applied to the bits of color data for the replicated brush and the bits of color data for the target rectangle on the display device.</span></span> <span data-ttu-id="f0c9b-108">Es sind 256 ROPS vorhanden. die **patblt** -Funktion erkennt jedoch nur diejenigen, die ein Muster und ein Ziel erfordern (nicht diejenigen, die eine Quelle erfordern).</span><span class="sxs-lookup"><span data-stu-id="f0c9b-108">There are 256 ROPs; however, the **PatBlt** function recognizes only those that require a pattern and a destination (not those that require a source).</span></span> <span data-ttu-id="f0c9b-109">In der folgenden Tabelle sind die gängigsten ROPS aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="f0c9b-109">The following table identifies the most common ROPs.</span></span>



| <span data-ttu-id="f0c9b-110">PS</span><span class="sxs-lookup"><span data-stu-id="f0c9b-110">ROP</span></span>       | <span data-ttu-id="f0c9b-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f0c9b-111">Description</span></span>                                                                         |
|-----------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f0c9b-112">Patcopy</span><span class="sxs-lookup"><span data-stu-id="f0c9b-112">PATCOPY</span></span>   | <span data-ttu-id="f0c9b-113">Kopiert das Muster in die Ziel Bitmap.</span><span class="sxs-lookup"><span data-stu-id="f0c9b-113">Copies the pattern to the destination bitmap.</span></span>                                       |
| <span data-ttu-id="f0c9b-114">Patinvert</span><span class="sxs-lookup"><span data-stu-id="f0c9b-114">PATINVERT</span></span> | <span data-ttu-id="f0c9b-115">Kombiniert die Ziel Bitmap mit dem Muster mithilfe des booleschen XOR-Operators.</span><span class="sxs-lookup"><span data-stu-id="f0c9b-115">Combines the destination bitmap with the pattern by using the Boolean XOR operator.</span></span> |
| <span data-ttu-id="f0c9b-116">Dstinvert</span><span class="sxs-lookup"><span data-stu-id="f0c9b-116">DSTINVERT</span></span> | <span data-ttu-id="f0c9b-117">Kehrt die Ziel Bitmap um.</span><span class="sxs-lookup"><span data-stu-id="f0c9b-117">Inverts the destination bitmap.</span></span>                                                     |
| <span data-ttu-id="f0c9b-118">Blackness</span><span class="sxs-lookup"><span data-stu-id="f0c9b-118">BLACKNESS</span></span> | <span data-ttu-id="f0c9b-119">Wandelt die gesamte Ausgabe in binäre Nullen um.</span><span class="sxs-lookup"><span data-stu-id="f0c9b-119">Turns all output to binary zeros.</span></span>                                                   |
| <span data-ttu-id="f0c9b-120">Whitheit</span><span class="sxs-lookup"><span data-stu-id="f0c9b-120">WHITENESS</span></span> | <span data-ttu-id="f0c9b-121">Wandelt die gesamte Ausgabe in binäre Dateien um.</span><span class="sxs-lookup"><span data-stu-id="f0c9b-121">Turns all output to binary ones.</span></span>                                                    |



 

<span data-ttu-id="f0c9b-122">Weitere Informationen finden Sie unter [Raster Vorgangs Codes](raster-operation-codes.md).</span><span class="sxs-lookup"><span data-stu-id="f0c9b-122">For more information, see [Raster Operation Codes](raster-operation-codes.md).</span></span>

 

 



