---
description: 'CPosPassThru.GetCapabilities-Methode: Die GetCapabilities-Methode ruft alle Suchfunktionen des Streams ab. Diese Methode implementiert die IMediaSeeking::GetCapabilities-Methode.'
ms.assetid: c60c4f47-48de-47d0-9b87-589b84df842c
title: CPosPassThru.GetCapabilities-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetCapabilities
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c21838d3df72d52255d0a2e35dd0b7d34ef55411
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085568"
---
# <a name="cpospassthrugetcapabilities-method"></a><span data-ttu-id="40350-104">CPosPassThru.GetCapabilities-Methode</span><span class="sxs-lookup"><span data-stu-id="40350-104">CPosPassThru.GetCapabilities method</span></span>

<span data-ttu-id="40350-105">Die **GetCapabilities-Methode** ruft alle Suchfunktionen des Streams ab.</span><span class="sxs-lookup"><span data-stu-id="40350-105">The **GetCapabilities** method retrieves all the seeking capabilities of the stream.</span></span> <span data-ttu-id="40350-106">Diese Methode implementiert die [**IMediaSeeking::GetCapabilities-Methode.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities)</span><span class="sxs-lookup"><span data-stu-id="40350-106">This method implements the [**IMediaSeeking::GetCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="40350-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="40350-107">Syntax</span></span>


```C++
HRESULT GetCapabilities(
   DWORD *pCapabilities
);
```



## <a name="parameters"></a><span data-ttu-id="40350-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="40350-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40350-109">*pCapabilities*</span><span class="sxs-lookup"><span data-stu-id="40350-109">*pCapabilities*</span></span> 
</dt> <dd>

<span data-ttu-id="40350-110">Zeiger auf eine Variable, die eine bitweise Kombination von [**AM \_ SEEKING SEEKING \_ \_ CAPABILITIES-Flags**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities) empfängt.</span><span class="sxs-lookup"><span data-stu-id="40350-110">Pointer to a variable that receives a bitwise combination of [**AM\_SEEKING\_SEEKING\_CAPABILITIES**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities) flags.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40350-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="40350-111">Return value</span></span>

<span data-ttu-id="40350-112">Gibt den **HRESULT-Wert** vom verbundenen Pin zurück.</span><span class="sxs-lookup"><span data-stu-id="40350-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="40350-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="40350-113">Requirements</span></span>



| <span data-ttu-id="40350-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="40350-114">Requirement</span></span> | <span data-ttu-id="40350-115">Wert</span><span class="sxs-lookup"><span data-stu-id="40350-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="40350-116">Header</span><span class="sxs-lookup"><span data-stu-id="40350-116">Header</span></span><br/>  | <dl> <span data-ttu-id="40350-117"><dt>Ctlutil.h (einschließlich Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="40350-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="40350-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="40350-118">Library</span></span><br/> | <dl> <span data-ttu-id="40350-119"><dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="40350-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40350-120">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="40350-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40350-121">**CPosPassThru-Klasse**</span><span class="sxs-lookup"><span data-stu-id="40350-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




