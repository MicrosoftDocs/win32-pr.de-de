---
description: Extrahiert den Mittelwert und die Hauptkomponentenanalyse (PCA) für einen bestimmten Cluster aus einem ID3DXPRTCompBuffer-komprimierten Datenpuffer.
ms.assetid: dcb1372f-2c8f-4d18-9840-5982b2ed0d6e
title: 'ID3DXPRTCompBuffer:: extractbasis-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTCompBuffer.ExtractBasis
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ebedef91c9f3d1e277a099ffd295903e9ba77ba8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106357251"
---
# <a name="id3dxprtcompbufferextractbasis-method"></a><span data-ttu-id="2f21a-103">ID3DXPRTCompBuffer:: extractbasis-Methode</span><span class="sxs-lookup"><span data-stu-id="2f21a-103">ID3DXPRTCompBuffer::ExtractBasis method</span></span>

<span data-ttu-id="2f21a-104">Extrahiert den Mittelwert und die Hauptkomponentenanalyse (PCA) für einen bestimmten Cluster aus einem [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) -komprimierten Datenpuffer.</span><span class="sxs-lookup"><span data-stu-id="2f21a-104">Extracts the mean and principal component analysis (PCA) basis vectors for a given cluster from an [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) compressed data buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f21a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2f21a-105">Syntax</span></span>


```C++
HRESULT ExtractBasis(
  [in]      UINT  Cluster,
  [in, out] FLOAT *pClusterBasis
);
```



## <a name="parameters"></a><span data-ttu-id="2f21a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2f21a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f21a-107">*Cluster* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2f21a-107">*Cluster* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f21a-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2f21a-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2f21a-109">Cluster, für den die Basis extrahiert wird.</span><span class="sxs-lookup"><span data-stu-id="2f21a-109">Cluster for which the basis will be extracted.</span></span>

</dd> <dt>

<span data-ttu-id="2f21a-110">*pclusterbasis* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="2f21a-110">*pClusterBasis* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2f21a-111">Typ: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="2f21a-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="2f21a-112">Zeiger auf ein Array von Basis Vektordaten für Cluster.</span><span class="sxs-lookup"><span data-stu-id="2f21a-112">Pointer to an array of basis vector data for Cluster.</span></span> <span data-ttu-id="2f21a-113">Die Größe der gespeicherten float-Daten beträgt: (1 + Anzahl der PCA-Vektoren pro Cluster) \* (Anzahl der Koeffizienten) \* (Anzahl der farbchannels)</span><span class="sxs-lookup"><span data-stu-id="2f21a-113">The size of the FLOAT data stored will be: (1 + Number of PCA vectors per cluster) \* (Number of coefficients) \* (Number of color channels)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f21a-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2f21a-114">Return value</span></span>

<span data-ttu-id="2f21a-115">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2f21a-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2f21a-116">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2f21a-116">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="2f21a-117">Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2f21a-117">If the method fails, the following value will be returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f21a-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2f21a-118">Requirements</span></span>



| <span data-ttu-id="2f21a-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2f21a-119">Requirement</span></span> | <span data-ttu-id="2f21a-120">Wert</span><span class="sxs-lookup"><span data-stu-id="2f21a-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2f21a-121">Header</span><span class="sxs-lookup"><span data-stu-id="2f21a-121">Header</span></span><br/>  | <dl> <span data-ttu-id="2f21a-122"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f21a-122"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="2f21a-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2f21a-123">Library</span></span><br/> | <dl> <span data-ttu-id="2f21a-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2f21a-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2f21a-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2f21a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f21a-126">ID3DXPRTCompBuffer</span><span class="sxs-lookup"><span data-stu-id="2f21a-126">ID3DXPRTCompBuffer</span></span>](id3dxprtcompbuffer.md)
</dt> </dl>

 

 
