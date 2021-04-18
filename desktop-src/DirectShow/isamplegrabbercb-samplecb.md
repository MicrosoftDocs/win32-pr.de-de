---
description: Die samplecb-Methode ist eine Rückruf Methode, die einen Zeiger auf das Medien Beispiel empfängt.
ms.assetid: e919b694-75cb-48c6-8427-5a7a886e0ff3
title: 'Isamplegrabbercb:: samplecb-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabberCB.SampleCB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 6e66f4a43666add7a5d6cb579fcf15f0fc1ec0cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365619"
---
# <a name="isamplegrabbercbsamplecb-method"></a><span data-ttu-id="17e16-103">Isamplegrabbercb:: samplecb-Methode</span><span class="sxs-lookup"><span data-stu-id="17e16-103">ISampleGrabberCB::SampleCB method</span></span>

> [!Note]  
> <span data-ttu-id="17e16-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="17e16-104">\[Deprecated.</span></span> <span data-ttu-id="17e16-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="17e16-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="17e16-106">Die- `SampleCB` Methode ist eine Rückruf Methode, die einen Zeiger auf das Medien Beispiel empfängt.</span><span class="sxs-lookup"><span data-stu-id="17e16-106">The `SampleCB` method is a callback method that receives a pointer to the media sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="17e16-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="17e16-107">Syntax</span></span>


```C++
HRESULT SampleCB(
   double       SampleTime,
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="17e16-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="17e16-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17e16-109">*Sampletime*</span><span class="sxs-lookup"><span data-stu-id="17e16-109">*SampleTime*</span></span> 
</dt> <dd>

<span data-ttu-id="17e16-110">Startzeit des Beispiels in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="17e16-110">Starting time of the sample, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="17e16-111">*psample*</span><span class="sxs-lookup"><span data-stu-id="17e16-111">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="17e16-112">Zeiger auf die [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) -Schnittstelle des Beispiels.</span><span class="sxs-lookup"><span data-stu-id="17e16-112">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface of the sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17e16-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="17e16-113">Return value</span></span>

<span data-ttu-id="17e16-114">Gibt \_ bei Erfolg S OK oder andernfalls einen **HRESULT** -Fehlercode zurück.</span><span class="sxs-lookup"><span data-stu-id="17e16-114">Returns S\_OK if successful, or an **HRESULT** error code otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="17e16-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="17e16-115">Remarks</span></span>

<span data-ttu-id="17e16-116">Rufen Sie zum Einrichten des Rückrufs [**isamplegrabber:: SetCallback**](isamplegrabber-setcallback.md)auf.</span><span class="sxs-lookup"><span data-stu-id="17e16-116">To set up the callback, call [**ISampleGrabber::SetCallback**](isamplegrabber-setcallback.md).</span></span>

> [!Note]  
> <span data-ttu-id="17e16-117">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="17e16-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="17e16-118">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="17e16-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="17e16-119">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="17e16-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="17e16-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="17e16-120">Requirements</span></span>



| <span data-ttu-id="17e16-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="17e16-121">Requirement</span></span> | <span data-ttu-id="17e16-122">Wert</span><span class="sxs-lookup"><span data-stu-id="17e16-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="17e16-123">Header</span><span class="sxs-lookup"><span data-stu-id="17e16-123">Header</span></span><br/>  | <dl> <span data-ttu-id="17e16-124"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="17e16-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="17e16-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="17e16-125">Library</span></span><br/> | <dl> <span data-ttu-id="17e16-126"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="17e16-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17e16-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="17e16-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17e16-128">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="17e16-128">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> <dt>

[<span data-ttu-id="17e16-129">**Isamplegrabbercb-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="17e16-129">**ISampleGrabberCB Interface**</span></span>](isamplegrabbercb.md)
</dt> </dl>

 

 




