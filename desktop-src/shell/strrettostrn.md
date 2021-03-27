---
description: 'Nimmt eine von IShellFolder:: GetDisplayNameOf zurückgegebene "strinret"-Struktur, konvertiert sie in eine Zeichenfolge und platziert das Ergebnis in einem Puffer.'
title: "\"Strauch\"-Funktion"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StrRetToStrN
api_type:
- DllExport
api_location:
- Shell32.dll
ms.assetid: a816fb5f-8320-4b63-a85d-dd4c59596ead
ms.openlocfilehash: 89a8d991e22e8615456bd8d4690c046ec0d325d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104995174"
---
# <a name="strrettostrn-function"></a><span data-ttu-id="54734-103">"Strauch"-Funktion</span><span class="sxs-lookup"><span data-stu-id="54734-103">StrRetToStrN function</span></span>

<span data-ttu-id="54734-104">Nimmt eine von [**IShellFolder:: GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof)zurückgegebene " [**strinret**](/windows/desktop/api/Shtypes/ns-shtypes-strret) "-Struktur, konvertiert sie in eine Zeichenfolge und platziert das Ergebnis in einem Puffer.</span><span class="sxs-lookup"><span data-stu-id="54734-104">Takes an [**STRRET**](/windows/desktop/api/Shtypes/ns-shtypes-strret) structure returned by [**IShellFolder::GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof), converts it to a string, and places the result in a buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="54734-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="54734-105">Syntax</span></span>


```C++
BOOL StrRetToStrN(
  _Out_   LPTSTR        pszOut,
  _In_    UINT          cchOut,
  _Inout_ LPSTRRET      pStrRet,
  _In_    LPCITEMIDLIST pidl
);
```



## <a name="parameters"></a><span data-ttu-id="54734-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="54734-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54734-107">*pszout* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="54734-107">*pszOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="54734-108">Typ: **LPTSTR**</span><span class="sxs-lookup"><span data-stu-id="54734-108">Type: **LPTSTR**</span></span>

<span data-ttu-id="54734-109">Puffer, der den anzeigen Amen enthalten soll.</span><span class="sxs-lookup"><span data-stu-id="54734-109">Buffer to hold the display name.</span></span> <span data-ttu-id="54734-110">Sie wird als eine NULL-terminierte Zeichenfolge zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="54734-110">It will be returned as a null-terminated string.</span></span> <span data-ttu-id="54734-111">Wenn das *cchout* zu klein ist, wird der Name abgeschnitten, damit er passt.</span><span class="sxs-lookup"><span data-stu-id="54734-111">If *cchOut* is too small, the name will be truncated to fit.</span></span>

</dd> <dt>

<span data-ttu-id="54734-112">*cchout* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="54734-112">*cchOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54734-113">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="54734-113">Type: **UINT**</span></span>

<span data-ttu-id="54734-114">Größe von *pszout* in Zeichen.</span><span class="sxs-lookup"><span data-stu-id="54734-114">Size of *pszOut*, in characters.</span></span> <span data-ttu-id="54734-115">Wenn das *cchout* zu klein ist, wird die Zeichenfolge gekürzt, damit Sie passt.</span><span class="sxs-lookup"><span data-stu-id="54734-115">If *cchOut* is too small, the string will be truncated to fit.</span></span>

</dd> <dt>

<span data-ttu-id="54734-116">*pstrauret* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="54734-116">*pStrRet* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="54734-117">Typ: **lpstrauret**</span><span class="sxs-lookup"><span data-stu-id="54734-117">Type: **LPSTRRET**</span></span>

<span data-ttu-id="54734-118">Zeiger auf eine " [**strinret**](/windows/desktop/api/Shtypes/ns-shtypes-strret) "-Struktur.</span><span class="sxs-lookup"><span data-stu-id="54734-118">Pointer to an [**STRRET**](/windows/desktop/api/Shtypes/ns-shtypes-strret) structure.</span></span> <span data-ttu-id="54734-119">Wenn die Funktion zurückgegeben wird, ist dieser Zeiger nicht mehr gültig.</span><span class="sxs-lookup"><span data-stu-id="54734-119">When the function returns, this pointer will no longer be valid.</span></span>

