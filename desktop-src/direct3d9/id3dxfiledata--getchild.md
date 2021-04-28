---
description: 'ID3DXFileData::GetChild-Methode: Ruft ein untergeordnetes Objekt in diesem Dateidatenobjekt ab.'
ms.assetid: 0c4f1efa-f096-443d-a482-a3c5a9138c3d
title: ID3DXFileData::GetChild-Methode (D3DX9Xof.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.GetChild
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 7fe6c0393e5cfb9ed8aeaf5808d33175e7f9bfe5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090378"
---
# <a name="id3dxfiledatagetchild-method"></a><span data-ttu-id="b53e6-103">ID3DXFileData::GetChild-Methode</span><span class="sxs-lookup"><span data-stu-id="b53e6-103">ID3DXFileData::GetChild method</span></span>

<span data-ttu-id="b53e6-104">Ruft ein untergeordnetes Objekt in diesem Dateidatenobjekt ab.</span><span class="sxs-lookup"><span data-stu-id="b53e6-104">Retrieves a child object in this file data object.</span></span>

## <a name="syntax"></a><span data-ttu-id="b53e6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b53e6-105">Syntax</span></span>


```C++
HRESULT GetChild(
  [in] SIZE_T        uiChild,
  [in] ID3DXFileData **ppChild
);
```



## <a name="parameters"></a><span data-ttu-id="b53e6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b53e6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b53e6-107">*uiChild* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="b53e6-107">*uiChild* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b53e6-108">Typ: **[ **SIZE \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b53e6-108">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b53e6-109">ID des abzurufenden untergeordneten Objekts.</span><span class="sxs-lookup"><span data-stu-id="b53e6-109">ID of the child object to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="b53e6-110">*ppChild* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="b53e6-110">*ppChild* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b53e6-111">Typ: **[ **ID3DXFileData**](id3dxfiledata.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="b53e6-111">Type: **[**ID3DXFileData**](id3dxfiledata.md)\*\***</span></span>

<span data-ttu-id="b53e6-112">Adresse eines Zeigers zum Empfangen des Schnittstellenzeigers des untergeordneten Objekts.</span><span class="sxs-lookup"><span data-stu-id="b53e6-112">Address of a pointer to receive the child object's interface pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b53e6-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b53e6-113">Return value</span></span>

<span data-ttu-id="b53e6-114">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b53e6-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b53e6-115">Wenn die Methode erfolgreich ist, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b53e6-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="b53e6-116">Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert einer der folgenden Werte sein: D3DXFERR \_ BADVALUE, D3DXFERR \_ NOMOREOBJECTS.</span><span class="sxs-lookup"><span data-stu-id="b53e6-116">If the method fails, the return value can be one of the following values: D3DXFERR\_BADVALUE, D3DXFERR\_NOMOREOBJECTS.</span></span>

## <a name="requirements"></a><span data-ttu-id="b53e6-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b53e6-117">Requirements</span></span>



| <span data-ttu-id="b53e6-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b53e6-118">Requirement</span></span> | <span data-ttu-id="b53e6-119">Wert</span><span class="sxs-lookup"><span data-stu-id="b53e6-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b53e6-120">Header</span><span class="sxs-lookup"><span data-stu-id="b53e6-120">Header</span></span><br/>  | <dl> <span data-ttu-id="b53e6-121"><dt>D3DX9Xof.h</dt></span><span class="sxs-lookup"><span data-stu-id="b53e6-121"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="b53e6-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b53e6-122">Library</span></span><br/> | <dl> <span data-ttu-id="b53e6-123"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="b53e6-123"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="b53e6-124">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b53e6-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b53e6-125">ID3DXFileData</span><span class="sxs-lookup"><span data-stu-id="b53e6-125">ID3DXFileData</span></span>](id3dxfiledata.md)
</dt> </dl>

 

 
