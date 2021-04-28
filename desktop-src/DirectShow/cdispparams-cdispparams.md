---
description: CDispParams.CDispParams-Konstruktor – Konstruktormethode.
ms.assetid: da67a5e4-b4a1-4a38-93fe-0965695e93f5
title: CDispParams.CDispParams-Konstruktor (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDispParams.CDispParams
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 42f55a57a0f9e06d3001c2638d457fe0b82a914d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095788"
---
# <a name="cdispparamscdispparams-constructor"></a><span data-ttu-id="4948a-103">CDispParams.CDispParams-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="4948a-103">CDispParams.CDispParams constructor</span></span>

<span data-ttu-id="4948a-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="4948a-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4948a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4948a-105">Syntax</span></span>


```C++
CDispParams(
   UINT    nArgs,
   VARIANT *pArgs
);
```



## <a name="parameters"></a><span data-ttu-id="4948a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4948a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4948a-107">*nArgs*</span><span class="sxs-lookup"><span data-stu-id="4948a-107">*nArgs*</span></span> 
</dt> <dd>

<span data-ttu-id="4948a-108">Anzahl von Argumenten, die an die Methode oder Eigenschaft übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="4948a-108">Number of arguments passed to the method or property.</span></span>

</dd> <dt>

<span data-ttu-id="4948a-109">*pArgs*</span><span class="sxs-lookup"><span data-stu-id="4948a-109">*pArgs*</span></span> 
</dt> <dd>

<span data-ttu-id="4948a-110">Zeiger auf die Liste der Argumente.</span><span class="sxs-lookup"><span data-stu-id="4948a-110">Pointer to the list of arguments.</span></span> <span data-ttu-id="4948a-111">In der Liste wird jedes Argument mit seinem Variant-Typ gespeichert.</span><span class="sxs-lookup"><span data-stu-id="4948a-111">In the list, each argument is stored with its variant type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4948a-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4948a-112">Requirements</span></span>



| <span data-ttu-id="4948a-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4948a-113">Requirement</span></span> | <span data-ttu-id="4948a-114">Wert</span><span class="sxs-lookup"><span data-stu-id="4948a-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4948a-115">Header</span><span class="sxs-lookup"><span data-stu-id="4948a-115">Header</span></span><br/>  | <dl> <span data-ttu-id="4948a-116"><dt>Ctlutil.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="4948a-116"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4948a-117">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4948a-117">Library</span></span><br/> | <dl> <span data-ttu-id="4948a-118"><dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="4948a-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4948a-119">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4948a-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4948a-120">**CDispParams-Klasse**</span><span class="sxs-lookup"><span data-stu-id="4948a-120">**CDispParams Class**</span></span>](cdispparams.md)
</dt> </dl>

 

 




