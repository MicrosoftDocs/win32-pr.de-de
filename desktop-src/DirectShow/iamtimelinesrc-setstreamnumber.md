---
description: Die setstreamnumber-Methode gibt an, welcher Stream aus der mit diesem Quell Objekt verknüpften Quelldatei gelesen werden soll.
ms.assetid: d40d0889-3b28-4114-9dd2-529e380eaeb8
title: 'Iamtimelinesrc:: setstreamnumber-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetStreamNumber
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 32deec91d4ae0fe55b4574344dd357932856db81
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373857"
---
# <a name="iamtimelinesrcsetstreamnumber-method"></a><span data-ttu-id="5a99f-103">Iamtimelinesrc:: setstreamnumber-Methode</span><span class="sxs-lookup"><span data-stu-id="5a99f-103">IAMTimelineSrc::SetStreamNumber method</span></span>

> [!Note]  
> <span data-ttu-id="5a99f-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="5a99f-104">\[Deprecated.</span></span> <span data-ttu-id="5a99f-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="5a99f-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="5a99f-106">Die- `SetStreamNumber` Methode gibt den Stream an, der aus der diesem Quell Objekt zugeordneten Quelldatei gelesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="5a99f-106">The `SetStreamNumber` method specifies which stream to read from the source file associated with this source object.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a99f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="5a99f-107">Syntax</span></span>


```C++
HRESULT SetStreamNumber(
   long Val
);
```



## <a name="parameters"></a><span data-ttu-id="5a99f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="5a99f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a99f-109">*Val*</span><span class="sxs-lookup"><span data-stu-id="5a99f-109">*Val*</span></span> 
</dt> <dd>

<span data-ttu-id="5a99f-110">Die streamnummer aus dem Satz von Streams, der mit dem Medientyp der übergeordneten Gruppe übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="5a99f-110">The stream number, from the set of streams matching the media type of the parent group.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a99f-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5a99f-111">Return value</span></span>

<span data-ttu-id="5a99f-112">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="5a99f-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5a99f-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5a99f-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a99f-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5a99f-114">Remarks</span></span>

<span data-ttu-id="5a99f-115">Der *Val* -Parameter gibt eine streamnummer aus dem Satz von Streams an, der mit dem Medientyp der übergeordneten Gruppe übereinstimmt, nicht aus dem gesamten Satz von Datenströmen in der Quelldatei.</span><span class="sxs-lookup"><span data-stu-id="5a99f-115">The *Val* parameter specifies a stream number from the set of streams that matches the parent group's media type, not from the entire set of streams in the source file.</span></span> <span data-ttu-id="5a99f-116">Angenommen, eine Datei enthält z. b. zwei Videostreams und zwei Audiodatenströme.</span><span class="sxs-lookup"><span data-stu-id="5a99f-116">For example, For example, suppose that a file contains two video streams and two audio streams.</span></span> <span data-ttu-id="5a99f-117">Wenn sich das Quell Objekt innerhalb einer Videogruppe befindet, wählt das Festlegen von *Val* auf 0 den ersten Videostream aus.</span><span class="sxs-lookup"><span data-stu-id="5a99f-117">If the source object is inside a video group, setting *Val* to 0 selects the first video stream.</span></span> <span data-ttu-id="5a99f-118">Der Aufrufer ist für das Angeben einer gültigen streamnummer verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="5a99f-118">The caller is responsible for specifying a valid stream number.</span></span>

<span data-ttu-id="5a99f-119">Die streamnummer ist standardmäßig 0 (null).</span><span class="sxs-lookup"><span data-stu-id="5a99f-119">The stream number defaults to zero.</span></span>

> [!Note]  
> <span data-ttu-id="5a99f-120">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="5a99f-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="5a99f-121">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="5a99f-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="5a99f-122">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5a99f-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5a99f-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5a99f-123">Requirements</span></span>



| <span data-ttu-id="5a99f-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5a99f-124">Requirement</span></span> | <span data-ttu-id="5a99f-125">Wert</span><span class="sxs-lookup"><span data-stu-id="5a99f-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5a99f-126">Header</span><span class="sxs-lookup"><span data-stu-id="5a99f-126">Header</span></span><br/>  | <dl> <span data-ttu-id="5a99f-127"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="5a99f-127"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="5a99f-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5a99f-128">Library</span></span><br/> | <dl> <span data-ttu-id="5a99f-129"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="5a99f-129"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a99f-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5a99f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a99f-131">**Iamtimelinesrc-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="5a99f-131">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="5a99f-132">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="5a99f-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




