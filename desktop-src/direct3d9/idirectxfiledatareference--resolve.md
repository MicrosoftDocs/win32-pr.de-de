---
description: Löst Daten Verweise auf. Veraltet.
ms.assetid: e8cf6e5d-c9b2-4a47-b058-24282dc65e74
title: 'Idirectxfiledatareferen:: Resolve-Methode (dxfile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileDataReference.Resolve
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 1b047245e3f89a618cde83e5c18a323f9364f3ef
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106364377"
---
# <a name="idirectxfiledatareferenceresolve-method"></a><span data-ttu-id="78d6e-104">Idirectxfiledatareferen:: Resolve-Methode</span><span class="sxs-lookup"><span data-stu-id="78d6e-104">IDirectXFileDataReference::Resolve method</span></span>

<span data-ttu-id="78d6e-105">Löst Daten Verweise auf.</span><span class="sxs-lookup"><span data-stu-id="78d6e-105">Resolves data references.</span></span> <span data-ttu-id="78d6e-106">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="78d6e-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="78d6e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="78d6e-107">Syntax</span></span>


```C++
HRESULT Resolve(
  [out, retval] LPDIRECTXFILEDATA *ppDataObj
);
```



## <a name="parameters"></a><span data-ttu-id="78d6e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="78d6e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78d6e-109">*ppdataobj* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="78d6e-109">*ppDataObj* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="78d6e-110">Typ: **[ **lpdirectxfiledata**](idirectxfiledata.md)\***</span><span class="sxs-lookup"><span data-stu-id="78d6e-110">Type: **[**LPDIRECTXFILEDATA**](idirectxfiledata.md)\***</span></span>

<span data-ttu-id="78d6e-111">Adresse eines Zeigers auf eine [**idirectxfiledata**](idirectxfiledata.md) -Schnittstelle, die das zurückgegebene Datei Datenobjekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="78d6e-111">Address of a pointer to an [**IDirectXFileData**](idirectxfiledata.md) interface, representing the returned file data object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78d6e-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="78d6e-112">Return value</span></span>

<span data-ttu-id="78d6e-113">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="78d6e-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="78d6e-114">Wenn die Methode erfolgreich ausgeführt wird, ist dxfile OK der Rückgabewert \_ .</span><span class="sxs-lookup"><span data-stu-id="78d6e-114">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="78d6e-115">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: dxfileerr \_ badvalue, dxfileerr \_ NotFound.</span><span class="sxs-lookup"><span data-stu-id="78d6e-115">If the method fails, the return value can be one of the following values: DXFILEERR\_BADVALUE, DXFILEERR\_NOTFOUND.</span></span>

## <a name="requirements"></a><span data-ttu-id="78d6e-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="78d6e-116">Requirements</span></span>



| <span data-ttu-id="78d6e-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="78d6e-117">Requirement</span></span> | <span data-ttu-id="78d6e-118">Wert</span><span class="sxs-lookup"><span data-stu-id="78d6e-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="78d6e-119">Header</span><span class="sxs-lookup"><span data-stu-id="78d6e-119">Header</span></span><br/>  | <dl> <span data-ttu-id="78d6e-120"><dt>Dxfile. h</dt></span><span class="sxs-lookup"><span data-stu-id="78d6e-120"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="78d6e-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="78d6e-121">Library</span></span><br/> | <dl> <span data-ttu-id="78d6e-122"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="78d6e-122"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78d6e-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="78d6e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78d6e-124">Idirectxfiledatareferenzierung</span><span class="sxs-lookup"><span data-stu-id="78d6e-124">IDirectXFileDataReference</span></span>](idirectxfiledatareference.md)
</dt> </dl>

 

 




