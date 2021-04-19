---
description: Handle für die Modul Instanz.
ms.assetid: ad889ebe-2bd8-4456-9517-9e2909697a02
title: 'Cbasewindow:: m_hInstance Member (winutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_hInstance
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6482aac80c1298ea403019f43ddc4effdc30b00a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373663"
---
# <a name="cbasewindowm_hinstance-member"></a><span data-ttu-id="2d27c-103">Cbasewindow:: m \_ HINSTANCE-Member</span><span class="sxs-lookup"><span data-stu-id="2d27c-103">CBaseWindow::m\_hInstance member</span></span>

<span data-ttu-id="2d27c-104">Handle für die Modul Instanz.</span><span class="sxs-lookup"><span data-stu-id="2d27c-104">Handle to the module instance.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d27c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2d27c-105">Syntax</span></span>


```C++
HINSTANCE m_hInstance;
```



## <a name="remarks"></a><span data-ttu-id="2d27c-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2d27c-106">Remarks</span></span>

<span data-ttu-id="2d27c-107">Die Funktion "DLL-Einstiegspunkt" legt eine globale Variable mit einem Handle für die Modul Instanz fest.</span><span class="sxs-lookup"><span data-stu-id="2d27c-107">The DLL entry point function sets a global variable with a handle to the module instance.</span></span> <span data-ttu-id="2d27c-108">Die **cbasewindow** -Klasse speichert dieses Handle in seiner Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="2d27c-108">The **CBaseWindow** class stores this handle in its constructor method.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d27c-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2d27c-109">Requirements</span></span>



| <span data-ttu-id="2d27c-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2d27c-110">Requirement</span></span> | <span data-ttu-id="2d27c-111">Wert</span><span class="sxs-lookup"><span data-stu-id="2d27c-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d27c-112">Header</span><span class="sxs-lookup"><span data-stu-id="2d27c-112">Header</span></span><br/>  | <dl> <span data-ttu-id="2d27c-113"><dt>Winutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2d27c-113"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2d27c-114">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2d27c-114">Library</span></span><br/> | <dl> <span data-ttu-id="2d27c-115">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="2d27c-115"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d27c-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2d27c-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d27c-117">**Cbasewindow-Klasse**</span><span class="sxs-lookup"><span data-stu-id="2d27c-117">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




