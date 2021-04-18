---
description: 'Die isamplegrabbercb-Schnittstelle stellt Rückruf Methoden für die isamplegrabber:: SetCallback-Methode bereit. Wenn die Anwendung diese Methode aufruft, muss Sie diese Schnittstelle implementieren. Weitere Informationen finden Sie unter isamplegrabber.'
ms.assetid: 30166d1b-cc37-43c4-8f64-681d8f2013b9
title: Isamplegrabbercb-Schnittstelle (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabberCB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5c39d11e6560bc5e50a4c8a9b42a1cbb095b4b71
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358314"
---
# <a name="isamplegrabbercb-interface"></a><span data-ttu-id="07589-105">Isamplegrabbercb-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="07589-105">ISampleGrabberCB interface</span></span>

> [!Note]  
> <span data-ttu-id="07589-106">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="07589-106">\[Deprecated.</span></span> <span data-ttu-id="07589-107">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="07589-107">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="07589-108">Die- `ISampleGrabberCB` Schnittstelle stellt Rückruf Methoden für die [**isamplegrabber:: SetCallback**](isamplegrabber-setcallback.md) -Methode bereit.</span><span class="sxs-lookup"><span data-stu-id="07589-108">The `ISampleGrabberCB` interface provides callback methods for the [**ISampleGrabber::SetCallback**](isamplegrabber-setcallback.md) method.</span></span> <span data-ttu-id="07589-109">Wenn die Anwendung diese Methode aufruft, muss Sie diese Schnittstelle implementieren.</span><span class="sxs-lookup"><span data-stu-id="07589-109">If your application calls that method, it must implement this interface.</span></span> <span data-ttu-id="07589-110">Weitere Informationen finden Sie unter [**isamplegrabber**](isamplegrabber.md).</span><span class="sxs-lookup"><span data-stu-id="07589-110">For more information, see [**ISampleGrabber**](isamplegrabber.md).</span></span>

## <a name="members"></a><span data-ttu-id="07589-111">Member</span><span class="sxs-lookup"><span data-stu-id="07589-111">Members</span></span>

<span data-ttu-id="07589-112">Die **isamplegrabbercb** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="07589-112">The **ISampleGrabberCB** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="07589-113">**Isamplegrabbercb** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="07589-113">**ISampleGrabberCB** also has these types of members:</span></span>

-   [<span data-ttu-id="07589-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="07589-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="07589-115">Methoden</span><span class="sxs-lookup"><span data-stu-id="07589-115">Methods</span></span>

<span data-ttu-id="07589-116">Die **isamplegrabbercb** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="07589-116">The **ISampleGrabberCB** interface has these methods.</span></span>



| <span data-ttu-id="07589-117">Methode</span><span class="sxs-lookup"><span data-stu-id="07589-117">Method</span></span>                                        | <span data-ttu-id="07589-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="07589-118">Description</span></span>                                                              |
|:----------------------------------------------|:-------------------------------------------------------------------------|
| [<span data-ttu-id="07589-119">**Buffercb**</span><span class="sxs-lookup"><span data-stu-id="07589-119">**BufferCB**</span></span>](isamplegrabbercb-buffercb.md) | <span data-ttu-id="07589-120">Rückruf Methode, die einen Zeiger auf den Beispiel Puffer empfängt.</span><span class="sxs-lookup"><span data-stu-id="07589-120">Callback method that receives a pointer to the sample buffer.</span></span><br/> |
| [<span data-ttu-id="07589-121">**Samplecb**</span><span class="sxs-lookup"><span data-stu-id="07589-121">**SampleCB**</span></span>](isamplegrabbercb-samplecb.md) | <span data-ttu-id="07589-122">Rückruf Methode, die einen Zeiger auf das Medien Beispiel empfängt.</span><span class="sxs-lookup"><span data-stu-id="07589-122">Callback method that receives a pointer to the media sample.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="07589-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="07589-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="07589-124">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="07589-124">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="07589-125">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="07589-125">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="07589-126">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="07589-126">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="07589-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="07589-127">Requirements</span></span>



| <span data-ttu-id="07589-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="07589-128">Requirement</span></span> | <span data-ttu-id="07589-129">Wert</span><span class="sxs-lookup"><span data-stu-id="07589-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="07589-130">Header</span><span class="sxs-lookup"><span data-stu-id="07589-130">Header</span></span><br/>  | <dl> <span data-ttu-id="07589-131"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="07589-131"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="07589-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="07589-132">Library</span></span><br/> | <dl> <span data-ttu-id="07589-133"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="07589-133"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
