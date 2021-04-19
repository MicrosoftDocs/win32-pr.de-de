---
title: D3DX12SerializeVersionedRootSignature-Funktion (D3dx12. h)
description: Unterstützt die Aktivierung von root Signature 1,1-Features, wenn diese verfügbar sind. es ist nicht erforderlich, zwei Codepfade zum Aufbauen von Stamm Signaturen zu verwalten. Diese Hilfsmethode rekonstruiert eine Stamm Signatur der Version 1,0, wenn Version 1,1 nicht unterstützt wird.
ms.assetid: 0F6BA6C1-9A33-4E99-BF34-4A0358E7427D
keywords:
- D3DX12SerializeVersionedRootSignature-Funktion
topic_type:
- apiref
api_name:
- D3DX12SerializeVersionedRootSignature
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70a9d0424f7f7a7f89edde18273c5d1fa22fae28
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355162"
---
# <a name="d3dx12serializeversionedrootsignature-function"></a><span data-ttu-id="12c54-105">D3DX12SerializeVersionedRootSignature-Funktion</span><span class="sxs-lookup"><span data-stu-id="12c54-105">D3DX12SerializeVersionedRootSignature function</span></span>

<span data-ttu-id="12c54-106">Unterstützt die Aktivierung von root Signature 1,1-Features, wenn diese verfügbar sind. es ist nicht erforderlich, zwei Codepfade zum Aufbauen von Stamm Signaturen zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="12c54-106">Helps enable root signature 1.1 features when they are available, and does not require maintaining two code paths for building root signatures.</span></span> <span data-ttu-id="12c54-107">Diese Hilfsmethode rekonstruiert eine Stamm Signatur der Version 1,0, wenn Version 1,1 nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="12c54-107">This helper method reconstructs a version 1.0 root signature when version 1.1 is not supported.</span></span>

## <a name="syntax"></a><span data-ttu-id="12c54-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="12c54-108">Syntax</span></span>


