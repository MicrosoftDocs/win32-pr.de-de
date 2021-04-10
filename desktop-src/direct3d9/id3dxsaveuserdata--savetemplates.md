---
description: Ein Rückruf für den Benutzer zum Speichern einer x-Datei Vorlage.
ms.assetid: c2e29495-5eeb-42b8-826e-1a60c1c6bda2
title: 'ID3DXSaveUserData:: savetemplates-Methode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSaveUserData.SaveTemplates
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 92040629b1b21cbfa1219eee237e357aa056b473
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961750"
---
# <a name="id3dxsaveuserdatasavetemplates-method"></a><span data-ttu-id="4bba8-103">ID3DXSaveUserData:: savetemplates-Methode</span><span class="sxs-lookup"><span data-stu-id="4bba8-103">ID3DXSaveUserData::SaveTemplates method</span></span>

<span data-ttu-id="4bba8-104">Ein Rückruf für den Benutzer zum Speichern einer x-Datei Vorlage.</span><span class="sxs-lookup"><span data-stu-id="4bba8-104">A callback for the user to save a .x file template.</span></span>

## <a name="syntax"></a><span data-ttu-id="4bba8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4bba8-105">Syntax</span></span>


```C++
HRESULT SaveTemplates(
  [in] LPD3DXFILESAVEOBJECT pXofSave
);
```



## <a name="parameters"></a><span data-ttu-id="4bba8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4bba8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4bba8-107">*pxofsave* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4bba8-107">*pXofSave* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4bba8-108">Typ: **[ **LPD3DXFILESAVEOBJECT**](id3dxfilesaveobject.md)**</span><span class="sxs-lookup"><span data-stu-id="4bba8-108">Type: **[**LPD3DXFILESAVEOBJECT**](id3dxfilesaveobject.md)**</span></span>

<span data-ttu-id="4bba8-109">Zeiger auf ein x-Dateispeicher Objekt.</span><span class="sxs-lookup"><span data-stu-id="4bba8-109">Pointer to a .x file save object.</span></span> <span data-ttu-id="4bba8-110">Verwenden Sie diesen Parameter nicht zum Hinzufügen von Datenobjekten.</span><span class="sxs-lookup"><span data-stu-id="4bba8-110">Do not use this parameter to add data objects.</span></span> <span data-ttu-id="4bba8-111">Siehe [**ID3DXFileSaveObject**](id3dxfilesaveobject.md).</span><span class="sxs-lookup"><span data-stu-id="4bba8-111">See [**ID3DXFileSaveObject**](id3dxfilesaveobject.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4bba8-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4bba8-112">Return value</span></span>

<span data-ttu-id="4bba8-113">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4bba8-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4bba8-114">Die Rückgabewerte dieser Methode werden von einem Anwendungsprogrammierer implementiert.</span><span class="sxs-lookup"><span data-stu-id="4bba8-114">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="4bba8-115">Wenn kein Fehler auftritt, programmieren Sie im Allgemeinen die-Methode, um D3D OK zurückzugeben \_ .</span><span class="sxs-lookup"><span data-stu-id="4bba8-115">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="4bba8-116">Andernfalls programmieren Sie die Methode, um eine entsprechende Fehlermeldung von [D3DERR](d3derr.md) oder [**D3DXERR**](./d3dxerr.md)zurückzugeben, da dies dazu führt, dass [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) ebenfalls fehlschlägt, und gibt den Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="4bba8-116">Otherwise, program the method to return an appropriate error message from [D3DERR](d3derr.md) or [**D3DXERR**](./d3dxerr.md), as this will cause [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) to fail also, and return the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="4bba8-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4bba8-117">Remarks</span></span>

<span data-ttu-id="4bba8-118">[**ID3DXSaveUserData:: registertemplates**](id3dxsaveuserdata--registertemplates.md) und **ID3DXSaveUserData:: savetemplates** bieten einen Mechanismus zum Hinzufügen einer Vorlage zu einer x-Datei zum Speichern von Benutzerdaten.</span><span class="sxs-lookup"><span data-stu-id="4bba8-118">[**ID3DXSaveUserData::RegisterTemplates**](id3dxsaveuserdata--registertemplates.md) and **ID3DXSaveUserData::SaveTemplates** provide a mechanism for adding a template to a .x file for saving user data.</span></span>

## <a name="requirements"></a><span data-ttu-id="4bba8-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4bba8-119">Requirements</span></span>



| <span data-ttu-id="4bba8-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4bba8-120">Requirement</span></span> | <span data-ttu-id="4bba8-121">Wert</span><span class="sxs-lookup"><span data-stu-id="4bba8-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4bba8-122">Header</span><span class="sxs-lookup"><span data-stu-id="4bba8-122">Header</span></span><br/>  | <dl> <span data-ttu-id="4bba8-123"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="4bba8-123"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="4bba8-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4bba8-124">Library</span></span><br/> | <dl> <span data-ttu-id="4bba8-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4bba8-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4bba8-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4bba8-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bba8-127">ID3DXSaveUserData</span><span class="sxs-lookup"><span data-stu-id="4bba8-127">ID3DXSaveUserData</span></span>](id3dxsaveuserdata.md)
</dt> </dl>

 

 
