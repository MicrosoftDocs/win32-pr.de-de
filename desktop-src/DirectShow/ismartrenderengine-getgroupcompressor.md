---
description: Die getgroupcompressor-Methode ruft den Komprimierungs Filter für die angegebene Gruppe ab.
ms.assetid: 9d71e659-7abb-48c6-b9bd-5239560dc150
title: 'Ismartrenderengine:: getgroupcompressor-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISmartRenderEngine.GetGroupCompressor
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fd866daa225ab398e1a578aa8d21e73bad15e96d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351339"
---
# <a name="ismartrenderenginegetgroupcompressor-method"></a><span data-ttu-id="84357-103">Ismartrenderengine:: getgroupcompressor-Methode</span><span class="sxs-lookup"><span data-stu-id="84357-103">ISmartRenderEngine::GetGroupCompressor method</span></span>

> [!Note]  
> <span data-ttu-id="84357-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="84357-104">\[Deprecated.</span></span> <span data-ttu-id="84357-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="84357-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="84357-106">Die- `GetGroupCompressor` Methode ruft den Komprimierungs Filter für die angegebene Gruppe ab.</span><span class="sxs-lookup"><span data-stu-id="84357-106">The `GetGroupCompressor` method retrieves the compression filter for the specified group.</span></span>

## <a name="syntax"></a><span data-ttu-id="84357-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="84357-107">Syntax</span></span>


```C++
HRESULT GetGroupCompressor(
   long        Group,
   IBaseFilter **pCompressor
);
```



## <a name="parameters"></a><span data-ttu-id="84357-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="84357-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84357-109">*Gruppieren*</span><span class="sxs-lookup"><span data-stu-id="84357-109">*Group*</span></span> 
</dt> <dd>

<span data-ttu-id="84357-110">Der null basierte Index der Gruppe.</span><span class="sxs-lookup"><span data-stu-id="84357-110">Zero-based index of the group.</span></span>

</dd> <dt>

<span data-ttu-id="84357-111">*pkompressor*</span><span class="sxs-lookup"><span data-stu-id="84357-111">*pCompressor*</span></span> 
</dt> <dd>

<span data-ttu-id="84357-112">Empfängt einen Zeiger auf die [**ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) -Schnittstelle des Komprimierungs Filters.</span><span class="sxs-lookup"><span data-stu-id="84357-112">Receives a pointer to the [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface of the compression filter.</span></span> <span data-ttu-id="84357-113">Er empfängt den Wert **null** , wenn kein Komprimierungs Filter vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="84357-113">It receives the value **NULL** if there is no compression filter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84357-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="84357-114">Return value</span></span>

<span data-ttu-id="84357-115">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="84357-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="84357-116">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="84357-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="84357-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="84357-117">Remarks</span></span>

<span data-ttu-id="84357-118">Verwenden Sie diese Methode, um Eigenschaften für den Komprimierungs Filter festzulegen, z. b. die Keyframe-Rate.</span><span class="sxs-lookup"><span data-stu-id="84357-118">Use this method to set properties on the compression filter, such as the key-frame rate.</span></span> <span data-ttu-id="84357-119">Rufen Sie diese Methode nach dem Aufrufen von " [**irienderengine:: connectfrontend**](irenderengine-connectfrontend.md)" auf, aber bevor Sie das Projekt rendern.</span><span class="sxs-lookup"><span data-stu-id="84357-119">Call this method after calling [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md), but before rendering the project.</span></span> <span data-ttu-id="84357-120">Fragen Sie dann die Ausgabepin des Komprimierungs Filters für die [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) -Schnittstelle ab, die Methoden zum Festlegen von Komprimierungs Parametern enthält.</span><span class="sxs-lookup"><span data-stu-id="84357-120">Then query the compression filter's output pin for the [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) interface, which contains methods for setting compression parameters.</span></span> <span data-ttu-id="84357-121">Geben Sie die Schnittstelle frei, wenn Sie abgeschlossen sind.</span><span class="sxs-lookup"><span data-stu-id="84357-121">Release the interface when you are done.</span></span> <span data-ttu-id="84357-122">Wenn Sie nachfolgende Änderungen an der Zeitachse vornehmen, müssen Sie **connectfrontend** aufrufen und **getgroupcompressor** erneut aufrufen, um die Komprimierungs Parameter zurückzusetzen.</span><span class="sxs-lookup"><span data-stu-id="84357-122">If you make any subsequent changes to the timeline, call **ConnectFrontEnd**, and then call **GetGroupCompressor** again to reset the compression parameters.</span></span>

<span data-ttu-id="84357-123">Wenn der Wert von \* *pkompressor* bei der Rückgabe nicht **null** ist, weist die [**ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) -Schnittstelle einen ausstehenden Verweis Zähler auf.</span><span class="sxs-lookup"><span data-stu-id="84357-123">On return, if the value of \**pCompressor* is non-**NULL**, the [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface has an outstanding reference count.</span></span> <span data-ttu-id="84357-124">Stellen Sie sicher, dass Sie die-Schnittstelle freigeben, wenn Sie Sie nicht mehr benötigen.</span><span class="sxs-lookup"><span data-stu-id="84357-124">Be sure to release the interface when you are done using it.</span></span>

> [!Note]  
> <span data-ttu-id="84357-125">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="84357-125">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="84357-126">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="84357-126">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="84357-127">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="84357-127">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="84357-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="84357-128">Requirements</span></span>



| <span data-ttu-id="84357-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="84357-129">Requirement</span></span> | <span data-ttu-id="84357-130">Wert</span><span class="sxs-lookup"><span data-stu-id="84357-130">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="84357-131">Header</span><span class="sxs-lookup"><span data-stu-id="84357-131">Header</span></span><br/>  | <dl> <span data-ttu-id="84357-132"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="84357-132"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="84357-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="84357-133">Library</span></span><br/> | <dl> <span data-ttu-id="84357-134"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="84357-134"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84357-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="84357-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84357-136">**Ismartrenderengine-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="84357-136">**ISmartRenderEngine Interface**</span></span>](ismartrenderengine.md)
</dt> <dt>

[<span data-ttu-id="84357-137">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="84357-137">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




