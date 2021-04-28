---
description: 'CSourceSeeking.GetCapabilities-Methode: Die GetCapabilities-Methode ruft alle Suchfunktionen des Streams ab. Diese Methode implementiert die IMediaSeeking::GetCapabilities-Methode.'
ms.assetid: a2ff7ea2-09bd-49a7-8e1b-d6360939036e
title: CSourceSeeking.GetCapabilities-Methode (Ctlutil.h)
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
ms.openlocfilehash: f1f354381c4c99cf880c75cbbc4b13355e386030
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098778"
---
# <a name="csourceseekinggetcapabilities-method"></a><span data-ttu-id="3cbe2-104">CSourceSeeking.GetCapabilities-Methode</span><span class="sxs-lookup"><span data-stu-id="3cbe2-104">CSourceSeeking.GetCapabilities method</span></span>

<span data-ttu-id="3cbe2-105">Die `GetCapabilities` -Methode ruft alle Suchfunktionen des Streams ab.</span><span class="sxs-lookup"><span data-stu-id="3cbe2-105">The `GetCapabilities` method retrieves all the seeking capabilities of the stream.</span></span> <span data-ttu-id="3cbe2-106">Diese Methode implementiert die [**IMediaSeeking::GetCapabilities-Methode.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities)</span><span class="sxs-lookup"><span data-stu-id="3cbe2-106">This method implements the [**IMediaSeeking::GetCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3cbe2-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="3cbe2-107">Syntax</span></span>


```C++
HRESULT GetCapabilities(
   DWORD *pCapabilities
);
```



## <a name="parameters"></a><span data-ttu-id="3cbe2-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="3cbe2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3cbe2-109">*pCapabilities*</span><span class="sxs-lookup"><span data-stu-id="3cbe2-109">*pCapabilities*</span></span> 
</dt> <dd>

<span data-ttu-id="3cbe2-110">Zeiger auf eine Variable, die eine bitweise Kombination von [**AM \_ SEEKING SEEKING \_ \_ CAPABILITIES-Flags**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities) empfängt.</span><span class="sxs-lookup"><span data-stu-id="3cbe2-110">Pointer to a variable that receives a bitwise combination of [**AM\_SEEKING\_SEEKING\_CAPABILITIES**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities) flags.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3cbe2-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3cbe2-111">Return value</span></span>

<span data-ttu-id="3cbe2-112">Gibt einen der in der folgenden Tabelle aufgeführten **HRESULT-Werte** zurück.</span><span class="sxs-lookup"><span data-stu-id="3cbe2-112">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="3cbe2-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="3cbe2-113">Return code</span></span>                                                                               | <span data-ttu-id="3cbe2-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3cbe2-114">Description</span></span>                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <span data-ttu-id="3cbe2-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3cbe2-115"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="3cbe2-116">Erfolg</span><span class="sxs-lookup"><span data-stu-id="3cbe2-116">Success</span></span><br/>                |
| <dl> <span data-ttu-id="3cbe2-117"><dt>**\_E-ZEIGER**</dt></span><span class="sxs-lookup"><span data-stu-id="3cbe2-117"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="3cbe2-118">**NULL-Zeigerwert**</span><span class="sxs-lookup"><span data-stu-id="3cbe2-118">**NULL** pointer value</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3cbe2-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3cbe2-119">Remarks</span></span>

<span data-ttu-id="3cbe2-120">Die Suchfunktionen werden von der [**CSourceSeeking::m \_ dwSeekingCaps-Membervariablen**](csourceseeking-m-dwseekingcaps.md) angegeben.</span><span class="sxs-lookup"><span data-stu-id="3cbe2-120">The seeking capabilities are specified by the [**CSourceSeeking::m\_dwSeekingCaps**](csourceseeking-m-dwseekingcaps.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="3cbe2-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3cbe2-121">Requirements</span></span>



| <span data-ttu-id="3cbe2-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3cbe2-122">Requirement</span></span> | <span data-ttu-id="3cbe2-123">Wert</span><span class="sxs-lookup"><span data-stu-id="3cbe2-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3cbe2-124">Header</span><span class="sxs-lookup"><span data-stu-id="3cbe2-124">Header</span></span><br/>  | <dl> <span data-ttu-id="3cbe2-125"><dt>Ctlutil.h (einschließlich Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="3cbe2-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3cbe2-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3cbe2-126">Library</span></span><br/> | <dl> <span data-ttu-id="3cbe2-127"><dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="3cbe2-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3cbe2-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="3cbe2-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3cbe2-129">**CSourceSeeking-Klasse**</span><span class="sxs-lookup"><span data-stu-id="3cbe2-129">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




