---
description: 'CBaseRenderer.CBaseRenderer-Konstruktor : Konstruktormethode.'
ms.assetid: df5efbb3-6bce-4e30-b1b1-d69bf64fa87d
title: CBaseRenderer.CBaseRenderer-Konstruktor (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.CBaseRenderer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 68ebc6255456f0fcbb4bf732a91dce981d0f78ce
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119908"
---
# <a name="cbaserenderercbaserenderer-constructor"></a><span data-ttu-id="cfbc5-103">CBaseRenderer.CBaseRenderer-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="cfbc5-103">CBaseRenderer.CBaseRenderer constructor</span></span>

<span data-ttu-id="cfbc5-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="cfbc5-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="cfbc5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="cfbc5-105">Syntax</span></span>


```C++
CBaseRenderer(
   REFCLSID  RenderClass,
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   HRESULT   *phr,
   UINT      TimerResolution = 1
);
```



## <a name="parameters"></a><span data-ttu-id="cfbc5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="cfbc5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cfbc5-107">*RenderClass*</span><span class="sxs-lookup"><span data-stu-id="cfbc5-107">*RenderClass*</span></span> 
</dt> <dd>

<span data-ttu-id="cfbc5-108">Klassenbezeichner des Renderers.</span><span class="sxs-lookup"><span data-stu-id="cfbc5-108">Class identifier of the renderer.</span></span>

</dd> <dt>

<span data-ttu-id="cfbc5-109">*pName*</span><span class="sxs-lookup"><span data-stu-id="cfbc5-109">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="cfbc5-110">Zeiger auf eine Zeichenfolge, die den Namen des Filters enthält, zu Debugzwecken.</span><span class="sxs-lookup"><span data-stu-id="cfbc5-110">Pointer to a string containing the name of the filter, for debugging purposes.</span></span>

</dd> <dt>

<span data-ttu-id="cfbc5-111">*Punk*</span><span class="sxs-lookup"><span data-stu-id="cfbc5-111">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="cfbc5-112">Zeiger auf den Besitzer dieses Objekts.</span><span class="sxs-lookup"><span data-stu-id="cfbc5-112">Pointer to the owner of this object.</span></span> <span data-ttu-id="cfbc5-113">Wenn das Objekt aggregiert wird, übergeben Sie einen Zeiger auf die **IUnknown-Schnittstelle des aggregierenden** Objekts.</span><span class="sxs-lookup"><span data-stu-id="cfbc5-113">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="cfbc5-114">Legen Sie andernfalls diesen Parameter auf **NULL fest.**</span><span class="sxs-lookup"><span data-stu-id="cfbc5-114">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="cfbc5-115">*Phr*</span><span class="sxs-lookup"><span data-stu-id="cfbc5-115">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="cfbc5-116">Empfängt einen **HRESULT-Wert.**</span><span class="sxs-lookup"><span data-stu-id="cfbc5-116">Receives an **HRESULT** value.</span></span>

</dd> <dt>

<span data-ttu-id="cfbc5-117">*TimerResolution*</span><span class="sxs-lookup"><span data-stu-id="cfbc5-117">*TimerResolution*</span></span> 
</dt> <dd>

<span data-ttu-id="cfbc5-118">Timerauflösung.</span><span class="sxs-lookup"><span data-stu-id="cfbc5-118">Timer resolution.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cfbc5-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cfbc5-119">Requirements</span></span>



| <span data-ttu-id="cfbc5-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cfbc5-120">Requirement</span></span> | <span data-ttu-id="cfbc5-121">Wert</span><span class="sxs-lookup"><span data-stu-id="cfbc5-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cfbc5-122">Header</span><span class="sxs-lookup"><span data-stu-id="cfbc5-122">Header</span></span><br/>  | <dl> <span data-ttu-id="cfbc5-123"><dt>Renbase.h (einschließlich Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="cfbc5-123"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="cfbc5-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="cfbc5-124">Library</span></span><br/> | <dl> <span data-ttu-id="cfbc5-125"><dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="cfbc5-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cfbc5-126">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="cfbc5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfbc5-127">**CBaseRenderer-Klasse**</span><span class="sxs-lookup"><span data-stu-id="cfbc5-127">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




