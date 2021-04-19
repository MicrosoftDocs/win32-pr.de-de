---
description: Sperre zum Schutz der Erstellung von Objekten innerhalb des Filters.
ms.assetid: ad1d2584-0d9e-42a8-83ea-0c1907ddcf33
title: 'Cbaserenderer:: m_ObjectCreationLock Member (renbase. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_ObjectCreationLock
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e344b20b4924ac26ebe6253f5388136b350abefe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356056"
---
# <a name="cbaserendererm_objectcreationlock-member"></a><span data-ttu-id="e4ecb-103">Cbaserenderer:: m \_ objectkreationlock-Member</span><span class="sxs-lookup"><span data-stu-id="e4ecb-103">CBaseRenderer::m\_ObjectCreationLock member</span></span>

<span data-ttu-id="e4ecb-104">Sperre zum Schutz der Erstellung von Objekten innerhalb des Filters.</span><span class="sxs-lookup"><span data-stu-id="e4ecb-104">Lock to protect the creation of objects inside the filter.</span></span> <span data-ttu-id="e4ecb-105">Der Filter enthält diese Sperre, wenn er die Eingabe-PIN ([**cbaserenderer:: m \_ pinputpin**](cbaserenderer-m-pinputpin.md)) oder das [**crendererpospassthru**](crendererpospassthru.md) -Objekt ([**cbaserenderer:: m \_ pposition**](cbaserenderer-m-pposition.md)) erstellt.</span><span class="sxs-lookup"><span data-stu-id="e4ecb-105">The filter holds this lock when it creates the input pin ([**CBaseRenderer::m\_pInputPin**](cbaserenderer-m-pinputpin.md)) or the [**CRendererPosPassThru**](crendererpospassthru.md) object ([**CBaseRenderer::m\_pPosition**](cbaserenderer-m-pposition.md)).</span></span> <span data-ttu-id="e4ecb-106">Diese Sperre verhindert, dass mehrere Threads gleichzeitig versuchen, eines dieser Objekte zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="e4ecb-106">This lock prevents multiple threads from attempting to create one of these objects at the same time.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4ecb-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e4ecb-107">Syntax</span></span>


```C++
CCritSec m_ObjectCreationLock;
```



## <a name="requirements"></a><span data-ttu-id="e4ecb-108">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="e4ecb-108">Requirements</span></span>



| <span data-ttu-id="e4ecb-109">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e4ecb-109">Requirement</span></span> | <span data-ttu-id="e4ecb-110">Wert</span><span class="sxs-lookup"><span data-stu-id="e4ecb-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4ecb-111">Header</span><span class="sxs-lookup"><span data-stu-id="e4ecb-111">Header</span></span><br/>  | <dl> <span data-ttu-id="e4ecb-112"><dt>Renbase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e4ecb-112"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e4ecb-113">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e4ecb-113">Library</span></span><br/> | <dl> <span data-ttu-id="e4ecb-114">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="e4ecb-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4ecb-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e4ecb-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4ecb-116">**Cbaserderderer-Klasse**</span><span class="sxs-lookup"><span data-stu-id="e4ecb-116">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




