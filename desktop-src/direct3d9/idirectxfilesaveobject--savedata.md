---
description: Speichert ein Datenobjekt und seine untergeordneten Elemente in einer DirectX-Datei. Veraltet.
ms.assetid: 18bd5ef6-9e17-4c21-bc14-373de8df9ffb
title: 'Idirectxfilesaveobject:: SaveData-Methode (dxfile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileSaveObject.SaveData
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: cb901bd984e1fcd923d0ea172fb5f387b3a9302a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106364359"
---
# <a name="idirectxfilesaveobjectsavedata-method"></a><span data-ttu-id="c34f2-104">Idirectxfilesaveobject:: SaveData-Methode</span><span class="sxs-lookup"><span data-stu-id="c34f2-104">IDirectXFileSaveObject::SaveData method</span></span>

<span data-ttu-id="c34f2-105">Speichert ein Datenobjekt und seine untergeordneten Elemente in einer DirectX-Datei.</span><span class="sxs-lookup"><span data-stu-id="c34f2-105">Saves a data object and its children to a DirectX file.</span></span> <span data-ttu-id="c34f2-106">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="c34f2-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="c34f2-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c34f2-107">Syntax</span></span>


```C++
HRESULT SaveData(
  [in] LPDIRECTXFILEDATA pDataObj
);
```



## <a name="parameters"></a><span data-ttu-id="c34f2-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c34f2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c34f2-109">*pdataobj* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c34f2-109">*pDataObj* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c34f2-110">Typ: **[ **lpdirectxfiledata**](idirectxfiledata.md)**</span><span class="sxs-lookup"><span data-stu-id="c34f2-110">Type: **[**LPDIRECTXFILEDATA**](idirectxfiledata.md)**</span></span>

<span data-ttu-id="c34f2-111">Zeiger auf eine [**idirectxfiledata**](idirectxfiledata.md) -Schnittstelle, die das zu speichernde Datei Datenobjekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="c34f2-111">Pointer to an [**IDirectXFileData**](idirectxfiledata.md) interface, representing the file data object to save.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c34f2-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c34f2-112">Return value</span></span>

<span data-ttu-id="c34f2-113">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c34f2-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c34f2-114">Wenn die Methode erfolgreich ausgeführt wird, ist dxfile OK der Rückgabewert \_ .</span><span class="sxs-lookup"><span data-stu-id="c34f2-114">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="c34f2-115">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: dxfileerr \_ badarraysize, dxfileerr \_ badvalue.</span><span class="sxs-lookup"><span data-stu-id="c34f2-115">If the method fails, the return value can be one of the following values: DXFILEERR\_BADARRAYSIZE, DXFILEERR\_BADVALUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="c34f2-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c34f2-116">Requirements</span></span>



| <span data-ttu-id="c34f2-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c34f2-117">Requirement</span></span> | <span data-ttu-id="c34f2-118">Wert</span><span class="sxs-lookup"><span data-stu-id="c34f2-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c34f2-119">Header</span><span class="sxs-lookup"><span data-stu-id="c34f2-119">Header</span></span><br/>  | <dl> <span data-ttu-id="c34f2-120"><dt>Dxfile. h</dt></span><span class="sxs-lookup"><span data-stu-id="c34f2-120"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="c34f2-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c34f2-121">Library</span></span><br/> | <dl> <span data-ttu-id="c34f2-122"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c34f2-122"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c34f2-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c34f2-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c34f2-124">Idirectxfilesaveobject</span><span class="sxs-lookup"><span data-stu-id="c34f2-124">IDirectXFileSaveObject</span></span>](idirectxfilesaveobject.md)
</dt> </dl>

 

 




