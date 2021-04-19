---
description: Die displaypininfo-Methode verfolgt während des Debuggens eine PIN-Verbindung.
ms.assetid: 3c1aa5ab-7f6b-4518-abf3-b5138f6267ee
title: Cbasepin. displaypininfo-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.DisplayPinInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ea563ca07eaea6b6974a831726918866414a33b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361317"
---
# <a name="cbasepindisplaypininfo-method"></a><span data-ttu-id="54439-103">Cbasepin. displaypininfo-Methode</span><span class="sxs-lookup"><span data-stu-id="54439-103">CBasePin.DisplayPinInfo method</span></span>

<span data-ttu-id="54439-104">Die- `DisplayPinInfo` Methode verfolgt während des Debuggens eine PIN-Verbindung.</span><span class="sxs-lookup"><span data-stu-id="54439-104">The `DisplayPinInfo` method traces a pin connection during debugging.</span></span>

## <a name="syntax"></a><span data-ttu-id="54439-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="54439-105">Syntax</span></span>


```C++
void DisplayPinInfo(
   IPin *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="54439-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="54439-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54439-107">*preceivepin*</span><span class="sxs-lookup"><span data-stu-id="54439-107">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="54439-108">Ein Zeiger auf die empfangende PIN.</span><span class="sxs-lookup"><span data-stu-id="54439-108">Pointer to the receiving pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54439-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="54439-109">Return value</span></span>

<span data-ttu-id="54439-110">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="54439-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="54439-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="54439-111">Remarks</span></span>

<span data-ttu-id="54439-112">In Debugbuilds ruft diese Methode die [**dbglog**](dbglog.md) -Funktion auf, um einen Verbindungsversuch zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="54439-112">In debug builds, this method calls the [**DbgLog**](dbglog.md) function to trace a connection attempt.</span></span> <span data-ttu-id="54439-113">Bei Einzelhandels Builds führt diese Methode keine Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="54439-113">In retail builds, this method does nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="54439-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="54439-114">Requirements</span></span>



| <span data-ttu-id="54439-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="54439-115">Requirement</span></span> | <span data-ttu-id="54439-116">Wert</span><span class="sxs-lookup"><span data-stu-id="54439-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54439-117">Header</span><span class="sxs-lookup"><span data-stu-id="54439-117">Header</span></span><br/>  | <dl> <span data-ttu-id="54439-118"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="54439-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="54439-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="54439-119">Library</span></span><br/> | <dl> <span data-ttu-id="54439-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="54439-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54439-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="54439-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54439-122">**Cbasepin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="54439-122">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




