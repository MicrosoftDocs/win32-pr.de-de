---
description: Erstellt ein Mesh mit dem angegebenen Text unter Verwendung der Schriftart, die dem Gerätekontext zugeordnet ist.
ms.assetid: 1c8b0dc6-51b8-45bf-b4c0-b67e3d128097
title: D3DXCreateText-Funktion (D3dx9shape. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateText
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4f6202a534dde727e21b6513ad30077f2e3b3e52
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106366467"
---
# <a name="d3dxcreatetext-function"></a><span data-ttu-id="72e6b-103">D3DXCreateText-Funktion</span><span class="sxs-lookup"><span data-stu-id="72e6b-103">D3DXCreateText function</span></span>

<span data-ttu-id="72e6b-104">Erstellt ein Mesh mit dem angegebenen Text unter Verwendung der Schriftart, die dem Gerätekontext zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="72e6b-104">Creates a mesh containing the specified text, using the font associated with the device context.</span></span>

## <a name="syntax"></a><span data-ttu-id="72e6b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="72e6b-105">Syntax</span></span>


```C++
HRESULT D3DXCreateText(
  _In_  LPDIRECT3DDEVICE9   pDevice,
  _In_  HDC                 hDC,
  _In_  LPCTSTR             pText,
  _In_  FLOAT               Deviation,
  _In_  FLOAT               Extrusion,
  _Out_ LPD3DXMESH          *ppMesh,
  _Out_ LPD3DXBUFFER        *ppAdjacency,
  _Out_ LPGLYPHMETRICSFLOAT pGlyphMetrics
);
```



## <a name="parameters"></a><span data-ttu-id="72e6b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="72e6b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72e6b-107">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="72e6b-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72e6b-108">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="72e6b-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="72e6b-109">Zeiger auf das Gerät, das das Mesh erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="72e6b-109">Pointer to the device that created the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="72e6b-110">*hdc* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="72e6b-110">*hDC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72e6b-111">Typ: **hdc**</span><span class="sxs-lookup"><span data-stu-id="72e6b-111">Type: **HDC**</span></span>

<span data-ttu-id="72e6b-112">Gerätekontext, der die Schriftart für die Ausgabe enthält.</span><span class="sxs-lookup"><span data-stu-id="72e6b-112">Device context, containing the font for output.</span></span> <span data-ttu-id="72e6b-113">Die vom Gerätekontext ausgewählte Schriftart muss eine TrueType-Schriftart sein.</span><span class="sxs-lookup"><span data-stu-id="72e6b-113">The font selected by the device context must be a TrueType font.</span></span>

</dd> <dt>

<span data-ttu-id="72e6b-114">*ptext* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="72e6b-114">*pText* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72e6b-115">Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="72e6b-115">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="72e6b-116">Zeiger auf eine Zeichenfolge, die den zu Generier Text angibt.</span><span class="sxs-lookup"><span data-stu-id="72e6b-116">Pointer to a string that specifies the text to generate.</span></span> <span data-ttu-id="72e6b-117">Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="72e6b-117">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="72e6b-118">Andernfalls wird der String-Datentyp in LPCSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="72e6b-118">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="72e6b-119">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="72e6b-119">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="72e6b-120">*Abweichung* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="72e6b-120">*Deviation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72e6b-121">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="72e6b-121">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="72e6b-122">Maximale Zeichen Abweichung von TrueType-Schriftart umrissen.</span><span class="sxs-lookup"><span data-stu-id="72e6b-122">Maximum chordal deviation from TrueType font outlines.</span></span>

</dd> <dt>

<span data-ttu-id="72e6b-123">*Extrusion* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="72e6b-123">*Extrusion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72e6b-124">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="72e6b-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="72e6b-125">Betrag, um den Text in der negativen z-Richtung zu extrudieren.</span><span class="sxs-lookup"><span data-stu-id="72e6b-125">Amount to extrude text in the negative z-direction.</span></span>

</dd> <dt>

<span data-ttu-id="72e6b-126">*ppmesh* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="72e6b-126">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="72e6b-127">Typ: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="72e6b-127">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="72e6b-128">Zeiger auf das zurückgegebene Mesh.</span><span class="sxs-lookup"><span data-stu-id="72e6b-128">Pointer to the returned mesh.</span></span>

</dd> <dt>

<span data-ttu-id="72e6b-129">*ppency* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="72e6b-129">*ppAdjacency* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="72e6b-130">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="72e6b-130">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="72e6b-131">Zeiger auf einen Puffer, der Informationen zu Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="72e6b-131">Pointer to a buffer containing adjacency information.</span></span> <span data-ttu-id="72e6b-132">Kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="72e6b-132">May be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="72e6b-133">*pglyphmetrics* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="72e6b-133">*pGlyphMetrics* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="72e6b-134">Typ: **[ **lpglyphmetricsfloat**](/windows/win32/api/wingdi/ns-wingdi-glyphmetricsfloat)**</span><span class="sxs-lookup"><span data-stu-id="72e6b-134">Type: **[**LPGLYPHMETRICSFLOAT**](/windows/win32/api/wingdi/ns-wingdi-glyphmetricsfloat)**</span></span>

<span data-ttu-id="72e6b-135">Zeiger auf ein Array von [**glyphmetricsfloat**](/windows/win32/api/wingdi/ns-wingdi-glyphmetricsfloat) -Strukturen, die die Glyphe-Metrikdaten enthalten.</span><span class="sxs-lookup"><span data-stu-id="72e6b-135">Pointer to an array of [**GLYPHMETRICSFLOAT**](/windows/win32/api/wingdi/ns-wingdi-glyphmetricsfloat) structures that contain the glyph metric data.</span></span> <span data-ttu-id="72e6b-136">Jedes-Element enthält Informationen zur Position und Ausrichtung des entsprechenden Symbols in der Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="72e6b-136">Each element contains information about the position and orientation of the corresponding glyph in the string.</span></span> <span data-ttu-id="72e6b-137">Die Anzahl der Elemente im Array sollte gleich der Anzahl der Zeichen in der Zeichenfolge sein.</span><span class="sxs-lookup"><span data-stu-id="72e6b-137">The number of elements in the array should be equal to the number of characters in the string.</span></span> <span data-ttu-id="72e6b-138">Beachten Sie, dass der Ursprung in jeder Struktur nicht relativ zur gesamten Zeichenfolge ist, sondern relativ zu dieser Zeichen Zelle ist.</span><span class="sxs-lookup"><span data-stu-id="72e6b-138">Note that the origin in each structure is not relative to the entire string, but rather is relative to that character cell.</span></span> <span data-ttu-id="72e6b-139">Fügen Sie das Inkrement für jedes Symbol beim Durchlaufen der Zeichenfolge hinzu, um das gesamte umgebende Feld zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="72e6b-139">To compute the entire bounding box, add the increment for each glyph while traversing the string.</span></span> <span data-ttu-id="72e6b-140">Wenn Sie sich nicht mit den Symbolgrößen beschäftigen, legen Sie diesen Parameter auf **null** fest.</span><span class="sxs-lookup"><span data-stu-id="72e6b-140">If you are not concerned with the glyph sizes, set this parameter to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72e6b-141">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="72e6b-141">Return value</span></span>

<span data-ttu-id="72e6b-142">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="72e6b-142">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="72e6b-143">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="72e6b-143">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="72e6b-144">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData, E \_ oudefmemory.</span><span class="sxs-lookup"><span data-stu-id="72e6b-144">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="72e6b-145">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="72e6b-145">Remarks</span></span>

<span data-ttu-id="72e6b-146">Die Compilereinstellung bestimmt auch die Funktions Version.</span><span class="sxs-lookup"><span data-stu-id="72e6b-146">The compiler setting also determines the function version.</span></span> <span data-ttu-id="72e6b-147">Wenn Unicode definiert ist, wird der Funktions aufrufin D3DXCreateTextW aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="72e6b-147">If Unicode is defined, the function call resolves to D3DXCreateTextW.</span></span> <span data-ttu-id="72e6b-148">Andernfalls wird der Funktions Aufruhe in D3DXCreateTextA aufgelöst, da ANSI-Zeichen folgen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="72e6b-148">Otherwise, the function call resolves to D3DXCreateTextA because ANSI strings are being used.</span></span>

<span data-ttu-id="72e6b-149">Diese Funktion erstellt ein Mesh mit der D3DXMESH \_ Managed Creation-Option und [D3DFVF \_ XYZ \| D3DFVF \_ Normal](d3dfvf.md) flexibles Scheitelpunkt Format (FVF).</span><span class="sxs-lookup"><span data-stu-id="72e6b-149">This function creates a mesh with the D3DXMESH\_MANAGED creation option and [D3DFVF\_XYZ \| D3DFVF\_NORMAL](d3dfvf.md) flexible vertex format (FVF).</span></span>

## <a name="requirements"></a><span data-ttu-id="72e6b-150">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="72e6b-150">Requirements</span></span>



| <span data-ttu-id="72e6b-151">Anforderung</span><span class="sxs-lookup"><span data-stu-id="72e6b-151">Requirement</span></span> | <span data-ttu-id="72e6b-152">Wert</span><span class="sxs-lookup"><span data-stu-id="72e6b-152">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="72e6b-153">Header</span><span class="sxs-lookup"><span data-stu-id="72e6b-153">Header</span></span><br/>  | <dl> <span data-ttu-id="72e6b-154"><dt>D3dx9shape. h</dt></span><span class="sxs-lookup"><span data-stu-id="72e6b-154"><dt>D3dx9shape.h</dt></span></span> </dl> |
| <span data-ttu-id="72e6b-155">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="72e6b-155">Library</span></span><br/> | <dl> <span data-ttu-id="72e6b-156"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="72e6b-156"><dt>D3dx9.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="72e6b-157">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="72e6b-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72e6b-158">Formen Zeichnungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="72e6b-158">Shape Drawing Functions</span></span>](dx9-graphics-reference-d3dx-functions-shape.md)
</dt> </dl>

 

 
