---
title: IDXCoreAdapter::QueryState
description: Ruft den aktuellen Zustand des angegebenen Elements auf dem Adapter ab.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 61fc5c601904011de8f343777a95385a16ec3d7e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106338283"
---
# <a name="idxcoreadapterquerystate-method"></a><span data-ttu-id="87c08-103">Idxcoreadapter:: querystate-Methode</span><span class="sxs-lookup"><span data-stu-id="87c08-103">IDXCoreAdapter::QueryState method</span></span>

<span data-ttu-id="87c08-104">Ruft den aktuellen Zustand des angegebenen Elements auf dem Adapter ab.</span><span class="sxs-lookup"><span data-stu-id="87c08-104">Retrieves the current state of the specified item on the adapter.</span></span> <span data-ttu-id="87c08-105">Rufen Sie vor dem Aufrufen von **querystate** für einen Eigenschaftentyp [isquerystaatupportiert](./nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) auf, um zu bestätigen, dass für diesen Adapter und dieses Betriebssystem eine Abfrage der Art des Zustands verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="87c08-105">Before calling **QueryState** for a property type, call [IsQueryStateSupported](./nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) to confirm that querying the state kind is available for this adapter and operating system (OS).</span></span>

## <a name="syntax"></a><span data-ttu-id="87c08-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="87c08-106">Syntax</span></span>

```cpp
virtual HRESULT STDMETHODCALLTYPE QueryState( 
  DXCoreAdapterState state,
  size_t inputStateDetailsSize,
  _In_reads_bytes_opt_(inputStateDetailsSize) const void *inputStateDetails,
  size_t outputBufferSize,
  _Out_writes_bytes_(outputBufferSize) void *outputBuffer) = 0;

template <class T1, class T2>
HRESULT QueryState( 
  DXCoreAdapterState state,
  _In_reads_bytes_opt_(sizeof(T1)) const T1 *inputStateDetails,
  _Out_writes_bytes_(sizeof(T2)) T2 *outputBuffer);

template <class T>
HRESULT QueryState( 
  DXCoreAdapterState state,
  _Out_writes_bytes_(sizeof(T)) T *outputBuffer);
```

## <a name="parameters"></a><span data-ttu-id="87c08-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="87c08-107">Parameters</span></span>

### <a name="state"></a><span data-ttu-id="87c08-108">state</span><span class="sxs-lookup"><span data-stu-id="87c08-108">state</span></span>

<span data-ttu-id="87c08-109">Typ: **[dxcoreadapterstate](./ne-dxcore_interface-dxcoreadapterstate.md)**</span><span class="sxs-lookup"><span data-stu-id="87c08-109">Type: **[DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md)**</span></span>

<span data-ttu-id="87c08-110">Die Art des Zustands Elements auf dem Adapter, dessen Zustand Sie abrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="87c08-110">The kind of state item on the adapter whose state you wish to retrieve.</span></span> <span data-ttu-id="87c08-111">Weitere Informationen zu den einzelnen adapterstatusarten finden Sie in der Tabelle unter [dxcoreadapterstate](./ne-dxcore_interface-dxcoreadapterstate.md) .</span><span class="sxs-lookup"><span data-stu-id="87c08-111">See the table in [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) for more info about each adapter state kind.</span></span>

### <a name="inputstatedetailssize"></a><span data-ttu-id="87c08-112">Input statedetailssize</span><span class="sxs-lookup"><span data-stu-id="87c08-112">inputStateDetailsSize</span></span>

<span data-ttu-id="87c08-113">Typ: **size_t**</span><span class="sxs-lookup"><span data-stu-id="87c08-113">Type: **size_t**</span></span>

<span data-ttu-id="87c08-114">Die Größe (in Bytes) des Eingangs Zustands Details-Puffers, den Sie (optional) zuordnen und in *inputstatedetails* angeben können.</span><span class="sxs-lookup"><span data-stu-id="87c08-114">The size, in bytes, of the input state details buffer that you (optionally) allocate and provide in *inputStateDetails*.</span></span>

