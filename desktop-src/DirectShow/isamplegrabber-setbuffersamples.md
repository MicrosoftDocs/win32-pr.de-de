---
description: Die setbuffersamples-Methode gibt an, ob Beispiel Daten beim Durchlaufen des Filters in einen Puffer kopiert werden sollen.
ms.assetid: 1ef4508e-441f-45e0-afb4-239dd947284b
title: 'Isamplegrabber:: setbuffersamples-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber.SetBufferSamples
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9fab426b7bcad1a12895f632a719a40b4aaa8da4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371432"
---
# <a name="isamplegrabbersetbuffersamples-method"></a><span data-ttu-id="bd936-103">Isamplegrabber:: setbuffersamples-Methode</span><span class="sxs-lookup"><span data-stu-id="bd936-103">ISampleGrabber::SetBufferSamples method</span></span>

> [!Note]  
> <span data-ttu-id="bd936-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="bd936-104">\[Deprecated.</span></span> <span data-ttu-id="bd936-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="bd936-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="bd936-106">Die **setbuffersamples** -Methode gibt an, ob Beispiel Daten beim Durchlaufen des Filters in einen Puffer kopiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="bd936-106">The **SetBufferSamples** method specifies whether to copy sample data into a buffer as it goes through the filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd936-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="bd936-107">Syntax</span></span>


```C++
void SetBufferSamples(
   BOOL BufferThem
);
```



## <a name="parameters"></a><span data-ttu-id="bd936-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="bd936-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd936-109">*Puffer*</span><span class="sxs-lookup"><span data-stu-id="bd936-109">*BufferThem*</span></span> 
</dt> <dd>

<span data-ttu-id="bd936-110">Boolescher Wert, der angibt, ob Beispiel Daten gepuffert werden.</span><span class="sxs-lookup"><span data-stu-id="bd936-110">Boolean value specifying whether to buffer sample data.</span></span> <span data-ttu-id="bd936-111">**True** gibt an, dass der Filter Beispiel Daten in einen internen Puffer kopiert.</span><span class="sxs-lookup"><span data-stu-id="bd936-111">If **TRUE**, the filter copies sample data into an internal buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd936-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bd936-112">Return value</span></span>

<span data-ttu-id="bd936-113">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="bd936-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd936-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bd936-114">Remarks</span></span>

<span data-ttu-id="bd936-115">Um den kopierten Puffer abzurufen, nennen Sie [**isamplegrabber:: getcurrentbuffer**](isamplegrabber-getcurrentbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="bd936-115">To get the copied buffer, call [**ISampleGrabber::GetCurrentBuffer**](isamplegrabber-getcurrentbuffer.md).</span></span>

> [!Note]  
> <span data-ttu-id="bd936-116">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="bd936-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="bd936-117">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="bd936-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="bd936-118">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="bd936-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="bd936-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bd936-119">Requirements</span></span>



| <span data-ttu-id="bd936-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bd936-120">Requirement</span></span> | <span data-ttu-id="bd936-121">Wert</span><span class="sxs-lookup"><span data-stu-id="bd936-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bd936-122">Header</span><span class="sxs-lookup"><span data-stu-id="bd936-122">Header</span></span><br/>  | <dl> <span data-ttu-id="bd936-123"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="bd936-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="bd936-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="bd936-124">Library</span></span><br/> | <dl> <span data-ttu-id="bd936-125"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="bd936-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd936-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bd936-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd936-127">Verwenden der Beispiel-Grabber</span><span class="sxs-lookup"><span data-stu-id="bd936-127">Using the Sample Grabber</span></span>](using-the-sample-grabber.md)
</dt> <dt>

[<span data-ttu-id="bd936-128">**Isamplegrabber-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="bd936-128">**ISampleGrabber Interface**</span></span>](isamplegrabber.md)
</dt> </dl>

 

 




