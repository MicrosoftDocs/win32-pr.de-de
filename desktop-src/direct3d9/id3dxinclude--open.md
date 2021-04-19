---
description: Eine vom Benutzer implementierte Methode zum Öffnen und Lesen des Inhalts einer-Shader- \# Includedatei.
ms.assetid: ad0105f7-042d-4e96-ad4a-1ece08e519af
title: 'ID3DXInclude:: Open-Methode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXInclude.Open
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 313b3f4845f9a46f758a40b6b315cc5b5eeecb29
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355231"
---
# <a name="id3dxincludeopen-method"></a><span data-ttu-id="2f5fc-103">ID3DXInclude:: Open-Methode</span><span class="sxs-lookup"><span data-stu-id="2f5fc-103">ID3DXInclude::Open method</span></span>

<span data-ttu-id="2f5fc-104">Eine vom Benutzer implementierte Methode zum Öffnen und Lesen des Inhalts einer-Shader- \# Includedatei.</span><span class="sxs-lookup"><span data-stu-id="2f5fc-104">A user-implemented method for opening and reading the contents of a shader \#include file.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f5fc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2f5fc-105">Syntax</span></span>


```C++
HRESULT Open(
  [in]  D3DXINCLUDE_TYPE IncludeType,
  [in]  LPCSTR           pFileName,
  [in]  LPCVOID          pParentData,
  [out] LPCVOID          *ppData,
  [out] UINT             *pBytes
);
```



## <a name="parameters"></a><span data-ttu-id="2f5fc-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2f5fc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f5fc-107">*IncludeType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2f5fc-107">*IncludeType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f5fc-108">Type: **[ **D3DXINCLUDE- \_ Typ**](./d3dxinclude-type.md)**</span><span class="sxs-lookup"><span data-stu-id="2f5fc-108">Type: **[**D3DXINCLUDE\_TYPE**](./d3dxinclude-type.md)**</span></span>

<span data-ttu-id="2f5fc-109">Der Speicherort der \# Includedatei.</span><span class="sxs-lookup"><span data-stu-id="2f5fc-109">The location of the \#include file.</span></span> <span data-ttu-id="2f5fc-110">Siehe [**D3DXINCLUDE \_ Type**](./d3dxinclude-type.md).</span><span class="sxs-lookup"><span data-stu-id="2f5fc-110">See [**D3DXINCLUDE\_TYPE**](./d3dxinclude-type.md).</span></span>

</dd> <dt>

<span data-ttu-id="2f5fc-111">*pfilename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2f5fc-111">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f5fc-112">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2f5fc-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2f5fc-113">Der Name der \# Includedatei.</span><span class="sxs-lookup"><span data-stu-id="2f5fc-113">Name of the \#include file.</span></span>

</dd> <dt>

