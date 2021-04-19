---
description: 'Nennen Sie dies nach ID3DX10Sprite:: Flush. Wenn \_ beim Aufruf von \_ \_ ID3DX10Sprite:: Begin der d3dx10 Sprite-Speicher Zustand angegeben wurde, stellt diese API den Gerätezustand vor dem Aufruf von ID3DX10Sprite:: begin wieder her.'
ms.assetid: 71645edb-be4a-4d87-9fb0-557cf5cf10e5
title: 'ID3DX10Sprite:: End-Methode (d3dx10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.End
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 02d25e41916bd5d7605f3c0e1bc6e7998ea06e86
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106367404"
---
# <a name="id3dx10spriteend-method"></a><span data-ttu-id="7b00d-104">ID3DX10Sprite:: End-Methode</span><span class="sxs-lookup"><span data-stu-id="7b00d-104">ID3DX10Sprite::End method</span></span>

<span data-ttu-id="7b00d-105">Nennen Sie dies nach ID3DX10Sprite:: Flush.</span><span class="sxs-lookup"><span data-stu-id="7b00d-105">Call this after ID3DX10Sprite::Flush.</span></span> <span data-ttu-id="7b00d-106">Wenn \_ beim Aufruf von \_ \_ ID3DX10Sprite:: Begin der d3dx10 Sprite-Speicher Zustand angegeben wurde, stellt diese API den Gerätezustand vor dem Aufruf von ID3DX10Sprite:: begin wieder her.</span><span class="sxs-lookup"><span data-stu-id="7b00d-106">If D3DX10\_SPRITE\_SAVE\_STATE was specified when ID3DX10Sprite::Begin was called, this API will restore the device state to how it was before ID3DX10Sprite::Begin was called.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b00d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="7b00d-107">Syntax</span></span>


```C++
HRESULT End();
```



## <a name="parameters"></a><span data-ttu-id="7b00d-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="7b00d-108">Parameters</span></span>

<span data-ttu-id="7b00d-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="7b00d-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7b00d-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7b00d-110">Return value</span></span>

<span data-ttu-id="7b00d-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7b00d-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7b00d-112">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7b00d-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="7b00d-113">Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben: D3DERR \_ invalidcall.</span><span class="sxs-lookup"><span data-stu-id="7b00d-113">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b00d-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7b00d-114">Requirements</span></span>



| <span data-ttu-id="7b00d-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7b00d-115">Requirement</span></span> | <span data-ttu-id="7b00d-116">Wert</span><span class="sxs-lookup"><span data-stu-id="7b00d-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7b00d-117">Header</span><span class="sxs-lookup"><span data-stu-id="7b00d-117">Header</span></span><br/>  | <dl> <span data-ttu-id="7b00d-118"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="7b00d-118"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="7b00d-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7b00d-119">Library</span></span><br/> | <dl> <span data-ttu-id="7b00d-120"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7b00d-120"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b00d-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7b00d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b00d-122">ID3DX10Sprite</span><span class="sxs-lookup"><span data-stu-id="7b00d-122">ID3DX10Sprite</span></span>](id3dx10sprite.md)
</dt> <dt>

[<span data-ttu-id="7b00d-123">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="7b00d-123">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