### <a name="inputstatedetails-in"></a><span data-ttu-id="87c08-115">Input statedetails [in]</span><span class="sxs-lookup"><span data-stu-id="87c08-115">inputStateDetails [in]</span></span>

<span data-ttu-id="87c08-116">Typ: **void konstant \***</span><span class="sxs-lookup"><span data-stu-id="87c08-116">Type: **void const\***</span></span>

<span data-ttu-id="87c08-117">Ein optionaler Zeiger auf einen konstanten Eingabe Zustands Details-Puffer, den Sie in der Anwendung zuordnen, der alle Informationen zu Ihrer Anforderung enthält, die für die im *Status* angegebene Zustands Angabe erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="87c08-117">An optional pointer to a constant input state details buffer that you allocate in your application, containing any information about your request that's required for the state kind you specify in *state*.</span></span> <span data-ttu-id="87c08-118">Weitere Informationen zu allen Eingabepuffer Anforderungen für eine bestimmte Statusart finden Sie in der Tabelle unter [dxcoreadapterstate](./ne-dxcore_interface-dxcoreadapterstate.md) .</span><span class="sxs-lookup"><span data-stu-id="87c08-118">See the table in [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) for more info about any input buffer requirement for a given state kind.</span></span>

### <a name="outputbuffersize"></a><span data-ttu-id="87c08-119">outputbuffersize</span><span class="sxs-lookup"><span data-stu-id="87c08-119">outputBufferSize</span></span>

<span data-ttu-id="87c08-120">Typ: **size_t**</span><span class="sxs-lookup"><span data-stu-id="87c08-120">Type: **size_t**</span></span>

<span data-ttu-id="87c08-121">Die Größe (in Bytes) des Ausgabepuffers, den Sie zuordnen und in *OUTPUTBUFFER* bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="87c08-121">The size, in bytes, of the output buffer that you allocate and provide in *outputBuffer*.</span></span>

### <a name="outputbuffer-out"></a><span data-ttu-id="87c08-122">OUTPUTBUFFER [out]</span><span class="sxs-lookup"><span data-stu-id="87c08-122">outputBuffer [out]</span></span>

<span data-ttu-id="87c08-123">Typ: **void \***</span><span class="sxs-lookup"><span data-stu-id="87c08-123">Type: **void\***</span></span>

<span data-ttu-id="87c08-124">Ein Zeiger auf einen Ausgabepuffer, den Sie in der Anwendung zuordnen, und der die Funktion ausfüllt.</span><span class="sxs-lookup"><span data-stu-id="87c08-124">A pointer to an output buffer that you allocate in your application, and that the function fills in.</span></span> <span data-ttu-id="87c08-125">Weitere Informationen zu den Anforderungen des Ausgabepuffers für eine bestimmte Art von Zustand finden Sie in der Tabelle unter [dxcoreadapterstate](./ne-dxcore_interface-dxcoreadapterstate.md) .</span><span class="sxs-lookup"><span data-stu-id="87c08-125">See the table in [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) for more info about the output buffer requirement for a given state kind.</span></span>

## <a name="returns"></a><span data-ttu-id="87c08-126">Gibt zurück</span><span class="sxs-lookup"><span data-stu-id="87c08-126">Returns</span></span>

<span data-ttu-id="87c08-127">Typ: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="87c08-127">Type: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="87c08-128">Wenn die Funktion erfolgreich ausgeführt wird, wird **S_OK** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="87c08-128">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="87c08-129">Andernfalls wird ein [**HRESULT**](../../com/structure-of-com-error-codes.md) - [Fehlercode](../../com/com-error-codes-10.md)zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="87c08-129">Otherwise, it returns an [**HRESULT**](../../com/structure-of-com-error-codes.md) [error code](../../com/com-error-codes-10.md).</span></span>

