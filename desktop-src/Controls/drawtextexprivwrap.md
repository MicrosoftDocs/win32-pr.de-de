---
title: Drawtextexprivwrap-Funktion
description: Zeichnet formatierten Text im angegebenen Rechteck. Diese Funktion umschließt einen aufzurufenden drawtextex-Befehl.
ms.assetid: 3212282c-1adb-4f7e-b4d7-7d833b26ac60
keywords:
- Windows-Steuerelemente der drawtextexprivwrap-Funktion
topic_type:
- apiref
api_name:
- DrawTextExPrivWrap
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eba496a121af3ba88ed24ab6c9c7834c90153ec0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957189"
---
# <a name="drawtextexprivwrap-function"></a><span data-ttu-id="b7e5a-105">Drawtextexprivwrap-Funktion</span><span class="sxs-lookup"><span data-stu-id="b7e5a-105">DrawTextExPrivWrap function</span></span>

<span data-ttu-id="b7e5a-106">\[**Drawtextexprivwrap** ist über Windows XP mit Service Pack 2 (SP2) verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b7e5a-106">\[**DrawTextExPrivWrap** is available through Windows XP with Service Pack 2 (SP2).</span></span> <span data-ttu-id="b7e5a-107">Sie wird möglicherweise in nachfolgenden Versionen geändert oder ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b7e5a-107">It might be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="b7e5a-108">Es wird empfohlen, stattdessen [**drawtextex**](/windows/desktop/api/winuser/nf-winuser-drawtextexa) direkt zu verwenden.\]</span><span class="sxs-lookup"><span data-stu-id="b7e5a-108">It is recommended to use [**DrawTextEx**](/windows/desktop/api/winuser/nf-winuser-drawtextexa) directly instead.\]</span></span>

<span data-ttu-id="b7e5a-109">Zeichnet formatierten Text im angegebenen Rechteck.</span><span class="sxs-lookup"><span data-stu-id="b7e5a-109">Draws formatted text in the specified rectangle.</span></span> <span data-ttu-id="b7e5a-110">Diese Funktion umschließt einen aufzurufenden [**drawtextex**](/windows/desktop/api/winuser/nf-winuser-drawtextexa)-Befehl.</span><span class="sxs-lookup"><span data-stu-id="b7e5a-110">This function wraps a call to [**DrawTextEx**](/windows/desktop/api/winuser/nf-winuser-drawtextexa).</span></span>

## <a name="syntax"></a><span data-ttu-id="b7e5a-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="b7e5a-111">Syntax</span></span>


```C++
int WINAPI DrawTextExPrivWrap(
  _In_    HDC              hdc,
  _Inout_ LPTSTR           lpchText,
  _In_    int              cchText,
  _Inout_ LPRECT           lprc,
  _In_    UINT             dwDTFormat,
  _In_    LPDRAWTEXTPARAMS lpDTParams
);
```



## <a name="parameters"></a><span data-ttu-id="b7e5a-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="b7e5a-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7e5a-113">*hdc* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b7e5a-113">*hdc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7e5a-114">Typ: **[ **hdc**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b7e5a-114">Type: **[**HDC**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="b7e5a-115">Ein Handle für den Gerätekontext, in dem gezeichnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b7e5a-115">A handle to the device context in which to draw.</span></span>

</dd> <dt>

