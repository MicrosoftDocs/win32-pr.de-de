---
description: Verwendet eine von IShellFolder::GetDisplayNameOf zurückgegebene STRRET-Struktur, konvertiert sie in eine Zeichenfolge und platziert das Ergebnis in einen Puffer.
title: StrRetToStrN-Funktion
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
ms.openlocfilehash: 50295d712e539c94f10a708674cea595a47ae4e0
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841031"
---
# <a name="strrettostrn-function"></a><span data-ttu-id="02fae-103">StrRetToStrN-Funktion</span><span class="sxs-lookup"><span data-stu-id="02fae-103">StrRetToStrN function</span></span>

<span data-ttu-id="02fae-104">Verwendet eine [**strret-Struktur,**](/windows/desktop/api/Shtypes/ns-shtypes-strret) die von [**IShellFolder::GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof)zurückgegeben wird, konvertiert sie in eine Zeichenfolge und platziert das Ergebnis in einen Puffer.</span><span class="sxs-lookup"><span data-stu-id="02fae-104">Takes an [**STRRET**](/windows/desktop/api/Shtypes/ns-shtypes-strret) structure returned by [**IShellFolder::GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof), converts it to a string, and places the result in a buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="02fae-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="02fae-105">Syntax</span></span>


```C++
BOOL StrRetToStrN(
  _Out_   LPTSTR        pszOut,
  _In_    UINT          cchOut,
  _Inout_ LPSTRRET      pStrRet,
  _In_    LPCITEMIDLIST pidl
);
```



## <a name="parameters"></a><span data-ttu-id="02fae-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="02fae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02fae-107">*pszOut* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="02fae-107">*pszOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="02fae-108">Typ: **LPTSTR**</span><span class="sxs-lookup"><span data-stu-id="02fae-108">Type: **LPTSTR**</span></span>

<span data-ttu-id="02fae-109">Puffer zum Halten des Anzeigenamens.</span><span class="sxs-lookup"><span data-stu-id="02fae-109">Buffer to hold the display name.</span></span> <span data-ttu-id="02fae-110">Sie wird als auf NULL beendete Zeichenfolge zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="02fae-110">It will be returned as a null-terminated string.</span></span> <span data-ttu-id="02fae-111">Wenn *cchOut* zu klein ist, wird der Name abgeschnitten, damit er passt.</span><span class="sxs-lookup"><span data-stu-id="02fae-111">If *cchOut* is too small, the name will be truncated to fit.</span></span>

</dd> <dt>

<span data-ttu-id="02fae-112">*cchOut* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="02fae-112">*cchOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02fae-113">Typ: **UINT**</span><span class="sxs-lookup"><span data-stu-id="02fae-113">Type: **UINT**</span></span>

<span data-ttu-id="02fae-114">Größe von *pszOut* in Zeichen.</span><span class="sxs-lookup"><span data-stu-id="02fae-114">Size of *pszOut*, in characters.</span></span> <span data-ttu-id="02fae-115">Wenn *cchOut* zu klein ist, wird die Zeichenfolge abgeschnitten, damit sie passt.</span><span class="sxs-lookup"><span data-stu-id="02fae-115">If *cchOut* is too small, the string will be truncated to fit.</span></span>

</dd> <dt>

<span data-ttu-id="02fae-116">*pStrRet* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="02fae-116">*pStrRet* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="02fae-117">Typ: **LPSTRRET**</span><span class="sxs-lookup"><span data-stu-id="02fae-117">Type: **LPSTRRET**</span></span>

<span data-ttu-id="02fae-118">Zeiger auf eine [**STRRET-Struktur.**](/windows/desktop/api/Shtypes/ns-shtypes-strret)</span><span class="sxs-lookup"><span data-stu-id="02fae-118">Pointer to an [**STRRET**](/windows/desktop/api/Shtypes/ns-shtypes-strret) structure.</span></span> <span data-ttu-id="02fae-119">Wenn die Funktion zurückgegeben wird, ist dieser Zeiger nicht mehr gültig.</span><span class="sxs-lookup"><span data-stu-id="02fae-119">When the function returns, this pointer will no longer be valid.</span></span>

</dd> <dt>

