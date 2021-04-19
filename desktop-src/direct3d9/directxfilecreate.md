---
description: Erstellt eine Instanz eines directxfile-Objekts. Veraltet.
ms.assetid: c920d480-2557-491d-87ea-7eea1f470498
title: Directxfilecreate-Funktion (dxfile. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DirectXFileCreate
api_type:
- DllExport
api_location:
- d3dxof.dll
ms.openlocfilehash: 8ee1787941bbb902e6f0f50b082867aaf2f0a8bc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106363962"
---
# <a name="directxfilecreate-function"></a><span data-ttu-id="4408b-104">Directxfilecreate-Funktion</span><span class="sxs-lookup"><span data-stu-id="4408b-104">DirectXFileCreate function</span></span>

<span data-ttu-id="4408b-105">Erstellt eine Instanz eines directxfile-Objekts.</span><span class="sxs-lookup"><span data-stu-id="4408b-105">Creates an instance of a DirectXFile object.</span></span> <span data-ttu-id="4408b-106">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="4408b-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="4408b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="4408b-107">Syntax</span></span>


```C++
HRESULT STDAPICALLTYPE DirectXFileCreate(
   LPDIRECTXFILE *lplpDirectXFile
);
```



## <a name="parameters"></a><span data-ttu-id="4408b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="4408b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4408b-109">*lplpdirectxfile*</span><span class="sxs-lookup"><span data-stu-id="4408b-109">*lplpDirectXFile*</span></span> 
</dt> <dd>

<span data-ttu-id="4408b-110">Typ: **[ **lpdirectxfile**](idirectxfile.md)\***</span><span class="sxs-lookup"><span data-stu-id="4408b-110">Type: **[**LPDIRECTXFILE**](idirectxfile.md)\***</span></span>

<span data-ttu-id="4408b-111">Adresse eines Zeigers auf eine [**idirectxfile**](idirectxfile.md) -Schnittstelle, die das erstellte directxfile-Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="4408b-111">Address of a pointer to an [**IDirectXFile**](idirectxfile.md) interface, representing the created DirectXFile object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4408b-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4408b-112">Return value</span></span>

<span data-ttu-id="4408b-113">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4408b-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4408b-114">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4408b-114">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="4408b-115">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: dxfileerr \_ badzuzuweisung, dxfileerr \_ badvalue.</span><span class="sxs-lookup"><span data-stu-id="4408b-115">If the function fails, the return value can be one of the following: DXFILEERR\_BADALLOC, DXFILEERR\_BADVALUE.</span></span>

## <a name="remarks"></a><span data-ttu-id="4408b-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4408b-116">Remarks</span></span>

<span data-ttu-id="4408b-117">Nachdem Sie diese Funktion verwendet haben, verwenden Sie [**registertemplates**](idirectxfile--registertemplates.md) , um Vorlagen zu [**registrieren, und erstellen Sie ein**](idirectxfile--createenumobject.md) Enumeratorobjekt mit dem Befehl "" [**, oder erstellen Sie ein**](idirectxfile--createsaveobject.md) "Save"-Objekt.</span><span class="sxs-lookup"><span data-stu-id="4408b-117">After using this function, use [**RegisterTemplates**](idirectxfile--registertemplates.md) to register templates, [**CreateEnumObject**](idirectxfile--createenumobject.md) to create an enumerator object, or [**CreateSaveObject**](idirectxfile--createsaveobject.md) to create a save object.</span></span>

## <a name="requirements"></a><span data-ttu-id="4408b-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4408b-118">Requirements</span></span>



| <span data-ttu-id="4408b-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4408b-119">Requirement</span></span> | <span data-ttu-id="4408b-120">Wert</span><span class="sxs-lookup"><span data-stu-id="4408b-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4408b-121">Header</span><span class="sxs-lookup"><span data-stu-id="4408b-121">Header</span></span><br/>  | <dl> <span data-ttu-id="4408b-122"><dt>Dxfile. h</dt></span><span class="sxs-lookup"><span data-stu-id="4408b-122"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="4408b-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4408b-123">Library</span></span><br/> | <dl> <span data-ttu-id="4408b-124"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4408b-124"><dt>D3dxof.lib</dt></span></span> </dl> |
| <span data-ttu-id="4408b-125">DLL</span><span class="sxs-lookup"><span data-stu-id="4408b-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="4408b-126"><dt>D3dxof.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4408b-126"><dt>D3dxof.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4408b-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4408b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4408b-128">X-Dateifunktionen</span><span class="sxs-lookup"><span data-stu-id="4408b-128">X File Functions</span></span>](dx9-graphics-reference-x-file-functions.md)
</dt> <dt>

[<span data-ttu-id="4408b-129">**"Kreateendumuject"**</span><span class="sxs-lookup"><span data-stu-id="4408b-129">**CreateEnumObject**</span></span>](idirectxfile--createenumobject.md)
</dt> <dt>

[<span data-ttu-id="4408b-130">**"Kreatesaveobject"**</span><span class="sxs-lookup"><span data-stu-id="4408b-130">**CreateSaveObject**</span></span>](idirectxfile--createsaveobject.md)
</dt> <dt>

[<span data-ttu-id="4408b-131">**Register Templates**</span><span class="sxs-lookup"><span data-stu-id="4408b-131">**RegisterTemplates**</span></span>](idirectxfile--registertemplates.md)
</dt> </dl>

 

 




