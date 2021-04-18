---
description: Ruft das Datenobjekt ab, das über die angegebene GUID verfügt. Veraltet.
ms.assetid: dd079b5c-18e1-4252-aabd-498c24910a08
title: 'Idirectxfileenduwbject:: getdataobjectbyid-Methode (dxfile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileEnumObject.GetDataObjectById
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: a27ac17963d4876a3cb0a26d05b63f4c34bf99fc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106365067"
---
# <a name="idirectxfileenumobjectgetdataobjectbyid-method"></a><span data-ttu-id="bd1da-104">Idirectxfileendumuject:: getdataobjectbyid-Methode</span><span class="sxs-lookup"><span data-stu-id="bd1da-104">IDirectXFileEnumObject::GetDataObjectById method</span></span>

<span data-ttu-id="bd1da-105">Ruft das Datenobjekt ab, das über die angegebene GUID verfügt.</span><span class="sxs-lookup"><span data-stu-id="bd1da-105">Retrieves the data object that has the specified GUID.</span></span> <span data-ttu-id="bd1da-106">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="bd1da-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd1da-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="bd1da-107">Syntax</span></span>


```C++
HRESULT GetDataObjectById(
  [in]  REFGUID           rguid,
  [out] LPDIRECTXFILEDATA *ppDataObj
);
```



## <a name="parameters"></a><span data-ttu-id="bd1da-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="bd1da-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd1da-109">*rguid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bd1da-109">*rguid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd1da-110">Typ: **[reguid](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**</span><span class="sxs-lookup"><span data-stu-id="bd1da-110">Type: **[REFGUID](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**</span></span>

<span data-ttu-id="bd1da-111">Verweis auf die angeforderte GUID.</span><span class="sxs-lookup"><span data-stu-id="bd1da-111">Reference to the requested GUID.</span></span>

</dd> <dt>

<span data-ttu-id="bd1da-112">*ppdataobj* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="bd1da-112">*ppDataObj* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bd1da-113">Typ: **[ **lpdirectxfiledata**](idirectxfiledata.md)\***</span><span class="sxs-lookup"><span data-stu-id="bd1da-113">Type: **[**LPDIRECTXFILEDATA**](idirectxfiledata.md)\***</span></span>

<span data-ttu-id="bd1da-114">Adresse eines Zeigers auf eine [**idirectxfiledata**](idirectxfiledata.md) -Schnittstelle, die das zurückgegebene Datei Datenobjekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="bd1da-114">Address of a pointer to an [**IDirectXFileData**](idirectxfiledata.md) interface, representing the returned file data object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd1da-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bd1da-115">Return value</span></span>

<span data-ttu-id="bd1da-116">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bd1da-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bd1da-117">Wenn die Methode erfolgreich ausgeführt wird, ist dxfile OK der Rückgabewert \_ .</span><span class="sxs-lookup"><span data-stu-id="bd1da-117">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="bd1da-118">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: dxfileerr \_ badvalue, dxfileerr \_ NotFound.</span><span class="sxs-lookup"><span data-stu-id="bd1da-118">If the method fails, the return value can be one of the following values: DXFILEERR\_BADVALUE, DXFILEERR\_NOTFOUND.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd1da-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bd1da-119">Requirements</span></span>



| <span data-ttu-id="bd1da-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bd1da-120">Requirement</span></span> | <span data-ttu-id="bd1da-121">Wert</span><span class="sxs-lookup"><span data-stu-id="bd1da-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bd1da-122">Header</span><span class="sxs-lookup"><span data-stu-id="bd1da-122">Header</span></span><br/>  | <dl> <span data-ttu-id="bd1da-123"><dt>Dxfile. h</dt></span><span class="sxs-lookup"><span data-stu-id="bd1da-123"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="bd1da-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="bd1da-124">Library</span></span><br/> | <dl> <span data-ttu-id="bd1da-125"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bd1da-125"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd1da-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bd1da-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd1da-127">Idirectxfile-umubject</span><span class="sxs-lookup"><span data-stu-id="bd1da-127">IDirectXFileEnumObject</span></span>](idirectxfileenumobject.md)
</dt> </dl>

 

 
