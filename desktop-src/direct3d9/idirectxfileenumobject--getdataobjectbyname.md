---
description: Ruft das Datenobjekt ab, das über den angegebenen Namen verfügt. Veraltet.
ms.assetid: d04d5a45-72d9-4256-8700-378e8139ed36
title: 'Idirectxfileenumubject:: getdataobjectbyname-Methode (dxfile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileEnumObject.GetDataObjectByName
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 858097139702770d148765c4c9a57f6522d9633b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106369327"
---
# <a name="idirectxfileenumobjectgetdataobjectbyname-method"></a><span data-ttu-id="d09e8-104">Idirectxfileenumubject:: getdataobjectbyname-Methode</span><span class="sxs-lookup"><span data-stu-id="d09e8-104">IDirectXFileEnumObject::GetDataObjectByName method</span></span>

<span data-ttu-id="d09e8-105">Ruft das Datenobjekt ab, das über den angegebenen Namen verfügt.</span><span class="sxs-lookup"><span data-stu-id="d09e8-105">Retrieves the data object that has the specified name.</span></span> <span data-ttu-id="d09e8-106">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="d09e8-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="d09e8-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d09e8-107">Syntax</span></span>


```C++
HRESULT GetDataObjectByName(
  [in]  LPCSTR            szName,
  [out] LPDIRECTXFILEDATA *ppDataObj
);
```



## <a name="parameters"></a><span data-ttu-id="d09e8-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d09e8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d09e8-109">*szName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d09e8-109">*szName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d09e8-110">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d09e8-110">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d09e8-111">Zeiger auf den angeforderten Namen.</span><span class="sxs-lookup"><span data-stu-id="d09e8-111">Pointer to the requested name.</span></span>

</dd> <dt>

<span data-ttu-id="d09e8-112">*ppdataobj* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="d09e8-112">*ppDataObj* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d09e8-113">Typ: **[ **lpdirectxfiledata**](idirectxfiledata.md)\***</span><span class="sxs-lookup"><span data-stu-id="d09e8-113">Type: **[**LPDIRECTXFILEDATA**](idirectxfiledata.md)\***</span></span>

<span data-ttu-id="d09e8-114">Adresse eines Zeigers auf eine [**idirectxfiledata**](idirectxfiledata.md) -Schnittstelle, die das zurückgegebene Datei Datenobjekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="d09e8-114">Address of a pointer to an [**IDirectXFileData**](idirectxfiledata.md) interface, representing the returned file data object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d09e8-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d09e8-115">Return value</span></span>

<span data-ttu-id="d09e8-116">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d09e8-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d09e8-117">Wenn die Methode erfolgreich ausgeführt wird, ist dxfile OK der Rückgabewert \_ .</span><span class="sxs-lookup"><span data-stu-id="d09e8-117">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="d09e8-118">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: dxfileerr \_ badvalue, dxfileerr \_ NotFound.</span><span class="sxs-lookup"><span data-stu-id="d09e8-118">If the method fails, the return value can be one of the following values: DXFILEERR\_BADVALUE, DXFILEERR\_NOTFOUND.</span></span>

## <a name="requirements"></a><span data-ttu-id="d09e8-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d09e8-119">Requirements</span></span>



| <span data-ttu-id="d09e8-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d09e8-120">Requirement</span></span> | <span data-ttu-id="d09e8-121">Wert</span><span class="sxs-lookup"><span data-stu-id="d09e8-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d09e8-122">Header</span><span class="sxs-lookup"><span data-stu-id="d09e8-122">Header</span></span><br/>  | <dl> <span data-ttu-id="d09e8-123"><dt>Dxfile. h</dt></span><span class="sxs-lookup"><span data-stu-id="d09e8-123"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="d09e8-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d09e8-124">Library</span></span><br/> | <dl> <span data-ttu-id="d09e8-125"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d09e8-125"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d09e8-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d09e8-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d09e8-127">Idirectxfile-umubject</span><span class="sxs-lookup"><span data-stu-id="d09e8-127">IDirectXFileEnumObject</span></span>](idirectxfileenumobject.md)
</dt> </dl>

 

 
