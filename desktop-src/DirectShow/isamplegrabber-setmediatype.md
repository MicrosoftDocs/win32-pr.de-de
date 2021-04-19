---
description: Die setmediatype-Methode gibt den Medientyp für die Verbindung in der Eingabe-PIN der Sample Grabber an.
ms.assetid: 9568832f-6666-45c9-9421-485c877affb3
title: 'Isamplegrabber:: setmediatype-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber.SetMediaType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a39aa79e9311fe3491d0925fdc1b2dd3b1cc65c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365784"
---
# <a name="isamplegrabbersetmediatype-method"></a><span data-ttu-id="4cab5-103">Isamplegrabber:: setmediatype-Methode</span><span class="sxs-lookup"><span data-stu-id="4cab5-103">ISampleGrabber::SetMediaType method</span></span>

> [!Note]  
> <span data-ttu-id="4cab5-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="4cab5-104">\[Deprecated.</span></span> <span data-ttu-id="4cab5-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="4cab5-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="4cab5-106">Die- `SetMediaType` Methode gibt den Medientyp für die Verbindung in der Eingabe-PIN der Sample Grabber an.</span><span class="sxs-lookup"><span data-stu-id="4cab5-106">The `SetMediaType` method specifies the media type for the connection on the input pin of the Sample Grabber.</span></span>

## <a name="syntax"></a><span data-ttu-id="4cab5-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="4cab5-107">Syntax</span></span>


```C++
HRESULT SetMediaType(
   const AM_MEDIA_TYPE *pType
);
```



## <a name="parameters"></a><span data-ttu-id="4cab5-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="4cab5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4cab5-109">*pType*</span><span class="sxs-lookup"><span data-stu-id="4cab5-109">*pType*</span></span> 
</dt> <dd>

<span data-ttu-id="4cab5-110">Ein Zeiger auf eine [**am- \_ \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) Struktur gibt den erforderlichen Medientyp an.</span><span class="sxs-lookup"><span data-stu-id="4cab5-110">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure specifies the required media type.</span></span> <span data-ttu-id="4cab5-111">Es ist nicht erforderlich, alle Strukturmember festzulegen. Weitere Informationen finden Sie in den hinweisen.</span><span class="sxs-lookup"><span data-stu-id="4cab5-111">It is not necessary to set all the structure members; see Remarks for details.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4cab5-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4cab5-112">Return value</span></span>

<span data-ttu-id="4cab5-113">Gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="4cab5-113">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="4cab5-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4cab5-114">Remarks</span></span>

<span data-ttu-id="4cab5-115">Standardmäßig hat der beispielgrabber keinen bevorzugten Medientyp.</span><span class="sxs-lookup"><span data-stu-id="4cab5-115">By default, the Sample Grabber has no preferred media type.</span></span> <span data-ttu-id="4cab5-116">Um sicherzustellen, dass der Sample Grabber eine Verbindung mit dem richtigen Filter herstellt, müssen Sie diese Methode vor dem Aufbau des Filter Diagramms abrufen.</span><span class="sxs-lookup"><span data-stu-id="4cab5-116">To ensure that the Sample Grabber connects to the correct filter, call this method before building the filter graph.</span></span>

<span data-ttu-id="4cab5-117">Diese Methode schränkt den Bereich der Medientypen ein, den der Filter akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="4cab5-117">This method restricts the range of media types that the filter will accept.</span></span> <span data-ttu-id="4cab5-118">Wenn der Filter eine Verbindung herstellt, versucht er, den in *pType* angegebenen Medientyp abzugleichen.</span><span class="sxs-lookup"><span data-stu-id="4cab5-118">When the filter connects, it tries to match the media type given in *pType*.</span></span> <span data-ttu-id="4cab5-119">Zu diesem Zweck werden der Haupttyp, der Untertyp und die Formattyp-GUIDs in dieser Reihenfolge verglichen.</span><span class="sxs-lookup"><span data-stu-id="4cab5-119">To do so, it compares the major type, subtype, and format type GUIDs, in that order.</span></span> <span data-ttu-id="4cab5-120">Wenn *pType* für jede dieser GUIDs den Wert GUID \_ null hat, akzeptiert der beispielgrabber den Medientyp ohne weitere Überprüfungen.</span><span class="sxs-lookup"><span data-stu-id="4cab5-120">For each of these GUIDs, if *pType* has the value GUID\_NULL, the Sample Grabber accepts the media type without any further checks.</span></span> <span data-ttu-id="4cab5-121">Wenn *pType* einen anderen Wert aufweist, vergleicht der Sample Grabber ihn mit der GUID im Verbindungstyp.</span><span class="sxs-lookup"><span data-stu-id="4cab5-121">If *pType* has any other value, the Sample Grabber compares it to the GUID in the connection type.</span></span> <span data-ttu-id="4cab5-122">Wenn die beiden GUIDs nicht exakt übereinstimmen, lehnt der Beispiel-Grabber die Verbindung ab.</span><span class="sxs-lookup"><span data-stu-id="4cab5-122">Unless the two GUIDs match exactly, the Sample Grabber rejects the connection.</span></span>

