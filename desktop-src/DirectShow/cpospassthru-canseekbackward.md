---
description: 'Die canseekabwärts-Methode bestimmt, ob der Stream rückwärts Seeding durchgeführt werden kann. Diese Methode implementiert die imediaposition:: canseekabwärts-Methode.'
ms.assetid: 6443980f-6863-4941-b2dd-4a31257b5810
title: Cpospassthru. canseekabwärts-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.CanSeekBackward
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a6a016f5cfeea7ca1e63bb4d0e603784b8f95a85
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367583"
---
# <a name="cpospassthrucanseekbackward-method"></a><span data-ttu-id="be12b-104">Cpospassthru. canseekabwärts-Methode</span><span class="sxs-lookup"><span data-stu-id="be12b-104">CPosPassThru.CanSeekBackward method</span></span>

<span data-ttu-id="be12b-105">Die- `CanSeekBackward` Methode bestimmt, ob der Stream rückwärts Seeding durchgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="be12b-105">The `CanSeekBackward` method determines whether the stream can be seeked backward.</span></span> <span data-ttu-id="be12b-106">Diese Methode implementiert die [**imediaposition:: canseekabwärts**](/windows/desktop/api/Control/nf-control-imediaposition-canseekbackward) -Methode.</span><span class="sxs-lookup"><span data-stu-id="be12b-106">This method implements the [**IMediaPosition::CanSeekBackward**](/windows/desktop/api/Control/nf-control-imediaposition-canseekbackward) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="be12b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="be12b-107">Syntax</span></span>


```C++
HRESULT CanSeekBackward(
   LONG *pCanSeekBackward
);
```



## <a name="parameters"></a><span data-ttu-id="be12b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="be12b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be12b-109">*pcanseekabwärts*</span><span class="sxs-lookup"><span data-stu-id="be12b-109">*pCanSeekBackward*</span></span> 
</dt> <dd>

<span data-ttu-id="be12b-110">Ein Zeiger auf eine Variable, die den Wert oatrue empfängt, wenn der Filter rückwärts suchen oder andernfalls oafalse.</span><span class="sxs-lookup"><span data-stu-id="be12b-110">Pointer to a variable that receives the value OATRUE if the filter can seek backward, or OAFALSE otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be12b-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="be12b-111">Return value</span></span>

<span data-ttu-id="be12b-112">Gibt den **HRESULT** -Wert aus der verbundenen PIN zurück.</span><span class="sxs-lookup"><span data-stu-id="be12b-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="be12b-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="be12b-113">Requirements</span></span>



| <span data-ttu-id="be12b-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="be12b-114">Requirement</span></span> | <span data-ttu-id="be12b-115">Wert</span><span class="sxs-lookup"><span data-stu-id="be12b-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be12b-116">Header</span><span class="sxs-lookup"><span data-stu-id="be12b-116">Header</span></span><br/>  | <dl> <span data-ttu-id="be12b-117"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="be12b-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="be12b-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="be12b-118">Library</span></span><br/> | <dl> <span data-ttu-id="be12b-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="be12b-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be12b-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="be12b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be12b-121">**Cpospassthru-Klasse**</span><span class="sxs-lookup"><span data-stu-id="be12b-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




