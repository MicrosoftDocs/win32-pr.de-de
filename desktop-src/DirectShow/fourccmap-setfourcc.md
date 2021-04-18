---
description: Legt den FourCC-Teil des fourccmap-Objekts fest.
ms.assetid: cc821e39-e565-4255-a289-2c9507d43433
title: 'Fourccmap:: setfourcc-Methode (FourCC. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FOURCCMap.SetFOURCC
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 435eb209e39ffad29f041e2e117a45d735abffed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358634"
---
# <a name="fourccmapsetfourcc-method"></a><span data-ttu-id="72cb8-103">Fourccmap:: setfourcc-Methode</span><span class="sxs-lookup"><span data-stu-id="72cb8-103">FOURCCMap::SetFOURCC method</span></span>

<span data-ttu-id="72cb8-104">Legt den **FourCC** -Teil des [**fourccmap**](fourccmap.md) -Objekts fest.</span><span class="sxs-lookup"><span data-stu-id="72cb8-104">Sets the **FOURCC** portion of the [**FOURCCMap**](fourccmap.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="72cb8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="72cb8-105">Syntax</span></span>


```C++
void SetFOURCC(
   const GUID *pguid
);
```



## <a name="parameters"></a><span data-ttu-id="72cb8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="72cb8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72cb8-107">*pguid*</span><span class="sxs-lookup"><span data-stu-id="72cb8-107">*pguid*</span></span> 
</dt> <dd>

<span data-ttu-id="72cb8-108">Zeiger auf den zurückgegebenen Globally Unique Identifier (**GUID**)-Teil des **fourccmap** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="72cb8-108">Pointer to the returned globally unique identifier (**GUID**) part of the **FOURCCMap** object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72cb8-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="72cb8-109">Return value</span></span>

<span data-ttu-id="72cb8-110">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="72cb8-110">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="72cb8-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="72cb8-111">Requirements</span></span>



| <span data-ttu-id="72cb8-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="72cb8-112">Requirement</span></span> | <span data-ttu-id="72cb8-113">Wert</span><span class="sxs-lookup"><span data-stu-id="72cb8-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72cb8-114">Header</span><span class="sxs-lookup"><span data-stu-id="72cb8-114">Header</span></span><br/>  | <dl> <span data-ttu-id="72cb8-115"><dt>FourCC. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="72cb8-115"><dt>Fourcc.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="72cb8-116">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="72cb8-116">Library</span></span><br/> | <dl> <span data-ttu-id="72cb8-117">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="72cb8-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72cb8-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="72cb8-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72cb8-119">**Fourccmap-Klasse**</span><span class="sxs-lookup"><span data-stu-id="72cb8-119">**FOURCCMap Class**</span></span>](fourccmap.md)
</dt> </dl>

 

 




