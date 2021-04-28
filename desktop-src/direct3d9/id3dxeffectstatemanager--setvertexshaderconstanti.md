---
description: 'ID3DXEffectStateManager::SetVertexShaderConstantI-Methode: Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um ein Array von ganzzahligen Vertexshaderkonstanten festlegen zu können.'
ms.assetid: 0035c97a-1b17-4665-9032-7b3b9a9d2cff
title: ID3DXEffectStateManager::SetVertexShaderConstantI-Methode (D3DX9Effect.h)
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
ms.openlocfilehash: c129e3e01fe6fbae6ba7ede1b9ea8c4bee5338a4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090398"
---
# <a name="id3dxeffectstatemanagersetvertexshaderconstanti-method"></a><span data-ttu-id="92b2e-103">ID3DXEffectStateManager::SetVertexShaderConstantI-Methode</span><span class="sxs-lookup"><span data-stu-id="92b2e-103">ID3DXEffectStateManager::SetVertexShaderConstantI method</span></span>

<span data-ttu-id="92b2e-104">Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um ein Array von ganzzahligen Vertex-Shaderkonstten festlegen zu können.</span><span class="sxs-lookup"><span data-stu-id="92b2e-104">A callback function that must be implemented by a user to set an array of vertex shader integer constants.</span></span>

## <a name="syntax"></a><span data-ttu-id="92b2e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="92b2e-105">Syntax</span></span>


```C++
HRESULT SetVertexShaderConstantI(
  [out]       UINT StartRegister,
  [out] const INT  *pConstantData,
  [out]       UINT RegisterCount
);
```



## <a name="parameters"></a><span data-ttu-id="92b2e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="92b2e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92b2e-107">*StartRegister* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="92b2e-107">*StartRegister* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="92b2e-108">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="92b2e-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="92b2e-109">Der nullbasierte Index des ersten konstanten Registers.</span><span class="sxs-lookup"><span data-stu-id="92b2e-109">The zero-based index of the first constant register.</span></span>

</dd> <dt>

<span data-ttu-id="92b2e-110">*pConstantData* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="92b2e-110">*pConstantData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="92b2e-111">Typ: **const [**INT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="92b2e-111">Type: **const [**INT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="92b2e-112">Ein Array von ganzzahligen Konstanten.</span><span class="sxs-lookup"><span data-stu-id="92b2e-112">An array of integer constants.</span></span>

</dd> <dt>

<span data-ttu-id="92b2e-113">*RegisterCount* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="92b2e-113">*RegisterCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="92b2e-114">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="92b2e-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="92b2e-115">Die Anzahl der Register in pConstantData.</span><span class="sxs-lookup"><span data-stu-id="92b2e-115">The number of registers in pConstantData.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92b2e-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="92b2e-116">Return value</span></span>

<span data-ttu-id="92b2e-117">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="92b2e-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="92b2e-118">Die vom Benutzer implementierte Methode sollte S \_ OK zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="92b2e-118">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="92b2e-119">Wenn der Rückruf beim Festlegen des Gerätestatus fehlschlägt, tritt eine der folgenden Bedingungen auf:</span><span class="sxs-lookup"><span data-stu-id="92b2e-119">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="92b2e-120">Die Auswirkung tritt während [**ID3DXEffect::BeginPass auf.**](id3dxeffect--beginpass.md)</span><span class="sxs-lookup"><span data-stu-id="92b2e-120">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="92b2e-121">Beim Dynamischen Effektzustandsaufruf (z. B. [**IDirect3DDevice9::SetVertexShaderConstantI)**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstanti)tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="92b2e-121">The dynamic effect state call (such as [**IDirect3DDevice9::SetVertexShaderConstantI**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstanti)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="92b2e-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="92b2e-122">Requirements</span></span>



| <span data-ttu-id="92b2e-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="92b2e-123">Requirement</span></span> | <span data-ttu-id="92b2e-124">Wert</span><span class="sxs-lookup"><span data-stu-id="92b2e-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="92b2e-125">Header</span><span class="sxs-lookup"><span data-stu-id="92b2e-125">Header</span></span><br/>  | <dl> <span data-ttu-id="92b2e-126"><dt>D3DX9Effect.h</dt></span><span class="sxs-lookup"><span data-stu-id="92b2e-126"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="92b2e-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="92b2e-127">Library</span></span><br/> | <dl> <span data-ttu-id="92b2e-128"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="92b2e-128"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="92b2e-129">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="92b2e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92b2e-130">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="92b2e-130">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
