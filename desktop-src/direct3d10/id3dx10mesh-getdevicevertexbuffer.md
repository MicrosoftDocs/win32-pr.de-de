---
description: 'Greifen Sie auf den Vertex-Puffer des Mesh zu, nachdem er mit ID3DX10Mesh:: committedevice an das Gerät übertragen wurde. Dies unterscheidet sich von ID3DX10Mesh:: getvertexbuffer, das den Vertex-Puffer zurückgibt, bevor er an das Gerät übertragen wurde.'
ms.assetid: 621d9105-e55d-47b8-8557-8adb7db19d66
title: 'ID3DX10Mesh:: getdevicevertexbuffer-Methode (d3dx10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetDeviceVertexBuffer
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 9943050d174acb4e8f8e676f56a95cfdcde88f5a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353746"
---
# <a name="id3dx10meshgetdevicevertexbuffer-method"></a><span data-ttu-id="8da26-104">ID3DX10Mesh:: getdevicevertexbuffer-Methode</span><span class="sxs-lookup"><span data-stu-id="8da26-104">ID3DX10Mesh::GetDeviceVertexBuffer method</span></span>

<span data-ttu-id="8da26-105">Greifen Sie auf den Vertex-Puffer des Mesh zu, nachdem er mit [**ID3DX10Mesh:: committedevice**](id3dx10mesh-committodevice.md)an das Gerät übertragen wurde.</span><span class="sxs-lookup"><span data-stu-id="8da26-105">Access the mesh's vertex buffer after it has been committed to the device with [**ID3DX10Mesh::CommitToDevice**](id3dx10mesh-committodevice.md).</span></span> <span data-ttu-id="8da26-106">Dies unterscheidet sich von [**ID3DX10Mesh:: getvertexbuffer**](id3dx10mesh-getvertexbuffer.md), das den Vertex-Puffer zurückgibt, bevor er an das Gerät übertragen wurde.</span><span class="sxs-lookup"><span data-stu-id="8da26-106">This is different from [**ID3DX10Mesh::GetVertexBuffer**](id3dx10mesh-getvertexbuffer.md), which returns the vertex buffer before it has been committed to the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="8da26-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="8da26-107">Syntax</span></span>


```C++
HRESULT GetDeviceVertexBuffer(
  [in]  UINT         iBuffer,
  [out] ID3D10Buffer **ppVertexBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="8da26-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="8da26-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8da26-109">*ibuffer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8da26-109">*iBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8da26-110">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8da26-110">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8da26-111">Ein Index, der den Zugriff auf den Vertex-Puffer identifiziert.</span><span class="sxs-lookup"><span data-stu-id="8da26-111">An index identifying which vertex buffer to access.</span></span>

</dd> <dt>

<span data-ttu-id="8da26-112">*ppvertexbuffer* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="8da26-112">*ppVertexBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8da26-113">Typ: **[ **ID3D10Buffer**](/windows/desktop/api/D3D10/nn-d3d10-id3d10buffer)\*\***</span><span class="sxs-lookup"><span data-stu-id="8da26-113">Type: **[**ID3D10Buffer**](/windows/desktop/api/D3D10/nn-d3d10-id3d10buffer)\*\***</span></span>

<span data-ttu-id="8da26-114">Der Vertex-Puffer, nachdem ein Commit für das Gerät ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="8da26-114">The vertex buffer after it has been committed to the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8da26-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8da26-115">Return value</span></span>

<span data-ttu-id="8da26-116">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8da26-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8da26-117">Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="8da26-117">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8da26-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8da26-118">Requirements</span></span>



| <span data-ttu-id="8da26-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8da26-119">Requirement</span></span> | <span data-ttu-id="8da26-120">Wert</span><span class="sxs-lookup"><span data-stu-id="8da26-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8da26-121">Header</span><span class="sxs-lookup"><span data-stu-id="8da26-121">Header</span></span><br/>  | <dl> <span data-ttu-id="8da26-122"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="8da26-122"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="8da26-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8da26-123">Library</span></span><br/> | <dl> <span data-ttu-id="8da26-124"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8da26-124"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8da26-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8da26-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8da26-126">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="8da26-126">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="8da26-127">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="8da26-127">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
