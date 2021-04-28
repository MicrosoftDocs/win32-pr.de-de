---
description: 'ID3DXEffectStateManager::SetVertexShaderConstantF-Methode: Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um ein Array von Vertexshader-Gleitkommakonstanten festzulegen.'
ms.assetid: 3a13040d-5d5a-4454-bf11-cda9653585c0
title: ID3DXEffectStateManager::SetVertexShaderConstantF-Methode (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetVertexShaderConstantF
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: ffbad3c695758a0388baf8161c322c1ff423699b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090388"
---
# <a name="id3dxeffectstatemanagersetvertexshaderconstantf-method"></a><span data-ttu-id="a555a-103">ID3DXEffectStateManager::SetVertexShaderConstantF-Methode</span><span class="sxs-lookup"><span data-stu-id="a555a-103">ID3DXEffectStateManager::SetVertexShaderConstantF method</span></span>

<span data-ttu-id="a555a-104">Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um ein Array von Vertex-Shader-Gleitkommakonstanten festzulegen.</span><span class="sxs-lookup"><span data-stu-id="a555a-104">A callback function that must be implemented by a user to set an array of vertex shader floating-point constants.</span></span>

## <a name="syntax"></a><span data-ttu-id="a555a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a555a-105">Syntax</span></span>


```C++
HRESULT SetVertexShaderConstantF(
  [out]       UINT  StartRegister,
  [out] const FLOAT *pConstantData,
  [out]       UINT  RegisterCount
);
```



## <a name="parameters"></a><span data-ttu-id="a555a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a555a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a555a-107">*StartRegister* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a555a-107">*StartRegister* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a555a-108">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a555a-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a555a-109">Der nullbasierte Index des ersten Konstantenregisters.</span><span class="sxs-lookup"><span data-stu-id="a555a-109">The zero-based index of the first constant register.</span></span>

</dd> <dt>

<span data-ttu-id="a555a-110">*pConstantData* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a555a-110">*pConstantData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a555a-111">Typ: **const [**FLOAT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="a555a-111">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="a555a-112">Ein Array von Gleitkommakonstanten.</span><span class="sxs-lookup"><span data-stu-id="a555a-112">An array of floating-point constants.</span></span>

</dd> <dt>

<span data-ttu-id="a555a-113">*RegisterCount* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a555a-113">*RegisterCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a555a-114">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a555a-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a555a-115">Die Anzahl der Register in pConstantData.</span><span class="sxs-lookup"><span data-stu-id="a555a-115">The number of registers in pConstantData.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a555a-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a555a-116">Return value</span></span>

<span data-ttu-id="a555a-117">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a555a-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a555a-118">Die vom Benutzer implementierte Methode sollte S \_ OK zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="a555a-118">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="a555a-119">Wenn der Rückruf beim Festlegen des Gerätezustands fehlschlägt, tritt eine der folgenden Schritte auf:</span><span class="sxs-lookup"><span data-stu-id="a555a-119">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="a555a-120">Die Auswirkung schlägt während [**id3DXEffect::BeginPass**](id3dxeffect--beginpass.md)fehl.</span><span class="sxs-lookup"><span data-stu-id="a555a-120">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="a555a-121">Der Dynamische Effektzustandsaufruf (z.B. [**IDirect3DDevice9::SetVertexShaderConstantF)**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantf)schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="a555a-121">The dynamic effect state call (such as [**IDirect3DDevice9::SetVertexShaderConstantF**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantf)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="a555a-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a555a-122">Requirements</span></span>



| <span data-ttu-id="a555a-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a555a-123">Requirement</span></span> | <span data-ttu-id="a555a-124">Wert</span><span class="sxs-lookup"><span data-stu-id="a555a-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a555a-125">Header</span><span class="sxs-lookup"><span data-stu-id="a555a-125">Header</span></span><br/>  | <dl> <span data-ttu-id="a555a-126"><dt>D3DX9Effect.h</dt></span><span class="sxs-lookup"><span data-stu-id="a555a-126"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="a555a-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a555a-127">Library</span></span><br/> | <dl> <span data-ttu-id="a555a-128"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="a555a-128"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="a555a-129">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a555a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a555a-130">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="a555a-130">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
