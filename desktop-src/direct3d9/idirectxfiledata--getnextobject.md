---
description: Ruft das nächste untergeordnete Datenobjekt, das Daten Verweis Objekt oder das binäre Objekt in der DirectX-Datei ab. Veraltet.
ms.assetid: 8232e911-6552-4b2b-a9c2-59e6a13a0d9b
title: 'Idirectxfiledata:: getnextobject-Methode (dxfile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileData.GetNextObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: e03351068cdc4f8fca28c612b7bb4c546125a4cc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106371935"
---
# <a name="idirectxfiledatagetnextobject-method"></a><span data-ttu-id="a02c3-104">Idirectxfiledata:: getnextobject-Methode</span><span class="sxs-lookup"><span data-stu-id="a02c3-104">IDirectXFileData::GetNextObject method</span></span>

<span data-ttu-id="a02c3-105">Ruft das nächste untergeordnete Datenobjekt, das Daten Verweis Objekt oder das binäre Objekt in der DirectX-Datei ab.</span><span class="sxs-lookup"><span data-stu-id="a02c3-105">Retrieves the next child data object, data reference object, or binary object in the DirectX file.</span></span> <span data-ttu-id="a02c3-106">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="a02c3-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="a02c3-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a02c3-107">Syntax</span></span>


```C++
HRESULT GetNextObject(
  [out, retval] LPDIRECTXFILEOBJECT *ppChildObj
);
```



## <a name="parameters"></a><span data-ttu-id="a02c3-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a02c3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a02c3-109">*ppchildobj* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="a02c3-109">*ppChildObj* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="a02c3-110">Typ: **[ **lpdirectxfileobject**](idirectxfileobject.md)\***</span><span class="sxs-lookup"><span data-stu-id="a02c3-110">Type: **[**LPDIRECTXFILEOBJECT**](idirectxfileobject.md)\***</span></span>

<span data-ttu-id="a02c3-111">Adresse eines Zeigers auf eine [**idirectxfileobject**](idirectxfileobject.md) -Schnittstelle, die die Datei Objektschnittstelle des zurückgegebenen untergeordneten Objekts darstellt.</span><span class="sxs-lookup"><span data-stu-id="a02c3-111">Address of a pointer to an [**IDirectXFileObject**](idirectxfileobject.md) interface, representing the returned child object's file object interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a02c3-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a02c3-112">Return value</span></span>

<span data-ttu-id="a02c3-113">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a02c3-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a02c3-114">Wenn die Methode erfolgreich ausgeführt wird, ist dxfile OK der Rückgabewert \_ .</span><span class="sxs-lookup"><span data-stu-id="a02c3-114">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="a02c3-115">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: dxfileerr \_ badvalue, dxfileerr \_ nomoreobjects.</span><span class="sxs-lookup"><span data-stu-id="a02c3-115">If the method fails, the return value can be one of the following values: DXFILEERR\_BADVALUE, DXFILEERR\_NOMOREOBJECTS.</span></span>

## <a name="remarks"></a><span data-ttu-id="a02c3-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a02c3-116">Remarks</span></span>

<span data-ttu-id="a02c3-117">Um den Typ des abgerufenen Objekts zu ermitteln, verwenden Sie QueryInterface, um das abgerufene Objekt zur Unterstützung der Schnittstellen [**idirectxfiledata**](idirectxfiledata.md), [**idirectxfiledatareferenoder**](idirectxfiledatareference.md) [**idirectxfilebinary**](idirectxfilebinary.md) abzufragen.</span><span class="sxs-lookup"><span data-stu-id="a02c3-117">To determine the type of object retrieved, use QueryInterface to query the retrieved object for support of [**IDirectXFileData**](idirectxfiledata.md), [**IDirectXFileDataReference**](idirectxfiledatareference.md), or [**IDirectXFileBinary**](idirectxfilebinary.md) interfaces.</span></span> <span data-ttu-id="a02c3-118">Die unterstützte Schnittstelle zeigt den Objekttyp an (Daten, Daten Verweis oder binär).</span><span class="sxs-lookup"><span data-stu-id="a02c3-118">The interface supported indicates the type of object (data, data reference, or binary).</span></span>

## <a name="requirements"></a><span data-ttu-id="a02c3-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a02c3-119">Requirements</span></span>



| <span data-ttu-id="a02c3-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a02c3-120">Requirement</span></span> | <span data-ttu-id="a02c3-121">Wert</span><span class="sxs-lookup"><span data-stu-id="a02c3-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a02c3-122">Header</span><span class="sxs-lookup"><span data-stu-id="a02c3-122">Header</span></span><br/>  | <dl> <span data-ttu-id="a02c3-123"><dt>Dxfile. h</dt></span><span class="sxs-lookup"><span data-stu-id="a02c3-123"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="a02c3-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a02c3-124">Library</span></span><br/> | <dl> <span data-ttu-id="a02c3-125"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a02c3-125"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a02c3-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a02c3-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a02c3-127">**Idirectxfilebinary**</span><span class="sxs-lookup"><span data-stu-id="a02c3-127">**IDirectXFileBinary**</span></span>](idirectxfilebinary.md)
</dt> <dt>

[<span data-ttu-id="a02c3-128">**Idirectxfiledata**</span><span class="sxs-lookup"><span data-stu-id="a02c3-128">**IDirectXFileData**</span></span>](idirectxfiledata.md)
</dt> <dt>

[<span data-ttu-id="a02c3-129">**Idirectxfiledatareferenzierung**</span><span class="sxs-lookup"><span data-stu-id="a02c3-129">**IDirectXFileDataReference**</span></span>](idirectxfiledatareference.md)
</dt> </dl>

 

 




