---
description: Die getdefaultfps-Methode ruft die Standardbildrate des Quell Objekts ab. Die Renderingengine verwendet diesen Wert, wenn Sie die Framerate aus der ursprünglichen Quelle nicht ermitteln kann.
ms.assetid: c167cd85-e9bb-46ff-9b35-c88898a6c5a3
title: 'Iamtimelinesrc:: getdefaultfps-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.GetDefaultFPS
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e48ee38f385ba5ff06b2ede9b27b4558dac65270
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367519"
---
# <a name="iamtimelinesrcgetdefaultfps-method"></a><span data-ttu-id="5de3f-104">Iamtimelinesrc:: getdefaultfps-Methode</span><span class="sxs-lookup"><span data-stu-id="5de3f-104">IAMTimelineSrc::GetDefaultFPS method</span></span>

> [!Note]  
> <span data-ttu-id="5de3f-105">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="5de3f-105">\[Deprecated.</span></span> <span data-ttu-id="5de3f-106">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="5de3f-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="5de3f-107">Die `GetDefaultFPS` -Methode ruft die Standardbildrate des Quell Objekts ab.</span><span class="sxs-lookup"><span data-stu-id="5de3f-107">The `GetDefaultFPS` method retrieves the source object's default frame rate.</span></span> <span data-ttu-id="5de3f-108">Die Renderingengine verwendet diesen Wert, wenn Sie die Framerate aus der ursprünglichen Quelle nicht ermitteln kann.</span><span class="sxs-lookup"><span data-stu-id="5de3f-108">The render engine uses this value if it cannot determine the frame rate from the original source.</span></span>

## <a name="syntax"></a><span data-ttu-id="5de3f-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="5de3f-109">Syntax</span></span>


```C++
HRESULT GetDefaultFPS(
   double *pFPS
);
```



## <a name="parameters"></a><span data-ttu-id="5de3f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="5de3f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5de3f-111">*pfps*</span><span class="sxs-lookup"><span data-stu-id="5de3f-111">*pFPS*</span></span> 
</dt> <dd>

<span data-ttu-id="5de3f-112">Empfängt die Standardbildrate in Frames pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="5de3f-112">Receives the default frame rate, in frames per second.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5de3f-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5de3f-113">Return value</span></span>

<span data-ttu-id="5de3f-114">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="5de3f-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5de3f-115">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5de3f-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5de3f-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5de3f-116">Remarks</span></span>

<span data-ttu-id="5de3f-117">Die Standardbildrate ist nicht erforderlich, wenn das Dateiformat die Framerate angibt.</span><span class="sxs-lookup"><span data-stu-id="5de3f-117">The default frame rate is not required if the file format specifies the frame rate.</span></span> <span data-ttu-id="5de3f-118">Dies ist der Fall bei Audio-und Videoformaten.</span><span class="sxs-lookup"><span data-stu-id="5de3f-118">This is the case for audio and video formats.</span></span>

<span data-ttu-id="5de3f-119">Wenn es sich bei der Quelle um ein Bitmap-oder JPEG-Bild handelt, verwendet die Renderingengine Sie als erstes Bild in einer geräteunabhängigen Bitmap-Sequenz (DIB) mit einer Frame Rate, die der Standard Frame Rate entspricht.</span><span class="sxs-lookup"><span data-stu-id="5de3f-119">If the source is a bitmap or JPEG image, the render engine uses it as the first image in a device-independent bitmap (DIB) sequence, with a frame rate equal to the default frame rate.</span></span> <span data-ttu-id="5de3f-120">Wenn Sie ein statisches Bild anstelle einer DIB-Sequenz darstellen möchten, legen Sie die Standardbildrate auf 0 fest.</span><span class="sxs-lookup"><span data-stu-id="5de3f-120">To render a static image, rather than a DIB sequence, set the default frame rate to 0.</span></span>

<span data-ttu-id="5de3f-121">Wenn die Quelle eine GIF ist, legen Sie die Framerate nicht fest.</span><span class="sxs-lookup"><span data-stu-id="5de3f-121">If the source is a GIF, do not set the frame rate.</span></span> <span data-ttu-id="5de3f-122">Bei animierten GIFs gibt die GIF-Datei die Verzögerung zwischen jedem Bild an.</span><span class="sxs-lookup"><span data-stu-id="5de3f-122">For animated GIFs, the GIF file specifies the delay between each image.</span></span>

> [!Note]  
> <span data-ttu-id="5de3f-123">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="5de3f-123">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="5de3f-124">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="5de3f-124">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="5de3f-125">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5de3f-125">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5de3f-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5de3f-126">Requirements</span></span>



| <span data-ttu-id="5de3f-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5de3f-127">Requirement</span></span> | <span data-ttu-id="5de3f-128">Wert</span><span class="sxs-lookup"><span data-stu-id="5de3f-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5de3f-129">Header</span><span class="sxs-lookup"><span data-stu-id="5de3f-129">Header</span></span><br/>  | <dl> <span data-ttu-id="5de3f-130"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="5de3f-130"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="5de3f-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5de3f-131">Library</span></span><br/> | <dl> <span data-ttu-id="5de3f-132"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="5de3f-132"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5de3f-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5de3f-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5de3f-134">**Iamtimelinesrc-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="5de3f-134">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="5de3f-135">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="5de3f-135">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




