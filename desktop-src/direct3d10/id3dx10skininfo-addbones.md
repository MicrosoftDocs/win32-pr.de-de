---
description: Speicherplatz für weitere Knochen zuweisen.
ms.assetid: f2acd338-f2c2-4340-a673-f36940cf31d9
title: 'ID3DX10SkinInfo:: addbones-Methode (d3dx10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.AddBones
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 4bf9667bd25dd717c4da96c2150e7bd7c45964f8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354937"
---
# <a name="id3dx10skininfoaddbones-method"></a><span data-ttu-id="e7aa1-103">ID3DX10SkinInfo:: addbones-Methode</span><span class="sxs-lookup"><span data-stu-id="e7aa1-103">ID3DX10SkinInfo::AddBones method</span></span>

<span data-ttu-id="e7aa1-104">Speicherplatz für weitere Knochen zuweisen.</span><span class="sxs-lookup"><span data-stu-id="e7aa1-104">Allocate space for more bones.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7aa1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e7aa1-105">Syntax</span></span>


```C++
HRESULT AddBones(
  [in] UINT Count
);
```



## <a name="parameters"></a><span data-ttu-id="e7aa1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e7aa1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7aa1-107">*Anzahl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e7aa1-107">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7aa1-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e7aa1-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e7aa1-109">Die Anzahl der hinzu zufügenden Knochen.</span><span class="sxs-lookup"><span data-stu-id="e7aa1-109">The number of bones to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7aa1-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e7aa1-110">Return value</span></span>

<span data-ttu-id="e7aa1-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e7aa1-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e7aa1-112">Wenn diese Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e7aa1-112">If this method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="e7aa1-113">Wenn die Methode fehlschlägt, kann der Rückgabewert lauten: E \_ outo-Memory.</span><span class="sxs-lookup"><span data-stu-id="e7aa1-113">If the method fails, the return value can be: E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7aa1-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e7aa1-114">Requirements</span></span>



| <span data-ttu-id="e7aa1-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e7aa1-115">Requirement</span></span> | <span data-ttu-id="e7aa1-116">Wert</span><span class="sxs-lookup"><span data-stu-id="e7aa1-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e7aa1-117">Header</span><span class="sxs-lookup"><span data-stu-id="e7aa1-117">Header</span></span><br/>  | <dl> <span data-ttu-id="e7aa1-118"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7aa1-118"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="e7aa1-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e7aa1-119">Library</span></span><br/> | <dl> <span data-ttu-id="e7aa1-120"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e7aa1-120"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7aa1-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e7aa1-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7aa1-122">ID3DX10SkinInfo</span><span class="sxs-lookup"><span data-stu-id="e7aa1-122">ID3DX10SkinInfo</span></span>](id3dx10skininfo.md)
</dt> <dt>

[<span data-ttu-id="e7aa1-123">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="e7aa1-123">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
