---
description: Erstellt ein Array von Handles für Symbole, die aus einer angegebenen Datei extrahiert werden.
title: Shextractiensw-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SHExtractIconsW
- SHExtractIconsW
api_type:
- DllExport
api_location:
- Shell32.dll
ms.assetid: 9f138b4e-6a84-4c7e-9521-5f8ffe0eaebf
ms.openlocfilehash: d82eb48d45210ebf12464708b09fe469d97432db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104994806"
---
# <a name="shextracticonsw-function"></a><span data-ttu-id="ee899-103">Shextractiensw-Funktion</span><span class="sxs-lookup"><span data-stu-id="ee899-103">SHExtractIconsW function</span></span>

<span data-ttu-id="ee899-104">\[**Shextractitsw** ist über Windows XP Service Pack 2 (SP2) verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ee899-104">\[**SHExtractIconsW** is available through Windows XP Service Pack 2 (SP2).</span></span> <span data-ttu-id="ee899-105">Sie wird möglicherweise in nachfolgenden Versionen geändert oder ist nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="ee899-105">It might be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="ee899-106">Erstellt ein Array von Handles für Symbole, die aus einer angegebenen Datei extrahiert werden.</span><span class="sxs-lookup"><span data-stu-id="ee899-106">Creates an array of handles to icons extracted from a specified file.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee899-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ee899-107">Syntax</span></span>


```C++
UINT SHExtractIconsW(
  _In_  LPCWSTR pszFileName,
  _In_  int     nIconIndex,
  _In_  int     cxIcon,
  _In_  int     cyIcon,
  _Out_ HICON   *phIcon,
  _Out_ UINT    *pIconId,
  _In_  UINT    nIcons,
  _In_  UINT    flags
);
```



## <a name="parameters"></a><span data-ttu-id="ee899-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ee899-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee899-109">*pszFileName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ee899-109">*pszFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee899-110">Typ: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="ee899-110">Type: **LPCWSTR**</span></span>

<span data-ttu-id="ee899-111">Ein Zeiger auf den Dateinamen, aus dem die Symbole extrahiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ee899-111">A pointer to the file name from which to extract the icons.</span></span>

</dd> <dt>

<span data-ttu-id="ee899-112">*nidindex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ee899-112">*nIconIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee899-113">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="ee899-113">Type: **int**</span></span>

<span data-ttu-id="ee899-114">Der Index des ersten Symbols, das aus der in *pszFileName* benannten Ressource extrahiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="ee899-114">The index of the first icon to extract from the resource named in *pszFileName*.</span></span>

</dd> <dt>

<span data-ttu-id="ee899-115">*cxicon* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ee899-115">*cxIcon* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee899-116">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="ee899-116">Type: **int**</span></span>

<span data-ttu-id="ee899-117">Die gewünschte Breite des Symbols.</span><span class="sxs-lookup"><span data-stu-id="ee899-117">The desired width of the icon.</span></span> <span data-ttu-id="ee899-118">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="ee899-118">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="ee899-119">*cyicon* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ee899-119">*cyIcon* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee899-120">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="ee899-120">Type: **int**</span></span>

<span data-ttu-id="ee899-121">Die gewünschte Höhe des Symbols.</span><span class="sxs-lookup"><span data-stu-id="ee899-121">The desired height of the icon.</span></span> <span data-ttu-id="ee899-122">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="ee899-122">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="ee899-123">*phicon* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="ee899-123">*phIcon* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ee899-124">Typ: \**HICON \** _</span><span class="sxs-lookup"><span data-stu-id="ee899-124">Type: \**HICON\** _</span></span>

<span data-ttu-id="ee899-125">Diese Funktion gibt einen Zeiger auf das Array von Symbol Handles zurück.</span><span class="sxs-lookup"><span data-stu-id="ee899-125">When this function returns, contains a pointer to the array of icon handles.</span></span>

</dd> <dt>

<span data-ttu-id="ee899-126">_pIconId \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ee899-126">_pIconId\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ee899-127">Typ: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="ee899-127">Type: \**UINT\** _</span></span>

<span data-ttu-id="ee899-128">Wenn diese Funktion zurückgegeben wird, enthält Sie einen Zeiger auf den Ressourcen Bezeichner des extrahierten Symbols, das am besten zum aktuellen Anzeigegerät passt.</span><span class="sxs-lookup"><span data-stu-id="ee899-128">When this function returns, contains a pointer to the resource identifier of the extracted icon that best fits the current display device.</span></span> <span data-ttu-id="ee899-129">Wenn kein Bezeichner für dieses Format verfügbar ist, enthält er "0xffffffff".</span><span class="sxs-lookup"><span data-stu-id="ee899-129">If there is no identifier available for this format, it contains 0xFFFFFFFF.</span></span> <span data-ttu-id="ee899-130">Wenn kein Bezeichner aus einem anderen Grund abgerufen werden kann, gibt 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="ee899-130">If no identifier can be obtained for any other reason, returns zero.</span></span>

</dd> <dt>

<span data-ttu-id="ee899-131">_nIcons \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ee899-131">_nIcons\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee899-132">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="ee899-132">Type: **UINT**</span></span>

<span data-ttu-id="ee899-133">Die Anzahl der Symbole, die aus der in *pszFileName* benannten Ressource extrahiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ee899-133">The number of icons to extract from the resource named in *pszFileName*.</span></span> <span data-ttu-id="ee899-134">Dieser Parameter ist nur gültig, wenn es sich bei der Ressource um eine exe-oder DLL-Datei handelt.</span><span class="sxs-lookup"><span data-stu-id="ee899-134">This parameter is valid only when the resource is a .exe or .dll file.</span></span>

</dd> <dt>

<span data-ttu-id="ee899-135">*Flags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ee899-135">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee899-136">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="ee899-136">Type: **UINT**</span></span>

<span data-ttu-id="ee899-137">Die Flags, die diese Funktion steuern.</span><span class="sxs-lookup"><span data-stu-id="ee899-137">The flags that control this function.</span></span> <span data-ttu-id="ee899-138">Mögliche Werte finden Sie unter dem *fuload* -Parameter der [**LoadImage**](/windows/win32/api/winuser/nf-winuser-loadimagea) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="ee899-138">For possible values, see the *fuLoad* parameter of the [**LoadImage**](/windows/win32/api/winuser/nf-winuser-loadimagea) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee899-139">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ee899-139">Return value</span></span>

<span data-ttu-id="ee899-140">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="ee899-140">Type: **UINT**</span></span>

<span data-ttu-id="ee899-141">Ein Wert ungleich 0 (null), wenn erfolgreich; andernfalls 0 (null).</span><span class="sxs-lookup"><span data-stu-id="ee899-141">A nonzero value if successful; otherwise, zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee899-142">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ee899-142">Remarks</span></span>

<span data-ttu-id="ee899-143">**Shextractikonsw** extrahiert aus den folgenden Dateitypen.</span><span class="sxs-lookup"><span data-stu-id="ee899-143">**SHExtractIconsW** extracts from the following file types.</span></span>

-   <span data-ttu-id="ee899-144">Ausführbare Datei (.exe)</span><span class="sxs-lookup"><span data-stu-id="ee899-144">Executable (.exe)</span></span>
-   <span data-ttu-id="ee899-145">Dll (dll)</span><span class="sxs-lookup"><span data-stu-id="ee899-145">DLL (.dll)</span></span>
-   <span data-ttu-id="ee899-146">Symbol (. ico)</span><span class="sxs-lookup"><span data-stu-id="ee899-146">Icon (.ico)</span></span>
-   <span data-ttu-id="ee899-147">Cursor (. cur)</span><span class="sxs-lookup"><span data-stu-id="ee899-147">Cursor (.cur)</span></span>
-   <span data-ttu-id="ee899-148">Animierter Cursor (. ani)</span><span class="sxs-lookup"><span data-stu-id="ee899-148">Animated cursor (.ani)</span></span>
-   <span data-ttu-id="ee899-149">Bitmap (.bmp)</span><span class="sxs-lookup"><span data-stu-id="ee899-149">Bitmap (.bmp)</span></span>

<span data-ttu-id="ee899-150">Extraktionen von Windows 3. ausführbare *x* 16-Bit-Dateien (exe-oder DLL-Dateien) werden ebenfalls unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ee899-150">Extractions from Windows 3.*x* 16-bit executable files (.exe or .dll) are also supported.</span></span>

<span data-ttu-id="ee899-151">Mit den Parametern *cxicon* und *cyicon* wird die Größe der zu extrahierenden Symbole angegeben.</span><span class="sxs-lookup"><span data-stu-id="ee899-151">The *cxIcon* and *cyIcon* parameters specify the size of the icons to extract.</span></span> <span data-ttu-id="ee899-152">Sie können zwei Größen durch die einzelnen Parameter extrahieren, indem Sie den Wert zwischen seinem LoWord und HIWORD aufteilen.</span><span class="sxs-lookup"><span data-stu-id="ee899-152">Two sizes can be extracted through each parameter by splitting the value between its LOWORD and HIWORD.</span></span> <span data-ttu-id="ee899-153">Legen Sie die erste gewünschte Größe in das lowort des-Parameters und die zweite Größe im HIWORD-Format ab.</span><span class="sxs-lookup"><span data-stu-id="ee899-153">Put the first desired size in the LOWORD of the parameter and the second size in the HIWORD.</span></span> <span data-ttu-id="ee899-154">Beispielsweise extrahiert [**makelong**](/previous-versions/windows/desktop/legacy/ms632660(v=vs.85))(24, 48) sowohl für *cxicon* als auch für *cyicon* sowohl 24-als auch 48-Symbole.</span><span class="sxs-lookup"><span data-stu-id="ee899-154">For example, [**MAKELONG**](/previous-versions/windows/desktop/legacy/ms632660(v=vs.85))(24, 48) for both *cxIcon* and *cyIcon* extracts both 24 and 48 sized icons.</span></span>

<span data-ttu-id="ee899-155">Der Aufrufprozess ist dafür verantwortlich, alle Symbole zu zerstören, die durch diese Funktion durch Aufrufen der [**DestroyIcon**](/windows/win32/api/winuser/nf-winuser-destroyicon) -Funktion extrahiert werden.</span><span class="sxs-lookup"><span data-stu-id="ee899-155">The calling process is responsible for destroying all icons extracted through this function by calling the [**DestroyIcon**](/windows/win32/api/winuser/nf-winuser-destroyicon) function.</span></span>

<span data-ttu-id="ee899-156">**Shextractiensw** wird nicht nach Name exportiert oder in einer öffentlichen Header Datei deklariert.</span><span class="sxs-lookup"><span data-stu-id="ee899-156">**SHExtractIconsW** is not exported by name or declared in a public header file.</span></span> <span data-ttu-id="ee899-157">Um es zu verwenden, müssen Sie einen übereinstimmenden Prototyp deklarieren und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) verwenden, um einen Funktionszeiger von Shell32.dll anzufordern, der zum Aufrufen dieser Funktion verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="ee899-157">To use it, you must declare a matching prototype and use [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) to request a function pointer from Shell32.dll that can be used to call this function.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee899-158">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="ee899-158">Requirements</span></span>



| <span data-ttu-id="ee899-159">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ee899-159">Requirement</span></span> | <span data-ttu-id="ee899-160">Wert</span><span class="sxs-lookup"><span data-stu-id="ee899-160">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee899-161">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ee899-161">Minimum supported client</span></span><br/> | <span data-ttu-id="ee899-162">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ee899-162">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ee899-163">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ee899-163">Minimum supported server</span></span><br/> | <span data-ttu-id="ee899-164">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ee899-164">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="ee899-165">DLL</span><span class="sxs-lookup"><span data-stu-id="ee899-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ee899-166"><dt>Shell32.dll (Version 5,0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="ee899-166"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |
| <span data-ttu-id="ee899-167">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="ee899-167">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="ee899-168">**Shextractitsw** (Unicode)</span><span class="sxs-lookup"><span data-stu-id="ee899-168">**SHExtractIconsW** (Unicode)</span></span><br/>                                                                      |



 

 
