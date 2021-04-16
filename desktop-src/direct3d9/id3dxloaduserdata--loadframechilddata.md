---
description: Laden von untergeordneten Frame-Daten aus einer x-Datei.
ms.assetid: 79d251f3-c661-42e3-9385-84aabd58fd4f
title: 'ID3DXLoadUserData:: loadframechilddata-Methode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLoadUserData.LoadFrameChildData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 53bde98f0e756fd1baff4c509179f15e8489e74f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104531058"
---
# <a name="id3dxloaduserdataloadframechilddata-method"></a><span data-ttu-id="9a80a-103">ID3DXLoadUserData:: loadframechilddata-Methode</span><span class="sxs-lookup"><span data-stu-id="9a80a-103">ID3DXLoadUserData::LoadFrameChildData method</span></span>

<span data-ttu-id="9a80a-104">Laden von untergeordneten Frame-Daten aus einer x-Datei.</span><span class="sxs-lookup"><span data-stu-id="9a80a-104">Load frame child data from a .x file.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a80a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9a80a-105">Syntax</span></span>


```C++
HRESULT LoadFrameChildData(
  [in] LPD3DXFRAME    pFrame,
  [in] LPD3DXFILEDATA pXofChildData
);
```



## <a name="parameters"></a><span data-ttu-id="9a80a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9a80a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a80a-107">*pFrame* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9a80a-107">*pFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a80a-108">Typ: **[ **LPD3DXFRAME**](d3dxframe.md)**</span><span class="sxs-lookup"><span data-stu-id="9a80a-108">Type: **[**LPD3DXFRAME**](d3dxframe.md)**</span></span>

<span data-ttu-id="9a80a-109">Zeiger auf einen Mesh-Container.</span><span class="sxs-lookup"><span data-stu-id="9a80a-109">Pointer to a mesh container.</span></span> <span data-ttu-id="9a80a-110">Siehe [**D3DXFRAME**](d3dxframe.md).</span><span class="sxs-lookup"><span data-stu-id="9a80a-110">See [**D3DXFRAME**](d3dxframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="9a80a-111">*pxofchilddata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9a80a-111">*pXofChildData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a80a-112">Typ: **[ **LPD3DXFILEDATA**](id3dxfiledata.md)**</span><span class="sxs-lookup"><span data-stu-id="9a80a-112">Type: **[**LPD3DXFILEDATA**](id3dxfiledata.md)**</span></span>

<span data-ttu-id="9a80a-113">Zeiger auf eine x-Datei Datenstruktur.</span><span class="sxs-lookup"><span data-stu-id="9a80a-113">Pointer to a .x file data structure.</span></span> <span data-ttu-id="9a80a-114">Dies wird in "dxfile. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="9a80a-114">This is defined in Dxfile.h.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a80a-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9a80a-115">Return value</span></span>

<span data-ttu-id="9a80a-116">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9a80a-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9a80a-117">Die Rückgabewerte dieser Methode werden von einem Anwendungsprogrammierer implementiert.</span><span class="sxs-lookup"><span data-stu-id="9a80a-117">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="9a80a-118">Wenn kein Fehler auftritt, programmieren Sie im Allgemeinen die-Methode, um D3D OK zurückzugeben \_ .</span><span class="sxs-lookup"><span data-stu-id="9a80a-118">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="9a80a-119">Andernfalls programmieren Sie die Methode, um eine entsprechende Fehlermeldung von D3DERR oder D3DXERR zurückzugeben, da dies dazu führt, dass [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) ebenfalls fehlschlägt, und gibt den Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="9a80a-119">Otherwise, program the method to return an appropriate error message from D3DERR or D3DXERR, as this will cause [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) to fail also, and return the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a80a-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9a80a-120">Requirements</span></span>



| <span data-ttu-id="9a80a-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9a80a-121">Requirement</span></span> | <span data-ttu-id="9a80a-122">Wert</span><span class="sxs-lookup"><span data-stu-id="9a80a-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9a80a-123">Header</span><span class="sxs-lookup"><span data-stu-id="9a80a-123">Header</span></span><br/>  | <dl> <span data-ttu-id="9a80a-124"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="9a80a-124"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="9a80a-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9a80a-125">Library</span></span><br/> | <dl> <span data-ttu-id="9a80a-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9a80a-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9a80a-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9a80a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a80a-128">ID3DXLoadUserData</span><span class="sxs-lookup"><span data-stu-id="9a80a-128">ID3DXLoadUserData</span></span>](id3dxloaduserdata.md)
</dt> </dl>

 

 




