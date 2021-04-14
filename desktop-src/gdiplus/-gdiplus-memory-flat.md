---
description: Windows GDI+ macht eine flache API verfügbar, die aus ungefähr 600 Funktionen besteht, die in Gdiplus.dll implementiert und in "Gdiplus. h" deklariert sind.
ms.assetid: b4fcc02c-1b0f-4731-8312-29894b1f722f
title: Speicherfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86e748f8a68cc6f04deba3c9676638ee48ee2e86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978985"
---
# <a name="memory-functions"></a><span data-ttu-id="23d60-103">Speicherfunktionen</span><span class="sxs-lookup"><span data-stu-id="23d60-103">Memory Functions</span></span>

<span data-ttu-id="23d60-104">Windows GDI+ macht eine flache API verfügbar, die aus ungefähr 600 Funktionen besteht, die in Gdiplus.dll implementiert und in "Gdiplus. h" deklariert sind.</span><span class="sxs-lookup"><span data-stu-id="23d60-104">Windows GDI+ exposes a flat API that consists of about 600 functions, which are implemented in Gdiplus.dll and declared in Gdiplusflat.h.</span></span> <span data-ttu-id="23d60-105">Die Funktionen in der flatapi GDI+ werden von einer Sammlung von ungefähr 40 C++-Klassen umschließt.</span><span class="sxs-lookup"><span data-stu-id="23d60-105">The functions in the GDI+ flat API are wrapped by a collection of about 40 C++ classes.</span></span> <span data-ttu-id="23d60-106">Es wird empfohlen, die Funktionen in der flatapi nicht direkt aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="23d60-106">It is recommended that you do not directly call the functions in the flat API.</span></span> <span data-ttu-id="23d60-107">Wenn Sie GDI+ aufrufen, sollten Sie dies tun, indem Sie die Methoden und Funktionen aufrufen, die von den C++-Wrappern bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="23d60-107">Whenever you make calls to GDI+, you should do so by calling the methods and functions provided by the C++ wrappers.</span></span> <span data-ttu-id="23d60-108">Der Microsoft-Produktsupport bietet keine Unterstützung für Code, mit dem die flatapi direkt aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="23d60-108">Microsoft Product Support Services will not provide support for code that calls the flat API directly.</span></span> <span data-ttu-id="23d60-109">Weitere Informationen zur Verwendung dieser Wrapper Methoden finden Sie unter [GDI+ Flat API](-gdiplus-flatapi-flat.md).</span><span class="sxs-lookup"><span data-stu-id="23d60-109">For more information on using these wrapper methods, see [GDI+ Flat API](-gdiplus-flatapi-flat.md).</span></span>

<span data-ttu-id="23d60-110">Die folgenden flatapi-Funktionen werden von der [**gdiplus Base**](/windows/desktop/api/gdiplusbase/nl-gdiplusbase-gdiplusbase) C++-Klasse umschließt.</span><span class="sxs-lookup"><span data-stu-id="23d60-110">The following flat API functions are wrapped by the [**GdiplusBase**](/windows/desktop/api/gdiplusbase/nl-gdiplusbase-gdiplusbase) C++ class.</span></span>

## <a name="memory-functions-and-corresponding-wrapper-methods"></a><span data-ttu-id="23d60-111">Speicherfunktionen und entsprechende Wrapper Methoden</span><span class="sxs-lookup"><span data-stu-id="23d60-111">Memory Functions and Corresponding Wrapper Methods</span></span>



| <span data-ttu-id="23d60-112">Flat-Funktion</span><span class="sxs-lookup"><span data-stu-id="23d60-112">Flat function</span></span>                                          | <span data-ttu-id="23d60-113">Wrapper Methode</span><span class="sxs-lookup"><span data-stu-id="23d60-113">Wrapper method</span></span>                                                                                                                                      | <span data-ttu-id="23d60-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="23d60-114">Remarks</span></span>                                                                                                      |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23d60-115">Gpstatus wingdipapi gdipalloc (Größe \_ t-Größe)</span><span class="sxs-lookup"><span data-stu-id="23d60-115">GpStatus WINGDIPAPI GdipAlloc(size\_t size)</span></span><br/> | [<span data-ttu-id="23d60-116">**Gpstatus wingdipapi gdiplusbase void \* (Operator new) (Größe \_ t in \_ Größe)**</span><span class="sxs-lookup"><span data-stu-id="23d60-116">**GpStatus WINGDIPAPI GdiplusBase void\* (operator new)(size\_t in\_size)**</span></span>](/windows/win32/api/gdiplusbase/nf-gdiplusbase-gdiplusbase-operatornew)<br/>      | <span data-ttu-id="23d60-117">Belegt Speicher für ein Windows-GDI+-Objekt.</span><span class="sxs-lookup"><span data-stu-id="23d60-117">Allocates memory for one Windows GDI+ object.</span></span> <br/> <span data-ttu-id="23d60-118">Gdipalloc ist in "gdipl. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="23d60-118">GdipAlloc is declared in GdiplusMem.h.</span></span><br/>  |
| <span data-ttu-id="23d60-119">Gpstatus wingdipapi gdipfree (void \* PTR);</span><span class="sxs-lookup"><span data-stu-id="23d60-119">GpStatus WINGDIPAPI GdipFree(void\* ptr);</span></span><br/>   | [<span data-ttu-id="23d60-120">**Gpstatus wingdipapi gdiplusbase void (Operator Delete) (void \* in \_ pVoid)**</span><span class="sxs-lookup"><span data-stu-id="23d60-120">**GpStatus WINGDIPAPI GdiplusBase void (operator delete)(void\* in\_pVoid)**</span></span>](/windows/win32/api/gdiplusbase/nf-gdiplusbase-gdiplusbase-operatordelete)<br/> | <span data-ttu-id="23d60-121">Hebt die Zuordnung von Arbeitsspeicher für ein Windows-GDI+-Objekt auf.</span><span class="sxs-lookup"><span data-stu-id="23d60-121">Deallocates memory for one Windows GDI+ object.</span></span> <br/> <span data-ttu-id="23d60-122">Gdipfree ist in "gdipl. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="23d60-122">GdipFree is declared in GdiplusMem.h.</span></span><br/> |



 

 

 
