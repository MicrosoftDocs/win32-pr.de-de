---
description: Die buffercb-Methode ist eine Rückruf Methode, die einen Zeiger auf den Beispiel Puffer empfängt.
ms.assetid: 9ee16dd6-8d05-4a9a-84c3-1b3bb95eaa04
title: 'Isamplegrabbercb:: buffercb-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabberCB.BufferCB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8af11545db1a3ed839f409deb141e5d910abe198
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359790"
---
# <a name="isamplegrabbercbbuffercb-method"></a><span data-ttu-id="7be1d-103">Isamplegrabbercb:: buffercb-Methode</span><span class="sxs-lookup"><span data-stu-id="7be1d-103">ISampleGrabberCB::BufferCB method</span></span>

> [!Note]  
> <span data-ttu-id="7be1d-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="7be1d-104">\[Deprecated.</span></span> <span data-ttu-id="7be1d-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="7be1d-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="7be1d-106">Die **buffercb** -Methode ist eine Rückruf Methode, die einen Zeiger auf den Beispiel Puffer empfängt.</span><span class="sxs-lookup"><span data-stu-id="7be1d-106">The **BufferCB** method is a callback method that receives a pointer to the sample buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="7be1d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="7be1d-107">Syntax</span></span>


```C++
HRESULT BufferCB(
   double SampleTime,
   BYTE   *pBuffer,
   long   BufferLen
);
```



## <a name="parameters"></a><span data-ttu-id="7be1d-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="7be1d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7be1d-109">*Sampletime*</span><span class="sxs-lookup"><span data-stu-id="7be1d-109">*SampleTime*</span></span> 
</dt> <dd>

<span data-ttu-id="7be1d-110">Startzeit des Beispiels in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="7be1d-110">Starting time of the sample, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="7be1d-111">*pBuffer*</span><span class="sxs-lookup"><span data-stu-id="7be1d-111">*pBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="7be1d-112">Zeiger auf einen Puffer, der die Beispiel Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="7be1d-112">Pointer to a buffer that contains the sample data.</span></span> <span data-ttu-id="7be1d-113">Das Format der Daten hängt vom Medientyp der Eingabe-PIN des beispielgrabers ab.</span><span class="sxs-lookup"><span data-stu-id="7be1d-113">The format of the data depends on the media type of the Sample Grabber's input pin.</span></span> <span data-ttu-id="7be1d-114">Um den Medientyp abzurufen, nennen Sie [**isamplegrabber:: getconnectedmediatype**](isamplegrabber-getconnectedmediatype.md).</span><span class="sxs-lookup"><span data-stu-id="7be1d-114">To get the media type, call [**ISampleGrabber::GetConnectedMediaType**](isamplegrabber-getconnectedmediatype.md).</span></span>

</dd> <dt>

<span data-ttu-id="7be1d-115">*Bufferlen*</span><span class="sxs-lookup"><span data-stu-id="7be1d-115">*BufferLen*</span></span> 
</dt> <dd>

<span data-ttu-id="7be1d-116">Länge des Puffers, auf den *pbuffer* zeigt (in Bytes).</span><span class="sxs-lookup"><span data-stu-id="7be1d-116">Length of the buffer pointed to by *pBuffer*, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7be1d-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7be1d-117">Return value</span></span>

<span data-ttu-id="7be1d-118">Gibt \_ bei Erfolg S OK oder andernfalls einen **HRESULT** -Fehlercode zurück.</span><span class="sxs-lookup"><span data-stu-id="7be1d-118">Returns S\_OK if successful, or an **HRESULT** error code otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="7be1d-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7be1d-119">Remarks</span></span>

<span data-ttu-id="7be1d-120">Diese Rückruf Methode erhält einen Zeiger auf die Daten im neuesten Medien Beispiel.</span><span class="sxs-lookup"><span data-stu-id="7be1d-120">This callback method receives a pointer to the data in the most recent media sample.</span></span>

> [!Note]  
> <span data-ttu-id="7be1d-121">Diese Methode erhält einen Zeiger auf die ursprünglichen Beispiel Daten, nicht auf eine Kopie.</span><span class="sxs-lookup"><span data-stu-id="7be1d-121">This method receives a pointer to the original sample data, not a copy.</span></span> <span data-ttu-id="7be1d-122">In der ursprünglichen Dokumentation wurde fälschlicherweise angegeben, dass *pbuffer* eine Kopie der Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="7be1d-122">The original documentation incorrectly stated that *pBuffer* contains a copy of the data.</span></span>

 

<span data-ttu-id="7be1d-123">Rufen Sie zum Einrichten des Rückrufs [**isamplegrabber:: SetCallback**](isamplegrabber-setcallback.md)auf.</span><span class="sxs-lookup"><span data-stu-id="7be1d-123">To set up the callback, call [**ISampleGrabber::SetCallback**](isamplegrabber-setcallback.md).</span></span>

> [!Note]  
> <span data-ttu-id="7be1d-124">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="7be1d-124">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="7be1d-125">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="7be1d-125">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="7be1d-126">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7be1d-126">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7be1d-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7be1d-127">Requirements</span></span>



| <span data-ttu-id="7be1d-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7be1d-128">Requirement</span></span> | <span data-ttu-id="7be1d-129">Wert</span><span class="sxs-lookup"><span data-stu-id="7be1d-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7be1d-130">Header</span><span class="sxs-lookup"><span data-stu-id="7be1d-130">Header</span></span><br/>  | <dl> <span data-ttu-id="7be1d-131"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="7be1d-131"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="7be1d-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7be1d-132">Library</span></span><br/> | <dl> <span data-ttu-id="7be1d-133"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="7be1d-133"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7be1d-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7be1d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7be1d-135">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="7be1d-135">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> <dt>

[<span data-ttu-id="7be1d-136">**Isamplegrabbercb-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="7be1d-136">**ISampleGrabberCB Interface**</span></span>](isamplegrabbercb.md)
</dt> </dl>

 

 




