---
description: Speichert einen komprimierten PRT-Puffer (preberechneten Radiance Transfer) auf dem Datenträger.
ms.assetid: cc94a83e-f755-411d-a993-4529c5d53cd5
title: D3DXSavePRTCompBufferToFile-Funktion (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSavePRTCompBufferToFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d06629185637ce6fa0d7d33d5454282d2bbb8ec2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961592"
---
# <a name="d3dxsaveprtcompbuffertofile-function"></a><span data-ttu-id="f4cdf-103">D3DXSavePRTCompBufferToFile-Funktion</span><span class="sxs-lookup"><span data-stu-id="f4cdf-103">D3DXSavePRTCompBufferToFile function</span></span>

<span data-ttu-id="f4cdf-104">Speichert einen komprimierten PRT-Puffer (preberechneten Radiance Transfer) auf dem Datenträger.</span><span class="sxs-lookup"><span data-stu-id="f4cdf-104">Saves a compressed precomputed radiance transfer (PRT) buffer to disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4cdf-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f4cdf-105">Syntax</span></span>

```cpp
HRESULT D3DXSavePRTCompBufferToFile(
  _In_ LPCSTR              pFileName,
  _In_ LPD3DXPRTCOMPBUFFER pBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="f4cdf-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f4cdf-106">Parameters</span></span>

<span data-ttu-id="f4cdf-107">*pfilename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f4cdf-107">*pFileName* \[in\]</span></span>

<span data-ttu-id="f4cdf-108">Typ: **[LPCSTR](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f4cdf-108">Type: **[LPCSTR](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f4cdf-109">Der Name der Datei, in der der komprimierte Puffer gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="f4cdf-109">Name of the file to which the compressed buffer is to be saved.</span></span>

<span data-ttu-id="f4cdf-110">*pbuffer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f4cdf-110">*pBuffer* \[in\]</span></span>

<span data-ttu-id="f4cdf-111">Typ: **[LPD3DXPRTCOMPBUFFER](id3dxprtcompbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="f4cdf-111">Type: **[LPD3DXPRTCOMPBUFFER](id3dxprtcompbuffer.md)**</span></span>

<span data-ttu-id="f4cdf-112">Adresse eines Zeigers auf das Eingabe- [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="f4cdf-112">Address of a pointer to the input [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="f4cdf-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f4cdf-113">Return value</span></span>

<span data-ttu-id="f4cdf-114">Typ: **[HRESULT](../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="f4cdf-114">Type: **[HRESULT](../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="f4cdf-115">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert **D3D \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="f4cdf-115">If the method succeeds, then the return value is **D3D\_OK**.</span></span> <span data-ttu-id="f4cdf-116">Wenn die Methode fehlschlägt, kann der Rückgabewert " **D3DERR \_ invalidcall"** lauten.</span><span class="sxs-lookup"><span data-stu-id="f4cdf-116">If the method fails, then the return value can be **D3DERR\_INVALIDCALL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4cdf-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f4cdf-117">Remarks</span></span>

<span data-ttu-id="f4cdf-118">Die Compilereinstellung bestimmt auch die Funktions Version.</span><span class="sxs-lookup"><span data-stu-id="f4cdf-118">The compiler setting also determines the function version.</span></span> <span data-ttu-id="f4cdf-119">Wenn Unicode definiert ist, wird der Funktions aufzurufen in [D3DXSavePRTCompBufferToFileW]()aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="f4cdf-119">If Unicode is defined, then the function call resolves to [D3DXSavePRTCompBufferToFileW]().</span></span> <span data-ttu-id="f4cdf-120">Andernfalls wird der Funktions aufrufin **D3DXSavePRTCompBufferToFileA** aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="f4cdf-120">Otherwise, the function call resolves to **D3DXSavePRTCompBufferToFileA**.</span></span>

<span data-ttu-id="f4cdf-121">Beim PCA-Dateiformat handelt es sich um eine Binärdatei in Form eines Headers und dann um zwei oder drei Datenblöcke.</span><span class="sxs-lookup"><span data-stu-id="f4cdf-121">The PCA file format is a binary file in the form of a header and then two or three data blocks.</span></span>

```cpp
struct PRTCompressHeader
{
    UINT NumSamples;
    UINT NumCoeffs;
    UINT NumChannels;
    UINT TexWidth;
    UINT TexHeight;
    UINT bIsTex;
    UINT NumClusters;
    UINT NumPCA;
};
```

<span data-ttu-id="f4cdf-122">Wenn " *bistex* " ungleich 0 (null) ist, sollten die *NumSamples* gleich sein `TexWidth * TexHeight` .</span><span class="sxs-lookup"><span data-stu-id="f4cdf-122">For the case of *bIsTex* being non-zero, *NumSamples* should equal `TexWidth * TexHeight`.</span></span>

<span data-ttu-id="f4cdf-123">Der Basisdaten Block, der auf den Header folgt, ist `NumCoeffs * NumChannels * (NumPCA + 1) * NumClusters * sizeof(float)` Bytes.</span><span class="sxs-lookup"><span data-stu-id="f4cdf-123">The basis data block that follows the header is `NumCoeffs * NumChannels * (NumPCA + 1) * NumClusters * sizeof(float)` bytes.</span></span>

<span data-ttu-id="f4cdf-124">Dabei handelt es sich um den Datenblock für PCA-Gewichtungen, der `NumPCA * NumSamples * sizeof(float)` Bytes ist.</span><span class="sxs-lookup"><span data-stu-id="f4cdf-124">Following that is the PCA weights data block, which is `NumPCA * NumSamples * sizeof(float)` bytes.</span></span>

<span data-ttu-id="f4cdf-125">Wenn *numclusters* größer als 1 ist, endet die Datei mit dem Cluster-IDs-Datenblock von `NumSamples * sizeof(UINT)` Bytes.</span><span class="sxs-lookup"><span data-stu-id="f4cdf-125">If *NumClusters* is greater than 1, then the file ends with the cluster IDs data block of `NumSamples * sizeof(UINT)` bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4cdf-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f4cdf-126">Requirements</span></span>

| <span data-ttu-id="f4cdf-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f4cdf-127">Requirement</span></span> | <span data-ttu-id="f4cdf-128">Wert</span><span class="sxs-lookup"><span data-stu-id="f4cdf-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f4cdf-129">Header</span><span class="sxs-lookup"><span data-stu-id="f4cdf-129">Header</span></span><br/>  | <dl> <span data-ttu-id="f4cdf-130"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="f4cdf-130"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="f4cdf-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f4cdf-131">Library</span></span><br/> | <dl> <span data-ttu-id="f4cdf-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f4cdf-132"><dt>D3dx9.lib</dt></span></span> </dl>   |

## <a name="see-also"></a><span data-ttu-id="f4cdf-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f4cdf-133">See also</span></span>

[<span data-ttu-id="f4cdf-134">Voraus berechnete Strahlungs Übertragungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="f4cdf-134">Precomputed Radiance Transfer Functions</span></span>](dx9-graphics-reference-d3dx-functions-prt.md)
