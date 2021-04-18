---
description: 'Die getfunktionalitäten-Methode ruft alle Suchfunktionen des Streams ab. Diese Methode implementiert die imediaseeking:: getfunktionalitäten-Methode.'
ms.assetid: a2ff7ea2-09bd-49a7-8e1b-d6360939036e
title: Csourceseeking. getSources-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetCapabilities
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: eda23944fd039576bb5de74fbb7c32e375415670
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354647"
---
# <a name="csourceseekinggetcapabilities-method"></a><span data-ttu-id="61f6f-104">Csourceseeking. getSources-Methode</span><span class="sxs-lookup"><span data-stu-id="61f6f-104">CSourceSeeking.GetCapabilities method</span></span>

<span data-ttu-id="61f6f-105">Die- `GetCapabilities` Methode ruft alle Suchfunktionen des Streams ab.</span><span class="sxs-lookup"><span data-stu-id="61f6f-105">The `GetCapabilities` method retrieves all the seeking capabilities of the stream.</span></span> <span data-ttu-id="61f6f-106">Diese Methode implementiert die [**imediaseeking:: getfunktionalitäten**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) -Methode.</span><span class="sxs-lookup"><span data-stu-id="61f6f-106">This method implements the [**IMediaSeeking::GetCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="61f6f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="61f6f-107">Syntax</span></span>


```C++
HRESULT GetCapabilities(
   DWORD *pCapabilities
);
```



## <a name="parameters"></a><span data-ttu-id="61f6f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="61f6f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61f6f-109">*pfunktionen*</span><span class="sxs-lookup"><span data-stu-id="61f6f-109">*pCapabilities*</span></span> 
</dt> <dd>

<span data-ttu-id="61f6f-110">Ein Zeiger auf eine Variable, die eine bitweise Kombination von für Suchvorgänge [**\_ \_ suchbare \_**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities) Flags empfängt.</span><span class="sxs-lookup"><span data-stu-id="61f6f-110">Pointer to a variable that receives a bitwise combination of [**AM\_SEEKING\_SEEKING\_CAPABILITIES**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities) flags.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61f6f-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="61f6f-111">Return value</span></span>

<span data-ttu-id="61f6f-112">Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="61f6f-112">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="61f6f-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="61f6f-113">Return code</span></span>                                                                               | <span data-ttu-id="61f6f-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="61f6f-114">Description</span></span>                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <span data-ttu-id="61f6f-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="61f6f-115"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="61f6f-116">Erfolg</span><span class="sxs-lookup"><span data-stu-id="61f6f-116">Success</span></span><br/>                |
| <dl> <span data-ttu-id="61f6f-117"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="61f6f-117"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="61f6f-118">**Null** -Zeiger Wert</span><span class="sxs-lookup"><span data-stu-id="61f6f-118">**NULL** pointer value</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="61f6f-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="61f6f-119">Remarks</span></span>

<span data-ttu-id="61f6f-120">Die Suchfunktionen werden von der Element Variablen [**csourceseeking:: m \_ dwseekingcaps**](csourceseeking-m-dwseekingcaps.md) angegeben.</span><span class="sxs-lookup"><span data-stu-id="61f6f-120">The seeking capabilities are specified by the [**CSourceSeeking::m\_dwSeekingCaps**](csourceseeking-m-dwseekingcaps.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="61f6f-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="61f6f-121">Requirements</span></span>



| <span data-ttu-id="61f6f-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="61f6f-122">Requirement</span></span> | <span data-ttu-id="61f6f-123">Wert</span><span class="sxs-lookup"><span data-stu-id="61f6f-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61f6f-124">Header</span><span class="sxs-lookup"><span data-stu-id="61f6f-124">Header</span></span><br/>  | <dl> <span data-ttu-id="61f6f-125"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="61f6f-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="61f6f-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="61f6f-126">Library</span></span><br/> | <dl> <span data-ttu-id="61f6f-127">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="61f6f-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61f6f-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="61f6f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61f6f-129">**Csourceseeking-Klasse**</span><span class="sxs-lookup"><span data-stu-id="61f6f-129">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




