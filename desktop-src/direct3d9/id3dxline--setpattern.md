---
description: Wendet ein stippingmuster auf die Zeile an.
ms.assetid: 53548a9f-cf09-4ab9-9327-d5053645fc1b
title: 'ID3DXLine:: SetPattern-Methode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.SetPattern
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 80a0485991bc06bdb9fcd3280017d4cc60b492ca
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104132389"
---
# <a name="id3dxlinesetpattern-method"></a><span data-ttu-id="599b1-103">ID3DXLine:: SetPattern-Methode</span><span class="sxs-lookup"><span data-stu-id="599b1-103">ID3DXLine::SetPattern method</span></span>

<span data-ttu-id="599b1-104">Wendet ein stippingmuster auf die Zeile an.</span><span class="sxs-lookup"><span data-stu-id="599b1-104">Applies a stipple pattern to the line.</span></span>

## <a name="syntax"></a><span data-ttu-id="599b1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="599b1-105">Syntax</span></span>


```C++
HRESULT SetPattern(
  [in] DWORD dwPattern
);
```



## <a name="parameters"></a><span data-ttu-id="599b1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="599b1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="599b1-107">*dwpattern* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="599b1-107">*dwPattern* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="599b1-108">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="599b1-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="599b1-109">Beschreibt das Stippel Muster: 1 ist undurchsichtig, 0 ist transparent.</span><span class="sxs-lookup"><span data-stu-id="599b1-109">Describes the stipple pattern: 1 is opaque, 0 is transparent.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="599b1-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="599b1-110">Return value</span></span>

<span data-ttu-id="599b1-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="599b1-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="599b1-112">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="599b1-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="599b1-113">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData.</span><span class="sxs-lookup"><span data-stu-id="599b1-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="599b1-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="599b1-114">Requirements</span></span>



| <span data-ttu-id="599b1-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="599b1-115">Requirement</span></span> | <span data-ttu-id="599b1-116">Wert</span><span class="sxs-lookup"><span data-stu-id="599b1-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="599b1-117">Header</span><span class="sxs-lookup"><span data-stu-id="599b1-117">Header</span></span><br/>  | <dl> <span data-ttu-id="599b1-118"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="599b1-118"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="599b1-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="599b1-119">Library</span></span><br/> | <dl> <span data-ttu-id="599b1-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="599b1-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="599b1-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="599b1-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="599b1-122">ID3DXLine</span><span class="sxs-lookup"><span data-stu-id="599b1-122">ID3DXLine</span></span>](id3dxline.md)
</dt> </dl>

 

 
