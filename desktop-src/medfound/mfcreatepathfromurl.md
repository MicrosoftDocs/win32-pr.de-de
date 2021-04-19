---
description: Konvertiert eine Datei-URL in einen Microsoft MS-DOS-Pfad.
ms.assetid: c35988ad-6cf8-41ec-bee9-e3bb982310ee
title: MF | atepathfromurl-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MFCreatePathFromURL
api_type:
- DllExport
api_location:
- mfplat.dll
ms.openlocfilehash: c1838a3b09dc5375588d562aa503d555a186e394
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345784"
---
# <a name="mfcreatepathfromurl-function"></a><span data-ttu-id="e6e2d-103">MF | atepathfromurl-Funktion</span><span class="sxs-lookup"><span data-stu-id="e6e2d-103">MFCreatePathFromURL function</span></span>

<span data-ttu-id="e6e2d-104">\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="e6e2d-104">\[This API is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="e6e2d-105">Stattdessen sollten Anwendungen [**pathkreatefromurl**](/windows/win32/api/shlwapi/nf-shlwapi-pathcreatefromurla)aufrufen.\]</span><span class="sxs-lookup"><span data-stu-id="e6e2d-105">Instead, applications should call [**PathCreateFromUrl**](/windows/win32/api/shlwapi/nf-shlwapi-pathcreatefromurla).\]</span></span>

<span data-ttu-id="e6e2d-106">Konvertiert eine Datei-URL in einen Microsoft MS-DOS-Pfad.</span><span class="sxs-lookup"><span data-stu-id="e6e2d-106">Converts a file URL to a Microsoft MS-DOS path.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6e2d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e6e2d-107">Syntax</span></span>


```C++
HRESULT MFCreatePathFromURL(
  _In_opt_ LPCWSTR pwszFileURL,
  _Out_    LPWSTR  *ppwszFilePath
);
```



## <a name="parameters"></a><span data-ttu-id="e6e2d-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e6e2d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6e2d-109">*pwszfileurl* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="e6e2d-109">*pwszFileURL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e6e2d-110">Eine NULL terminierte Zeichenfolge, die die URL enthält.</span><span class="sxs-lookup"><span data-stu-id="e6e2d-110">A null-terminated string that contains the URL.</span></span> <span data-ttu-id="e6e2d-111">Die maximale Länge der Zeichenfolge ist die Internet-maximale **\_ URL- \_ \_ Länge**.</span><span class="sxs-lookup"><span data-stu-id="e6e2d-111">The maximum length of the string is **INTERNET\_MAX\_URL\_LENGTH**.</span></span>

</dd> <dt>

<span data-ttu-id="e6e2d-112">*ppwszfilepath* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e6e2d-112">*ppwszFilePath* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e6e2d-113">Empfängt eine NULL-terminierte Zeichenfolge, die die URL enthält.</span><span class="sxs-lookup"><span data-stu-id="e6e2d-113">Receives a null-terminated string that contains the URL.</span></span> <span data-ttu-id="e6e2d-114">Der Aufrufer muss die Zeichenfolge durch Aufrufen von [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree)freigeben.</span><span class="sxs-lookup"><span data-stu-id="e6e2d-114">The caller must free the string by calling [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6e2d-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e6e2d-115">Return value</span></span>

<span data-ttu-id="e6e2d-116">Die-Funktion gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="e6e2d-116">The function returns an **HRESULT**.</span></span> <span data-ttu-id="e6e2d-117">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="e6e2d-117">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="e6e2d-118">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="e6e2d-118">Return code</span></span>                                                                                  | <span data-ttu-id="e6e2d-119">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e6e2d-119">Description</span></span>                                                                                                 |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e6e2d-120"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e6e2d-120"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="e6e2d-121">Die Funktion wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e6e2d-121">The function succeeded.</span></span> <br/>                                                                         |
| <dl> <span data-ttu-id="e6e2d-122"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="e6e2d-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="e6e2d-123">Ungültiges Argument.</span><span class="sxs-lookup"><span data-stu-id="e6e2d-123">Invalid argument.</span></span> <span data-ttu-id="e6e2d-124">Die im *pwszfileurl* -Parameter angegebene Zeichenfolge kann nicht in einen Pfad konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="e6e2d-124">The string given in the *pwszFileURL* parameter cannot be converted to a path.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e6e2d-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e6e2d-125">Remarks</span></span>

<span data-ttu-id="e6e2d-126">Diese Funktion verfügt über keine zugeordnete Import Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="e6e2d-126">This function has no associated import library.</span></span> <span data-ttu-id="e6e2d-127">Um diese Funktion aufzurufen, müssen Sie die [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit Mfplat.dll zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="e6e2d-127">To call this function, you must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mfplat.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6e2d-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e6e2d-128">Requirements</span></span>



| <span data-ttu-id="e6e2d-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e6e2d-129">Requirement</span></span> | <span data-ttu-id="e6e2d-130">Wert</span><span class="sxs-lookup"><span data-stu-id="e6e2d-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e6e2d-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e6e2d-131">Minimum supported client</span></span><br/> | <span data-ttu-id="e6e2d-132">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e6e2d-132">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e6e2d-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e6e2d-133">Minimum supported server</span></span><br/> | <span data-ttu-id="e6e2d-134">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e6e2d-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e6e2d-135">DLL</span><span class="sxs-lookup"><span data-stu-id="e6e2d-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e6e2d-136"><dt>Mfplat.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e6e2d-136"><dt>Mfplat.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6e2d-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e6e2d-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6e2d-138">Media Foundation Funktionen</span><span class="sxs-lookup"><span data-stu-id="e6e2d-138">Media Foundation Functions</span></span>](media-foundation-functions.md)
</dt> </dl>

 

 
