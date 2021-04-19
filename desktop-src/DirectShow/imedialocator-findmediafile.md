---
description: Die findmediafile-Methode sucht nach einer Datei und ruft, wenn erfolgreich, den Pfad zur Datei ab.
ms.assetid: ddfa2c75-e51f-4aad-afe6-8a60c46e8d35
title: 'Imedialocator:: findmediafile-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaLocator.FindMediaFile
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 3561b77873c90b2d4bd0202bed8e2da822a0362f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369414"
---
# <a name="imedialocatorfindmediafile-method"></a><span data-ttu-id="09df4-103">Imedialocator:: findmediafile-Methode</span><span class="sxs-lookup"><span data-stu-id="09df4-103">IMediaLocator::FindMediaFile method</span></span>

> [!Note]  
> <span data-ttu-id="09df4-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="09df4-104">\[Deprecated.</span></span> <span data-ttu-id="09df4-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="09df4-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="09df4-106">Die `FindMediaFile` -Methode sucht nach einer Datei und ruft, wenn erfolgreich, den Pfad zur Datei ab.</span><span class="sxs-lookup"><span data-stu-id="09df4-106">The `FindMediaFile` method searches for a file and, if successful, retrieves the path to the file.</span></span>

## <a name="syntax"></a><span data-ttu-id="09df4-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="09df4-107">Syntax</span></span>


```C++
HRESULT FindMediaFile(
   BSTR Input,
   BSTR FilterString,
   BSTR *pOutput,
   long Flags
);
```



## <a name="parameters"></a><span data-ttu-id="09df4-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="09df4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09df4-109">*Input* (Eingabe)</span><span class="sxs-lookup"><span data-stu-id="09df4-109">*Input*</span></span> 
</dt> <dd>

<span data-ttu-id="09df4-110">Dateiname, einschließlich des Pfads, in dem die Datei zuletzt bekannt war.</span><span class="sxs-lookup"><span data-stu-id="09df4-110">File name, including path, where the file was last known to reside.</span></span> <span data-ttu-id="09df4-111">Verwenden Sie für Quell Objekte in der Zeitachse den Namen des aktuellen Mediums.</span><span class="sxs-lookup"><span data-stu-id="09df4-111">For source objects in the timeline, use the current media name.</span></span>

</dd> <dt>

<span data-ttu-id="09df4-112">*Filter Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="09df4-112">*FilterString*</span></span> 
</dt> <dd>

<span data-ttu-id="09df4-113">Ein **BSTR** , das Paare von Filter Zeichenfolgen enthält, die entsprechend dem **lpstrfilter** -Member der [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) -Struktur formatiert sind.</span><span class="sxs-lookup"><span data-stu-id="09df4-113">A **BSTR** containing pairs of filter strings, formatted as required by the **lpstrFilter** member of the [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) structure.</span></span> <span data-ttu-id="09df4-114">Der medienlocator verwendet diesen Filter, wenn ein Dialogfeld zum Öffnen von Dateien angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="09df4-114">The media locator uses this filter if it displays a File Open dialog box.</span></span> <span data-ttu-id="09df4-115">Der Wert kann **null** sein, wenn der *Flags* -Parameter das SFN \_ validatef-Popup Kennzeichen nicht enthält \_ .</span><span class="sxs-lookup"><span data-stu-id="09df4-115">The value can be **NULL** if the *Flags* parameter does not include the SFN\_VALIDATEF\_POPUP flag.</span></span>

</dd> <dt>

<span data-ttu-id="09df4-116">*poutput*</span><span class="sxs-lookup"><span data-stu-id="09df4-116">*pOutput*</span></span> 
</dt> <dd>

<span data-ttu-id="09df4-117">Ein Zeiger auf eine Variable, die den eigentlichen Pfad zur Datei empfängt, wenn Sie sich von dem in der *Eingabe* enthaltenen Wert unterscheidet und die Methode die Datei erfolgreich findet.</span><span class="sxs-lookup"><span data-stu-id="09df4-117">Pointer to a variable that receives the actual path to the file, if it differs from the value contained in *Input* and if the method successfully locates the file.</span></span>

</dd> <dt>

<span data-ttu-id="09df4-118">*Flags*</span><span class="sxs-lookup"><span data-stu-id="09df4-118">*Flags*</span></span> 
</dt> <dd>

