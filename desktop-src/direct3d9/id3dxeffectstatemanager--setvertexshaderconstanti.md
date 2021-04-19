---
description: Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um ein Array von Vertex-Shader-ganzzahligen Konstanten festzulegen.
ms.assetid: 0035c97a-1b17-4665-9032-7b3b9a9d2cff
title: 'ID3DXEffectStateManager:: setvertexshaderconstanti-Methode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetVertexShaderConstantI
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: be95d678ee6b0c44dc49e180df4d3332a84d5fe7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361877"
---
# <a name="id3dxeffectstatemanagersetvertexshaderconstanti-method"></a><span data-ttu-id="41a33-103">ID3DXEffectStateManager:: setvertexshaderconstanti-Methode</span><span class="sxs-lookup"><span data-stu-id="41a33-103">ID3DXEffectStateManager::SetVertexShaderConstantI method</span></span>

<span data-ttu-id="41a33-104">Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um ein Array von Vertex-Shader-ganzzahligen Konstanten festzulegen.</span><span class="sxs-lookup"><span data-stu-id="41a33-104">A callback function that must be implemented by a user to set an array of vertex shader integer constants.</span></span>

## <a name="syntax"></a><span data-ttu-id="41a33-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="41a33-105">Syntax</span></span>


```C++
HRESULT SetVertexShaderConstantI(
  [out]       UINT StartRegister,
  [out] const INT  *pConstantData,
  [out]       UINT RegisterCount
);
```



## <a name="parameters"></a><span data-ttu-id="41a33-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="41a33-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41a33-107">*Startregiester* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="41a33-107">*StartRegister* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="41a33-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="41a33-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="41a33-109">Der null basierte Index des ersten Konstanten Registers.</span><span class="sxs-lookup"><span data-stu-id="41a33-109">The zero-based index of the first constant register.</span></span>

</dd> <dt>

<span data-ttu-id="41a33-110">*pconstantdata* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="41a33-110">*pConstantData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="41a33-111">Typ: Konstante **[**int**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="41a33-111">Type: **const [**INT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="41a33-112">Ein Array von ganzzahligen Konstanten.</span><span class="sxs-lookup"><span data-stu-id="41a33-112">An array of integer constants.</span></span>

</dd> <dt>

<span data-ttu-id="41a33-113">*Register count* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="41a33-113">*RegisterCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="41a33-114">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="41a33-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="41a33-115">Die Anzahl der Register in pconstantdata.</span><span class="sxs-lookup"><span data-stu-id="41a33-115">The number of registers in pConstantData.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41a33-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="41a33-116">Return value</span></span>

<span data-ttu-id="41a33-117">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="41a33-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="41a33-118">Die vom Benutzer implementierte Methode sollte S \_ OK zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="41a33-118">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="41a33-119">Wenn der Rückruf beim Festlegen des Geräte Zustands fehlschlägt, wird eine der folgenden Aktionen ausgeführt:</span><span class="sxs-lookup"><span data-stu-id="41a33-119">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="41a33-120">Der Effekt schlägt während [**ID3DXEffect:: beginpass**](id3dxeffect--beginpass.md)fehl.</span><span class="sxs-lookup"><span data-stu-id="41a33-120">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="41a33-121">Der dynamische Effekt Zustands Aufrufe (z. b. [**IDirect3DDevice9:: setvertexshaderconstanti**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstanti)) schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="41a33-121">The dynamic effect state call (such as [**IDirect3DDevice9::SetVertexShaderConstantI**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstanti)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="41a33-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="41a33-122">Requirements</span></span>



| <span data-ttu-id="41a33-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="41a33-123">Requirement</span></span> | <span data-ttu-id="41a33-124">Wert</span><span class="sxs-lookup"><span data-stu-id="41a33-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="41a33-125">Header</span><span class="sxs-lookup"><span data-stu-id="41a33-125">Header</span></span><br/>  | <dl> <span data-ttu-id="41a33-126"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="41a33-126"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="41a33-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="41a33-127">Library</span></span><br/> | <dl> <span data-ttu-id="41a33-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="41a33-128"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="41a33-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="41a33-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41a33-130">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="41a33-130">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
