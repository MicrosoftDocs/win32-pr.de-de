---
description: 'Beendet die Lebensdauer des ppData-Zeigers, der von ID3DXFileData:: Lock zurückgegeben wurde.'
ms.assetid: 6032ea1f-3c73-4157-ba3f-41ce9e73d64c
title: 'ID3DXFileData:: Unlock-Methode (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.Unlock
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 8371b87152a6184f34a225b24d2de1b0fd21248f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762141"
---
# <a name="id3dxfiledataunlock-method"></a><span data-ttu-id="6f386-103">ID3DXFileData:: Unlock-Methode</span><span class="sxs-lookup"><span data-stu-id="6f386-103">ID3DXFileData::Unlock method</span></span>

<span data-ttu-id="6f386-104">Beendet die Lebensdauer des *ppData* -Zeigers, der von [**ID3DXFileData:: Lock**](id3dxfiledata--lock.md)zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="6f386-104">Ends the lifespan of the *ppData* pointer returned by [**ID3DXFileData::Lock**](id3dxfiledata--lock.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="6f386-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6f386-105">Syntax</span></span>


```C++
BOOL Unlock();
```



## <a name="parameters"></a><span data-ttu-id="6f386-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6f386-106">Parameters</span></span>

<span data-ttu-id="6f386-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="6f386-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6f386-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6f386-108">Return value</span></span>

<span data-ttu-id="6f386-109">Typ: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6f386-109">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6f386-110">Der Rückgabewert ist "S \_ OK".</span><span class="sxs-lookup"><span data-stu-id="6f386-110">The return value is S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f386-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6f386-111">Remarks</span></span>

<span data-ttu-id="6f386-112">Sie müssen sicherstellen, dass die Anzahl von [**ID3DXFileData:: Lock**](id3dxfiledata--lock.md) -aufrufen mit der Anzahl von **ID3DXFileData:: Unlock** -aufrufen übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="6f386-112">You must ensure that the number of [**ID3DXFileData::Lock**](id3dxfiledata--lock.md) calls matches the number of **ID3DXFileData::Unlock** calls.</span></span> <span data-ttu-id="6f386-113">Nach dem Aufrufen von Unlock sollte der von **ID3DXFileData:: Lock** zurückgegebene ppData-Zeiger nicht mehr verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6f386-113">After calling Unlock, the ppData pointer returned by **ID3DXFileData::Lock** should no longer be used.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f386-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6f386-114">Requirements</span></span>



| <span data-ttu-id="6f386-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6f386-115">Requirement</span></span> | <span data-ttu-id="6f386-116">Wert</span><span class="sxs-lookup"><span data-stu-id="6f386-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6f386-117">Header</span><span class="sxs-lookup"><span data-stu-id="6f386-117">Header</span></span><br/>  | <dl> <span data-ttu-id="6f386-118"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f386-118"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="6f386-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6f386-119">Library</span></span><br/> | <dl> <span data-ttu-id="6f386-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6f386-120"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="6f386-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6f386-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f386-122">ID3DXFileData</span><span class="sxs-lookup"><span data-stu-id="6f386-122">ID3DXFileData</span></span>](id3dxfiledata.md)
</dt> </dl>

 

 
