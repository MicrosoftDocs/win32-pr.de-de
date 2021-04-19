---
description: 'Erzwingt, dass alle Batch-Sprites an das Gerät übermittelt werden. Gerätezustände verbleiben nach dem letzten ID3DXSprite:: begin-Rückruf. Die Liste der im Batch verarbeiteten Sprites wird dann gelöscht.'
ms.assetid: e5717bde-e339-4344-8ce7-b0c3fe118887
title: 'ID3DXSprite:: Flush-Methode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.Flush
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3bcd89984672f0dcfa2df120ede1abdfee23d171
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106367381"
---
# <a name="id3dxspriteflush-method"></a><span data-ttu-id="07835-105">ID3DXSprite:: Flush-Methode</span><span class="sxs-lookup"><span data-stu-id="07835-105">ID3DXSprite::Flush method</span></span>

<span data-ttu-id="07835-106">Erzwingt, dass alle Batch-Sprites an das Gerät übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="07835-106">Forces all batched sprites to be submitted to the device.</span></span> <span data-ttu-id="07835-107">Gerätezustände verbleiben nach dem letzten [**ID3DXSprite:: begin**](id3dxsprite--begin.md)-Rückruf.</span><span class="sxs-lookup"><span data-stu-id="07835-107">Device states remain as they were after the last call to [**ID3DXSprite::Begin**](id3dxsprite--begin.md).</span></span> <span data-ttu-id="07835-108">Die Liste der im Batch verarbeiteten Sprites wird dann gelöscht.</span><span class="sxs-lookup"><span data-stu-id="07835-108">The list of batched sprites is then cleared.</span></span>

## <a name="syntax"></a><span data-ttu-id="07835-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="07835-109">Syntax</span></span>


```C++
HRESULT Flush();
```



## <a name="parameters"></a><span data-ttu-id="07835-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="07835-110">Parameters</span></span>

<span data-ttu-id="07835-111">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="07835-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="07835-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="07835-112">Return value</span></span>

<span data-ttu-id="07835-113">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="07835-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="07835-114">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="07835-114">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="07835-115">Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben. D3DERR \_ invalidcall</span><span class="sxs-lookup"><span data-stu-id="07835-115">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="requirements"></a><span data-ttu-id="07835-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="07835-116">Requirements</span></span>



| <span data-ttu-id="07835-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="07835-117">Requirement</span></span> | <span data-ttu-id="07835-118">Wert</span><span class="sxs-lookup"><span data-stu-id="07835-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="07835-119">Header</span><span class="sxs-lookup"><span data-stu-id="07835-119">Header</span></span><br/>  | <dl> <span data-ttu-id="07835-120"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="07835-120"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="07835-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="07835-121">Library</span></span><br/> | <dl> <span data-ttu-id="07835-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="07835-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="07835-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="07835-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07835-124">ID3DXSprite</span><span class="sxs-lookup"><span data-stu-id="07835-124">ID3DXSprite</span></span>](id3dxsprite.md)
</dt> <dt>

[<span data-ttu-id="07835-125">**ID3DXSprite:: End**</span><span class="sxs-lookup"><span data-stu-id="07835-125">**ID3DXSprite::End**</span></span>](id3dxsprite--end.md)
</dt> </dl>

 

 




