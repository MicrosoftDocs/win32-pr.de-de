---
title: Getrequiredintermediatesize-Funktion (D3dx12. h)
description: Gibt die erforderliche Größe eines Puffers zurück, der zum Hochladen von Daten verwendet werden soll.
ms.assetid: 424B52E9-DE52-40D2-B8B0-C27FD3D3C298
keywords:
- Getrequiredintermediatesize-Funktion
topic_type:
- apiref
api_name:
- GetRequiredIntermediateSize
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15293ce1588704d55f41c364c35db57cbf4c869d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106363160"
---
# <a name="getrequiredintermediatesize-function"></a><span data-ttu-id="00602-104">Getrequiredintermediatesize-Funktion</span><span class="sxs-lookup"><span data-stu-id="00602-104">GetRequiredIntermediateSize function</span></span>

<span data-ttu-id="00602-105">Gibt die erforderliche Größe eines Puffers zurück, der zum Hochladen von Daten verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="00602-105">Returns the required size of a buffer to be used for data upload.</span></span>

## <a name="syntax"></a><span data-ttu-id="00602-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="00602-106">Syntax</span></span>


```C++
UINT64 inline GetRequiredIntermediateSize(
  _In_ ID3D12Resource *pDestinationResource,
  _In_ UINT           FirstSubresource,
  _In_ UINT           NumSubresources
);
```



## <a name="parameters"></a><span data-ttu-id="00602-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="00602-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00602-108">*pdestinationresource* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="00602-108">*pDestinationResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00602-109">Typ: **[ **ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***</span><span class="sxs-lookup"><span data-stu-id="00602-109">Type: **[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***</span></span>

<span data-ttu-id="00602-110">Ein Zeiger auf die [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) -Schnittstelle, die die Ziel Ressource darstellt.</span><span class="sxs-lookup"><span data-stu-id="00602-110">A pointer to the [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) interface that represents the destination resource.</span></span>

</dd> <dt>

<span data-ttu-id="00602-111">*Firstsubresource* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="00602-111">*FirstSubresource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00602-112">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="00602-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="00602-113">Der Index der ersten unter Quelle in der Ressource.</span><span class="sxs-lookup"><span data-stu-id="00602-113">The index of the first subresource in the resource.</span></span> <span data-ttu-id="00602-114">Der Bereich gültiger Werte ist 0 bis D3D12 \_ req \_ subresources.</span><span class="sxs-lookup"><span data-stu-id="00602-114">The range of valid values is 0 to D3D12\_REQ\_SUBRESOURCES.</span></span>

</dd> <dt>

<span data-ttu-id="00602-115">*Numsubresources* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="00602-115">*NumSubresources* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00602-116">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="00602-116">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="00602-117">Die Anzahl der unter Ressourcen in der Ressource.</span><span class="sxs-lookup"><span data-stu-id="00602-117">The number of subresources in the resource.</span></span> <span data-ttu-id="00602-118">Der Bereich gültiger Werte ist 0 bis (D3D12 \_ req \_ subresources- *firstsubresource*).</span><span class="sxs-lookup"><span data-stu-id="00602-118">The range of valid values is 0 to (D3D12\_REQ\_SUBRESOURCES - *FirstSubresource*).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00602-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="00602-119">Return value</span></span>

<span data-ttu-id="00602-120">Typ: **[ **UINT64**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="00602-120">Type: **[**UINT64**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="00602-121">Die Größe des Puffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="00602-121">The size of the buffer, in bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="00602-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="00602-122">Requirements</span></span>



| <span data-ttu-id="00602-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="00602-123">Requirement</span></span> | <span data-ttu-id="00602-124">Wert</span><span class="sxs-lookup"><span data-stu-id="00602-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="00602-125">Header</span><span class="sxs-lookup"><span data-stu-id="00602-125">Header</span></span><br/>  | <dl> <span data-ttu-id="00602-126"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="00602-126"><dt>D3dx12.h</dt></span></span> </dl>  |
| <span data-ttu-id="00602-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="00602-127">Library</span></span><br/> | <dl> <span data-ttu-id="00602-128"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="00602-128"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="00602-129">DLL</span><span class="sxs-lookup"><span data-stu-id="00602-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="00602-130"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="00602-130"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00602-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="00602-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00602-132">Funktionen des Hilfsprogramms für D3D12</span><span class="sxs-lookup"><span data-stu-id="00602-132">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)
</dt> </dl>

 

