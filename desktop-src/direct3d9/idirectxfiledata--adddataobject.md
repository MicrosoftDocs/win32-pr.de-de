---
description: Fügt ein Datenobjekt als untergeordnetes Objekt hinzu. Veraltet.
ms.assetid: 43771dd6-c17f-4376-9b0a-459ba61ff4c5
title: 'Idirectxfiledata:: adddataobject-Methode (dxfile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileData.AddDataObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 393526bb249b0337964bee0af5be1b55b8dd513e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355397"
---
# <a name="idirectxfiledataadddataobject-method"></a><span data-ttu-id="07434-104">Idirectxfiledata:: adddataobject-Methode</span><span class="sxs-lookup"><span data-stu-id="07434-104">IDirectXFileData::AddDataObject method</span></span>

<span data-ttu-id="07434-105">Fügt ein Datenobjekt als untergeordnetes Objekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="07434-105">Adds a data object as a child object.</span></span> <span data-ttu-id="07434-106">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="07434-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="07434-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="07434-107">Syntax</span></span>


```C++
HRESULT AddDataObject(
  [in] LPDIRECTXFILEDATA pDataObj
);
```



## <a name="parameters"></a><span data-ttu-id="07434-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="07434-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07434-109">*pdataobj* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="07434-109">*pDataObj* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07434-110">Typ: **[ **lpdirectxfiledata**](idirectxfiledata.md)**</span><span class="sxs-lookup"><span data-stu-id="07434-110">Type: **[**LPDIRECTXFILEDATA**](idirectxfiledata.md)**</span></span>

<span data-ttu-id="07434-111">Ein Zeiger auf eine [**idirectxfiledata**](idirectxfiledata.md) -Schnittstelle, die das Datei Datenobjekt darstellt, das als untergeordnetes Objekt hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="07434-111">Pointer to an [**IDirectXFileData**](idirectxfiledata.md) interface, representing the file data object to add as a child object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07434-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="07434-112">Return value</span></span>

<span data-ttu-id="07434-113">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="07434-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="07434-114">Wenn die Methode erfolgreich ausgeführt wird, ist dxfile OK der Rückgabewert \_ .</span><span class="sxs-lookup"><span data-stu-id="07434-114">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="07434-115">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein. dxfileerr \_ badzuweisung dxfileerr \_ badvalue</span><span class="sxs-lookup"><span data-stu-id="07434-115">If the method fails, the return value can be one of the following values.DXFILEERR\_BADALLOC DXFILEERR\_BADVALUE</span></span>

## <a name="remarks"></a><span data-ttu-id="07434-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="07434-116">Remarks</span></span>

<span data-ttu-id="07434-117">Verwenden Sie die [**idirectxfilesaveobject:: createDataObject**](idirectxfilesaveobject--createdataobject.md) -Methode, um das [**idirectxfiledata**](idirectxfiledata.md) -Objekt zu erstellen, bevor Sie diese Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="07434-117">Use the [**IDirectXFileSaveObject::CreateDataObject**](idirectxfilesaveobject--createdataobject.md) method to create the [**IDirectXFileData**](idirectxfiledata.md) object before calling this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="07434-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="07434-118">Requirements</span></span>



| <span data-ttu-id="07434-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="07434-119">Requirement</span></span> | <span data-ttu-id="07434-120">Wert</span><span class="sxs-lookup"><span data-stu-id="07434-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="07434-121">Header</span><span class="sxs-lookup"><span data-stu-id="07434-121">Header</span></span><br/>  | <dl> <span data-ttu-id="07434-122"><dt>Dxfile. h</dt></span><span class="sxs-lookup"><span data-stu-id="07434-122"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="07434-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="07434-123">Library</span></span><br/> | <dl> <span data-ttu-id="07434-124"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="07434-124"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07434-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="07434-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07434-126">Idirectxfiledata</span><span class="sxs-lookup"><span data-stu-id="07434-126">IDirectXFileData</span></span>](idirectxfiledata.md)
</dt> <dt>

[<span data-ttu-id="07434-127">**Idirectxfilesaveobject:: kreatedataobject**</span><span class="sxs-lookup"><span data-stu-id="07434-127">**IDirectXFileSaveObject::CreateDataObject**</span></span>](idirectxfilesaveobject--createdataobject.md)
</dt> </dl>

 

 




