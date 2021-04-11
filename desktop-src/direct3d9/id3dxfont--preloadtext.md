---
description: Lädt formatierten Text in den Videospeicher, um die Effizienz des Renderings auf dem Gerät zu verbessern. Diese Methode unterstützt ANSI-und Unicode-Zeichen folgen.
ms.assetid: f2a4e9f5-87c5-46c0-965d-ce1535a6921d
title: ID3DXFont::P reloadtext-Methode (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.PreloadText
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 958979e3008cf9ae0b79e2de3591635187df0f12
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104132401"
---
# <a name="id3dxfontpreloadtext-method"></a><span data-ttu-id="52be7-104">ID3DXFont::P reloadtext-Methode</span><span class="sxs-lookup"><span data-stu-id="52be7-104">ID3DXFont::PreloadText method</span></span>

<span data-ttu-id="52be7-105">Lädt formatierten Text in den Videospeicher, um die Effizienz des Renderings auf dem Gerät zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="52be7-105">Loads formatted text into video memory to improve the efficiency of rendering to the device.</span></span> <span data-ttu-id="52be7-106">Diese Methode unterstützt ANSI-und Unicode-Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="52be7-106">This method supports ANSI and Unicode strings.</span></span>

## <a name="syntax"></a><span data-ttu-id="52be7-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="52be7-107">Syntax</span></span>


```C++
HRESULT PreloadText(
  [in] LPCTSTR *pString,
  [in] INT     Count
);
```



## <a name="parameters"></a><span data-ttu-id="52be7-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="52be7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52be7-109">*pstring* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="52be7-109">*pString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52be7-110">Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="52be7-110">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="52be7-111">Zeiger auf eine Zeichenfolge, die in den Videospeicher geladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="52be7-111">Pointer to a string of characters to be loaded into video memory.</span></span> <span data-ttu-id="52be7-112">Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR aufgelöst. Andernfalls wird der Datentyp in LPCSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="52be7-112">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR; otherwise, the data type resolves to LPCSTR.</span></span> <span data-ttu-id="52be7-113">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="52be7-113">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="52be7-114">*Anzahl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="52be7-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52be7-115">Typ: **[ **int**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="52be7-115">Type: **[**INT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="52be7-116">Anzahl der Zeichen in der Text Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="52be7-116">Number of characters in the text string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52be7-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="52be7-117">Return value</span></span>

<span data-ttu-id="52be7-118">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="52be7-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="52be7-119">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="52be7-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="52be7-120">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData.</span><span class="sxs-lookup"><span data-stu-id="52be7-120">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="52be7-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="52be7-121">Remarks</span></span>

<span data-ttu-id="52be7-122">Die Compilereinstellung bestimmt auch die Funktions Version.</span><span class="sxs-lookup"><span data-stu-id="52be7-122">The compiler setting also determines the function version.</span></span> <span data-ttu-id="52be7-123">Wenn Unicode definiert ist, wird der Funktions aufzurufen in preloadtextw aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="52be7-123">If Unicode is defined, the function call resolves to PreloadTextW.</span></span> <span data-ttu-id="52be7-124">Andernfalls wird der Funktions Aufrufwert in preloadtexta aufgelöst, da ANSI-Zeichen folgen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="52be7-124">Otherwise, the function call resolves to PreloadTextA because ANSI strings are being used.</span></span>

<span data-ttu-id="52be7-125">Diese Methode generiert Texturen, die Symbole enthalten, die den Eingabetext darstellen.</span><span class="sxs-lookup"><span data-stu-id="52be7-125">This method generates textures that contain glyphs that represent the input text.</span></span> <span data-ttu-id="52be7-126">Die Symbole werden als eine Reihe von Dreiecken gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="52be7-126">The glyphs are drawn as a series of triangles.</span></span>

<span data-ttu-id="52be7-127">Der Text wird nicht auf dem Gerät gerendert. [**DrawText**](id3dxfont--drawtext.md) muss dennoch aufgerufen werden, um den Text zu erzeugen.</span><span class="sxs-lookup"><span data-stu-id="52be7-127">Text will not be rendered to the device; [**DrawText**](id3dxfont--drawtext.md) must still be called to render the text.</span></span> <span data-ttu-id="52be7-128">Durch das vorab Laden von Text in den Videospeicher verwendet **DrawText** jedoch erheblich weniger CPU-Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="52be7-128">However, by preloading text into video memory, **DrawText** will use substantially fewer CPU resources.</span></span>

<span data-ttu-id="52be7-129">Diese Methode konvertiert Zeichen intern mithilfe der GDI-Funktion [**getcharakteriplacement**](/windows/win32/api/wingdi/nf-wingdi-getcharacterplacementa)in Glyphen.</span><span class="sxs-lookup"><span data-stu-id="52be7-129">This method internally converts characters to glyphs using the GDI function [**GetCharacterPlacement**](/windows/win32/api/wingdi/nf-wingdi-getcharacterplacementa).</span></span>

## <a name="requirements"></a><span data-ttu-id="52be7-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="52be7-130">Requirements</span></span>



| <span data-ttu-id="52be7-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="52be7-131">Requirement</span></span> | <span data-ttu-id="52be7-132">Wert</span><span class="sxs-lookup"><span data-stu-id="52be7-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="52be7-133">Header</span><span class="sxs-lookup"><span data-stu-id="52be7-133">Header</span></span><br/>  | <dl> <span data-ttu-id="52be7-134"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="52be7-134"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="52be7-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="52be7-135">Library</span></span><br/> | <dl> <span data-ttu-id="52be7-136"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="52be7-136"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="52be7-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="52be7-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52be7-138">ID3DXFont</span><span class="sxs-lookup"><span data-stu-id="52be7-138">ID3DXFont</span></span>](id3dxfont.md)
</dt> </dl>

 

 
