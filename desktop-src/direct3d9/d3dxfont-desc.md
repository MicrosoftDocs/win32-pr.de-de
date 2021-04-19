---
description: Definiert die Attribute einer Schriftart.
ms.assetid: 6f456f26-3410-4205-a013-e3c12bf0feb1
title: D3DXFONT_DESC-Struktur (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFONT_DESC
api_type:
- HeaderDef
api_location:
- d3dx9core.h
ms.openlocfilehash: d7c142787e4e4fac5be53763a3c19fd86a27efd9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106351949"
---
# <a name="d3dxfont_desc-structure"></a><span data-ttu-id="49d06-103">D3DXFONT- \_ Struktur</span><span class="sxs-lookup"><span data-stu-id="49d06-103">D3DXFONT\_DESC structure</span></span>

<span data-ttu-id="49d06-104">Definiert die Attribute einer Schriftart.</span><span class="sxs-lookup"><span data-stu-id="49d06-104">Defines the attributes of a font.</span></span>

## <a name="syntax"></a><span data-ttu-id="49d06-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="49d06-105">Syntax</span></span>


```C++
typedef struct D3DXFONT_DESC {
  INT   Height;
  UINT  Width;
  UINT  Weight;
  UINT  MipLevels;
  BOOL  Italic;
  BYTE  CharSet;
  BYTE  OutputPrecision;
  BYTE  Quality;
  BYTE  PitchAndFamily;
  TCHAR FaceName;
} D3DXFONT_DESC, *LPD3DXFONT_DESC;
```



## <a name="members"></a><span data-ttu-id="49d06-106">Member</span><span class="sxs-lookup"><span data-stu-id="49d06-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="49d06-107">**Height**</span><span class="sxs-lookup"><span data-stu-id="49d06-107">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="49d06-108">Typ: **[ **int**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="49d06-108">Type: **[**INT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="49d06-109">Höhe (in logischen Einheiten) der Zeichen Zelle oder des Zeichens der Schriftart.</span><span class="sxs-lookup"><span data-stu-id="49d06-109">Height, in logical units, of the font's character cell or character.</span></span>

</dd> <dt>

<span data-ttu-id="49d06-110">**Width**</span><span class="sxs-lookup"><span data-stu-id="49d06-110">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="49d06-111">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="49d06-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="49d06-112">Breite (in logischen Einheiten) der Zeichen in der Schriftart.</span><span class="sxs-lookup"><span data-stu-id="49d06-112">Width, in logical units, of characters in the font.</span></span>

</dd> <dt>

<span data-ttu-id="49d06-113">**Weight**</span><span class="sxs-lookup"><span data-stu-id="49d06-113">**Weight**</span></span>
</dt> <dd>

<span data-ttu-id="49d06-114">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="49d06-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="49d06-115">Gewichtung der Schriftart im Bereich von 0 bis 1000.</span><span class="sxs-lookup"><span data-stu-id="49d06-115">Weight of the font in the range from 0 through 1000.</span></span>

</dd> <dt>

<span data-ttu-id="49d06-116">**MipLevels**</span><span class="sxs-lookup"><span data-stu-id="49d06-116">**MipLevels**</span></span>
</dt> <dd>

<span data-ttu-id="49d06-117">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="49d06-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="49d06-118">Anzahl der angeforderten Mip-Ebenen.</span><span class="sxs-lookup"><span data-stu-id="49d06-118">Number of mip levels requested.</span></span> <span data-ttu-id="49d06-119">Wenn dieser Wert 0 (null) oder D3DX \_ Default ist, wird eine komplette MipMap-Kette erstellt.</span><span class="sxs-lookup"><span data-stu-id="49d06-119">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span> <span data-ttu-id="49d06-120">Wenn der Wert 1 ist, wird der Textur Bereich identisch mit dem Bildschirmbereich zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="49d06-120">If the value is 1, the texture space is mapped identically to the screen space.</span></span>

</dd> <dt>

<span data-ttu-id="49d06-121">**Kursiv**</span><span class="sxs-lookup"><span data-stu-id="49d06-121">**Italic**</span></span>
</dt> <dd>

<span data-ttu-id="49d06-122">Typ: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="49d06-122">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="49d06-123">Legen Sie für eine kursiv Schrift auf **true** fest.</span><span class="sxs-lookup"><span data-stu-id="49d06-123">Set to **TRUE** for an Italic font.</span></span>

</dd> <dt>

<span data-ttu-id="49d06-124">**CharSet**</span><span class="sxs-lookup"><span data-stu-id="49d06-124">**CharSet**</span></span>
</dt> <dd>

<span data-ttu-id="49d06-125">Type: **[ **Byte**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="49d06-125">Type: **[**BYTE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="49d06-126">Zeichensatz.</span><span class="sxs-lookup"><span data-stu-id="49d06-126">Character set.</span></span>

</dd> <dt>

<span data-ttu-id="49d06-127">**Outputprecision**</span><span class="sxs-lookup"><span data-stu-id="49d06-127">**OutputPrecision**</span></span>
</dt> <dd>

<span data-ttu-id="49d06-128">Type: **[ **Byte**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="49d06-128">Type: **[**BYTE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="49d06-129">Ausgabe Genauigkeit.</span><span class="sxs-lookup"><span data-stu-id="49d06-129">Output precision.</span></span> <span data-ttu-id="49d06-130">Die Ausgabe Genauigkeit definiert, wie genau die Ausgabe der angeforderten Schrift Höhe, der Breite, der Zeichen Ausrichtung, dem Escapezeichen, der Tonhöhe und dem Schrifttyp entsprechen muss.</span><span class="sxs-lookup"><span data-stu-id="49d06-130">The output precision defines how closely the output must match the requested font height, width, character orientation, escapement, pitch, and font type.</span></span>

</dd> <dt>

<span data-ttu-id="49d06-131">**Qualität**</span><span class="sxs-lookup"><span data-stu-id="49d06-131">**Quality**</span></span>
</dt> <dd>

<span data-ttu-id="49d06-132">Type: **[ **Byte**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="49d06-132">Type: **[**BYTE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="49d06-133">Ausgabequalität.</span><span class="sxs-lookup"><span data-stu-id="49d06-133">Output quality.</span></span>

</dd> <dt>

<span data-ttu-id="49d06-134">**PitchAndFamily**</span><span class="sxs-lookup"><span data-stu-id="49d06-134">**PitchAndFamily**</span></span>
</dt> <dd>

<span data-ttu-id="49d06-135">Type: **[ **Byte**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="49d06-135">Type: **[**BYTE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="49d06-136">Tonhöhe und Familie der Schriftart.</span><span class="sxs-lookup"><span data-stu-id="49d06-136">Pitch and family of the font.</span></span>

</dd> <dt>

<span data-ttu-id="49d06-137">**Fakename**</span><span class="sxs-lookup"><span data-stu-id="49d06-137">**FaceName**</span></span>
</dt> <dd>

<span data-ttu-id="49d06-138">Typ: **TCHAR**</span><span class="sxs-lookup"><span data-stu-id="49d06-138">Type: **TCHAR**</span></span>

</dd> <dd>

<span data-ttu-id="49d06-139">Eine mit NULL endenden Zeichenfolge oder Zeichen, die den Schriftart Namen der Schriftart angibt.</span><span class="sxs-lookup"><span data-stu-id="49d06-139">A null-terminated string or characters that specifies the typeface name of the font.</span></span> <span data-ttu-id="49d06-140">Die Länge der Zeichenfolge darf 32 Zeichen nicht überschreiten, einschließlich des abschließenden NULL-Zeichens.</span><span class="sxs-lookup"><span data-stu-id="49d06-140">The length of the string must not exceed 32 characters, including the terminating null character.</span></span> <span data-ttu-id="49d06-141">Wenn "fakename" eine leere Zeichenfolge ist, wird die erste Schriftart verwendet, die mit den anderen angegebenen Attributen übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="49d06-141">If FaceName is an empty string, the first font that matches the other specified attributes will be used.</span></span> <span data-ttu-id="49d06-142">Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp "TCHAR" in "WCHAR;" aufgelöst. Andernfalls wird der-Datentyp in char aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="49d06-142">If the compiler settings require Unicode, the data type TCHAR resolves to WCHAR; otherwise, the data type resolves to CHAR.</span></span> <span data-ttu-id="49d06-143">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="49d06-143">See Remarks.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="49d06-144">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="49d06-144">Remarks</span></span>

<span data-ttu-id="49d06-145">Die Compilereinstellung bestimmt auch den Strukturtyp.</span><span class="sxs-lookup"><span data-stu-id="49d06-145">The compiler setting also determines the structure type.</span></span> <span data-ttu-id="49d06-146">Wenn Unicode definiert ist, wird der D3DXFONT \_ DESC-Strukturtyp zu einem D3DXFONT- \_ descw aufgelöst; andernfalls wird der Strukturtyp in einen D3DXFONT \_ DeScA aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="49d06-146">If Unicode is defined, the D3DXFONT\_DESC structure type resolves to a D3DXFONT\_DESCW; otherwise the structure type resolves to a D3DXFONT\_DESCA.</span></span>

<span data-ttu-id="49d06-147">Mögliche Werte der obigen Member werden in der GDI- [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) -Struktur angegeben.</span><span class="sxs-lookup"><span data-stu-id="49d06-147">Possible values of the above members are given in the GDI [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="49d06-148">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="49d06-148">Requirements</span></span>



| <span data-ttu-id="49d06-149">Anforderung</span><span class="sxs-lookup"><span data-stu-id="49d06-149">Requirement</span></span> | <span data-ttu-id="49d06-150">Wert</span><span class="sxs-lookup"><span data-stu-id="49d06-150">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="49d06-151">Header</span><span class="sxs-lookup"><span data-stu-id="49d06-151">Header</span></span><br/> | <dl> <span data-ttu-id="49d06-152"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="49d06-152"><dt>D3dx9core.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49d06-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="49d06-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49d06-154">D3DX-Strukturen</span><span class="sxs-lookup"><span data-stu-id="49d06-154">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="49d06-155">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="49d06-155">**GetDesc**</span></span>](id3dxfont--getdesc.md)
</dt> </dl>

 

 
