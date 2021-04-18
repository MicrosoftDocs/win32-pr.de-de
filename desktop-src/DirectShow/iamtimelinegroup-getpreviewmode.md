---
description: Die getpreviewmode-Methode ruft den Vorschaumodus für die Gruppe ab.
ms.assetid: 635354e5-5cb2-4045-8a7f-21d31005c5f3
title: 'Iamtimelinegroup:: getpreviewmode-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.GetPreviewMode
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 724c35c57ff90216547a8a343b469cb627e32415
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354838"
---
# <a name="iamtimelinegroupgetpreviewmode-method"></a><span data-ttu-id="21ee9-103">Iamtimelinegroup:: getpreviewmode-Methode</span><span class="sxs-lookup"><span data-stu-id="21ee9-103">IAMTimelineGroup::GetPreviewMode method</span></span>

> [!Note]  
> <span data-ttu-id="21ee9-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="21ee9-104">\[Deprecated.</span></span> <span data-ttu-id="21ee9-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="21ee9-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="21ee9-106">Die- `GetPreviewMode` Methode ruft den Vorschaumodus für die Gruppe ab.</span><span class="sxs-lookup"><span data-stu-id="21ee9-106">The `GetPreviewMode` method retrieves the preview mode for the group.</span></span>

## <a name="syntax"></a><span data-ttu-id="21ee9-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="21ee9-107">Syntax</span></span>


```C++
HRESULT GetPreviewMode(
   BOOL *pfPreview
);
```



## <a name="parameters"></a><span data-ttu-id="21ee9-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="21ee9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21ee9-109">*pfpreview*</span><span class="sxs-lookup"><span data-stu-id="21ee9-109">*pfPreview*</span></span> 
</dt> <dd>

<span data-ttu-id="21ee9-110">Empfängt einen booleschen Wert, der den Vorschaumodus angibt.</span><span class="sxs-lookup"><span data-stu-id="21ee9-110">Receives a Boolean value indicating the preview mode.</span></span> <span data-ttu-id="21ee9-111">**True** gibt an, dass sich die Gruppe im Vorschaumodus befindet.</span><span class="sxs-lookup"><span data-stu-id="21ee9-111">If **TRUE**, the group is in preview mode.</span></span> <span data-ttu-id="21ee9-112">Wenn der Wert **false** ist, befindet sich die Gruppe im Erstellungs Modus.</span><span class="sxs-lookup"><span data-stu-id="21ee9-112">If **FALSE**, the group is in authoring mode.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21ee9-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="21ee9-113">Return value</span></span>

<span data-ttu-id="21ee9-114">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="21ee9-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="21ee9-115">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="21ee9-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="21ee9-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="21ee9-116">Remarks</span></span>

<span data-ttu-id="21ee9-117">Im Vorschaumodus werden Frames bei langsamen Effekten oder Übergängen gelöscht, damit das Video mit dem Audioformat synchronisiert wird.</span><span class="sxs-lookup"><span data-stu-id="21ee9-117">In preview mode, frames are dropped during slow effects or transitions to keep the video synchronized with the audio.</span></span> <span data-ttu-id="21ee9-118">Das Video könnte als Ergebnis aussehen.</span><span class="sxs-lookup"><span data-stu-id="21ee9-118">The video might look choppy as a result.</span></span> <span data-ttu-id="21ee9-119">Im Erstellungs Modus wird jeder Frame gerendert.</span><span class="sxs-lookup"><span data-stu-id="21ee9-119">In authoring mode, every frame is rendered.</span></span> <span data-ttu-id="21ee9-120">Der Erstellungs Modus eignet sich zum Schreiben von Dateien. bei der Bildschirm Vorschau wird das Video möglicherweise nicht mehr mit dem Audioformat synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="21ee9-120">Authoring mode is appropriate for writing files; for on-screen preview, the video might become out of sync with the audio.</span></span>

> [!Note]  
> <span data-ttu-id="21ee9-121">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="21ee9-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="21ee9-122">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="21ee9-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="21ee9-123">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="21ee9-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="21ee9-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="21ee9-124">Requirements</span></span>



| <span data-ttu-id="21ee9-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="21ee9-125">Requirement</span></span> | <span data-ttu-id="21ee9-126">Wert</span><span class="sxs-lookup"><span data-stu-id="21ee9-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="21ee9-127">Header</span><span class="sxs-lookup"><span data-stu-id="21ee9-127">Header</span></span><br/>  | <dl> <span data-ttu-id="21ee9-128"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="21ee9-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="21ee9-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="21ee9-129">Library</span></span><br/> | <dl> <span data-ttu-id="21ee9-130"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="21ee9-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21ee9-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="21ee9-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21ee9-132">**Iamtimelinegroup-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="21ee9-132">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="21ee9-133">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="21ee9-133">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




