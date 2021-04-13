---
title: IDXCoreAdapterFactory::GetAdapterByLuid
description: Ruft das DXCore-Adapter Objekt ([idxcoreadapter](./nn-dxcore_interface-idxcoreadapter.md)) für eine angegebene LUID ab, falls verfügbar.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 30835948978e5c7f3f11f903322e4fa41f71d210
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390742"
---
# <a name="idxcoreadapterfactorygetadapterbyluid-method"></a><span data-ttu-id="2f965-103">Idxcoreadapterfactory:: getadapterbyluid-Methode</span><span class="sxs-lookup"><span data-stu-id="2f965-103">IDXCoreAdapterFactory::GetAdapterByLuid method</span></span>

<span data-ttu-id="2f965-104">Ruft das DXCore-Adapter Objekt ([idxcoreadapter](./nn-dxcore_interface-idxcoreadapter.md)) für eine angegebene LUID ab, falls verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2f965-104">Retrieves the DXCore adapter object ([IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md)) for a specified LUID, if available.</span></span> <span data-ttu-id="2f965-105">Programmieranleitungen und Codebeispiele finden [Sie unter Verwenden von DXCore zum Aufzählen von Adaptern](../dxcore-enum-adapters.md).</span><span class="sxs-lookup"><span data-stu-id="2f965-105">For programming guidance, and code examples, see [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="2f965-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="2f965-106">Syntax</span></span>

```cpp
virtual HRESULT STDMETHODCALLTYPE GetAdapterByLuid( 
  const LUID &adapterLUID,
   REFIID riid,
  _COM_Outptr_ void **ppvAdapter) = 0;

template<class T>
HRESULT STDMETHODCALLTYPE GetAdapterByLuid( 
  const LUID &adapterLUID,
  _COM_Outptr_ T **ppvAdapter);
```

## <a name="parameters"></a><span data-ttu-id="2f965-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="2f965-107">Parameters</span></span>

### <a name="adapterluid"></a><span data-ttu-id="2f965-108">adapterluid</span><span class="sxs-lookup"><span data-stu-id="2f965-108">adapterLUID</span></span>

<span data-ttu-id="2f965-109">Typ: **[LUID](/windows/win32/api/winnt/ns-winnt-luid) -Konstante\&**</span><span class="sxs-lookup"><span data-stu-id="2f965-109">Type: **[LUID](/windows/win32/api/winnt/ns-winnt-luid) const\&**</span></span>

<span data-ttu-id="2f965-110">Der lokal eindeutige Wert, der die Adapter Instanz identifiziert.</span><span class="sxs-lookup"><span data-stu-id="2f965-110">The locally unique value that identifies the adapter instance.</span></span>

### <a name="riid-in"></a><span data-ttu-id="2f965-111">riid [in]</span><span class="sxs-lookup"><span data-stu-id="2f965-111">riid [in]</span></span>

<span data-ttu-id="2f965-112">Typ: **refID**</span><span class="sxs-lookup"><span data-stu-id="2f965-112">Type: **REFIID**</span></span>

<span data-ttu-id="2f965-113">Ein Verweis auf die Globally Unique Identifier (GUID) der Schnittstelle, die in *ppvadapter* zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="2f965-113">A reference to the globally unique identifier (GUID) of the interface that you wish to be returned in *ppvAdapter*.</span></span> <span data-ttu-id="2f965-114">Dies wird als Schnittstellen Bezeichner (IID) von [idxcoreadapter](./nn-dxcore_interface-idxcoreadapter.md)erwartet.</span><span class="sxs-lookup"><span data-stu-id="2f965-114">This is expected to be the interface identifier (IID) of [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md).</span></span>

### <a name="ppvadapter-out"></a><span data-ttu-id="2f965-115">ppvadapter [out]</span><span class="sxs-lookup"><span data-stu-id="2f965-115">ppvAdapter [out]</span></span>

<span data-ttu-id="2f965-116">Typ: **void \* \***</span><span class="sxs-lookup"><span data-stu-id="2f965-116">Type: **void\*\***</span></span>

