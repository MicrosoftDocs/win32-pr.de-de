---
description: Diese Funktionen bieten Unterstützung für die Implementierung der IUnknown-Schnittstelle in DirectShow.
ms.assetid: 991e4c69-7d30-4ecf-9ccf-4920452c21d6
title: COM-Hilfsfunktionen (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COM
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9522469ee1aa4f4efa63b4cff6ad73204973a622
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370928"
---
# <a name="com-helper-functions"></a><span data-ttu-id="205e9-103">COM-Hilfsfunktionen</span><span class="sxs-lookup"><span data-stu-id="205e9-103">COM Helper Functions</span></span>

<span data-ttu-id="205e9-104">Diese Funktionen bieten Unterstützung für die Implementierung der **IUnknown** -Schnittstelle in DirectShow.</span><span class="sxs-lookup"><span data-stu-id="205e9-104">These functions provide support for implementing the **IUnknown** interface in DirectShow.</span></span>



| <span data-ttu-id="205e9-105">Funktion</span><span class="sxs-lookup"><span data-stu-id="205e9-105">Function</span></span>                                               | <span data-ttu-id="205e9-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="205e9-106">Description</span></span>                                                           |
|--------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="205e9-107">**\_IUnknown deklarieren**</span><span class="sxs-lookup"><span data-stu-id="205e9-107">**DECLARE\_IUNKNOWN**</span></span>](declare-iunknown.md)          | <span data-ttu-id="205e9-108">Deklariert die drei Methoden der Basisschnittstelle für eine neue Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="205e9-108">Declares the three methods of the base interface for a new interface.</span></span> |
| [<span data-ttu-id="205e9-109">**GetInterface**</span><span class="sxs-lookup"><span data-stu-id="205e9-109">**GetInterface**</span></span>](getinterface.md)                   | <span data-ttu-id="205e9-110">Ruft einen Schnittstellen Zeiger auf den angeforderten Client ab.</span><span class="sxs-lookup"><span data-stu-id="205e9-110">Retrieves an interface pointer to the requested client.</span></span>               |
| [<span data-ttu-id="205e9-111">**Inondelegatingunknown**</span><span class="sxs-lookup"><span data-stu-id="205e9-111">**INonDelegatingUnknown**</span></span>](inondelegatingunknown.md) | <span data-ttu-id="205e9-112">Nicht delegierende Version der **IUnknown** -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="205e9-112">Nondelegating version of the **IUnknown** interface.</span></span>                  |
| [<span data-ttu-id="205e9-113">**LoadOLEAut32**</span><span class="sxs-lookup"><span data-stu-id="205e9-113">**LoadOLEAut32**</span></span>](loadoleaut32.md)                   | <span data-ttu-id="205e9-114">Lädt die Automation-dll (OleAut32.dll).</span><span class="sxs-lookup"><span data-stu-id="205e9-114">Loads the Automation DLL (OleAut32.dll).</span></span>                              |



 

## <a name="requirements"></a><span data-ttu-id="205e9-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="205e9-115">Requirements</span></span>



| <span data-ttu-id="205e9-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="205e9-116">Requirement</span></span> | <span data-ttu-id="205e9-117">Wert</span><span class="sxs-lookup"><span data-stu-id="205e9-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="205e9-118">Header</span><span class="sxs-lookup"><span data-stu-id="205e9-118">Header</span></span><br/>  | <dl> <span data-ttu-id="205e9-119"><dt>ComBase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="205e9-119"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="205e9-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="205e9-120">Library</span></span><br/> | <dl> <span data-ttu-id="205e9-121">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="205e9-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="205e9-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="205e9-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="205e9-123">Hilfsfunktionen</span><span class="sxs-lookup"><span data-stu-id="205e9-123">Utility Functions</span></span>](utility-functions.md)
</dt> </dl>

 

 




