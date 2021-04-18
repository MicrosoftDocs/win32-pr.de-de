---
description: Die validatesourcenames-Methode überprüft die Quellnamen in der Zeitachse mithilfe des medienlocators. Diese Methode aktualisiert optional auch jedes Quell Objekt, für das es eine Datei sucht.
ms.assetid: 8f4b9ff0-f283-4bcb-83f4-92410cead7db
title: 'Iamtimeline:: validatesourcenames-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.ValidateSourceNames
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5154926cb9f814c94762b556721c7580e5b0d82c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360922"
---
# <a name="iamtimelinevalidatesourcenames-method"></a><span data-ttu-id="da851-104">Iamtimeline:: validatesourcenames-Methode</span><span class="sxs-lookup"><span data-stu-id="da851-104">IAMTimeline::ValidateSourceNames method</span></span>

> [!Note]  
> <span data-ttu-id="da851-105">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="da851-105">\[Deprecated.</span></span> <span data-ttu-id="da851-106">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="da851-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="da851-107">Die- `ValidateSourceNames` Methode überprüft die Quellnamen in der Zeitachse mithilfe des medienlocators.</span><span class="sxs-lookup"><span data-stu-id="da851-107">The `ValidateSourceNames` method validates source names in the timeline, using the media locator.</span></span> <span data-ttu-id="da851-108">Diese Methode aktualisiert optional auch jedes Quell Objekt, für das es eine Datei sucht.</span><span class="sxs-lookup"><span data-stu-id="da851-108">Optionally, this method also updates any source object for which it locates a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="da851-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="da851-109">Syntax</span></span>


```C++
HRESULT ValidateSourceNames(
   long          ValidateFlags,
   IMediaLocator *pOverride,
   long          NotifyEventHandle
);
```



## <a name="parameters"></a><span data-ttu-id="da851-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="da851-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da851-111">*Validateflags*</span><span class="sxs-lookup"><span data-stu-id="da851-111">*ValidateFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="da851-112">Bitweise Kombination von [**Dateinamens-Validierungsflags**](file-name-validation-flags.md) , die das Verhalten des medienlocators angeben.</span><span class="sxs-lookup"><span data-stu-id="da851-112">Bitwise combination of [**File Name Validation Flags**](file-name-validation-flags.md) specifying the behavior of the media locator.</span></span> <span data-ttu-id="da851-113">Die SFN \_ validatef \_ Replace-und SFN \_ validatef- \_ prüfflags müssen vorhanden sein, oder die Methode gibt E \_ invalidArg zurück.</span><span class="sxs-lookup"><span data-stu-id="da851-113">The SFN\_VALIDATEF\_REPLACE and SFN\_VALIDATEF\_CHECK flags must be present, or the method returns E\_INVALIDARG.</span></span>

</dd> <dt>

<span data-ttu-id="da851-114">*poverride*</span><span class="sxs-lookup"><span data-stu-id="da851-114">*pOverride*</span></span> 
</dt> <dd>

<span data-ttu-id="da851-115">Optionaler Zeiger auf die [**imedialocator**](imedialocator.md) -Schnittstelle eines medienlocators, der anstelle der Standardeinstellung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="da851-115">Optional pointer to the [**IMediaLocator**](imedialocator.md) interface of a media locator to use in place of the default.</span></span> <span data-ttu-id="da851-116">Legen Sie den Wert dieses Parameters auf **null** fest, um den standardmedienlocator zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="da851-116">To use the default media locator, set the value of this parameter to **NULL**.</span></span> <span data-ttu-id="da851-117">Weitere Informationen finden Sie unter Hinweise.</span><span class="sxs-lookup"><span data-stu-id="da851-117">See Remarks for more information.</span></span>

</dd> <dt>

<span data-ttu-id="da851-118">*Notierter benachrichtigsthread*</span><span class="sxs-lookup"><span data-stu-id="da851-118">*NotifyEventHandle*</span></span> 
</dt> <dd>

<span data-ttu-id="da851-119">Handle für ein Ereignis.</span><span class="sxs-lookup"><span data-stu-id="da851-119">Handle to an event.</span></span> <span data-ttu-id="da851-120">Die-Methode signalisiert das-Ereignis, nachdem die Überprüfung abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="da851-120">The method signals the event after it has completed the validation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da851-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="da851-121">Return value</span></span>

<span data-ttu-id="da851-122">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="da851-122">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="da851-123">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="da851-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="da851-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="da851-124">Remarks</span></span>

<span data-ttu-id="da851-125">Mithilfe des Parameters " *poverride* " können Sie eine eigene benutzerdefinierte Implementierung der [**imedialocator**](imedialocator.md) -Schnittstelle bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="da851-125">Using the *pOverride* parameter, you can supply your own custom implementation of the [**IMediaLocator**](imedialocator.md) interface.</span></span> <span data-ttu-id="da851-126">Der standardmäßige medienlocator benachrichtigt Ihre Anwendung z. b. nicht über die gefundenen Dateien (oder kann nicht gefunden werden).</span><span class="sxs-lookup"><span data-stu-id="da851-126">For example, the default media locator will not notify your application about the files that it finds (or cannot find).</span></span> <span data-ttu-id="da851-127">Um diese Einschränkung zu umgehen, können Sie einen benutzerdefinierten medienlocator implementieren, der als Wrapper für die Standardversion definiert ist.</span><span class="sxs-lookup"><span data-stu-id="da851-127">To get around this limitation, you could implement a custom media locator, making it a wrapper for the default version.</span></span> <span data-ttu-id="da851-128">Übergeben Sie in der benutzerdefinierten Version [**imedialocator:: findmediafile**](imedialocator-findmediafile.md) -Aufrufe direkt an die Standardversion, und überprüfen Sie den Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="da851-128">In your custom version, pass [**IMediaLocator::FindMediaFile**](imedialocator-findmediafile.md) calls directly to the default version, and examine the return value.</span></span>

> [!Note]  
> <span data-ttu-id="da851-129">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="da851-129">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="da851-130">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="da851-130">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="da851-131">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="da851-131">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="da851-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="da851-132">Requirements</span></span>



| <span data-ttu-id="da851-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="da851-133">Requirement</span></span> | <span data-ttu-id="da851-134">Wert</span><span class="sxs-lookup"><span data-stu-id="da851-134">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="da851-135">Header</span><span class="sxs-lookup"><span data-stu-id="da851-135">Header</span></span><br/>  | <dl> <span data-ttu-id="da851-136"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="da851-136"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="da851-137">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="da851-137">Library</span></span><br/> | <dl> <span data-ttu-id="da851-138"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="da851-138"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da851-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="da851-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da851-140">**Iamtimeline-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="da851-140">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="da851-141">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="da851-141">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




