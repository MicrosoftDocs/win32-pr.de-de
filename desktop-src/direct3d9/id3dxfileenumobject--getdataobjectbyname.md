---
description: Ruft das Datenobjekt ab, das über den angegebenen Namen verfügt.
ms.assetid: ed53d871-24e8-4c51-8897-1055ef8a9af1
title: 'ID3DXFileEnumObject:: getdataobjectbyname-Methode (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileEnumObject.GetDataObjectByName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 41850615726ac15e890162c6e28df9b638c582a2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106364372"
---
# <a name="id3dxfileenumobjectgetdataobjectbyname-method"></a><span data-ttu-id="844db-103">ID3DXFileEnumObject:: getdataobjectbyname-Methode</span><span class="sxs-lookup"><span data-stu-id="844db-103">ID3DXFileEnumObject::GetDataObjectByName method</span></span>

<span data-ttu-id="844db-104">Ruft das Datenobjekt ab, das über den angegebenen Namen verfügt.</span><span class="sxs-lookup"><span data-stu-id="844db-104">Retrieves the data object that has the specified name.</span></span>

## <a name="syntax"></a><span data-ttu-id="844db-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="844db-105">Syntax</span></span>


```C++
HRESULT GetDataObjectByName(
  [in]  LPCSTR        szName,
  [out] ID3DXFileData **ppObj
);
```



## <a name="parameters"></a><span data-ttu-id="844db-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="844db-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="844db-107">*szName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="844db-107">*szName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="844db-108">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="844db-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="844db-109">Zeiger auf den angeforderten Namen.</span><span class="sxs-lookup"><span data-stu-id="844db-109">Pointer to the requested name.</span></span>

</dd> <dt>

<span data-ttu-id="844db-110">*ppobj* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="844db-110">*ppObj* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="844db-111">Typ: **[ **ID3DXFileData**](id3dxfiledata.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="844db-111">Type: **[**ID3DXFileData**](id3dxfiledata.md)\*\***</span></span>

<span data-ttu-id="844db-112">Adresse eines Zeigers auf eine [**ID3DXFileData**](id3dxfiledata.md) -Schnittstelle, die das zurückgegebene Datei Datenobjekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="844db-112">Address of a pointer to an [**ID3DXFileData**](id3dxfiledata.md) interface, representing the returned file data object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="844db-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="844db-113">Return value</span></span>

<span data-ttu-id="844db-114">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="844db-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="844db-115">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="844db-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="844db-116">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: dxfileerr \_ badvalue, dxfileerr \_ NotFound.</span><span class="sxs-lookup"><span data-stu-id="844db-116">If the method fails, the return value can be one of the following:DXFILEERR\_BADVALUE, DXFILEERR\_NOTFOUND.</span></span>

## <a name="remarks"></a><span data-ttu-id="844db-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="844db-117">Remarks</span></span>

<span data-ttu-id="844db-118">Rufen Sie den Namen szName des aktuellen Datei Datenobjekts mit der [**ID3DXFileData:: GetName**](id3dxfiledata--getname.md) -Methode ab.</span><span class="sxs-lookup"><span data-stu-id="844db-118">Obtain the name szName of the current file data object with the [**ID3DXFileData::GetName**](id3dxfiledata--getname.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="844db-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="844db-119">Requirements</span></span>



| <span data-ttu-id="844db-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="844db-120">Requirement</span></span> | <span data-ttu-id="844db-121">Wert</span><span class="sxs-lookup"><span data-stu-id="844db-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="844db-122">Header</span><span class="sxs-lookup"><span data-stu-id="844db-122">Header</span></span><br/>  | <dl> <span data-ttu-id="844db-123"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="844db-123"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="844db-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="844db-124">Library</span></span><br/> | <dl> <span data-ttu-id="844db-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="844db-125"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="844db-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="844db-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="844db-127">ID3DXFileEnumObject</span><span class="sxs-lookup"><span data-stu-id="844db-127">ID3DXFileEnumObject</span></span>](id3dxfileenumobject.md)
</dt> </dl>

 

 
