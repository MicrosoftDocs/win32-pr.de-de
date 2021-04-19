---
description: Die Methode "*-martrecompressformat" gibt ein Video Komprimierungs Format an, das für die intelligente Neukomprimierung verwendet wird.
ms.assetid: 80c02215-6da2-4b3e-ab0d-004e49480fb9
title: Iamtimelinegroup::-Methode für das-martrecompressformat (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetSmartRecompressFormat
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9c8505f54d6ee9f6b2ec02216fd875fddbc619de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361424"
---
# <a name="iamtimelinegroupsetsmartrecompressformat-method"></a><span data-ttu-id="a9ce7-103">Iamtimelinegroup::.</span><span class="sxs-lookup"><span data-stu-id="a9ce7-103">IAMTimelineGroup::SetSmartRecompressFormat method</span></span>

> [!Note]  
> <span data-ttu-id="a9ce7-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="a9ce7-104">\[Deprecated.</span></span> <span data-ttu-id="a9ce7-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="a9ce7-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="a9ce7-106">Die `SetSmartRecompressFormat` Methode gibt ein Video Komprimierungs Format an, das für die intelligente Neukomprimierung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a9ce7-106">The `SetSmartRecompressFormat` method specifies a video compression format to use for smart recompression.</span></span>

<span data-ttu-id="a9ce7-107">Die intelligente Neukomprimierung wird für Audiogruppen nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a9ce7-107">Smart recompression is not supported for audio groups.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9ce7-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="a9ce7-108">Syntax</span></span>


```C++
HRESULT SetSmartRecompressFormat(
   long *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="a9ce7-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="a9ce7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9ce7-110">*pformat*</span><span class="sxs-lookup"><span data-stu-id="a9ce7-110">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="a9ce7-111">Zeiger auf eine-Struktur, die das Komprimierungs Format beschreibt.</span><span class="sxs-lookup"><span data-stu-id="a9ce7-111">Pointer to a structure describing the compression format.</span></span> <span data-ttu-id="a9ce7-112">Derzeit ist nur die [**SCompFmt0**](scompfmt0.md) -Struktur gültig.</span><span class="sxs-lookup"><span data-stu-id="a9ce7-112">Currently, only the [**SCompFmt0**](scompfmt0.md) structure is valid.</span></span> <span data-ttu-id="a9ce7-113">Sie müssen diesen Parameter in einen Zeiger vom Typ **Long** umwandeln.</span><span class="sxs-lookup"><span data-stu-id="a9ce7-113">You must cast this parameter to a pointer of type **long**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9ce7-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a9ce7-114">Return value</span></span>

<span data-ttu-id="a9ce7-115">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="a9ce7-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a9ce7-116">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a9ce7-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a9ce7-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a9ce7-117">Remarks</span></span>

<span data-ttu-id="a9ce7-118">Bevor Sie diese Methode aufrufen, rufen Sie die [**iamtimelinegroup:: setmediatype**](iamtimelinegroup-setmediatype.md) -Methode für die gleiche Gruppe auf, um ein nicht komprimiertes Format anzugeben.</span><span class="sxs-lookup"><span data-stu-id="a9ce7-118">Before calling this method, call the [**IAMTimelineGroup::SetMediaType**](iamtimelinegroup-setmediatype.md) method on the same group, to specify an uncompressed format.</span></span>

<span data-ttu-id="a9ce7-119">Wenn die `SetSmartRecompressFormat` Methode erfolgreich ist, können Sie die Smart-Rendering-Engine zum Ausgeben eines komprimierten Videodaten Stroms verwenden.</span><span class="sxs-lookup"><span data-stu-id="a9ce7-119">If the `SetSmartRecompressFormat` method succeeds, you can use the Smart Render Engine to output a compressed video stream.</span></span> <span data-ttu-id="a9ce7-120">Das komprimierte Video enthält die Breite, Höhe und Framerate, die im *pformat* -Parameter angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="a9ce7-120">The compressed video will have the width, height, and frame rate that was specified in the *pFormat* parameter.</span></span> <span data-ttu-id="a9ce7-121">Diese Werte überschreiben die Werte, die für das unkomprimierte Format in der **setmediatype** -Methode angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="a9ce7-121">These values will override those given for the uncompressed format in the **SetMediaType** method.</span></span> <span data-ttu-id="a9ce7-122">Um jedoch die Vorteile der intelligenten Neukomprimierung zu erzielen, sollten die beiden Formate identisch sein.</span><span class="sxs-lookup"><span data-stu-id="a9ce7-122">However, to get the benefits of smart recompression, the two formats should match.</span></span> <span data-ttu-id="a9ce7-123">Das heißt, die komprimierten und unkomprimierten Formate sollten die gleiche Höhe, Breite und Framerate aufweisen.</span><span class="sxs-lookup"><span data-stu-id="a9ce7-123">In other words, the compressed and uncompressed formats should have the same height, width, and frame rate.</span></span>

<span data-ttu-id="a9ce7-124">Wenn die Smart-Rendering-Engine das komprimierte Format nicht erzeugen kann, wird stattdessen ein unkomprimierter Videostream erzeugt.</span><span class="sxs-lookup"><span data-stu-id="a9ce7-124">If the Smart Render Engine is unable to produce the compressed format, it will produce an uncompressed video stream instead.</span></span> <span data-ttu-id="a9ce7-125">Wenn dies der Fall ist, meldet das Smart-Rendering-Modul \_ \_ \_ \_ bei der Methode " [**unenderengine:: connectfrontend**](irenderengine-connectfrontend.md) " eine DEX-ID nicht.</span><span class="sxs-lookup"><span data-stu-id="a9ce7-125">If that occurs, the Smart Render Engine reports a DEX\_IDS\_CANT\_FIND\_COMPRESSOR rendering error during the [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md) method.</span></span> <span data-ttu-id="a9ce7-126">Die Anwendung kann diesen Fehler durch die [**iamerrorlog:: LogError**](iamerrorlog-logerror.md) -Methode abfangen.</span><span class="sxs-lookup"><span data-stu-id="a9ce7-126">The application can catch this error through the [**IAMErrorLog::LogError**](iamerrorlog-logerror.md) method.</span></span> <span data-ttu-id="a9ce7-127">(Weitere Informationen finden Sie unter [Protokollieren von Fehlern](logging-errors.md) und [Rendern von Fehlern](rendering-errors.md).)</span><span class="sxs-lookup"><span data-stu-id="a9ce7-127">(For more information, see [Logging Errors](logging-errors.md) and [Rendering Errors](rendering-errors.md).)</span></span>

<span data-ttu-id="a9ce7-128">Das Format der intelligenten Neukomprimierung ist nicht persistent.</span><span class="sxs-lookup"><span data-stu-id="a9ce7-128">The smart recompression format is not persistent.</span></span> <span data-ttu-id="a9ce7-129">Wenn eine Anwendung eine intelligente Neukomprimierung verwendet, muss Sie beim Laden einer Projektdatei das neukomprimierungs Format festlegen.</span><span class="sxs-lookup"><span data-stu-id="a9ce7-129">If an application uses smart recompression, it must set the recompression format whenever it loads a project file.</span></span>

> [!Note]  
> <span data-ttu-id="a9ce7-130">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="a9ce7-130">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="a9ce7-131">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="a9ce7-131">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="a9ce7-132">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a9ce7-132">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a9ce7-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a9ce7-133">Requirements</span></span>



| <span data-ttu-id="a9ce7-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a9ce7-134">Requirement</span></span> | <span data-ttu-id="a9ce7-135">Wert</span><span class="sxs-lookup"><span data-stu-id="a9ce7-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a9ce7-136">Header</span><span class="sxs-lookup"><span data-stu-id="a9ce7-136">Header</span></span><br/>  | <dl> <span data-ttu-id="a9ce7-137"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="a9ce7-137"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="a9ce7-138">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a9ce7-138">Library</span></span><br/> | <dl> <span data-ttu-id="a9ce7-139"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="a9ce7-139"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9ce7-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a9ce7-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9ce7-141">**Iamtimelinegroup-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="a9ce7-141">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="a9ce7-142">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="a9ce7-142">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> <dt>

[<span data-ttu-id="a9ce7-143">Smart-Rendering-Engine</span><span class="sxs-lookup"><span data-stu-id="a9ce7-143">Smart Render Engine</span></span>](smart-render-engine.md)
</dt> <dt>

[<span data-ttu-id="a9ce7-144">Schreiben eines Projekts in eine Datei</span><span class="sxs-lookup"><span data-stu-id="a9ce7-144">Writing a Project to a File</span></span>](writing-a-project-to-a-file.md)
</dt> </dl>

 

 




