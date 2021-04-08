---
title: GetTextExtentPoint32Wrap-Funktion
description: Berechnet die Breite und Höhe der angegebenen Text Zeichenfolge. Diese Funktion umschließt einen Aufrufen von GetTextExtentPoint.
ms.assetid: 156f9344-6071-451c-94c7-63f369a5573a
keywords:
- GetTextExtentPoint32Wrap-Funktion Windows-Steuerelemente
topic_type:
- apiref
api_name:
- GetTextExtentPoint32Wrap
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6a0db92ad019950cf8be0a72260da75acc06779
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740112"
---
# <a name="gettextextentpoint32wrap-function"></a><span data-ttu-id="50923-105">GetTextExtentPoint32Wrap-Funktion</span><span class="sxs-lookup"><span data-stu-id="50923-105">GetTextExtentPoint32Wrap function</span></span>

<span data-ttu-id="50923-106">\[**GetTextExtentPoint32Wrap** ist über Windows XP mit Service Pack 2 (SP2) verfügbar.</span><span class="sxs-lookup"><span data-stu-id="50923-106">\[**GetTextExtentPoint32Wrap** is available through Windows XP with Service Pack 2 (SP2).</span></span> <span data-ttu-id="50923-107">Sie wird möglicherweise in nachfolgenden Versionen geändert oder ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="50923-107">It might be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="50923-108">Es wird empfohlen, stattdessen [**GetTextExtentPoint**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpointa) direkt zu verwenden.\]</span><span class="sxs-lookup"><span data-stu-id="50923-108">It is recommended to use [**GetTextExtentPoint**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpointa) directly instead.\]</span></span>

<span data-ttu-id="50923-109">Berechnet die Breite und Höhe der angegebenen Text Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="50923-109">Computes the width and height of the specified string of text.</span></span> <span data-ttu-id="50923-110">Diese Funktion umschließt einen Aufrufen von [**GetTextExtentPoint**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpointa).</span><span class="sxs-lookup"><span data-stu-id="50923-110">This function wraps a call to [**GetTextExtentPoint**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpointa).</span></span>

## <a name="syntax"></a><span data-ttu-id="50923-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="50923-111">Syntax</span></span>


```C++
BOOL GetTextExtentPoint32Wrap(
  _In_  HDC     hdc,
  _In_  LPCTSTR lpString,
  _In_  UINT    cbCount,
  _Out_ LPSIZE  lpSize
);
```



## <a name="parameters"></a><span data-ttu-id="50923-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="50923-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50923-113">*hdc* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="50923-113">*hdc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50923-114">Typ: **[ **hdc**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="50923-114">Type: **[**HDC**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="50923-115">Ein Handle für den Gerätekontext.</span><span class="sxs-lookup"><span data-stu-id="50923-115">A handle to the device context.</span></span>

</dd> <dt>

<span data-ttu-id="50923-116">*lpString* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="50923-116">*lpString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50923-117">Typ: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="50923-117">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="50923-118">Ein Zeiger auf einen Puffer, der den Text enthält, der gezeichnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="50923-118">A pointer to a buffer that contains the text to be drawn.</span></span> <span data-ttu-id="50923-119">Die Zeichenfolge muss nicht mit 0 (null) beendet werden, da *cbcount* die Länge der Zeichenfolge angibt.</span><span class="sxs-lookup"><span data-stu-id="50923-119">The string does not need to be zero-terminated, since *cbCount* specifies the length of the string.</span></span>

</dd> <dt>

<span data-ttu-id="50923-120">*cbcount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="50923-120">*cbCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50923-121">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="50923-121">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="50923-122">Die Länge der Zeichenfolge in Bytes, auf die von *lpString* verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="50923-122">The length, in bytes, of the string pointed to by *lpString*.</span></span>

</dd> <dt>

<span data-ttu-id="50923-123">*lpsize* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="50923-123">*lpSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="50923-124">Typ: **lpsize**</span><span class="sxs-lookup"><span data-stu-id="50923-124">Type: **LPSIZE**</span></span>

<span data-ttu-id="50923-125">Wenn diese Methode zurückgegeben wird, enthält Sie einen Zeiger auf eine [**Größen**](/previous-versions//dd145106(v=vs.85)) Struktur, die die Dimensionen der Zeichenfolge in logischen Einheiten enthält.</span><span class="sxs-lookup"><span data-stu-id="50923-125">When this method returns, contains a pointer to a [**SIZE**](/previous-versions//dd145106(v=vs.85)) structure containing the dimensions of the string, in logical units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50923-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="50923-126">Return value</span></span>

<span data-ttu-id="50923-127">Typ: **[ **bool**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="50923-127">Type: **[**BOOL**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="50923-128">Gibt bei Erfolg einen Wert ungleich 0 (null) zurück. andernfalls 0.</span><span class="sxs-lookup"><span data-stu-id="50923-128">Returns a nonzero value if successful; otherwise, 0.</span></span>

<span data-ttu-id="50923-129">Um erweiterte Fehlerinformationen zu erhalten, rufen Sie [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) auf.</span><span class="sxs-lookup"><span data-stu-id="50923-129">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="50923-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="50923-130">Remarks</span></span>

<span data-ttu-id="50923-131">**GetTextExtentPoint32Wrap** wird nicht nach Name exportiert oder in einer öffentlichen Header Datei deklariert.</span><span class="sxs-lookup"><span data-stu-id="50923-131">**GetTextExtentPoint32Wrap** is not exported by name or declared in a public header file.</span></span> <span data-ttu-id="50923-132">Um es zu verwenden, müssen Sie [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) und Request Ordnungszahl 420 aus ComCtl32.dll verwenden, um einen Funktionszeiger zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="50923-132">To use it, you must use [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) and request ordinal 420 from ComCtl32.dll to obtain a function pointer.</span></span>

<span data-ttu-id="50923-133">Weitere Hinweise finden Sie unter [**GetTextExtentPoint**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpointa).</span><span class="sxs-lookup"><span data-stu-id="50923-133">For additional remarks, please see [**GetTextExtentPoint**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpointa).</span></span>

## <a name="requirements"></a><span data-ttu-id="50923-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="50923-134">Requirements</span></span>



| <span data-ttu-id="50923-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="50923-135">Requirement</span></span> | <span data-ttu-id="50923-136">Wert</span><span class="sxs-lookup"><span data-stu-id="50923-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50923-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="50923-137">Minimum supported client</span></span><br/> | <span data-ttu-id="50923-138">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="50923-138">Windows Vista \[desktop apps only\]</span></span><br/>                                                                  |
| <span data-ttu-id="50923-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="50923-139">Minimum supported server</span></span><br/> | <span data-ttu-id="50923-140">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="50923-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="50923-141">DLL</span><span class="sxs-lookup"><span data-stu-id="50923-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="50923-142"><dt>Comctl32.dll (Version 5,81 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="50923-142"><dt>Comctl32.dll (version 5.81 or later)</dt></span></span> </dl> |



 

