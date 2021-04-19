---
description: Extrahiert die Cluster-IDs pro Beispiel aus einem komprimierten ID3DXPRTCompBuffer-Datenpuffer.
ms.assetid: d78d82ab-58bc-4b73-9ca0-8b7f06867618
title: 'ID3DXPRTCompBuffer:: extractclusterids-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTCompBuffer.ExtractClusterIDs
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ef68a972109e89e318adb83ab388c653c6a3deed
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106364011"
---
# <a name="id3dxprtcompbufferextractclusterids-method"></a><span data-ttu-id="62871-103">ID3DXPRTCompBuffer:: extractclusterids-Methode</span><span class="sxs-lookup"><span data-stu-id="62871-103">ID3DXPRTCompBuffer::ExtractClusterIDs method</span></span>

<span data-ttu-id="62871-104">Extrahiert die Cluster-IDs pro Beispiel aus einem komprimierten [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) -Datenpuffer.</span><span class="sxs-lookup"><span data-stu-id="62871-104">Extracts the per-sample cluster IDs from an [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) compressed data buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="62871-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="62871-105">Syntax</span></span>


```C++
HRESULT ExtractClusterIDs(
  [in, out] UINT *pClusterIDs
);
```



## <a name="parameters"></a><span data-ttu-id="62871-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="62871-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62871-107">*pclusterids* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="62871-107">*pClusterIDs* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="62871-108">Typ: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="62871-108">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="62871-109">Zeiger auf den Speicherort im Arbeitsspeicher, an dem IDs geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="62871-109">Pointer to the location in memory where IDs are written.</span></span> <span data-ttu-id="62871-110">Die erforderliche Arbeitsspeicher Länge ist der von [**ID3DXPRTCompBuffer:: getnumsamples**](id3dxprtcompbuffer--getnumsamples.md)zurückgegebene Wert.</span><span class="sxs-lookup"><span data-stu-id="62871-110">The length of memory required is the value returned by [**ID3DXPRTCompBuffer::GetNumSamples**](id3dxprtcompbuffer--getnumsamples.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62871-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="62871-111">Return value</span></span>

<span data-ttu-id="62871-112">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="62871-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="62871-113">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="62871-113">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="62871-114">Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="62871-114">If the method fails, the following value will be returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="62871-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="62871-115">Requirements</span></span>



| <span data-ttu-id="62871-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="62871-116">Requirement</span></span> | <span data-ttu-id="62871-117">Wert</span><span class="sxs-lookup"><span data-stu-id="62871-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="62871-118">Header</span><span class="sxs-lookup"><span data-stu-id="62871-118">Header</span></span><br/>  | <dl> <span data-ttu-id="62871-119"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="62871-119"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="62871-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="62871-120">Library</span></span><br/> | <dl> <span data-ttu-id="62871-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="62871-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="62871-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="62871-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62871-123">ID3DXPRTCompBuffer</span><span class="sxs-lookup"><span data-stu-id="62871-123">ID3DXPRTCompBuffer</span></span>](id3dxprtcompbuffer.md)
</dt> </dl>

 

 
