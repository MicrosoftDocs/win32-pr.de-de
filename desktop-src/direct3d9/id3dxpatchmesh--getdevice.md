---
description: Ruft das Gerät ab, das das Mesh erstellt hat.
ms.assetid: b03dadda-ca54-4a55-a0a5-cf5ccdb55a72
title: 'ID3DXPatchMesh:: getdevice-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.GetDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a026398b719bf3ba9a9c02082105cbc7dd299013
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961738"
---
# <a name="id3dxpatchmeshgetdevice-method"></a><span data-ttu-id="99b84-103">ID3DXPatchMesh:: getdevice-Methode</span><span class="sxs-lookup"><span data-stu-id="99b84-103">ID3DXPatchMesh::GetDevice method</span></span>

<span data-ttu-id="99b84-104">Ruft das Gerät ab, das das Mesh erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="99b84-104">Gets the device that created the mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="99b84-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="99b84-105">Syntax</span></span>


```C++
HRESULT GetDevice(
  [out] LPDIRECT3DDEVICE9 *ppDevice
);
```



## <a name="parameters"></a><span data-ttu-id="99b84-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="99b84-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99b84-107">*ppdevice* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="99b84-107">*ppDevice* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="99b84-108">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span><span class="sxs-lookup"><span data-stu-id="99b84-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span></span>

<span data-ttu-id="99b84-109">Zeiger auf das Gerät.</span><span class="sxs-lookup"><span data-stu-id="99b84-109">Pointer to the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99b84-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="99b84-110">Return value</span></span>

<span data-ttu-id="99b84-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="99b84-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="99b84-112">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="99b84-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="99b84-113">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ outo fmemory.</span><span class="sxs-lookup"><span data-stu-id="99b84-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="99b84-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="99b84-114">Requirements</span></span>



| <span data-ttu-id="99b84-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="99b84-115">Requirement</span></span> | <span data-ttu-id="99b84-116">Wert</span><span class="sxs-lookup"><span data-stu-id="99b84-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="99b84-117">Header</span><span class="sxs-lookup"><span data-stu-id="99b84-117">Header</span></span><br/>  | <dl> <span data-ttu-id="99b84-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="99b84-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="99b84-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="99b84-119">Library</span></span><br/> | <dl> <span data-ttu-id="99b84-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="99b84-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="99b84-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="99b84-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99b84-122">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="99b84-122">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 
