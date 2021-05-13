---
description: Erstellt ein Array von Handles für Symbole, die aus einer angegebenen Datei extrahiert wurden.
title: SHExtractIconsW-Funktion
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
ms.openlocfilehash: 699b6d5473d97548a22e220372b9f53633cb2346
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840911"
---
# <a name="shextracticonsw-function"></a><span data-ttu-id="8af7b-103">SHExtractIconsW-Funktion</span><span class="sxs-lookup"><span data-stu-id="8af7b-103">SHExtractIconsW function</span></span>

<span data-ttu-id="8af7b-104">\[**SHExtractIconsW** ist über Windows XP Service Pack 2 (SP2) verfügbar.</span><span class="sxs-lookup"><span data-stu-id="8af7b-104">\[**SHExtractIconsW** is available through Windows XP Service Pack 2 (SP2).</span></span> <span data-ttu-id="8af7b-105">Sie kann in nachfolgenden Versionen geändert oder nicht verfügbar sein.\]</span><span class="sxs-lookup"><span data-stu-id="8af7b-105">It might be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="8af7b-106">Erstellt ein Array von Handles für Symbole, die aus einer angegebenen Datei extrahiert wurden.</span><span class="sxs-lookup"><span data-stu-id="8af7b-106">Creates an array of handles to icons extracted from a specified file.</span></span>

## <a name="syntax"></a><span data-ttu-id="8af7b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="8af7b-107">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="8af7b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="8af7b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8af7b-109">*pszFileName* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="8af7b-109">*pszFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8af7b-110">Typ: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="8af7b-110">Type: **LPCWSTR**</span></span>

<span data-ttu-id="8af7b-111">Ein Zeiger auf den Dateinamen, aus dem die Symbole extrahiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8af7b-111">A pointer to the file name from which to extract the icons.</span></span>

</dd> <dt>

<span data-ttu-id="8af7b-112">*nIconIndex* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="8af7b-112">*nIconIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8af7b-113">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="8af7b-113">Type: **int**</span></span>

<span data-ttu-id="8af7b-114">Der Index des ersten Symbols, das aus der Ressource namens in *pszFileName* extrahiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="8af7b-114">The index of the first icon to extract from the resource named in *pszFileName*.</span></span>

</dd> <dt>

<span data-ttu-id="8af7b-115">*cxIcon* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="8af7b-115">*cxIcon* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8af7b-116">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="8af7b-116">Type: **int**</span></span>

<span data-ttu-id="8af7b-117">Die gewünschte Breite des Symbols.</span><span class="sxs-lookup"><span data-stu-id="8af7b-117">The desired width of the icon.</span></span> <span data-ttu-id="8af7b-118">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="8af7b-118">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="8af7b-119">*cyIcon* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="8af7b-119">*cyIcon* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8af7b-120">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="8af7b-120">Type: **int**</span></span>

<span data-ttu-id="8af7b-121">Die gewünschte Höhe des Symbols.</span><span class="sxs-lookup"><span data-stu-id="8af7b-121">The desired height of the icon.</span></span> <span data-ttu-id="8af7b-122">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="8af7b-122">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="8af7b-123">*phIcon* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="8af7b-123">*phIcon* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8af7b-124">Typ: **HICON \***</span><span class="sxs-lookup"><span data-stu-id="8af7b-124">Type: **HICON\***</span></span>

<span data-ttu-id="8af7b-125">Enthält nach der Rückkehr dieser Funktion einen Zeiger auf das Array von Symbolhandles.</span><span class="sxs-lookup"><span data-stu-id="8af7b-125">When this function returns, contains a pointer to the array of icon handles.</span></span>

</dd> <dt>

<span data-ttu-id="8af7b-126">*pIconId* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="8af7b-126">*pIconId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8af7b-127">Typ: **UINT \***</span><span class="sxs-lookup"><span data-stu-id="8af7b-127">Type: **UINT\***</span></span>

<span data-ttu-id="8af7b-128">Wenn diese Funktion zurückgegeben wird, enthält sie einen Zeiger auf den Ressourcenbezeichner des extrahierten Symbols, das am besten zum aktuellen Anzeigegerät passt.</span><span class="sxs-lookup"><span data-stu-id="8af7b-128">When this function returns, contains a pointer to the resource identifier of the extracted icon that best fits the current display device.</span></span> <span data-ttu-id="8af7b-129">Wenn für dieses Format kein Bezeichner verfügbar ist, enthält es 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="8af7b-129">If there is no identifier available for this format, it contains 0xFFFFFFFF.</span></span> <span data-ttu-id="8af7b-130">Wenn aus einem anderen Grund kein Bezeichner erhalten werden kann, gibt 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="8af7b-130">If no identifier can be obtained for any other reason, returns zero.</span></span>

</dd> <dt>

<span data-ttu-id="8af7b-131">*nIcons* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="8af7b-131">*nIcons* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8af7b-132">Typ: **UINT**</span><span class="sxs-lookup"><span data-stu-id="8af7b-132">Type: **UINT**</span></span>

<span data-ttu-id="8af7b-133">Die Anzahl der Symbole, die aus der Ressource mit dem Namen in *pszFileName extrahiert werden.*</span><span class="sxs-lookup"><span data-stu-id="8af7b-133">The number of icons to extract from the resource named in *pszFileName*.</span></span> <span data-ttu-id="8af7b-134">Dieser Parameter ist nur gültig, wenn die Ressource eine EXE- oder DLL-Datei ist.</span><span class="sxs-lookup"><span data-stu-id="8af7b-134">This parameter is valid only when the resource is a .exe or .dll file.</span></span>

</dd> <dt>

<span data-ttu-id="8af7b-135">*Flags* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="8af7b-135">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8af7b-136">Typ: **UINT**</span><span class="sxs-lookup"><span data-stu-id="8af7b-136">Type: **UINT**</span></span>

<span data-ttu-id="8af7b-137">Die Flags, die diese Funktion steuern.</span><span class="sxs-lookup"><span data-stu-id="8af7b-137">The flags that control this function.</span></span> <span data-ttu-id="8af7b-138">Mögliche Werte finden Sie unter *dem fuLoad-Parameter* der [**LoadImage-Funktion.**](/windows/win32/api/winuser/nf-winuser-loadimagea)</span><span class="sxs-lookup"><span data-stu-id="8af7b-138">For possible values, see the *fuLoad* parameter of the [**LoadImage**](/windows/win32/api/winuser/nf-winuser-loadimagea) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8af7b-139">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8af7b-139">Return value</span></span>

<span data-ttu-id="8af7b-140">Typ: **UINT**</span><span class="sxs-lookup"><span data-stu-id="8af7b-140">Type: **UINT**</span></span>

<span data-ttu-id="8af7b-141">Ein Wert ungleich 0 (null), wenn erfolgreich; andernfalls 0 (null).</span><span class="sxs-lookup"><span data-stu-id="8af7b-141">A nonzero value if successful; otherwise, zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="8af7b-142">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8af7b-142">Remarks</span></span>

<span data-ttu-id="8af7b-143">**SHExtractIconsW** extrahiert aus den folgenden Dateitypen.</span><span class="sxs-lookup"><span data-stu-id="8af7b-143">**SHExtractIconsW** extracts from the following file types.</span></span>

-   <span data-ttu-id="8af7b-144">Ausführbare Datei (.exe)</span><span class="sxs-lookup"><span data-stu-id="8af7b-144">Executable (.exe)</span></span>
-   <span data-ttu-id="8af7b-145">DLL (.dll)</span><span class="sxs-lookup"><span data-stu-id="8af7b-145">DLL (.dll)</span></span>
-   <span data-ttu-id="8af7b-146">Symbol (.ico)</span><span class="sxs-lookup"><span data-stu-id="8af7b-146">Icon (.ico)</span></span>
-   <span data-ttu-id="8af7b-147">Cursor (.cur)</span><span class="sxs-lookup"><span data-stu-id="8af7b-147">Cursor (.cur)</span></span>
-   <span data-ttu-id="8af7b-148">Animierter Cursor (.ani)</span><span class="sxs-lookup"><span data-stu-id="8af7b-148">Animated cursor (.ani)</span></span>
-   <span data-ttu-id="8af7b-149">Bitmap (.bmp)</span><span class="sxs-lookup"><span data-stu-id="8af7b-149">Bitmap (.bmp)</span></span>

<span data-ttu-id="8af7b-150">Extraktionen aus Windows 3. *x* ausführbare 16-Bit-Dateien (EXE oder DLL) werden ebenfalls unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8af7b-150">Extractions from Windows 3.*x* 16-bit executable files (.exe or .dll) are also supported.</span></span>

<span data-ttu-id="8af7b-151">Die Parameter *cxIcon* und *cyIcon* geben die Größe der zu extrahierende Symbole an.</span><span class="sxs-lookup"><span data-stu-id="8af7b-151">The *cxIcon* and *cyIcon* parameters specify the size of the icons to extract.</span></span> <span data-ttu-id="8af7b-152">Zwei Größen können über jeden Parameter extrahiert werden, indem der Wert zwischen LOWORD und HIWORD aufgeteilt wird.</span><span class="sxs-lookup"><span data-stu-id="8af7b-152">Two sizes can be extracted through each parameter by splitting the value between its LOWORD and HIWORD.</span></span> <span data-ttu-id="8af7b-153">Legen Sie die erste gewünschte Größe in loword des Parameters und die zweite Größe in hiword ein.</span><span class="sxs-lookup"><span data-stu-id="8af7b-153">Put the first desired size in the LOWORD of the parameter and the second size in the HIWORD.</span></span> <span data-ttu-id="8af7b-154">Beispielsweise extrahiert [**MAKELONG**](/previous-versions/windows/desktop/legacy/ms632660(v=vs.85))(24, 48) sowohl für *cxIcon* als auch *für cyIcon* symbole mit einer Größe von 24 und 48.</span><span class="sxs-lookup"><span data-stu-id="8af7b-154">For example, [**MAKELONG**](/previous-versions/windows/desktop/legacy/ms632660(v=vs.85))(24, 48) for both *cxIcon* and *cyIcon* extracts both 24 and 48 sized icons.</span></span>

<span data-ttu-id="8af7b-155">Der aufrufende Prozess ist dafür verantwortlich, alle Über diese Funktion extrahierten Symbole zu zerstören, indem die [**DestroyIcon-Funktion**](/windows/win32/api/winuser/nf-winuser-destroyicon) aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="8af7b-155">The calling process is responsible for destroying all icons extracted through this function by calling the [**DestroyIcon**](/windows/win32/api/winuser/nf-winuser-destroyicon) function.</span></span>

<span data-ttu-id="8af7b-156">**SHExtractIconsW** wird nicht anhand des Namens exportiert oder in einer öffentlichen Headerdatei deklariert.</span><span class="sxs-lookup"><span data-stu-id="8af7b-156">**SHExtractIconsW** is not exported by name or declared in a public header file.</span></span> <span data-ttu-id="8af7b-157">Um ihn zu verwenden, müssen Sie einen übereinstimmenden Prototyp deklarieren und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) verwenden, um einen Funktionszeiger von Shell32.dll anzufordern, der zum Aufrufen dieser Funktion verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="8af7b-157">To use it, you must declare a matching prototype and use [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) to request a function pointer from Shell32.dll that can be used to call this function.</span></span>

## <a name="requirements"></a><span data-ttu-id="8af7b-158">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8af7b-158">Requirements</span></span>



| <span data-ttu-id="8af7b-159">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8af7b-159">Requirement</span></span> | <span data-ttu-id="8af7b-160">Wert</span><span class="sxs-lookup"><span data-stu-id="8af7b-160">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8af7b-161">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8af7b-161">Minimum supported client</span></span><br/> | <span data-ttu-id="8af7b-162">Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8af7b-162">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8af7b-163">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8af7b-163">Minimum supported server</span></span><br/> | <span data-ttu-id="8af7b-164">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8af7b-164">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="8af7b-165">DLL</span><span class="sxs-lookup"><span data-stu-id="8af7b-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8af7b-166"><dt>Shell32.dll (Version 5.0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="8af7b-166"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |
| <span data-ttu-id="8af7b-167">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="8af7b-167">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="8af7b-168">**SHExtractIconsW** (Unicode)</span><span class="sxs-lookup"><span data-stu-id="8af7b-168">**SHExtractIconsW** (Unicode)</span></span><br/>                                                                      |



 

 
