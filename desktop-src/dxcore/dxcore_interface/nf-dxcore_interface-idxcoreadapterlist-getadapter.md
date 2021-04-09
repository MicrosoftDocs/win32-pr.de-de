---
title: IDXCoreAdapterList::GetAdapter
description: Ruft einen bestimmten Adapter nach Index aus einem DXCore-Adapter Listen Objekt ab.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 5ba03c9e6f2711adc5264354a6abd70ee489965f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039417"
---
# <a name="idxcoreadapterlistgetadapter-method"></a><span data-ttu-id="56ed3-103">Idxcoreadapterlist:: GetAdapter-Methode</span><span class="sxs-lookup"><span data-stu-id="56ed3-103">IDXCoreAdapterList::GetAdapter method</span></span>

<span data-ttu-id="56ed3-104">Ruft einen bestimmten Adapter nach Index aus einem DXCore-Adapter Listen Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="56ed3-104">Retrieves a specific adapter by index from a DXCore adapter list object.</span></span> <span data-ttu-id="56ed3-105">Programmieranleitungen und Codebeispiele finden [Sie unter Verwenden von DXCore zum Aufzählen von Adaptern](../dxcore-enum-adapters.md).</span><span class="sxs-lookup"><span data-stu-id="56ed3-105">For programming guidance, and code examples, see [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="56ed3-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="56ed3-106">Syntax</span></span>

```cpp
virtual HRESULT STDMETHODCALLTYPE GetAdapter(
  uint32_t index,
  REFIID riid,
  _COM_Outptr_ void **ppvAdapter) = 0;

template<class T>
HRESULT STDMETHODCALLTYPE GetAdapter( 
  uint32_t index,
  _COM_Outptr_ T **ppvAdapter);
```

## <a name="parameters"></a><span data-ttu-id="56ed3-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="56ed3-107">Parameters</span></span>

### <a name="index"></a><span data-ttu-id="56ed3-108">Index</span><span class="sxs-lookup"><span data-stu-id="56ed3-108">index</span></span>

<span data-ttu-id="56ed3-109">Typ: **uint32_t**</span><span class="sxs-lookup"><span data-stu-id="56ed3-109">Type: **uint32_t**</span></span>

<span data-ttu-id="56ed3-110">Ein NULL basierter Index, der eine Adapter Instanz innerhalb der DXCore-Adapter Liste identifiziert.</span><span class="sxs-lookup"><span data-stu-id="56ed3-110">A zero-based index, identifying an adapter instance within the DXCore adapter list.</span></span>

### <a name="riid"></a><span data-ttu-id="56ed3-111">riid</span><span class="sxs-lookup"><span data-stu-id="56ed3-111">riid</span></span>

<span data-ttu-id="56ed3-112">Typ: **refID**</span><span class="sxs-lookup"><span data-stu-id="56ed3-112">Type: **REFIID**</span></span>

<span data-ttu-id="56ed3-113">Ein Verweis auf die Globally Unique Identifier (GUID) der Schnittstelle, die in *ppvadapter* zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="56ed3-113">A reference to the globally unique identifier (GUID) of the interface that you wish to be returned in *ppvAdapter*.</span></span> <span data-ttu-id="56ed3-114">Dies wird als Schnittstellen Bezeichner (IID) von [idxcoreadapter](./nn-dxcore_interface-idxcoreadapter.md)erwartet.</span><span class="sxs-lookup"><span data-stu-id="56ed3-114">This is expected to be the interface identifier (IID) of [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md).</span></span>

### <a name="ppvadapter-out"></a><span data-ttu-id="56ed3-115">ppvadapter [out]</span><span class="sxs-lookup"><span data-stu-id="56ed3-115">ppvAdapter [out]</span></span>

<span data-ttu-id="56ed3-116">Typ: **void \* \***</span><span class="sxs-lookup"><span data-stu-id="56ed3-116">Type: **void\*\***</span></span>

<span data-ttu-id="56ed3-117">Die Adresse eines Zeigers auf eine Schnittstelle mit der im *riid* -Parameter angegebenen IID.</span><span class="sxs-lookup"><span data-stu-id="56ed3-117">The address of a pointer to an interface with the IID specified in the *riid* parameter.</span></span> <span data-ttu-id="56ed3-118">Bei erfolgreicher Rückgabe enthält *\* ppvadapter* (die Dereferenzierte Adresse) einen Zeiger auf den erstellten DXCore-Adapter.</span><span class="sxs-lookup"><span data-stu-id="56ed3-118">Upon successful return, *\*ppvAdapter* (the dereferenced address) contains a pointer to the DXCore adapter created.</span></span>

## <a name="returns"></a><span data-ttu-id="56ed3-119">Gibt zurück</span><span class="sxs-lookup"><span data-stu-id="56ed3-119">Returns</span></span>

<span data-ttu-id="56ed3-120">Typ: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="56ed3-120">Type: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="56ed3-121">Wenn die Funktion erfolgreich ausgeführt wird, wird **S_OK** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="56ed3-121">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="56ed3-122">Andernfalls wird ein [**HRESULT**](../../com/structure-of-com-error-codes.md) - [Fehlercode](../../com/com-error-codes-10.md)zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="56ed3-122">Otherwise, it returns an [**HRESULT**](../../com/structure-of-com-error-codes.md) [error code](../../com/com-error-codes-10.md).</span></span>

|<span data-ttu-id="56ed3-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="56ed3-123">Return value</span></span>|<span data-ttu-id="56ed3-124">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="56ed3-124">Description</span></span>|
|-|-|
|<span data-ttu-id="56ed3-125">DXGI_ERROR_DEVICE_REMOVED</span><span class="sxs-lookup"><span data-stu-id="56ed3-125">DXGI_ERROR_DEVICE_REMOVED</span></span>|<span data-ttu-id="56ed3-126">Der *Index* ist gültig, aber der Adapter befindet sich nicht mehr in einem gültigen Zustand.</span><span class="sxs-lookup"><span data-stu-id="56ed3-126">The *index* is valid, but the adapter is no longer in a valid state.</span></span>|
|<span data-ttu-id="56ed3-127">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="56ed3-127">E_INVALIDARG</span></span>|<span data-ttu-id="56ed3-128">Der angegebene *Index* ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="56ed3-128">The provided *index* is not valid.</span></span>|
|<span data-ttu-id="56ed3-129">E_NOINTERFACE</span><span class="sxs-lookup"><span data-stu-id="56ed3-129">E_NOINTERFACE</span></span>|<span data-ttu-id="56ed3-130">Für *riid* wurde ein ungültiger Wert angegeben.</span><span class="sxs-lookup"><span data-stu-id="56ed3-130">An invalid value was provided for *riid*.</span></span>|
|<span data-ttu-id="56ed3-131">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="56ed3-131">E_POINTER</span></span>|<span data-ttu-id="56ed3-132">`nullptr` wurde für *ppvadapter* bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="56ed3-132">`nullptr` was provided for *ppvAdapter*.</span></span>|

## <a name="remarks"></a><span data-ttu-id="56ed3-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="56ed3-133">Remarks</span></span>

<span data-ttu-id="56ed3-134">Mehrere Aufrufe, die einen Index übergeben, der denselben Adapter darstellt, geben identische Schnittstellen Zeiger zurück, auch über verschiedene Adapter Listen hinweg.</span><span class="sxs-lookup"><span data-stu-id="56ed3-134">Multiple calls passing an index that represents the same adapter return identical interface pointers, even across different adapter lists.</span></span> <span data-ttu-id="56ed3-135">Daher ist es sicher, Schnittstellen Zeiger zu vergleichen, um zu bestimmen, ob mehrere Zeiger auf dasselbe Adapter Objekt verweisen.</span><span class="sxs-lookup"><span data-stu-id="56ed3-135">As a result, it's safe to compare interface pointers to determine whether multiple pointers refer to the same adapter object.</span></span>

## <a name="see-also"></a><span data-ttu-id="56ed3-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="56ed3-136">See also</span></span>

<span data-ttu-id="56ed3-137">[Idxcoreadapterlist](./nn-dxcore_interface-idxcoreadapterlist.md), [DXCore-Referenz](../dxcore-reference.md), [Verwenden von DXCore zum Auflisten von Adaptern](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="56ed3-137">[IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>