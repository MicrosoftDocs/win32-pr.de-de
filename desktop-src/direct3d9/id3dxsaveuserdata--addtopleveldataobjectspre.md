---
description: Fügen Sie ein Objekt der obersten Ebene vor der Frame Hierarchie hinzu.
ms.assetid: ab4bfc3e-58eb-4de6-b080-8b3392b801bf
title: 'ID3DXSaveUserData:: addtopleveldataobjectspre-Methode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSaveUserData.AddTopLevelDataObjectsPre
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d0194c8c9c6806f96cbe75394e6650ca3e7dc74b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361242"
---
# <a name="id3dxsaveuserdataaddtopleveldataobjectspre-method"></a><span data-ttu-id="0bcf1-103">ID3DXSaveUserData:: addtopleveldataobjectspre-Methode</span><span class="sxs-lookup"><span data-stu-id="0bcf1-103">ID3DXSaveUserData::AddTopLevelDataObjectsPre method</span></span>

<span data-ttu-id="0bcf1-104">Fügen Sie ein Objekt der obersten Ebene vor der Frame Hierarchie hinzu.</span><span class="sxs-lookup"><span data-stu-id="0bcf1-104">Add a top level object before the frame hierarchy.</span></span>

## <a name="syntax"></a><span data-ttu-id="0bcf1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0bcf1-105">Syntax</span></span>


```C++
HRESULT AddTopLevelDataObjectsPre(
  [in] LPD3DXFILESAVEOBJECT pXofSave
);
```



## <a name="parameters"></a><span data-ttu-id="0bcf1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0bcf1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0bcf1-107">*pxofsave* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0bcf1-107">*pXofSave* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0bcf1-108">Typ: **[ **LPD3DXFILESAVEOBJECT**](id3dxfilesaveobject.md)**</span><span class="sxs-lookup"><span data-stu-id="0bcf1-108">Type: **[**LPD3DXFILESAVEOBJECT**](id3dxfilesaveobject.md)**</span></span>

<span data-ttu-id="0bcf1-109">Zeiger auf ein x-Dateispeicher Objekt.</span><span class="sxs-lookup"><span data-stu-id="0bcf1-109">Pointer to a .x file save object.</span></span> <span data-ttu-id="0bcf1-110">Verwenden Sie diesen Zeiger, um [**idirectxfilesaveobject:: kreatedataobject**](idirectxfilesaveobject--createdataobject.md) aufzurufen, um das zu speichernde Datenobjekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0bcf1-110">Use this pointer to call [**IDirectXFileSaveObject::CreateDataObject**](idirectxfilesaveobject--createdataobject.md) to create the data object to be saved.</span></span> <span data-ttu-id="0bcf1-111">Anschließend wird [**idirectxfilesaveobject:: SaveData**](idirectxfilesaveobject--savedata.md) aufgerufen, um die Daten zu speichern.</span><span class="sxs-lookup"><span data-stu-id="0bcf1-111">Then call [**IDirectXFileSaveObject::SaveData**](idirectxfilesaveobject--savedata.md) to save the data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0bcf1-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0bcf1-112">Return value</span></span>

<span data-ttu-id="0bcf1-113">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0bcf1-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0bcf1-114">Die Rückgabewerte dieser Methode werden von einem Anwendungsprogrammierer implementiert.</span><span class="sxs-lookup"><span data-stu-id="0bcf1-114">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="0bcf1-115">Wenn kein Fehler auftritt, programmieren Sie im Allgemeinen die-Methode, um D3D OK zurückzugeben \_ .</span><span class="sxs-lookup"><span data-stu-id="0bcf1-115">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="0bcf1-116">Andernfalls programmieren Sie die Methode, um eine entsprechende Fehlermeldung von [D3DERR](d3derr.md) oder [**D3DXERR**](./d3dxerr.md)zurückzugeben, da dies dazu führt, dass [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) ebenfalls fehlschlägt, und gibt den Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="0bcf1-116">Otherwise, program the method to return an appropriate error message from [D3DERR](d3derr.md) or [**D3DXERR**](./d3dxerr.md), as this will cause [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) to fail also, and return the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="0bcf1-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0bcf1-117">Requirements</span></span>



| <span data-ttu-id="0bcf1-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0bcf1-118">Requirement</span></span> | <span data-ttu-id="0bcf1-119">Wert</span><span class="sxs-lookup"><span data-stu-id="0bcf1-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0bcf1-120">Header</span><span class="sxs-lookup"><span data-stu-id="0bcf1-120">Header</span></span><br/>  | <dl> <span data-ttu-id="0bcf1-121"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="0bcf1-121"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="0bcf1-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0bcf1-122">Library</span></span><br/> | <dl> <span data-ttu-id="0bcf1-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0bcf1-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0bcf1-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0bcf1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bcf1-125">ID3DXSaveUserData</span><span class="sxs-lookup"><span data-stu-id="0bcf1-125">ID3DXSaveUserData</span></span>](id3dxsaveuserdata.md)
</dt> </dl>

 

 
