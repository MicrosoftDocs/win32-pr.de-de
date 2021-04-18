---
title: IDXCoreAdapter::SetState
description: Legt den Zustand des angegebenen Elements auf dem Adapter fest.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 8cbeacdb8c6020441b5dd74a9f9233a6c112b4f6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106340729"
---
# <a name="idxcoreadaptersetstate-method"></a><span data-ttu-id="f5090-103">Idxcoreadapter:: SetState-Methode</span><span class="sxs-lookup"><span data-stu-id="f5090-103">IDXCoreAdapter::SetState method</span></span>

<span data-ttu-id="f5090-104">Legt den Zustand des angegebenen Elements auf dem Adapter fest.</span><span class="sxs-lookup"><span data-stu-id="f5090-104">Sets the state of the specified item on the adapter.</span></span> <span data-ttu-id="f5090-105">Bevor Sie **SetState** für einen Eigenschaftentyp aufrufen, rufen Sie [issetstaatupportiert](./nf-dxcore_interface-idxcoreadapter-issetstatesupported.md) auf, um zu bestätigen, dass das Festlegen der Statusart für diesen Adapter und das Betriebssystem (OS) verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="f5090-105">Before calling **SetState** for a property type, call [IsSetStateSupported](./nf-dxcore_interface-idxcoreadapter-issetstatesupported.md) to confirm that setting the state kind is available for this adapter and operating system (OS).</span></span>

## <a name="syntax"></a><span data-ttu-id="f5090-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="f5090-106">Syntax</span></span>

```cpp
virtual HRESULT STDMETHODCALLTYPE SetState( 
  DXCoreAdapterState state,
  size_t inputStateDetailsSize,
  _In_reads_bytes_opt_(inputStateDetailsSize) const void *inputStateDetails,
  size_t inputDataSize,
  _In_reads_bytes_(inputDataSize) const void *inputData) = 0;

template <class T1, class T2>
HRESULT SetState( 
  DXCoreAdapterState state,
  const T1 *inputStateDetails,
  const T2 *inputData);
```

## <a name="parameters"></a><span data-ttu-id="f5090-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="f5090-107">Parameters</span></span>

### <a name="state"></a><span data-ttu-id="f5090-108">state</span><span class="sxs-lookup"><span data-stu-id="f5090-108">state</span></span>

<span data-ttu-id="f5090-109">Typ: **[dxcoreadapterstate](./ne-dxcore_interface-dxcoreadapterstate.md)**</span><span class="sxs-lookup"><span data-stu-id="f5090-109">Type: **[DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md)**</span></span>

<span data-ttu-id="f5090-110">Die Art des Zustands Elements auf dem Adapter, dessen Zustand Sie festlegen möchten.</span><span class="sxs-lookup"><span data-stu-id="f5090-110">The kind of state item on the adapter whose state you wish to set.</span></span> <span data-ttu-id="f5090-111">Weitere Informationen zu den einzelnen adapterstatusarten finden Sie in der Tabelle unter [dxcoreadapterstate](./ne-dxcore_interface-dxcoreadapterstate.md) .</span><span class="sxs-lookup"><span data-stu-id="f5090-111">See the table in [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) for more info about each adapter state kind.</span></span>

### <a name="inputstatedetailssize"></a><span data-ttu-id="f5090-112">Input statedetailssize</span><span class="sxs-lookup"><span data-stu-id="f5090-112">inputStateDetailsSize</span></span>

<span data-ttu-id="f5090-113">Typ: **size_t**</span><span class="sxs-lookup"><span data-stu-id="f5090-113">Type: **size_t**</span></span>

<span data-ttu-id="f5090-114">Die Größe (in Bytes) des Eingangs Zustands Details-Puffers, den Sie (optional) zuordnen und in *inputstatedetails* angeben können.</span><span class="sxs-lookup"><span data-stu-id="f5090-114">The size, in bytes, of the input state details buffer that you (optionally) allocate and provide in *inputStateDetails*.</span></span>

