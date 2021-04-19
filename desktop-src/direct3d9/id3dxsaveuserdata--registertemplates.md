---
description: Ein Rückruf für den Benutzer zum Registrieren einer x-Datei Vorlage.
ms.assetid: 60568556-704c-4be3-bbde-04887583cf70
title: 'ID3DXSaveUserData:: registertemplates-Methode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSaveUserData.RegisterTemplates
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c1465b76b758f6a5ed9e7dff4c7126935fb7c5d1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355837"
---
# <a name="id3dxsaveuserdataregistertemplates-method"></a><span data-ttu-id="e0e11-103">ID3DXSaveUserData:: registertemplates-Methode</span><span class="sxs-lookup"><span data-stu-id="e0e11-103">ID3DXSaveUserData::RegisterTemplates method</span></span>

<span data-ttu-id="e0e11-104">Ein Rückruf für den Benutzer zum Registrieren einer x-Datei Vorlage.</span><span class="sxs-lookup"><span data-stu-id="e0e11-104">A callback for the user to register a .x file template.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0e11-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e0e11-105">Syntax</span></span>


```C++
HRESULT RegisterTemplates(
  [in] LPD3DXFILE pXFileApi
);
```



## <a name="parameters"></a><span data-ttu-id="e0e11-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e0e11-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0e11-107">*pxfileapi* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e0e11-107">*pXFileApi* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0e11-108">Typ: **[ **LPD3DXFILE**](id3dxfile.md)**</span><span class="sxs-lookup"><span data-stu-id="e0e11-108">Type: **[**LPD3DXFILE**](id3dxfile.md)**</span></span>

<span data-ttu-id="e0e11-109">Verwenden Sie diesen Zeiger, um benutzerdefinierte x-Datei Vorlagen zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="e0e11-109">Use this pointer to register user-defined .x file templates.</span></span> <span data-ttu-id="e0e11-110">Siehe [**ID3DXFile**](id3dxfile.md).</span><span class="sxs-lookup"><span data-stu-id="e0e11-110">See [**ID3DXFile**](id3dxfile.md).</span></span> <span data-ttu-id="e0e11-111">Verwenden Sie diesen Parameter nicht zum Hinzufügen von Datenobjekten.</span><span class="sxs-lookup"><span data-stu-id="e0e11-111">Do not use this parameter to add data objects.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0e11-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e0e11-112">Return value</span></span>

<span data-ttu-id="e0e11-113">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e0e11-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e0e11-114">Die Rückgabewerte dieser Methode werden von einem Anwendungsprogrammierer implementiert.</span><span class="sxs-lookup"><span data-stu-id="e0e11-114">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="e0e11-115">Wenn kein Fehler auftritt, programmieren Sie im Allgemeinen die-Methode, um D3D OK zurückzugeben \_ .</span><span class="sxs-lookup"><span data-stu-id="e0e11-115">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="e0e11-116">Andernfalls programmieren Sie die Methode, um eine entsprechende Fehlermeldung von [D3DERR](d3derr.md) oder [**D3DXERR**](./d3dxerr.md)zurückzugeben, da dies dazu führt, dass [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) ebenfalls fehlschlägt, und gibt den Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="e0e11-116">Otherwise, program the method to return an appropriate error message from [D3DERR](d3derr.md) or [**D3DXERR**](./d3dxerr.md), as this will cause [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) to fail also, and return the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0e11-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e0e11-117">Remarks</span></span>

<span data-ttu-id="e0e11-118">**ID3DXSaveUserData:: registertemplates** und [**ID3DXSaveUserData:: savetemplates**](id3dxsaveuserdata--savetemplates.md) bieten einen Mechanismus zum Hinzufügen einer Vorlage zu einer x-Datei zum Speichern von Benutzerdaten.</span><span class="sxs-lookup"><span data-stu-id="e0e11-118">**ID3DXSaveUserData::RegisterTemplates** and [**ID3DXSaveUserData::SaveTemplates**](id3dxsaveuserdata--savetemplates.md) provide a mechanism for adding a template to a .x file for saving user data.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0e11-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e0e11-119">Requirements</span></span>



| <span data-ttu-id="e0e11-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e0e11-120">Requirement</span></span> | <span data-ttu-id="e0e11-121">Wert</span><span class="sxs-lookup"><span data-stu-id="e0e11-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e0e11-122">Header</span><span class="sxs-lookup"><span data-stu-id="e0e11-122">Header</span></span><br/>  | <dl> <span data-ttu-id="e0e11-123"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0e11-123"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="e0e11-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e0e11-124">Library</span></span><br/> | <dl> <span data-ttu-id="e0e11-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e0e11-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e0e11-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e0e11-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0e11-127">ID3DXSaveUserData</span><span class="sxs-lookup"><span data-stu-id="e0e11-127">ID3DXSaveUserData</span></span>](id3dxsaveuserdata.md)
</dt> </dl>

 

 
