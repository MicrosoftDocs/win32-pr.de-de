---
title: Drawtextwrap-Funktion
description: Zeichnet formatierten Text im angegebenen Rechteck. Er formatiert den Text gemäß der angegebenen Methode (erweitert Registerkarten, rechtfertigt Zeichen, Zeilenumbruch usw.). Diese Funktion umschließt einen aufzurufenden DrawText-Befehl.
ms.assetid: 28ab4c5e-3b8f-49e8-b072-500ba1916caf
keywords:
- Windows-Steuerelemente der drawtextwrap-Funktion
topic_type:
- apiref
api_name:
- DrawTextWrap
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfc5eb707b4016a592ad339223e0f32ab21d4a29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949469"
---
# <a name="drawtextwrap-function"></a><span data-ttu-id="3c99f-106">Drawtextwrap-Funktion</span><span class="sxs-lookup"><span data-stu-id="3c99f-106">DrawTextWrap function</span></span>

<span data-ttu-id="3c99f-107">\[**Drawtextwrap** ist über Windows XP mit Service Pack 2 (SP2) verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3c99f-107">\[**DrawTextWrap** is available through Windows XP with Service Pack 2 (SP2).</span></span> <span data-ttu-id="3c99f-108">Sie wird möglicherweise in nachfolgenden Versionen geändert oder ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3c99f-108">It might be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="3c99f-109">Es wird empfohlen, stattdessen [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) direkt zu verwenden.\]</span><span class="sxs-lookup"><span data-stu-id="3c99f-109">It is recommended to use [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) directly instead.\]</span></span>

<span data-ttu-id="3c99f-110">Zeichnet formatierten Text im angegebenen Rechteck.</span><span class="sxs-lookup"><span data-stu-id="3c99f-110">Draws formatted text in the specified rectangle.</span></span> <span data-ttu-id="3c99f-111">Er formatiert den Text gemäß der angegebenen Methode (erweitert Registerkarten, rechtfertigt Zeichen, Zeilenumbruch usw.).</span><span class="sxs-lookup"><span data-stu-id="3c99f-111">It formats the text according to the specified method (expanding tabs, justifying characters, breaking lines, and so on).</span></span> <span data-ttu-id="3c99f-112">Diese Funktion umschließt einen aufzurufenden [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext)-Befehl.</span><span class="sxs-lookup"><span data-stu-id="3c99f-112">This function wraps a call to [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext).</span></span>

## <a name="syntax"></a><span data-ttu-id="3c99f-113">Syntax</span><span class="sxs-lookup"><span data-stu-id="3c99f-113">Syntax</span></span>


```C++
int WINAPI DrawTextWrap(
  _In_    HDC              hdc,
  _Inout_ LPCTSTR          lpString,
  _In_    int              nCount,
  _Inout_ LPRECT           lpRect,
  _In_    UINT             uFormat,
  _In_    LPDRAWTEXTPARAMS lpDTParams
);
```



## <a name="parameters"></a><span data-ttu-id="3c99f-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="3c99f-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c99f-115">*hdc* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3c99f-115">*hdc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c99f-116">Typ: **[ **hdc**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="3c99f-116">Type: **[**HDC**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="3c99f-117">Ein Handle für den Gerätekontext.</span><span class="sxs-lookup"><span data-stu-id="3c99f-117">A handle to the device context.</span></span>

</dd> <dt>

<span data-ttu-id="3c99f-118">*lpString* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="3c99f-118">*lpString* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="3c99f-119">Typ: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="3c99f-119">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="3c99f-120">Ein Zeiger auf einen Puffer, der den zu zeichnenden Text enthält.</span><span class="sxs-lookup"><span data-stu-id="3c99f-120">A pointer to a buffer that contains the text to draw.</span></span> <span data-ttu-id="3c99f-121">Wenn der *nCount* -Parameter-1 ist, muss die Zeichenfolge mit Null beendet werden.</span><span class="sxs-lookup"><span data-stu-id="3c99f-121">If the *nCount* parameter is -1, the string must be null-terminated.</span></span>

<span data-ttu-id="3c99f-122">Wenn " *Uformat* " dt \_ modifystring enthält, kann die Funktion dieser Zeichenfolge bis zu vier zusätzliche Zeichen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="3c99f-122">If *uFormat* includes DT\_MODIFYSTRING, the function might add up to four additional characters to this string.</span></span> <span data-ttu-id="3c99f-123">Der Puffer, der die Zeichenfolge enthält, sollte groß genug sein, um diese zusätzlichen Zeichen aufnehmen zu können.</span><span class="sxs-lookup"><span data-stu-id="3c99f-123">The buffer that contains the string should be large enough to accommodate these extra characters.</span></span>

</dd> <dt>

<span data-ttu-id="3c99f-124">*nCount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3c99f-124">*nCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c99f-125">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="3c99f-125">Type: **int**</span></span>

<span data-ttu-id="3c99f-126">Die Länge der Zeichenfolge, auf die von *lpString* verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="3c99f-126">The length of the string pointed to by *lpString*.</span></span> <span data-ttu-id="3c99f-127">Wenn *nCount* den Wert-1 hat, wird angenommen, dass der *lpString* -Parameter ein Zeiger auf eine auf NULL endende Zeichenfolge ist, und [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) berechnet automatisch die Zeichen Anzahl.</span><span class="sxs-lookup"><span data-stu-id="3c99f-127">If *nCount* is -1, then the *lpString* parameter is assumed to be a pointer to a null-terminated string and [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) computes the character count automatically.</span></span>

