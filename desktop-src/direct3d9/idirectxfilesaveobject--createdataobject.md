---
description: Erstellt ein Datenobjekt. Veraltet.
ms.assetid: bb0ef2cf-db76-40f6-968f-3599c58459a7
title: 'Idirectxfilesaveobject:: kreatedataobject-Methode (dxfile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileSaveObject.CreateDataObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 7c5a67a72f6ff5a63730167d2fe2d12213a9ab72
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354676"
---
# <a name="idirectxfilesaveobjectcreatedataobject-method"></a><span data-ttu-id="1e14b-104">Idirectxfilesaveobject:: kreatedataobject-Methode</span><span class="sxs-lookup"><span data-stu-id="1e14b-104">IDirectXFileSaveObject::CreateDataObject method</span></span>

<span data-ttu-id="1e14b-105">Erstellt ein Datenobjekt.</span><span class="sxs-lookup"><span data-stu-id="1e14b-105">Creates a data object.</span></span> <span data-ttu-id="1e14b-106">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="1e14b-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e14b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="1e14b-107">Syntax</span></span>


```C++
HRESULT CreateDataObject(
  [in]                REFGUID           rguidTemplate,
  [in]                LPCSTR            szName,
  [in]          const GUID              *pguid,
  [in]                DWORD             cbSize,
  [in]                LPVOID            pvData,
  [out, retval]       LPDIRECTXFILEDATA *ppDataObj
);
```



## <a name="parameters"></a><span data-ttu-id="1e14b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="1e14b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e14b-109">*rguidtemplate* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1e14b-109">*rguidTemplate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e14b-110">Typ: **[reguid](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**</span><span class="sxs-lookup"><span data-stu-id="1e14b-110">Type: **[REFGUID](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**</span></span>

<span data-ttu-id="1e14b-111">GUID, die die Vorlage des Datenobjekts darstellt.</span><span class="sxs-lookup"><span data-stu-id="1e14b-111">GUID representing the data object's template.</span></span>

</dd> <dt>

<span data-ttu-id="1e14b-112">*szName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1e14b-112">*szName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e14b-113">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1e14b-113">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1e14b-114">Zeiger auf den Namen des Datenobjekts.</span><span class="sxs-lookup"><span data-stu-id="1e14b-114">Pointer to the name of the data object.</span></span> <span data-ttu-id="1e14b-115">Geben Sie **null** an, wenn das Objekt keinen Namen hat.</span><span class="sxs-lookup"><span data-stu-id="1e14b-115">Specify **NULL** if the object does not have a name.</span></span>

</dd> <dt>

<span data-ttu-id="1e14b-116">*pguid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1e14b-116">*pguid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e14b-117">Typ: Konstante **[**GUID**](guid.md) \***</span><span class="sxs-lookup"><span data-stu-id="1e14b-117">Type: **const [**GUID**](guid.md)\***</span></span>

<span data-ttu-id="1e14b-118">Zeiger auf eine GUID, die das Datenobjekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="1e14b-118">Pointer to a GUID representing the data object.</span></span> <span data-ttu-id="1e14b-119">Geben Sie **null** an, wenn das Objekt nicht über eine GUID verfügt.</span><span class="sxs-lookup"><span data-stu-id="1e14b-119">Specify **NULL** if the object does not have a GUID.</span></span>

</dd> <dt>

<span data-ttu-id="1e14b-120">*CBSIZE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1e14b-120">*cbSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e14b-121">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1e14b-121">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1e14b-122">Größe des Datenobjekts in Bytes.</span><span class="sxs-lookup"><span data-stu-id="1e14b-122">Size of the data object, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="1e14b-123">*pvData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1e14b-123">*pvData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e14b-124">Typ: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1e14b-124">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1e14b-125">Zeiger auf einen Puffer, der alle erforderlichen Elementdaten enthält.</span><span class="sxs-lookup"><span data-stu-id="1e14b-125">Pointer to a buffer containing all required member's data.</span></span>

</dd> <dt>

<span data-ttu-id="1e14b-126">*ppdataobj* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="1e14b-126">*ppDataObj* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="1e14b-127">Typ: **[ **lpdirectxfiledata**](idirectxfiledata.md)\***</span><span class="sxs-lookup"><span data-stu-id="1e14b-127">Type: **[**LPDIRECTXFILEDATA**](idirectxfiledata.md)\***</span></span>

<span data-ttu-id="1e14b-128">Adresse eines Zeigers auf eine [**idirectxfiledata**](idirectxfiledata.md) -Schnittstelle, die das erstellte Datei Datenobjekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="1e14b-128">Address of a pointer to an [**IDirectXFileData**](idirectxfiledata.md) interface, representing the created file data object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e14b-129">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1e14b-129">Return value</span></span>

