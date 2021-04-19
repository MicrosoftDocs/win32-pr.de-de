---
description: 'Die Checkfunktionen-Methode fragt ab, ob ein Stream Suchfunktionen angegeben hat. Diese Methode implementiert die imediaseeking:: Checkfunktionen-Methode.'
ms.assetid: 48096af6-bbce-4a1f-be9a-fd150ed4536e
title: Cpospassthru. Checkfunktionen-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.CheckCapabilities
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 33f7a685684667d2f5d465b14070a595c70b178c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355946"
---
# <a name="cpospassthrucheckcapabilities-method"></a><span data-ttu-id="58f6a-104">Cpospassthru. Checkfunktionen-Methode</span><span class="sxs-lookup"><span data-stu-id="58f6a-104">CPosPassThru.CheckCapabilities method</span></span>

<span data-ttu-id="58f6a-105">Die- `CheckCapabilities` Methode fragt ab, ob ein Stream Suchfunktionen angegeben hat.</span><span class="sxs-lookup"><span data-stu-id="58f6a-105">The `CheckCapabilities` method queries whether a stream has specified seeking capabilities.</span></span> <span data-ttu-id="58f6a-106">Diese Methode implementiert die [**imediaseeking:: Checkfunktionen**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) -Methode.</span><span class="sxs-lookup"><span data-stu-id="58f6a-106">This method implements the [**IMediaSeeking::CheckCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="58f6a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="58f6a-107">Syntax</span></span>


```C++
HRESULT CheckCapabilities(
   DWORD *pCapabilities
);
```



## <a name="parameters"></a><span data-ttu-id="58f6a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="58f6a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58f6a-109">*pfunktionen*</span><span class="sxs-lookup"><span data-stu-id="58f6a-109">*pCapabilities*</span></span> 
</dt> <dd>

<span data-ttu-id="58f6a-110">Zeiger auf eine bitweise Kombination von einem oder mehreren Suchfunktionen, die [**\_ \_ Such \_ Funktionen**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities) suchen.</span><span class="sxs-lookup"><span data-stu-id="58f6a-110">Pointer to a bitwise combination of one or more [**AM\_SEEKING\_SEEKING\_CAPABILITIES**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities) attributes.</span></span> <span data-ttu-id="58f6a-111">Wenn die-Methode zurückgibt, gibt der Wert an, welches dieser Attribute verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="58f6a-111">When the method returns, the value indicates which of those attributes are available.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58f6a-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="58f6a-112">Return value</span></span>

<span data-ttu-id="58f6a-113">Gibt den **HRESULT** -Wert aus der verbundenen PIN zurück.</span><span class="sxs-lookup"><span data-stu-id="58f6a-113">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="58f6a-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="58f6a-114">Requirements</span></span>



| <span data-ttu-id="58f6a-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="58f6a-115">Requirement</span></span> | <span data-ttu-id="58f6a-116">Wert</span><span class="sxs-lookup"><span data-stu-id="58f6a-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58f6a-117">Header</span><span class="sxs-lookup"><span data-stu-id="58f6a-117">Header</span></span><br/>  | <dl> <span data-ttu-id="58f6a-118"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="58f6a-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="58f6a-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="58f6a-119">Library</span></span><br/> | <dl> <span data-ttu-id="58f6a-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="58f6a-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58f6a-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="58f6a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58f6a-122">**Cpospassthru-Klasse**</span><span class="sxs-lookup"><span data-stu-id="58f6a-122">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