<span data-ttu-id="2f965-117">Die Adresse eines Zeigers auf eine Schnittstelle mit der im *riid* -Parameter angegebenen IID.</span><span class="sxs-lookup"><span data-stu-id="2f965-117">The address of a pointer to an interface with the IID specified in the *riid* parameter.</span></span> <span data-ttu-id="2f965-118">Bei erfolgreicher Rückgabe enthält *\* ppvadapter* (die Dereferenzierte Adresse) einen Zeiger auf den erstellten DXCore-Adapter.</span><span class="sxs-lookup"><span data-stu-id="2f965-118">Upon successful return, *\*ppvAdapter* (the dereferenced address) contains a pointer to the DXCore adapter created.</span></span>

## <a name="returns"></a><span data-ttu-id="2f965-119">Gibt zurück</span><span class="sxs-lookup"><span data-stu-id="2f965-119">Returns</span></span>

<span data-ttu-id="2f965-120">Typ: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="2f965-120">Type: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="2f965-121">Wenn die Funktion erfolgreich ausgeführt wird, wird **S_OK** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2f965-121">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="2f965-122">Andernfalls wird ein [**HRESULT**](../../com/structure-of-com-error-codes.md) - [Fehlercode](../../com/com-error-codes-10.md)zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2f965-122">Otherwise, it returns an [**HRESULT**](../../com/structure-of-com-error-codes.md) [error code](../../com/com-error-codes-10.md).</span></span>

|<span data-ttu-id="2f965-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2f965-123">Return value</span></span>|<span data-ttu-id="2f965-124">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2f965-124">Description</span></span>|
|-|-|
|<span data-ttu-id="2f965-125">DXGI_ERROR_DEVICE_REMOVED</span><span class="sxs-lookup"><span data-stu-id="2f965-125">DXGI_ERROR_DEVICE_REMOVED</span></span>|<span data-ttu-id="2f965-126">Die in *adapterluid* weiter gegebene Adapter-LUID wird erkannt, aber der Adapter befindet sich nicht mehr in einem gültigen Zustand.</span><span class="sxs-lookup"><span data-stu-id="2f965-126">The adapter LUID passed in *adapterLUID* is recognized, but the adapter is no longer in a valid state.</span></span>|
|<span data-ttu-id="2f965-127">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="2f965-127">E_INVALIDARG</span></span>|<span data-ttu-id="2f965-128">Keine solche Adapter-LUID, da der in *adapterluid* über gegebene Wert über DXCore verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="2f965-128">No such adapter LUID as the value passed in *adapterLUID* is available through DXCore.</span></span>|
|<span data-ttu-id="2f965-129">E_NOINTERFACE</span><span class="sxs-lookup"><span data-stu-id="2f965-129">E_NOINTERFACE</span></span>|<span data-ttu-id="2f965-130">Für *riid* wurde ein ungültiger Wert angegeben.</span><span class="sxs-lookup"><span data-stu-id="2f965-130">An invalid value was provided for *riid*.</span></span>|
|<span data-ttu-id="2f965-131">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="2f965-131">E_POINTER</span></span>|<span data-ttu-id="2f965-132">`nullptr` wurde für *ppvadapter* bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="2f965-132">`nullptr` was provided for *ppvAdapter*.</span></span>|

## <a name="remarks"></a><span data-ttu-id="2f965-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2f965-133">Remarks</span></span>

<span data-ttu-id="2f965-134">Mehrere Aufrufe, die dieselbe [LUID](/windows/win32/api/winnt/ns-winnt-luid) übergeben, geben identische Schnittstellen Zeiger zurück.</span><span class="sxs-lookup"><span data-stu-id="2f965-134">Multiple calls passing the same [LUID](/windows/win32/api/winnt/ns-winnt-luid) return identical interface pointers.</span></span> <span data-ttu-id="2f965-135">Daher ist es sicher, Schnittstellen Zeiger zu vergleichen, um zu bestimmen, ob mehrere Zeiger auf dasselbe Adapter Objekt verweisen.</span><span class="sxs-lookup"><span data-stu-id="2f965-135">As a result, it's safe to compare interface pointers to determine whether multiple pointers refer to the same adapter object.</span></span>

## <a name="see-also"></a><span data-ttu-id="2f965-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2f965-136">See also</span></span>

<span data-ttu-id="2f965-137">[Idxcoreadapterfactory](./nn-dxcore_interface-idxcoreadapterfactory.md), [DXCore-Referenz](../dxcore-reference.md), [Verwenden von DXCore zum Auflisten von Adaptern](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="2f965-137">[IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>