<span data-ttu-id="1e14b-130">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1e14b-130">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1e14b-131">Wenn die Methode erfolgreich ausgeführt wird, ist dxfile OK der Rückgabewert \_ .</span><span class="sxs-lookup"><span data-stu-id="1e14b-131">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="1e14b-132">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein. dxfileerr \_ badzuweisung dxfileerr \_ badvalue</span><span class="sxs-lookup"><span data-stu-id="1e14b-132">If the method fails, the return value can be one of the following values.DXFILEERR\_BADALLOC DXFILEERR\_BADVALUE</span></span>

## <a name="remarks"></a><span data-ttu-id="1e14b-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1e14b-133">Remarks</span></span>

<span data-ttu-id="1e14b-134">Wenn ein Daten Verweis Objekt auf das Datenobjekt verweist, muss der szName-Parameter oder der pguid-Parameter nicht **null** sein.</span><span class="sxs-lookup"><span data-stu-id="1e14b-134">If a data reference object will reference the data object, either the szName or pguid parameter must be non-**NULL**.</span></span>

<span data-ttu-id="1e14b-135">Speichern Sie alle Vorlagen, indem Sie die [**idirectxfilesaveobject:: savetemplates**](idirectxfilesaveobject--savetemplates.md) -Methode verwenden, bevor Sie die von dieser Methode erstellten Daten speichern.</span><span class="sxs-lookup"><span data-stu-id="1e14b-135">Save any templates by using the [**IDirectXFileSaveObject::SaveTemplates**](idirectxfilesaveobject--savetemplates.md) method before saving the data created by this method.</span></span> <span data-ttu-id="1e14b-136">Speichern Sie die erstellten Daten mit der [**idirectxfilesaveobject:: SaveData**](idirectxfilesaveobject--savedata.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="1e14b-136">Save the created data by using the [**IDirectXFileSaveObject::SaveData**](idirectxfilesaveobject--savedata.md) method.</span></span>

<span data-ttu-id="1e14b-137">Wenn Sie optionale Daten speichern müssen, verwenden Sie die [**idirectxfiledata:: adddataobject**](idirectxfiledata--adddataobject.md) -Methode, nachdem Sie diese Methode und vor der Verwendung von [**idirectxfilesaveobject:: SaveData**](idirectxfilesaveobject--savedata.md)verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="1e14b-137">If you need to save optional data, use the [**IDirectXFileData::AddDataObject**](idirectxfiledata--adddataobject.md) method after using this method and before using [**IDirectXFileSaveObject::SaveData**](idirectxfilesaveobject--savedata.md).</span></span> <span data-ttu-id="1e14b-138">Wenn das Objekt über untergeordnete Objekte verfügt, fügen Sie diese vor dem Aufruf von **idirectxfilesaveobject:: SaveData** hinzu.</span><span class="sxs-lookup"><span data-stu-id="1e14b-138">If the object has child objects, add them before calling **IDirectXFileSaveObject::SaveData**.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e14b-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1e14b-139">Requirements</span></span>



| <span data-ttu-id="1e14b-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1e14b-140">Requirement</span></span> | <span data-ttu-id="1e14b-141">Wert</span><span class="sxs-lookup"><span data-stu-id="1e14b-141">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1e14b-142">Header</span><span class="sxs-lookup"><span data-stu-id="1e14b-142">Header</span></span><br/>  | <dl> <span data-ttu-id="1e14b-143"><dt>Dxfile. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e14b-143"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="1e14b-144">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1e14b-144">Library</span></span><br/> | <dl> <span data-ttu-id="1e14b-145"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1e14b-145"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e14b-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1e14b-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e14b-147">Idirectxfilesaveobject</span><span class="sxs-lookup"><span data-stu-id="1e14b-147">IDirectXFileSaveObject</span></span>](idirectxfilesaveobject.md)
</dt> <dt>

[<span data-ttu-id="1e14b-148">**Idirectxfiledata:: adddataobject**</span><span class="sxs-lookup"><span data-stu-id="1e14b-148">**IDirectXFileData::AddDataObject**</span></span>](idirectxfiledata--adddataobject.md)
</dt> <dt>

[<span data-ttu-id="1e14b-149">**Idirectxfilesaveobject:: SaveData**</span><span class="sxs-lookup"><span data-stu-id="1e14b-149">**IDirectXFileSaveObject::SaveData**</span></span>](idirectxfilesaveobject--savedata.md)
</dt> <dt>

[<span data-ttu-id="1e14b-150">**Idirectxfilesaveobject:: savetemplates**</span><span class="sxs-lookup"><span data-stu-id="1e14b-150">**IDirectXFileSaveObject::SaveTemplates**</span></span>](idirectxfilesaveobject--savetemplates.md)
</dt> </dl>

 

 
