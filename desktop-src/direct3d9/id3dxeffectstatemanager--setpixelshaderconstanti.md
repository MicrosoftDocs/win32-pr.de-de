---
description: 'ID3DXEffectStateManager::SetPixelShaderConstantI-Methode: Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um ein Array von ganzzahligen Vertexshaderkonstanten festlegen zu können.'
ms.assetid: 55f5747d-b7f8-4d13-ac2c-df2dcb160091
title: ID3DXEffectStateManager::SetPixelShaderConstantI-Methode (D3DX9Effect.h)
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
ms.openlocfilehash: 53eab5993ee737efe866c73a550e6b216edaac3b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090478"
---
# <a name="id3dxeffectstatemanagersetpixelshaderconstanti-method"></a><span data-ttu-id="b7144-103">ID3DXEffectStateManager::SetPixelShaderConstantI-Methode</span><span class="sxs-lookup"><span data-stu-id="b7144-103">ID3DXEffectStateManager::SetPixelShaderConstantI method</span></span>

<span data-ttu-id="b7144-104">Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um ein Array von ganzzahligen Vertex-Shaderkonstten festlegen zu können.</span><span class="sxs-lookup"><span data-stu-id="b7144-104">A callback function that must be implemented by a user to set an array of vertex shader integer constants.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7144-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b7144-105">Syntax</span></span>


```C++
HRESULT SetPixelShaderConstantI(
  [out]       UINT StartRegister,
  [out] const INT  *pConstantData,
  [out]       UINT RegisterCount
);
```



## <a name="parameters"></a><span data-ttu-id="b7144-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b7144-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7144-107">*StartRegister* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b7144-107">*StartRegister* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b7144-108">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b7144-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b7144-109">Der nullbasierte Index des ersten konstanten Registers.</span><span class="sxs-lookup"><span data-stu-id="b7144-109">The zero-based index of the first constant register.</span></span>

</dd> <dt>

<span data-ttu-id="b7144-110">*pConstantData* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b7144-110">*pConstantData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b7144-111">Typ: **const [**INT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="b7144-111">Type: **const [**INT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="b7144-112">Ein Array von ganzzahligen Konstanten.</span><span class="sxs-lookup"><span data-stu-id="b7144-112">An array of integer constants.</span></span>

</dd> <dt>

<span data-ttu-id="b7144-113">*RegisterCount* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b7144-113">*RegisterCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b7144-114">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b7144-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b7144-115">Die Anzahl der Register in pConstantData.</span><span class="sxs-lookup"><span data-stu-id="b7144-115">The number of registers in pConstantData.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7144-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b7144-116">Return value</span></span>

<span data-ttu-id="b7144-117">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b7144-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b7144-118">Die vom Benutzer implementierte Methode sollte S \_ OK zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="b7144-118">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="b7144-119">Wenn der Rückruf beim Festlegen des Gerätestatus fehlschlägt, tritt eine der folgenden Bedingungen auf:</span><span class="sxs-lookup"><span data-stu-id="b7144-119">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="b7144-120">Die Auswirkung tritt während [**ID3DXEffect::BeginPass auf.**](id3dxeffect--beginpass.md)</span><span class="sxs-lookup"><span data-stu-id="b7144-120">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="b7144-121">Der Dynamische Effektzustandsaufruf (z. B. [**IDirect3DDevice9::SetPixelShaderConstantI)**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstanti)tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="b7144-121">The dynamic effect state call (such as [**IDirect3DDevice9::SetPixelShaderConstantI**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstanti)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7144-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b7144-122">Requirements</span></span>



| <span data-ttu-id="b7144-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b7144-123">Requirement</span></span> | <span data-ttu-id="b7144-124">Wert</span><span class="sxs-lookup"><span data-stu-id="b7144-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7144-125">Header</span><span class="sxs-lookup"><span data-stu-id="b7144-125">Header</span></span><br/>  | <dl> <span data-ttu-id="b7144-126"><dt>D3DX9Effect.h</dt></span><span class="sxs-lookup"><span data-stu-id="b7144-126"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="b7144-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b7144-127">Library</span></span><br/> | <dl> <span data-ttu-id="b7144-128"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="b7144-128"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="b7144-129">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b7144-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7144-130">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="b7144-130">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