|<span data-ttu-id="87c08-130">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="87c08-130">Return value</span></span>|<span data-ttu-id="87c08-131">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="87c08-131">Description</span></span>|
|-|-|
|<span data-ttu-id="87c08-132">DXGI_ERROR_DEVICE_REMOVED</span><span class="sxs-lookup"><span data-stu-id="87c08-132">DXGI_ERROR_DEVICE_REMOVED</span></span>|<span data-ttu-id="87c08-133">Der Adapter befindet sich nicht mehr in einem gültigen Zustand.</span><span class="sxs-lookup"><span data-stu-id="87c08-133">The adapter is no longer in a valid state.</span></span>|
|<span data-ttu-id="87c08-134">DXGI_ERROR_INVALID_CALL</span><span class="sxs-lookup"><span data-stu-id="87c08-134">DXGI_ERROR_INVALID_CALL</span></span>|<span data-ttu-id="87c08-135">Die im *Status* angegebene Zustands Angabe wird von diesem Betriebssystem (OS) nicht erkannt.</span><span class="sxs-lookup"><span data-stu-id="87c08-135">The state kind specified in *state* is not recognized by this operating system (OS).</span></span> <span data-ttu-id="87c08-136">Wenden Sie sich an [isquerystaatupportiert](./nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) , um zu bestätigen, dass für diesen Adapter und dieses Betriebssystem eine Abfrage der Art des Zustands verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="87c08-136">Call [IsQueryStateSupported](./nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) to confirm that querying the state kind is available for this adapter and operating system (OS).</span></span>|
|<span data-ttu-id="87c08-137">DXGI_ERROR_UNSUPPORTED</span><span class="sxs-lookup"><span data-stu-id="87c08-137">DXGI_ERROR_UNSUPPORTED</span></span>|<span data-ttu-id="87c08-138">Die im *Status* angegebene Statusart wird vom Adapter nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="87c08-138">The state kind specified in *state* is not supported by the adapter.</span></span> <span data-ttu-id="87c08-139">Wenden Sie sich an [isquerystaatupportiert](./nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) , um zu bestätigen, dass für diesen Adapter und dieses Betriebssystem eine Abfrage der Art des Zustands verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="87c08-139">Call [IsQueryStateSupported](./nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) to confirm that querying the state kind is available for this adapter and operating system (OS).</span></span>|
|<span data-ttu-id="87c08-140">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="87c08-140">E_INVALIDARG</span></span>|<span data-ttu-id="87c08-141">Eine unzureichende Puffergröße wird für *OUTPUTBUFFER* bereitgestellt (oder für input *statedetails* , wenn ein Eingabe Zustands Details-Puffer erforderlich ist).</span><span class="sxs-lookup"><span data-stu-id="87c08-141">An insufficient buffer size is provided for *outputBuffer* (or for *inputStateDetails* where an input state details buffer is necessary).</span></span>|
|<span data-ttu-id="87c08-142">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="87c08-142">E_POINTER</span></span>|<span data-ttu-id="87c08-143">`nullptr` wurde für *OUTPUTBUFFER* bereitgestellt (oder für *inputstatedetails* , wenn ein Eingabe Zustands Details-Puffer erforderlich ist).</span><span class="sxs-lookup"><span data-stu-id="87c08-143">`nullptr` was provided for *outputBuffer* (or for *inputStateDetails* where an input state details buffer is necessary).</span></span>|

## <a name="remarks"></a><span data-ttu-id="87c08-144">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="87c08-144">Remarks</span></span>

<span data-ttu-id="87c08-145">Weitere Informationen zu den einzelnen adapterstatusart und den verwendeten Eingaben und Ausgaben finden Sie unter [dxcoreadapterstate](./ne-dxcore_interface-dxcoreadapterstate.md) .</span><span class="sxs-lookup"><span data-stu-id="87c08-145">See [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) for more info about each adapter state kind, and what inputs and outputs are used.</span></span> <span data-ttu-id="87c08-146">Diese Funktion gibt den *OUTPUTBUFFER* -Puffer aus, bevor Sie aufgefüllt wird.</span><span class="sxs-lookup"><span data-stu-id="87c08-146">This function zeros out the *outputBuffer* buffer prior to filling it in.</span></span>

## <a name="see-also"></a><span data-ttu-id="87c08-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="87c08-147">See also</span></span>

<span data-ttu-id="87c08-148">[Idxcoreadapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore-Referenz](../dxcore-reference.md), [Verwenden von DXCore zum Auflisten von Adaptern](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="87c08-148">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>