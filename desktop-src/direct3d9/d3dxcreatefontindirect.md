---
description: Erstellt ein Schriftart Objekt indirekt für ein Gerät und eine Schriftart.
ms.assetid: 480f3012-8495-47ca-a649-11ce53cee06c
title: D3DXCreateFontIndirect-Funktion (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateFontIndirect
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 086f9cb4cff7666fc3977551e2c9fd4a61150d46
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355457"
---
# <a name="d3dxcreatefontindirect-function"></a><span data-ttu-id="541fe-103">D3DXCreateFontIndirect-Funktion</span><span class="sxs-lookup"><span data-stu-id="541fe-103">D3DXCreateFontIndirect function</span></span>

<span data-ttu-id="541fe-104">Erstellt ein Schriftart Objekt indirekt für ein Gerät und eine Schriftart.</span><span class="sxs-lookup"><span data-stu-id="541fe-104">Creates a font object indirectly for both a device and a font.</span></span>

## <a name="syntax"></a><span data-ttu-id="541fe-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="541fe-105">Syntax</span></span>


```C++
HRESULT D3DXCreateFontIndirect(
  _In_        LPDIRECT3DDEVICE9 pDevice,
  _In_  const D3DXFONT_DESC     *pDesc,
  _Out_       LPD3DXFONT        *ppFont
);
```



## <a name="parameters"></a><span data-ttu-id="541fe-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="541fe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="541fe-107">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="541fe-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="541fe-108">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="541fe-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="541fe-109">Zeiger auf eine [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle, das Gerät, das dem Schriftart Objekt zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="541fe-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, the device to be associated with the font object.</span></span>

</dd> <dt>

<span data-ttu-id="541fe-110">*PDE SC* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="541fe-110">*pDesc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="541fe-111">Typ: **[**D3DXFONT \_ DESC**](d3dxfont-desc.md) \***</span><span class="sxs-lookup"><span data-stu-id="541fe-111">Type: **const [**D3DXFONT\_DESC**](d3dxfont-desc.md)\***</span></span>

<span data-ttu-id="541fe-112">Ein Zeiger auf eine [**D3DXFONT \_ -Struktur**](d3dxfont-desc.md) , die die Attribute des zu erstellenden Schriftart Objekts beschreibt.</span><span class="sxs-lookup"><span data-stu-id="541fe-112">Pointer to a [**D3DXFONT\_DESC**](d3dxfont-desc.md) structure, describing the attributes of the font object to create.</span></span> <span data-ttu-id="541fe-113">Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp D3DXFONT \_ DESC in D3DXFONT \_ descw aufgelöst; andernfalls wird der Datentyp in D3DXFONT \_ DeScA aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="541fe-113">If the compiler settings require Unicode, the data type D3DXFONT\_DESC resolves to D3DXFONT\_DESCW; otherwise, the data type resolves to D3DXFONT\_DESCA.</span></span> <span data-ttu-id="541fe-114">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="541fe-114">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="541fe-115">*ppfont* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="541fe-115">*ppFont* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="541fe-116">Typ: **[ **LPD3DXFONT**](id3dxfont.md)\***</span><span class="sxs-lookup"><span data-stu-id="541fe-116">Type: **[**LPD3DXFONT**](id3dxfont.md)\***</span></span>

<span data-ttu-id="541fe-117">Gibt einen Zeiger auf eine [**ID3DXFont**](id3dxfont.md) -Schnittstelle zurück, die das erstellte Schriftart Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="541fe-117">Returns a pointer to an [**ID3DXFont**](id3dxfont.md) interface, representing the created font object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="541fe-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="541fe-118">Return value</span></span>

<span data-ttu-id="541fe-119">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="541fe-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="541fe-120">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="541fe-120">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="541fe-121">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ oudefmemory.</span><span class="sxs-lookup"><span data-stu-id="541fe-121">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="541fe-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="541fe-122">Remarks</span></span>

<span data-ttu-id="541fe-123">Die Compilereinstellung bestimmt auch die Funktions Version.</span><span class="sxs-lookup"><span data-stu-id="541fe-123">The compiler setting also determines the function version.</span></span> <span data-ttu-id="541fe-124">Wenn Unicode definiert ist, wird der Funktions aufrufin D3DXCreateFontIndirectW aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="541fe-124">If Unicode is defined, the function call resolves to D3DXCreateFontIndirectW.</span></span> <span data-ttu-id="541fe-125">Andernfalls wird der Funktions Aufruhe in D3DXCreateFontIndirectA aufgelöst, da ANSI-Zeichen folgen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="541fe-125">Otherwise, the function call resolves to D3DXCreateFontIndirectA because ANSI strings are being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="541fe-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="541fe-126">Requirements</span></span>



| <span data-ttu-id="541fe-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="541fe-127">Requirement</span></span> | <span data-ttu-id="541fe-128">Wert</span><span class="sxs-lookup"><span data-stu-id="541fe-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="541fe-129">Header</span><span class="sxs-lookup"><span data-stu-id="541fe-129">Header</span></span><br/>  | <dl> <span data-ttu-id="541fe-130"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="541fe-130"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="541fe-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="541fe-131">Library</span></span><br/> | <dl> <span data-ttu-id="541fe-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="541fe-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="541fe-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="541fe-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="541fe-134">Universell Funktionen</span><span class="sxs-lookup"><span data-stu-id="541fe-134">General Purpose Functions</span></span>](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
