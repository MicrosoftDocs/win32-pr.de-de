---
description: Die SetCallback-Methode gibt eine Rückruf Methode an, die für eingehende Stichproben aufgerufen wird.
ms.assetid: b84d3f52-b986-492a-a8b9-1d98618dcdd3
title: 'Isamplegrabber:: SetCallback-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber.SetCallback
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 46e0565c314bab86967ee0d5dabee6ba449a87dd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360934"
---
# <a name="isamplegrabbersetcallback-method"></a><span data-ttu-id="1b77b-103">Isamplegrabber:: SetCallback-Methode</span><span class="sxs-lookup"><span data-stu-id="1b77b-103">ISampleGrabber::SetCallback method</span></span>

> [!Note]  
> <span data-ttu-id="1b77b-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="1b77b-104">\[Deprecated.</span></span> <span data-ttu-id="1b77b-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="1b77b-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="1b77b-106">Die **SetCallback** -Methode gibt eine Rückruf Methode an, die für eingehende Stichproben aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="1b77b-106">The **SetCallback** method specifies a callback method to call on incoming samples.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b77b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="1b77b-107">Syntax</span></span>


```C++
HRESULT SetCallback(
   ISampleGrabberCB *pCallback,
   long             WhichMethodToCallback
);
```



## <a name="parameters"></a><span data-ttu-id="1b77b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="1b77b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b77b-109">*pCallback*</span><span class="sxs-lookup"><span data-stu-id="1b77b-109">*pCallback*</span></span> 
</dt> <dd>

<span data-ttu-id="1b77b-110">Zeiger auf eine [**isamplegrabbercb**](isamplegrabbercb.md) -Schnittstelle, die die Rückruf Methode enthält, oder **null** , um den Rückruf abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="1b77b-110">Pointer to an [**ISampleGrabberCB**](isamplegrabbercb.md) interface containing the callback method, or **NULL** to cancel the callback.</span></span>

</dd> <dt>

<span data-ttu-id="1b77b-111">*Whichmethodumcallback*</span><span class="sxs-lookup"><span data-stu-id="1b77b-111">*WhichMethodToCallback*</span></span> 
</dt> <dd>

<span data-ttu-id="1b77b-112">Der Index, der die Rückruf Methode angibt.</span><span class="sxs-lookup"><span data-stu-id="1b77b-112">Index specifying the callback method.</span></span> <span data-ttu-id="1b77b-113">Muss einen der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="1b77b-113">Must be one of the following values.</span></span>



| <span data-ttu-id="1b77b-114">Wert</span><span class="sxs-lookup"><span data-stu-id="1b77b-114">Value</span></span> | <span data-ttu-id="1b77b-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1b77b-115">Description</span></span>                                                                                                                                                                                     |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b77b-116">0</span><span class="sxs-lookup"><span data-stu-id="1b77b-116">0</span></span>     | <span data-ttu-id="1b77b-117">Der Beispiel-Grabber Filter Ruft die [**isamplegrabbercb:: samplecb**](isamplegrabbercb-samplecb.md) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="1b77b-117">The Sample Grabber filter calls the [**ISampleGrabberCB::SampleCB**](isamplegrabbercb-samplecb.md) method.</span></span> <span data-ttu-id="1b77b-118">Diese Methode empfängt einen [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) -Zeiger.</span><span class="sxs-lookup"><span data-stu-id="1b77b-118">This method receives an [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) pointer.</span></span>               |
| <span data-ttu-id="1b77b-119">1</span><span class="sxs-lookup"><span data-stu-id="1b77b-119">1</span></span>     | <span data-ttu-id="1b77b-120">Der Beispiel-Grabber Filter Ruft die [**isamplegrabbercb:: buffercb**](isamplegrabbercb-buffercb.md) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="1b77b-120">The Sample Grabber filter calls the [**ISampleGrabberCB::BufferCB**](isamplegrabbercb-buffercb.md) method.</span></span> <span data-ttu-id="1b77b-121">Diese Methode empfängt einen Zeiger auf den Puffer, der im Medien Beispiel enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="1b77b-121">This method receives a pointer to the buffer that is contained in the media sample.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b77b-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1b77b-122">Return value</span></span>

<span data-ttu-id="1b77b-123">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="1b77b-123">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1b77b-124">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1b77b-124">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b77b-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1b77b-125">Remarks</span></span>

<span data-ttu-id="1b77b-126">Der Datenverarbeitungs Thread wird blockiert, bis die Rückruf Methode zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="1b77b-126">The data processing thread blocks until the callback method returns.</span></span> <span data-ttu-id="1b77b-127">Wenn der Rückruf nicht schnell zurückgegeben wird, kann er die Wiedergabe beeinträchtigen.</span><span class="sxs-lookup"><span data-stu-id="1b77b-127">If the callback does not return quickly, it can interfere with playback.</span></span>

<span data-ttu-id="1b77b-128">Der Filter ruft nicht die Rückruffunktion für ein Vorlauf ausgeführt-Beispiele oder Beispiele auf, bei denen das **dwstreamid** -Element der " [**am \_ SAMPLE2 \_ Properties**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) "-Struktur etwas anderes als "am-Stream-Medien" ist \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="1b77b-128">The filter does not invoke the callback function for preroll samples, or for samples in which the **dwStreamId** member of the [**AM\_SAMPLE2\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) structure is anything other than AM\_STREAM\_MEDIA.</span></span>

> [!Note]  
> <span data-ttu-id="1b77b-129">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="1b77b-129">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="1b77b-130">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="1b77b-130">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="1b77b-131">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="1b77b-131">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1b77b-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1b77b-132">Requirements</span></span>



| <span data-ttu-id="1b77b-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1b77b-133">Requirement</span></span> | <span data-ttu-id="1b77b-134">Wert</span><span class="sxs-lookup"><span data-stu-id="1b77b-134">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1b77b-135">Header</span><span class="sxs-lookup"><span data-stu-id="1b77b-135">Header</span></span><br/>  | <dl> <span data-ttu-id="1b77b-136"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="1b77b-136"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="1b77b-137">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1b77b-137">Library</span></span><br/> | <dl> <span data-ttu-id="1b77b-138"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="1b77b-138"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b77b-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1b77b-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b77b-140">Verwenden der Beispiel-Grabber</span><span class="sxs-lookup"><span data-stu-id="1b77b-140">Using the Sample Grabber</span></span>](using-the-sample-grabber.md)
</dt> <dt>

[<span data-ttu-id="1b77b-141">**Isamplegrabber-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="1b77b-141">**ISampleGrabber Interface**</span></span>](isamplegrabber.md)
</dt> </dl>

 

 




