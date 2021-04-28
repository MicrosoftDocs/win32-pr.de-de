---
description: 'CBaseVideoRenderer.CBaseVideoRenderer-Konstruktor : Konstruktormethode.'
ms.assetid: 9b69632b-7932-4a9b-bd68-69b06dd8a5ec
title: CBaseVideoRenderer.CBaseVideoRenderer-Konstruktor (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.CBaseVideoRenderer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c0ae558238b94402150e5cb15373d202065e485e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095838"
---
# <a name="cbasevideorenderercbasevideorenderer-constructor"></a><span data-ttu-id="cd99b-103">CBaseVideoRenderer.CBaseVideoRenderer-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="cd99b-103">CBaseVideoRenderer.CBaseVideoRenderer constructor</span></span>

<span data-ttu-id="cd99b-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="cd99b-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd99b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="cd99b-105">Syntax</span></span>


```C++
CBaseVideoRenderer(
   REFCLSID  RenderClass,
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="cd99b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="cd99b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd99b-107">*RenderClass*</span><span class="sxs-lookup"><span data-stu-id="cd99b-107">*RenderClass*</span></span> 
</dt> <dd>

<span data-ttu-id="cd99b-108">Klassenbezeichner für diesen Renderer.</span><span class="sxs-lookup"><span data-stu-id="cd99b-108">Class identifier for this renderer.</span></span>

</dd> <dt>

<span data-ttu-id="cd99b-109">*pName*</span><span class="sxs-lookup"><span data-stu-id="cd99b-109">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="cd99b-110">Zeiger auf eine Beschreibung, die zu Debugzwecken verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="cd99b-110">Pointer to a description used for debugging purposes.</span></span>

</dd> <dt>

<span data-ttu-id="cd99b-111">*Punk*</span><span class="sxs-lookup"><span data-stu-id="cd99b-111">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="cd99b-112">Zeiger auf das aggregierte Besitzerobjekt.</span><span class="sxs-lookup"><span data-stu-id="cd99b-112">Pointer to the aggregated owner object.</span></span>

</dd> <dt>

<span data-ttu-id="cd99b-113">*Phr*</span><span class="sxs-lookup"><span data-stu-id="cd99b-113">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="cd99b-114">Zeiger auf einen **HRESULT-Wert.**</span><span class="sxs-lookup"><span data-stu-id="cd99b-114">Pointer to an **HRESULT** value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cd99b-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cd99b-115">Requirements</span></span>



| <span data-ttu-id="cd99b-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cd99b-116">Requirement</span></span> | <span data-ttu-id="cd99b-117">Wert</span><span class="sxs-lookup"><span data-stu-id="cd99b-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd99b-118">Header</span><span class="sxs-lookup"><span data-stu-id="cd99b-118">Header</span></span><br/>  | <dl> <span data-ttu-id="cd99b-119"><dt>Renbase.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="cd99b-119"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="cd99b-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="cd99b-120">Library</span></span><br/> | <dl> <span data-ttu-id="cd99b-121"><dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="cd99b-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd99b-122">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="cd99b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd99b-123">**CBaseVideoRenderer-Klasse**</span><span class="sxs-lookup"><span data-stu-id="cd99b-123">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