### <a name="inputstatedetails-in"></a><span data-ttu-id="f5090-115">Input statedetails [in]</span><span class="sxs-lookup"><span data-stu-id="f5090-115">inputStateDetails [in]</span></span>

<span data-ttu-id="f5090-116">Typ: **void konstant \***</span><span class="sxs-lookup"><span data-stu-id="f5090-116">Type: **void const\***</span></span>

<span data-ttu-id="f5090-117">Ein optionaler Zeiger auf einen konstanten Eingabe Zustands Details-Puffer, den Sie in der Anwendung zuordnen, der alle Informationen zu Ihrer Anforderung enthält, die für die im *Status* angegebene Zustands Angabe erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="f5090-117">An optional pointer to a constant input state details buffer that you allocate in your application, containing any information about your request that's required for the state kind you specify in *state*.</span></span> <span data-ttu-id="f5090-118">Weitere Informationen zu allen Eingabepuffer Anforderungen für eine bestimmte Statusart finden Sie in der Tabelle unter [dxcoreadapterstate](./ne-dxcore_interface-dxcoreadapterstate.md) .</span><span class="sxs-lookup"><span data-stu-id="f5090-118">See the table in [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) for more info about any input buffer requirement for a given state kind.</span></span>

### <a name="inputdatasize"></a><span data-ttu-id="f5090-119">inputdatasize</span><span class="sxs-lookup"><span data-stu-id="f5090-119">inputDataSize</span></span>

<span data-ttu-id="f5090-120">Typ: **size_t**</span><span class="sxs-lookup"><span data-stu-id="f5090-120">Type: **size_t**</span></span>

<span data-ttu-id="f5090-121">Die Größe (in Bytes) des Eingabe Puffers, den Sie zuordnen und in *inputData* bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="f5090-121">The size, in bytes, of the input buffer that you allocate and provide in *inputData*.</span></span>

### <a name="inputdata-in"></a><span data-ttu-id="f5090-122">Input Data [in]</span><span class="sxs-lookup"><span data-stu-id="f5090-122">inputData [in]</span></span>

<span data-ttu-id="f5090-123">Typ: **void \***</span><span class="sxs-lookup"><span data-stu-id="f5090-123">Type: **void\***</span></span>

<span data-ttu-id="f5090-124">Ein Zeiger auf einen Eingabepuffer, den Sie in der Anwendung zuordnen, mit den Zustandsinformationen, die für das Zustands Element festgelegt werden, dessen Art Sie im *Zustand* angeben.</span><span class="sxs-lookup"><span data-stu-id="f5090-124">A pointer to an input buffer that you allocate in your application, containing the state information to set for the state item whose kind you specify in *state*.</span></span> <span data-ttu-id="f5090-125">Weitere Informationen zu den Eingabepuffer Anforderungen für eine bestimmte Art von Zustand finden Sie in der Tabelle unter [dxcoreadapterstate](./ne-dxcore_interface-dxcoreadapterstate.md) .</span><span class="sxs-lookup"><span data-stu-id="f5090-125">See the table in [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) for more info about the input buffer requirement for a given state kind.</span></span>

## <a name="returns"></a><span data-ttu-id="f5090-126">Gibt zurück</span><span class="sxs-lookup"><span data-stu-id="f5090-126">Returns</span></span>

<span data-ttu-id="f5090-127">Typ: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="f5090-127">Type: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="f5090-128">Wenn die Funktion erfolgreich ausgeführt wird, wird **S_OK** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f5090-128">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="f5090-129">Andernfalls wird ein [**HRESULT**](../../com/structure-of-com-error-codes.md) - [Fehlercode](../../com/com-error-codes-10.md)zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f5090-129">Otherwise, it returns an [**HRESULT**](../../com/structure-of-com-error-codes.md) [error code](../../com/com-error-codes-10.md).</span></span>