<span data-ttu-id="02fae-120">*pidl* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="02fae-120">*pidl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02fae-121">Typ: **LPJSMIDLIST**</span><span class="sxs-lookup"><span data-stu-id="02fae-121">Type: **LPCITEMIDLIST**</span></span>

<span data-ttu-id="02fae-122">Zeiger auf die [**ITEMIDLIST-Struktur des**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) Elements.</span><span class="sxs-lookup"><span data-stu-id="02fae-122">Pointer to the item's [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02fae-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="02fae-123">Return value</span></span>

<span data-ttu-id="02fae-124">Typ: **BOOL**</span><span class="sxs-lookup"><span data-stu-id="02fae-124">Type: **BOOL**</span></span>

<span data-ttu-id="02fae-125">**TRUE** für Erfolg, **FALSE** für Fehler.</span><span class="sxs-lookup"><span data-stu-id="02fae-125">**TRUE** for success, **FALSE** for failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="02fae-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="02fae-126">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="02fae-127">Ab Shell32.dll Version 5.0 entspricht das Aufrufen dieser Funktion dem Aufruf von [**StrRetToBuf.**](/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobufa)</span><span class="sxs-lookup"><span data-stu-id="02fae-127">As of Shell32.dll version 5.0, calling this function is equivalent to calling [**StrRetToBuf**](/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobufa).</span></span>

 

<span data-ttu-id="02fae-128">**StrRetToStrN** wird nicht anhand des Namens exportiert.</span><span class="sxs-lookup"><span data-stu-id="02fae-128">**StrRetToStrN** is not exported by name.</span></span> <span data-ttu-id="02fae-129">Um es zu verwenden, müssen Sie [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) verwenden und Ordnungszahl 96 von Shell32.dll anfordern, um einen Funktionszeiger abzurufen.</span><span class="sxs-lookup"><span data-stu-id="02fae-129">To use it, you must use [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) and request ordinal 96 from Shell32.dll to obtain a function pointer.</span></span>

<span data-ttu-id="02fae-130">Wenn der **uType-Member** der -Struktur, auf die *pStrRet* zeigt, auf **STRRET \_ WSTR** festgelegt ist, wird der **pOleStr-Member** dieser Struktur bei der Rückgabe freigegeben.</span><span class="sxs-lookup"><span data-stu-id="02fae-130">If the **uType** member of the structure pointed to by *pStrRet* is set to **STRRET\_WSTR**, the **pOleStr** member of that structure will be freed on return.</span></span>

<span data-ttu-id="02fae-131">Beachten Sie, dass diese Funktion nicht aus Shlwapi.dll, sondern aus Shell32.dll exportiert wird.</span><span class="sxs-lookup"><span data-stu-id="02fae-131">Note that this function is exported from Shell32.dll rather than Shlwapi.dll.</span></span> <span data-ttu-id="02fae-132">Sie ist auch in "Shlobj.h" und nicht in "Shlwapi.h" enthalten.</span><span class="sxs-lookup"><span data-stu-id="02fae-132">It is also included in Shlobj.h rather than Shlwapi.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="02fae-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="02fae-133">Requirements</span></span>



| <span data-ttu-id="02fae-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="02fae-134">Requirement</span></span> | <span data-ttu-id="02fae-135">Wert</span><span class="sxs-lookup"><span data-stu-id="02fae-135">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02fae-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="02fae-136">Minimum supported client</span></span><br/> | <span data-ttu-id="02fae-137">Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="02fae-137">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="02fae-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="02fae-138">Minimum supported server</span></span><br/> | <span data-ttu-id="02fae-139">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="02fae-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="02fae-140">DLL</span><span class="sxs-lookup"><span data-stu-id="02fae-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="02fae-141"><dt>Shell32.dll (Version 4.71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="02fae-141"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02fae-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="02fae-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02fae-143">**StrRetToStr**</span><span class="sxs-lookup"><span data-stu-id="02fae-143">**StrRetToStr**</span></span>](/windows/desktop/api/Shlwapi/nf-shlwapi-strrettostra)
</dt> <dt>

[<span data-ttu-id="02fae-144">**StrRetToBuf**</span><span class="sxs-lookup"><span data-stu-id="02fae-144">**StrRetToBuf**</span></span>](/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobufa)
</dt> </dl>

 

 
