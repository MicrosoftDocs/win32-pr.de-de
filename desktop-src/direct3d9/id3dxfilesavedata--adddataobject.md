---
description: Fügt ein Datenobjekt als untergeordnetes Element des ID3DXFileSaveData-Datei Daten Knotens hinzu.
ms.assetid: 47faad99-3ee8-4ca8-b8d7-413d4cd5b090
title: 'ID3DXFileSaveData:: adddataobject-Methode (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveData.AddDataObject
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b097e63792b32bc1688ce93c8ce32ffaedeae6ee
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355217"
---
# <a name="id3dxfilesavedataadddataobject-method"></a><span data-ttu-id="e88da-103">ID3DXFileSaveData:: adddataobject-Methode</span><span class="sxs-lookup"><span data-stu-id="e88da-103">ID3DXFileSaveData::AddDataObject method</span></span>

<span data-ttu-id="e88da-104">Fügt ein Datenobjekt als untergeordnetes Element des [**ID3DXFileSaveData**](id3dxfilesavedata.md) -Datei Daten Knotens hinzu.</span><span class="sxs-lookup"><span data-stu-id="e88da-104">Adds a data object as a child of the [**ID3DXFileSaveData**](id3dxfilesavedata.md) file data node.</span></span>

## <a name="syntax"></a><span data-ttu-id="e88da-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e88da-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="e88da-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e88da-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e88da-107">*rguidtemplate* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e88da-107">*rguidTemplate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e88da-108">Typ: **[reguid](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**</span><span class="sxs-lookup"><span data-stu-id="e88da-108">Type: **[REFGUID](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**</span></span>

<span data-ttu-id="e88da-109">GUID, die die Vorlage des Datenobjekts darstellt.</span><span class="sxs-lookup"><span data-stu-id="e88da-109">GUID representing the data object's template.</span></span>

</dd> <dt>

<span data-ttu-id="e88da-110">*szName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e88da-110">*szName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e88da-111">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e88da-111">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e88da-112">Zeiger auf den Namen des hinzu zufügenden Datenobjekts.</span><span class="sxs-lookup"><span data-stu-id="e88da-112">Pointer to the name of the data object to add.</span></span> <span data-ttu-id="e88da-113">Geben Sie **null** an, wenn das Objekt keinen Namen hat.</span><span class="sxs-lookup"><span data-stu-id="e88da-113">Specify **NULL** if the object does not have a name.</span></span>

</dd> <dt>

<span data-ttu-id="e88da-114">*pId* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e88da-114">*pId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e88da-115">Typ: Konstante **[**GUID**](guid.md) \***</span><span class="sxs-lookup"><span data-stu-id="e88da-115">Type: **const [**GUID**](guid.md)\***</span></span>

<span data-ttu-id="e88da-116">Zeiger auf eine GUID, die das Datenobjekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="e88da-116">Pointer to a GUID representing the data object.</span></span> <span data-ttu-id="e88da-117">Das Datenobjekt muss mit [**ID3DXFile:: registertemplates**](id3dxfile--registertemplates.md) oder [**ID3DXFile:: registerenumtemplates**](id3dxfile--registerenumtemplates.md)registriert werden.</span><span class="sxs-lookup"><span data-stu-id="e88da-117">The data object must have been registered with [**ID3DXFile::RegisterTemplates**](id3dxfile--registertemplates.md) or [**ID3DXFile::RegisterEnumTemplates**](id3dxfile--registerenumtemplates.md).</span></span> <span data-ttu-id="e88da-118">Geben Sie **null** an, wenn das Objekt nicht über eine GUID verfügt.</span><span class="sxs-lookup"><span data-stu-id="e88da-118">Specify **NULL** if the object does not have a GUID.</span></span>

</dd> <dt>

<span data-ttu-id="e88da-119">*CBSIZE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e88da-119">*cbSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e88da-120">Typ: **[ **Größe \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e88da-120">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e88da-121">Größe des Datenobjekts in Bytes.</span><span class="sxs-lookup"><span data-stu-id="e88da-121">Size of the data object, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="e88da-122">*pvData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e88da-122">*pvData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e88da-123">Geben Sie Folgendes ein: **[ **lpcvoid**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e88da-123">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e88da-124">Zeiger auf einen Puffer, der alle erforderlichen Daten im Datenobjekt enthält.</span><span class="sxs-lookup"><span data-stu-id="e88da-124">Pointer to a buffer containing all required data in the data object.</span></span>

</dd> <dt>

<span data-ttu-id="e88da-125">*ppobj* \[ in, retval\]</span><span class="sxs-lookup"><span data-stu-id="e88da-125">*ppObj* \[in, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="e88da-126">Typ: **[ **ID3DXFileSaveData**](id3dxfilesavedata.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="e88da-126">Type: **[**ID3DXFileSaveData**](id3dxfilesavedata.md)\*\***</span></span>

<span data-ttu-id="e88da-127">Adresse eines Zeigers auf eine [**ID3DXFileSaveData**](id3dxfilesavedata.md) -Schnittstelle, die den Datei Datenknoten darstellt, dem das Datenobjekt hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="e88da-127">Address of a pointer to an [**ID3DXFileSaveData**](id3dxfilesavedata.md) interface, representing the file data node to which the data object will be added.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e88da-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e88da-128">Return value</span></span>

<span data-ttu-id="e88da-129">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e88da-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e88da-130">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e88da-130">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="e88da-131">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DXFERR \_ badobject, D3DXFERR \_ badvalue, E \_ oudebmemory.</span><span class="sxs-lookup"><span data-stu-id="e88da-131">If the method fails, the return value can be one of the following: D3DXFERR\_BADOBJECT, D3DXFERR\_BADVALUE, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="e88da-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e88da-132">Requirements</span></span>



| <span data-ttu-id="e88da-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e88da-133">Requirement</span></span> | <span data-ttu-id="e88da-134">Wert</span><span class="sxs-lookup"><span data-stu-id="e88da-134">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e88da-135">Header</span><span class="sxs-lookup"><span data-stu-id="e88da-135">Header</span></span><br/>  | <dl> <span data-ttu-id="e88da-136"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="e88da-136"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="e88da-137">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e88da-137">Library</span></span><br/> | <dl> <span data-ttu-id="e88da-138"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e88da-138"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="e88da-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e88da-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e88da-140">ID3DXFileSaveData</span><span class="sxs-lookup"><span data-stu-id="e88da-140">ID3DXFileSaveData</span></span>](id3dxfilesavedata.md)
</dt> </dl>

 

 
