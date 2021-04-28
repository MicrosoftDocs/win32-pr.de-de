---
description: 'ID3DXFileEnumObject::GetChild-Methode: Ruft ein untergeordnetes Objekt in diesem Dateidatenobjekt ab.'
ms.assetid: d8f367dd-8858-48ae-9de5-17de1538aadf
title: ID3DXFileEnumObject::GetChild-Methode (D3DX9Xof.h)
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
ms.openlocfilehash: b26cf058b31d1016c68cccf3dde6ade9f84cde1d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090358"
---
# <a name="id3dxfileenumobjectgetchild-method"></a><span data-ttu-id="7caed-103">ID3DXFileEnumObject::GetChild-Methode</span><span class="sxs-lookup"><span data-stu-id="7caed-103">ID3DXFileEnumObject::GetChild method</span></span>

<span data-ttu-id="7caed-104">Ruft ein untergeordnetes Objekt in diesem Dateidatenobjekt ab.</span><span class="sxs-lookup"><span data-stu-id="7caed-104">Retrieves a child object in this file data object.</span></span>

## <a name="syntax"></a><span data-ttu-id="7caed-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7caed-105">Syntax</span></span>


```C++
HRESULT GetChild(
  [in]  SIZE_T        id,
  [out] ID3DXFileData **ppObj
);
```



## <a name="parameters"></a><span data-ttu-id="7caed-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7caed-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7caed-107">*id* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7caed-107">*id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7caed-108">Typ: **[ **SIZE \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7caed-108">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7caed-109">ID des abzurufenden untergeordneten Objekts.</span><span class="sxs-lookup"><span data-stu-id="7caed-109">ID of the child object to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="7caed-110">*ppObj* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="7caed-110">*ppObj* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7caed-111">Typ: **[ **ID3DXFileData**](id3dxfiledata.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="7caed-111">Type: **[**ID3DXFileData**](id3dxfiledata.md)\*\***</span></span>

<span data-ttu-id="7caed-112">Adresse eines Zeigers zum Empfangen des Schnittstellenzeigers des untergeordneten Objekts.</span><span class="sxs-lookup"><span data-stu-id="7caed-112">Address of a pointer to receive the child object's interface pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7caed-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7caed-113">Return value</span></span>

<span data-ttu-id="7caed-114">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7caed-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7caed-115">Wenn die Methode erfolgreich ist, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7caed-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="7caed-116">Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert einer der folgenden Sein: D3DXFERR \_ BADVALUE, D3DXFERR \_ NOMOREOBJECTS.</span><span class="sxs-lookup"><span data-stu-id="7caed-116">If the method fails, the return value can be one of the following: D3DXFERR\_BADVALUE, D3DXFERR\_NOMOREOBJECTS.</span></span>

## <a name="requirements"></a><span data-ttu-id="7caed-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7caed-117">Requirements</span></span>



| <span data-ttu-id="7caed-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7caed-118">Requirement</span></span> | <span data-ttu-id="7caed-119">Wert</span><span class="sxs-lookup"><span data-stu-id="7caed-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7caed-120">Header</span><span class="sxs-lookup"><span data-stu-id="7caed-120">Header</span></span><br/>  | <dl> <span data-ttu-id="7caed-121"><dt>D3DX9Xof.h</dt></span><span class="sxs-lookup"><span data-stu-id="7caed-121"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="7caed-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7caed-122">Library</span></span><br/> | <dl> <span data-ttu-id="7caed-123"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="7caed-123"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="7caed-124">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="7caed-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7caed-125">ID3DXFileEnumObject</span><span class="sxs-lookup"><span data-stu-id="7caed-125">ID3DXFileEnumObject</span></span>](id3dxfileenumobject.md)
</dt> </dl>

 

 
