---
title: D3DX12ParsePipelineStream-Funktion (D3dx12. h)
description: Analysiert eine Pipeline Status-Datenstrom Beschreibung und ruft für jede analysierte untergeordnete Instanz einen benutzerdefinierten Rückruf auf.
ms.assetid: BE4E8CC4-1E1F-4FE8-B109-05FAF93EB620
keywords:
- D3DX12ParsePipelineStream-Funktion
topic_type:
- apiref
api_name:
- D3DX12ParsePipelineStream
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6778c29793f01ff7f1e5fd6424fb6795a29e64c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106354986"
---
# <a name="d3dx12parsepipelinestream-function"></a><span data-ttu-id="f9585-104">D3DX12ParsePipelineStream-Funktion</span><span class="sxs-lookup"><span data-stu-id="f9585-104">D3DX12ParsePipelineStream function</span></span>

<span data-ttu-id="f9585-105">Analysiert eine Pipeline Status-Datenstrom Beschreibung und ruft für jede analysierte untergeordnete Instanz einen benutzerdefinierten Rückruf auf.</span><span class="sxs-lookup"><span data-stu-id="f9585-105">Parses a pipeline state stream description, calling a user-defined callback for each subobject instance parsed.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9585-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="f9585-106">Syntax</span></span>


```C++
HRESULT inline D3DX12ParsePipelineStream(
   const D3D12_PIPELINE_STATE_STREAM_DESC &Desc,
         ID3DX12PipelineParserCallbacks   *pCallbacks
);
```



## <a name="parameters"></a><span data-ttu-id="f9585-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="f9585-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9585-108">*Wird deaktiviert* \[ atur\]</span><span class="sxs-lookup"><span data-stu-id="f9585-108">*Desc* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="f9585-109">Typ: **Konstanten [**D3D12 \_ Pipeline \_ State \_ Stream \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_pipeline_state_stream_desc)**</span><span class="sxs-lookup"><span data-stu-id="f9585-109">Type: **const [**D3D12\_PIPELINE\_STATE\_STREAM\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_pipeline_state_stream_desc)**</span></span>

<span data-ttu-id="f9585-110">Die Beschreibung des Pipeline Zustandsdaten Stroms, die analysiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="f9585-110">The pipeline state stream description to parse.</span></span>

</dd> <dt>

<span data-ttu-id="f9585-111">*pcallbacks*</span><span class="sxs-lookup"><span data-stu-id="f9585-111">*pCallbacks*</span></span> 
</dt> <dd>

<span data-ttu-id="f9585-112">Typ: **[ **ID3DX12PipelineParserCallbacks**](id3dx12pipelineparsercallbacks.md)\***</span><span class="sxs-lookup"><span data-stu-id="f9585-112">Type: **[**ID3DX12PipelineParserCallbacks**](id3dx12pipelineparsercallbacks.md)\***</span></span>

<span data-ttu-id="f9585-113">Eine-Struktur, die die Rückrufe angibt, die für jeden untergeordneten Objekttyp aufgerufen werden sollen, sowie zusätzliche Rückrufe, die im Fall eines Fehler bei der Verarbeitung aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="f9585-113">A structure that specifies the callbacks to call for each subobject type and additional callbacks to call in the event of a parsing error.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9585-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f9585-114">Return value</span></span>

<span data-ttu-id="f9585-115">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f9585-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f9585-116">Diese Methode gibt einen HRESULT Success (**S \_ OK** -oder **E \_ invalidArg** -Fehler zurück, wenn ein unbekannter unter Typ gefunden wird, wenn die Datenstrom Beschreibung leer ist, NULL ist oder doppelte unter Objekte (einschließlich abgeleiteter unter Objekte) enthält, oder wenn *pcallbacks* NULL ist.</span><span class="sxs-lookup"><span data-stu-id="f9585-116">This method returns an HRESULT success (**S\_OK** or **E\_INVALIDARG** error if an unknown subobject type is encountered, if the stream description is empty, null, or contains duplicate subobjects (including derived subobjects), or if *pCallbacks* is null.</span></span> <span data-ttu-id="f9585-117">In jedem Fall, dass E \_ invalidArg zurückgegeben wird, wird zuerst ein entsprechender Rückruf aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="f9585-117">In each case that E\_INVALIDARG is returned, a corresponding callback is first called.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9585-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f9585-118">Requirements</span></span>



| <span data-ttu-id="f9585-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f9585-119">Requirement</span></span> | <span data-ttu-id="f9585-120">Wert</span><span class="sxs-lookup"><span data-stu-id="f9585-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f9585-121">Header</span><span class="sxs-lookup"><span data-stu-id="f9585-121">Header</span></span><br/>  | <dl> <span data-ttu-id="f9585-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9585-122"><dt>D3dx12.h</dt></span></span> </dl>  |
| <span data-ttu-id="f9585-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f9585-123">Library</span></span><br/> | <dl> <span data-ttu-id="f9585-124"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f9585-124"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="f9585-125">DLL</span><span class="sxs-lookup"><span data-stu-id="f9585-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="f9585-126"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f9585-126"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9585-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f9585-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9585-128">Funktionen des Hilfsprogramms für D3D12</span><span class="sxs-lookup"><span data-stu-id="f9585-128">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)
</dt> </dl>

 

 





