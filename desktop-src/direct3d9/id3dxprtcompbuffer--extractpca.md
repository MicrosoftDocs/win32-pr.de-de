---
description: Extrahiert die pro-Beispiel-PCA-Projektions Koeffizienten (Principal Component Analysis) aus einem komprimierten ID3DXPRTCompBuffer-Datenpuffer.
ms.assetid: 149098c2-35ca-46e9-a13a-94906c95cfd9
title: 'ID3DXPRTCompBuffer:: extractpca-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTCompBuffer.ExtractPCA
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6ef949e9f88a843f4636643dadd7d00ffd94d98b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106354353"
---
# <a name="id3dxprtcompbufferextractpca-method"></a><span data-ttu-id="27605-103">ID3DXPRTCompBuffer:: extractpca-Methode</span><span class="sxs-lookup"><span data-stu-id="27605-103">ID3DXPRTCompBuffer::ExtractPCA method</span></span>

<span data-ttu-id="27605-104">Extrahiert die pro-Beispiel-PCA-Projektions Koeffizienten (Principal Component Analysis) aus einem komprimierten [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) -Datenpuffer.</span><span class="sxs-lookup"><span data-stu-id="27605-104">Extracts the per-sample principal component analysis (PCA) projection coefficients from an [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) compressed data buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="27605-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="27605-105">Syntax</span></span>


```C++
HRESULT ExtractPCA(
  [in] UINT  StartPCA,
  [in] UINT  NumExtract,
  [in] FLOAT *pPCACoefficients
);
```



## <a name="parameters"></a><span data-ttu-id="27605-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="27605-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27605-107">*Startpca* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="27605-107">*StartPCA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27605-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="27605-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="27605-109">Der Start Index für die PCA-Projektions Koeffizienten zum Extrahieren aus dem Puffer.</span><span class="sxs-lookup"><span data-stu-id="27605-109">Starting index for PCA projection coefficients to extract from the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="27605-110">*Numextract* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="27605-110">*NumExtract* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27605-111">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="27605-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="27605-112">Anzahl der aus dem Puffer zu extrahierenden PCA-Projektions Koeffizienten.</span><span class="sxs-lookup"><span data-stu-id="27605-112">Number of PCA projection coefficients to extract from the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="27605-113">*ppcacoefficients* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="27605-113">*pPCACoefficients* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27605-114">Typ: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="27605-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="27605-115">Zeiger auf den Speicherort, an dem die CPCA (gruppierten Principal Component Analysis)-Koeffizienten geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="27605-115">Pointer to the location where clustered principal component analysis (CPCA) coefficients are written.</span></span> <span data-ttu-id="27605-116">Die Größe der geschriebenen Daten ist (Anzahl der Stichproben) \* (Anzahl der PCA-Koeffizienten).</span><span class="sxs-lookup"><span data-stu-id="27605-116">The size of the data written is (Number of Samples) \* (Number of PCA Coefficients).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27605-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="27605-117">Return value</span></span>

<span data-ttu-id="27605-118">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="27605-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="27605-119">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="27605-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="27605-120">Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="27605-120">If the method fails, the following value will be returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="27605-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="27605-121">Requirements</span></span>



| <span data-ttu-id="27605-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="27605-122">Requirement</span></span> | <span data-ttu-id="27605-123">Wert</span><span class="sxs-lookup"><span data-stu-id="27605-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="27605-124">Header</span><span class="sxs-lookup"><span data-stu-id="27605-124">Header</span></span><br/>  | <dl> <span data-ttu-id="27605-125"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="27605-125"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="27605-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="27605-126">Library</span></span><br/> | <dl> <span data-ttu-id="27605-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="27605-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="27605-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="27605-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27605-129">ID3DXPRTCompBuffer</span><span class="sxs-lookup"><span data-stu-id="27605-129">ID3DXPRTCompBuffer</span></span>](id3dxprtcompbuffer.md)
</dt> </dl>

 

 
