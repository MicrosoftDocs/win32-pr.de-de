---
description: 'Erzwingen, dass alle Batch-Sprites an das Gerät übermittelt werden. Gerätezustände verbleiben nach dem letzten ID3DX10Sprite:: begin-Rückruf. Die Liste der im Batch verarbeiteten Sprites wird dann gelöscht.'
ms.assetid: ae03e17c-1a14-4a41-a9a9-8757d2f7a81d
title: 'ID3DX10Sprite:: Flush-Methode (d3dx10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.Flush
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 748be56a7b89223db1957b9c0144143edd90ee4c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106369344"
---
# <a name="id3dx10spriteflush-method"></a><span data-ttu-id="4986b-105">ID3DX10Sprite:: Flush-Methode</span><span class="sxs-lookup"><span data-stu-id="4986b-105">ID3DX10Sprite::Flush method</span></span>

<span data-ttu-id="4986b-106">Erzwingen, dass alle Batch-Sprites an das Gerät übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="4986b-106">Force all batched sprites to be submitted to the device.</span></span> <span data-ttu-id="4986b-107">Gerätezustände verbleiben nach dem letzten ID3DX10Sprite:: begin-Rückruf.</span><span class="sxs-lookup"><span data-stu-id="4986b-107">Device states remain as they were after the last call to ID3DX10Sprite::Begin.</span></span> <span data-ttu-id="4986b-108">Die Liste der im Batch verarbeiteten Sprites wird dann gelöscht.</span><span class="sxs-lookup"><span data-stu-id="4986b-108">The list of batched sprites is then cleared.</span></span>

## <a name="syntax"></a><span data-ttu-id="4986b-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="4986b-109">Syntax</span></span>


```C++
HRESULT Flush();
```



## <a name="parameters"></a><span data-ttu-id="4986b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="4986b-110">Parameters</span></span>

<span data-ttu-id="4986b-111">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="4986b-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4986b-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4986b-112">Return value</span></span>

<span data-ttu-id="4986b-113">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4986b-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4986b-114">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4986b-114">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="4986b-115">Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben: D3DERR \_ invalidcall.</span><span class="sxs-lookup"><span data-stu-id="4986b-115">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="4986b-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4986b-116">Requirements</span></span>



| <span data-ttu-id="4986b-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4986b-117">Requirement</span></span> | <span data-ttu-id="4986b-118">Wert</span><span class="sxs-lookup"><span data-stu-id="4986b-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4986b-119">Header</span><span class="sxs-lookup"><span data-stu-id="4986b-119">Header</span></span><br/>  | <dl> <span data-ttu-id="4986b-120"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="4986b-120"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="4986b-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4986b-121">Library</span></span><br/> | <dl> <span data-ttu-id="4986b-122"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4986b-122"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4986b-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4986b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4986b-124">ID3DX10Sprite</span><span class="sxs-lookup"><span data-stu-id="4986b-124">ID3DX10Sprite</span></span>](id3dx10sprite.md)
</dt> <dt>

[<span data-ttu-id="4986b-125">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="4986b-125">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




