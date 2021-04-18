---
description: Gibt die Anzahl der Elemente in jeder der drei Warteschlangen innerhalb der Thread Pumpe an.
ms.assetid: b5b829a5-5ef7-4ef5-afb4-efe1bb22ae70
title: 'ID3DX10ThreadPump:: getqueuestatus-Methode (d3dx10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10ThreadPump.GetQueueStatus
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 4cf3b5879da0346cefbb5b8835d6922dd736cfd3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106365867"
---
# <a name="id3dx10threadpumpgetqueuestatus-method"></a><span data-ttu-id="94c22-103">ID3DX10ThreadPump:: getqueuestatus-Methode</span><span class="sxs-lookup"><span data-stu-id="94c22-103">ID3DX10ThreadPump::GetQueueStatus method</span></span>

<span data-ttu-id="94c22-104">Gibt die Anzahl der Elemente in jeder der drei Warteschlangen innerhalb der Thread Pumpe an.</span><span class="sxs-lookup"><span data-stu-id="94c22-104">Get the number of items in each of the three queues inside the thread pump.</span></span>

## <a name="syntax"></a><span data-ttu-id="94c22-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="94c22-105">Syntax</span></span>


```C++
HRESULT GetQueueStatus(
  [in] UINT *pIoQueue,
  [in] UINT *pProcessQueue,
  [in] UINT *pDeviceQueue
);
```



## <a name="parameters"></a><span data-ttu-id="94c22-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="94c22-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94c22-107">*pioqueue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="94c22-107">*pIoQueue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94c22-108">Typ: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="94c22-108">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="94c22-109">Anzahl der Elemente in der e/a-Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="94c22-109">Number of items in the I/O queue.</span></span>

</dd> <dt>

<span data-ttu-id="94c22-110">*pprocessqueue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="94c22-110">*pProcessQueue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94c22-111">Typ: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="94c22-111">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="94c22-112">Anzahl der Elemente in der Verarbeitungs Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="94c22-112">Number of items in the process queue.</span></span>

</dd> <dt>

<span data-ttu-id="94c22-113">*pdevicequeue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="94c22-113">*pDeviceQueue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94c22-114">Typ: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="94c22-114">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="94c22-115">Anzahl der Elemente in der Geräte Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="94c22-115">Number of items in the device queue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94c22-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="94c22-116">Return value</span></span>

<span data-ttu-id="94c22-117">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="94c22-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="94c22-118">Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="94c22-118">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="94c22-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="94c22-119">Requirements</span></span>



| <span data-ttu-id="94c22-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="94c22-120">Requirement</span></span> | <span data-ttu-id="94c22-121">Wert</span><span class="sxs-lookup"><span data-stu-id="94c22-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="94c22-122">Header</span><span class="sxs-lookup"><span data-stu-id="94c22-122">Header</span></span><br/>  | <dl> <span data-ttu-id="94c22-123"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="94c22-123"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="94c22-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="94c22-124">Library</span></span><br/> | <dl> <span data-ttu-id="94c22-125"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="94c22-125"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94c22-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="94c22-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94c22-127">ID3DX10ThreadPump</span><span class="sxs-lookup"><span data-stu-id="94c22-127">ID3DX10ThreadPump</span></span>](id3dx10threadpump.md)
</dt> <dt>

[<span data-ttu-id="94c22-128">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="94c22-128">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
