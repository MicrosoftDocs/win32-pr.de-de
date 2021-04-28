---
description: 'CPosPassThru.IsFormatSupported-Methode: Die IsFormatSupported-Methode bestimmt, ob ein angegebenes Zeitformat unterstützt wird. Diese Methode implementiert die IMediaSeeking::IsFormatSupported-Methode.'
ms.assetid: dd8751d6-8439-4155-bdaf-b152a7c6cad4
title: CPosPassThru.IsFormatSupported-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.IsFormatSupported
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6bd4b90bbe86e7ba05aa48fb7888c946babd8ed9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095248"
---
# <a name="cpospassthruisformatsupported-method"></a><span data-ttu-id="f8e9d-104">CPosPassThru.IsFormatSupported-Methode</span><span class="sxs-lookup"><span data-stu-id="f8e9d-104">CPosPassThru.IsFormatSupported method</span></span>

<span data-ttu-id="f8e9d-105">Die `IsFormatSupported` -Methode bestimmt, ob ein angegebenes Zeitformat unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="f8e9d-105">The `IsFormatSupported` method determines whether a specified time format is supported.</span></span> <span data-ttu-id="f8e9d-106">Diese Methode implementiert die [**IMediaSeeking::IsFormatSupported-Methode.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isformatsupported)</span><span class="sxs-lookup"><span data-stu-id="f8e9d-106">This method implements the [**IMediaSeeking::IsFormatSupported**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isformatsupported) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8e9d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f8e9d-107">Syntax</span></span>


```C++
HRESULT IsFormatSupported(
   const GUID *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="f8e9d-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f8e9d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8e9d-109">*pFormat*</span><span class="sxs-lookup"><span data-stu-id="f8e9d-109">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="f8e9d-110">Zeiger auf eine Zeitformat-GUID.</span><span class="sxs-lookup"><span data-stu-id="f8e9d-110">Pointer to a time format GUID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8e9d-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f8e9d-111">Return value</span></span>

<span data-ttu-id="f8e9d-112">Gibt den **HRESULT-Wert** vom verbundenen Pin zurück.</span><span class="sxs-lookup"><span data-stu-id="f8e9d-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8e9d-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f8e9d-113">Requirements</span></span>



| <span data-ttu-id="f8e9d-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f8e9d-114">Requirement</span></span> | <span data-ttu-id="f8e9d-115">Wert</span><span class="sxs-lookup"><span data-stu-id="f8e9d-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8e9d-116">Header</span><span class="sxs-lookup"><span data-stu-id="f8e9d-116">Header</span></span><br/>  | <dl> <span data-ttu-id="f8e9d-117"><dt>Ctlutil.h (einschließlich Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="f8e9d-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f8e9d-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f8e9d-118">Library</span></span><br/> | <dl> <span data-ttu-id="f8e9d-119"><dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="f8e9d-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8e9d-120">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f8e9d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8e9d-121">**CPosPassThru-Klasse**</span><span class="sxs-lookup"><span data-stu-id="f8e9d-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> <dt>

[<span data-ttu-id="f8e9d-122">**Zeitformat-GUIDs**</span><span class="sxs-lookup"><span data-stu-id="f8e9d-122">**Time Format GUIDs**</span></span>](time-format-guids.md)
</dt> </dl>

 

 




