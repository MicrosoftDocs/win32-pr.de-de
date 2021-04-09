---
title: Exttextoutwrap-Funktion
description: Zeichnet Text mithilfe der aktuell ausgewählten Schriftart, Hintergrundfarbe und Textfarbe. Optional können Sie Dimensionen angeben, die für das Abschneiden, die Deckkraft oder beides verwendet werden sollen. Diese Funktion umschließt einen exttextout-aufrufsausdruck.
ms.assetid: 0804c231-53f9-4de6-b703-0077cdcebcb5
keywords:
- Windows-Steuerelemente der exttextoutwrap-Funktion
topic_type:
- apiref
api_name:
- ExtTextOutWrap
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a173fedb7d8534dbd926a8a147e833435a7710b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102978"
---
# <a name="exttextoutwrap-function"></a><span data-ttu-id="710c3-106">Exttextoutwrap-Funktion</span><span class="sxs-lookup"><span data-stu-id="710c3-106">ExtTextOutWrap function</span></span>

<span data-ttu-id="710c3-107">\[**Exttextoutwrap** ist über Windows XP mit Service Pack 2 (SP2) verfügbar.</span><span class="sxs-lookup"><span data-stu-id="710c3-107">\[**ExtTextOutWrap** is available through Windows XP with Service Pack 2 (SP2).</span></span> <span data-ttu-id="710c3-108">Sie wird möglicherweise in nachfolgenden Versionen geändert oder ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="710c3-108">It might be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="710c3-109">Es wird empfohlen, stattdessen [**exttextout**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta) direkt zu verwenden.\]</span><span class="sxs-lookup"><span data-stu-id="710c3-109">It is recommended to use [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta) directly instead.\]</span></span>

<span data-ttu-id="710c3-110">Zeichnet Text mithilfe der aktuell ausgewählten Schriftart, Hintergrundfarbe und Textfarbe.</span><span class="sxs-lookup"><span data-stu-id="710c3-110">Draws text using the currently selected font, background color, and text color.</span></span> <span data-ttu-id="710c3-111">Optional können Sie Dimensionen angeben, die für das Abschneiden, die Deckkraft oder beides verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="710c3-111">You can optionally provide dimensions to be used for clipping, opacity, or both.</span></span> <span data-ttu-id="710c3-112">Diese Funktion umschließt einen [**exttextout**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta)-aufrufsausdruck.</span><span class="sxs-lookup"><span data-stu-id="710c3-112">This function wraps a call to [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta).</span></span>

## <a name="syntax"></a><span data-ttu-id="710c3-113">Syntax</span><span class="sxs-lookup"><span data-stu-id="710c3-113">Syntax</span></span>


```C++
BOOL ExtTextOutWrap(
  _In_       HDC     hdc,
  _In_       int     X,
  _In_       int     Y,
  _In_       UINT    uOptions,
  _In_ const RECT    *lprc,
  _In_       LPCTSTR lpString,
  _In_       UINT    cbCount,
  _In_ const INT     *lpDx
);
```



## <a name="parameters"></a><span data-ttu-id="710c3-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="710c3-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="710c3-115">*hdc* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="710c3-115">*hdc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="710c3-116">Typ: **[ **hdc**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="710c3-116">Type: **[**HDC**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="710c3-117">Ein Handle für den Gerätekontext.</span><span class="sxs-lookup"><span data-stu-id="710c3-117">A handle to the device context.</span></span>

</dd> <dt>

<span data-ttu-id="710c3-118">*X* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="710c3-118">*X* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="710c3-119">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="710c3-119">Type: **int**</span></span>

<span data-ttu-id="710c3-120">Die x-Koordinate (in logischen Koordinaten) des Bezugspunkts, der zum Positionieren der Zeichenfolge verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="710c3-120">The x-coordinate, in logical coordinates, of the reference point used to position the string.</span></span>

</dd> <dt>

<span data-ttu-id="710c3-121">*J* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="710c3-121">*Y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="710c3-122">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="710c3-122">Type: **int**</span></span>

<span data-ttu-id="710c3-123">Die y-Koordinate (in logischen Koordinaten) des Bezugspunkts, der zum Positionieren der Zeichenfolge verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="710c3-123">The y-coordinate, in logical coordinates, of the reference point used to position the string.</span></span>

</dd> <dt>

<span data-ttu-id="710c3-124">*uoptions* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="710c3-124">*uOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="710c3-125">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="710c3-125">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="710c3-126">Werte, die angeben, wie das Anwendungs definierte Rechteck verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="710c3-126">Values that specify how to use the application-defined rectangle.</span></span> <span data-ttu-id="710c3-127">Eine umfassende Liste der Optionen finden [**Sie unter exttextout**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta) .</span><span class="sxs-lookup"><span data-stu-id="710c3-127">See [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta) for a complete list of options.</span></span>

</dd> <dt>

