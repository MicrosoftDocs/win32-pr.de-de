---
description: Der Operator = weist eine neue Bezugszeit zu.
ms.assetid: 0b11e2ea-23dc-4c75-88c6-94215a4b14b6
title: Methode "kref time. Operator =" (Ref time. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRefTime.operator=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b87e6517946c64cb2a60e95912aba423a1880215
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370749"
---
# <a name="creftimeoperator-method-reftimeh"></a><span data-ttu-id="d4ee5-103">Methode "kref time. Operator =" (Ref time. h)</span><span class="sxs-lookup"><span data-stu-id="d4ee5-103">CRefTime.operator= method (Reftime.h)</span></span>

<span data-ttu-id="d4ee5-104">Der Operator = weist eine neue Bezugszeit zu.</span><span class="sxs-lookup"><span data-stu-id="d4ee5-104">The = operator assigns a new reference time.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4ee5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d4ee5-105">Syntax</span></span>


```C++
CRefTime& operator=(
  [ref] const CRefTime &rt
);
```



## <a name="parameters"></a><span data-ttu-id="d4ee5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d4ee5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4ee5-107">*RT* \[ atur\]</span><span class="sxs-lookup"><span data-stu-id="d4ee5-107">*rt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="d4ee5-108">Verweis auf ein-Objekt, das die neue **Bezugszeit angibt** .</span><span class="sxs-lookup"><span data-stu-id="d4ee5-108">Reference to a **CRefTime** object that specifies the new reference time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4ee5-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d4ee5-109">Return value</span></span>

<span data-ttu-id="d4ee5-110">Gibt einen Verweis auf das-Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="d4ee5-110">Returns a reference to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4ee5-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d4ee5-111">Requirements</span></span>



| <span data-ttu-id="d4ee5-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d4ee5-112">Requirement</span></span> | <span data-ttu-id="d4ee5-113">Wert</span><span class="sxs-lookup"><span data-stu-id="d4ee5-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4ee5-114">Header</span><span class="sxs-lookup"><span data-stu-id="d4ee5-114">Header</span></span><br/>  | <dl> <span data-ttu-id="d4ee5-115"><dt>Ref time. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d4ee5-115"><dt>Reftime.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d4ee5-116">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d4ee5-116">Library</span></span><br/> | <dl> <span data-ttu-id="d4ee5-117">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="d4ee5-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