</dd> <dt>

<span data-ttu-id="54734-120">*PIDL* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="54734-120">*pidl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54734-121">Typ: **lpcitemittellist**</span><span class="sxs-lookup"><span data-stu-id="54734-121">Type: **LPCITEMIDLIST**</span></span>

<span data-ttu-id="54734-122">Ein Zeiger auf die [**itemittellist**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) -Struktur des Elements.</span><span class="sxs-lookup"><span data-stu-id="54734-122">Pointer to the item's [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54734-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="54734-123">Return value</span></span>

<span data-ttu-id="54734-124">Typ: **bool**</span><span class="sxs-lookup"><span data-stu-id="54734-124">Type: **BOOL**</span></span>

<span data-ttu-id="54734-125">**True** für Erfolg, **false** für Fehler.</span><span class="sxs-lookup"><span data-stu-id="54734-125">**TRUE** for success, **FALSE** for failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="54734-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="54734-126">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="54734-127">Ab Shell32.dll Version 5,0 entspricht das Aufrufen dieser Funktion dem Aufrufen von " [**straurettobuf**](/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobufa)".</span><span class="sxs-lookup"><span data-stu-id="54734-127">As of Shell32.dll version 5.0, calling this function is equivalent to calling [**StrRetToBuf**](/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobufa).</span></span>

 

<span data-ttu-id="54734-128"> "" "" "" "" "" ".</span><span class="sxs-lookup"><span data-stu-id="54734-128">**StrRetToStrN** is not exported by name.</span></span> <span data-ttu-id="54734-129">Um es zu verwenden, müssen Sie [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) und Request Ordnungszahl 96 aus Shell32.dll verwenden, um einen Funktionszeiger zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="54734-129">To use it, you must use [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) and request ordinal 96 from Shell32.dll to obtain a function pointer.</span></span>

<span data-ttu-id="54734-130">Wenn das **uType** -Element der Struktur, auf die von *pstrinret* verwiesen wird, auf " **chanret \_ WSTR**" festgelegt ist, wird der **polestr** -Member dieser Struktur bei der Rückgabe freigegeben.</span><span class="sxs-lookup"><span data-stu-id="54734-130">If the **uType** member of the structure pointed to by *pStrRet* is set to **STRRET\_WSTR**, the **pOleStr** member of that structure will be freed on return.</span></span>

<span data-ttu-id="54734-131">Beachten Sie, dass diese Funktion aus Shell32.dll und nicht Shlwapi.dll exportiert wird.</span><span class="sxs-lookup"><span data-stu-id="54734-131">Note that this function is exported from Shell32.dll rather than Shlwapi.dll.</span></span> <span data-ttu-id="54734-132">Es ist auch in "shlobj. h" und nicht in "shlwapi. h" enthalten.</span><span class="sxs-lookup"><span data-stu-id="54734-132">It is also included in Shlobj.h rather than Shlwapi.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="54734-133">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="54734-133">Requirements</span></span>



| <span data-ttu-id="54734-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="54734-134">Requirement</span></span> | <span data-ttu-id="54734-135">Wert</span><span class="sxs-lookup"><span data-stu-id="54734-135">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54734-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="54734-136">Minimum supported client</span></span><br/> | <span data-ttu-id="54734-137">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="54734-137">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="54734-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="54734-138">Minimum supported server</span></span><br/> | <span data-ttu-id="54734-139">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="54734-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="54734-140">DLL</span><span class="sxs-lookup"><span data-stu-id="54734-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="54734-141"><dt>Shell32.dll (Version 4,71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="54734-141"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54734-142">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="54734-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54734-143">**"Strauch"**</span><span class="sxs-lookup"><span data-stu-id="54734-143">**StrRetToStr**</span></span>](/windows/desktop/api/Shlwapi/nf-shlwapi-strrettostra)
</dt> <dt>

[<span data-ttu-id="54734-144">**"Stringebuf"**</span><span class="sxs-lookup"><span data-stu-id="54734-144">**StrRetToBuf**</span></span>](/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobufa)
</dt> </dl>

 

 
