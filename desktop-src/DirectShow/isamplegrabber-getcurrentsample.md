---
description: Die getcurrentsample-Methode ist nicht implementiert.
ms.assetid: 0c903498-3c1d-4e95-a797-ca8cfded25f2
title: 'Isamplegrabber:: getcurrentsample-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber.GetCurrentSample
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9a21f50f84f030502cfd3243d36595e465e1b85b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359675"
---
# <a name="isamplegrabbergetcurrentsample-method"></a><span data-ttu-id="b8e86-103">Isamplegrabber:: getcurrentsample-Methode</span><span class="sxs-lookup"><span data-stu-id="b8e86-103">ISampleGrabber::GetCurrentSample method</span></span>

> [!Note]  
> <span data-ttu-id="b8e86-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="b8e86-104">\[Deprecated.</span></span> <span data-ttu-id="b8e86-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="b8e86-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="b8e86-106">Die `GetCurrentSample`-Methode ist nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="b8e86-106">The `GetCurrentSample` method is not implemented.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8e86-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b8e86-107">Syntax</span></span>


```C++
HRESULT GetCurrentSample(
   IMediaSample **ppSample
);
```



## <a name="parameters"></a><span data-ttu-id="b8e86-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b8e86-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8e86-109">*ppsample*</span><span class="sxs-lookup"><span data-stu-id="b8e86-109">*ppSample*</span></span> 
</dt> <dd>

<span data-ttu-id="b8e86-110">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="b8e86-110">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8e86-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b8e86-111">Return value</span></span>

<span data-ttu-id="b8e86-112">Gibt "E \_ notimpl" zurück.</span><span class="sxs-lookup"><span data-stu-id="b8e86-112">Returns E\_NOTIMPL.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8e86-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b8e86-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b8e86-114">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="b8e86-114">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="b8e86-115">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="b8e86-115">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="b8e86-116">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b8e86-116">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b8e86-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b8e86-117">Requirements</span></span>



| <span data-ttu-id="b8e86-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b8e86-118">Requirement</span></span> | <span data-ttu-id="b8e86-119">Wert</span><span class="sxs-lookup"><span data-stu-id="b8e86-119">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b8e86-120">Header</span><span class="sxs-lookup"><span data-stu-id="b8e86-120">Header</span></span><br/>  | <dl> <span data-ttu-id="b8e86-121"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="b8e86-121"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="b8e86-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b8e86-122">Library</span></span><br/> | <dl> <span data-ttu-id="b8e86-123"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="b8e86-123"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8e86-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b8e86-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8e86-125">Verwenden der Beispiel-Grabber</span><span class="sxs-lookup"><span data-stu-id="b8e86-125">Using the Sample Grabber</span></span>](using-the-sample-grabber.md)
</dt> <dt>

[<span data-ttu-id="b8e86-126">**Isamplegrabber-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="b8e86-126">**ISampleGrabber Interface**</span></span>](isamplegrabber.md)
</dt> </dl>

 

 




