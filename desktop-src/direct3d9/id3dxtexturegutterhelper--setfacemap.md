---
description: Legt den Index des Mesh-Blatts fest, zu dem die einzelnen textengehören.
ms.assetid: 45d931bc-fb8b-48da-b30d-99d5dc183494
title: 'ID3DXTextureGutterHelper:: setfacemap-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.SetFaceMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8ba0472052d5e2e06d759c83a404a197ecda148f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219657"
---
# <a name="id3dxtexturegutterhelpersetfacemap-method"></a><span data-ttu-id="8ac90-103">ID3DXTextureGutterHelper:: setfacemap-Methode</span><span class="sxs-lookup"><span data-stu-id="8ac90-103">ID3DXTextureGutterHelper::SetFaceMap method</span></span>

<span data-ttu-id="8ac90-104">Legt den Index des Mesh-Blatts fest, zu dem die einzelnen textengehören.</span><span class="sxs-lookup"><span data-stu-id="8ac90-104">Sets the index of the mesh face to which each texel belongs.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ac90-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8ac90-105">Syntax</span></span>


```C++
HRESULT SetFaceMap(
  [in] UINT *pFaceData
);
```



## <a name="parameters"></a><span data-ttu-id="8ac90-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8ac90-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ac90-107">*pfacedata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8ac90-107">*pFaceData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ac90-108">Typ: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="8ac90-108">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="8ac90-109">Zeiger auf den Index der Mesh-Seite, zu der jeder textexgehört.</span><span class="sxs-lookup"><span data-stu-id="8ac90-109">Pointer to the index of the mesh face to which each texel belongs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ac90-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8ac90-110">Return value</span></span>

<span data-ttu-id="8ac90-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8ac90-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8ac90-112">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8ac90-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="8ac90-113">Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben. D3DERR \_ invalidcall</span><span class="sxs-lookup"><span data-stu-id="8ac90-113">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="8ac90-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8ac90-114">Remarks</span></span>

<span data-ttu-id="8ac90-115">Die Dateneingabe für das Gitter Gesicht für diese Methode ist nur gültig für gültige Texels (nicht Class 0).</span><span class="sxs-lookup"><span data-stu-id="8ac90-115">The mesh face data input to this method is valid only for valid (non-class 0) texels.</span></span> <span data-ttu-id="8ac90-116">[**ID3DXTextureGutterHelper:: getguttermap**](id3dxtexturegutterhelper--getguttermap.md) gibt Werte ungleich 0 (null) für gültige Texels zurück.</span><span class="sxs-lookup"><span data-stu-id="8ac90-116">[**ID3DXTextureGutterHelper::GetGutterMap**](id3dxtexturegutterhelper--getguttermap.md) will return non-zero values for valid texels.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ac90-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8ac90-117">Requirements</span></span>



| <span data-ttu-id="8ac90-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8ac90-118">Requirement</span></span> | <span data-ttu-id="8ac90-119">Wert</span><span class="sxs-lookup"><span data-stu-id="8ac90-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8ac90-120">Header</span><span class="sxs-lookup"><span data-stu-id="8ac90-120">Header</span></span><br/>  | <dl> <span data-ttu-id="8ac90-121"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="8ac90-121"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="8ac90-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8ac90-122">Library</span></span><br/> | <dl> <span data-ttu-id="8ac90-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8ac90-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8ac90-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8ac90-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ac90-125">ID3DXTextureGutterHelper</span><span class="sxs-lookup"><span data-stu-id="8ac90-125">ID3DXTextureGutterHelper</span></span>](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 
