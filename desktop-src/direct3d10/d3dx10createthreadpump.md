---
description: Erstellen Sie ein Thread-Pump.
ms.assetid: a7a016e2-784d-4d7a-8058-88895bf3c4e2
title: D3DX10CreateThreadPump-Funktion (d3dx10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateThreadPump
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 8a27f8df1f4eaa8e7f41e863d703063308f9c595
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961723"
---
# <a name="d3dx10createthreadpump-function"></a><span data-ttu-id="a5697-103">D3DX10CreateThreadPump-Funktion</span><span class="sxs-lookup"><span data-stu-id="a5697-103">D3DX10CreateThreadPump function</span></span>

<span data-ttu-id="a5697-104">Erstellen Sie ein Thread-Pump.</span><span class="sxs-lookup"><span data-stu-id="a5697-104">Create a thread pump.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5697-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a5697-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateThreadPump(
  _In_  UINT              cIoThreads,
  _In_  UINT              cProcThreads,
  _Out_ ID3DX10ThreadPump **ppThreadPump
);
```



## <a name="parameters"></a><span data-ttu-id="a5697-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a5697-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5697-107">*ciothreads* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a5697-107">*cIoThreads* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5697-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a5697-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a5697-109">Die Anzahl der zu erstellenden e/a-Threads.</span><span class="sxs-lookup"><span data-stu-id="a5697-109">The number of I/O threads to create.</span></span> <span data-ttu-id="a5697-110">Wenn 0 angegeben wird, versucht Direct3D, die optimale Anzahl von Threads basierend auf der Hardwarekonfiguration zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="a5697-110">If 0 is specified, Direct3D will attempt to calculate the optimal number of threads based on the hardware configuration.</span></span>

</dd> <dt>

<span data-ttu-id="a5697-111">*cprocthreads* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a5697-111">*cProcThreads* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5697-112">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a5697-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a5697-113">Die Anzahl der zu erstellenden Prozessthreads.</span><span class="sxs-lookup"><span data-stu-id="a5697-113">The number of process threads to create.</span></span> <span data-ttu-id="a5697-114">Wenn 0 angegeben wird, versucht Direct3D, die optimale Anzahl von Threads basierend auf der Hardwarekonfiguration zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="a5697-114">If 0 is specified, Direct3D will attempt to calculate the optimal number of threads based on the hardware configuration.</span></span>

</dd> <dt>

<span data-ttu-id="a5697-115">*ppthreadpump* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a5697-115">*ppThreadPump* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a5697-116">Typ: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="a5697-116">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\*\***</span></span>

<span data-ttu-id="a5697-117">Die erstellte Thread-Pump.</span><span class="sxs-lookup"><span data-stu-id="a5697-117">The created thread pump.</span></span> <span data-ttu-id="a5697-118">Siehe [**ID3DX10ThreadPump-Schnittstelle**](id3dx10threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="a5697-118">See [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5697-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a5697-119">Return value</span></span>

<span data-ttu-id="a5697-120">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a5697-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a5697-121">Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="a5697-121">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a5697-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a5697-122">Remarks</span></span>

<span data-ttu-id="a5697-123">Ein Thread Pump ist ein sehr Ressourcen intensives Objekt.</span><span class="sxs-lookup"><span data-stu-id="a5697-123">A thread pump is a very resource-intensive object.</span></span> <span data-ttu-id="a5697-124">Pro Anwendung sollte nur ein Thread Pump erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="a5697-124">Only one thread pump should be created per application.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5697-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a5697-125">Requirements</span></span>



| <span data-ttu-id="a5697-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a5697-126">Requirement</span></span> | <span data-ttu-id="a5697-127">Wert</span><span class="sxs-lookup"><span data-stu-id="a5697-127">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a5697-128">Header</span><span class="sxs-lookup"><span data-stu-id="a5697-128">Header</span></span><br/>  | <dl> <span data-ttu-id="a5697-129"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="a5697-129"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="a5697-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a5697-130">Library</span></span><br/> | <dl> <span data-ttu-id="a5697-131"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a5697-131"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5697-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a5697-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5697-133">Universell Funktionen</span><span class="sxs-lookup"><span data-stu-id="a5697-133">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
