---
description: 'CRendererPosPassThru.CRendererPosPassThru-Konstruktor : Konstruktormethode.'
ms.assetid: 9d6f40ee-31bf-4334-bee5-4be834f1f269
title: CRendererPosPassThru.CRendererPosPassThru-Konstruktor (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererPosPassThru.CRendererPosPassThru
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 59972f12f0f746ef68c267e3fbd0d071d54193c3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085408"
---
# <a name="crendererpospassthrucrendererpospassthru-constructor"></a><span data-ttu-id="0ab1b-103">CRendererPosPassThru.CRendererPosPassThru-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="0ab1b-103">CRendererPosPassThru.CRendererPosPassThru constructor</span></span>

<span data-ttu-id="0ab1b-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="0ab1b-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ab1b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0ab1b-105">Syntax</span></span>


```C++
CRendererPosPassThru(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         HRESULT   *phr,
         IPin      *pPin
);
```



## <a name="parameters"></a><span data-ttu-id="0ab1b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0ab1b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ab1b-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="0ab1b-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="0ab1b-108">Zeiger auf den Namen des Objekts zu Debugzwecken.</span><span class="sxs-lookup"><span data-stu-id="0ab1b-108">Pointer to the name of the object, for debugging purposes.</span></span> <span data-ttu-id="0ab1b-109">Ordnen Sie diesen Parameter im statischen Speicher zu.</span><span class="sxs-lookup"><span data-stu-id="0ab1b-109">Allocate this parameter in static memory.</span></span>

</dd> <dt>

<span data-ttu-id="0ab1b-110">*Punk*</span><span class="sxs-lookup"><span data-stu-id="0ab1b-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="0ab1b-111">Zeiger auf den Besitzer dieses Objekts.</span><span class="sxs-lookup"><span data-stu-id="0ab1b-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="0ab1b-112">Wenn das Objekt aggregiert wird, übergeben Sie einen Zeiger auf die **IUnknown-Schnittstelle** des aggregierenden Objekts.</span><span class="sxs-lookup"><span data-stu-id="0ab1b-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="0ab1b-113">Legen Sie andernfalls diesen Parameter auf **NULL** fest.</span><span class="sxs-lookup"><span data-stu-id="0ab1b-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="0ab1b-114">*Phr*</span><span class="sxs-lookup"><span data-stu-id="0ab1b-114">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="0ab1b-115">Zeiger auf einen **HRESULT-Wert.**</span><span class="sxs-lookup"><span data-stu-id="0ab1b-115">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="0ab1b-116">Ignoriert.</span><span class="sxs-lookup"><span data-stu-id="0ab1b-116">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="0ab1b-117">*pPin*</span><span class="sxs-lookup"><span data-stu-id="0ab1b-117">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="0ab1b-118">Zeiger auf die [**IPin-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ipin) des Eingabepins des Filters.</span><span class="sxs-lookup"><span data-stu-id="0ab1b-118">Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the filter's input pin.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0ab1b-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0ab1b-119">Requirements</span></span>



| <span data-ttu-id="0ab1b-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0ab1b-120">Requirement</span></span> | <span data-ttu-id="0ab1b-121">Wert</span><span class="sxs-lookup"><span data-stu-id="0ab1b-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ab1b-122">Header</span><span class="sxs-lookup"><span data-stu-id="0ab1b-122">Header</span></span><br/>  | <dl> <span data-ttu-id="0ab1b-123"><dt>Ctlutil.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="0ab1b-123"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0ab1b-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0ab1b-124">Library</span></span><br/> | <dl> <span data-ttu-id="0ab1b-125"><dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="0ab1b-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




