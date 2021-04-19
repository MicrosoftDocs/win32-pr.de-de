---
description: Die setdefaultfps-Methode legt die Standard Frame Rate des Quell Objekts fest.
ms.assetid: ea93acde-3e05-43d5-8130-9ab2ee841b4e
title: 'Iamtimelinesrc:: setdefaultfps-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetDefaultFPS
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fd15f0606b1a4e4ee1aacdb1b3f56d63a024708b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362007"
---
# <a name="iamtimelinesrcsetdefaultfps-method"></a><span data-ttu-id="ebab7-103">Iamtimelinesrc:: setdefaultfps-Methode</span><span class="sxs-lookup"><span data-stu-id="ebab7-103">IAMTimelineSrc::SetDefaultFPS method</span></span>

> [!Note]  
> <span data-ttu-id="ebab7-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="ebab7-104">\[Deprecated.</span></span> <span data-ttu-id="ebab7-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="ebab7-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="ebab7-106">Die `SetDefaultFPS` -Methode legt die Standardbildrate des Quell Objekts fest.</span><span class="sxs-lookup"><span data-stu-id="ebab7-106">The `SetDefaultFPS` method sets the source object's default frame rate.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebab7-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ebab7-107">Syntax</span></span>


```C++
HRESULT SetDefaultFPS(
   double FPS
);
```



## <a name="parameters"></a><span data-ttu-id="ebab7-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ebab7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ebab7-109">*FPS*</span><span class="sxs-lookup"><span data-stu-id="ebab7-109">*FPS*</span></span> 
</dt> <dd>

<span data-ttu-id="ebab7-110">Standard Frame Rate in Frames pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="ebab7-110">Default frame rate, in frames per second.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ebab7-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ebab7-111">Return value</span></span>

<span data-ttu-id="ebab7-112">Gibt \_ bei Erfolg S OK oder E \_ invalidArg zurück, wenn die angegebene Framerate kleiner als 0 (null) ist.</span><span class="sxs-lookup"><span data-stu-id="ebab7-112">Returns S\_OK if successful, or E\_INVALIDARG if the specified frame rate is less than zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="ebab7-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ebab7-113">Remarks</span></span>

<span data-ttu-id="ebab7-114">Die Renderingengine verwendet diesen Wert, wenn Sie die Framerate der ursprünglichen Quelldatei nicht ermitteln kann.</span><span class="sxs-lookup"><span data-stu-id="ebab7-114">The render engine uses this value if it cannot determine the frame rate from the original source file.</span></span>

<span data-ttu-id="ebab7-115">Diese Methode wird nur für Quelldateien ohne vordefinierte Framerate aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="ebab7-115">Call this method only for source files without a predefined frame rate.</span></span> <span data-ttu-id="ebab7-116">Bei Bitmap-und JPEG-Dateien ist die Standardbildrate NULL. Dadurch wird die Quelle als Bild gerendert.</span><span class="sxs-lookup"><span data-stu-id="ebab7-116">For bitmap and JPEG files, the default frame rate is zero, which causes the source to be rendered as a still image.</span></span> <span data-ttu-id="ebab7-117">Um das Bild als ersten Frame in einer DIB-Sequenz zu verwenden, legen Sie die Framerate auf einen Wert größer als 0 (null) fest.</span><span class="sxs-lookup"><span data-stu-id="ebab7-117">To use the image as the first frame in a DIB sequence set the frame rate to a value greater than zero.</span></span> <span data-ttu-id="ebab7-118">Weitere Informationen finden Sie unter [Arbeiten mit Quellen](working-with-sources.md).</span><span class="sxs-lookup"><span data-stu-id="ebab7-118">For more information, see [Working with Sources](working-with-sources.md).</span></span>

> [!Note]  
> <span data-ttu-id="ebab7-119">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="ebab7-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="ebab7-120">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="ebab7-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="ebab7-121">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ebab7-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ebab7-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ebab7-122">Requirements</span></span>



| <span data-ttu-id="ebab7-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ebab7-123">Requirement</span></span> | <span data-ttu-id="ebab7-124">Wert</span><span class="sxs-lookup"><span data-stu-id="ebab7-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ebab7-125">Header</span><span class="sxs-lookup"><span data-stu-id="ebab7-125">Header</span></span><br/>  | <dl> <span data-ttu-id="ebab7-126"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="ebab7-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="ebab7-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ebab7-127">Library</span></span><br/> | <dl> <span data-ttu-id="ebab7-128"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="ebab7-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ebab7-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ebab7-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebab7-130">**Iamtimelinesrc-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="ebab7-130">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="ebab7-131">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="ebab7-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




