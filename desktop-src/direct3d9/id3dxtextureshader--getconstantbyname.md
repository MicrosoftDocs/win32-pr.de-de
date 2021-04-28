---
description: 'ID3DXTextureShader::GetConstantByName-Methode: Ruft eine Konstante ab, indem ihr Name gesucht wird.'
ms.assetid: 0c57f6ce-ea81-4b34-9251-c385bfe6ebe7
title: ID3DXTextureShader::GetConstantByName-Methode (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.GetConstantByName
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 825aca3f3227a340952092985f4730018fe316e5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117658"
---
# <a name="id3dxtextureshadergetconstantbyname-method"></a><span data-ttu-id="6b6f3-103">ID3DXTextureShader::GetConstantByName-Methode</span><span class="sxs-lookup"><span data-stu-id="6b6f3-103">ID3DXTextureShader::GetConstantByName method</span></span>

<span data-ttu-id="6b6f3-104">Ruft eine Konstante ab, indem ihr Name gesucht wird.</span><span class="sxs-lookup"><span data-stu-id="6b6f3-104">Gets a constant by looking up its name.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b6f3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6b6f3-105">Syntax</span></span>


```C++
D3DXHANDLE GetConstantByName(
  [in] D3DXHANDLE hConstant,
  [in] LPCSTR     pName
);
```



## <a name="parameters"></a><span data-ttu-id="6b6f3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6b6f3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b6f3-107">*hConstant* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="6b6f3-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b6f3-108">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="6b6f3-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="6b6f3-109">Ein [Handle](handles.md) für die übergeordnete Datenstruktur.</span><span class="sxs-lookup"><span data-stu-id="6b6f3-109">A [handle](handles.md) to the parent data structure.</span></span> <span data-ttu-id="6b6f3-110">Wenn die Konstante ein Parameter der obersten Ebene ist (es gibt keine übergeordnete Datenstruktur), verwenden Sie **NULL.**</span><span class="sxs-lookup"><span data-stu-id="6b6f3-110">If the constant is a top-level parameter (there is no parent data structure), use **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="6b6f3-111">*pName* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="6b6f3-111">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b6f3-112">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6b6f3-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6b6f3-113">Eine Zeichenfolge, die den Namen der Konstante enthält.</span><span class="sxs-lookup"><span data-stu-id="6b6f3-113">A string containing the name of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b6f3-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6b6f3-114">Return value</span></span>

<span data-ttu-id="6b6f3-115">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="6b6f3-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="6b6f3-116">Gibt einen eindeutigen Bezeichner an die Konstante zurück.</span><span class="sxs-lookup"><span data-stu-id="6b6f3-116">Returns a unique identifier to the constant.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b6f3-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6b6f3-117">Requirements</span></span>



| <span data-ttu-id="6b6f3-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6b6f3-118">Requirement</span></span> | <span data-ttu-id="6b6f3-119">Wert</span><span class="sxs-lookup"><span data-stu-id="6b6f3-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b6f3-120">Header</span><span class="sxs-lookup"><span data-stu-id="6b6f3-120">Header</span></span><br/>  | <dl> <span data-ttu-id="6b6f3-121"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="6b6f3-121"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="6b6f3-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6b6f3-122">Library</span></span><br/> | <dl> <span data-ttu-id="6b6f3-123"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="6b6f3-123"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="6b6f3-124">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="6b6f3-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b6f3-125">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="6b6f3-125">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