<span data-ttu-id="09df4-119">Bitweise Kombination von 0 (null) oder mehr Flags.</span><span class="sxs-lookup"><span data-stu-id="09df4-119">Bitwise combination of zero or more flags.</span></span> <span data-ttu-id="09df4-120">Eine Liste möglicher Flags finden Sie unter [**Validierungsflags für Dateinamen**](file-name-validation-flags.md).</span><span class="sxs-lookup"><span data-stu-id="09df4-120">For a list of possible flags, see [**File Name Validation Flags**](file-name-validation-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09df4-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="09df4-121">Return value</span></span>

<span data-ttu-id="09df4-122">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="09df4-122">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="09df4-123">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="09df4-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="09df4-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="09df4-124">Remarks</span></span>

<span data-ttu-id="09df4-125">Die Filter Zeichenfolge für das Dialogfeld zum Öffnen von Dateien, das durch den *filterstring* -Parameter angegeben wird, enthält interne NULL-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="09df4-125">The filter string for the File Open dialog, which is specified by the *FilterString* parameter, contains internal Null characters.</span></span> <span data-ttu-id="09df4-126">Video \\ 0 \* . avi \\ 0 \\ 0 ist beispielsweise eine gültige Filter Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="09df4-126">For example, Video\\0\*.avi\\0\\0 is a valid filter string.</span></span> <span data-ttu-id="09df4-127">Sie können den BSTR nicht mithilfe der **sysallocstr** -Funktion zuordnen, da diese Funktion eine NULL-terminierte Zeichenfolge erwartet und die Zeichenfolge beim ersten NULL-Zeichen abschneidet.</span><span class="sxs-lookup"><span data-stu-id="09df4-127">You cannot use the **SysAllocStr** function to allocate the BSTR, because that function expects a Null-terminated string and will truncate the string at the first Null character.</span></span> <span data-ttu-id="09df4-128">Verwenden Sie daher eine Funktion wie z. b. " **SysAllocStringLen**", die einen expliziten Parameter für die Länge enthält:</span><span class="sxs-lookup"><span data-stu-id="09df4-128">Therefore, use a function such as **SysAllocStringLen**, which includes an explicit parameter for the length:</span></span>


```C++
BSTR filter = SysAllocStringLen(L"Video\0*.avi\0", 12);
// Note: SysAllocStringLen appends an additional '\0' to the string.
```



<span data-ttu-id="09df4-129">Wenn der Benutzer das Dialogfeld zum Öffnen von Dateien abbricht, gibt die Methode E \_ Fail zurück.</span><span class="sxs-lookup"><span data-stu-id="09df4-129">If the user cancels the File Open dialog, the method returns E\_FAIL.</span></span>

<span data-ttu-id="09df4-130">Die-Methode ordnet Speicher für **BSTR** in *poutput* zu.</span><span class="sxs-lookup"><span data-stu-id="09df4-130">The method allocates memory for the **BSTR** in *pOutput*.</span></span> <span data-ttu-id="09df4-131">Die Anwendung muss **SysFreeString** aufzurufen, um den Arbeitsspeicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="09df4-131">The application must call **SysFreeString** to free the memory.</span></span>

> [!Note]  
> <span data-ttu-id="09df4-132">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="09df4-132">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="09df4-133">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="09df4-133">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="09df4-134">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="09df4-134">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="09df4-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="09df4-135">Requirements</span></span>



| <span data-ttu-id="09df4-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="09df4-136">Requirement</span></span> | <span data-ttu-id="09df4-137">Wert</span><span class="sxs-lookup"><span data-stu-id="09df4-137">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="09df4-138">Header</span><span class="sxs-lookup"><span data-stu-id="09df4-138">Header</span></span><br/>  | <dl> <span data-ttu-id="09df4-139"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="09df4-139"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="09df4-140">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="09df4-140">Library</span></span><br/> | <dl> <span data-ttu-id="09df4-141"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="09df4-141"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09df4-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="09df4-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09df4-143">**Imedialocator-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="09df4-143">**IMediaLocator Interface**</span></span>](imedialocator.md)
</dt> <dt>

[<span data-ttu-id="09df4-144">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="09df4-144">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 