<span data-ttu-id="710c3-128">*LPRC* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="710c3-128">*lprc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="710c3-129">Typ: \* Konstante *[**Rect**](/previous-versions//dd162897(v=vs.85)) \** _</span><span class="sxs-lookup"><span data-stu-id="710c3-129">Type: \**const [**RECT**](/previous-versions//dd162897(v=vs.85))\** _</span></span>

<span data-ttu-id="710c3-130">Ein Zeiger auf eine optionale [_ *Rect* \*](/previous-versions//dd162897(v=vs.85)) -Struktur, die die Dimensionen (in logischen Koordinaten) eines Rechtecks angibt, das für Clipping, Deckkraft oder beides verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="710c3-130">A pointer to an optional [_ *RECT*\*](/previous-versions//dd162897(v=vs.85)) structure that specifies the dimensions, in logical coordinates, of a rectangle that is used for clipping, opacity, or both.</span></span>

</dd> <dt>

<span data-ttu-id="710c3-131">*lpString* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="710c3-131">*lpString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="710c3-132">Typ: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="710c3-132">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="710c3-133">Ein Zeiger auf einen Puffer, der den Text enthält, der gezeichnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="710c3-133">A pointer to a buffer that contains the text to be drawn.</span></span> <span data-ttu-id="710c3-134">Die Zeichenfolge muss nicht mit 0 (null) beendet werden, da *cbcount* die Länge der Zeichenfolge angibt.</span><span class="sxs-lookup"><span data-stu-id="710c3-134">The string does not need to be zero-terminated, since *cbCount* specifies the length of the string.</span></span>

</dd> <dt>

<span data-ttu-id="710c3-135">*cbcount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="710c3-135">*cbCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="710c3-136">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="710c3-136">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="710c3-137">Die Länge der Zeichenfolge in Bytes, auf die von *lpString* verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="710c3-137">The length of the string, in bytes, pointed to by *lpString*.</span></span>

</dd> <dt>

<span data-ttu-id="710c3-138">*lpdx* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="710c3-138">*lpDx* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="710c3-139">Typ: \* Konstante *[**int**](/windows/desktop/WinProg/windows-data-types) \** _</span><span class="sxs-lookup"><span data-stu-id="710c3-139">Type: \**const [**INT**](/windows/desktop/WinProg/windows-data-types)\** _</span></span>

<span data-ttu-id="710c3-140">Ein Zeiger auf ein optionales Array von-Werten, die den Abstand zwischen den Ursprüngen der angrenzenden Zeichen Zellen angeben.</span><span class="sxs-lookup"><span data-stu-id="710c3-140">A pointer to an optional array of values that indicate the distance between origins of adjacent character cells.</span></span> <span data-ttu-id="710c3-141">Beispielsweise trennen _lpDx x \[ \] -Einheiten logische Einheiten die Ursprünge der Zeichen Zelle x und der Zeichen Zelle (x + 1).</span><span class="sxs-lookup"><span data-stu-id="710c3-141">For example, _lpDx\*\[x\] logical units separate the origins of character cell x and character cell (x + 1).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="710c3-142">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="710c3-142">Return value</span></span>

<span data-ttu-id="710c3-143">Typ: **[ **bool**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="710c3-143">Type: **[**BOOL**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="710c3-144">Gibt einen Wert ungleich 0 (null) zurück, wenn die Zeichenfolge erfolgreich gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="710c3-144">Returns a nonzero value if the string is drawn successfully.</span></span> <span data-ttu-id="710c3-145">Wenn die ANSI-Version von [**exttextout**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta) jedoch mit dem Eto- \_ Glyphe-Index aufgerufen wird \_ , gibt die Funktion **true** zurück, auch wenn die Funktion keine Aktion ausführt.</span><span class="sxs-lookup"><span data-stu-id="710c3-145">However, if the ANSI version of [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta) is called with ETO\_GLYPH\_INDEX, the function returns **TRUE** even though the function does nothing.</span></span>

<span data-ttu-id="710c3-146">Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.</span><span class="sxs-lookup"><span data-stu-id="710c3-146">If the function fails, the return value is zero.</span></span>

<span data-ttu-id="710c3-147">Um erweiterte Fehlerinformationen zu erhalten, rufen Sie [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) auf.</span><span class="sxs-lookup"><span data-stu-id="710c3-147">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="710c3-148">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="710c3-148">Remarks</span></span>

<span data-ttu-id="710c3-149">**Exttextoutwrap** wird nicht nach Name exportiert oder in einer öffentlichen Header Datei deklariert.</span><span class="sxs-lookup"><span data-stu-id="710c3-149">**ExtTextOutWrap** is not exported by name or declared in a public header file.</span></span> <span data-ttu-id="710c3-150">Um es zu verwenden, müssen Sie [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) und Request Ordnungszahl 417 aus ComCtl32.dll verwenden, um einen Funktionszeiger zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="710c3-150">To use it, you must use [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) and request ordinal 417 from ComCtl32.dll to obtain a function pointer.</span></span>

<span data-ttu-id="710c3-151">Weitere Hinweise finden Sie unter [**exttextout**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta).</span><span class="sxs-lookup"><span data-stu-id="710c3-151">For additional remarks, please see [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta).</span></span>

## <a name="requirements"></a><span data-ttu-id="710c3-152">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="710c3-152">Requirements</span></span>



| <span data-ttu-id="710c3-153">Anforderung</span><span class="sxs-lookup"><span data-stu-id="710c3-153">Requirement</span></span> | <span data-ttu-id="710c3-154">Wert</span><span class="sxs-lookup"><span data-stu-id="710c3-154">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="710c3-155">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="710c3-155">Minimum supported client</span></span><br/> | <span data-ttu-id="710c3-156">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="710c3-156">Windows Vista \[desktop apps only\]</span></span><br/>                                                                 |
| <span data-ttu-id="710c3-157">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="710c3-157">Minimum supported server</span></span><br/> | <span data-ttu-id="710c3-158">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="710c3-158">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="710c3-159">DLL</span><span class="sxs-lookup"><span data-stu-id="710c3-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="710c3-160"><dt>Comctl32.dll (Version 6,0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="710c3-160"><dt>Comctl32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

