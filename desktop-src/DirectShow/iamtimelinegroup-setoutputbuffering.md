---
description: Die setoutputbuffereing-Methode gibt die Anzahl der Rahmen an, die während der Vorschau vorab gerendert werden.
ms.assetid: 6e69b196-a6ce-4ce0-8c48-58b1738fb197
title: 'Iamtimelinegroup:: setoutputbuffereing-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetOutputBuffering
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ab249c1a6af63b0fc0f2ee535daeab1dec9cd558
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371706"
---
# <a name="iamtimelinegroupsetoutputbuffering-method"></a><span data-ttu-id="b335d-103">Iamtimelinegroup:: setoutputbuffereing-Methode</span><span class="sxs-lookup"><span data-stu-id="b335d-103">IAMTimelineGroup::SetOutputBuffering method</span></span>

> [!Note]  
> <span data-ttu-id="b335d-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="b335d-104">\[Deprecated.</span></span> <span data-ttu-id="b335d-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="b335d-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="b335d-106">Die- `SetOutputBuffering` Methode gibt die Anzahl der Rahmen an, die während der Vorschau vorab gerendert werden</span><span class="sxs-lookup"><span data-stu-id="b335d-106">The `SetOutputBuffering` method specifies the number of frames rendered in advance during preview.</span></span>

## <a name="syntax"></a><span data-ttu-id="b335d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b335d-107">Syntax</span></span>


```C++
HRESULT SetOutputBuffering(
  [in] int nBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="b335d-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b335d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b335d-109">*npuffer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b335d-109">*nBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b335d-110">Anzahl der Rahmen, die während der Vorschau puffert werden.</span><span class="sxs-lookup"><span data-stu-id="b335d-110">Number of frames to buffer during preview.</span></span> <span data-ttu-id="b335d-111">Muss zwei oder größer sein.</span><span class="sxs-lookup"><span data-stu-id="b335d-111">Must be two or greater.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b335d-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b335d-112">Return value</span></span>

<span data-ttu-id="b335d-113">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="b335d-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b335d-114">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b335d-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b335d-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b335d-115">Remarks</span></span>

<span data-ttu-id="b335d-116">Ein größerer Puffer benötigt mehr Arbeitsspeicher, kann jedoch zu einer glatteren Vorschau der Anzeige führen, insbesondere bei Effekten oder Übergängen, die mehr Zeit für das Rendering benötigen.</span><span class="sxs-lookup"><span data-stu-id="b335d-116">A larger buffer requires more memory but can result in smoother previewing, especially during effects or transitions that require more time to render.</span></span> <span data-ttu-id="b335d-117">Der Standard Puffer ist 30 Frames.</span><span class="sxs-lookup"><span data-stu-id="b335d-117">The default buffer is 30 frames.</span></span>

> [!Note]  
> <span data-ttu-id="b335d-118">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="b335d-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="b335d-119">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="b335d-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="b335d-120">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b335d-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b335d-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b335d-121">Requirements</span></span>



| <span data-ttu-id="b335d-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b335d-122">Requirement</span></span> | <span data-ttu-id="b335d-123">Wert</span><span class="sxs-lookup"><span data-stu-id="b335d-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b335d-124">Header</span><span class="sxs-lookup"><span data-stu-id="b335d-124">Header</span></span><br/>  | <dl> <span data-ttu-id="b335d-125"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="b335d-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="b335d-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b335d-126">Library</span></span><br/> | <dl> <span data-ttu-id="b335d-127"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="b335d-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b335d-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b335d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b335d-129">**Iamtimelinegroup-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="b335d-129">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="b335d-130">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="b335d-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




