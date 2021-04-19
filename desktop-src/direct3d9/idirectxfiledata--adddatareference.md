---
description: Erstellt ein Daten Verweis Objekt als untergeordnetes Objekt und fügt es hinzu. Veraltet.
ms.assetid: 71a770a2-1502-4b93-b368-990c3318bd33
title: 'Idirectxfiledata:: adddatareferenzierungsmethode (dxfile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileData.AddDataReference
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 44834af51380c3b8bdbb4e9a4b24bf911ea6a07f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106366455"
---
# <a name="idirectxfiledataadddatareference-method"></a><span data-ttu-id="95cc5-104">Idirectxfiledata:: adddatareferenzierungsmethode</span><span class="sxs-lookup"><span data-stu-id="95cc5-104">IDirectXFileData::AddDataReference method</span></span>

<span data-ttu-id="95cc5-105">Erstellt ein Daten Verweis Objekt als untergeordnetes Objekt und fügt es hinzu.</span><span class="sxs-lookup"><span data-stu-id="95cc5-105">Creates and adds a data reference object as a child object.</span></span> <span data-ttu-id="95cc5-106">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="95cc5-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="95cc5-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="95cc5-107">Syntax</span></span>


```C++
HRESULT AddDataReference(
  [in]       LPCSTR szRef,
  [in] const GUID   *pguidRef
);
```



## <a name="parameters"></a><span data-ttu-id="95cc5-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="95cc5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95cc5-109">*szref* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="95cc5-109">*szRef* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95cc5-110">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="95cc5-110">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="95cc5-111">Zeiger auf den Namen des Datenobjekts, auf das verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="95cc5-111">Pointer to the name of the referenced data object.</span></span> <span data-ttu-id="95cc5-112">Dieser Parameter kann **null** sein, wenn pguidref einen Verweis auf die GUID bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="95cc5-112">This parameter can be **NULL** if pguidRef provides a reference to the GUID.</span></span>

</dd> <dt>

<span data-ttu-id="95cc5-113">*pguidref* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="95cc5-113">*pguidRef* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95cc5-114">Typ: Konstante **[**GUID**](guid.md) \***</span><span class="sxs-lookup"><span data-stu-id="95cc5-114">Type: **const [**GUID**](guid.md)\***</span></span>

<span data-ttu-id="95cc5-115">Zeiger auf die GUID, die die Daten darstellt.</span><span class="sxs-lookup"><span data-stu-id="95cc5-115">Pointer to the GUID representing the data.</span></span> <span data-ttu-id="95cc5-116">Dieser Parameter kann **null** sein, wenn szref einen Verweis auf den Namen bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="95cc5-116">This parameter can be **NULL** if szRef provides a reference to the name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95cc5-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="95cc5-117">Return value</span></span>

<span data-ttu-id="95cc5-118">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="95cc5-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="95cc5-119">Wenn die Methode erfolgreich ausgeführt wird, ist dxfile OK der Rückgabewert \_ .</span><span class="sxs-lookup"><span data-stu-id="95cc5-119">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="95cc5-120">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein. dxfileerr \_ badzuweisung dxfileerr \_ badvalue</span><span class="sxs-lookup"><span data-stu-id="95cc5-120">If the method fails, the return value can be one of the following values.DXFILEERR\_BADALLOC DXFILEERR\_BADVALUE</span></span>

## <a name="remarks"></a><span data-ttu-id="95cc5-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="95cc5-121">Remarks</span></span>

<span data-ttu-id="95cc5-122">Damit diese Methode erfolgreich ausgeführt werden kann, darf der szref-oder pguidref-Parameter nicht **null** sein.</span><span class="sxs-lookup"><span data-stu-id="95cc5-122">For this method to succeed, either the szRef or pguidRef parameter must be non-**NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="95cc5-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="95cc5-123">Requirements</span></span>



| <span data-ttu-id="95cc5-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="95cc5-124">Requirement</span></span> | <span data-ttu-id="95cc5-125">Wert</span><span class="sxs-lookup"><span data-stu-id="95cc5-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="95cc5-126">Header</span><span class="sxs-lookup"><span data-stu-id="95cc5-126">Header</span></span><br/>  | <dl> <span data-ttu-id="95cc5-127"><dt>Dxfile. h</dt></span><span class="sxs-lookup"><span data-stu-id="95cc5-127"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="95cc5-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="95cc5-128">Library</span></span><br/> | <dl> <span data-ttu-id="95cc5-129"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="95cc5-129"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95cc5-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="95cc5-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95cc5-131">Idirectxfiledata</span><span class="sxs-lookup"><span data-stu-id="95cc5-131">IDirectXFileData</span></span>](idirectxfiledata.md)
</dt> </dl>

 

 
