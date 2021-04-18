---
description: Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um ein Array von Vertex-Shader-Gleit Komma Konstanten festzulegen.
ms.assetid: db87ca8c-2539-4d80-854c-25b114a7e7e0
title: 'ID3DXEffectStateManager:: setpixelshaderconstantf-Methode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetPixelShaderConstantF
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 19e8654fbc851460fea932a8c858240c5e4631de
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361221"
---
# <a name="id3dxeffectstatemanagersetpixelshaderconstantf-method"></a><span data-ttu-id="474b8-103">ID3DXEffectStateManager:: setpixelshaderconstantf-Methode</span><span class="sxs-lookup"><span data-stu-id="474b8-103">ID3DXEffectStateManager::SetPixelShaderConstantF method</span></span>

<span data-ttu-id="474b8-104">Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um ein Array von Vertex-Shader-Gleit Komma Konstanten festzulegen.</span><span class="sxs-lookup"><span data-stu-id="474b8-104">A callback function that must be implemented by a user to set an array of vertex shader floating-point constants.</span></span>

## <a name="syntax"></a><span data-ttu-id="474b8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="474b8-105">Syntax</span></span>


```C++
HRESULT SetPixelShaderConstantF(
  [out]       UINT  StartRegister,
  [out] const FLOAT *pConstantData,
  [out]       UINT  RegisterCount
);
```



## <a name="parameters"></a><span data-ttu-id="474b8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="474b8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="474b8-107">*Startregiester* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="474b8-107">*StartRegister* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="474b8-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="474b8-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="474b8-109">Der null basierte Index des ersten Konstanten Registers.</span><span class="sxs-lookup"><span data-stu-id="474b8-109">The zero-based index of the first constant register.</span></span>

</dd> <dt>

<span data-ttu-id="474b8-110">*pconstantdata* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="474b8-110">*pConstantData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="474b8-111">Typ: Konstante **[**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="474b8-111">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="474b8-112">Ein Array von Gleit Komma Konstanten.</span><span class="sxs-lookup"><span data-stu-id="474b8-112">An array of floating-point constants.</span></span>

</dd> <dt>

<span data-ttu-id="474b8-113">*Register count* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="474b8-113">*RegisterCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="474b8-114">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="474b8-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="474b8-115">Die Anzahl der Register in pconstantdata.</span><span class="sxs-lookup"><span data-stu-id="474b8-115">The number of registers in pConstantData.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="474b8-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="474b8-116">Return value</span></span>

<span data-ttu-id="474b8-117">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="474b8-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="474b8-118">Die vom Benutzer implementierte Methode sollte S \_ OK zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="474b8-118">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="474b8-119">Wenn der Rückruf beim Festlegen des Geräte Zustands fehlschlägt, wird eine der folgenden Aktionen ausgeführt:</span><span class="sxs-lookup"><span data-stu-id="474b8-119">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="474b8-120">Der Effekt schlägt während [**ID3DXEffect:: beginpass**](id3dxeffect--beginpass.md)fehl.</span><span class="sxs-lookup"><span data-stu-id="474b8-120">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="474b8-121">Der dynamische Effekt Zustands Aufrufe (z. b. [**IDirect3DDevice9:: setpixelshaderconstantf**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf)) schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="474b8-121">The dynamic effect state call (such as [**IDirect3DDevice9::SetPixelShaderConstantF**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="474b8-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="474b8-122">Requirements</span></span>



| <span data-ttu-id="474b8-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="474b8-123">Requirement</span></span> | <span data-ttu-id="474b8-124">Wert</span><span class="sxs-lookup"><span data-stu-id="474b8-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="474b8-125">Header</span><span class="sxs-lookup"><span data-stu-id="474b8-125">Header</span></span><br/>  | <dl> <span data-ttu-id="474b8-126"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="474b8-126"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="474b8-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="474b8-127">Library</span></span><br/> | <dl> <span data-ttu-id="474b8-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="474b8-128"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="474b8-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="474b8-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="474b8-130">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="474b8-130">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
