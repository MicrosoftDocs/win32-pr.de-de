---
description: Speichert Vorlagen in einer DirectX-Datei. Veraltet.
ms.assetid: 7a45565a-8c04-4fa1-a424-294b847d3a2f
title: 'Idirectxfilesaveobject:: savetemplates-Methode (dxfile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileSaveObject.SaveTemplates
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 3c63ae2e0f211aa8e7064161d03a66cafe1e8289
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354667"
---
# <a name="idirectxfilesaveobjectsavetemplates-method"></a><span data-ttu-id="93e91-104">Idirectxfilesaveobject:: savetemplates-Methode</span><span class="sxs-lookup"><span data-stu-id="93e91-104">IDirectXFileSaveObject::SaveTemplates method</span></span>

<span data-ttu-id="93e91-105">Speichert Vorlagen in einer DirectX-Datei.</span><span class="sxs-lookup"><span data-stu-id="93e91-105">Saves templates to a DirectX file.</span></span> <span data-ttu-id="93e91-106">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="93e91-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="93e91-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="93e91-107">Syntax</span></span>


```C++
HRESULT SaveTemplates(
  [in]       DWORD cTemplates,
  [in] const GUID  **ppguidTemplates
);
```



## <a name="parameters"></a><span data-ttu-id="93e91-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="93e91-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93e91-109">*ctemplates* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="93e91-109">*cTemplates* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93e91-110">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="93e91-110">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="93e91-111">Die Gesamtanzahl der zu speichernden Vorlagen.</span><span class="sxs-lookup"><span data-stu-id="93e91-111">Total number of templates to save.</span></span>

</dd> <dt>

<span data-ttu-id="93e91-112">*ppguidtemplates* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="93e91-112">*ppguidTemplates* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93e91-113">Typ: Konstante **[**GUID**](guid.md) \* \***</span><span class="sxs-lookup"><span data-stu-id="93e91-113">Type: **const [**GUID**](guid.md)\*\***</span></span>

<span data-ttu-id="93e91-114">Adresse eines Zeigers auf ein Array von GUIDs für alle zu speichernden Vorlagen.</span><span class="sxs-lookup"><span data-stu-id="93e91-114">Address of a pointer to an array of the GUIDs for all templates to save.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93e91-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="93e91-115">Return value</span></span>

<span data-ttu-id="93e91-116">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="93e91-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="93e91-117">Wenn die Methode erfolgreich ausgeführt wird, ist dxfile OK der Rückgabewert \_ .</span><span class="sxs-lookup"><span data-stu-id="93e91-117">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="93e91-118">Wenn die Methode fehlschlägt, kann der Rückgabewert dxfileerr \_ badvalue lauten.</span><span class="sxs-lookup"><span data-stu-id="93e91-118">If the method fails, the return value can be DXFILEERR\_BADVALUE.</span></span>

## <a name="remarks"></a><span data-ttu-id="93e91-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="93e91-119">Remarks</span></span>

<span data-ttu-id="93e91-120">Das folgende Code Fragment stellt einen Beispiel Aufrufe von **idirectxfilesaveobject:: savetemplates** und Beispiel Inhalt für das Array bereit, auf das ppguidtemplates zeigt.</span><span class="sxs-lookup"><span data-stu-id="93e91-120">The following code fragment provides an example call to **IDirectXFileSaveObject::SaveTemplates** and example contents for the array to which ppguidTemplates points.</span></span>


```
IDirectXFileSaveObject * pDXFileSaveObject;
    
const GUID *aIds[] = {
    &DXFILEOBJ_SimpleData,
    &DXFILEOBJ_ArrayData,
    &DXFILEOBJ_RestrictedData};
    
hr = pDXFileSaveObject->SaveTemplates(3, aIds);
```



<span data-ttu-id="93e91-121">Nachdem Sie diese Methode zum Speichern der Vorlagen verwendet haben, verwenden Sie die [**idirectxfilesaveobject:: kreatedataobject**](idirectxfilesaveobject--createdataobject.md) -Methode zum Erstellen eines Datenobjekts.</span><span class="sxs-lookup"><span data-stu-id="93e91-121">After using this method to save the templates, use the [**IDirectXFileSaveObject::CreateDataObject**](idirectxfilesaveobject--createdataobject.md) method to create a data object.</span></span>

## <a name="requirements"></a><span data-ttu-id="93e91-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="93e91-122">Requirements</span></span>



| <span data-ttu-id="93e91-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="93e91-123">Requirement</span></span> | <span data-ttu-id="93e91-124">Wert</span><span class="sxs-lookup"><span data-stu-id="93e91-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="93e91-125">Header</span><span class="sxs-lookup"><span data-stu-id="93e91-125">Header</span></span><br/>  | <dl> <span data-ttu-id="93e91-126"><dt>Dxfile. h</dt></span><span class="sxs-lookup"><span data-stu-id="93e91-126"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="93e91-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="93e91-127">Library</span></span><br/> | <dl> <span data-ttu-id="93e91-128"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="93e91-128"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93e91-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="93e91-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93e91-130">Idirectxfilesaveobject</span><span class="sxs-lookup"><span data-stu-id="93e91-130">IDirectXFileSaveObject</span></span>](idirectxfilesaveobject.md)
</dt> <dt>

[<span data-ttu-id="93e91-131">**Idirectxfilesaveobject:: kreatedataobject**</span><span class="sxs-lookup"><span data-stu-id="93e91-131">**IDirectXFileSaveObject::CreateDataObject**</span></span>](idirectxfilesaveobject--createdataobject.md)
</dt> </dl>

 

 
