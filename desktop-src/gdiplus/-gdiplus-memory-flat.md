---
description: Windows GDI+ macht eine flache API verfügbar, die aus etwa 600 Funktionen besteht. Diese flachen API-Funktionen werden von der C++-Klasse GdiplusBase umschlossen.
ms.assetid: b4fcc02c-1b0f-4731-8312-29894b1f722f
title: Arbeitsspeicherfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ed10574f9cc88c5b7ca8a2b0ed09924fe8c5192
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395825"
---
# <a name="memory-functions"></a><span data-ttu-id="4fd94-104">Arbeitsspeicherfunktionen</span><span class="sxs-lookup"><span data-stu-id="4fd94-104">Memory Functions</span></span>

<span data-ttu-id="4fd94-105">Windows GDI+ macht eine flache API verfügbar, die aus etwa 600 Funktionen besteht, die in Gdiplus.dll implementiert und in Gdiplusflat.h deklariert werden.</span><span class="sxs-lookup"><span data-stu-id="4fd94-105">Windows GDI+ exposes a flat API that consists of about 600 functions, which are implemented in Gdiplus.dll and declared in Gdiplusflat.h.</span></span> <span data-ttu-id="4fd94-106">Die Funktionen in der flachen GDI+-API werden von einer Sammlung von etwa 40 C++-Klassen umschlossen.</span><span class="sxs-lookup"><span data-stu-id="4fd94-106">The functions in the GDI+ flat API are wrapped by a collection of about 40 C++ classes.</span></span> <span data-ttu-id="4fd94-107">Es wird empfohlen, die Funktionen in der flachen API nicht direkt aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="4fd94-107">It is recommended that you do not directly call the functions in the flat API.</span></span> <span data-ttu-id="4fd94-108">Wenn Sie GDI+ aufrufen, sollten Sie dazu die Methoden und Funktionen aufrufen, die von den C++-Wrappern bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="4fd94-108">Whenever you make calls to GDI+, you should do so by calling the methods and functions provided by the C++ wrappers.</span></span> <span data-ttu-id="4fd94-109">Microsoft Product Support Services bietet keine Unterstützung für Code, der die flache API direkt aufruft.</span><span class="sxs-lookup"><span data-stu-id="4fd94-109">Microsoft Product Support Services will not provide support for code that calls the flat API directly.</span></span> <span data-ttu-id="4fd94-110">Weitere Informationen zur Verwendung dieser Wrappermethoden finden Sie unter [GDI+ Flat API](-gdiplus-flatapi-flat.md).</span><span class="sxs-lookup"><span data-stu-id="4fd94-110">For more information on using these wrapper methods, see [GDI+ Flat API](-gdiplus-flatapi-flat.md).</span></span>

<span data-ttu-id="4fd94-111">Die folgenden flachen API-Funktionen werden von der C++-Klasse [**GdiplusBase**](/windows/desktop/api/gdiplusbase/nl-gdiplusbase-gdiplusbase) umschlossen.</span><span class="sxs-lookup"><span data-stu-id="4fd94-111">The following flat API functions are wrapped by the [**GdiplusBase**](/windows/desktop/api/gdiplusbase/nl-gdiplusbase-gdiplusbase) C++ class.</span></span>

## <a name="memory-functions-and-corresponding-wrapper-methods"></a><span data-ttu-id="4fd94-112">Speicherfunktionen und entsprechende Wrappermethoden</span><span class="sxs-lookup"><span data-stu-id="4fd94-112">Memory Functions and Corresponding Wrapper Methods</span></span>



| <span data-ttu-id="4fd94-113">Flat-Funktion</span><span class="sxs-lookup"><span data-stu-id="4fd94-113">Flat function</span></span>                                          | <span data-ttu-id="4fd94-114">Wrappermethode</span><span class="sxs-lookup"><span data-stu-id="4fd94-114">Wrapper method</span></span>                                                                                                                                      | <span data-ttu-id="4fd94-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4fd94-115">Remarks</span></span>                                                                                                      |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4fd94-116">GpStatus WINGDIPAPI GdipAlloc(size \_ t size)</span><span class="sxs-lookup"><span data-stu-id="4fd94-116">GpStatus WINGDIPAPI GdipAlloc(size\_t size)</span></span><br/> | [<span data-ttu-id="4fd94-117">**GpStatus WINGDIPAPI GdiplusBase void \* (operator new)(size \_ t in \_ size)**</span><span class="sxs-lookup"><span data-stu-id="4fd94-117">**GpStatus WINGDIPAPI GdiplusBase void\* (operator new)(size\_t in\_size)**</span></span>](/windows/win32/api/gdiplusbase/nf-gdiplusbase-gdiplusbase-operatornew)<br/>      | <span data-ttu-id="4fd94-118">Belegt Arbeitsspeicher für ein Windows GDI+-Objekt.</span><span class="sxs-lookup"><span data-stu-id="4fd94-118">Allocates memory for one Windows GDI+ object.</span></span> <br/> <span data-ttu-id="4fd94-119">GdipAlloc wird in GdiplusMem.h deklariert.</span><span class="sxs-lookup"><span data-stu-id="4fd94-119">GdipAlloc is declared in GdiplusMem.h.</span></span><br/>  |
| <span data-ttu-id="4fd94-120">GpStatus WINGDIPAPI GdipFree(void \* ptr);</span><span class="sxs-lookup"><span data-stu-id="4fd94-120">GpStatus WINGDIPAPI GdipFree(void\* ptr);</span></span><br/>   | [<span data-ttu-id="4fd94-121">**GpStatus WINGDIPAPI GdiplusBase void (operator delete)(void \* in \_ pVoid)**</span><span class="sxs-lookup"><span data-stu-id="4fd94-121">**GpStatus WINGDIPAPI GdiplusBase void (operator delete)(void\* in\_pVoid)**</span></span>](/windows/win32/api/gdiplusbase/nf-gdiplusbase-gdiplusbase-operatordelete)<br/> | <span data-ttu-id="4fd94-122">Hebt die Speicherbeteilung für ein Windows GDI+-Objekt auf.</span><span class="sxs-lookup"><span data-stu-id="4fd94-122">Deallocates memory for one Windows GDI+ object.</span></span> <br/> <span data-ttu-id="4fd94-123">GdipFree wird in GdiplusMem.h deklariert.</span><span class="sxs-lookup"><span data-stu-id="4fd94-123">GdipFree is declared in GdiplusMem.h.</span></span><br/> |



 

 

 
