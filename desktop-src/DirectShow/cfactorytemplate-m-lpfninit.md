---
description: Ein Zeiger auf eine Funktion, die vom DLL-Einstiegspunkt aufgerufen wird. Kann den Wert NULL haben.
ms.assetid: 0769f55b-6f0d-4a89-9d3f-64f211426342
title: 'Cfactoriytemplate:: m_lpfnInit Member (ComBase. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_lpfnInit
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b44181f926f77ecc7cc22673622d4a0d3dcb7d26
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365508"
---
# <a name="cfactorytemplatem_lpfninit-member"></a><span data-ttu-id="c5af1-104">Cfactoriytemplate:: m \_ lpfninit-Member</span><span class="sxs-lookup"><span data-stu-id="c5af1-104">CFactoryTemplate::m\_lpfnInit member</span></span>

<span data-ttu-id="c5af1-105">Ein Zeiger auf eine Funktion, die vom DLL-Einstiegspunkt aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="c5af1-105">Pointer to a function that gets called from the DLL entry point.</span></span> <span data-ttu-id="c5af1-106">Kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="c5af1-106">Can be **NULL**.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5af1-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c5af1-107">Syntax</span></span>


```C++
LPFNInitRoutine m_lpfnInit;
```



## <a name="remarks"></a><span data-ttu-id="c5af1-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c5af1-108">Remarks</span></span>

<span data-ttu-id="c5af1-109">Der Funktions Zeigertyp ist " [**lpfninitroutine**](lpfninitroutine.md)".</span><span class="sxs-lookup"><span data-stu-id="c5af1-109">The function pointer type is [**LPFNInitRoutine**](lpfninitroutine.md).</span></span> <span data-ttu-id="c5af1-110">Wenn Sie diese Funktion in der DLL bereitstellen, ruft die DLL-Einstiegspunkt Funktion Sie mit den folgenden Parametern auf:</span><span class="sxs-lookup"><span data-stu-id="c5af1-110">If you provide this function in your DLL, the DLL entry-point function calls it with following parameters:</span></span>

-   <span data-ttu-id="c5af1-111">*bloading*: **true** , wenn die dll geladen wird, **false** , wenn die DLL entladen wird.</span><span class="sxs-lookup"><span data-stu-id="c5af1-111">*bLoading*: **TRUE** when the DLL is loaded, **FALSE** when the DLL is unloaded.</span></span>
-   <span data-ttu-id="c5af1-112">*rclsid*: Zeiger auf das CLISD des Objekts, das in der [**cfactorytemplate:: m \_ CLSID**](cfactorytemplate-m-clsid.md) -Element Variablen angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="c5af1-112">*rclsid*: Pointer to the object's CLISD, specified in the [**CFactoryTemplate::m\_ClsID**](cfactorytemplate-m-clsid.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5af1-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c5af1-113">Requirements</span></span>



| <span data-ttu-id="c5af1-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c5af1-114">Requirement</span></span> | <span data-ttu-id="c5af1-115">Wert</span><span class="sxs-lookup"><span data-stu-id="c5af1-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5af1-116">Header</span><span class="sxs-lookup"><span data-stu-id="c5af1-116">Header</span></span><br/>  | <dl> <span data-ttu-id="c5af1-117"><dt>ComBase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c5af1-117"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c5af1-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c5af1-118">Library</span></span><br/> | <dl> <span data-ttu-id="c5af1-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="c5af1-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5af1-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c5af1-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5af1-121">**Cfactorytemplate-Klasse**</span><span class="sxs-lookup"><span data-stu-id="c5af1-121">**CFactoryTemplate Class**</span></span>](cfactorytemplate.md)
</dt> </dl>

 

 




