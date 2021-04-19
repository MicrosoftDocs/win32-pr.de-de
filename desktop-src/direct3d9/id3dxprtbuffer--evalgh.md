---
description: Wendet gespeicherte Textur Daten auf einen ID3DXPRTBuffer-Textur Puffer an.
ms.assetid: 05cc0709-543a-4df5-980a-8549451d396b
title: 'ID3DXPRTBuffer:: evalgh-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.EvalGH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 23896ff2514db7b5e12b164ea0c0a763b5d1d3b1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106373549"
---
# <a name="id3dxprtbufferevalgh-method"></a><span data-ttu-id="ed2e6-103">ID3DXPRTBuffer:: evalgh-Methode</span><span class="sxs-lookup"><span data-stu-id="ed2e6-103">ID3DXPRTBuffer::EvalGH method</span></span>

<span data-ttu-id="ed2e6-104">Wendet gespeicherte Textur Daten auf einen [**ID3DXPRTBuffer**](id3dxprtbuffer.md) -Textur Puffer an.</span><span class="sxs-lookup"><span data-stu-id="ed2e6-104">Applies stored texture gutter data to an [**ID3DXPRTBuffer**](id3dxprtbuffer.md) texture buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed2e6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ed2e6-105">Syntax</span></span>


```C++
HRESULT EvalGH();
```



## <a name="parameters"></a><span data-ttu-id="ed2e6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ed2e6-106">Parameters</span></span>

<span data-ttu-id="ed2e6-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="ed2e6-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ed2e6-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ed2e6-108">Return value</span></span>

<span data-ttu-id="ed2e6-109">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ed2e6-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ed2e6-110">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ed2e6-110">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="ed2e6-111">Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ed2e6-111">If the method fails, the following value will be returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed2e6-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ed2e6-112">Remarks</span></span>

<span data-ttu-id="ed2e6-113">Diese Methode führt einen internen Aufrufen von [**ID3DXTextureGutterHelper:: applyguttersfloat**](id3dxtexturegutterhelper--applyguttersfloat.md) aus, um Textur bunddaten abzurufen und anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="ed2e6-113">This method makes an internal call to [**ID3DXTextureGutterHelper::ApplyGuttersFloat**](id3dxtexturegutterhelper--applyguttersfloat.md) to retrieve and apply texture gutter data.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed2e6-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ed2e6-114">Requirements</span></span>



| <span data-ttu-id="ed2e6-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ed2e6-115">Requirement</span></span> | <span data-ttu-id="ed2e6-116">Wert</span><span class="sxs-lookup"><span data-stu-id="ed2e6-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ed2e6-117">Header</span><span class="sxs-lookup"><span data-stu-id="ed2e6-117">Header</span></span><br/>  | <dl> <span data-ttu-id="ed2e6-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed2e6-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="ed2e6-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ed2e6-119">Library</span></span><br/> | <dl> <span data-ttu-id="ed2e6-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ed2e6-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ed2e6-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ed2e6-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed2e6-122">ID3DXPRTBuffer</span><span class="sxs-lookup"><span data-stu-id="ed2e6-122">ID3DXPRTBuffer</span></span>](id3dxprtbuffer.md)
</dt> </dl>

 

 




