---
description: Konstruktormethode.
ms.assetid: 35198320-d028-42d4-823f-4f8346d8f977
title: 'Cmediatype. cmediatype-Konstruktor (mtype. h): cmtype-Parameter und PHR-Parameter'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.CMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a40929bb6f53df7ce721e20eefba3019eb71cb0e
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/05/2021
ms.locfileid: "106389064"
---
# <a name="cmediatypecmediatype-constructor-mtypeh"></a><span data-ttu-id="488ce-103">Cmediatype. cmediatype-Konstruktor (mtype. h)</span><span class="sxs-lookup"><span data-stu-id="488ce-103">CMediaType.CMediaType constructor (Mtype.h)</span></span>

<span data-ttu-id="488ce-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="488ce-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="488ce-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="488ce-105">Syntax</span></span>


```C++
CMediaType(
  [ref] const CMediaType &cmtype,
              HRESULT    *phr = NULL
);
```



## <a name="parameters"></a><span data-ttu-id="488ce-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="488ce-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="488ce-107">*cmtype* \[ atur\]</span><span class="sxs-lookup"><span data-stu-id="488ce-107">*cmtype* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="488ce-108">Verweis auf ein- `CMediaType` Objekt.</span><span class="sxs-lookup"><span data-stu-id="488ce-108">Reference to a `CMediaType` object.</span></span> <span data-ttu-id="488ce-109">Der-Konstruktor kopiert den Medientyp in das neue-Objekt, einschließlich des-Format Blocks, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="488ce-109">The constructor copies the media type to the new object, including the format block, if any.</span></span>

</dd> <dt>

<span data-ttu-id="488ce-110">*PHR*</span><span class="sxs-lookup"><span data-stu-id="488ce-110">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="488ce-111">Ein Zeiger auf eine Variable, die einen HRESULT-Wert empfängt.</span><span class="sxs-lookup"><span data-stu-id="488ce-111">Pointer to a variable that receives an HRESULT value.</span></span> <span data-ttu-id="488ce-112">Dieser Parameter kann ein **null** -Zeiger sein.</span><span class="sxs-lookup"><span data-stu-id="488ce-112">This parameter can be a **NULL** pointer.</span></span> <span data-ttu-id="488ce-113">Andernfalls muss der Aufrufer den Wert vor dem \_ Aufrufen des Konstruktors auf S OK festlegen.</span><span class="sxs-lookup"><span data-stu-id="488ce-113">Otherwise, the caller must set the value to S\_OK before calling the constructor.</span></span> <span data-ttu-id="488ce-114">Wenn der Konstruktor fehlschlägt, wird der Wert auf einen Fehlercode festgelegt.</span><span class="sxs-lookup"><span data-stu-id="488ce-114">If the constructor fails, it sets the value to a failure code.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="488ce-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="488ce-115">Remarks</span></span>

<span data-ttu-id="488ce-116">Der Konstruktor ruft die [**cmediatype:: initmediatype**](cmediatype-initmediatype.md) -Methode auf, um den Medientyp zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="488ce-116">The constructor calls the [**CMediaType::InitMediaType**](cmediatype-initmediatype.md) method to initialize the media type.</span></span>

## <a name="requirements"></a><span data-ttu-id="488ce-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="488ce-117">Requirements</span></span>



| <span data-ttu-id="488ce-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="488ce-118">Requirement</span></span> | <span data-ttu-id="488ce-119">Wert</span><span class="sxs-lookup"><span data-stu-id="488ce-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="488ce-120">Header</span><span class="sxs-lookup"><span data-stu-id="488ce-120">Header</span></span><br/>  | <dl> <span data-ttu-id="488ce-121"><dt>Mtype. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="488ce-121"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="488ce-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="488ce-122">Library</span></span><br/> | <dl> <span data-ttu-id="488ce-123">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="488ce-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="488ce-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="488ce-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="488ce-125">**Cmediatype-Klasse**</span><span class="sxs-lookup"><span data-stu-id="488ce-125">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




