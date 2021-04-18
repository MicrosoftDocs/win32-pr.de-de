---
description: Die setsourcenamevalidation-Methode gibt an, wie Dateinamen von der Renderingengine überprüft werden.
ms.assetid: b33904cd-ed7d-41b5-9ebf-50983ec9f7b3
title: 'Unenderengine:: setsourcenamevalidation-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.SetSourceNameValidation
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 96164a817fd04f505b32c17be1bff3268e847df8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360953"
---
# <a name="irenderenginesetsourcenamevalidation-method"></a><span data-ttu-id="e324f-103">Unenderengine:: setsourcenamevalidation-Methode</span><span class="sxs-lookup"><span data-stu-id="e324f-103">IRenderEngine::SetSourceNameValidation method</span></span>

> [!Note]  
> <span data-ttu-id="e324f-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="e324f-104">\[Deprecated.</span></span> <span data-ttu-id="e324f-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="e324f-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="e324f-106">Die- `SetSourceNameValidation` Methode gibt an, wie Dateinamen von der Renderingengine überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="e324f-106">The `SetSourceNameValidation` method specifies how the render engine validates file names.</span></span>

## <a name="syntax"></a><span data-ttu-id="e324f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e324f-107">Syntax</span></span>


```C++
HRESULT SetSourceNameValidation(
   BSTR          FilterString,
   IMediaLocator *pOverride,
   LONG          Flags
);
```



## <a name="parameters"></a><span data-ttu-id="e324f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e324f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e324f-109">*Filter Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="e324f-109">*FilterString*</span></span> 
</dt> <dd>

<span data-ttu-id="e324f-110">**BSTR** -Wert, der Paare von Filter Zeichenfolgen enthält, die entsprechend dem **lpstrfilter** -Member der [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) -Struktur formatiert sind.</span><span class="sxs-lookup"><span data-stu-id="e324f-110">**BSTR** value containing pairs of filter strings, formatted as required by the **lpstrFilter** member of the [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) structure.</span></span> <span data-ttu-id="e324f-111">Der medienlocator verwendet diesen Filter, wenn dem Endbenutzer ein Dialogfeld "Datei öffnen" angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="e324f-111">The media locator uses this filter if it presents an Open File dialog box to the end user.</span></span>

</dd> <dt>

<span data-ttu-id="e324f-112">*poverride*</span><span class="sxs-lookup"><span data-stu-id="e324f-112">*pOverride*</span></span> 
</dt> <dd>

<span data-ttu-id="e324f-113">Optionaler Zeiger auf die [**imedialocator**](imedialocator.md) -Schnittstelle eines medienlocators, der anstelle der Standardeinstellung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e324f-113">Optional pointer to the [**IMediaLocator**](imedialocator.md) interface of a media locator to use in place of the default.</span></span> <span data-ttu-id="e324f-114">Legen Sie den Wert dieses Parameters auf **null** fest, um den standardmedienlocator zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="e324f-114">To use the default media locator, set the value of this parameter to **NULL**.</span></span> <span data-ttu-id="e324f-115">Weitere Informationen finden Sie unter Hinweise.</span><span class="sxs-lookup"><span data-stu-id="e324f-115">See Remarks for more information.</span></span>

</dd> <dt>

<span data-ttu-id="e324f-116">*Flags*</span><span class="sxs-lookup"><span data-stu-id="e324f-116">*Flags*</span></span> 
</dt> <dd>

<span data-ttu-id="e324f-117">Bitweise Kombination von [**Dateinamens-Validierungsflags**](file-name-validation-flags.md) , die das Verhalten des medienlocators angeben.</span><span class="sxs-lookup"><span data-stu-id="e324f-117">Bitwise combination of [**File Name Validation Flags**](file-name-validation-flags.md) specifying the behavior of the media locator.</span></span> <span data-ttu-id="e324f-118">Das Check-Flag von SFN \_ validatef \_ muss vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="e324f-118">The SFN\_VALIDATEF\_CHECK flag must be present.</span></span> <span data-ttu-id="e324f-119">Das Flag SFN \_ validatef \_ hlinkgedämpfhat keine Auswirkung auf diese Methode.</span><span class="sxs-lookup"><span data-stu-id="e324f-119">The SFN\_VALIDATEF\_hlinkMUTED flag has no effect with this method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e324f-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e324f-120">Return value</span></span>

