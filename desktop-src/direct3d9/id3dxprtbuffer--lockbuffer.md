---
description: Sperrt einen Bereich von Vertex-oder Texel-Beispiel Daten und erhält einen Zeiger auf die Position im Pufferspeicher.
ms.assetid: 8de2725f-507e-41ee-828d-2fb19cc2252c
title: 'ID3DXPRTBuffer:: LockBuffer-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.LockBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a2da8cb5a6a2e036fb7b495a129a5ef29d9ff749
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106350700"
---
# <a name="id3dxprtbufferlockbuffer-method"></a><span data-ttu-id="74419-103">ID3DXPRTBuffer:: LockBuffer-Methode</span><span class="sxs-lookup"><span data-stu-id="74419-103">ID3DXPRTBuffer::LockBuffer method</span></span>

<span data-ttu-id="74419-104">Sperrt einen Bereich von Vertex-oder Texel-Beispiel Daten und erhält einen Zeiger auf die Position im Pufferspeicher.</span><span class="sxs-lookup"><span data-stu-id="74419-104">Locks a range of vertex or texel sample data and obtains a pointer to the location in buffer memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="74419-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="74419-105">Syntax</span></span>


```C++
HRESULT LockBuffer(
  [in]  UINT  Start,
  [in]  UINT  NumSamples,
  [out] FLOAT **ppData
);
```



## <a name="parameters"></a><span data-ttu-id="74419-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="74419-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74419-107">*Starten* \[ Sie in\]</span><span class="sxs-lookup"><span data-stu-id="74419-107">*Start* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74419-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="74419-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="74419-109">Index der Stichprobenentnahme von Vertex-oder textex.</span><span class="sxs-lookup"><span data-stu-id="74419-109">Index of the sample of vertex or texel data.</span></span>

</dd> <dt>

<span data-ttu-id="74419-110">*NumSamples* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="74419-110">*NumSamples* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74419-111">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="74419-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="74419-112">Anzahl der abtasteten Scheitel Punkte (oder Texels).</span><span class="sxs-lookup"><span data-stu-id="74419-112">Number of vertices (or texels) sampled.</span></span>

</dd> <dt>

<span data-ttu-id="74419-113">*ppData* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="74419-113">*ppData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="74419-114">Typ: **[ **float**](../winprog/windows-data-types.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="74419-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)\*\***</span></span>

<span data-ttu-id="74419-115">Zeiger auf den Speicherort im Arbeitsspeicher, an dem das Start Beispiel beginnt.</span><span class="sxs-lookup"><span data-stu-id="74419-115">Pointer to the location in memory where the Start sample begins.</span></span> <span data-ttu-id="74419-116">Das Speicher Layout der Puffer Daten lautet:</span><span class="sxs-lookup"><span data-stu-id="74419-116">The memory layout of the buffer data is:</span></span>


```
float fData[NumberSamples][NumberChannels][NumberCoefficients]      
```



</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74419-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="74419-117">Return value</span></span>

<span data-ttu-id="74419-118">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="74419-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="74419-119">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="74419-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="74419-120">Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben:</span><span class="sxs-lookup"><span data-stu-id="74419-120">If the method fails, the following value will be returned:</span></span>

## <a name="remarks"></a><span data-ttu-id="74419-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="74419-121">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="74419-122">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="74419-122">Requirements</span></span>



| <span data-ttu-id="74419-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="74419-123">Requirement</span></span> | <span data-ttu-id="74419-124">Wert</span><span class="sxs-lookup"><span data-stu-id="74419-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="74419-125">Header</span><span class="sxs-lookup"><span data-stu-id="74419-125">Header</span></span><br/>  | <dl> <span data-ttu-id="74419-126"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="74419-126"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="74419-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="74419-127">Library</span></span><br/> | <dl> <span data-ttu-id="74419-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="74419-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="74419-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="74419-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74419-130">ID3DXPRTBuffer</span><span class="sxs-lookup"><span data-stu-id="74419-130">ID3DXPRTBuffer</span></span>](id3dxprtbuffer.md)
</dt> <dt>

[<span data-ttu-id="74419-131">**ID3DXPRTBuffer:: getnumchannels**</span><span class="sxs-lookup"><span data-stu-id="74419-131">**ID3DXPRTBuffer::GetNumChannels**</span></span>](id3dxprtbuffer--getnumchannels.md)
</dt> <dt>

[<span data-ttu-id="74419-132">**ID3DXPRTBuffer:: getnumcoeffs**</span><span class="sxs-lookup"><span data-stu-id="74419-132">**ID3DXPRTBuffer::GetNumCoeffs**</span></span>](id3dxprtbuffer--getnumcoeffs.md)
</dt> <dt>

[<span data-ttu-id="74419-133">**ID3DXPRTBuffer:: getnumsamples**</span><span class="sxs-lookup"><span data-stu-id="74419-133">**ID3DXPRTBuffer::GetNumSamples**</span></span>](id3dxprtbuffer--getnumsamples.md)
</dt> </dl>

 

 
