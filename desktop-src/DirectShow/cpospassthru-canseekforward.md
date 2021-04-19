---
description: 'Die canseekforward-Methode bestimmt, ob für den Datenstrom ein Seeding durchgeführt werden kann. Diese Methode implementiert die imediaposition:: canseekforward-Methode.'
ms.assetid: ccb2db8d-b52e-4e3d-b49b-9689197a974a
title: Cpospassthru. canseekforward-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.CanSeekForward
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 701bfdff1d3a3a37dc0e3935aa82bfca2e01cfcb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360887"
---
# <a name="cpospassthrucanseekforward-method"></a><span data-ttu-id="fdc28-104">Cpospassthru. canseekforward-Methode</span><span class="sxs-lookup"><span data-stu-id="fdc28-104">CPosPassThru.CanSeekForward method</span></span>

<span data-ttu-id="fdc28-105">Die- `CanSeekForward` Methode bestimmt, ob für den Datenstrom ein Seeding durchgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="fdc28-105">The `CanSeekForward` method determines whether the stream can be seeked forward.</span></span> <span data-ttu-id="fdc28-106">Diese Methode implementiert die [**imediaposition:: canseekforward**](/windows/desktop/api/Control/nf-control-imediaposition-canseekforward) -Methode.</span><span class="sxs-lookup"><span data-stu-id="fdc28-106">This method implements the [**IMediaPosition::CanSeekForward**](/windows/desktop/api/Control/nf-control-imediaposition-canseekforward) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="fdc28-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="fdc28-107">Syntax</span></span>


```C++
HRESULT CanSeekForward(
   LONG *pCanSeekForward
);
```



## <a name="parameters"></a><span data-ttu-id="fdc28-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="fdc28-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fdc28-109">*pcanseekforward*</span><span class="sxs-lookup"><span data-stu-id="fdc28-109">*pCanSeekForward*</span></span> 
</dt> <dd>

<span data-ttu-id="fdc28-110">Ein Zeiger auf eine Variable, die den Wert oatrue empfängt, wenn der Filter eine Suche durchsuchen oder andernfalls oafalse.</span><span class="sxs-lookup"><span data-stu-id="fdc28-110">Pointer to a variable that receives the value OATRUE if the filter can seek forward, or OAFALSE otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fdc28-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fdc28-111">Return value</span></span>

<span data-ttu-id="fdc28-112">Gibt den **HRESULT** -Wert aus der verbundenen PIN zurück.</span><span class="sxs-lookup"><span data-stu-id="fdc28-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="fdc28-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fdc28-113">Requirements</span></span>



| <span data-ttu-id="fdc28-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fdc28-114">Requirement</span></span> | <span data-ttu-id="fdc28-115">Wert</span><span class="sxs-lookup"><span data-stu-id="fdc28-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fdc28-116">Header</span><span class="sxs-lookup"><span data-stu-id="fdc28-116">Header</span></span><br/>  | <dl> <span data-ttu-id="fdc28-117"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fdc28-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="fdc28-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="fdc28-118">Library</span></span><br/> | <dl> <span data-ttu-id="fdc28-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="fdc28-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fdc28-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fdc28-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fdc28-121">**Cpospassthru-Klasse**</span><span class="sxs-lookup"><span data-stu-id="fdc28-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




