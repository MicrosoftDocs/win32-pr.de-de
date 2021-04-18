---
description: Die get \_ Streamtype-Methode ruft die Globally Unique Identifier (GUID) für den Medientyp des aktuellen Streams ab.
ms.assetid: 2f61b3fe-c041-4031-9211-2f5fc189542b
title: 'Imediadet:: get_StreamType-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.get_StreamType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5834183229580c1aadbcbe80e54a30e9b9b60c03
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361445"
---
# <a name="imediadetget_streamtype-method"></a><span data-ttu-id="e62c6-103">Imediadet:: get \_ Streamtype-Methode</span><span class="sxs-lookup"><span data-stu-id="e62c6-103">IMediaDet::get\_StreamType method</span></span>

> [!Note]  
> <span data-ttu-id="e62c6-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="e62c6-104">\[Deprecated.</span></span> <span data-ttu-id="e62c6-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="e62c6-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="e62c6-106">Die- `get_StreamType` Methode ruft die Globally Unique Identifier (GUID) für den Medientyp des aktuellen Streams ab.</span><span class="sxs-lookup"><span data-stu-id="e62c6-106">The `get_StreamType` method retrieves the globally unique identifier (GUID) for the media type of the current stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="e62c6-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e62c6-107">Syntax</span></span>


```C++
HRESULT get_StreamType(
  [out, retval] GUID *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="e62c6-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e62c6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e62c6-109">*PVal* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="e62c6-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="e62c6-110">Empfängt die GUID des Haupt Typs für den Medientyp.</span><span class="sxs-lookup"><span data-stu-id="e62c6-110">Receives the major type GUID for the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e62c6-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e62c6-111">Return value</span></span>

<span data-ttu-id="e62c6-112">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="e62c6-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e62c6-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e62c6-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e62c6-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e62c6-114">Remarks</span></span>

<span data-ttu-id="e62c6-115">Diese Methode ruft den **majortype** -Member der Struktur des [**am- \_ Medien \_ Typs**](/windows/win32/api/strmif/ns-strmif-am_media_type) ab.</span><span class="sxs-lookup"><span data-stu-id="e62c6-115">This method retrieves the **majortype** member of the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span> <span data-ttu-id="e62c6-116">Die **am \_ Medientyp \_** -Struktur beschreibt das Format des Streams, und der **majortype** -Member ist eine GUID, die die allgemeine Kategorie angibt, z. b. Audiodaten oder Videos.</span><span class="sxs-lookup"><span data-stu-id="e62c6-116">The **AM\_MEDIA\_TYPE** structure describes the format of the stream, and the **majortype** member is a GUID that indicates the general category, such as audio or video.</span></span> <span data-ttu-id="e62c6-117">Bei einem Videostream ist die GUID MediaType \_ Video.</span><span class="sxs-lookup"><span data-stu-id="e62c6-117">For a video stream, the GUID is MEDIATYPE\_Video.</span></span> <span data-ttu-id="e62c6-118">Bei Audiodaten handelt es sich um MediaType \_ -Audiodaten.</span><span class="sxs-lookup"><span data-stu-id="e62c6-118">For audio, it is MEDIATYPE\_Audio.</span></span> <span data-ttu-id="e62c6-119">Um die gesamte **\_ \_ Medientyp** Struktur abzurufen, rufen Sie die [**imediadet:: get \_ streammediatype**](imediadet-get-streammediatype.md) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="e62c6-119">To retrieve the entire **AM\_MEDIA\_TYPE** structure, call the [**IMediaDet::get\_StreamMediaType**](imediadet-get-streammediatype.md) method.</span></span>

<span data-ttu-id="e62c6-120">Bevor Sie diese Methode aufrufen, legen Sie den Dateinamen und den Stream durch Aufrufen von [**imediadet::p UT \_ filename**](imediadet-put-filename.md) und [**imediadet::p UT \_ currentstream**](imediadet-put-currentstream.md)fest.</span><span class="sxs-lookup"><span data-stu-id="e62c6-120">Before calling this method, set the file name and stream by calling [**IMediaDet::put\_Filename**](imediadet-put-filename.md) and [**IMediaDet::put\_CurrentStream**](imediadet-put-currentstream.md).</span></span>

<span data-ttu-id="e62c6-121">Wenn sich der Medien Detektor im bitmapingmodus befindet, gibt diese Methode E \_ invalidArg zurück.</span><span class="sxs-lookup"><span data-stu-id="e62c6-121">If the media detector is in bitmap grab mode, this method returns E\_INVALIDARG.</span></span> <span data-ttu-id="e62c6-122">Weitere Informationen finden Sie unter [**imediadet:: enterbitmapgrabmode**](imediadet-enterbitmapgrabmode.md).</span><span class="sxs-lookup"><span data-stu-id="e62c6-122">For more information, see [**IMediaDet::EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md).</span></span>

> [!Note]  
> <span data-ttu-id="e62c6-123">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="e62c6-123">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="e62c6-124">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="e62c6-124">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="e62c6-125">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e62c6-125">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e62c6-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e62c6-126">Requirements</span></span>



| <span data-ttu-id="e62c6-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e62c6-127">Requirement</span></span> | <span data-ttu-id="e62c6-128">Wert</span><span class="sxs-lookup"><span data-stu-id="e62c6-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e62c6-129">Header</span><span class="sxs-lookup"><span data-stu-id="e62c6-129">Header</span></span><br/>  | <dl> <span data-ttu-id="e62c6-130"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="e62c6-130"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="e62c6-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e62c6-131">Library</span></span><br/> | <dl> <span data-ttu-id="e62c6-132"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="e62c6-132"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e62c6-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e62c6-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e62c6-134">**Imediadet-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="e62c6-134">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="e62c6-135">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="e62c6-135">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




