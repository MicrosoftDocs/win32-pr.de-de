---
description: Ruft das nächste Objekt der obersten Ebene in der DirectX-Datei ab. Veraltet.
ms.assetid: 91cd3205-5603-4a62-aab2-7ef4adb9e6d1
title: 'Idirectxfileenumubject:: getnextdataobject-Methode (dxfile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileEnumObject.GetNextDataObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: bc50af216eaae1687351d472b7151aaaeae9116f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354227"
---
# <a name="idirectxfileenumobjectgetnextdataobject-method"></a><span data-ttu-id="653c6-104">Idirectxfileenumubject:: getnextdataobject-Methode</span><span class="sxs-lookup"><span data-stu-id="653c6-104">IDirectXFileEnumObject::GetNextDataObject method</span></span>

<span data-ttu-id="653c6-105">Ruft das nächste Objekt der obersten Ebene in der DirectX-Datei ab.</span><span class="sxs-lookup"><span data-stu-id="653c6-105">Retrieves the next top-level object in the DirectX file.</span></span> <span data-ttu-id="653c6-106">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="653c6-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="653c6-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="653c6-107">Syntax</span></span>


```C++
HRESULT GetNextDataObject(
  [out] LPDIRECTXFILEDATA *ppDataObj
);
```



## <a name="parameters"></a><span data-ttu-id="653c6-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="653c6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="653c6-109">*ppdataobj* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="653c6-109">*ppDataObj* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="653c6-110">Typ: **[ **lpdirectxfiledata**](idirectxfiledata.md)\***</span><span class="sxs-lookup"><span data-stu-id="653c6-110">Type: **[**LPDIRECTXFILEDATA**](idirectxfiledata.md)\***</span></span>

<span data-ttu-id="653c6-111">Adresse eines Zeigers auf eine [**idirectxfiledata**](idirectxfiledata.md) -Schnittstelle, die das zurückgegebene Datei Datenobjekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="653c6-111">Address of a pointer to an [**IDirectXFileData**](idirectxfiledata.md) interface, representing the returned file data object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="653c6-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="653c6-112">Return value</span></span>

<span data-ttu-id="653c6-113">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="653c6-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="653c6-114">Wenn die Methode erfolgreich ausgeführt wird, ist dxfile OK der Rückgabewert \_ .</span><span class="sxs-lookup"><span data-stu-id="653c6-114">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="653c6-115">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: dxfileerr \_ badvalue, dxfileerr \_ nomoreobjects</span><span class="sxs-lookup"><span data-stu-id="653c6-115">If the method fails, the return value can be one of the following values: DXFILEERR\_BADVALUE, DXFILEERR\_NOMOREOBJECTS</span></span>

## <a name="remarks"></a><span data-ttu-id="653c6-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="653c6-116">Remarks</span></span>

<span data-ttu-id="653c6-117">Objekte der obersten Ebene sind immer Datenobjekte.</span><span class="sxs-lookup"><span data-stu-id="653c6-117">Top-level objects are always data objects.</span></span> <span data-ttu-id="653c6-118">Daten Verweis Objekte und binäre Objekte können nur untergeordnete Elemente von Datenobjekten sein.</span><span class="sxs-lookup"><span data-stu-id="653c6-118">Data reference objects and binary objects can only be children of data objects.</span></span>

## <a name="requirements"></a><span data-ttu-id="653c6-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="653c6-119">Requirements</span></span>



| <span data-ttu-id="653c6-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="653c6-120">Requirement</span></span> | <span data-ttu-id="653c6-121">Wert</span><span class="sxs-lookup"><span data-stu-id="653c6-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="653c6-122">Header</span><span class="sxs-lookup"><span data-stu-id="653c6-122">Header</span></span><br/>  | <dl> <span data-ttu-id="653c6-123"><dt>Dxfile. h</dt></span><span class="sxs-lookup"><span data-stu-id="653c6-123"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="653c6-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="653c6-124">Library</span></span><br/> | <dl> <span data-ttu-id="653c6-125"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="653c6-125"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="653c6-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="653c6-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="653c6-127">Idirectxfile-umubject</span><span class="sxs-lookup"><span data-stu-id="653c6-127">IDirectXFileEnumObject</span></span>](idirectxfileenumobject.md)
</dt> </dl>

 

 