```C++
HRESULT inline D3DX12SerializeVersionedRootSignature(
  _In_      const D3D12_VERSIONED_ROOT_SIGNATURE_DESC *pRootSignatureDesc,
                  D3D_ROOT_SIGNATURE_VERSION          MaxVersion,
  _Out_           ID3DBlob                            **ppBlob,
  _Out_opt_       ID3DBlob                            **ppErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="12c54-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="12c54-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12c54-110">*prootsignatueinlösen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="12c54-110">*pRootSignatureDesc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12c54-111">Typ: **Konstanten D3D12 \_ versionierte Stamm \_ \_ Signatur \_ DESC \***</span><span class="sxs-lookup"><span data-stu-id="12c54-111">Type: **const D3D12\_VERSIONED\_ROOT\_SIGNATURE\_DESC\***</span></span>

<span data-ttu-id="12c54-112">Gibt eine mit [**D3D12 \_ versionierte Stamm \_ \_ Signatur \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) an, die eine Beschreibung einer beliebigen Version einer Stamm Signatur enthält.</span><span class="sxs-lookup"><span data-stu-id="12c54-112">Specifies a [**D3D12\_VERSIONED\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) that contains a description of any version of a root signature.</span></span>

</dd> <dt>

<span data-ttu-id="12c54-113">*MaxVersion*</span><span class="sxs-lookup"><span data-stu-id="12c54-113">*MaxVersion*</span></span> 
</dt> <dd>

<span data-ttu-id="12c54-114">Type: **D3D \_ root \_ Signature \_ Version**</span><span class="sxs-lookup"><span data-stu-id="12c54-114">Type: **D3D\_ROOT\_SIGNATURE\_VERSION**</span></span>

<span data-ttu-id="12c54-115">Gibt die maximal unterstützte D3D-Stamm [**\_ \_ Signatur \_ Version**](/windows/desktop/api/d3d12/ne-d3d12-d3d_root_signature_version)an.</span><span class="sxs-lookup"><span data-stu-id="12c54-115">Specifies the maximum supported [**D3D\_ROOT\_SIGNATURE\_VERSION**](/windows/desktop/api/d3d12/ne-d3d12-d3d_root_signature_version).</span></span>

</dd> <dt>

<span data-ttu-id="12c54-116">*ppBlob* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="12c54-116">*ppBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="12c54-117">Typ: **ID3DBlob \* \***</span><span class="sxs-lookup"><span data-stu-id="12c54-117">Type: **ID3DBlob\*\***</span></span>

<span data-ttu-id="12c54-118">Ein Zeiger auf einen Speicherblock, der einen Zeiger auf die [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) -Schnittstelle empfängt, mit der Sie auf die serialisierte Stamm Signatur zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="12c54-118">A pointer to a memory block that receives a pointer to the [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) interface that you can use to access the serialized root signature.</span></span>

</dd> <dt>

<span data-ttu-id="12c54-119">*pperrorblob* \[ Out, optional\]</span><span class="sxs-lookup"><span data-stu-id="12c54-119">*ppErrorBlob* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="12c54-120">Typ: **ID3DBlob \* \***</span><span class="sxs-lookup"><span data-stu-id="12c54-120">Type: **ID3DBlob\*\***</span></span>

<span data-ttu-id="12c54-121">Ein Zeiger auf einen Speicherblock, der einen Zeiger auf die [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) -Schnittstelle empfängt, die Sie verwenden können, um auf Fehlermeldungen des Serialisierungsprogramms zuzugreifen, oder **null** , wenn keine Fehler vorliegen.</span><span class="sxs-lookup"><span data-stu-id="12c54-121">A pointer to a memory block that receives a pointer to the [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) interface that you can use to access serializer error messages, or **NULL** if there are no errors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12c54-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="12c54-122">Return value</span></span>

<span data-ttu-id="12c54-123">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="12c54-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="12c54-124">Gibt bei Erfolg **S \_ OK** zurück; andernfalls wird einer der [Rückgabe Codes Direct3D 12 zurückgegeben](d3d12-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="12c54-124">Returns **S\_OK** if successful; otherwise, returns one of the [Direct3D 12 Return Codes](d3d12-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="12c54-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="12c54-125">Remarks</span></span>

<span data-ttu-id="12c54-126">Diese Funktion wurde im Zusammenhang mit dem Windows 10 Anniversary Update (14393) veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="12c54-126">This function was released to coincide with the Windows 10 Anniversary Update (14393).</span></span> <span data-ttu-id="12c54-127">Um Windows 10-Versionen zu unterstützen, muss für die Verwendung dieser Funktion d3d12. lib für das *verzögerte Laden* eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="12c54-127">In order to support Windows 10 versions prior to this, use of this function requires d3d12.lib be set up for *delay loading*.</span></span>

## <a name="requirements"></a><span data-ttu-id="12c54-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="12c54-128">Requirements</span></span>



| <span data-ttu-id="12c54-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="12c54-129">Requirement</span></span> | <span data-ttu-id="12c54-130">Wert</span><span class="sxs-lookup"><span data-stu-id="12c54-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="12c54-131">Header</span><span class="sxs-lookup"><span data-stu-id="12c54-131">Header</span></span><br/>  | <dl> <span data-ttu-id="12c54-132"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="12c54-132"><dt>D3dx12.h</dt></span></span> </dl>  |
| <span data-ttu-id="12c54-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="12c54-133">Library</span></span><br/> | <dl> <span data-ttu-id="12c54-134"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="12c54-134"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="12c54-135">DLL</span><span class="sxs-lookup"><span data-stu-id="12c54-135">DLL</span></span><br/>     | <dl> <span data-ttu-id="12c54-136"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="12c54-136"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12c54-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="12c54-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12c54-138">**D3D12SerializeVersionedRootSignature**</span><span class="sxs-lookup"><span data-stu-id="12c54-138">**D3D12SerializeVersionedRootSignature**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializeversionedrootsignature)
</dt> <dt>

[<span data-ttu-id="12c54-139">Funktionen des Hilfsprogramms für D3D12</span><span class="sxs-lookup"><span data-stu-id="12c54-139">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)
</dt> </dl>

 

