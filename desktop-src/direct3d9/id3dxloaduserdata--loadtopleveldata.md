---
description: Laden von Daten der obersten Ebene aus einer x-Datei.
ms.assetid: 0270b923-d524-46c5-bd1a-44c782722635
title: 'ID3DXLoadUserData:: loadtopleveldata-Methode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLoadUserData.LoadTopLevelData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f52d6853b12b666ab64602711a42c3698d6d8032
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106364003"
---
# <a name="id3dxloaduserdataloadtopleveldata-method"></a><span data-ttu-id="8608f-103">ID3DXLoadUserData:: loadtopleveldata-Methode</span><span class="sxs-lookup"><span data-stu-id="8608f-103">ID3DXLoadUserData::LoadTopLevelData method</span></span>

<span data-ttu-id="8608f-104">Laden von Daten der obersten Ebene aus einer x-Datei.</span><span class="sxs-lookup"><span data-stu-id="8608f-104">Load top level data from a .x file.</span></span>

## <a name="syntax"></a><span data-ttu-id="8608f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8608f-105">Syntax</span></span>


```C++
HRESULT LoadTopLevelData(
  [in] LPD3DXFILEDATA pXofChildData
);
```



## <a name="parameters"></a><span data-ttu-id="8608f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8608f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8608f-107">*pxofchilddata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8608f-107">*pXofChildData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8608f-108">Typ: **[ **LPD3DXFILEDATA**](id3dxfiledata.md)**</span><span class="sxs-lookup"><span data-stu-id="8608f-108">Type: **[**LPD3DXFILEDATA**](id3dxfiledata.md)**</span></span>

<span data-ttu-id="8608f-109">Zeiger auf eine x-Datei Datenstruktur.</span><span class="sxs-lookup"><span data-stu-id="8608f-109">Pointer to a .x file data structure.</span></span> <span data-ttu-id="8608f-110">Dies wird in "dxfile. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="8608f-110">This is defined in Dxfile.h.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8608f-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8608f-111">Return value</span></span>

<span data-ttu-id="8608f-112">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8608f-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8608f-113">Die Rückgabewerte dieser Methode werden von einem Anwendungsprogrammierer implementiert.</span><span class="sxs-lookup"><span data-stu-id="8608f-113">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="8608f-114">Wenn kein Fehler auftritt, programmieren Sie im Allgemeinen die-Methode, um D3D OK zurückzugeben \_ .</span><span class="sxs-lookup"><span data-stu-id="8608f-114">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="8608f-115">Andernfalls programmieren Sie die Methode, um eine entsprechende Fehlermeldung von D3DERR oder D3DXERR zurückzugeben, da dies dazu führt, dass [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) ebenfalls fehlschlägt, und gibt den Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="8608f-115">Otherwise, program the method to return an appropriate error message from D3DERR or D3DXERR, as this will cause [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) to fail also, and return the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="8608f-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8608f-116">Requirements</span></span>



| <span data-ttu-id="8608f-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8608f-117">Requirement</span></span> | <span data-ttu-id="8608f-118">Wert</span><span class="sxs-lookup"><span data-stu-id="8608f-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8608f-119">Header</span><span class="sxs-lookup"><span data-stu-id="8608f-119">Header</span></span><br/>  | <dl> <span data-ttu-id="8608f-120"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="8608f-120"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="8608f-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8608f-121">Library</span></span><br/> | <dl> <span data-ttu-id="8608f-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8608f-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8608f-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8608f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8608f-124">ID3DXLoadUserData</span><span class="sxs-lookup"><span data-stu-id="8608f-124">ID3DXLoadUserData</span></span>](id3dxloaduserdata.md)
</dt> </dl>

 

 




