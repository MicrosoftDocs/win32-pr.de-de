---
description: Die isamplegrabber-Schnittstelle wird durch den Sample-Grabber Filter verfügbar gemacht. Sie ermöglicht es einer Anwendung, einzelne Medien Beispiele abzurufen, während Sie durch das Filter Diagramm bewegt werden.
ms.assetid: 97cf1127-d5d7-4e6a-a371-19f24e497a7f
title: Isamplegrabber-Schnittstelle (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: f6e923032e74f88dceb1c2465e27dab9423bae1c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369537"
---
# <a name="isamplegrabber-interface"></a><span data-ttu-id="43515-104">Isamplegrabber-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="43515-104">ISampleGrabber interface</span></span>

> [!Note]  
> <span data-ttu-id="43515-105">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="43515-105">\[Deprecated.</span></span> <span data-ttu-id="43515-106">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="43515-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="43515-107">Die **isamplegrabber** -Schnittstelle wird durch den [**Sample-Grabber**](sample-grabber-filter.md) Filter verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="43515-107">The **ISampleGrabber** interface is exposed by the [**Sample Grabber**](sample-grabber-filter.md) filter.</span></span> <span data-ttu-id="43515-108">Sie ermöglicht es einer Anwendung, einzelne Medien Beispiele abzurufen, während Sie durch das Filter Diagramm bewegt werden.</span><span class="sxs-lookup"><span data-stu-id="43515-108">It enables an application to retrieve individual media samples as they move through the filter graph.</span></span>

## <a name="members"></a><span data-ttu-id="43515-109">Member</span><span class="sxs-lookup"><span data-stu-id="43515-109">Members</span></span>

<span data-ttu-id="43515-110">Die **isamplegrabber** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="43515-110">The **ISampleGrabber** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="43515-111">**Isamplegrabber** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="43515-111">**ISampleGrabber** also has these types of members:</span></span>

-   [<span data-ttu-id="43515-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="43515-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="43515-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="43515-113">Methods</span></span>

<span data-ttu-id="43515-114">Die **isamplegrabber** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="43515-114">The **ISampleGrabber** interface has these methods.</span></span>



| <span data-ttu-id="43515-115">Methode</span><span class="sxs-lookup"><span data-stu-id="43515-115">Method</span></span>                                                                | <span data-ttu-id="43515-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="43515-116">Description</span></span>                                                                                                                       |
|:----------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="43515-117">**Getconnectedmediatype**</span><span class="sxs-lookup"><span data-stu-id="43515-117">**GetConnectedMediaType**</span></span>](isamplegrabber-getconnectedmediatype.md) | <span data-ttu-id="43515-118">Ruft den Medientyp für die Verbindung mit der Eingabe-PIN von Sample Grabber ab.</span><span class="sxs-lookup"><span data-stu-id="43515-118">Retrieves the media type for the connection on the input pin of Sample Grabber.</span></span><br/>                                        |
| [<span data-ttu-id="43515-119">**Getcurrentbuffer**</span><span class="sxs-lookup"><span data-stu-id="43515-119">**GetCurrentBuffer**</span></span>](isamplegrabber-getcurrentbuffer.md)           | <span data-ttu-id="43515-120">Ruft eine Kopie des Beispiels ab, das der Filter zuletzt empfangen hat.</span><span class="sxs-lookup"><span data-stu-id="43515-120">Retrieves a copy of the sample that the filter received most recently.</span></span><br/>                                                 |
| [<span data-ttu-id="43515-121">**Getcurrentsample**</span><span class="sxs-lookup"><span data-stu-id="43515-121">**GetCurrentSample**</span></span>](isamplegrabber-getcurrentsample.md)           | <span data-ttu-id="43515-122">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="43515-122">Not implemented.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="43515-123">**Setbuffersamples**</span><span class="sxs-lookup"><span data-stu-id="43515-123">**SetBufferSamples**</span></span>](isamplegrabber-setbuffersamples.md)           | <span data-ttu-id="43515-124">Gibt an, ob Beispiel Daten beim Durchlaufen des Filters in einen Puffer kopiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="43515-124">Specifies whether to copy sample data into a buffer as it goes through the filter.</span></span><br/>                                     |
| [<span data-ttu-id="43515-125">**SetCallback**</span><span class="sxs-lookup"><span data-stu-id="43515-125">**SetCallback**</span></span>](isamplegrabber-setcallback.md)                     | <span data-ttu-id="43515-126">Gibt eine Rückruf Methode an, die für eingehende Stichproben aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="43515-126">Specifies a callback method to call on incoming samples.</span></span><br/>                                                               |
| [<span data-ttu-id="43515-127">**Setmediatype**</span><span class="sxs-lookup"><span data-stu-id="43515-127">**SetMediaType**</span></span>](isamplegrabber-setmediatype.md)                   | <span data-ttu-id="43515-128">Gibt den Medientyp für die Verbindung in der Eingabe-PIN der Beispiel-Grabber an.</span><span class="sxs-lookup"><span data-stu-id="43515-128">Specifies the media type for the connection on the input pin of the Sample Grabber.</span></span><br/>                                    |
| [<span data-ttu-id="43515-129">**"Abtoneshot"**</span><span class="sxs-lookup"><span data-stu-id="43515-129">**SetOneShot**</span></span>](isamplegrabber-setoneshot.md)                       | <span data-ttu-id="43515-130">Gibt an, ob der [**Sample Grabber**](sample-grabber-filter.md) -Filter angehalten wird, nachdem der Filter ein Beispiel erhalten hat.</span><span class="sxs-lookup"><span data-stu-id="43515-130">Specifies whether the [**Sample Grabber**](sample-grabber-filter.md) filter halts after the filter receives a sample.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="43515-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="43515-131">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="43515-132">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="43515-132">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="43515-133">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="43515-133">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="43515-134">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="43515-134">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="43515-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="43515-135">Requirements</span></span>



| <span data-ttu-id="43515-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="43515-136">Requirement</span></span> | <span data-ttu-id="43515-137">Wert</span><span class="sxs-lookup"><span data-stu-id="43515-137">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="43515-138">Header</span><span class="sxs-lookup"><span data-stu-id="43515-138">Header</span></span><br/>  | <dl> <span data-ttu-id="43515-139"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="43515-139"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="43515-140">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="43515-140">Library</span></span><br/> | <dl> <span data-ttu-id="43515-141"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="43515-141"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43515-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="43515-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43515-143">Verwenden der Beispiel-Grabber</span><span class="sxs-lookup"><span data-stu-id="43515-143">Using the Sample Grabber</span></span>](using-the-sample-grabber.md)
</dt> </dl>

 

 
