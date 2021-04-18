---
description: Fügen Sie der Thread Pumpe ein Arbeits Element hinzu.
ms.assetid: f07789dc-a3d5-4bad-9768-527e701271b8
title: 'ID3DX10ThreadPump:: addworkitem-Methode (d3dx10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10ThreadPump.AddWorkItem
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: aaf5286ca6cf7b61b0027b176d9a9261bd0beaa8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106354416"
---
# <a name="id3dx10threadpumpaddworkitem-method"></a><span data-ttu-id="11f4c-103">ID3DX10ThreadPump:: addworkitem-Methode</span><span class="sxs-lookup"><span data-stu-id="11f4c-103">ID3DX10ThreadPump::AddWorkItem method</span></span>

<span data-ttu-id="11f4c-104">Fügen Sie der Thread Pumpe ein Arbeits Element hinzu.</span><span class="sxs-lookup"><span data-stu-id="11f4c-104">Add a work item to the thread pump.</span></span>

## <a name="syntax"></a><span data-ttu-id="11f4c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="11f4c-105">Syntax</span></span>


```C++
HRESULT AddWorkItem(
  [in]  ID3DX10DataLoader    *pDataLoader,
  [in]  ID3DX10DataProcessor *pDataProcessor,
  [in]  HRESULT              *pHResult,
  [out] void                 **ppDeviceObject
);
```



## <a name="parameters"></a><span data-ttu-id="11f4c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="11f4c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11f4c-107">*pdataloader* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="11f4c-107">*pDataLoader* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11f4c-108">Typ: **[ **ID3DX10DataLoader**](id3dx10dataloader.md)\***</span><span class="sxs-lookup"><span data-stu-id="11f4c-108">Type: **[**ID3DX10DataLoader**](id3dx10dataloader.md)\***</span></span>

<span data-ttu-id="11f4c-109">Das Lade Modul, das vom threadpump verwendet wird, wenn ein Arbeits Element zum Laden von Daten benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="11f4c-109">The loader that the thread pump will use when a work item requires data to be loaded.</span></span>

</dd> <dt>

<span data-ttu-id="11f4c-110">*pdataprocessor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="11f4c-110">*pDataProcessor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11f4c-111">Typ: **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\***</span><span class="sxs-lookup"><span data-stu-id="11f4c-111">Type: **[**ID3DX10DataProcessor**](id3dx10dataprocessor.md)\***</span></span>

<span data-ttu-id="11f4c-112">Der Prozessor, den das Thread-Pump-Element verwendet, wenn für eine Arbeitsaufgabe die Verarbeitung von Daten erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="11f4c-112">The processor that the thread pump will use when a work item requires data to be processed.</span></span>

</dd> <dt>

<span data-ttu-id="11f4c-113">*phresult* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="11f4c-113">*pHResult* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11f4c-114">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="11f4c-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="11f4c-115">Ein Zeiger auf den Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="11f4c-115">A pointer to the return value.</span></span> <span data-ttu-id="11f4c-116">Kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="11f4c-116">May be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="11f4c-117">*ppdeviceobject* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="11f4c-117">*ppDeviceObject* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="11f4c-118">Typ: **void \* \***</span><span class="sxs-lookup"><span data-stu-id="11f4c-118">Type: **void\*\***</span></span>

<span data-ttu-id="11f4c-119">Das Gerät, von dem das-Objekt verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="11f4c-119">The device that uses the object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11f4c-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="11f4c-120">Return value</span></span>

<span data-ttu-id="11f4c-121">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="11f4c-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="11f4c-122">Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="11f4c-122">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="11f4c-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="11f4c-123">Requirements</span></span>



| <span data-ttu-id="11f4c-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="11f4c-124">Requirement</span></span> | <span data-ttu-id="11f4c-125">Wert</span><span class="sxs-lookup"><span data-stu-id="11f4c-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="11f4c-126">Header</span><span class="sxs-lookup"><span data-stu-id="11f4c-126">Header</span></span><br/>  | <dl> <span data-ttu-id="11f4c-127"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="11f4c-127"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="11f4c-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="11f4c-128">Library</span></span><br/> | <dl> <span data-ttu-id="11f4c-129"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="11f4c-129"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11f4c-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="11f4c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11f4c-131">ID3DX10ThreadPump</span><span class="sxs-lookup"><span data-stu-id="11f4c-131">ID3DX10ThreadPump</span></span>](id3dx10threadpump.md)
</dt> <dt>

[<span data-ttu-id="11f4c-132">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="11f4c-132">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