<span data-ttu-id="4cab5-123">Bei Video Medientypen ignoriert der Sample Grabber den Format Block.</span><span class="sxs-lookup"><span data-stu-id="4cab5-123">For video media types, the Sample Grabber ignores the format block.</span></span> <span data-ttu-id="4cab5-124">Aus diesem Grund werden die Videogröße und die Framerate akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="4cab5-124">Therefore, it will accept any video size and frame rate.</span></span> <span data-ttu-id="4cab5-125">Wenn Sie aufzurufen `SetMediaType` , legen Sie den Format Block (**pbformat**) auf **null** und die Größe (**cbformat**) auf 0 (null) fest.</span><span class="sxs-lookup"><span data-stu-id="4cab5-125">When you call `SetMediaType`, set the format block (**pbFormat**) to **NULL** and the size (**cbFormat**) to zero.</span></span> <span data-ttu-id="4cab5-126">Für audiomedientyp untersucht der Beispiel-Grabber die [**WaveFormatEx**](/previous-versions/dd757713(v=vs.85)) -Struktur und erfordert, dass der andere Filter eine Verbindung mit diesem Format herstellt – es sei denn, der Format Block in *pType* ist **null**, oder das Format-Tag ist das Wave \_ \_ -Format PCM, und die anderen Strukturmember sind 0 (null).</span><span class="sxs-lookup"><span data-stu-id="4cab5-126">For audio media types, the Sample Grabber will examine the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure and will require the other filter to connect with that format — unless the format block in *pType* is **NULL**, or the format tag is WAVE\_FORMAT\_PCM and the other structure members are zero.</span></span>

<span data-ttu-id="4cab5-127">Beispiel 1:</span><span class="sxs-lookup"><span data-stu-id="4cab5-127">Example 1:</span></span>

-   <span data-ttu-id="4cab5-128">Haupttyp: MediaType- \_ Video</span><span class="sxs-lookup"><span data-stu-id="4cab5-128">Major type: MEDIATYPE\_Video</span></span>
-   <span data-ttu-id="4cab5-129">Untertyp: GUID \_ null</span><span class="sxs-lookup"><span data-stu-id="4cab5-129">Subtype: GUID\_NULL</span></span>
-   <span data-ttu-id="4cab5-130">Formattyp: GUID \_ null</span><span class="sxs-lookup"><span data-stu-id="4cab5-130">Format type: GUID\_NULL</span></span>

<span data-ttu-id="4cab5-131">Der beispielgrabber akzeptiert jeden Videotyp, bei dem der Haupttyp dem Video "MediaType" gleicht \_ .</span><span class="sxs-lookup"><span data-stu-id="4cab5-131">The Sample Grabber will accept any video type where the major type equals MEDIATYPE\_Video.</span></span> <span data-ttu-id="4cab5-132">Der Untertyp wird nicht überprüft.</span><span class="sxs-lookup"><span data-stu-id="4cab5-132">It will not check the subtype.</span></span>

<span data-ttu-id="4cab5-133">Beispiel 2:</span><span class="sxs-lookup"><span data-stu-id="4cab5-133">Example 2:</span></span>

-   <span data-ttu-id="4cab5-134">Haupttyp: MediaType- \_ Video</span><span class="sxs-lookup"><span data-stu-id="4cab5-134">Major type: MEDIATYPE\_Video</span></span>
-   <span data-ttu-id="4cab5-135">Untertyp: mediasubtype \_ RGB24</span><span class="sxs-lookup"><span data-stu-id="4cab5-135">Subtype: MEDIASUBTYPE\_RGB24</span></span>
-   <span data-ttu-id="4cab5-136">Formattyp: GUID \_ null</span><span class="sxs-lookup"><span data-stu-id="4cab5-136">Format type: GUID\_NULL</span></span>

<span data-ttu-id="4cab5-137">Nun prüft der Sample Grabber den Untertyp und akzeptiert nur RGB 24-Videos.</span><span class="sxs-lookup"><span data-stu-id="4cab5-137">Now the Sample Grabber will check the subtype, and accept only RGB 24 video.</span></span>

<span data-ttu-id="4cab5-138">**Einschränkungen:** Unabhängig davon, welchen Typ Sie festlegen, lehnt der Sample Grabber Filter alle Video Typen mit der Top-Down-Ausrichtung (negative *biheight*) oder dem Formattyp Format \_ VideoInfo2 ab.</span><span class="sxs-lookup"><span data-stu-id="4cab5-138">**Limitations:** Regardless of what type you set, the Sample Grabber Filter rejects any video types with top-down orientation (negative *biHeight*), or with a format type of FORMAT\_VideoInfo2.</span></span> <span data-ttu-id="4cab5-139">In diesem Fall stellt `SetMediaType` der Filter keine Verbindung her, obwohl die Methode erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4cab5-139">In this case, although the `SetMediaType` method succeeds, the filter will not connect.</span></span>

> [!Note]  
> <span data-ttu-id="4cab5-140">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="4cab5-140">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="4cab5-141">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="4cab5-141">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="4cab5-142">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4cab5-142">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4cab5-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4cab5-143">Requirements</span></span>



| <span data-ttu-id="4cab5-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4cab5-144">Requirement</span></span> | <span data-ttu-id="4cab5-145">Wert</span><span class="sxs-lookup"><span data-stu-id="4cab5-145">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4cab5-146">Header</span><span class="sxs-lookup"><span data-stu-id="4cab5-146">Header</span></span><br/>  | <dl> <span data-ttu-id="4cab5-147"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="4cab5-147"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="4cab5-148">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4cab5-148">Library</span></span><br/> | <dl> <span data-ttu-id="4cab5-149"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="4cab5-149"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4cab5-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4cab5-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cab5-151">Verwenden der Beispiel-Grabber</span><span class="sxs-lookup"><span data-stu-id="4cab5-151">Using the Sample Grabber</span></span>](using-the-sample-grabber.md)
</dt> <dt>

[<span data-ttu-id="4cab5-152">**Isamplegrabber-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="4cab5-152">**ISampleGrabber Interface**</span></span>](isamplegrabber.md)
</dt> </dl>

 

 
