---
description: Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um ein Array von Vertex-Shader-ganzzahligen Konstanten festzulegen.
ms.assetid: 55f5747d-b7f8-4d13-ac2c-df2dcb160091
title: 'ID3DXEffectStateManager:: setpixelshaderconstanti-Methode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetPixelShaderConstantI
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 2e84d883370038435dc59bb948ef94fcd82223db
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106354384"
---
# <a name="id3dxeffectstatemanagersetpixelshaderconstanti-method"></a><span data-ttu-id="2b55f-103">ID3DXEffectStateManager:: setpixelshaderconstanti-Methode</span><span class="sxs-lookup"><span data-stu-id="2b55f-103">ID3DXEffectStateManager::SetPixelShaderConstantI method</span></span>

<span data-ttu-id="2b55f-104">Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um ein Array von Vertex-Shader-ganzzahligen Konstanten festzulegen.</span><span class="sxs-lookup"><span data-stu-id="2b55f-104">A callback function that must be implemented by a user to set an array of vertex shader integer constants.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b55f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2b55f-105">Syntax</span></span>


```C++
HRESULT SetPixelShaderConstantI(
  [out]       UINT StartRegister,
  [out] const INT  *pConstantData,
  [out]       UINT RegisterCount
);
```



## <a name="parameters"></a><span data-ttu-id="2b55f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2b55f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b55f-107">*Startregiester* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="2b55f-107">*StartRegister* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2b55f-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2b55f-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2b55f-109">Der null basierte Index des ersten Konstanten Registers.</span><span class="sxs-lookup"><span data-stu-id="2b55f-109">The zero-based index of the first constant register.</span></span>

</dd> <dt>

<span data-ttu-id="2b55f-110">*pconstantdata* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="2b55f-110">*pConstantData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2b55f-111">Typ: Konstante **[**int**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="2b55f-111">Type: **const [**INT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="2b55f-112">Ein Array von ganzzahligen Konstanten.</span><span class="sxs-lookup"><span data-stu-id="2b55f-112">An array of integer constants.</span></span>

</dd> <dt>

<span data-ttu-id="2b55f-113">*Register count* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="2b55f-113">*RegisterCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2b55f-114">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2b55f-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2b55f-115">Die Anzahl der Register in pconstantdata.</span><span class="sxs-lookup"><span data-stu-id="2b55f-115">The number of registers in pConstantData.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b55f-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2b55f-116">Return value</span></span>

<span data-ttu-id="2b55f-117">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2b55f-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2b55f-118">Die vom Benutzer implementierte Methode sollte S \_ OK zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="2b55f-118">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="2b55f-119">Wenn der Rückruf beim Festlegen des Geräte Zustands fehlschlägt, wird eine der folgenden Aktionen ausgeführt:</span><span class="sxs-lookup"><span data-stu-id="2b55f-119">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="2b55f-120">Der Effekt schlägt während [**ID3DXEffect:: beginpass**](id3dxeffect--beginpass.md)fehl.</span><span class="sxs-lookup"><span data-stu-id="2b55f-120">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="2b55f-121">Der dynamische Effekt Zustands Aufrufe (z. b. [**IDirect3DDevice9:: setpixelshaderconstanti**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstanti)) schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="2b55f-121">The dynamic effect state call (such as [**IDirect3DDevice9::SetPixelShaderConstantI**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstanti)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b55f-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2b55f-122">Requirements</span></span>



| <span data-ttu-id="2b55f-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2b55f-123">Requirement</span></span> | <span data-ttu-id="2b55f-124">Wert</span><span class="sxs-lookup"><span data-stu-id="2b55f-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b55f-125">Header</span><span class="sxs-lookup"><span data-stu-id="2b55f-125">Header</span></span><br/>  | <dl> <span data-ttu-id="2b55f-126"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="2b55f-126"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="2b55f-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2b55f-127">Library</span></span><br/> | <dl> <span data-ttu-id="2b55f-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2b55f-128"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="2b55f-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2b55f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b55f-130">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="2b55f-130">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
