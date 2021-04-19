---
description: Die setsubtype-Methode gibt den Untertyp an.
ms.assetid: cf52e0dc-d75b-408e-a63c-481d55151d4a
title: Cmediatype. setsubtype-Methode (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetSubtype
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6474777b1b2e91ce0b676fdc7dbd572d7c622f0b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352949"
---
# <a name="cmediatypesetsubtype-method"></a><span data-ttu-id="9f468-103">Cmediatype. setsubtype-Methode</span><span class="sxs-lookup"><span data-stu-id="9f468-103">CMediaType.SetSubtype method</span></span>

<span data-ttu-id="9f468-104">Die- `SetSubtype` Methode gibt den Untertyp an.</span><span class="sxs-lookup"><span data-stu-id="9f468-104">The `SetSubtype` method specifies the subtype.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f468-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9f468-105">Syntax</span></span>


```C++
void SetSubtype(
   const GUID *psubtype
);
```



## <a name="parameters"></a><span data-ttu-id="9f468-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9f468-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f468-107">*psubtype*</span><span class="sxs-lookup"><span data-stu-id="9f468-107">*psubtype*</span></span> 
</dt> <dd>

<span data-ttu-id="9f468-108">Zeiger auf eine **GUID** , die den Untertyp angibt.</span><span class="sxs-lookup"><span data-stu-id="9f468-108">Pointer to a **GUID** that specifies the subtype.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f468-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9f468-109">Return value</span></span>

<span data-ttu-id="9f468-110">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="9f468-110">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f468-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9f468-111">Requirements</span></span>



| <span data-ttu-id="9f468-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9f468-112">Requirement</span></span> | <span data-ttu-id="9f468-113">Wert</span><span class="sxs-lookup"><span data-stu-id="9f468-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f468-114">Header</span><span class="sxs-lookup"><span data-stu-id="9f468-114">Header</span></span><br/>  | <dl> <span data-ttu-id="9f468-115"><dt>Mtype. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9f468-115"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="9f468-116">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9f468-116">Library</span></span><br/> | <dl> <span data-ttu-id="9f468-117">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="9f468-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f468-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9f468-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f468-119">**Cmediatype-Klasse**</span><span class="sxs-lookup"><span data-stu-id="9f468-119">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




