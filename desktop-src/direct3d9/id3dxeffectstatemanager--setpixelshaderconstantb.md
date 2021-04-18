---
description: Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um ein Array von booleschen Scheitelpunkt Konstanten für Vertex-Shader festzulegen.
ms.assetid: ad4d9beb-fd34-4574-9787-61bd3bfaaaaa
title: 'ID3DXEffectStateManager:: setpixelshaderconstantb-Methode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetPixelShaderConstantB
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: e3c3c988bdbfa84a3e815fe94d89c24f3fa3a264
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355029"
---
# <a name="id3dxeffectstatemanagersetpixelshaderconstantb-method"></a><span data-ttu-id="0c58e-103">ID3DXEffectStateManager:: setpixelshaderconstantb-Methode</span><span class="sxs-lookup"><span data-stu-id="0c58e-103">ID3DXEffectStateManager::SetPixelShaderConstantB method</span></span>

<span data-ttu-id="0c58e-104">Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um ein Array von booleschen Scheitelpunkt Konstanten für Vertex-Shader festzulegen.</span><span class="sxs-lookup"><span data-stu-id="0c58e-104">A callback function that must be implemented by a user to set an array of vertex shader Boolean constants.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c58e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0c58e-105">Syntax</span></span>


```C++
HRESULT SetPixelShaderConstantB(
  [out]       UINT StartRegister,
  [out] const BOOL *pConstantData,
  [out]       UINT RegisterCount
);
```



## <a name="parameters"></a><span data-ttu-id="0c58e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0c58e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c58e-107">*Startregiester* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="0c58e-107">*StartRegister* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0c58e-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0c58e-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0c58e-109">Der null basierte Index des ersten Konstanten Registers.</span><span class="sxs-lookup"><span data-stu-id="0c58e-109">The zero-based index of the first constant register.</span></span>

</dd> <dt>

<span data-ttu-id="0c58e-110">*pconstantdata* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="0c58e-110">*pConstantData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0c58e-111">Typ: Konstante **[**bool**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="0c58e-111">Type: **const [**BOOL**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="0c58e-112">Ein Array von booleschen Konstanten.</span><span class="sxs-lookup"><span data-stu-id="0c58e-112">An array of Boolean constants.</span></span>

</dd> <dt>

<span data-ttu-id="0c58e-113">*Register count* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="0c58e-113">*RegisterCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0c58e-114">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0c58e-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0c58e-115">Die Anzahl der Register in pconstantdata.</span><span class="sxs-lookup"><span data-stu-id="0c58e-115">The number of registers in pConstantData.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c58e-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0c58e-116">Return value</span></span>

<span data-ttu-id="0c58e-117">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0c58e-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0c58e-118">Die vom Benutzer implementierte Methode sollte S \_ OK zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="0c58e-118">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="0c58e-119">Wenn der Rückruf beim Festlegen des Geräte Zustands fehlschlägt, wird eine der folgenden Aktionen ausgeführt:</span><span class="sxs-lookup"><span data-stu-id="0c58e-119">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="0c58e-120">Der Effekt schlägt während [**ID3DXEffect:: beginpass**](id3dxeffect--beginpass.md)fehl.</span><span class="sxs-lookup"><span data-stu-id="0c58e-120">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="0c58e-121">Der dynamische Effekt Zustands Aufrufe (z. b. [**IDirect3DDevice9:: setpixelshaderconstantb**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb)) schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="0c58e-121">The dynamic effect state call (such as [**IDirect3DDevice9::SetPixelShaderConstantB**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c58e-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0c58e-122">Requirements</span></span>



| <span data-ttu-id="0c58e-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0c58e-123">Requirement</span></span> | <span data-ttu-id="0c58e-124">Wert</span><span class="sxs-lookup"><span data-stu-id="0c58e-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c58e-125">Header</span><span class="sxs-lookup"><span data-stu-id="0c58e-125">Header</span></span><br/>  | <dl> <span data-ttu-id="0c58e-126"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c58e-126"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="0c58e-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0c58e-127">Library</span></span><br/> | <dl> <span data-ttu-id="0c58e-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0c58e-128"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="0c58e-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0c58e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c58e-130">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="0c58e-130">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
