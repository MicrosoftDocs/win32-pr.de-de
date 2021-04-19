---
description: Legt den Inhalt des Puffers auf die Konstante Tabelle fest.
ms.assetid: 6058795c-fa32-42aa-9a36-af0b7f6eed1d
title: 'ID3DXConstantTable:: SetValue-Methode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetValue
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e5e02c43e0d0ad84615650bc0b1c0d5fd5654e38
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106363976"
---
# <a name="id3dxconstanttablesetvalue-method"></a><span data-ttu-id="fada2-103">ID3DXConstantTable:: SetValue-Methode</span><span class="sxs-lookup"><span data-stu-id="fada2-103">ID3DXConstantTable::SetValue method</span></span>

<span data-ttu-id="fada2-104">Legt den Inhalt des Puffers auf die Konstante Tabelle fest.</span><span class="sxs-lookup"><span data-stu-id="fada2-104">Sets the contents of the buffer to the constant table.</span></span>

## <a name="syntax"></a><span data-ttu-id="fada2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fada2-105">Syntax</span></span>


```C++
HRESULT SetValue(
  [in] LPDIRECT3DDEVICE9 pDevice,
  [in] D3DXHANDLE        hConstant,
  [in] LPCVOID           pData,
  [in] UINT              Bytes
);
```



## <a name="parameters"></a><span data-ttu-id="fada2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fada2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fada2-107">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fada2-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fada2-108">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="fada2-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="fada2-109">Zeiger auf eine [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle, die das Gerät darstellt, das der Konstanten Tabelle zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="fada2-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="fada2-110">*hconstant* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fada2-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fada2-111">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="fada2-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="fada2-112">Eindeutiger Bezeichner für eine Konstante.</span><span class="sxs-lookup"><span data-stu-id="fada2-112">Unique identifier to a constant.</span></span> <span data-ttu-id="fada2-113">Siehe [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="fada2-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="fada2-114">*pData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fada2-114">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fada2-115">Geben Sie Folgendes ein: **[ **lpcvoid**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fada2-115">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fada2-116">Puffer, der Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="fada2-116">Buffer containing data.</span></span>

</dd> <dt>

<span data-ttu-id="fada2-117">*Bytes* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fada2-117">*Bytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fada2-118">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fada2-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fada2-119">Größe des Puffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="fada2-119">Size of the buffer, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fada2-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fada2-120">Return value</span></span>

<span data-ttu-id="fada2-121">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fada2-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fada2-122">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="fada2-122">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="fada2-123">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="fada2-123">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="fada2-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fada2-124">Requirements</span></span>



| <span data-ttu-id="fada2-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fada2-125">Requirement</span></span> | <span data-ttu-id="fada2-126">Wert</span><span class="sxs-lookup"><span data-stu-id="fada2-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fada2-127">Header</span><span class="sxs-lookup"><span data-stu-id="fada2-127">Header</span></span><br/>  | <dl> <span data-ttu-id="fada2-128"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="fada2-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="fada2-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="fada2-129">Library</span></span><br/> | <dl> <span data-ttu-id="fada2-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fada2-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="fada2-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fada2-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fada2-132">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="fada2-132">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
