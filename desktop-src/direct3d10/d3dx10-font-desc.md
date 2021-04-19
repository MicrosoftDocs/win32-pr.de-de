---
description: Definiert Schriftart Attribute.
ms.assetid: 66e8a320-2b83-4766-a9a7-5571ee6c9f2a
title: D3DX10_FONT_DESC-Struktur (d3dx10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_FONT_DESC
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: 0b358c57e6410827177e76e3da30b2f5f9896ee2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106373497"
---
# <a name="d3dx10_font_desc-structure"></a><span data-ttu-id="73119-103">D3dx10 \_ Font- \_ Struktur Struktur</span><span class="sxs-lookup"><span data-stu-id="73119-103">D3DX10\_FONT\_DESC structure</span></span>

<span data-ttu-id="73119-104">Definiert Schriftart Attribute.</span><span class="sxs-lookup"><span data-stu-id="73119-104">Defines font attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="73119-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="73119-105">Syntax</span></span>


```C++
typedef struct D3DX10_FONT_DESC {
  INT   Height;
  UINT  Width;
  UINT  Weight;
  UINT  MipLevels;
  BOOL  Italic;
  BYTE  CharSet;
  BYTE  OutputPrecision;
  BYTE  Quality;
  BYTE  PitchAndFamily;
  TCHAR FaceName[LF_FACESIZE];
} D3DX10_FONT_DESC, *LPD3DX10_FONT_DESC;
```



## <a name="members"></a><span data-ttu-id="73119-106">Member</span><span class="sxs-lookup"><span data-stu-id="73119-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="73119-107">**Height**</span><span class="sxs-lookup"><span data-stu-id="73119-107">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="73119-108">Typ: **[ **int**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="73119-108">Type: **[**INT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="73119-109">Höhe (in logischen Einheiten) der Zeichen Zelle oder des Zeichens der Schriftart.</span><span class="sxs-lookup"><span data-stu-id="73119-109">Height, in logical units, of the font's character cell or character.</span></span>

</dd> <dt>

<span data-ttu-id="73119-110">**Width**</span><span class="sxs-lookup"><span data-stu-id="73119-110">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="73119-111">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="73119-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="73119-112">Breite (in logischen Einheiten) der Zeichen in der Schriftart.</span><span class="sxs-lookup"><span data-stu-id="73119-112">Width, in logical units, of characters in the font.</span></span>

</dd> <dt>

<span data-ttu-id="73119-113">**Weight**</span><span class="sxs-lookup"><span data-stu-id="73119-113">**Weight**</span></span>
</dt> <dd>

<span data-ttu-id="73119-114">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="73119-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="73119-115">Gewichtung der Schriftart im Bereich von 0 bis 1000.</span><span class="sxs-lookup"><span data-stu-id="73119-115">Weight of the font in the range from 0 through 1000.</span></span>

</dd> <dt>

<span data-ttu-id="73119-116">**MipLevels**</span><span class="sxs-lookup"><span data-stu-id="73119-116">**MipLevels**</span></span>
</dt> <dd>

<span data-ttu-id="73119-117">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="73119-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="73119-118">Anzahl der angeforderten MipMap-Ebenen.</span><span class="sxs-lookup"><span data-stu-id="73119-118">Number of mipmap levels requested.</span></span> <span data-ttu-id="73119-119">Wenn dieser Wert 0 (null) oder D3DX \_ Default ist, wird eine komplette MipMap-Kette erstellt.</span><span class="sxs-lookup"><span data-stu-id="73119-119">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span> <span data-ttu-id="73119-120">Wenn der Wert 1 ist, wird der Textur Bereich identisch mit dem Bildschirmbereich zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="73119-120">If the value is 1, the texture space is mapped identically to the screen space.</span></span>

</dd> <dt>

<span data-ttu-id="73119-121">**Kursiv**</span><span class="sxs-lookup"><span data-stu-id="73119-121">**Italic**</span></span>
</dt> <dd>

<span data-ttu-id="73119-122">Typ: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="73119-122">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="73119-123">Legen Sie für eine kursiv Schrift auf **true** fest.</span><span class="sxs-lookup"><span data-stu-id="73119-123">Set to **TRUE** for an Italic font.</span></span>

</dd> <dt>

<span data-ttu-id="73119-124">**CharSet**</span><span class="sxs-lookup"><span data-stu-id="73119-124">**CharSet**</span></span>
</dt> <dd>

<span data-ttu-id="73119-125">Type: **[ **Byte**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="73119-125">Type: **[**BYTE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="73119-126">Zeichensatz.</span><span class="sxs-lookup"><span data-stu-id="73119-126">Character set.</span></span>

</dd> <dt>

<span data-ttu-id="73119-127">**Outputprecision**</span><span class="sxs-lookup"><span data-stu-id="73119-127">**OutputPrecision**</span></span>
</dt> <dd>

<span data-ttu-id="73119-128">Type: **[ **Byte**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="73119-128">Type: **[**BYTE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="73119-129">Ausgabe Genauigkeit.</span><span class="sxs-lookup"><span data-stu-id="73119-129">Output precision.</span></span> <span data-ttu-id="73119-130">Die Ausgabe Genauigkeit definiert, wie genau die Ausgabe der angeforderten Schrift Höhe, der Breite, der Zeichen Ausrichtung, dem Escapezeichen, der Tonhöhe und dem Schrifttyp entsprechen muss.</span><span class="sxs-lookup"><span data-stu-id="73119-130">The output precision defines how closely the output must match the requested font height, width, character orientation, escapement, pitch, and font type.</span></span>

</dd> <dt>

<span data-ttu-id="73119-131">**Qualität**</span><span class="sxs-lookup"><span data-stu-id="73119-131">**Quality**</span></span>
</dt> <dd>

<span data-ttu-id="73119-132">Type: **[ **Byte**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="73119-132">Type: **[**BYTE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="73119-133">Ausgabequalität.</span><span class="sxs-lookup"><span data-stu-id="73119-133">Output quality.</span></span>

</dd> <dt>

<span data-ttu-id="73119-134">**PitchAndFamily**</span><span class="sxs-lookup"><span data-stu-id="73119-134">**PitchAndFamily**</span></span>
</dt> <dd>

<span data-ttu-id="73119-135">Type: **[ **Byte**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="73119-135">Type: **[**BYTE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="73119-136">Tonhöhe und Familie der Schriftart.</span><span class="sxs-lookup"><span data-stu-id="73119-136">Pitch and family of the font.</span></span>

</dd> <dt>

<span data-ttu-id="73119-137">**Fakename \[ LF- \_ fakesisieren\]**</span><span class="sxs-lookup"><span data-stu-id="73119-137">**FaceName\[LF\_FACESIZE\]**</span></span>
</dt> <dd>

<span data-ttu-id="73119-138">Typ: **TCHAR**</span><span class="sxs-lookup"><span data-stu-id="73119-138">Type: **TCHAR**</span></span>

</dd> <dd>

<span data-ttu-id="73119-139">Eine NULL-terminierte Zeichenfolge, die den Schriftart Namen der Schriftart angibt.</span><span class="sxs-lookup"><span data-stu-id="73119-139">A NULL-terminated string that specifies the typeface name of the font.</span></span> <span data-ttu-id="73119-140">Die Länge der Zeichenfolge darf 32 Zeichen nicht überschreiten, einschließlich des abschließenden **null** -Zeichens.</span><span class="sxs-lookup"><span data-stu-id="73119-140">The length of the string must not exceed 32 characters, including the terminating **NULL** character.</span></span> <span data-ttu-id="73119-141">Wenn "fakename" eine leere Zeichenfolge ist, wird die erste Schriftart verwendet, die mit den anderen angegebenen Attributen übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="73119-141">If FaceName is an empty string, the first font that matches the other specified attributes will be used.</span></span> <span data-ttu-id="73119-142">Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp "TCHAR" in "WCHAR;" aufgelöst. Andernfalls wird der-Datentyp in char aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="73119-142">If the compiler settings require Unicode, the data type TCHAR resolves to WCHAR; otherwise, the data type resolves to CHAR.</span></span> <span data-ttu-id="73119-143">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="73119-143">See Remarks.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="73119-144">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="73119-144">Remarks</span></span>

<span data-ttu-id="73119-145">Die Compilereinstellung bestimmt auch den Strukturtyp.</span><span class="sxs-lookup"><span data-stu-id="73119-145">The compiler setting also determines the structure type.</span></span> <span data-ttu-id="73119-146">Wenn Unicode definiert ist, wird der d3dx10 \_ Font \_ DESC-Strukturtyp in einen d3dx10 \_ Schriftart- \_ descw aufgelöst; andernfalls wird der Strukturtyp in eine d3dx10- \_ Schriftart \_ DeScA aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="73119-146">If Unicode is defined, the D3DX10\_FONT\_DESC structure type resolves to a D3DX10\_FONT\_DESCW; otherwise the structure type resolves to a D3DX10\_FONT\_DESCA.</span></span>

<span data-ttu-id="73119-147">Mögliche Werte der obigen Member werden in der GDI- [LOGFONT](/previous-versions//ms533931(v=vs.85)) -Struktur angegeben.</span><span class="sxs-lookup"><span data-stu-id="73119-147">Possible values of the above members are given in the GDI [LOGFONT](/previous-versions//ms533931(v=vs.85)) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="73119-148">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="73119-148">Requirements</span></span>



| <span data-ttu-id="73119-149">Anforderung</span><span class="sxs-lookup"><span data-stu-id="73119-149">Requirement</span></span> | <span data-ttu-id="73119-150">Wert</span><span class="sxs-lookup"><span data-stu-id="73119-150">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="73119-151">Header</span><span class="sxs-lookup"><span data-stu-id="73119-151">Header</span></span><br/> | <dl> <span data-ttu-id="73119-152"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="73119-152"><dt>D3DX10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73119-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="73119-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73119-154">D3DX-Strukturen</span><span class="sxs-lookup"><span data-stu-id="73119-154">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
