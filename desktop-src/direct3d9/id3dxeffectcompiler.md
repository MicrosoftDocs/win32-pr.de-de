---
description: Die ID3DXEffectCompiler-Schnittstelle kompiliert einen Effekt aus einer Funktion oder einem Scheitelpunkt-Shader.
ms.assetid: 2d1dbc63-1eb9-4736-a0b5-7f899c0638be
title: ID3DXEffectCompiler-Schnittstelle (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectCompiler
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d69cbcd6c14bb3a874a382f46fe5aee6619b8168
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354346"
---
# <a name="id3dxeffectcompiler-interface"></a><span data-ttu-id="0ec78-103">ID3DXEffectCompiler-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="0ec78-103">ID3DXEffectCompiler interface</span></span>

<span data-ttu-id="0ec78-104">Die **ID3DXEffectCompiler** -Schnittstelle kompiliert einen Effekt aus einer Funktion oder einem Scheitelpunkt-Shader.</span><span class="sxs-lookup"><span data-stu-id="0ec78-104">The **ID3DXEffectCompiler** interface compiles an effect from a function or from a vertex shader.</span></span>

## <a name="members"></a><span data-ttu-id="0ec78-105">Member</span><span class="sxs-lookup"><span data-stu-id="0ec78-105">Members</span></span>

<span data-ttu-id="0ec78-106">Die **ID3DXEffectCompiler** -Schnittstelle erbt von [**ID3DXBaseEffect**](id3dxbaseeffect.md).</span><span class="sxs-lookup"><span data-stu-id="0ec78-106">The **ID3DXEffectCompiler** interface inherits from [**ID3DXBaseEffect**](id3dxbaseeffect.md).</span></span> <span data-ttu-id="0ec78-107">**ID3DXEffectCompiler** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="0ec78-107">**ID3DXEffectCompiler** also has these types of members:</span></span>

-   [<span data-ttu-id="0ec78-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="0ec78-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="0ec78-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="0ec78-109">Methods</span></span>

<span data-ttu-id="0ec78-110">Die **ID3DXEffectCompiler** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="0ec78-110">The **ID3DXEffectCompiler** interface has these methods.</span></span>



| <span data-ttu-id="0ec78-111">Methode</span><span class="sxs-lookup"><span data-stu-id="0ec78-111">Method</span></span>                                                      | <span data-ttu-id="0ec78-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0ec78-112">Description</span></span>                                                                                                                                 |
|:------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0ec78-113">**Compileeffect**</span><span class="sxs-lookup"><span data-stu-id="0ec78-113">**CompileEffect**</span></span>](id3dxeffectcompiler--compileeffect.md) | <span data-ttu-id="0ec78-114">Kompilieren eines Effekts.</span><span class="sxs-lookup"><span data-stu-id="0ec78-114">Compile an effect.</span></span><br/>                                                                                                               |
| [<span data-ttu-id="0ec78-115">**Compileshader**</span><span class="sxs-lookup"><span data-stu-id="0ec78-115">**CompileShader**</span></span>](id3dxeffectcompiler--compileshader.md) | <span data-ttu-id="0ec78-116">Kompiliert einen Shader aus einem Effekt, der eine oder mehrere Funktionen enthält.</span><span class="sxs-lookup"><span data-stu-id="0ec78-116">Compiles a shader from an effect that contains one or more functions.</span></span><br/>                                                            |
| [<span data-ttu-id="0ec78-117">**Getliteral**</span><span class="sxs-lookup"><span data-stu-id="0ec78-117">**GetLiteral**</span></span>](id3dxeffectcompiler--getliteral.md)       | <span data-ttu-id="0ec78-118">Ruft den literalstatus eines Parameters ab.</span><span class="sxs-lookup"><span data-stu-id="0ec78-118">Gets a literal status of a parameter.</span></span> <span data-ttu-id="0ec78-119">Ein literalparameter weist einen Wert auf, der sich während der Lebensdauer eines Effekts nicht ändert.</span><span class="sxs-lookup"><span data-stu-id="0ec78-119">A literal parameter has a value that doesn't change during the lifetime of an effect.</span></span><br/>      |
| [<span data-ttu-id="0ec78-120">**Setliterale**</span><span class="sxs-lookup"><span data-stu-id="0ec78-120">**SetLiteral**</span></span>](id3dxeffectcompiler--setliteral.md)       | <span data-ttu-id="0ec78-121">Schaltet den literalstatus eines Parameters um.</span><span class="sxs-lookup"><span data-stu-id="0ec78-121">Toggles the literal status of a parameter.</span></span> <span data-ttu-id="0ec78-122">Ein literalparameter weist einen Wert auf, der sich während der Lebensdauer eines Effekts nicht ändert.</span><span class="sxs-lookup"><span data-stu-id="0ec78-122">A literal parameter has a value that doesn't change during the lifetime of an effect.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0ec78-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0ec78-123">Remarks</span></span>

<span data-ttu-id="0ec78-124">Die ID3DXEffectCompiler-Schnittstelle wird durch Aufrufen von [**D3DXCreateEffectCompiler**](d3dxcreateeffectcompiler.md), [**D3DXCreateEffectCompilerFromFile**](d3dxcreateeffectcompilerfromfile.md)oder [**D3DXCreateEffectCompilerFromResource**](d3dxcreateeffectcompilerfromresource.md)abgerufen.</span><span class="sxs-lookup"><span data-stu-id="0ec78-124">The ID3DXEffectCompiler interface is obtained by calling [**D3DXCreateEffectCompiler**](d3dxcreateeffectcompiler.md), [**D3DXCreateEffectCompilerFromFile**](d3dxcreateeffectcompilerfromfile.md), or [**D3DXCreateEffectCompilerFromResource**](d3dxcreateeffectcompilerfromresource.md).</span></span>

<span data-ttu-id="0ec78-125">Der LPD3DXEFFECTCOMPILER-Typ wird als Zeiger auf diese Schnittstelle definiert.</span><span class="sxs-lookup"><span data-stu-id="0ec78-125">The LPD3DXEFFECTCOMPILER type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXEffectCompiler ID3DXEffectCompiler;
typedef interface ID3DXEffectCompiler *LPD3DXEFFECTCOMPILER;
```



## <a name="requirements"></a><span data-ttu-id="0ec78-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0ec78-126">Requirements</span></span>



| <span data-ttu-id="0ec78-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0ec78-127">Requirement</span></span> | <span data-ttu-id="0ec78-128">Wert</span><span class="sxs-lookup"><span data-stu-id="0ec78-128">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ec78-129">Header</span><span class="sxs-lookup"><span data-stu-id="0ec78-129">Header</span></span><br/>  | <dl> <span data-ttu-id="0ec78-130"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ec78-130"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="0ec78-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0ec78-131">Library</span></span><br/> | <dl> <span data-ttu-id="0ec78-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0ec78-132"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="0ec78-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0ec78-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ec78-134">**ID3DXBaseEffect**</span><span class="sxs-lookup"><span data-stu-id="0ec78-134">**ID3DXBaseEffect**</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="0ec78-135">Effekt Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="0ec78-135">Effect Interfaces</span></span>](dx9-graphics-reference-effects-interfaces.md)
</dt> <dt>

[<span data-ttu-id="0ec78-136">**D3DXCreateEffectCompiler**</span><span class="sxs-lookup"><span data-stu-id="0ec78-136">**D3DXCreateEffectCompiler**</span></span>](d3dxcreateeffectcompiler.md)
</dt> <dt>

[<span data-ttu-id="0ec78-137">**D3DXCreateEffectCompilerFromFile**</span><span class="sxs-lookup"><span data-stu-id="0ec78-137">**D3DXCreateEffectCompilerFromFile**</span></span>](d3dxcreateeffectcompilerfromfile.md)
</dt> <dt>

[<span data-ttu-id="0ec78-138">**D3DXCreateEffectCompilerFromResource**</span><span class="sxs-lookup"><span data-stu-id="0ec78-138">**D3DXCreateEffectCompilerFromResource**</span></span>](d3dxcreateeffectcompilerfromresource.md)
</dt> </dl>

 

 




