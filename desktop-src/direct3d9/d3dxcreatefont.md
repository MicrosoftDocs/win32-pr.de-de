---
description: Erstellt ein Schriftart Objekt für ein Gerät und eine Schriftart.
ms.assetid: 3e65dfdc-9608-420c-9672-c38289d13ab1
title: D3DXCreateFont-Funktion (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateFont
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 488a400928ecc270612a307fbede971e02b43b25
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762192"
---
# <a name="d3dxcreatefont-function"></a><span data-ttu-id="9be48-103">D3DXCreateFont-Funktion</span><span class="sxs-lookup"><span data-stu-id="9be48-103">D3DXCreateFont function</span></span>

<span data-ttu-id="9be48-104">Erstellt ein Schriftart Objekt für ein Gerät und eine Schriftart.</span><span class="sxs-lookup"><span data-stu-id="9be48-104">Creates a font object for a device and font.</span></span>

## <a name="syntax"></a><span data-ttu-id="9be48-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9be48-105">Syntax</span></span>


```C++
HRESULT D3DXCreateFont(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _In_  INT               Height,
  _In_  UINT              Width,
  _In_  UINT              Weight,
  _In_  UINT              MipLevels,
  _In_  BOOL              Italic,
  _In_  DWORD             CharSet,
  _In_  DWORD             OutputPrecision,
  _In_  DWORD             Quality,
  _In_  DWORD             PitchAndFamily,
  _In_  LPCTSTR           pFacename,
  _Out_ LPD3DXFONT        *ppFont
);
```



## <a name="parameters"></a><span data-ttu-id="9be48-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9be48-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9be48-107">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9be48-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9be48-108">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="9be48-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="9be48-109">Zeiger auf eine [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle, das Gerät, das dem Schriftart Objekt zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9be48-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, the device to be associated with the font object.</span></span>

</dd> <dt>

<span data-ttu-id="9be48-110">*Höhe* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9be48-110">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9be48-111">Typ: **[ **int**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9be48-111">Type: **[**INT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9be48-112">Die Höhe der Zeichen in logischen Einheiten.</span><span class="sxs-lookup"><span data-stu-id="9be48-112">The height of the characters in logical units.</span></span>

</dd> <dt>

<span data-ttu-id="9be48-113">*Breite* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9be48-113">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9be48-114">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9be48-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9be48-115">Die Breite der Zeichen in logischen Einheiten.</span><span class="sxs-lookup"><span data-stu-id="9be48-115">The width of the characters in logical units.</span></span>

</dd> <dt>

<span data-ttu-id="9be48-116">*Gewichtung* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9be48-116">*Weight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9be48-117">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9be48-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9be48-118">Schrift Breite.</span><span class="sxs-lookup"><span data-stu-id="9be48-118">Typeface weight.</span></span> <span data-ttu-id="9be48-119">Ein Beispiel ist "Bold".</span><span class="sxs-lookup"><span data-stu-id="9be48-119">One example is bold.</span></span>

</dd> <dt>

<span data-ttu-id="9be48-120">*Miplevels* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9be48-120">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9be48-121">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9be48-121">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9be48-122">Die Anzahl von MipMap-Ebenen.</span><span class="sxs-lookup"><span data-stu-id="9be48-122">The number of mipmap levels.</span></span>

</dd> <dt>

<span data-ttu-id="9be48-123">*Kursiv* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9be48-123">*Italic* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9be48-124">Typ: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9be48-124">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9be48-125">True für kursiv Schrift, andernfalls false.</span><span class="sxs-lookup"><span data-stu-id="9be48-125">True for italic font, false otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="9be48-126">Zeichen *Satz* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9be48-126">*CharSet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9be48-127">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9be48-127">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9be48-128">Der Zeichensatz der Schriftart.</span><span class="sxs-lookup"><span data-stu-id="9be48-128">The character set of the font.</span></span>

</dd> <dt>

<span data-ttu-id="9be48-129">*Outputprecision* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9be48-129">*OutputPrecision* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9be48-130">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9be48-130">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9be48-131">Gibt an, wie Windows versuchen soll, die gewünschten Schriftgrößen und Merkmale mit tatsächlichen Schriftarten abzugleichen.</span><span class="sxs-lookup"><span data-stu-id="9be48-131">Specifies how Windows should attempt to match the desired font sizes and characteristics with actual fonts.</span></span> <span data-ttu-id="9be48-132">Verwenden \_ \_ \_ Sie nur die Precis-präcis, um sicherzustellen, dass Sie immer eine TrueType-Schriftart erhalten.</span><span class="sxs-lookup"><span data-stu-id="9be48-132">Use OUT\_TT\_ONLY\_PRECIS for instance, to ensure that you always get a TrueType font.</span></span>

</dd> <dt>

<span data-ttu-id="9be48-133">*Qualität* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9be48-133">*Quality* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9be48-134">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9be48-134">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9be48-135">Gibt an, wie Windows der gewünschten Schriftart mit einer echten Schriftart entsprechen soll.</span><span class="sxs-lookup"><span data-stu-id="9be48-135">Specifies how Windows should match the desired font with a real font.</span></span> <span data-ttu-id="9be48-136">Sie gilt nur für Raster Schriftarten und sollte sich nicht auf TrueType-Schriftarten auswirken.</span><span class="sxs-lookup"><span data-stu-id="9be48-136">It applies to raster fonts only and should not affect TrueType fonts.</span></span>

</dd> <dt>

<span data-ttu-id="9be48-137">*PitchAndFamily* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9be48-137">*PitchAndFamily* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9be48-138">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9be48-138">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9be48-139">Der-und der-Familien Index.</span><span class="sxs-lookup"><span data-stu-id="9be48-139">Pitch and family index.</span></span>

</dd> <dt>

<span data-ttu-id="9be48-140">*pfakename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9be48-140">*pFacename* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9be48-141">Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9be48-141">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9be48-142">Zeichenfolge, die den Namen der Schriftart enthält.</span><span class="sxs-lookup"><span data-stu-id="9be48-142">String containing the typeface name.</span></span> <span data-ttu-id="9be48-143">Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="9be48-143">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="9be48-144">Andernfalls wird der String-Datentyp in LPCSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="9be48-144">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="9be48-145">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="9be48-145">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="9be48-146">*ppfont* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="9be48-146">*ppFont* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9be48-147">Typ: **[ **LPD3DXFONT**](id3dxfont.md)\***</span><span class="sxs-lookup"><span data-stu-id="9be48-147">Type: **[**LPD3DXFONT**](id3dxfont.md)\***</span></span>

<span data-ttu-id="9be48-148">Gibt einen Zeiger auf eine [**ID3DXFont**](id3dxfont.md) -Schnittstelle zurück, die das erstellte Schriftart Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="9be48-148">Returns a pointer to an [**ID3DXFont**](id3dxfont.md) interface, representing the created font object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9be48-149">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9be48-149">Return value</span></span>

<span data-ttu-id="9be48-150">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9be48-150">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9be48-151">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="9be48-151">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="9be48-152">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData, E \_ oudefmemory.</span><span class="sxs-lookup"><span data-stu-id="9be48-152">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="9be48-153">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9be48-153">Remarks</span></span>

<span data-ttu-id="9be48-154">Die Erstellung eines ID3DXFont-Objekts erfordert, dass das Gerät 32-Bit-Farbe unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9be48-154">The creation of an ID3DXFont object requires that the device supports 32-bit color.</span></span>

<span data-ttu-id="9be48-155">Die Compilereinstellung bestimmt auch die Funktions Version.</span><span class="sxs-lookup"><span data-stu-id="9be48-155">The compiler setting also determines the function version.</span></span> <span data-ttu-id="9be48-156">Wenn Unicode definiert ist, wird der Funktions aufrufin D3DXCreateFontW aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="9be48-156">If Unicode is defined, the function call resolves to D3DXCreateFontW.</span></span> <span data-ttu-id="9be48-157">Andernfalls wird der Funktions Aufruhe in D3DXCreateFontA aufgelöst, da ANSI-Zeichen folgen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9be48-157">Otherwise, the function call resolves to D3DXCreateFontA because ANSI strings are being used.</span></span>

<span data-ttu-id="9be48-158">Weitere Informationen zu Schriftart Parametern finden Sie in [der logischen Schriftart](../gdi/creating-a-logical-font.md).</span><span class="sxs-lookup"><span data-stu-id="9be48-158">If you want more information about font parameters, see [The Logical Font](../gdi/creating-a-logical-font.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9be48-159">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9be48-159">Requirements</span></span>



| <span data-ttu-id="9be48-160">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9be48-160">Requirement</span></span> | <span data-ttu-id="9be48-161">Wert</span><span class="sxs-lookup"><span data-stu-id="9be48-161">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9be48-162">Header</span><span class="sxs-lookup"><span data-stu-id="9be48-162">Header</span></span><br/>  | <dl> <span data-ttu-id="9be48-163"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="9be48-163"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="9be48-164">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9be48-164">Library</span></span><br/> | <dl> <span data-ttu-id="9be48-165"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9be48-165"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9be48-166">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9be48-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9be48-167">Universell Funktionen</span><span class="sxs-lookup"><span data-stu-id="9be48-167">General Purpose Functions</span></span>](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
