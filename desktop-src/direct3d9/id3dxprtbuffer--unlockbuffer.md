---
description: 'Beendet die Lebensdauer des ppData-Zeigers, der von ID3DXPRTBuffer:: LockBuffer zurückgegeben wurde.'
ms.assetid: 25464566-8a93-48a4-93fa-17828861f98c
title: 'ID3DXPRTBuffer:: UnlockBuffer-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.UnlockBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9a17d8f186fc1baf62dda3652372c4e73a5de141
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219592"
---
# <a name="id3dxprtbufferunlockbuffer-method"></a><span data-ttu-id="49cfb-103">ID3DXPRTBuffer:: UnlockBuffer-Methode</span><span class="sxs-lookup"><span data-stu-id="49cfb-103">ID3DXPRTBuffer::UnlockBuffer method</span></span>

<span data-ttu-id="49cfb-104">Beendet die Lebensdauer des ppData-Zeigers, der von [**ID3DXPRTBuffer:: LockBuffer**](id3dxprtbuffer--lockbuffer.md)zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="49cfb-104">Ends the lifespan of the ppData pointer returned by [**ID3DXPRTBuffer::LockBuffer**](id3dxprtbuffer--lockbuffer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="49cfb-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="49cfb-105">Syntax</span></span>


```C++
HRESULT UnlockBuffer();
```



## <a name="parameters"></a><span data-ttu-id="49cfb-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="49cfb-106">Parameters</span></span>

<span data-ttu-id="49cfb-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="49cfb-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="49cfb-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="49cfb-108">Return value</span></span>

<span data-ttu-id="49cfb-109">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="49cfb-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="49cfb-110">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="49cfb-110">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="49cfb-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="49cfb-111">Requirements</span></span>



| <span data-ttu-id="49cfb-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="49cfb-112">Requirement</span></span> | <span data-ttu-id="49cfb-113">Wert</span><span class="sxs-lookup"><span data-stu-id="49cfb-113">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="49cfb-114">Header</span><span class="sxs-lookup"><span data-stu-id="49cfb-114">Header</span></span><br/>  | <dl> <span data-ttu-id="49cfb-115"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="49cfb-115"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="49cfb-116">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="49cfb-116">Library</span></span><br/> | <dl> <span data-ttu-id="49cfb-117"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="49cfb-117"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="49cfb-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="49cfb-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49cfb-119">ID3DXPRTBuffer</span><span class="sxs-lookup"><span data-stu-id="49cfb-119">ID3DXPRTBuffer</span></span>](id3dxprtbuffer.md)
</dt> </dl>

 

 




