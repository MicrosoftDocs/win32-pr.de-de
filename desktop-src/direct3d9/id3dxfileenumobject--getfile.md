---
description: Ruft das ID3DXFile-Objekt ab.
ms.assetid: 832878c6-73a4-400a-af30-57112b172977
title: 'ID3DXFileEnumObject:: GetFile-Methode (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileEnumObject.GetFile
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: d3b5d672ca9b462e08c75a6f3352b01b07ead43c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961658"
---
# <a name="id3dxfileenumobjectgetfile-method"></a><span data-ttu-id="24d05-103">ID3DXFileEnumObject:: GetFile-Methode</span><span class="sxs-lookup"><span data-stu-id="24d05-103">ID3DXFileEnumObject::GetFile method</span></span>

<span data-ttu-id="24d05-104">Ruft das [**ID3DXFile**](id3dxfile.md) -Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="24d05-104">Retrieves the [**ID3DXFile**](id3dxfile.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="24d05-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="24d05-105">Syntax</span></span>


```C++
HRESULT GetFile(
  [out] ID3DXFile **ppFile
);
```



## <a name="parameters"></a><span data-ttu-id="24d05-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="24d05-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24d05-107">*ppfile* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="24d05-107">*ppFile* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="24d05-108">Typ: **[ **ID3DXFile**](id3dxfile.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="24d05-108">Type: **[**ID3DXFile**](id3dxfile.md)\*\***</span></span>

<span data-ttu-id="24d05-109">Adresse eines Zeigers auf eine [**ID3DXFile**](id3dxfile.md) -Schnittstelle, die das zurückgegebene Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="24d05-109">Address of a pointer to an [**ID3DXFile**](id3dxfile.md) interface, representing the returned object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24d05-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="24d05-110">Return value</span></span>

<span data-ttu-id="24d05-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="24d05-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="24d05-112">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="24d05-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="24d05-113">Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben: D3DXFERR \_ badvalue.</span><span class="sxs-lookup"><span data-stu-id="24d05-113">If the method fails, the following value will be returned: D3DXFERR\_BADVALUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="24d05-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="24d05-114">Requirements</span></span>



| <span data-ttu-id="24d05-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="24d05-115">Requirement</span></span> | <span data-ttu-id="24d05-116">Wert</span><span class="sxs-lookup"><span data-stu-id="24d05-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="24d05-117">Header</span><span class="sxs-lookup"><span data-stu-id="24d05-117">Header</span></span><br/>  | <dl> <span data-ttu-id="24d05-118"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="24d05-118"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="24d05-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="24d05-119">Library</span></span><br/> | <dl> <span data-ttu-id="24d05-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="24d05-120"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="24d05-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="24d05-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24d05-122">ID3DXFileEnumObject</span><span class="sxs-lookup"><span data-stu-id="24d05-122">ID3DXFileEnumObject</span></span>](id3dxfileenumobject.md)
</dt> </dl>

 

 




