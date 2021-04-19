---
description: Ruft das Datenobjekt ab, das über die angegebene GUID verfügt.
ms.assetid: c3d598bd-0646-4f99-8517-4475ef7cd8c9
title: 'ID3DXFileEnumObject:: getdataobjectbyid-Methode (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileEnumObject.GetDataObjectById
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 82a74ca4ff472d678ded92aa01f2c2406560955e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106366664"
---
# <a name="id3dxfileenumobjectgetdataobjectbyid-method"></a><span data-ttu-id="9b0b9-103">ID3DXFileEnumObject:: getdataobjectbyid-Methode</span><span class="sxs-lookup"><span data-stu-id="9b0b9-103">ID3DXFileEnumObject::GetDataObjectById method</span></span>

<span data-ttu-id="9b0b9-104">Ruft das Datenobjekt ab, das über die angegebene GUID verfügt.</span><span class="sxs-lookup"><span data-stu-id="9b0b9-104">Retrieves the data object that has the specified GUID.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b0b9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9b0b9-105">Syntax</span></span>


```C++
HRESULT GetDataObjectById(
  [in]  REFGUID        rguid,
  [out] LPD3DXFILEDATA *ppDataObj
);
```



## <a name="parameters"></a><span data-ttu-id="9b0b9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9b0b9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b0b9-107">*rguid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9b0b9-107">*rguid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b0b9-108">Typ: **[reguid](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**</span><span class="sxs-lookup"><span data-stu-id="9b0b9-108">Type: **[REFGUID](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**</span></span>

<span data-ttu-id="9b0b9-109">Verweis auf die angeforderte GUID.</span><span class="sxs-lookup"><span data-stu-id="9b0b9-109">Reference to the requested GUID.</span></span>

</dd> <dt>

<span data-ttu-id="9b0b9-110">*ppdataobj* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="9b0b9-110">*ppDataObj* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9b0b9-111">Typ: **[ **LPD3DXFILEDATA**](id3dxfiledata.md)\***</span><span class="sxs-lookup"><span data-stu-id="9b0b9-111">Type: **[**LPD3DXFILEDATA**](id3dxfiledata.md)\***</span></span>

<span data-ttu-id="9b0b9-112">Adresse eines Zeigers auf eine [**ID3DXFileData**](id3dxfiledata.md) -Schnittstelle, die das zurückgegebene Datei Datenobjekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="9b0b9-112">Address of a pointer to an [**ID3DXFileData**](id3dxfiledata.md) interface, representing the returned file data object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b0b9-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9b0b9-113">Return value</span></span>

<span data-ttu-id="9b0b9-114">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9b0b9-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9b0b9-115">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="9b0b9-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="9b0b9-116">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: dxfileerr \_ badvalue, dxfileerr \_ NotFound.</span><span class="sxs-lookup"><span data-stu-id="9b0b9-116">If the method fails, the return value can be one of the following:DXFILEERR\_BADVALUE, DXFILEERR\_NOTFOUND.</span></span>

## <a name="remarks"></a><span data-ttu-id="9b0b9-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9b0b9-117">Remarks</span></span>

<span data-ttu-id="9b0b9-118">Rufen Sie die GUID-rguid des aktuellen Datei Datenobjekts mit der [**ID3DXFileData:: GetId**](id3dxfiledata--getid.md) -Methode ab.</span><span class="sxs-lookup"><span data-stu-id="9b0b9-118">Obtain the GUID rguid of the current file data object with the [**ID3DXFileData::GetId**](id3dxfiledata--getid.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b0b9-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9b0b9-119">Requirements</span></span>



| <span data-ttu-id="9b0b9-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9b0b9-120">Requirement</span></span> | <span data-ttu-id="9b0b9-121">Wert</span><span class="sxs-lookup"><span data-stu-id="9b0b9-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9b0b9-122">Header</span><span class="sxs-lookup"><span data-stu-id="9b0b9-122">Header</span></span><br/>  | <dl> <span data-ttu-id="9b0b9-123"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="9b0b9-123"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="9b0b9-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9b0b9-124">Library</span></span><br/> | <dl> <span data-ttu-id="9b0b9-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9b0b9-125"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="9b0b9-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9b0b9-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b0b9-127">ID3DXFileEnumObject</span><span class="sxs-lookup"><span data-stu-id="9b0b9-127">ID3DXFileEnumObject</span></span>](id3dxfileenumobject.md)
</dt> </dl>

 

 
