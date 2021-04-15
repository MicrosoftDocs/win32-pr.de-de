---
description: Registriert benutzerdefinierte Vorlagen bei Angabe eines ID3DXFileEnumObject-Enumerationsobjekt.
ms.assetid: 1b0c71db-639b-4836-8a65-7d0a2ed3ba4f
title: 'ID3DXFile:: registerenumtemplates-Methode (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFile.RegisterEnumTemplates
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 89a8b136bdc0e202fc87ba8fd4d7f013203814eb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394178"
---
# <a name="id3dxfileregisterenumtemplates-method"></a><span data-ttu-id="0c200-103">ID3DXFile:: registerenumtemplates-Methode</span><span class="sxs-lookup"><span data-stu-id="0c200-103">ID3DXFile::RegisterEnumTemplates method</span></span>

<span data-ttu-id="0c200-104">Registriert benutzerdefinierte Vorlagen bei Angabe eines [**ID3DXFileEnumObject**](id3dxfileenumobject.md) -Enumerationsobjekt.</span><span class="sxs-lookup"><span data-stu-id="0c200-104">Registers custom templates, given an [**ID3DXFileEnumObject**](id3dxfileenumobject.md) enumeration object.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c200-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0c200-105">Syntax</span></span>


```C++
HRESULT RegisterEnumTemplates(
  [in] ID3DXFileEnumObject *pEnum
);
```



## <a name="parameters"></a><span data-ttu-id="0c200-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0c200-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c200-107">"- *ID* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="0c200-107">*pEnum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c200-108">Typ: **[ **ID3DXFileEnumObject**](id3dxfileenumobject.md)\***</span><span class="sxs-lookup"><span data-stu-id="0c200-108">Type: **[**ID3DXFileEnumObject**](id3dxfileenumobject.md)\***</span></span>

<span data-ttu-id="0c200-109">Zeiger auf ein [**ID3DXFileEnumObject**](id3dxfileenumobject.md) -Enumerationsobjekt, das Vorlagen enthält.</span><span class="sxs-lookup"><span data-stu-id="0c200-109">Pointer to an [**ID3DXFileEnumObject**](id3dxfileenumobject.md) enumeration object that contains templates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c200-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0c200-110">Return value</span></span>

<span data-ttu-id="0c200-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0c200-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0c200-112">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0c200-112">If the method succeeds, the return value is S\_OK .</span></span>

<span data-ttu-id="0c200-113">Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben: D3DXFERR \_ badvalue.</span><span class="sxs-lookup"><span data-stu-id="0c200-113">If the method fails, the following value will be returned: D3DXFERR\_BADVALUE.</span></span>

## <a name="remarks"></a><span data-ttu-id="0c200-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0c200-114">Remarks</span></span>

<span data-ttu-id="0c200-115">Wenn diese Methode aufgerufen wird, kopiert Sie Vorlagen, die mit dem ID3DXFileEnumObject, das die Datei darstellt, in den lokalen Vorlagen Speicher des [**ID3DXFile**](id3dxfile.md) -Objekts.</span><span class="sxs-lookup"><span data-stu-id="0c200-115">When this method is called, it copies templates stored with the ID3DXFileEnumObject, representing the file, to the local template store of the [**ID3DXFile**](id3dxfile.md) object.</span></span>

<span data-ttu-id="0c200-116">Wenn ein [**ID3DXFileEnumObject**](id3dxfileenumobject.md) -Zeiger nicht verfügbar ist, sollten Sie stattdessen die [**registertemplates**](id3dxfile--registertemplates.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="0c200-116">If an [**ID3DXFileEnumObject**](id3dxfileenumobject.md) pointer is not available, call the [**RegisterTemplates**](id3dxfile--registertemplates.md) method instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c200-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0c200-117">Requirements</span></span>



| <span data-ttu-id="0c200-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0c200-118">Requirement</span></span> | <span data-ttu-id="0c200-119">Wert</span><span class="sxs-lookup"><span data-stu-id="0c200-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0c200-120">Header</span><span class="sxs-lookup"><span data-stu-id="0c200-120">Header</span></span><br/>  | <dl> <span data-ttu-id="0c200-121"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c200-121"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="0c200-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0c200-122">Library</span></span><br/> | <dl> <span data-ttu-id="0c200-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0c200-123"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="0c200-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0c200-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c200-125">ID3DXFile</span><span class="sxs-lookup"><span data-stu-id="0c200-125">ID3DXFile</span></span>](id3dxfile.md)
</dt> <dt>

[<span data-ttu-id="0c200-126">**Register Templates**</span><span class="sxs-lookup"><span data-stu-id="0c200-126">**RegisterTemplates**</span></span>](id3dxfile--registertemplates.md)
</dt> </dl>

 

 




