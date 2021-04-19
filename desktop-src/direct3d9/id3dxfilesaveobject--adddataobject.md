---
description: Fügt ein Datenobjekt als untergeordnetes Element des ID3DXFileSaveData-Objekts hinzu.
ms.assetid: 710a1588-d766-4555-97a3-4b5a517ce805
title: 'ID3DXFileSaveObject:: adddataobject-Methode (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveObject.AddDataObject
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: d1586035a0d8a81c2210009bad903aac5197bcf7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353718"
---
# <a name="id3dxfilesaveobjectadddataobject-method"></a><span data-ttu-id="949d1-103">ID3DXFileSaveObject:: adddataobject-Methode</span><span class="sxs-lookup"><span data-stu-id="949d1-103">ID3DXFileSaveObject::AddDataObject method</span></span>

<span data-ttu-id="949d1-104">Fügt ein Datenobjekt als untergeordnetes Element des [**ID3DXFileSaveData**](id3dxfilesavedata.md) -Objekts hinzu.</span><span class="sxs-lookup"><span data-stu-id="949d1-104">Adds a data object as a child of the [**ID3DXFileSaveData**](id3dxfilesavedata.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="949d1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="949d1-105">Syntax</span></span>


```C++
HRESULT AddDataObject(
  [in]               REFGUID           rguidTemplate,
  [in]               LPCSTR            szName,
  [in]         const GUID              *pId,
  [in]               SIZE_T            cbSize,
  [in]               LPCVOID           pvData,
  [in, retval]       ID3DXFileSaveData **ppObj
);
```



## <a name="parameters"></a><span data-ttu-id="949d1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="949d1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="949d1-107">*rguidtemplate* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="949d1-107">*rguidTemplate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="949d1-108">Typ: **[reguid](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**</span><span class="sxs-lookup"><span data-stu-id="949d1-108">Type: **[REFGUID](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**</span></span>

<span data-ttu-id="949d1-109">GUID, die die Vorlage des Datenobjekts darstellt.</span><span class="sxs-lookup"><span data-stu-id="949d1-109">GUID representing the data object's template.</span></span>

</dd> <dt>

<span data-ttu-id="949d1-110">*szName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="949d1-110">*szName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="949d1-111">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="949d1-111">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="949d1-112">Zeiger auf den Namen des Datenobjekts.</span><span class="sxs-lookup"><span data-stu-id="949d1-112">Pointer to the name of the data object.</span></span> <span data-ttu-id="949d1-113">Geben Sie **null** an, wenn das Objekt keinen Namen hat.</span><span class="sxs-lookup"><span data-stu-id="949d1-113">Specify **NULL** if the object does not have a name.</span></span>

</dd> <dt>

<span data-ttu-id="949d1-114">*pId* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="949d1-114">*pId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="949d1-115">Typ: Konstante **[**GUID**](guid.md) \***</span><span class="sxs-lookup"><span data-stu-id="949d1-115">Type: **const [**GUID**](guid.md)\***</span></span>

<span data-ttu-id="949d1-116">Zeiger auf eine GUID, die das Datenobjekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="949d1-116">Pointer to a GUID representing the data object.</span></span> <span data-ttu-id="949d1-117">Geben Sie **null** an, wenn das Objekt nicht über eine GUID verfügt.</span><span class="sxs-lookup"><span data-stu-id="949d1-117">Specify **NULL** if the object does not have a GUID.</span></span>

</dd> <dt>

<span data-ttu-id="949d1-118">*CBSIZE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="949d1-118">*cbSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="949d1-119">Typ: **[ **Größe \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="949d1-119">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="949d1-120">Größe des Datenobjekts in Bytes.</span><span class="sxs-lookup"><span data-stu-id="949d1-120">Size of the data object, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="949d1-121">*pvData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="949d1-121">*pvData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="949d1-122">Geben Sie Folgendes ein: **[ **lpcvoid**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="949d1-122">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="949d1-123">Zeiger auf einen Puffer, der alle erforderlichen Daten im Datenobjekt enthält.</span><span class="sxs-lookup"><span data-stu-id="949d1-123">Pointer to a buffer containing all required data in the data object.</span></span>

</dd> <dt>

<span data-ttu-id="949d1-124">*ppobj* \[ in, retval\]</span><span class="sxs-lookup"><span data-stu-id="949d1-124">*ppObj* \[in, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="949d1-125">Typ: **[ **ID3DXFileSaveData**](id3dxfilesavedata.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="949d1-125">Type: **[**ID3DXFileSaveData**](id3dxfilesavedata.md)\*\***</span></span>

<span data-ttu-id="949d1-126">Adresse eines Zeigers auf eine [**ID3DXFileSaveData**](id3dxfilesavedata.md) -Schnittstelle, die den Datei Datenknoten darstellt, dem das Datenobjekt hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="949d1-126">Address of a pointer to an [**ID3DXFileSaveData**](id3dxfilesavedata.md) interface, representing the file data node to which the data object will be added.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="949d1-127">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="949d1-127">Return value</span></span>

<span data-ttu-id="949d1-128">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="949d1-128">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="949d1-129">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="949d1-129">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="949d1-130">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DXFERR \_ badobject, dxfileerr \_ badvalue, E \_ ouyfimemory.</span><span class="sxs-lookup"><span data-stu-id="949d1-130">If the method fails, the return value can be one of the following: D3DXFERR\_BADOBJECT, DXFILEERR\_BADVALUE, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="949d1-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="949d1-131">Remarks</span></span>

<span data-ttu-id="949d1-132">Wenn ein Daten Verweis Objekt auf das Datenobjekt verweist, muss der szName-Parameter oder der pId-Parameter nicht **null** sein.</span><span class="sxs-lookup"><span data-stu-id="949d1-132">If a data reference object will reference the data object, either the szName or pId parameter must be non-**NULL**.</span></span>

<span data-ttu-id="949d1-133">Speichern Sie die erstellten Daten mithilfe der [**ID3DXFileSaveObject:: Save**](id3dxfilesaveobject--save.md) -Methode auf dem Datenträger.</span><span class="sxs-lookup"><span data-stu-id="949d1-133">Save the created data to disk by using the [**ID3DXFileSaveObject::Save**](id3dxfilesaveobject--save.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="949d1-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="949d1-134">Requirements</span></span>



| <span data-ttu-id="949d1-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="949d1-135">Requirement</span></span> | <span data-ttu-id="949d1-136">Wert</span><span class="sxs-lookup"><span data-stu-id="949d1-136">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="949d1-137">Header</span><span class="sxs-lookup"><span data-stu-id="949d1-137">Header</span></span><br/>  | <dl> <span data-ttu-id="949d1-138"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="949d1-138"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="949d1-139">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="949d1-139">Library</span></span><br/> | <dl> <span data-ttu-id="949d1-140"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="949d1-140"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="949d1-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="949d1-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="949d1-142">ID3DXFileSaveObject</span><span class="sxs-lookup"><span data-stu-id="949d1-142">ID3DXFileSaveObject</span></span>](id3dxfilesaveobject.md)
</dt> </dl>

 

 
