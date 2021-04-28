---
description: 'CEnumPins.CEnumPins-Konstruktor : Konstruktormethode.'
ms.assetid: f696e433-b051-4de0-80e5-f9cd31fd0f23
title: CEnumPins.CEnumPins-Konstruktor (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumPins.CEnumPins
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: caa27dfe0190df15be1e41b7128c06249f1ae2b8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099228"
---
# <a name="cenumpinscenumpins-constructor"></a><span data-ttu-id="313ac-103">CEnumPins.CEnumPins-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="313ac-103">CEnumPins.CEnumPins constructor</span></span>

<span data-ttu-id="313ac-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="313ac-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="313ac-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="313ac-105">Syntax</span></span>


```C++
CEnumPins(
   CBaseFilter *pFilter,
   CEnumPins   *pEnumPins
);
```



## <a name="parameters"></a><span data-ttu-id="313ac-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="313ac-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="313ac-107">*pFilter*</span><span class="sxs-lookup"><span data-stu-id="313ac-107">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="313ac-108">Zeiger auf den Filter, für den die Stecknadeln aufzählt werden.</span><span class="sxs-lookup"><span data-stu-id="313ac-108">Pointer to the filter on which to enumerate the pins.</span></span>

</dd> <dt>

<span data-ttu-id="313ac-109">*pEnumPins*</span><span class="sxs-lookup"><span data-stu-id="313ac-109">*pEnumPins*</span></span> 
</dt> <dd>

<span data-ttu-id="313ac-110">Zeiger auf die [**IEnumPins-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) eines zu klonenden Enumerators oder **NULL.**</span><span class="sxs-lookup"><span data-stu-id="313ac-110">Pointer to the [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) interface of an enumerator to clone, or **NULL**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="313ac-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="313ac-111">Remarks</span></span>

<span data-ttu-id="313ac-112">Wenn *pEnumPins* **NULL ist,** initialisiert diese Methode den Enumerator am Anfang der Enumerationssequenz.</span><span class="sxs-lookup"><span data-stu-id="313ac-112">If *pEnumPins* is **NULL**, this method initializes the enumerator to the beginning of the enumeration sequence.</span></span> <span data-ttu-id="313ac-113">Andernfalls wird der interne Zustand des durch *pEnumPins angegebenen Enumerators dupliziert.*</span><span class="sxs-lookup"><span data-stu-id="313ac-113">Otherwise, it duplicates the internal state of the enumerator specified by *pEnumPins*.</span></span>

## <a name="requirements"></a><span data-ttu-id="313ac-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="313ac-114">Requirements</span></span>



| <span data-ttu-id="313ac-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="313ac-115">Requirement</span></span> | <span data-ttu-id="313ac-116">Wert</span><span class="sxs-lookup"><span data-stu-id="313ac-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="313ac-117">Header</span><span class="sxs-lookup"><span data-stu-id="313ac-117">Header</span></span><br/>  | <dl> <span data-ttu-id="313ac-118"><dt>Amfilter.h (streams.h enthalten)</dt></span><span class="sxs-lookup"><span data-stu-id="313ac-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="313ac-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="313ac-119">Library</span></span><br/> | <dl> <span data-ttu-id="313ac-120"><dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="313ac-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="313ac-121">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="313ac-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="313ac-122">**CEnumPins-Klasse**</span><span class="sxs-lookup"><span data-stu-id="313ac-122">**CEnumPins Class**</span></span>](cenumpins.md)
</dt> </dl>

 

 