<span data-ttu-id="e324f-121">Gibt einen der folgenden **HRESULT** -Werte zurück:</span><span class="sxs-lookup"><span data-stu-id="e324f-121">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="e324f-122">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="e324f-122">Return code</span></span>                                                                                            | <span data-ttu-id="e324f-123">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e324f-123">Description</span></span>                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="e324f-124"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e324f-124"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="e324f-125">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="e324f-125">Success.</span></span><br/>                            |
| <dl> <span data-ttu-id="e324f-126"><dt>**E \_ muss \_ Init \_ Renderer**</dt></span><span class="sxs-lookup"><span data-stu-id="e324f-126"><dt>**E\_MUST\_INIT\_RENDERER**</dt></span></span> </dl> | <span data-ttu-id="e324f-127">Fehler beim Initialisieren der Rendering-Engine.</span><span class="sxs-lookup"><span data-stu-id="e324f-127">Render engine failed to initialize.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e324f-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e324f-128">Remarks</span></span>

<span data-ttu-id="e324f-129">Mithilfe des Parameters " *poverride* " können Sie eine eigene benutzerdefinierte Implementierung der [**imedialocator**](imedialocator.md) -Schnittstelle bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="e324f-129">Using the *pOverride* parameter, you can supply your own custom implementation of the [**IMediaLocator**](imedialocator.md) interface.</span></span> <span data-ttu-id="e324f-130">Beispielsweise benachrichtigt der Standard Medien-Serverlocatorpunkt eine Anwendung nicht über die gefundenen Dateien (oder kann nicht gefunden werden).</span><span class="sxs-lookup"><span data-stu-id="e324f-130">For example, the default media locator does not notify an application about the files that it finds (or cannot find).</span></span> <span data-ttu-id="e324f-131">Um diese Einschränkung zu umgehen, können Sie einen benutzerdefinierten medienlocator implementieren, der als Wrapper für die Standardversion definiert ist.</span><span class="sxs-lookup"><span data-stu-id="e324f-131">To get around this limitation, you could implement a custom media locator, making it a wrapper for the default version.</span></span> <span data-ttu-id="e324f-132">Übergeben Sie dann [**imedialocator:: findmediafile**](imedialocator-findmediafile.md) -Aufrufe direkt an die Standardversion, und überprüfen Sie den Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="e324f-132">Then pass [**IMediaLocator::FindMediaFile**](imedialocator-findmediafile.md) calls directly to the default version and examine the return value.</span></span>

<span data-ttu-id="e324f-133">Derzeit werden von dieser Methode keine dynamisch geladenen Quellen überprüft.</span><span class="sxs-lookup"><span data-stu-id="e324f-133">Currently, this method does not validate dynamically loaded sources.</span></span> <span data-ttu-id="e324f-134">Weitere Informationen finden Sie unter " [**unenderengine:: setdynamikreconnectlevel**](irenderengine-setdynamicreconnectlevel.md)".</span><span class="sxs-lookup"><span data-stu-id="e324f-134">See [**IRenderEngine::SetDynamicReconnectLevel**](irenderengine-setdynamicreconnectlevel.md).</span></span>

> [!Note]  
> <span data-ttu-id="e324f-135">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="e324f-135">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="e324f-136">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="e324f-136">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="e324f-137">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e324f-137">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e324f-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e324f-138">Requirements</span></span>



| <span data-ttu-id="e324f-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e324f-139">Requirement</span></span> | <span data-ttu-id="e324f-140">Wert</span><span class="sxs-lookup"><span data-stu-id="e324f-140">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e324f-141">Header</span><span class="sxs-lookup"><span data-stu-id="e324f-141">Header</span></span><br/>  | <dl> <span data-ttu-id="e324f-142"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="e324f-142"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="e324f-143">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e324f-143">Library</span></span><br/> | <dl> <span data-ttu-id="e324f-144"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="e324f-144"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e324f-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e324f-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e324f-146">**Schnittstelle ""**</span><span class="sxs-lookup"><span data-stu-id="e324f-146">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> <dt>

[<span data-ttu-id="e324f-147">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="e324f-147">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 
