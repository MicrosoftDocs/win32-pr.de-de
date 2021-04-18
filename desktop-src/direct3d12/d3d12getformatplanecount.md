---
title: D3D12GetFormatPlaneCount-Funktion (D3dx12. h)
description: Ruft die Anzahl der Ebenen für das angegebene DXGI-Format für den angegebenen virtuellen Adapter (ein ID3D12Device) ab.
ms.assetid: CD21F6F9-A9AA-4CE8-A430-57C70326CB4B
keywords:
- D3D12GetFormatPlaneCount-Funktion
topic_type:
- apiref
api_name:
- D3D12GetFormatPlaneCount
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bfc2e88c162068de2b97c9df5071398e2fab068
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106371883"
---
# <a name="d3d12getformatplanecount-function"></a><span data-ttu-id="8a144-104">D3D12GetFormatPlaneCount-Funktion</span><span class="sxs-lookup"><span data-stu-id="8a144-104">D3D12GetFormatPlaneCount function</span></span>

<span data-ttu-id="8a144-105">Ruft die Anzahl der Ebenen für das angegebene DXGI-Format für den angegebenen virtuellen Adapter (ein **ID3D12Device**) ab.</span><span class="sxs-lookup"><span data-stu-id="8a144-105">Gets the number of planes for the specified DXGI format for the specified virtual adapter (an **ID3D12Device**).</span></span>

## <a name="syntax"></a><span data-ttu-id="8a144-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="8a144-106">Syntax</span></span>


```C++
UINT8 inline D3D12GetFormatPlaneCount(
  _In_ ID3D12Device *pDevice,
       DXGI_FORMAT  Format
);
```



## <a name="parameters"></a><span data-ttu-id="8a144-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="8a144-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a144-108">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8a144-108">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a144-109">Typ: **[ **ID3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device)\***</span><span class="sxs-lookup"><span data-stu-id="8a144-109">Type: **[**ID3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device)\***</span></span>

<span data-ttu-id="8a144-110">Der virtuelle Adapter (ein [**ID3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device)), für den die Anzahl der Ebenen erhalten werden soll.</span><span class="sxs-lookup"><span data-stu-id="8a144-110">The virtual adapter (an [**ID3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device)) for which to get the plane count.</span></span>

</dd> <dt>

<span data-ttu-id="8a144-111">*Format*</span><span class="sxs-lookup"><span data-stu-id="8a144-111">*Format*</span></span> 
</dt> <dd>

<span data-ttu-id="8a144-112">Typ: **[ **DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="8a144-112">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="8a144-113">Das [**DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) , für das die Anzahl der Ebenen angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="8a144-113">The [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) for which to get the plane count.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a144-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8a144-114">Return value</span></span>

<span data-ttu-id="8a144-115">Typ: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="8a144-115">Type: **UINT8**</span></span>

<span data-ttu-id="8a144-116">Die Anzahl der Ebenen für das angegebene Format auf dem angegebenen virtuellen Adapter.</span><span class="sxs-lookup"><span data-stu-id="8a144-116">The plane count for the specified format on the specified virtual adapter.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a144-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8a144-117">Requirements</span></span>



| <span data-ttu-id="8a144-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8a144-118">Requirement</span></span> | <span data-ttu-id="8a144-119">Wert</span><span class="sxs-lookup"><span data-stu-id="8a144-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8a144-120">Header</span><span class="sxs-lookup"><span data-stu-id="8a144-120">Header</span></span><br/>  | <dl> <span data-ttu-id="8a144-121"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="8a144-121"><dt>D3dx12.h</dt></span></span> </dl>  |
| <span data-ttu-id="8a144-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8a144-122">Library</span></span><br/> | <dl> <span data-ttu-id="8a144-123"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8a144-123"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="8a144-124">DLL</span><span class="sxs-lookup"><span data-stu-id="8a144-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="8a144-125"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8a144-125"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a144-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8a144-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a144-127">**D3D12 \_ Feature- \_ Daten \_ Format \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="8a144-127">**D3D12\_FEATURE\_DATA\_FORMAT\_INFO**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_format_info)
</dt> <dt>

[<span data-ttu-id="8a144-128">**CheckFeatureSupport**</span><span class="sxs-lookup"><span data-stu-id="8a144-128">**CheckFeatureSupport**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport)
</dt> <dt>

[<span data-ttu-id="8a144-129">Funktionen des Hilfsprogramms für D3D12</span><span class="sxs-lookup"><span data-stu-id="8a144-129">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)
</dt> </dl>

 

