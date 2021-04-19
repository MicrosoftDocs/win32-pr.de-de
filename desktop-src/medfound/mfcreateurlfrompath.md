---
description: Konvertiert einen Microsoft MS-DOS-Pfad in eine kanonisierte URL.
ms.assetid: 1186b970-9ae1-4020-b999-55157cff1741
title: MF | ateurlfrompath-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MFCreateURLFromPath
api_type:
- DllExport
api_location:
- mfplat.dll
ms.openlocfilehash: e43c2d7df299792d8b5be99226e9cfdbd11976a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348462"
---
# <a name="mfcreateurlfrompath-function"></a><span data-ttu-id="ef227-103">MF | ateurlfrompath-Funktion</span><span class="sxs-lookup"><span data-stu-id="ef227-103">MFCreateURLFromPath function</span></span>

<span data-ttu-id="ef227-104">\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="ef227-104">\[This API is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="ef227-105">Stattdessen sollten Anwendungen [urlkreatefrompath](/windows/desktop/api/shlwapi/nf-shlwapi-urlcreatefrompatha)aufrufen.\]</span><span class="sxs-lookup"><span data-stu-id="ef227-105">Instead, Applications should call [UrlCreateFromPath](/windows/desktop/api/shlwapi/nf-shlwapi-urlcreatefrompatha).\]</span></span>

<span data-ttu-id="ef227-106">Konvertiert einen Microsoft MS-DOS-Pfad in eine kanonisierte URL.</span><span class="sxs-lookup"><span data-stu-id="ef227-106">Converts a Microsoft MS-DOS path to a canonicalized URL.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef227-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ef227-107">Syntax</span></span>


```C++
HRESULT MFCreateURLFromPath(
  _In_opt_ LPCWSTR pwszFilePath,
  _Out_    LPWSTR  *ppwszFileURL
);
```



## <a name="parameters"></a><span data-ttu-id="ef227-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ef227-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef227-109">*pwszfilepath* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="ef227-109">*pwszFilePath* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ef227-110">Eine NULL terminierte Zeichenfolge, die den Pfad enthält.</span><span class="sxs-lookup"><span data-stu-id="ef227-110">A null-terminated string that contains the path.</span></span> <span data-ttu-id="ef227-111">Die maximale Länge der Zeichenfolge ist die Internet-maximale **\_ URL- \_ \_ Länge**.</span><span class="sxs-lookup"><span data-stu-id="ef227-111">The maximum length of the string is **INTERNET\_MAX\_URL\_LENGTH**.</span></span>

</dd> <dt>

<span data-ttu-id="ef227-112">*ppwszfileurl* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="ef227-112">*ppwszFileURL* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ef227-113">Empfängt eine NULL-terminierte Zeichenfolge, die die URL enthält.</span><span class="sxs-lookup"><span data-stu-id="ef227-113">Receives a null-terminated string that contains the URL.</span></span> <span data-ttu-id="ef227-114">Der Aufrufer muss die Zeichenfolge durch Aufrufen von [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree)freigeben.</span><span class="sxs-lookup"><span data-stu-id="ef227-114">The caller must free the string by calling [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef227-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ef227-115">Return value</span></span>

<span data-ttu-id="ef227-116">Die-Funktion gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="ef227-116">The function returns an **HRESULT**.</span></span> <span data-ttu-id="ef227-117">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="ef227-117">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="ef227-118">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="ef227-118">Return code</span></span>                                                                             | <span data-ttu-id="ef227-119">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ef227-119">Description</span></span>                                                                                                                                                               |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ef227-120"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="ef227-120"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="ef227-121">Die im *pwszfilepath* -Parameter angegebene Zeichenfolge weist bereits das URL-Format auf.</span><span class="sxs-lookup"><span data-stu-id="ef227-121">The string given in the *pwszFilePath* parameter is already in URL format.</span></span> <span data-ttu-id="ef227-122">In diesem Fall wird *pszfilepath* einfach ohne Änderung in *ppszfileurl* kopiert.</span><span class="sxs-lookup"><span data-stu-id="ef227-122">In this case, *pszFilePath* is simply copied to *ppszFileURL* without modification.</span></span><br/> |
| <dl> <span data-ttu-id="ef227-123"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ef227-123"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="ef227-124">Die Funktion wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ef227-124">The function succeeded.</span></span> <br/>                                                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="ef227-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ef227-125">Remarks</span></span>

<span data-ttu-id="ef227-126">Diese Funktion verfügt über keine zugeordnete Import Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="ef227-126">This function has no associated import library.</span></span> <span data-ttu-id="ef227-127">Um diese Funktion aufzurufen, müssen Sie die [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit Mfplat.dll zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="ef227-127">To call this function, you must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mfplat.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef227-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ef227-128">Requirements</span></span>



| <span data-ttu-id="ef227-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ef227-129">Requirement</span></span> | <span data-ttu-id="ef227-130">Wert</span><span class="sxs-lookup"><span data-stu-id="ef227-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ef227-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ef227-131">Minimum supported client</span></span><br/> | <span data-ttu-id="ef227-132">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ef227-132">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ef227-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ef227-133">Minimum supported server</span></span><br/> | <span data-ttu-id="ef227-134">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ef227-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ef227-135">DLL</span><span class="sxs-lookup"><span data-stu-id="ef227-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ef227-136"><dt>Mfplat.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ef227-136"><dt>Mfplat.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef227-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ef227-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef227-138">Media Foundation Funktionen</span><span class="sxs-lookup"><span data-stu-id="ef227-138">Media Foundation Functions</span></span>](media-foundation-functions.md)
</dt> </dl>

 

 
