---
description: Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um ein Array von booleschen Scheitelpunkt Konstanten für Vertex-Shader festzulegen.
ms.assetid: 25fd0c68-11b5-4401-a2f8-86075ba3fa54
title: 'ID3DXEffectStateManager:: setvertexshaderconstantb-Methode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetVertexShaderConstantB
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 1eaf68f27d477aee36bd7773488f34bad29db61d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106351967"
---
# <a name="id3dxeffectstatemanagersetvertexshaderconstantb-method"></a><span data-ttu-id="1e83f-103">ID3DXEffectStateManager:: setvertexshaderconstantb-Methode</span><span class="sxs-lookup"><span data-stu-id="1e83f-103">ID3DXEffectStateManager::SetVertexShaderConstantB method</span></span>

<span data-ttu-id="1e83f-104">Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um ein Array von booleschen Scheitelpunkt Konstanten für Vertex-Shader festzulegen.</span><span class="sxs-lookup"><span data-stu-id="1e83f-104">A callback function that must be implemented by a user to set an array of vertex shader Boolean constants.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e83f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1e83f-105">Syntax</span></span>


```C++
HRESULT SetVertexShaderConstantB(
  [out]       UINT StartRegister,
  [out] const BOOL *pConstantData,
  [out]       UINT RegisterCount
);
```



## <a name="parameters"></a><span data-ttu-id="1e83f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1e83f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e83f-107">*Startregiester* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="1e83f-107">*StartRegister* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1e83f-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1e83f-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1e83f-109">Der null basierte Index des ersten Konstanten Registers.</span><span class="sxs-lookup"><span data-stu-id="1e83f-109">The zero-based index of the first constant register.</span></span>

</dd> <dt>

<span data-ttu-id="1e83f-110">*pconstantdata* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="1e83f-110">*pConstantData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1e83f-111">Typ: Konstante **[**bool**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="1e83f-111">Type: **const [**BOOL**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="1e83f-112">Ein Array von booleschen Konstanten.</span><span class="sxs-lookup"><span data-stu-id="1e83f-112">An array of Boolean constants.</span></span>

</dd> <dt>

<span data-ttu-id="1e83f-113">*Register count* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="1e83f-113">*RegisterCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1e83f-114">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1e83f-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1e83f-115">Die Anzahl der Register in pconstantdata.</span><span class="sxs-lookup"><span data-stu-id="1e83f-115">The number of registers in pConstantData.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e83f-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1e83f-116">Return value</span></span>

<span data-ttu-id="1e83f-117">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1e83f-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1e83f-118">Die vom Benutzer implementierte Methode sollte S \_ OK zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="1e83f-118">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="1e83f-119">Wenn der Rückruf beim Festlegen des Geräte Zustands fehlschlägt, wird eine der folgenden Aktionen ausgeführt:</span><span class="sxs-lookup"><span data-stu-id="1e83f-119">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="1e83f-120">Der Effekt schlägt während [**ID3DXEffect:: beginpass**](id3dxeffect--beginpass.md)fehl.</span><span class="sxs-lookup"><span data-stu-id="1e83f-120">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="1e83f-121">Der dynamische Effekt Status-aufrufen (z. [**b. IDirect3DDevice9:: setvertexshaderconstantb**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantb)) schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="1e83f-121">The dynamic effect state call (such as [**IDirect3DDevice9::SetVertexShaderConstantB**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantb)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e83f-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1e83f-122">Requirements</span></span>



| <span data-ttu-id="1e83f-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1e83f-123">Requirement</span></span> | <span data-ttu-id="1e83f-124">Wert</span><span class="sxs-lookup"><span data-stu-id="1e83f-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e83f-125">Header</span><span class="sxs-lookup"><span data-stu-id="1e83f-125">Header</span></span><br/>  | <dl> <span data-ttu-id="1e83f-126"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e83f-126"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="1e83f-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1e83f-127">Library</span></span><br/> | <dl> <span data-ttu-id="1e83f-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1e83f-128"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="1e83f-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1e83f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e83f-130">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="1e83f-130">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
