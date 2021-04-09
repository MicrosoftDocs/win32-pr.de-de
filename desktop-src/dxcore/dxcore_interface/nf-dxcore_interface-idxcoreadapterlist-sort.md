---
title: IDXCoreAdapterList::Sort
description: Sortiert ein DXCore-Adapter Listen Objekt auf Grundlage eines angegebenen Eingabe Arrays von Sortierkriterien.
ms.localizationpriority: low
ms.topic: reference
ms.date: 09/03/2019
ms.openlocfilehash: 6260e700053a99b531a66a5c19e15d4a32f07e46
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102195"
---
# <a name="idxcoreadapterlistsort-method"></a><span data-ttu-id="0acf8-103">Idxcoreadapterlist:: Sort-Methode</span><span class="sxs-lookup"><span data-stu-id="0acf8-103">IDXCoreAdapterList::Sort method</span></span>

## <a name="description"></a><span data-ttu-id="0acf8-104">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0acf8-104">Description</span></span>

<span data-ttu-id="0acf8-105">Sortiert ein DXCore-Adapter Listen Objekt auf Grundlage eines angegebenen Eingabe Arrays von Sortierkriterien, wobei Array Elemente an früherer Stelle im Array von Kriterien eine höhere Gewichtung erhalten.</span><span class="sxs-lookup"><span data-stu-id="0acf8-105">Sorts a DXCore adapter list object based on a provided input array of sort criteria, where array items earlier in the array of criteria are given a higher weight.</span></span> <span data-ttu-id="0acf8-106">Mit **Sort** können Sie den idealen Adapter leichter in einer Adapter Liste finden.</span><span class="sxs-lookup"><span data-stu-id="0acf8-106">**Sort** helps you to more easily find your ideal adapter in an adapter list.</span></span>

## <a name="syntax"></a><span data-ttu-id="0acf8-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="0acf8-107">Syntax</span></span>

```cpp
HRESULT Sort(
  uint32_t numPreferences,
  _In_reads_(numPreferences) const DXCoreAdapterPreference* preferences
);
```

## <a name="parameters"></a><span data-ttu-id="0acf8-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="0acf8-108">Parameters</span></span>

### <a name="numpreferences"></a><span data-ttu-id="0acf8-109">numpreferences</span><span class="sxs-lookup"><span data-stu-id="0acf8-109">numPreferences</span></span>

<span data-ttu-id="0acf8-110">Typ: **uint32_t**</span><span class="sxs-lookup"><span data-stu-id="0acf8-110">Type: **uint32_t**</span></span>

<span data-ttu-id="0acf8-111">Die Anzahl der Elemente im Array, auf die durch den *Preferences* -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="0acf8-111">The number of elements that are in the array pointed to by the *preferences* parameter.</span></span>

### <a name="preferences-in"></a><span data-ttu-id="0acf8-112">Einstellungen [in]</span><span class="sxs-lookup"><span data-stu-id="0acf8-112">preferences [in]</span></span>

<span data-ttu-id="0acf8-113">Typ: Konstante **[dxcoreadapterpreference](./ne-dxcore_interface-dxcoreadapterpreference.md) \***</span><span class="sxs-lookup"><span data-stu-id="0acf8-113">Type: **const [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md)\***</span></span>

<span data-ttu-id="0acf8-114">Ein Zeiger auf ein konstantes Array von [dxcoreadapterpreference](./ne-dxcore_interface-dxcoreadapterpreference.md) -Werten, das Sortierkriterien darstellt.</span><span class="sxs-lookup"><span data-stu-id="0acf8-114">A pointer to a constant array of [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) values, representing sort criteria.</span></span>

## <a name="returns"></a><span data-ttu-id="0acf8-115">Gibt zurück</span><span class="sxs-lookup"><span data-stu-id="0acf8-115">Returns</span></span>

<span data-ttu-id="0acf8-116">Typ: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="0acf8-116">Type: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="0acf8-117">Wenn die Funktion erfolgreich ausgeführt wird, wird **S_OK** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0acf8-117">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="0acf8-118">Andernfalls wird ein [**HRESULT**](../../com/structure-of-com-error-codes.md) - [Fehlercode](../../com/com-error-codes-10.md)zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0acf8-118">Otherwise, it returns an [**HRESULT**](../../com/structure-of-com-error-codes.md) [error code](../../com/com-error-codes-10.md).</span></span>

