---
description: Die folgenden Funktionen werden mit Pinseln verwendet.
ms.assetid: 617eb778-876c-4bbb-90da-c5f13359becb
title: Pinsel Funktionen (Windows GDI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2170ff5c4b743e19da669bd76b340ca95ac2ef9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528394"
---
# <a name="brush-functions-windows-gdi"></a><span data-ttu-id="6fe99-103">Pinsel Funktionen (Windows GDI)</span><span class="sxs-lookup"><span data-stu-id="6fe99-103">Brush Functions (Windows GDI)</span></span>

<span data-ttu-id="6fe99-104">Die folgenden Funktionen werden mit Pinseln verwendet.</span><span class="sxs-lookup"><span data-stu-id="6fe99-104">The following functions are used with brushes.</span></span>



| <span data-ttu-id="6fe99-105">Funktion</span><span class="sxs-lookup"><span data-stu-id="6fe99-105">Function</span></span>                                                   | <span data-ttu-id="6fe99-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6fe99-106">Description</span></span>                                                |
|------------------------------------------------------------|------------------------------------------------------------|
| [<span data-ttu-id="6fe99-107">**"Kreatebrushindirekte"**</span><span class="sxs-lookup"><span data-stu-id="6fe99-107">**CreateBrushIndirect**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-createbrushindirect)         | <span data-ttu-id="6fe99-108">Erstellt einen Pinsel mit einem angegebenen Stil, einer angegebenen Farbe und einem angegebenen Muster.</span><span class="sxs-lookup"><span data-stu-id="6fe99-108">Creates a brush with a specified style, color, and pattern</span></span> |
| [<span data-ttu-id="6fe99-109">**"Kreatedibpatternbrushpt"**</span><span class="sxs-lookup"><span data-stu-id="6fe99-109">**CreateDIBPatternBrushPt**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-createdibpatternbrushpt) | <span data-ttu-id="6fe99-110">Erstellt einen Pinsel mit dem Muster aus einem DIB.</span><span class="sxs-lookup"><span data-stu-id="6fe99-110">Creates a brush with the pattern from a DIB</span></span>                |
| [<span data-ttu-id="6fe99-111">**"Kreatehatchbrush"**</span><span class="sxs-lookup"><span data-stu-id="6fe99-111">**CreateHatchBrush**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-createhatchbrush)               | <span data-ttu-id="6fe99-112">Erstellt einen Pinsel mit einem Schraffurmuster und einer Farbe.</span><span class="sxs-lookup"><span data-stu-id="6fe99-112">Creates a brush with a hatch pattern and color</span></span>             |
| [<span data-ttu-id="6fe99-113">**"Kreatepatternbrush"**</span><span class="sxs-lookup"><span data-stu-id="6fe99-113">**CreatePatternBrush**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-createpatternbrush)           | <span data-ttu-id="6fe99-114">Erstellt einen Pinsel mit einem Bitmapmuster.</span><span class="sxs-lookup"><span data-stu-id="6fe99-114">Creates a brush with a bitmap pattern</span></span>                      |
| [<span data-ttu-id="6fe99-115">**"Kreatesolidbrush"**</span><span class="sxs-lookup"><span data-stu-id="6fe99-115">**CreateSolidBrush**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-createsolidbrush)               | <span data-ttu-id="6fe99-116">Erstellt einen Pinsel mit einer voll Tonfarbe.</span><span class="sxs-lookup"><span data-stu-id="6fe99-116">Creates a brush with a solid color</span></span>                         |
| [<span data-ttu-id="6fe99-117">**Getbrushorgex**</span><span class="sxs-lookup"><span data-stu-id="6fe99-117">**GetBrushOrgEx**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getbrushorgex)                     | <span data-ttu-id="6fe99-118">Ruft den Pinsel Ursprung für einen Gerätekontext ab.</span><span class="sxs-lookup"><span data-stu-id="6fe99-118">Gets the brush origin for a device context</span></span>                 |
| [<span data-ttu-id="6fe99-119">**Getsyscolorbrush**</span><span class="sxs-lookup"><span data-stu-id="6fe99-119">**GetSysColorBrush**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getsyscolorbrush)               | <span data-ttu-id="6fe99-120">Ruft ein Handle für einen Pinsel ab, der einem Farbindex entspricht.</span><span class="sxs-lookup"><span data-stu-id="6fe99-120">Gets a handle to a brush that corresponds to a color index</span></span> |
| [<span data-ttu-id="6fe99-121">**Patblt**</span><span class="sxs-lookup"><span data-stu-id="6fe99-121">**PatBlt**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-patblt)                                   | <span data-ttu-id="6fe99-122">Zeichnet ein Rechteck.</span><span class="sxs-lookup"><span data-stu-id="6fe99-122">Paints a rectangle</span></span>                                         |
| [<span data-ttu-id="6fe99-123">**Setbrushorgex**</span><span class="sxs-lookup"><span data-stu-id="6fe99-123">**SetBrushOrgEx**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setbrushorgex)                     | <span data-ttu-id="6fe99-124">Legt den Pinsel Ursprung für einen Gerätekontext fest.</span><span class="sxs-lookup"><span data-stu-id="6fe99-124">Sets the brush origin for a device context</span></span>                 |
| [<span data-ttu-id="6fe99-125">**Setdcbrushcolor**</span><span class="sxs-lookup"><span data-stu-id="6fe99-125">**SetDCBrushColor**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setdcbrushcolor)                 | <span data-ttu-id="6fe99-126">Legt die Farbe des aktuellen Gerätekontext Pinsels fest.</span><span class="sxs-lookup"><span data-stu-id="6fe99-126">Sets the current device context brush color.</span></span>               |



 

## <a name="obsolete-functions"></a><span data-ttu-id="6fe99-127">Veraltete Funktionen</span><span class="sxs-lookup"><span data-stu-id="6fe99-127">Obsolete Functions</span></span>

<span data-ttu-id="6fe99-128">Die folgenden Funktionen werden nur aus Gründen der Kompatibilität mit 16-Bit-Versionen von Windows bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="6fe99-128">The following functions are provided only for compatibility with 16-bit versions of Windows.</span></span>

[<span data-ttu-id="6fe99-129">**"Kreatedibpatternbrush"**</span><span class="sxs-lookup"><span data-stu-id="6fe99-129">**CreateDIBPatternBrush**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-createdibpatternbrush)

 

 