<span data-ttu-id="b7e5a-116">*lpchtext* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="b7e5a-116">*lpchText* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b7e5a-117">Typ: **[ **LPTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b7e5a-117">Type: **[**LPTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="b7e5a-118">Ein Zeiger auf einen Puffer, der den zu zeichnenden Text enthält.</span><span class="sxs-lookup"><span data-stu-id="b7e5a-118">A pointer to a buffer that contains the text to draw.</span></span> <span data-ttu-id="b7e5a-119">Wenn der *cchtext* -Parameter-1 ist, muss die Zeichenfolge mit Null beendet werden.</span><span class="sxs-lookup"><span data-stu-id="b7e5a-119">If the *cchText* parameter is -1, the string must be null-terminated.</span></span>

<span data-ttu-id="b7e5a-120">Wenn *dwdtformat* dt \_ modifystring enthält, kann die Funktion dieser Zeichenfolge bis zu vier zusätzliche Zeichen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="b7e5a-120">If *dwDTFormat* includes DT\_MODIFYSTRING, the function might add up to four additional characters to this string.</span></span> <span data-ttu-id="b7e5a-121">Der Puffer, der die Zeichenfolge enthält, sollte groß genug sein, um diese zusätzlichen Zeichen aufnehmen zu können.</span><span class="sxs-lookup"><span data-stu-id="b7e5a-121">The buffer that contains the string should be large enough to accommodate these extra characters.</span></span>

</dd> <dt>

<span data-ttu-id="b7e5a-122">*cchtext* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b7e5a-122">*cchText* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7e5a-123">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="b7e5a-123">Type: **int**</span></span>

<span data-ttu-id="b7e5a-124">Die Länge der Zeichenfolge, auf die von *lpchtext* verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="b7e5a-124">The length of the string pointed to by *lpchText*.</span></span> <span data-ttu-id="b7e5a-125">Wenn *cchtext* -1 ist, wird angenommen, dass der *lpchtext* -Parameter ein Zeiger auf eine mit NULL endende Zeichenfolge ist, und [**drawtextex**](/windows/desktop/api/winuser/nf-winuser-drawtextexa) berechnet automatisch die Zeichen Anzahl.</span><span class="sxs-lookup"><span data-stu-id="b7e5a-125">If *cchText* is -1, then the *lpchText* parameter is assumed to be a pointer to a null-terminated string and [**DrawTextEx**](/windows/desktop/api/winuser/nf-winuser-drawtextexa) computes the character count automatically.</span></span>

</dd> <dt>

<span data-ttu-id="b7e5a-126">*LPRC* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="b7e5a-126">*lprc* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b7e5a-127">Typ: **lprect**</span><span class="sxs-lookup"><span data-stu-id="b7e5a-127">Type: **LPRECT**</span></span>

<span data-ttu-id="b7e5a-128">Ein Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur, die das Rechteck in logischen Koordinaten enthält, in dem der Text formatiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="b7e5a-128">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that contains the rectangle, in logical coordinates, in which the text is to be formatted.</span></span>

</dd> <dt>

<span data-ttu-id="b7e5a-129">*dwdtformat* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b7e5a-129">*dwDTFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7e5a-130">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b7e5a-130">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="b7e5a-131">Die Formatierungsoptionen.</span><span class="sxs-lookup"><span data-stu-id="b7e5a-131">The formatting options.</span></span> <span data-ttu-id="b7e5a-132">Eine umfassende Liste der Optionen finden Sie in der Dokumentation zu [**drawtextex**](/windows/desktop/api/winuser/nf-winuser-drawtextexa) .</span><span class="sxs-lookup"><span data-stu-id="b7e5a-132">See the documentation for [**DrawTextEx**](/windows/desktop/api/winuser/nf-winuser-drawtextexa) for a complete list of options.</span></span>

</dd> <dt>

<span data-ttu-id="b7e5a-133">*lpdtparametriams* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b7e5a-133">*lpDTParams* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7e5a-134">Typ: **lpdrawtextparametriams**</span><span class="sxs-lookup"><span data-stu-id="b7e5a-134">Type: **LPDRAWTEXTPARAMS**</span></span>

<span data-ttu-id="b7e5a-135">Ein Zeiger auf eine [**drawtextparameams**](/windows/win32/api/winuser/ns-winuser-drawtextparams) -Struktur, die zusätzliche Formatierungsoptionen angibt.</span><span class="sxs-lookup"><span data-stu-id="b7e5a-135">A pointer to a [**DRAWTEXTPARAMS**](/windows/win32/api/winuser/ns-winuser-drawtextparams) structure that specifies additional formatting options.</span></span> <span data-ttu-id="b7e5a-136">Dieser Parameter kann **NULL** sein.</span><span class="sxs-lookup"><span data-stu-id="b7e5a-136">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7e5a-137">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b7e5a-137">Return value</span></span>

<span data-ttu-id="b7e5a-138">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="b7e5a-138">Type: **int**</span></span>

<span data-ttu-id="b7e5a-139">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert die Texthöhe in logischen Einheiten.</span><span class="sxs-lookup"><span data-stu-id="b7e5a-139">If the function succeeds, the return value is the text height in logical units.</span></span> <span data-ttu-id="b7e5a-140">Wenn **dt \_ vCenter** oder **dt \_ Bottom** angegeben ist, ist der Rückgabewert der Offset vom **obersten** Member von *LPRC* bis zum unteren Rand des gezeichneten Texts.</span><span class="sxs-lookup"><span data-stu-id="b7e5a-140">If **DT\_VCENTER** or **DT\_BOTTOM** is specified, the return value is the offset from the **top** member of *lprc* to the bottom of the drawn text.</span></span>

<span data-ttu-id="b7e5a-141">Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.</span><span class="sxs-lookup"><span data-stu-id="b7e5a-141">If the function fails, the return value is zero.</span></span>

<span data-ttu-id="b7e5a-142">Um erweiterte Fehlerinformationen zu erhalten, rufen Sie [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) auf.</span><span class="sxs-lookup"><span data-stu-id="b7e5a-142">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="b7e5a-143">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b7e5a-143">Remarks</span></span>

<span data-ttu-id="b7e5a-144">**Drawtextexprivwrap** wird nicht nach Name exportiert oder in einer öffentlichen Header Datei deklariert.</span><span class="sxs-lookup"><span data-stu-id="b7e5a-144">**DrawTextExPrivWrap** is not exported by name or declared in a public header file.</span></span> <span data-ttu-id="b7e5a-145">Um es zu verwenden, müssen Sie [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) und Request Ordnungszahl 416 aus ComCtl32.dll verwenden, um einen Funktionszeiger zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="b7e5a-145">To use it, you must use [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) and request ordinal 416 from ComCtl32.dll to obtain a function pointer.</span></span>

<span data-ttu-id="b7e5a-146">Weitere Hinweise finden Sie unter [**drawtextex**](/windows/desktop/api/winuser/nf-winuser-drawtextexa).</span><span class="sxs-lookup"><span data-stu-id="b7e5a-146">For additional remarks, please see [**DrawTextEx**](/windows/desktop/api/winuser/nf-winuser-drawtextexa).</span></span>

## <a name="requirements"></a><span data-ttu-id="b7e5a-147">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b7e5a-147">Requirements</span></span>



| <span data-ttu-id="b7e5a-148">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b7e5a-148">Requirement</span></span> | <span data-ttu-id="b7e5a-149">Wert</span><span class="sxs-lookup"><span data-stu-id="b7e5a-149">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7e5a-150">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b7e5a-150">Minimum supported client</span></span><br/> | <span data-ttu-id="b7e5a-151">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b7e5a-151">Windows Vista \[desktop apps only\]</span></span><br/>                                                                 |
| <span data-ttu-id="b7e5a-152">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b7e5a-152">Minimum supported server</span></span><br/> | <span data-ttu-id="b7e5a-153">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b7e5a-153">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b7e5a-154">DLL</span><span class="sxs-lookup"><span data-stu-id="b7e5a-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b7e5a-155"><dt>Comctl32.dll (Version 6,0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="b7e5a-155"><dt>Comctl32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

