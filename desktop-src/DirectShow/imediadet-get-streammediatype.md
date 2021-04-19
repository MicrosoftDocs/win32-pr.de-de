---
description: Die get \_ streammediatype-Methode ruft den Medientyp des aktuellen Streams ab. Alle Videostreams werden in videoinfoheader-Typen konvertiert, und alle Audiodatenströme werden in WaveFormatEx-Typen konvertiert.
ms.assetid: 7fc15cb3-af77-42c1-b5eb-d1d88bf9cd1d
title: 'Imediadet:: get_StreamMediaType-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.get_StreamMediaType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0c2bea0c9cad7e1a25666cc38735107e14a884ec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373936"
---
# <a name="imediadetget_streammediatype-method"></a><span data-ttu-id="f9b85-104">Imediadet:: get \_ streammediatype-Methode</span><span class="sxs-lookup"><span data-stu-id="f9b85-104">IMediaDet::get\_StreamMediaType method</span></span>

> [!Note]  
> <span data-ttu-id="f9b85-105">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="f9b85-105">\[Deprecated.</span></span> <span data-ttu-id="f9b85-106">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="f9b85-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="f9b85-107">Die- `get_StreamMediaType` Methode ruft den Medientyp des aktuellen Streams ab.</span><span class="sxs-lookup"><span data-stu-id="f9b85-107">The `get_StreamMediaType` method retrieves the media type of the current stream.</span></span> <span data-ttu-id="f9b85-108">Alle Videostreams werden in [**videoinfoheader**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) -Typen konvertiert, und alle Audiodatenströme werden in [**WaveFormatEx**](/previous-versions/dd757713(v=vs.85)) -Typen konvertiert.</span><span class="sxs-lookup"><span data-stu-id="f9b85-108">All video streams are converted to [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) types, and all audio streams are converted to [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) types.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9b85-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="f9b85-109">Syntax</span></span>


```C++
HRESULT get_StreamMediaType(
  [out, retval] AM_MEDIA_TYPE *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="f9b85-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f9b85-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9b85-111">*PVal* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="f9b85-111">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="f9b85-112">Zeiger auf eine [**\_ \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) Struktur, die mit dem Medientyp gefüllt ist.</span><span class="sxs-lookup"><span data-stu-id="f9b85-112">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that is filled with the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9b85-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f9b85-113">Return value</span></span>

<span data-ttu-id="f9b85-114">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="f9b85-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f9b85-115">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f9b85-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9b85-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f9b85-116">Remarks</span></span>

<span data-ttu-id="f9b85-117">Bevor Sie diese Methode aufrufen, legen Sie den Dateinamen und den Stream durch Aufrufen von [**imediadet::p UT \_ filename**](imediadet-put-filename.md) und [**imediadet::p UT \_ currentstream**](imediadet-put-currentstream.md)fest.</span><span class="sxs-lookup"><span data-stu-id="f9b85-117">Before calling this method, set the file name and stream by calling [**IMediaDet::put\_Filename**](imediadet-put-filename.md) and [**IMediaDet::put\_CurrentStream**](imediadet-put-currentstream.md).</span></span>

<span data-ttu-id="f9b85-118">Wenn sich der Medien Detektor im bitmapingmodus befindet, gibt diese Methode E \_ invalidArg zurück.</span><span class="sxs-lookup"><span data-stu-id="f9b85-118">If the media detector is in bitmap grab mode, this method returns E\_INVALIDARG.</span></span> <span data-ttu-id="f9b85-119">Weitere Informationen finden Sie unter [**imediadet:: enterbitmapgrabmode**](imediadet-enterbitmapgrabmode.md).</span><span class="sxs-lookup"><span data-stu-id="f9b85-119">For more information, see [**IMediaDet::EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md).</span></span>

> [!Note]  
> <span data-ttu-id="f9b85-120">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="f9b85-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="f9b85-121">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="f9b85-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="f9b85-122">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f9b85-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f9b85-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f9b85-123">Requirements</span></span>



| <span data-ttu-id="f9b85-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f9b85-124">Requirement</span></span> | <span data-ttu-id="f9b85-125">Wert</span><span class="sxs-lookup"><span data-stu-id="f9b85-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f9b85-126">Header</span><span class="sxs-lookup"><span data-stu-id="f9b85-126">Header</span></span><br/>  | <dl> <span data-ttu-id="f9b85-127"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="f9b85-127"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="f9b85-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f9b85-128">Library</span></span><br/> | <dl> <span data-ttu-id="f9b85-129"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="f9b85-129"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9b85-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f9b85-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9b85-131">**Imediadet-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="f9b85-131">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="f9b85-132">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="f9b85-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 
