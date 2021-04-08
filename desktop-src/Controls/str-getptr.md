---
title: Str_GetPtr-Funktion
description: Kopiert eine Zeichenfolge von einem Puffer in einen anderen.
ms.assetid: a3dd55a0-3f8b-4d6c-9956-666bebc3ab8d
keywords:
- Windows-Steuerelemente Str_GetPtr-Funktion
topic_type:
- apiref
api_name:
- Str_GetPtr
- Str_GetPtrA
- Str_GetPtrW
api_location:
- ComCtl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fec99bb4d91bde86d901c0e7ed4761bafd15f3a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740512"
---
# <a name="str_getptr-function"></a><span data-ttu-id="2a923-104">Str \_ GetPtr-Funktion</span><span class="sxs-lookup"><span data-stu-id="2a923-104">Str\_GetPtr function</span></span>

<span data-ttu-id="2a923-105">\[Diese Funktion ist über Windows XP mit Service Pack 2 (SP2) und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2a923-105">\[This function is available through Windows XP with Service Pack 2 (SP2) and Windows Server 2003.</span></span> <span data-ttu-id="2a923-106">Sie wird möglicherweise in nachfolgenden Versionen von Windows geändert oder ist nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="2a923-106">It might be altered or unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="2a923-107">Kopiert eine Zeichenfolge von einem Puffer in einen anderen.</span><span class="sxs-lookup"><span data-stu-id="2a923-107">Copies a string from one buffer to another.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a923-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="2a923-108">Syntax</span></span>


```C++
int WINAPI Str_GetPtr(
  _In_    LPCTSTR pszSource,
  _Inout_ LPCSTR  pszDest,
  _In_    int     cchDest
);
```



## <a name="parameters"></a><span data-ttu-id="2a923-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="2a923-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a923-110">*pszsource* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2a923-110">*pszSource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a923-111">Typ: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="2a923-111">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="2a923-112">Ein Zeiger auf eine Quell Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="2a923-112">A pointer to a source string.</span></span>

</dd> <dt>

<span data-ttu-id="2a923-113">*pszdest* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="2a923-113">*pszDest* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2a923-114">Typ: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="2a923-114">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="2a923-115">Ein Zeiger auf den Ziel Puffer.</span><span class="sxs-lookup"><span data-stu-id="2a923-115">A pointer to the destination buffer.</span></span> <span data-ttu-id="2a923-116">Dieser Wert kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="2a923-116">This value can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="2a923-117">*cchdest* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2a923-117">*cchDest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a923-118">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="2a923-118">Type: **int**</span></span>

<span data-ttu-id="2a923-119">Die Größe von *pszdest* in Zeichen.</span><span class="sxs-lookup"><span data-stu-id="2a923-119">The size of *pszDest*, in characters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a923-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2a923-120">Return value</span></span>

<span data-ttu-id="2a923-121">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="2a923-121">Type: **int**</span></span>

<span data-ttu-id="2a923-122">Wenn *pszdest* gleich NULL oder *cchdest* gleich NULL ist, wird die Größe des Puffers in Zeichen zurückgegeben, die eine mit NULL endenden Kopie der Zeichenfolge enthalten muss, auf die von *pszsource* **verwiesen wird.**</span><span class="sxs-lookup"><span data-stu-id="2a923-122">If *pszDest* is **NULL** or *cchDest* is zero, returns the size of the buffer, in characters, needed to contain a null-terminated copy of the string pointed to by *pszSource*.</span></span>

<span data-ttu-id="2a923-123">Wenn *pszdest* nicht **null** ist, wird die Anzahl der erfolgreich kopierten Zeichen zurückgegeben, einschließlich des abschließenden NULL-Zeichens.</span><span class="sxs-lookup"><span data-stu-id="2a923-123">If *pszDest* is non-**NULL**, returns the number of characters successfully copied, including the terminating null character.</span></span>

<span data-ttu-id="2a923-124">Wenn *pszdest* nicht die gesamte Zeichenfolge enthalten kann, auf die *pszsource* zeigt, werden (*cchdest*-1) Zeichen kopiert, die Zeichenfolge mit NULL-terminiert und *cchdest* zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2a923-124">If *pszDest* cannot hold the entire string pointed to by *pszSource*, then (*cchDest*-1) characters are copied, the string null-terminated, and *cchDest* returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a923-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2a923-125">Remarks</span></span>

<span data-ttu-id="2a923-126">**Str \_ GetPtr** ist als ANSI-(**Str \_ getptra**) und Unicode-Versionen (**Str \_ getptrw**) verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2a923-126">**Str\_GetPtr** is available as ANSI (**Str\_GetPtrA**) and Unicode (**Str\_GetPtrW**) versions.</span></span> <span data-ttu-id="2a923-127">Diese Funktionen werden nicht nach Namen exportiert oder in einer öffentlichen Header Datei deklariert.</span><span class="sxs-lookup"><span data-stu-id="2a923-127">These functions are not exported by name or declared in a public header file.</span></span> <span data-ttu-id="2a923-128">Um Sie verwenden zu können, müssen Sie [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) und Request Ordnungszahl 233 (**Str \_ getptra**) oder 235 (**Str \_ getptrw**) aus ComCtl32.dll verwenden, um einen Funktionszeiger zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="2a923-128">To use them, you must use [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) and request ordinal 233 (**Str\_GetPtrA**) or 235 (**Str\_GetPtrW**) from ComCtl32.dll to obtain a function pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a923-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2a923-129">Requirements</span></span>



| <span data-ttu-id="2a923-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2a923-130">Requirement</span></span> | <span data-ttu-id="2a923-131">Wert</span><span class="sxs-lookup"><span data-stu-id="2a923-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2a923-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2a923-132">Minimum supported client</span></span><br/> | <span data-ttu-id="2a923-133">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2a923-133">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="2a923-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2a923-134">Minimum supported server</span></span><br/> | <span data-ttu-id="2a923-135">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2a923-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2a923-136">DLL</span><span class="sxs-lookup"><span data-stu-id="2a923-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2a923-137"><dt>ComCtl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2a923-137"><dt>ComCtl32.dll</dt></span></span> </dl> |
| <span data-ttu-id="2a923-138">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="2a923-138">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="2a923-139">**Str \_ Getptrw** (Unicode) und **Str \_ getptra** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="2a923-139">**Str\_GetPtrW** (Unicode) and **Str\_GetPtrA** (ANSI)</span></span><br/>                       |



 

