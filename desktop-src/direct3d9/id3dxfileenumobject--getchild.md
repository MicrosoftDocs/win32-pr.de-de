---
description: Ruft ein untergeordnetes-Objekt in diesem Datei Datenobjekt ab.
ms.assetid: d8f367dd-8858-48ae-9de5-17de1538aadf
title: 'ID3DXFileEnumObject:: GetChild-Methode (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileEnumObject.GetChild
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b5b8d535a9060e80318d4043af6362810023b9d0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106365112"
---
# <a name="id3dxfileenumobjectgetchild-method"></a><span data-ttu-id="70328-103">ID3DXFileEnumObject:: GetChild-Methode</span><span class="sxs-lookup"><span data-stu-id="70328-103">ID3DXFileEnumObject::GetChild method</span></span>

<span data-ttu-id="70328-104">Ruft ein untergeordnetes-Objekt in diesem Datei Datenobjekt ab.</span><span class="sxs-lookup"><span data-stu-id="70328-104">Retrieves a child object in this file data object.</span></span>

## <a name="syntax"></a><span data-ttu-id="70328-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="70328-105">Syntax</span></span>


```C++
HRESULT GetChild(
  [in]  SIZE_T        id,
  [out] ID3DXFileData **ppObj
);
```



## <a name="parameters"></a><span data-ttu-id="70328-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="70328-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70328-107">*ID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="70328-107">*id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70328-108">Typ: **[ **Größe \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="70328-108">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="70328-109">ID des abzurufenden untergeordneten Objekts.</span><span class="sxs-lookup"><span data-stu-id="70328-109">ID of the child object to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="70328-110">*ppobj* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="70328-110">*ppObj* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="70328-111">Typ: **[ **ID3DXFileData**](id3dxfiledata.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="70328-111">Type: **[**ID3DXFileData**](id3dxfiledata.md)\*\***</span></span>

<span data-ttu-id="70328-112">Adresse eines Zeigers, der den Schnittstellen Zeiger des untergeordneten Objekts empfängt.</span><span class="sxs-lookup"><span data-stu-id="70328-112">Address of a pointer to receive the child object's interface pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70328-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="70328-113">Return value</span></span>

<span data-ttu-id="70328-114">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="70328-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="70328-115">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="70328-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="70328-116">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DXFERR \_ badvalue, D3DXFERR \_ nomoreobjects.</span><span class="sxs-lookup"><span data-stu-id="70328-116">If the method fails, the return value can be one of the following: D3DXFERR\_BADVALUE, D3DXFERR\_NOMOREOBJECTS.</span></span>

## <a name="requirements"></a><span data-ttu-id="70328-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="70328-117">Requirements</span></span>



| <span data-ttu-id="70328-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="70328-118">Requirement</span></span> | <span data-ttu-id="70328-119">Wert</span><span class="sxs-lookup"><span data-stu-id="70328-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="70328-120">Header</span><span class="sxs-lookup"><span data-stu-id="70328-120">Header</span></span><br/>  | <dl> <span data-ttu-id="70328-121"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="70328-121"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="70328-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="70328-122">Library</span></span><br/> | <dl> <span data-ttu-id="70328-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="70328-123"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="70328-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="70328-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70328-125">ID3DXFileEnumObject</span><span class="sxs-lookup"><span data-stu-id="70328-125">ID3DXFileEnumObject</span></span>](id3dxfileenumobject.md)
</dt> </dl>

 

 
