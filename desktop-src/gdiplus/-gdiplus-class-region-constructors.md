---
description: In diesem Thema werden die Konstruktoren der Regions Klasse aufgelistet. Eine komplette Klassen Auflistung finden Sie unter Region-Klasse.
ms.assetid: 94f4971c-defa-43e0-a0c0-4000557b0a5c
title: Region. Region-Konstruktoren
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name: ''
api_type:
- NA
api_location: ''
ms.openlocfilehash: 98663587fab3722d689c9d34578d60daad922a2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131365"
---
# <a name="regionregion-constructors"></a><span data-ttu-id="3cc15-104">Region. Region-Konstruktoren</span><span class="sxs-lookup"><span data-stu-id="3cc15-104">Region.Region constructors</span></span>

<span data-ttu-id="3cc15-105">In diesem Thema werden die Konstruktoren der [**Regions**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-region) Klasse aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="3cc15-105">This topic lists the constructors of the [**Region**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-region) class.</span></span> <span data-ttu-id="3cc15-106">Eine komplette Klassen Auflistung finden Sie unter **Region-Klasse**.</span><span class="sxs-lookup"><span data-stu-id="3cc15-106">For a complete class listing, see **Region Class**.</span></span>

### <a name="overload-list"></a><span data-ttu-id="3cc15-107">Überladeliste</span><span class="sxs-lookup"><span data-stu-id="3cc15-107">Overload list</span></span>



| <span data-ttu-id="3cc15-108">Konstruktor</span><span class="sxs-lookup"><span data-stu-id="3cc15-108">Constructor</span></span>                                                                 | <span data-ttu-id="3cc15-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3cc15-109">Description</span></span>                                                                                                                                                                                      |
|:----------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3cc15-110">[**Region (hrgn)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(inhrgn))</span><span class="sxs-lookup"><span data-stu-id="3cc15-110">[**Region(HRGN)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(inhrgn))</span></span>                  | <span data-ttu-id="3cc15-111">Erstellt einen Bereich, der mit dem Bereich identisch ist, der durch ein Handle für einen GDI-Bereich angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="3cc15-111">Creates a region that is identical to the region that is specified by a handle to a GDI region.</span></span><br/>                                                                                       |
| <span data-ttu-id="3cc15-112">[**Region (Rect&)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(inconstrect_))</span><span class="sxs-lookup"><span data-stu-id="3cc15-112">[**Region(Rect&)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(inconstrect_))</span></span>            | <span data-ttu-id="3cc15-113">Erstellt einen Bereich, der durch ein Rechteck definiert wird.</span><span class="sxs-lookup"><span data-stu-id="3cc15-113">Creates a region that is defined by a rectangle.</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="3cc15-114">[**Region (RectF&)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(inconstrectf_))</span><span class="sxs-lookup"><span data-stu-id="3cc15-114">[**Region(RectF&)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(inconstrectf_))</span></span>          | <span data-ttu-id="3cc15-115">Erstellt einen Bereich, der durch ein Rechteck definiert wird.</span><span class="sxs-lookup"><span data-stu-id="3cc15-115">Creates a region that is defined by a rectangle.</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="3cc15-116">[**Region (Byte \* , int)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(inconstbyte_inint))</span><span class="sxs-lookup"><span data-stu-id="3cc15-116">[**Region(BYTE\*,INT)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(inconstbyte_inint))</span></span> | <span data-ttu-id="3cc15-117">Erstellt einen Bereich, der durch Daten aus einer anderen Region definiert wird.</span><span class="sxs-lookup"><span data-stu-id="3cc15-117">Creates a region that is defined by data obtained from another region.</span></span> <br/>                                                                                                               |
| <span data-ttu-id="3cc15-118">[**Region (GraphicsPath \* )**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(inconstgraphicspath))</span><span class="sxs-lookup"><span data-stu-id="3cc15-118">[**Region(GraphicsPath\*)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(inconstgraphicspath))</span></span>        | <span data-ttu-id="3cc15-119">Erstellt einen Bereich, der durch einen Pfad (ein [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) -Objekt) definiert ist und über einen im **GraphicsPath** -Objekt enthaltenen Füllmodus verfügt.</span><span class="sxs-lookup"><span data-stu-id="3cc15-119">Creates a region that is defined by a path (a [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) object) and has a fill mode that is contained in the **GraphicsPath** object.</span></span><br/> |
| <span data-ttu-id="3cc15-120">[**Region ()**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(constregion_))</span><span class="sxs-lookup"><span data-stu-id="3cc15-120">[**Region()**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(constregion_))</span></span>                           | <span data-ttu-id="3cc15-121">Erstellt einen Bereich, der unendlich ist.</span><span class="sxs-lookup"><span data-stu-id="3cc15-121">Creates a region that is infinite.</span></span> <span data-ttu-id="3cc15-122">Dies ist der Standardkonstruktor</span><span class="sxs-lookup"><span data-stu-id="3cc15-122">This is the default constructor.</span></span> <br/>                                                                                                                  |



 

 
