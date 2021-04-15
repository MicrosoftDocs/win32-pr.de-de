---
description: Ruft die maximalen Gesichts Einflüsse in einem Dreiecks Mesh mit dem angegebenen Index Puffer ab.
ms.assetid: 72dc2440-87df-461e-80d0-9ad9b1e4d8ee
title: 'ID3DXSkinInfo:: getmaxfaceingefluences-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetMaxFaceInfluences
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 11724c50d5224f0bcb2c9ced25523b869f3e347f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394046"
---
# <a name="id3dxskininfogetmaxfaceinfluences-method"></a><span data-ttu-id="e7882-103">ID3DXSkinInfo:: getmaxfaceingefluences-Methode</span><span class="sxs-lookup"><span data-stu-id="e7882-103">ID3DXSkinInfo::GetMaxFaceInfluences method</span></span>

<span data-ttu-id="e7882-104">Ruft die maximalen Gesichts Einflüsse in einem Dreiecks Mesh mit dem angegebenen Index Puffer ab.</span><span class="sxs-lookup"><span data-stu-id="e7882-104">Gets the maximum face influences in a triangle mesh with the specified index buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7882-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e7882-105">Syntax</span></span>


```C++
HRESULT GetMaxFaceInfluences(
  [in] LPDIRECT3DINDEXBUFFER9 pIB,
  [in] DWORD                  NumFaces,
  [in] DWORD                  *maxFaceInfluences
);
```



## <a name="parameters"></a><span data-ttu-id="e7882-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e7882-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7882-107">*PIB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e7882-107">*pIB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7882-108">Typ: **[ **LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)**</span><span class="sxs-lookup"><span data-stu-id="e7882-108">Type: **[**LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)**</span></span>

<span data-ttu-id="e7882-109">Zeiger auf den Index Puffer, der die Mesh-Indexdaten enthält.</span><span class="sxs-lookup"><span data-stu-id="e7882-109">Pointer to the index buffer that contains the mesh index data.</span></span>

</dd> <dt>

<span data-ttu-id="e7882-110">*Numerische Werte* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e7882-110">*NumFaces* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7882-111">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e7882-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e7882-112">Anzahl der Gesichter im Mesh.</span><span class="sxs-lookup"><span data-stu-id="e7882-112">Number of faces in the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="e7882-113">*maxfacetten* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e7882-113">*maxFaceInfluences* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7882-114">Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="e7882-114">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="e7882-115">Zeiger auf die maximalen Gesichts Einflüsse.</span><span class="sxs-lookup"><span data-stu-id="e7882-115">Pointer to the maximum face influences.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7882-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e7882-116">Return value</span></span>

<span data-ttu-id="e7882-117">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e7882-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e7882-118">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e7882-118">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e7882-119">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="e7882-119">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7882-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e7882-120">Requirements</span></span>



| <span data-ttu-id="e7882-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e7882-121">Requirement</span></span> | <span data-ttu-id="e7882-122">Wert</span><span class="sxs-lookup"><span data-stu-id="e7882-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e7882-123">Header</span><span class="sxs-lookup"><span data-stu-id="e7882-123">Header</span></span><br/>  | <dl> <span data-ttu-id="e7882-124"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7882-124"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="e7882-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e7882-125">Library</span></span><br/> | <dl> <span data-ttu-id="e7882-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e7882-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e7882-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e7882-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7882-128">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="e7882-128">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> </dl>

 

 
