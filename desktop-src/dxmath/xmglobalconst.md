---
description: Deklariert ein Objekt als eine pick-any-Konstante, um redundante Neuladungen dieses Objekts zu vermeiden, wenn es an mehreren Stellen in der directxmath-Bibliothek verwendet (und deklariert) wird.
ms.assetid: FDE5C004-9E8E-4890-8FDC-987C1569D8E5
title: Xmglobalconst-Makro
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6675b17138fca66e293321a9d848262a8bffc94e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106355575"
---
# <a name="xmglobalconst-macro"></a><span data-ttu-id="9f3a2-103">Xmglobalconst-Makro</span><span class="sxs-lookup"><span data-stu-id="9f3a2-103">XMGLOBALCONST macro</span></span>

<span data-ttu-id="9f3a2-104">Deklariert ein Objekt als eine *pick-any-* Konstante, um redundante Neuladungen dieses Objekts zu vermeiden, wenn es an mehreren Stellen in der directxmath-Bibliothek verwendet (und deklariert) wird.</span><span class="sxs-lookup"><span data-stu-id="9f3a2-104">Declares an object to be a *pick-any* constant, to avoid redundant reloads of that object if it is used (and declared) in multiple places in the DirectXMath Library.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f3a2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9f3a2-105">Syntax</span></span>

``` syntax
#define XMGLOBALCONST  extern const __declspec(selectany)
```

## <a name="remarks"></a><span data-ttu-id="9f3a2-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9f3a2-106">Remarks</span></span>

<span data-ttu-id="9f3a2-107">Die Verwendung von xmglobalconst ermöglicht die Angabe von globalen Konstanten.</span><span class="sxs-lookup"><span data-stu-id="9f3a2-107">Using XMGLOBALCONST permits the specification of global constants.</span></span> <span data-ttu-id="9f3a2-108">Dies trägt dazu bei, die Größe des Datensegments einer Anwendung zu reduzieren, eine redundante Objekt Erstellung und-Zerstörung zu vermeiden und Lade-und Speichervorgänge zu verringern.</span><span class="sxs-lookup"><span data-stu-id="9f3a2-108">This helps to reduce the size of an application's data segment, avoid redundant object creation and destruction, and reduce load and store operations.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f3a2-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9f3a2-109">Requirements</span></span>

<span data-ttu-id="9f3a2-110">**Header:** Deklariert in "directxmath. h".</span><span class="sxs-lookup"><span data-stu-id="9f3a2-110">**Header:** Declared in DirectXMath.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9f3a2-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9f3a2-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9f3a2-112">Directxmath-Bibliotheks Makros</span><span class="sxs-lookup"><span data-stu-id="9f3a2-112">DirectXMath Library Macros</span></span>](ovw-xnamath-reference-macros.md)
</dt> <dt>

[<span data-ttu-id="9f3a2-113">Globale Konstanten in der directxmath-Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9f3a2-113">Global Constants in the DirectXMath Library</span></span>](pg-xnamath-internals.md)
</dt> <dt>

<span data-ttu-id="9f3a2-114">[selectany](/previous-versions/visualstudio/visual-studio-6.0/aa273550(v=vs.60))</span><span class="sxs-lookup"><span data-stu-id="9f3a2-114">[selectany](/previous-versions/visualstudio/visual-studio-6.0/aa273550(v=vs.60))</span></span>
</dt> <dt>

<span data-ttu-id="9f3a2-115">[declspec](/previous-versions/visualstudio/visual-studio-6.0/aa273692(v=vs.60))</span><span class="sxs-lookup"><span data-stu-id="9f3a2-115">[declspec](/previous-versions/visualstudio/visual-studio-6.0/aa273692(v=vs.60))</span></span>
</dt> </dl>

 

 
