---
description: Mit der AddHead-Methode wird eine Liste am Anfang der Liste hinzugefügt.
ms.assetid: 9a344bed-d871-4082-9bbb-330f2ff42cca
title: Cgenericlist. AddHead-Methode (wxlist. h)-plist-Parameter
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.AddHead
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0039566f111033062bca080cb24924c7ea4324ac
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "106367407"
---
# <a name="cgenericlistaddhead-method-wxlisth---plist-parameter"></a><span data-ttu-id="ace6d-103">Cgenericlist. AddHead-Methode (wxlist. h)-plist-Parameter</span><span class="sxs-lookup"><span data-stu-id="ace6d-103">CGenericList.AddHead method (Wxlist.h) - pList parameter</span></span>

<span data-ttu-id="ace6d-104">Mit der- `AddHead` Methode wird eine Liste am Anfang der Liste hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="ace6d-104">The `AddHead` method adds a list to the front of the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="ace6d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ace6d-105">Syntax</span></span>


```C++
BOOL AddHead(
   CGenericList<OBJECT> *pList
);
```



## <a name="parameters"></a><span data-ttu-id="ace6d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ace6d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ace6d-107">*pList*</span><span class="sxs-lookup"><span data-stu-id="ace6d-107">*pList*</span></span> 
</dt> <dd>

<span data-ttu-id="ace6d-108">Ein Zeiger auf die Liste der hinzu zufügenden Elemente.</span><span class="sxs-lookup"><span data-stu-id="ace6d-108">Pointer to the list of items to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ace6d-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ace6d-109">Return value</span></span>

<span data-ttu-id="ace6d-110">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="ace6d-110">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="ace6d-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ace6d-111">Requirements</span></span>

| <span data-ttu-id="ace6d-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ace6d-112">Requirement</span></span> | <span data-ttu-id="ace6d-113">Wert</span><span class="sxs-lookup"><span data-stu-id="ace6d-113">Value</span></span> |
|-|-|
| <span data-ttu-id="ace6d-114">Header</span><span class="sxs-lookup"><span data-stu-id="ace6d-114">Header</span></span> | <span data-ttu-id="ace6d-115">Wxlist. h (Include Streams. h)</span><span class="sxs-lookup"><span data-stu-id="ace6d-115">Wxlist.h (include Streams.h)</span></span> |
| <span data-ttu-id="ace6d-116">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ace6d-116">Library</span></span>| <span data-ttu-id="ace6d-117">"Straumbase. lib" (Einzelhandels Builds); "Straumbasd. lib" (Debugbuilds)</span><span class="sxs-lookup"><span data-stu-id="ace6d-117">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="ace6d-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ace6d-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ace6d-119">**Cgenericlist-Klasse**</span><span class="sxs-lookup"><span data-stu-id="ace6d-119">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 




