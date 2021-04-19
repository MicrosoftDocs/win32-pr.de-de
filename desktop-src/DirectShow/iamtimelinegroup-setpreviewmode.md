---
description: Die SetPreviewMode-Methode legt den Vorschaumodus für die Gruppe fest.
ms.assetid: 40b7e9ac-30b3-454e-82ac-10ac99f1b86f
title: 'Iamtimelinegroup:: SetPreviewMode-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetPreviewMode
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fe03e6be3572b6cc660e51c27551a316db990d80
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361648"
---
# <a name="iamtimelinegroupsetpreviewmode-method"></a><span data-ttu-id="645ce-103">Iamtimelinegroup:: SetPreviewMode-Methode</span><span class="sxs-lookup"><span data-stu-id="645ce-103">IAMTimelineGroup::SetPreviewMode method</span></span>

> [!Note]  
> <span data-ttu-id="645ce-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="645ce-104">\[Deprecated.</span></span> <span data-ttu-id="645ce-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="645ce-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="645ce-106">Die SetPreviewMode-Methode legt den Vorschaumodus für die Gruppe fest.</span><span class="sxs-lookup"><span data-stu-id="645ce-106">The SetPreviewMode method sets the preview mode for the group.</span></span>

## <a name="syntax"></a><span data-ttu-id="645ce-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="645ce-107">Syntax</span></span>


```C++
HRESULT SetPreviewMode(
   BOOL fPreview
);
```



## <a name="parameters"></a><span data-ttu-id="645ce-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="645ce-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="645ce-109">*f-Vorschau*</span><span class="sxs-lookup"><span data-stu-id="645ce-109">*fPreview*</span></span> 
</dt> <dd>

<span data-ttu-id="645ce-110">Der Vorschaumodus.</span><span class="sxs-lookup"><span data-stu-id="645ce-110">The preview mode.</span></span> <span data-ttu-id="645ce-111">**True** gibt an, dass sich die Gruppe im Vorschaumodus befindet.</span><span class="sxs-lookup"><span data-stu-id="645ce-111">If **TRUE**, the group is in preview mode.</span></span> <span data-ttu-id="645ce-112">Wenn der Wert **false** ist, befindet sich die Gruppe im Erstellungs Modus.</span><span class="sxs-lookup"><span data-stu-id="645ce-112">If **FALSE**, the group is in authoring mode.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="645ce-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="645ce-113">Return value</span></span>

<span data-ttu-id="645ce-114">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="645ce-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="645ce-115">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="645ce-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="645ce-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="645ce-116">Remarks</span></span>

<span data-ttu-id="645ce-117">Im Vorschaumodus werden Frames bei langsamen Effekten oder Übergängen gelöscht, damit das Video mit dem Audioformat synchronisiert wird.</span><span class="sxs-lookup"><span data-stu-id="645ce-117">In preview mode, frames are dropped during slow effects or transitions to keep the video synchronized with the audio.</span></span> <span data-ttu-id="645ce-118">Das Video könnte als Ergebnis aussehen.</span><span class="sxs-lookup"><span data-stu-id="645ce-118">The video might look choppy as a result.</span></span> <span data-ttu-id="645ce-119">Im Erstellungs Modus wird jeder Frame gerendert.</span><span class="sxs-lookup"><span data-stu-id="645ce-119">In authoring mode, every frame is rendered.</span></span> <span data-ttu-id="645ce-120">Der Erstellungs Modus eignet sich zum Schreiben von Dateien. bei der Bildschirm Vorschau ist das Video möglicherweise nicht synchron mit der Audiodatei.</span><span class="sxs-lookup"><span data-stu-id="645ce-120">Authoring mode is appropriate for writing files; for on-screen preview, the video might be out of sync with the audio.</span></span>

> [!Note]  
> <span data-ttu-id="645ce-121">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="645ce-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="645ce-122">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="645ce-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="645ce-123">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="645ce-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="645ce-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="645ce-124">Requirements</span></span>



| <span data-ttu-id="645ce-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="645ce-125">Requirement</span></span> | <span data-ttu-id="645ce-126">Wert</span><span class="sxs-lookup"><span data-stu-id="645ce-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="645ce-127">Header</span><span class="sxs-lookup"><span data-stu-id="645ce-127">Header</span></span><br/>  | <dl> <span data-ttu-id="645ce-128"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="645ce-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="645ce-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="645ce-129">Library</span></span><br/> | <dl> <span data-ttu-id="645ce-130"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="645ce-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="645ce-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="645ce-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="645ce-132">**Iamtimelinegroup-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="645ce-132">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="645ce-133">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="645ce-133">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