|<span data-ttu-id="0acf8-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0acf8-119">Return value</span></span>|<span data-ttu-id="0acf8-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0acf8-120">Description</span></span>|
|-|-|
|<span data-ttu-id="0acf8-121">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="0acf8-121">E_INVALIDARG</span></span>|<span data-ttu-id="0acf8-122">Das *numpreferences* -Argument ist 0 (null), oder das *Preferences* -Argument ist `nullptr` .</span><span class="sxs-lookup"><span data-stu-id="0acf8-122">The *numPreferences* argument is zero, or the *preferences* argument is `nullptr`.</span></span>|

## <a name="remarks"></a><span data-ttu-id="0acf8-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0acf8-123">Remarks</span></span>

<span data-ttu-id="0acf8-124">In Fällen, in denen ein bereitgestellter [dxcoreadapterpreference](./ne-dxcore_interface-dxcoreadapterpreference.md) -Wert vom Betriebssystem (OS) nicht erkannt wird, wird er ignoriert und führt nicht zu einem Fehler bei der API.</span><span class="sxs-lookup"><span data-stu-id="0acf8-124">In cases where a provided [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) value isn't recognized by the operating system (OS), it is ignored, and won't cause the API to fail.</span></span> <span data-ttu-id="0acf8-125">Bekannte **dxcoreadapterpreference** -Werte werden in diesem Fall weiterhin berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="0acf8-125">Known **DXCoreAdapterPreference** values will still be considered in this case.</span></span> <span data-ttu-id="0acf8-126">Um zu ermitteln, ob ein Sortierungstyp von der API verstanden wird, nennen Sie [idxcoreadapterlist:: isadapterpreferencesupportiert](./nf-dxcore_interface-idxcoreadapterlist-isadapterpreferencesupported.md).</span><span class="sxs-lookup"><span data-stu-id="0acf8-126">To determine whether a sort type is understood by the API, call [IDXCoreAdapterList::IsAdapterPreferenceSupported](./nf-dxcore_interface-idxcoreadapterlist-isadapterpreferencesupported.md).</span></span>

<span data-ttu-id="0acf8-127">**Dxcoreadapterpreference** -Werte, die zuvor im angegebenen *Einstellungs* Array auftreten, werden mit höherer Priorität behandelt.</span><span class="sxs-lookup"><span data-stu-id="0acf8-127">**DXCoreAdapterPreference** values that occur earlier in the provided *preferences* array are treated with higher priority.</span></span> 

<span data-ttu-id="0acf8-128">Ausführliche Informationen dazu, welche Logik für die einzelnen Typen angewendet wird, finden Sie in der Dokumentation zur **dxcoreadapterpreference** -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="0acf8-128">Refer to the **DXCoreAdapterPreference** enumeration documentation for details about what logic is applied for each type.</span></span> <span data-ttu-id="0acf8-129">Die interne Logik für einen Typ kann sich entwickeln, wenn das Betriebssystem entwickelt wird.</span><span class="sxs-lookup"><span data-stu-id="0acf8-129">The internal logic for a type may develop as the OS develops.</span></span>

<span data-ttu-id="0acf8-130">Wenn " **Sort** " zurückgegeben wird, wurden Elemente in der DXCore-Adapter Liste nach den am wenigsten bevorzugten Elementen sortiert.</span><span class="sxs-lookup"><span data-stu-id="0acf8-130">When **Sort** returns, items in the DXCore adapter list will have been sorted from most preferable to least preferable.</span></span> <span data-ttu-id="0acf8-131">Wenn Sie daher [idxcoreadapterlist:: GetAdapter](./nf-dxcore_interface-idxcoreadapterlist-getadapter.md) mit dem Index 0 aufrufen, wird der Adapter abgerufen, der den angeforderten Sortier Einstellungs Typen am besten entspricht. Index 1 ist die nächste am besten geeignete Entsprechung usw.</span><span class="sxs-lookup"><span data-stu-id="0acf8-131">So, calling [IDXCoreAdapterList::GetAdapter](./nf-dxcore_interface-idxcoreadapterlist-getadapter.md) with index 0 retrieves the adapter that best matches the requested sort preference types; index 1 is the next best match, and so on.</span></span>

## <a name="see-also"></a><span data-ttu-id="0acf8-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0acf8-132">See also</span></span>

<span data-ttu-id="0acf8-133">[Idxcoreadapterlist](./nn-dxcore_interface-idxcoreadapterlist.md), [DXCore-Referenz](../dxcore-reference.md), [Verwenden von DXCore zum Auflisten von Adaptern](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="0acf8-133">[IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>