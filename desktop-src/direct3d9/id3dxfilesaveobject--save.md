---
description: Speichert ein Datenobjekt und seine untergeordneten Elemente in einer x-Datei auf dem Datenträger.
ms.assetid: a48cd1b2-d1e7-446b-8482-485ccdd59353
title: 'ID3DXFileSaveObject:: Save-Methode (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveObject.Save
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: c97c2ccf6c509aec1d217e3179c927fe2bb5a797
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394125"
---
# <a name="id3dxfilesaveobjectsave-method"></a><span data-ttu-id="09894-103">ID3DXFileSaveObject:: Save-Methode</span><span class="sxs-lookup"><span data-stu-id="09894-103">ID3DXFileSaveObject::Save method</span></span>

<span data-ttu-id="09894-104">Speichert ein Datenobjekt und seine untergeordneten Elemente in einer x-Datei auf dem Datenträger.</span><span class="sxs-lookup"><span data-stu-id="09894-104">Saves a data object and its children to a .x file on disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="09894-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="09894-105">Syntax</span></span>


```C++
HRESULT Save();
```



## <a name="parameters"></a><span data-ttu-id="09894-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="09894-106">Parameters</span></span>

<span data-ttu-id="09894-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="09894-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="09894-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="09894-108">Return value</span></span>

<span data-ttu-id="09894-109">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="09894-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="09894-110">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="09894-110">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="09894-111">Wenn die Methode fehlschlägt, kann der Rückgabewert wie folgt lauten: D3DXFERR \_ badobject.</span><span class="sxs-lookup"><span data-stu-id="09894-111">If the method fails, the return value can be the following: D3DXFERR\_BADOBJECT.</span></span>

## <a name="remarks"></a><span data-ttu-id="09894-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="09894-112">Remarks</span></span>

<span data-ttu-id="09894-113">Nachdem diese Methode erfolgreich ausgeführt wurde, können [**ID3DXFileSaveObject:: adddataobject**](id3dxfilesaveobject--adddataobject.md), [**ID3DXFileSaveData:: adddataobject**](id3dxfilesavedata--adddataobject.md) und [**ID3DXFileSaveData:: adddatareferenzierungsart**](id3dxfilesavedata--adddatareference.md) nicht mehr aufgerufen werden, bis ein neues [**ID3DXFile**](id3dxfile.md) -Objekt erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="09894-113">After this method succeeds, [**ID3DXFileSaveObject::AddDataObject**](id3dxfilesaveobject--adddataobject.md), [**ID3DXFileSaveData::AddDataObject**](id3dxfilesavedata--adddataobject.md) and [**ID3DXFileSaveData::AddDataReference**](id3dxfilesavedata--adddatareference.md) can no longer be called until a new [**ID3DXFile**](id3dxfile.md) object is created.</span></span>

## <a name="requirements"></a><span data-ttu-id="09894-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="09894-114">Requirements</span></span>



| <span data-ttu-id="09894-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="09894-115">Requirement</span></span> | <span data-ttu-id="09894-116">Wert</span><span class="sxs-lookup"><span data-stu-id="09894-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="09894-117">Header</span><span class="sxs-lookup"><span data-stu-id="09894-117">Header</span></span><br/>  | <dl> <span data-ttu-id="09894-118"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="09894-118"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="09894-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="09894-119">Library</span></span><br/> | <dl> <span data-ttu-id="09894-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="09894-120"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="09894-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="09894-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09894-122">ID3DXFileSaveObject</span><span class="sxs-lookup"><span data-stu-id="09894-122">ID3DXFileSaveObject</span></span>](id3dxfilesaveobject.md)
</dt> </dl>

 

 