<span data-ttu-id="2f5fc-114">*pparser-Daten* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2f5fc-114">*pParentData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f5fc-115">Geben Sie Folgendes ein: **[ **lpcvoid**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2f5fc-115">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2f5fc-116">Zeiger auf den Container, der die \# Includedatei enthält.</span><span class="sxs-lookup"><span data-stu-id="2f5fc-116">Pointer to the container that includes the \#include file.</span></span> <span data-ttu-id="2f5fc-117">Der Compiler kann NULL in *pparameentdata* übergeben.</span><span class="sxs-lookup"><span data-stu-id="2f5fc-117">The compiler might pass NULL in *pParentData*.</span></span> <span data-ttu-id="2f5fc-118">Weitere Informationen finden Sie im Abschnitt "Suchen nach Includedateien" unter [Kompilieren eines Effekts (Direct3D 11)](../direct3d11/d3d11-graphics-programming-guide-effects-compile.md).</span><span class="sxs-lookup"><span data-stu-id="2f5fc-118">For more information, see the "Searching for Include Files" section in [Compile an Effect (Direct3D 11)](../direct3d11/d3d11-graphics-programming-guide-effects-compile.md).</span></span>

</dd> <dt>

<span data-ttu-id="2f5fc-119">*ppData* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="2f5fc-119">*ppData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2f5fc-120">Geben Sie Folgendes ein: **[ **lpcvoid**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="2f5fc-120">Type: **[**LPCVOID**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="2f5fc-121">Ein Zeiger auf den zurückgegebenen Puffer, der die include-Direktiven enthält.</span><span class="sxs-lookup"><span data-stu-id="2f5fc-121">Pointer to the returned buffer that contains the include directives.</span></span> <span data-ttu-id="2f5fc-122">Dieser Zeiger bleibt gültig, bis [**ID3DXInclude:: Close**](id3dxinclude--close.md) aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="2f5fc-122">This pointer remains valid until [**ID3DXInclude::Close**](id3dxinclude--close.md) is called.</span></span>

</dd> <dt>

<span data-ttu-id="2f5fc-123">*Pbytes* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="2f5fc-123">*pBytes* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2f5fc-124">Typ: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="2f5fc-124">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="2f5fc-125">Anzahl der in ppData zurückgegebenen Bytes.</span><span class="sxs-lookup"><span data-stu-id="2f5fc-125">Number of bytes returned in ppData.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f5fc-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2f5fc-126">Return value</span></span>

<span data-ttu-id="2f5fc-127">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2f5fc-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2f5fc-128">Die vom Benutzer implementierte Methode sollte S \_ OK zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="2f5fc-128">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="2f5fc-129">Wenn beim Lesen der Includedatei der Rückruf fehlschlägt \# , schlägt die API fehl, die den Aufruf des Rückrufs bewirkt hat.</span><span class="sxs-lookup"><span data-stu-id="2f5fc-129">If the callback fails when reading the \#include file, the API that caused the callback to be called will fail.</span></span> <span data-ttu-id="2f5fc-130">Folgende Werte sind möglich:</span><span class="sxs-lookup"><span data-stu-id="2f5fc-130">This is one of the following:</span></span>

-   <span data-ttu-id="2f5fc-131">Der HLSL-Shader erzeugt eine der D3DXCompileShader- \* \* \* Funktionen nicht.</span><span class="sxs-lookup"><span data-stu-id="2f5fc-131">The HLSL shader will fail one of the D3DXCompileShader\*\*\* functions.</span></span>
-   <span data-ttu-id="2f5fc-132">Der assemblyshader führt einen der D3DXAssembleShader- \* \* \* Funktionen aus.</span><span class="sxs-lookup"><span data-stu-id="2f5fc-132">The assembly shader will fail one of the D3DXAssembleShader\*\*\* functions.</span></span>
-   <span data-ttu-id="2f5fc-133">Der Effekt führt nicht zu einer der D3DXCreateEffect- \* \* \* oder D3DXCreateEffectCompiler- \* \* \* Funktionen.</span><span class="sxs-lookup"><span data-stu-id="2f5fc-133">The effect will fail one of the D3DXCreateEffect\*\*\* or D3DXCreateEffectCompiler\*\*\* functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f5fc-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2f5fc-134">Requirements</span></span>



| <span data-ttu-id="2f5fc-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2f5fc-135">Requirement</span></span> | <span data-ttu-id="2f5fc-136">Wert</span><span class="sxs-lookup"><span data-stu-id="2f5fc-136">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f5fc-137">Header</span><span class="sxs-lookup"><span data-stu-id="2f5fc-137">Header</span></span><br/>  | <dl> <span data-ttu-id="2f5fc-138"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f5fc-138"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="2f5fc-139">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2f5fc-139">Library</span></span><br/> | <dl> <span data-ttu-id="2f5fc-140"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2f5fc-140"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="2f5fc-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2f5fc-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f5fc-142">ID3DXInclude</span><span class="sxs-lookup"><span data-stu-id="2f5fc-142">ID3DXInclude</span></span>](id3dxinclude.md)
</dt> <dt>

[<span data-ttu-id="2f5fc-143">**ID3DXInclude:: Close**</span><span class="sxs-lookup"><span data-stu-id="2f5fc-143">**ID3DXInclude::Close**</span></span>](id3dxinclude--close.md)
</dt> </dl>

 

 
