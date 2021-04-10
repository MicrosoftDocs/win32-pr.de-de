---
description: Extrahiert Koeffizient Daten aus einem Farbkanal des Puffers für einen angegebenen Bereich von Koeffizienten und fügt die Daten einem IDirect3DTexture9-Objekt hinzu.
ms.assetid: 75854676-706a-4675-857e-4f2f8fc8365b
title: 'ID3DXPRTBuffer:: extracttexture-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.ExtractTexture
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2ea6cfdc8fb6ec83f847ccf37d06972974ea4de8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961652"
---
# <a name="id3dxprtbufferextracttexture-method"></a><span data-ttu-id="887ac-103">ID3DXPRTBuffer:: extracttexture-Methode</span><span class="sxs-lookup"><span data-stu-id="887ac-103">ID3DXPRTBuffer::ExtractTexture method</span></span>

<span data-ttu-id="887ac-104">Extrahiert Koeffizient Daten aus einem Farbkanal des Puffers für einen angegebenen Bereich von Koeffizienten und fügt die Daten einem [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) -Objekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="887ac-104">Extracts coefficient data from a color channel of the buffer for a specified range of coefficients, and adds the data to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="887ac-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="887ac-105">Syntax</span></span>


```C++
HRESULT ExtractTexture(
  [in] UINT               Channel,
  [in] UINT               StartCoefficient,
  [in] UINT               NumCoefficients,
  [in] LPDIRECT3DTEXTURE9 pTexture
);
```



## <a name="parameters"></a><span data-ttu-id="887ac-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="887ac-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="887ac-107">*Channel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="887ac-107">*Channel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="887ac-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="887ac-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="887ac-109">Der Puffer Farbkanal, von dem Textur Daten extrahiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="887ac-109">Buffer color channel from which to extract texture data.</span></span>

</dd> <dt>

<span data-ttu-id="887ac-110">*Startkoeffizienten* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="887ac-110">*StartCoefficient* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="887ac-111">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="887ac-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="887ac-112">Startwert des Puffer Koeffizienten, von dem Textur Daten extrahiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="887ac-112">Starting value of the buffer coefficient from which to extract texture data.</span></span>

</dd> <dt>

<span data-ttu-id="887ac-113">*Numkoefficients* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="887ac-113">*NumCoefficients* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="887ac-114">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="887ac-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="887ac-115">Anzahl von skalaren, beginnend bei startkoeffizienten, aus denen Textur Daten extrahiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="887ac-115">Number of scalars, beginning at StartCoefficient, from which to extract texture data.</span></span>

</dd> <dt>

<span data-ttu-id="887ac-116">*ptexture* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="887ac-116">*pTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="887ac-117">Typ: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="887ac-117">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="887ac-118">Zeiger auf ein [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) -Textur Objekt, in dem Koeffizienten gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="887ac-118">Pointer to a [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) texture object that will store coefficients.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="887ac-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="887ac-119">Return value</span></span>

<span data-ttu-id="887ac-120">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="887ac-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="887ac-121">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="887ac-121">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="887ac-122">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ outo fmemory.</span><span class="sxs-lookup"><span data-stu-id="887ac-122">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="887ac-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="887ac-123">Requirements</span></span>



| <span data-ttu-id="887ac-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="887ac-124">Requirement</span></span> | <span data-ttu-id="887ac-125">Wert</span><span class="sxs-lookup"><span data-stu-id="887ac-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="887ac-126">Header</span><span class="sxs-lookup"><span data-stu-id="887ac-126">Header</span></span><br/>  | <dl> <span data-ttu-id="887ac-127"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="887ac-127"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="887ac-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="887ac-128">Library</span></span><br/> | <dl> <span data-ttu-id="887ac-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="887ac-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="887ac-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="887ac-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="887ac-131">ID3DXPRTBuffer</span><span class="sxs-lookup"><span data-stu-id="887ac-131">ID3DXPRTBuffer</span></span>](id3dxprtbuffer.md)
</dt> </dl>

 

 