|<span data-ttu-id="f5090-130">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f5090-130">Return value</span></span>|<span data-ttu-id="f5090-131">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f5090-131">Description</span></span>|
|-|-|
|<span data-ttu-id="f5090-132">DXGI_ERROR_DEVICE_REMOVED</span><span class="sxs-lookup"><span data-stu-id="f5090-132">DXGI_ERROR_DEVICE_REMOVED</span></span>|<span data-ttu-id="f5090-133">Der Adapter befindet sich nicht mehr in einem gültigen Zustand.</span><span class="sxs-lookup"><span data-stu-id="f5090-133">The adapter is no longer in a valid state.</span></span>|
|<span data-ttu-id="f5090-134">DXGI_ERROR_INVALID_CALL</span><span class="sxs-lookup"><span data-stu-id="f5090-134">DXGI_ERROR_INVALID_CALL</span></span>|<span data-ttu-id="f5090-135">Die im *Status* angegebene Zustands Angabe wird von diesem Betriebssystem (OS) nicht erkannt.</span><span class="sxs-lookup"><span data-stu-id="f5090-135">The state kind specified in *state* is not recognized by this operating system (OS).</span></span> <span data-ttu-id="f5090-136">Wenden Sie sich an [issetstaatupportiert](./nf-dxcore_interface-idxcoreadapter-issetstatesupported.md) , um zu bestätigen, dass das Festlegen der Zustands Art für diesen Adapter und das Betriebssystem (OS) verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="f5090-136">Call [IsSetStateSupported](./nf-dxcore_interface-idxcoreadapter-issetstatesupported.md) to confirm that setting the state kind is available for this adapter and operating system (OS).</span></span>|
|<span data-ttu-id="f5090-137">DXGI_ERROR_UNSUPPORTED</span><span class="sxs-lookup"><span data-stu-id="f5090-137">DXGI_ERROR_UNSUPPORTED</span></span>|<span data-ttu-id="f5090-138">Die im *Status* angegebene Statusart wird vom Adapter nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f5090-138">The state kind specified in *state* is not supported by the adapter.</span></span> <span data-ttu-id="f5090-139">Wenden Sie sich an [issetstaatupportiert](./nf-dxcore_interface-idxcoreadapter-issetstatesupported.md) , um zu bestätigen, dass das Festlegen der Zustands Art für diesen Adapter und das Betriebssystem (OS) verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="f5090-139">Call [IsSetStateSupported](./nf-dxcore_interface-idxcoreadapter-issetstatesupported.md) to confirm that setting the state kind is available for this adapter and operating system (OS).</span></span>|
|<span data-ttu-id="f5090-140">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="f5090-140">E_INVALIDARG</span></span>|<span data-ttu-id="f5090-141">Für *inputData* (oder für *inputstatedetails* , bei denen ein Eingabe Zustands Details-Puffer erforderlich ist) ist eine unzureichende Puffergröße angegeben.</span><span class="sxs-lookup"><span data-stu-id="f5090-141">An insufficient buffer size is provided for *inputData* (or for *inputStateDetails* where an input state details buffer is necessary).</span></span>|
|<span data-ttu-id="f5090-142">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="f5090-142">E_POINTER</span></span>|<span data-ttu-id="f5090-143">`nullptr` wurde für *inputData* bereitgestellt (oder für *inputstatedetails* , wenn ein Eingabe Zustands Details-Puffer erforderlich ist).</span><span class="sxs-lookup"><span data-stu-id="f5090-143">`nullptr` was provided for *inputData* (or for *inputStateDetails* where an input state details buffer is necessary).</span></span>|

## <a name="see-also"></a><span data-ttu-id="f5090-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f5090-144">See also</span></span>

<span data-ttu-id="f5090-145">[Idxcoreadapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore-Referenz](../dxcore-reference.md), [Verwenden von DXCore zum Auflisten von Adaptern](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="f5090-145">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>