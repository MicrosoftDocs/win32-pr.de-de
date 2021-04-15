---
description: Legt einen normalen Vektor für jeden Texttyp in einem Textur Objekt fest. Diese Methode wird verwendet, um Scheitelpunkt normale Vektoren aus einem Mesh (oder interpoliert Vertex-Normale) zu speichern, wenn die pixelbasierte Voraus berechnete Strahlungs Übertragung (PRT) berechnet wird).
ms.assetid: 165a3ef6-c142-4988-b4fb-5aafd8ff11fe
title: 'ID3DXPRTEngine:: setpertexelnormal-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetPerTexelNormal
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5220ad500312792cd158967e9502381f49b0e3e7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394165"
---
# <a name="id3dxprtenginesetpertexelnormal-method"></a><span data-ttu-id="6868a-104">ID3DXPRTEngine:: setpertexelnormal-Methode</span><span class="sxs-lookup"><span data-stu-id="6868a-104">ID3DXPRTEngine::SetPerTexelNormal method</span></span>

<span data-ttu-id="6868a-105">Legt einen normalen Vektor für jeden Texttyp in einem Textur Objekt fest.</span><span class="sxs-lookup"><span data-stu-id="6868a-105">Sets a normal vector for each texel in a texture object.</span></span> <span data-ttu-id="6868a-106">Diese Methode wird verwendet, um Scheitelpunkt normale Vektoren aus einem Mesh (oder interpoliert Vertex-Normale) zu speichern, wenn die pixelbasierte Voraus berechnete Strahlungs Übertragung (PRT) berechnet wird).</span><span class="sxs-lookup"><span data-stu-id="6868a-106">This method is used to store vertex normal vectors from a mesh (or interpolated vertex normals if pixel-based precomputed radiance transfer (PRT) is being computed).</span></span>

## <a name="syntax"></a><span data-ttu-id="6868a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="6868a-107">Syntax</span></span>


```C++
HRESULT SetPerTexelNormal(
  [in] LPDIRECT3DTEXTURE9 pNormalTexture
);
```



## <a name="parameters"></a><span data-ttu-id="6868a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="6868a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6868a-109">*pnormaltexture* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6868a-109">*pNormalTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6868a-110">Typ: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="6868a-110">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="6868a-111">Ein Zeiger auf ein [**IDirect3DTexture9**](/windows/desktop/api) -Textur Objekt, das als eine Objekt Raum normale Zuordnung fungiert, in der normale Vektoren gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="6868a-111">Pointer to an [**IDirect3DTexture9**](/windows/desktop/api) texture object that serves as an object space normal map in which to store normal vectors.</span></span> <span data-ttu-id="6868a-112">Die Textur muss die gleichen Dimensionen wie [**ID3DXPRTBuffer**](id3dxprtbuffer.md) aufweisen und muss signierte Textur Formate speichern können.</span><span class="sxs-lookup"><span data-stu-id="6868a-112">The texture must have the same dimensions as [**ID3DXPRTBuffer**](id3dxprtbuffer.md) and must be able to store signed texture formats.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6868a-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6868a-113">Return value</span></span>

<span data-ttu-id="6868a-114">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6868a-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6868a-115">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6868a-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="6868a-116">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ outo fmemory.</span><span class="sxs-lookup"><span data-stu-id="6868a-116">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="6868a-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6868a-117">Requirements</span></span>



| <span data-ttu-id="6868a-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6868a-118">Requirement</span></span> | <span data-ttu-id="6868a-119">Wert</span><span class="sxs-lookup"><span data-stu-id="6868a-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6868a-120">Header</span><span class="sxs-lookup"><span data-stu-id="6868a-120">Header</span></span><br/>  | <dl> <span data-ttu-id="6868a-121"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="6868a-121"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="6868a-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6868a-122">Library</span></span><br/> | <dl> <span data-ttu-id="6868a-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6868a-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6868a-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6868a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6868a-125">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="6868a-125">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 
