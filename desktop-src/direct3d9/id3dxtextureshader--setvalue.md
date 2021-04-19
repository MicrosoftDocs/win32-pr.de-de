---
description: Legt die Konstante Tabelle mit den Daten im Puffer fest.
ms.assetid: 55cf5456-8f23-405d-9329-8ff737c5c139
title: 'ID3DXTextureShader:: SetValue-Methode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetValue
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2f18902c73f44bc4294e5152f8da5ea3e37f27ba
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106363965"
---
# <a name="id3dxtextureshadersetvalue-method"></a><span data-ttu-id="9e68c-103">ID3DXTextureShader:: SetValue-Methode</span><span class="sxs-lookup"><span data-stu-id="9e68c-103">ID3DXTextureShader::SetValue method</span></span>

<span data-ttu-id="9e68c-104">Legt die Konstante Tabelle mit den Daten im Puffer fest.</span><span class="sxs-lookup"><span data-stu-id="9e68c-104">Sets the constant table with the data in the buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e68c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9e68c-105">Syntax</span></span>


```C++
HRESULT SetValue(
  [in] D3DXHANDLE hConstant,
  [in] LPCVOID    pData,
  [in] UINT       Bytes
);
```



## <a name="parameters"></a><span data-ttu-id="9e68c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9e68c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e68c-107">*hconstant* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9e68c-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e68c-108">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="9e68c-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="9e68c-109">Eindeutiger Bezeichner für eine Konstante.</span><span class="sxs-lookup"><span data-stu-id="9e68c-109">Unique identifier to a constant.</span></span> <span data-ttu-id="9e68c-110">Siehe [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="9e68c-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="9e68c-111">*pData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9e68c-111">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e68c-112">Geben Sie Folgendes ein: **[ **lpcvoid**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9e68c-112">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9e68c-113">Ein Zeiger auf einen Puffer, der die Konstanten Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="9e68c-113">A pointer to a buffer containing the constant data.</span></span>

</dd> <dt>

<span data-ttu-id="9e68c-114">*Bytes* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9e68c-114">*Bytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e68c-115">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9e68c-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9e68c-116">Größe des Puffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="9e68c-116">Size of the buffer, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e68c-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9e68c-117">Return value</span></span>

<span data-ttu-id="9e68c-118">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9e68c-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9e68c-119">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="9e68c-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="9e68c-120">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="9e68c-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e68c-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9e68c-121">Requirements</span></span>



| <span data-ttu-id="9e68c-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9e68c-122">Requirement</span></span> | <span data-ttu-id="9e68c-123">Wert</span><span class="sxs-lookup"><span data-stu-id="9e68c-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e68c-124">Header</span><span class="sxs-lookup"><span data-stu-id="9e68c-124">Header</span></span><br/>  | <dl> <span data-ttu-id="9e68c-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e68c-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="9e68c-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9e68c-126">Library</span></span><br/> | <dl> <span data-ttu-id="9e68c-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9e68c-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="9e68c-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9e68c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e68c-129">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="9e68c-129">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
