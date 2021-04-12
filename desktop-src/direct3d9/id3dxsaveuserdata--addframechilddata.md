---
description: Fügen Sie dem Frame untergeordnete Daten hinzu.
ms.assetid: b1e02b2a-628f-49c3-a81c-0e96ba0d5f4a
title: 'ID3DXSaveUserData:: addframechilddata-Methode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSaveUserData.AddFrameChildData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3e3017ec2dafa9d4188da4f50d14257a09ffe72f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219686"
---
# <a name="id3dxsaveuserdataaddframechilddata-method"></a><span data-ttu-id="f97d6-103">ID3DXSaveUserData:: addframechilddata-Methode</span><span class="sxs-lookup"><span data-stu-id="f97d6-103">ID3DXSaveUserData::AddFrameChildData method</span></span>

<span data-ttu-id="f97d6-104">Fügen Sie dem Frame untergeordnete Daten hinzu.</span><span class="sxs-lookup"><span data-stu-id="f97d6-104">Add child data to the frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="f97d6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f97d6-105">Syntax</span></span>


```C++
HRESULT AddFrameChildData(
  [in] const D3DXFRAME            *pFrame,
  [in]       LPD3DXFILESAVEOBJECT pXofSave,
  [in]       LPD3DXFileSaveData   pXofFrameData
);
```



## <a name="parameters"></a><span data-ttu-id="f97d6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f97d6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f97d6-107">*pFrame* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f97d6-107">*pFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f97d6-108">Typ: **Konstanten [**D3DXFRAME**](d3dxframe.md) \***</span><span class="sxs-lookup"><span data-stu-id="f97d6-108">Type: **const [**D3DXFRAME**](d3dxframe.md)\***</span></span>

<span data-ttu-id="f97d6-109">Zeiger auf einen Mesh-Container.</span><span class="sxs-lookup"><span data-stu-id="f97d6-109">Pointer to a mesh container.</span></span> <span data-ttu-id="f97d6-110">Siehe [**D3DXFRAME**](d3dxframe.md).</span><span class="sxs-lookup"><span data-stu-id="f97d6-110">See [**D3DXFRAME**](d3dxframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="f97d6-111">*pxofsave* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f97d6-111">*pXofSave* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f97d6-112">Typ: **[ **LPD3DXFILESAVEOBJECT**](id3dxfilesaveobject.md)**</span><span class="sxs-lookup"><span data-stu-id="f97d6-112">Type: **[**LPD3DXFILESAVEOBJECT**](id3dxfilesaveobject.md)**</span></span>

<span data-ttu-id="f97d6-113">Zeiger auf ein x-Dateispeicher Objekt.</span><span class="sxs-lookup"><span data-stu-id="f97d6-113">Pointer to a .x file save object.</span></span> <span data-ttu-id="f97d6-114">Verwenden Sie den Zeiger, um [**ID3DXFileSaveObject:: adddataobject**](id3dxfilesaveobject--adddataobject.md) aufzurufen, um ein untergeordnetes Datenobjekt hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="f97d6-114">Use the pointer to call [**ID3DXFileSaveObject::AddDataObject**](id3dxfilesaveobject--adddataobject.md) to add a child data object.</span></span> <span data-ttu-id="f97d6-115">Speichern Sie die Daten nicht mit [**ID3DXFileSaveObject:: Save**](id3dxfilesaveobject--save.md).</span><span class="sxs-lookup"><span data-stu-id="f97d6-115">Do not save the data with [**ID3DXFileSaveObject::Save**](id3dxfilesaveobject--save.md).</span></span>

</dd> <dt>

<span data-ttu-id="f97d6-116">*pxofframedata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f97d6-116">*pXofFrameData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f97d6-117">Typ: **[ **LPD3DXFileSaveData**](id3dxfilesavedata.md)**</span><span class="sxs-lookup"><span data-stu-id="f97d6-117">Type: **[**LPD3DXFileSaveData**](id3dxfilesavedata.md)**</span></span>

<span data-ttu-id="f97d6-118">Zeiger auf einen x-Datei Datenknoten.</span><span class="sxs-lookup"><span data-stu-id="f97d6-118">Pointer to a .x file data node.</span></span> <span data-ttu-id="f97d6-119">Verwenden Sie den Zeiger, um [**ID3DXFileSaveData:: adddataobject**](id3dxfilesavedata--adddataobject.md) aufzurufen, um ein untergeordnetes Datenobjekt hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="f97d6-119">Use the pointer to call [**ID3DXFileSaveData::AddDataObject**](id3dxfilesavedata--adddataobject.md) to add a child data object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f97d6-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f97d6-120">Return value</span></span>

<span data-ttu-id="f97d6-121">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f97d6-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f97d6-122">Die Rückgabewerte dieser Methode werden von einem Anwendungsprogrammierer implementiert.</span><span class="sxs-lookup"><span data-stu-id="f97d6-122">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="f97d6-123">Wenn kein Fehler auftritt, programmieren Sie im Allgemeinen die-Methode, um D3D OK zurückzugeben \_ .</span><span class="sxs-lookup"><span data-stu-id="f97d6-123">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="f97d6-124">Andernfalls programmieren Sie die Methode, um eine entsprechende Fehlermeldung von [D3DERR](d3derr.md) oder [**D3DXERR**](./d3dxerr.md)zurückzugeben, da dies dazu führt, dass [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) ebenfalls fehlschlägt, und gibt den Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="f97d6-124">Otherwise, program the method to return an appropriate error message from [D3DERR](d3derr.md) or [**D3DXERR**](./d3dxerr.md), as this will cause [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) to fail also, and return the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="f97d6-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f97d6-125">Remarks</span></span>

<span data-ttu-id="f97d6-126">[**ID3DXSaveUserData:: registertemplates**](id3dxsaveuserdata--registertemplates.md) und [**ID3DXSaveUserData:: savetemplates**](id3dxsaveuserdata--savetemplates.md) bieten einen Mechanismus zum Hinzufügen einer Vorlage zu einer x-Datei zum Speichern von Benutzerdaten.</span><span class="sxs-lookup"><span data-stu-id="f97d6-126">[**ID3DXSaveUserData::RegisterTemplates**](id3dxsaveuserdata--registertemplates.md) and [**ID3DXSaveUserData::SaveTemplates**](id3dxsaveuserdata--savetemplates.md) provide a mechanism for adding a template to a .x file for saving user data.</span></span>

## <a name="requirements"></a><span data-ttu-id="f97d6-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f97d6-127">Requirements</span></span>



| <span data-ttu-id="f97d6-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f97d6-128">Requirement</span></span> | <span data-ttu-id="f97d6-129">Wert</span><span class="sxs-lookup"><span data-stu-id="f97d6-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f97d6-130">Header</span><span class="sxs-lookup"><span data-stu-id="f97d6-130">Header</span></span><br/>  | <dl> <span data-ttu-id="f97d6-131"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="f97d6-131"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="f97d6-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f97d6-132">Library</span></span><br/> | <dl> <span data-ttu-id="f97d6-133"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f97d6-133"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f97d6-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f97d6-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f97d6-135">ID3DXSaveUserData</span><span class="sxs-lookup"><span data-stu-id="f97d6-135">ID3DXSaveUserData</span></span>](id3dxsaveuserdata.md)
</dt> </dl>

 

 
