---
description: Laden Sie formatierten Text in den Videospeicher, um die Effizienz beim Rendern auf das Gerät zu verbessern. Diese Methode unterstützt ANSI-und Unicode-Zeichen folgen.
ms.assetid: 0e5380fc-7a01-4e09-9c18-22087be56780
title: ID3DX10Font::P reloadtext-Methode (d3dx10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.PreloadText
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: c7294fb7e86b3532960a34a15e1118dc33f748f2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219533"
---
# <a name="id3dx10fontpreloadtext-method"></a><span data-ttu-id="93d9c-104">ID3DX10Font::P reloadtext-Methode</span><span class="sxs-lookup"><span data-stu-id="93d9c-104">ID3DX10Font::PreloadText method</span></span>

<span data-ttu-id="93d9c-105">Laden Sie formatierten Text in den Videospeicher, um die Effizienz beim Rendern auf das Gerät zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="93d9c-105">Load formatted text into video memory to improve the efficiency of rendering to the device.</span></span> <span data-ttu-id="93d9c-106">Diese Methode unterstützt ANSI-und Unicode-Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="93d9c-106">This method supports ANSI and Unicode strings.</span></span>

## <a name="syntax"></a><span data-ttu-id="93d9c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="93d9c-107">Syntax</span></span>


```C++
HRESULT PreloadText(
  [in] LPCSTR pString,
  [in] INT    Count
);
```



## <a name="parameters"></a><span data-ttu-id="93d9c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="93d9c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93d9c-109">*pstring* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="93d9c-109">*pString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93d9c-110">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="93d9c-110">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="93d9c-111">Zeiger auf eine Zeichenfolge, die in den Videospeicher geladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="93d9c-111">Pointer to a string of characters to be loaded into video memory.</span></span> <span data-ttu-id="93d9c-112">Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR aufgelöst. Andernfalls wird der Datentyp in LPCSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="93d9c-112">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR; otherwise, the data type resolves to LPCSTR.</span></span> <span data-ttu-id="93d9c-113">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="93d9c-113">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="93d9c-114">*Anzahl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="93d9c-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93d9c-115">Typ: **[ **int**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="93d9c-115">Type: **[**INT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="93d9c-116">Anzahl der Zeichen in der Text Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="93d9c-116">Number of characters in the text string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93d9c-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="93d9c-117">Return value</span></span>

<span data-ttu-id="93d9c-118">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="93d9c-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="93d9c-119">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="93d9c-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="93d9c-120">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData.</span><span class="sxs-lookup"><span data-stu-id="93d9c-120">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="93d9c-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="93d9c-121">Remarks</span></span>

<span data-ttu-id="93d9c-122">Die Compilereinstellung bestimmt auch die Funktions Version.</span><span class="sxs-lookup"><span data-stu-id="93d9c-122">The compiler setting also determines the function version.</span></span> <span data-ttu-id="93d9c-123">Wenn Unicode definiert ist, wird der Funktions aufzurufen in preloadtextw aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="93d9c-123">If Unicode is defined, the function call resolves to PreloadTextW.</span></span> <span data-ttu-id="93d9c-124">Andernfalls wird der Funktions Aufrufwert in preloadtexta aufgelöst, da ANSI-Zeichen folgen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="93d9c-124">Otherwise, the function call resolves to PreloadTextA because ANSI strings are being used.</span></span>

<span data-ttu-id="93d9c-125">Diese Methode generiert Texturen, die Symbole enthalten, die den Eingabetext darstellen.</span><span class="sxs-lookup"><span data-stu-id="93d9c-125">This method generates textures that contain glyphs that represent the input text.</span></span> <span data-ttu-id="93d9c-126">Die Symbole werden als eine Reihe von Dreiecken gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="93d9c-126">The glyphs are drawn as a series of triangles.</span></span>

<span data-ttu-id="93d9c-127">Der Text wird nicht auf dem Gerät gerendert. ID3DX10Font::D rawtext muss nach wie vor aufgerufen werden, um den Text zu erzeugen.</span><span class="sxs-lookup"><span data-stu-id="93d9c-127">Text will not be rendered to the device; ID3DX10Font::DrawText must still be called to render the text.</span></span> <span data-ttu-id="93d9c-128">Durch das vorab Laden von Text in den Videospeicher verwendet ID3DX10Font::D rawtext erheblich weniger CPU-Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="93d9c-128">However, by preloading text into video memory, ID3DX10Font::DrawText will use substantially fewer CPU resources.</span></span>

<span data-ttu-id="93d9c-129">Diese Methode konvertiert Zeichen intern mithilfe der GDI-Funktion [getcharakteriplacement](/previous-versions//ms534004(v=vs.85))in Glyphen.</span><span class="sxs-lookup"><span data-stu-id="93d9c-129">This method internally converts characters to glyphs using the GDI function [GetCharacterPlacement](/previous-versions//ms534004(v=vs.85)).</span></span>

## <a name="requirements"></a><span data-ttu-id="93d9c-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="93d9c-130">Requirements</span></span>



| <span data-ttu-id="93d9c-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="93d9c-131">Requirement</span></span> | <span data-ttu-id="93d9c-132">Wert</span><span class="sxs-lookup"><span data-stu-id="93d9c-132">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="93d9c-133">Header</span><span class="sxs-lookup"><span data-stu-id="93d9c-133">Header</span></span><br/>  | <dl> <span data-ttu-id="93d9c-134"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="93d9c-134"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="93d9c-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="93d9c-135">Library</span></span><br/> | <dl> <span data-ttu-id="93d9c-136"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="93d9c-136"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93d9c-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="93d9c-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93d9c-138">ID3DX10Font</span><span class="sxs-lookup"><span data-stu-id="93d9c-138">ID3DX10Font</span></span>](id3dx10font.md)
</dt> <dt>

[<span data-ttu-id="93d9c-139">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="93d9c-139">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
