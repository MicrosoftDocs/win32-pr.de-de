---
description: Die setrecompformatfromsource-Methode legt das Format der Video Neukomprimierung mithilfe des Komprimierungs Formats aus einer Quelldatei fest.
ms.assetid: 2d42876a-524b-454d-b4f1-353afe3a4d28
title: 'Iamtimelinegroup:: abtrecompformatfromsource-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetRecompFormatFromSource
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: adf4bfcf9d76ed40092eba7c612f4213c7aacb0d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352074"
---
# <a name="iamtimelinegroupsetrecompformatfromsource-method"></a><span data-ttu-id="ef787-103">Iamtimelinegroup:: abtrecompformatfromsource-Methode</span><span class="sxs-lookup"><span data-stu-id="ef787-103">IAMTimelineGroup::SetRecompFormatFromSource method</span></span>

> [!Note]  
> <span data-ttu-id="ef787-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="ef787-104">\[Deprecated.</span></span> <span data-ttu-id="ef787-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="ef787-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="ef787-106">Die- `SetRecompFormatFromSource` Methode legt das Format der Video Neukomprimierung mit dem Komprimierungs Format aus einer Quelldatei fest.</span><span class="sxs-lookup"><span data-stu-id="ef787-106">The `SetRecompFormatFromSource` method sets the video recompression format using the compression format from a source file.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef787-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ef787-107">Syntax</span></span>


```C++
HRESULT SetRecompFormatFromSource(
   IAMTimelineSrc *pSource
);
```



## <a name="parameters"></a><span data-ttu-id="ef787-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ef787-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef787-109">*psource*</span><span class="sxs-lookup"><span data-stu-id="ef787-109">*pSource*</span></span> 
</dt> <dd>

<span data-ttu-id="ef787-110">Ein Zeiger auf die [**iamtimelinesrc**](iamtimelinesrc.md) -Schnittstelle des Quell Objekts.</span><span class="sxs-lookup"><span data-stu-id="ef787-110">Pointer to the [**IAMTimelineSrc**](iamtimelinesrc.md) interface of the source object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef787-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ef787-111">Return value</span></span>

<span data-ttu-id="ef787-112">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="ef787-112">Returns an **HRESULT** values.</span></span> <span data-ttu-id="ef787-113">Die folgenden Werte sind möglich.</span><span class="sxs-lookup"><span data-stu-id="ef787-113">Possible values include the following.</span></span>



| <span data-ttu-id="ef787-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="ef787-114">Return code</span></span>                                                                                             | <span data-ttu-id="ef787-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ef787-115">Description</span></span>                                                                                            |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ef787-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ef787-116"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="ef787-117">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="ef787-117">Success.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="ef787-118"><dt>**E \_ keine \_ Zeitachse**</dt></span><span class="sxs-lookup"><span data-stu-id="ef787-118"><dt>**E\_NO\_TIMELINE**</dt></span></span> </dl>          | <span data-ttu-id="ef787-119">Die Gruppe befindet sich nicht in einer Zeitachse.</span><span class="sxs-lookup"><span data-stu-id="ef787-119">The group is not within a timeline.</span></span><br/>                                                         |
| <dl> <span data-ttu-id="ef787-120"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="ef787-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>           | <span data-ttu-id="ef787-121">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="ef787-121">Insufficient memory.</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="ef787-122"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="ef787-122"><dt>**E\_POINTER**</dt></span></span> </dl>               | <span data-ttu-id="ef787-123">**Null** -Zeigerargument.</span><span class="sxs-lookup"><span data-stu-id="ef787-123">**NULL** pointer argument.</span></span><br/>                                                                  |
| <dl> <span data-ttu-id="ef787-124"><dt>**VFW \_ E \_ invalidmediatype**</dt></span><span class="sxs-lookup"><span data-stu-id="ef787-124"><dt>**VFW\_E\_INVALIDMEDIATYPE**</dt></span></span> </dl> | <span data-ttu-id="ef787-125">Ungültiger Medientyp.</span><span class="sxs-lookup"><span data-stu-id="ef787-125">Invalid media type.</span></span> <span data-ttu-id="ef787-126">Die Gruppe ist keine Videogruppe, oder die Quelldatei enthält keinen Videostream.</span><span class="sxs-lookup"><span data-stu-id="ef787-126">The group is not a video group, or the source file has no video stream.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ef787-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ef787-127">Remarks</span></span>

<span data-ttu-id="ef787-128">Diese Methode sucht nach der Quelldatei, die *psource* zugeordnet ist, Ruft den Medientyp des ersten Videostreams in der Datei ab und legt das Gruppen Komprimierungs Format mithilfe dieses Typs fest.</span><span class="sxs-lookup"><span data-stu-id="ef787-128">This method finds the source file associated with *pSource*, retrieves the media type of the first video stream in the file, and sets the group compression format using that type.</span></span> <span data-ttu-id="ef787-129">Weitere Informationen zu den Komprimierungs Formaten finden Sie unter [**iamtimelinegroup:: See-martrecompressformat**](iamtimelinegroup-setsmartrecompressformat.md).</span><span class="sxs-lookup"><span data-stu-id="ef787-129">For more information about compression formats, see [**IAMTimelineGroup::SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md).</span></span>

> [!Note]  
> <span data-ttu-id="ef787-130">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="ef787-130">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="ef787-131">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="ef787-131">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="ef787-132">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ef787-132">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ef787-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ef787-133">Requirements</span></span>



| <span data-ttu-id="ef787-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ef787-134">Requirement</span></span> | <span data-ttu-id="ef787-135">Wert</span><span class="sxs-lookup"><span data-stu-id="ef787-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ef787-136">Header</span><span class="sxs-lookup"><span data-stu-id="ef787-136">Header</span></span><br/>  | <dl> <span data-ttu-id="ef787-137"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="ef787-137"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="ef787-138">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ef787-138">Library</span></span><br/> | <dl> <span data-ttu-id="ef787-139"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="ef787-139"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef787-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ef787-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef787-141">**Iamtimelinegroup-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="ef787-141">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="ef787-142">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="ef787-142">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




