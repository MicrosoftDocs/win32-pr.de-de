---
description: Fügt der ID3DXPRTBuffer einen weiteren Puffer hinzu und speichert die Ergebnisse in ID3DXPRTBuffer.
ms.assetid: 345412f4-30c5-4c1d-b0ef-6e3e18c4e5ab
title: 'ID3DXPRTBuffer:: addbuffer-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.AddBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 90b86ad3d5d9fe5aa65db722757bdb34574a1006
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106360244"
---
# <a name="id3dxprtbufferaddbuffer-method"></a><span data-ttu-id="a1f64-103">ID3DXPRTBuffer:: addbuffer-Methode</span><span class="sxs-lookup"><span data-stu-id="a1f64-103">ID3DXPRTBuffer::AddBuffer method</span></span>

<span data-ttu-id="a1f64-104">Fügt der [**ID3DXPRTBuffer**](id3dxprtbuffer.md) einen weiteren Puffer hinzu und speichert die Ergebnisse in **ID3DXPRTBuffer**.</span><span class="sxs-lookup"><span data-stu-id="a1f64-104">Adds another buffer to the [**ID3DXPRTBuffer**](id3dxprtbuffer.md) and stores the results in **ID3DXPRTBuffer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1f64-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a1f64-105">Syntax</span></span>


```C++
HRESULT AddBuffer(
  [in] LPD3DXPRTBUFFER pBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="a1f64-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a1f64-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1f64-107">*pbuffer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a1f64-107">*pBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1f64-108">Typ: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="a1f64-108">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="a1f64-109">Ein Zeiger auf einen Puffer, der Elemente enthält, die den entsprechenden Membern des [**ID3DXPRTBuffer**](id3dxprtbuffer.md) -Puffers hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a1f64-109">Pointer to a buffer that contains members to be added to the respective members of the [**ID3DXPRTBuffer**](id3dxprtbuffer.md) buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1f64-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a1f64-110">Return value</span></span>

<span data-ttu-id="a1f64-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a1f64-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a1f64-112">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a1f64-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="a1f64-113">Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a1f64-113">If the method fails, the following value will be returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1f64-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a1f64-114">Remarks</span></span>

<span data-ttu-id="a1f64-115">pbuffer und [**ID3DXPRTBuffer**](id3dxprtbuffer.md) müssen über die gleiche Anzahl von Beispielen, Koeffizienten und Farbkanälen verfügen. Andernfalls führt die-Methode zu einem Fehler.</span><span class="sxs-lookup"><span data-stu-id="a1f64-115">pBuffer and [**ID3DXPRTBuffer**](id3dxprtbuffer.md) must have the same number of samples, coefficients, and color channels; the method will fail otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1f64-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a1f64-116">Requirements</span></span>



| <span data-ttu-id="a1f64-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a1f64-117">Requirement</span></span> | <span data-ttu-id="a1f64-118">Wert</span><span class="sxs-lookup"><span data-stu-id="a1f64-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a1f64-119">Header</span><span class="sxs-lookup"><span data-stu-id="a1f64-119">Header</span></span><br/>  | <dl> <span data-ttu-id="a1f64-120"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="a1f64-120"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="a1f64-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a1f64-121">Library</span></span><br/> | <dl> <span data-ttu-id="a1f64-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a1f64-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a1f64-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a1f64-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1f64-124">ID3DXPRTBuffer</span><span class="sxs-lookup"><span data-stu-id="a1f64-124">ID3DXPRTBuffer</span></span>](id3dxprtbuffer.md)
</dt> </dl>

 

 




