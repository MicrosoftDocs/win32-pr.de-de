---
description: 'Greifen Sie auf den Index Puffer des Mesh zu, nachdem er mit ID3DX10Mesh:: committedevice an das Gerät übertragen wurde. Dies unterscheidet sich von ID3DX10Mesh:: getindexbuffer, das den Index Puffer zurückgibt, bevor er an das Gerät übertragen wurde.'
ms.assetid: 94d21f50-91b5-4f8d-ac73-7a851bba8685
title: 'ID3DX10Mesh:: getdeviceidexbuffer-Methode (d3dx10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetDeviceIndexBuffer
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 3ec3e65cfc4acb5a903bcf18d2f707d39127e975
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353747"
---
# <a name="id3dx10meshgetdeviceindexbuffer-method"></a><span data-ttu-id="8f21f-104">ID3DX10Mesh:: getdeviceidexbuffer-Methode</span><span class="sxs-lookup"><span data-stu-id="8f21f-104">ID3DX10Mesh::GetDeviceIndexBuffer method</span></span>

<span data-ttu-id="8f21f-105">Greifen Sie auf den Index Puffer des Mesh zu, nachdem er mit [**ID3DX10Mesh:: committedevice**](id3dx10mesh-committodevice.md)an das Gerät übertragen wurde.</span><span class="sxs-lookup"><span data-stu-id="8f21f-105">Access the mesh's index buffer after it has been committed to the device with [**ID3DX10Mesh::CommitToDevice**](id3dx10mesh-committodevice.md).</span></span> <span data-ttu-id="8f21f-106">Dies unterscheidet sich von [**ID3DX10Mesh:: getindexbuffer**](id3dx10mesh-getindexbuffer.md), das den Index Puffer zurückgibt, bevor er an das Gerät übertragen wurde.</span><span class="sxs-lookup"><span data-stu-id="8f21f-106">This is different from [**ID3DX10Mesh::GetIndexBuffer**](id3dx10mesh-getindexbuffer.md), which returns the index buffer before it has been committed to the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f21f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="8f21f-107">Syntax</span></span>


```C++
HRESULT GetDeviceIndexBuffer(
  [out] ID3D10Buffer **ppIndexBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="8f21f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="8f21f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f21f-109">*ppindexbuffer* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="8f21f-109">*ppIndexBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8f21f-110">Typ: **[ **ID3D10Buffer**](/windows/desktop/api/D3D10/nn-d3d10-id3d10buffer)\*\***</span><span class="sxs-lookup"><span data-stu-id="8f21f-110">Type: **[**ID3D10Buffer**](/windows/desktop/api/D3D10/nn-d3d10-id3d10buffer)\*\***</span></span>

<span data-ttu-id="8f21f-111">Der Index Puffer, nachdem ein Commit für das Gerät ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="8f21f-111">The index buffer after it has been committed to the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f21f-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8f21f-112">Return value</span></span>

<span data-ttu-id="8f21f-113">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8f21f-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8f21f-114">Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="8f21f-114">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="8f21f-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8f21f-115">Remarks</span></span>

<span data-ttu-id="8f21f-116">Wenn der Index Puffer des Netzes noch nicht an das Gerät übergeben wurde, führt diese API automatisch einen Commit für den Index Puffer aus, bevor er einen Zeiger auf den Puffer zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="8f21f-116">If the mesh's index buffer has not already been committed to the device, this API will automatically commit the index buffer before it returns a pointer to the buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f21f-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8f21f-117">Requirements</span></span>



| <span data-ttu-id="8f21f-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8f21f-118">Requirement</span></span> | <span data-ttu-id="8f21f-119">Wert</span><span class="sxs-lookup"><span data-stu-id="8f21f-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8f21f-120">Header</span><span class="sxs-lookup"><span data-stu-id="8f21f-120">Header</span></span><br/>  | <dl> <span data-ttu-id="8f21f-121"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="8f21f-121"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="8f21f-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8f21f-122">Library</span></span><br/> | <dl> <span data-ttu-id="8f21f-123"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8f21f-123"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f21f-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8f21f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f21f-125">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="8f21f-125">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="8f21f-126">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="8f21f-126">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




