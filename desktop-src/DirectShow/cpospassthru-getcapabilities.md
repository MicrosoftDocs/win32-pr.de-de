---
description: 'Die getfunktionalitäten-Methode ruft alle Suchfunktionen des Streams ab. Diese Methode implementiert die imediaseeking:: getfunktionalitäten-Methode.'
ms.assetid: c60c4f47-48de-47d0-9b87-589b84df842c
title: Cpospassthru. getfunktionalitäten-Methode (ctlutil. h)
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
ms.openlocfilehash: f896adbc1015cb34e6f9063cb5ebf73e5cdb441c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358069"
---
# <a name="cpospassthrugetcapabilities-method"></a><span data-ttu-id="b5c18-104">Cpospassthru. getfunktionalitäten-Methode</span><span class="sxs-lookup"><span data-stu-id="b5c18-104">CPosPassThru.GetCapabilities method</span></span>

<span data-ttu-id="b5c18-105">Die **getfunktionalitäten** -Methode ruft alle Suchfunktionen des Streams ab.</span><span class="sxs-lookup"><span data-stu-id="b5c18-105">The **GetCapabilities** method retrieves all the seeking capabilities of the stream.</span></span> <span data-ttu-id="b5c18-106">Diese Methode implementiert die [**imediaseeking:: getfunktionalitäten**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) -Methode.</span><span class="sxs-lookup"><span data-stu-id="b5c18-106">This method implements the [**IMediaSeeking::GetCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5c18-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b5c18-107">Syntax</span></span>


```C++
HRESULT GetCapabilities(
   DWORD *pCapabilities
);
```



## <a name="parameters"></a><span data-ttu-id="b5c18-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b5c18-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5c18-109">*pfunktionen*</span><span class="sxs-lookup"><span data-stu-id="b5c18-109">*pCapabilities*</span></span> 
</dt> <dd>

<span data-ttu-id="b5c18-110">Ein Zeiger auf eine Variable, die eine bitweise Kombination von für Suchvorgänge [**\_ \_ suchbare \_**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities) Flags empfängt.</span><span class="sxs-lookup"><span data-stu-id="b5c18-110">Pointer to a variable that receives a bitwise combination of [**AM\_SEEKING\_SEEKING\_CAPABILITIES**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities) flags.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5c18-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b5c18-111">Return value</span></span>

<span data-ttu-id="b5c18-112">Gibt den **HRESULT** -Wert aus der verbundenen PIN zurück.</span><span class="sxs-lookup"><span data-stu-id="b5c18-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5c18-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b5c18-113">Requirements</span></span>



| <span data-ttu-id="b5c18-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b5c18-114">Requirement</span></span> | <span data-ttu-id="b5c18-115">Wert</span><span class="sxs-lookup"><span data-stu-id="b5c18-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5c18-116">Header</span><span class="sxs-lookup"><span data-stu-id="b5c18-116">Header</span></span><br/>  | <dl> <span data-ttu-id="b5c18-117"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b5c18-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b5c18-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b5c18-118">Library</span></span><br/> | <dl> <span data-ttu-id="b5c18-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="b5c18-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5c18-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b5c18-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5c18-121">**Cpospassthru-Klasse**</span><span class="sxs-lookup"><span data-stu-id="b5c18-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




