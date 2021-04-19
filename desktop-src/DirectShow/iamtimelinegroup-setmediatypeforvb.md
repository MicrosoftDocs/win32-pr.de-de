---
description: Die setmediatypeer forvb-Methode gibt den Gruppen Medientyp für Automatisierungs Clients an.
ms.assetid: 86f52088-a0dd-40be-98a0-8adc09b264dd
title: 'Iamtimelinegroup:: setmediatypeer forvb-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetMediaTypeForVB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 1371b1d6c906666ca30e5df2d26dbe20eddf1745
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370283"
---
# <a name="iamtimelinegroupsetmediatypeforvb-method"></a><span data-ttu-id="f0a78-103">Iamtimelinegroup:: setmediatypeer forvb-Methode</span><span class="sxs-lookup"><span data-stu-id="f0a78-103">IAMTimelineGroup::SetMediaTypeForVB method</span></span>

> [!Note]  
> <span data-ttu-id="f0a78-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="f0a78-104">\[Deprecated.</span></span> <span data-ttu-id="f0a78-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="f0a78-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="f0a78-106">Die- `SetMediaTypeForVB` Methode gibt den Gruppen Medientyp für Automation-Clients an.</span><span class="sxs-lookup"><span data-stu-id="f0a78-106">The `SetMediaTypeForVB` method specifies the group media type, for Automation clients.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0a78-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f0a78-107">Syntax</span></span>


```C++
HRESULT SetMediaTypeForVB(
  [in] long Val
);
```



## <a name="parameters"></a><span data-ttu-id="f0a78-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f0a78-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0a78-109">*Val* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f0a78-109">*Val* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0a78-110">Der-Wert, der den Medientyp angibt.</span><span class="sxs-lookup"><span data-stu-id="f0a78-110">Value that specifies the media type.</span></span> <span data-ttu-id="f0a78-111">Legen Sie den Wert für Video auf 0 oder für Audiodaten den Wert 1 fest.</span><span class="sxs-lookup"><span data-stu-id="f0a78-111">Set the value to 0 for video, or 1 for audio.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0a78-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f0a78-112">Return value</span></span>

<span data-ttu-id="f0a78-113">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="f0a78-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f0a78-114">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f0a78-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0a78-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f0a78-115">Remarks</span></span>

<span data-ttu-id="f0a78-116">Diese Methode ist für Automatisierungs Clients vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="f0a78-116">This method is intended for Automation clients.</span></span> <span data-ttu-id="f0a78-117">Verwenden Sie für C++-Anwendungen die [**iamtimelinegroup:: setmediatype**](iamtimelinegroup-setmediatype.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="f0a78-117">For C++ applications, use the [**IAMTimelineGroup::SetMediaType**](iamtimelinegroup-setmediatype.md) method.</span></span>

> [!Note]  
> <span data-ttu-id="f0a78-118">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="f0a78-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="f0a78-119">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="f0a78-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="f0a78-120">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f0a78-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f0a78-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f0a78-121">Requirements</span></span>



| <span data-ttu-id="f0a78-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f0a78-122">Requirement</span></span> | <span data-ttu-id="f0a78-123">Wert</span><span class="sxs-lookup"><span data-stu-id="f0a78-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f0a78-124">Header</span><span class="sxs-lookup"><span data-stu-id="f0a78-124">Header</span></span><br/>  | <dl> <span data-ttu-id="f0a78-125"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="f0a78-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="f0a78-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f0a78-126">Library</span></span><br/> | <dl> <span data-ttu-id="f0a78-127"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="f0a78-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0a78-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f0a78-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0a78-129">**Iamtimelinegroup-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="f0a78-129">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="f0a78-130">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="f0a78-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




