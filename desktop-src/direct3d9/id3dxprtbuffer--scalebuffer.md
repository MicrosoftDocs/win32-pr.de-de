---
description: Multipliziert jeden Wert im Puffer mit einem konstanten Wert.
ms.assetid: 3d7ef530-b83a-4123-a2ed-fff2b21378ee
title: 'ID3DXPRTBuffer:: scalebuffer-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.ScaleBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 05bdd066f4b7c33ad06f089551f16f0489608c83
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106351993"
---
# <a name="id3dxprtbufferscalebuffer-method"></a><span data-ttu-id="54720-103">ID3DXPRTBuffer:: scalebuffer-Methode</span><span class="sxs-lookup"><span data-stu-id="54720-103">ID3DXPRTBuffer::ScaleBuffer method</span></span>

<span data-ttu-id="54720-104">Multipliziert jeden Wert im Puffer mit einem konstanten Wert.</span><span class="sxs-lookup"><span data-stu-id="54720-104">Multiplies every value in the buffer by a constant value.</span></span>

## <a name="syntax"></a><span data-ttu-id="54720-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="54720-105">Syntax</span></span>


```C++
HRESULT ScaleBuffer(
  [in] FLOAT Scale
);
```



## <a name="parameters"></a><span data-ttu-id="54720-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="54720-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54720-107">*Skalieren* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="54720-107">*Scale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54720-108">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="54720-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="54720-109">Konstanter Wert, mit dem der Puffer skaliert wird.</span><span class="sxs-lookup"><span data-stu-id="54720-109">Constant value used to scale the buffer.</span></span> <span data-ttu-id="54720-110">Jeder Wert im Puffer wird durch das Produkt dieses Werts und den ursprünglichen Puffer Wert ersetzt.</span><span class="sxs-lookup"><span data-stu-id="54720-110">Every value in the buffer is replaced by the product of this value and the original buffer value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54720-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="54720-111">Return value</span></span>

<span data-ttu-id="54720-112">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="54720-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="54720-113">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="54720-113">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="54720-114">Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="54720-114">If the method fails, the following value will be returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="54720-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="54720-115">Requirements</span></span>



| <span data-ttu-id="54720-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="54720-116">Requirement</span></span> | <span data-ttu-id="54720-117">Wert</span><span class="sxs-lookup"><span data-stu-id="54720-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="54720-118">Header</span><span class="sxs-lookup"><span data-stu-id="54720-118">Header</span></span><br/>  | <dl> <span data-ttu-id="54720-119"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="54720-119"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="54720-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="54720-120">Library</span></span><br/> | <dl> <span data-ttu-id="54720-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="54720-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="54720-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="54720-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54720-123">ID3DXPRTBuffer</span><span class="sxs-lookup"><span data-stu-id="54720-123">ID3DXPRTBuffer</span></span>](id3dxprtbuffer.md)
</dt> </dl>

 

 