</dd> <dt>

<span data-ttu-id="3c99f-128">*lprect* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="3c99f-128">*lpRect* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="3c99f-129">Typ: **lprect**</span><span class="sxs-lookup"><span data-stu-id="3c99f-129">Type: **LPRECT**</span></span>

<span data-ttu-id="3c99f-130">Ein Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur, die das Rechteck in logischen Koordinaten enthält, in dem der Text formatiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="3c99f-130">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that contains the rectangle, in logical coordinates, in which the text is to be formatted.</span></span>

</dd> <dt>

<span data-ttu-id="3c99f-131">*Uformat* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3c99f-131">*uFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c99f-132">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="3c99f-132">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="3c99f-133">Die Formatierungsoptionen.</span><span class="sxs-lookup"><span data-stu-id="3c99f-133">The formatting options.</span></span> <span data-ttu-id="3c99f-134">Eine vollständige Liste der Optionen finden Sie in der Dokumentation zu [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) .</span><span class="sxs-lookup"><span data-stu-id="3c99f-134">See the documentation for [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) for a complete list of options.</span></span>

</dd> <dt>

<span data-ttu-id="3c99f-135">*lpdtparametriams* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3c99f-135">*lpDTParams* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c99f-136">Typ: **lpdrawtextparametriams**</span><span class="sxs-lookup"><span data-stu-id="3c99f-136">Type: **LPDRAWTEXTPARAMS**</span></span>

<span data-ttu-id="3c99f-137">Ein Zeiger auf eine [**drawtextparameams**](/windows/win32/api/winuser/ns-winuser-drawtextparams) -Struktur, die zusätzliche Formatierungsoptionen angibt.</span><span class="sxs-lookup"><span data-stu-id="3c99f-137">A pointer to a [**DRAWTEXTPARAMS**](/windows/win32/api/winuser/ns-winuser-drawtextparams) structure that specifies additional formatting options.</span></span> <span data-ttu-id="3c99f-138">Dieser Parameter kann **NULL** sein.</span><span class="sxs-lookup"><span data-stu-id="3c99f-138">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c99f-139">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3c99f-139">Return value</span></span>

<span data-ttu-id="3c99f-140">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="3c99f-140">Type: **int**</span></span>

<span data-ttu-id="3c99f-141">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert die Texthöhe in logischen Einheiten.</span><span class="sxs-lookup"><span data-stu-id="3c99f-141">If the function succeeds, the return value is the text height in logical units.</span></span> <span data-ttu-id="3c99f-142">Wenn **dt \_ vCenter** oder **dt \_ Bottom** angegeben ist, ist der Rückgabewert der Offset vom **obersten** Member von *LPRC* bis zum unteren Rand des gezeichneten Texts, wenn die Funktion fehlschlägt, der Rückgabewert 0 (null) ist.</span><span class="sxs-lookup"><span data-stu-id="3c99f-142">If **DT\_VCENTER** or **DT\_BOTTOM** is specified, the return value is the offset from the **top** member of *lprc* to the bottom of the drawn text If the function fails, the return value is zero.</span></span>

<span data-ttu-id="3c99f-143">Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.</span><span class="sxs-lookup"><span data-stu-id="3c99f-143">If the function fails, the return value is zero.</span></span>

<span data-ttu-id="3c99f-144">Um erweiterte Fehlerinformationen zu erhalten, rufen Sie [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) auf.</span><span class="sxs-lookup"><span data-stu-id="3c99f-144">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="3c99f-145">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3c99f-145">Remarks</span></span>

<span data-ttu-id="3c99f-146">**Drawtextwrap** wird nicht nach Name exportiert oder in einem öffentlichen Header deklariert.</span><span class="sxs-lookup"><span data-stu-id="3c99f-146">**DrawTextWrap** is not exported by name or declared in a public header.</span></span> <span data-ttu-id="3c99f-147">Um es zu verwenden, müssen Sie [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) und Request Ordnungszahl 415 aus ComCtl32.dll verwenden, um einen Funktionszeiger zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="3c99f-147">To use it, you must use [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) and request ordinal 415 from ComCtl32.dll to obtain a function pointer.</span></span>

<span data-ttu-id="3c99f-148">Weitere Hinweise finden Sie unter [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext).</span><span class="sxs-lookup"><span data-stu-id="3c99f-148">For additional remarks, please see [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext).</span></span>

## <a name="requirements"></a><span data-ttu-id="3c99f-149">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3c99f-149">Requirements</span></span>



| <span data-ttu-id="3c99f-150">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3c99f-150">Requirement</span></span> | <span data-ttu-id="3c99f-151">Wert</span><span class="sxs-lookup"><span data-stu-id="3c99f-151">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c99f-152">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3c99f-152">Minimum supported client</span></span><br/> | <span data-ttu-id="3c99f-153">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3c99f-153">Windows Vista \[desktop apps only\]</span></span><br/>                                                                 |
| <span data-ttu-id="3c99f-154">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3c99f-154">Minimum supported server</span></span><br/> | <span data-ttu-id="3c99f-155">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3c99f-155">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="3c99f-156">DLL</span><span class="sxs-lookup"><span data-stu-id="3c99f-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c99f-157"><dt>Comctl32.dll (Version 6,0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="3c99f-157"><dt>Comctl32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

