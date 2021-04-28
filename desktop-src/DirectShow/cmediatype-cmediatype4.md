---
description: 'CMediaType.CMediaType-Konstruktor (Mtype.h): Konstruktormethode.'
ms.assetid: 35198320-d028-42d4-823f-4f8346d8f977
title: CMediaType.CMediaType-Konstruktor (Mtype.h) – cmtype- und phr-Parameter
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
ms.openlocfilehash: dd91252920c74d45e4218be3c3d03249a116bfcf
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095418"
---
# <a name="cmediatypecmediatype-constructor-mtypeh"></a><span data-ttu-id="4b675-103">CMediaType.CMediaType-Konstruktor (Mtype.h)</span><span class="sxs-lookup"><span data-stu-id="4b675-103">CMediaType.CMediaType constructor (Mtype.h)</span></span>

<span data-ttu-id="4b675-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="4b675-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b675-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4b675-105">Syntax</span></span>


```C++
CMediaType(
  [ref] const CMediaType &cmtype,
              HRESULT    *phr = NULL
);
```



## <a name="parameters"></a><span data-ttu-id="4b675-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4b675-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b675-107">*cmtype* \[ Ref\]</span><span class="sxs-lookup"><span data-stu-id="4b675-107">*cmtype* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="4b675-108">Verweis auf ein `CMediaType` -Objekt.</span><span class="sxs-lookup"><span data-stu-id="4b675-108">Reference to a `CMediaType` object.</span></span> <span data-ttu-id="4b675-109">Der -Konstruktor kopiert den Medientyp in das neue -Objekt, einschließlich des Formatblocks( sofern verfügbar).</span><span class="sxs-lookup"><span data-stu-id="4b675-109">The constructor copies the media type to the new object, including the format block, if any.</span></span>

</dd> <dt>

<span data-ttu-id="4b675-110">*Phr*</span><span class="sxs-lookup"><span data-stu-id="4b675-110">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="4b675-111">Zeiger auf eine Variable, die einen HRESULT-Wert empfängt.</span><span class="sxs-lookup"><span data-stu-id="4b675-111">Pointer to a variable that receives an HRESULT value.</span></span> <span data-ttu-id="4b675-112">Dieser Parameter kann ein **NULL-Zeiger** sein.</span><span class="sxs-lookup"><span data-stu-id="4b675-112">This parameter can be a **NULL** pointer.</span></span> <span data-ttu-id="4b675-113">Andernfalls muss der Aufrufer den Wert auf S \_ OK festlegen, bevor der Konstruktor aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="4b675-113">Otherwise, the caller must set the value to S\_OK before calling the constructor.</span></span> <span data-ttu-id="4b675-114">Wenn der Konstruktor fehlschlägt, legt er den Wert auf einen Fehlercode fest.</span><span class="sxs-lookup"><span data-stu-id="4b675-114">If the constructor fails, it sets the value to a failure code.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4b675-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4b675-115">Remarks</span></span>

<span data-ttu-id="4b675-116">Der Konstruktor ruft die [**CMediaType::InitMediaType-Methode**](cmediatype-initmediatype.md) auf, um den Medientyp zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="4b675-116">The constructor calls the [**CMediaType::InitMediaType**](cmediatype-initmediatype.md) method to initialize the media type.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b675-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4b675-117">Requirements</span></span>



| <span data-ttu-id="4b675-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4b675-118">Requirement</span></span> | <span data-ttu-id="4b675-119">Wert</span><span class="sxs-lookup"><span data-stu-id="4b675-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b675-120">Header</span><span class="sxs-lookup"><span data-stu-id="4b675-120">Header</span></span><br/>  | <dl> <span data-ttu-id="4b675-121"><dt>Mtype.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="4b675-121"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="4b675-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4b675-122">Library</span></span><br/> | <dl> <span data-ttu-id="4b675-123"><dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="4b675-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b675-124">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4b675-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b675-125">**CMediaType-Klasse**</span><span class="sxs-lookup"><span data-stu-id="4b675-125">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




