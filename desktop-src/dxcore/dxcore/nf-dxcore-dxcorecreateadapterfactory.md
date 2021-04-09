---
title: DXCoreCreateAdapterFactory
description: Erstellt eine DXCore-AdapterFactory, die Sie verwenden können, um weitere DXCore-Objekte zu generieren.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 3f5164578da87af8f4d92c3bedcecb6f3dbaa95e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948994"
---
# <a name="dxcorecreateadapterfactory-function"></a><span data-ttu-id="a87cc-103">Dxcorecreateadapterfactory-Funktion</span><span class="sxs-lookup"><span data-stu-id="a87cc-103">DXCoreCreateAdapterFactory function</span></span>

## <a name="description"></a><span data-ttu-id="a87cc-104">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a87cc-104">Description</span></span>

<span data-ttu-id="a87cc-105">Erstellt eine DXCore-AdapterFactory, die Sie verwenden können, um weitere DXCore-Objekte zu generieren.</span><span class="sxs-lookup"><span data-stu-id="a87cc-105">Creates a DXCore adapter factory, which you can use to generate further DXCore objects.</span></span> <span data-ttu-id="a87cc-106">Programmieranleitungen und Codebeispiele finden [Sie unter Verwenden von DXCore zum Aufzählen von Adaptern](../dxcore-enum-adapters.md).</span><span class="sxs-lookup"><span data-stu-id="a87cc-106">For programming guidance, and code examples, see [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md).</span></span>

## <a name="parameters"></a><span data-ttu-id="a87cc-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="a87cc-107">Parameters</span></span>

### <a name="riid"></a><span data-ttu-id="a87cc-108">riid</span><span class="sxs-lookup"><span data-stu-id="a87cc-108">riid</span></span>

<span data-ttu-id="a87cc-109">Typ: **refID**</span><span class="sxs-lookup"><span data-stu-id="a87cc-109">Type: **REFIID**</span></span>

<span data-ttu-id="a87cc-110">Ein Verweis auf die Globally Unique Identifier (GUID) der Schnittstelle, die in *ppvfactory* zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="a87cc-110">A reference to the globally unique identifier (GUID) of the interface that you wish to be returned in *ppvFactory*.</span></span> <span data-ttu-id="a87cc-111">Dies wird als Schnittstellen Bezeichner (IID) von [idxcoreadapterfactory](../dxcore_interface/nn-dxcore_interface-idxcoreadapterfactory.md)erwartet.</span><span class="sxs-lookup"><span data-stu-id="a87cc-111">This is expected to be the interface identifier (IID) of [IDXCoreAdapterFactory](../dxcore_interface/nn-dxcore_interface-idxcoreadapterfactory.md).</span></span>

### <a name="ppvfactory-out"></a><span data-ttu-id="a87cc-112">ppvfactory [out]</span><span class="sxs-lookup"><span data-stu-id="a87cc-112">ppvFactory [out]</span></span>

<span data-ttu-id="a87cc-113">Typ: **void \* \***</span><span class="sxs-lookup"><span data-stu-id="a87cc-113">Type: **void\*\***</span></span>

<span data-ttu-id="a87cc-114">Die Adresse eines Zeigers auf eine Schnittstelle mit der im *riid* -Parameter angegebenen IID.</span><span class="sxs-lookup"><span data-stu-id="a87cc-114">The address of a pointer to an interface with the IID specified in the *riid* parameter.</span></span> <span data-ttu-id="a87cc-115">Bei erfolgreicher Rückgabe enthält *\* ppvfactory* (die Dereferenzierte Adresse) einen Zeiger auf die erstellte DXCore-Factory.</span><span class="sxs-lookup"><span data-stu-id="a87cc-115">Upon successful return, *\*ppvFactory* (the dereferenced address) contains a pointer to the DXCore factory created.</span></span>

## <a name="returns"></a><span data-ttu-id="a87cc-116">Gibt zurück</span><span class="sxs-lookup"><span data-stu-id="a87cc-116">Returns</span></span>

<span data-ttu-id="a87cc-117">Typ: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="a87cc-117">Type: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="a87cc-118">Wenn die Funktion erfolgreich ausgeführt wird, wird **S_OK** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a87cc-118">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="a87cc-119">Andernfalls wird ein [**HRESULT**](../../com/structure-of-com-error-codes.md) - [Fehlercode](../../com/com-error-codes-10.md)zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a87cc-119">Otherwise, it returns an [**HRESULT**](../../com/structure-of-com-error-codes.md) [error code](../../com/com-error-codes-10.md).</span></span>

|<span data-ttu-id="a87cc-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a87cc-120">Return value</span></span>|<span data-ttu-id="a87cc-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a87cc-121">Description</span></span>|
|-|-|
|<span data-ttu-id="a87cc-122">E_NOINTERFACE</span><span class="sxs-lookup"><span data-stu-id="a87cc-122">E_NOINTERFACE</span></span>|<span data-ttu-id="a87cc-123">Für *riid* wurde ein ungültiger Wert angegeben.</span><span class="sxs-lookup"><span data-stu-id="a87cc-123">An invalid value was provided for *riid*.</span></span>|
|<span data-ttu-id="a87cc-124">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="a87cc-124">E_POINTER</span></span>|<span data-ttu-id="a87cc-125">`nullptr` wurde für *ppvfactory* bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="a87cc-125">`nullptr` was provided for *ppvFactory*.</span></span>|

## <a name="remarks"></a><span data-ttu-id="a87cc-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a87cc-126">Remarks</span></span>

<span data-ttu-id="a87cc-127">Für den Zeitraum, in dem ein Verweis auf einer [idxcoreadapterfactory](../dxcore_interface/nn-dxcore_interface-idxcoreadapterfactory.md) -Schnittstelle vorhanden ist, eine [idxcoreadapterlist](../dxcore_interface/nn-dxcore_interface-idxcoreadapterlist.md) -Schnittstelle oder eine [idxcoreadapter](../dxcore_interface/nn-dxcore_interface-idxcoreadapter.md) -Schnittstelle, zusätzliche Aufrufe von **dxcorecreateadapterfactory**, [idxcoreadapterlist:: GetFactory](../dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-getfactory.md)oder [idxcoreadapter:: GetFactory](../dxcore_interface/nf-dxcore_interface-idxcoreadapter-getfactory.md) geben Zeiger auf dasselbe Objekt zurück und erhöhen den Verweis Zähler der **idxcoreadapterfactory** -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="a87cc-127">For the duration of time that a reference exists on an [IDXCoreAdapterFactory](../dxcore_interface/nn-dxcore_interface-idxcoreadapterfactory.md) interface, an [IDXCoreAdapterList](../dxcore_interface/nn-dxcore_interface-idxcoreadapterlist.md) interface, or an [IDXCoreAdapter](../dxcore_interface/nn-dxcore_interface-idxcoreadapter.md) interface, additional calls to **DXCoreCreateAdapterFactory**, [IDXCoreAdapterList::GetFactory](../dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-getfactory.md), or [IDXCoreAdapter::GetFactory](../dxcore_interface/nf-dxcore_interface-idxcoreadapter-getfactory.md) will return pointers to the same object, increasing the reference count of the **IDXCoreAdapterFactory** interface.</span></span>

## <a name="see-also"></a><span data-ttu-id="a87cc-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a87cc-128">See also</span></span>

<span data-ttu-id="a87cc-129">[DXCore-Referenz](../dxcore-reference.md), [Verwenden von DXCore zum Auflisten von Adaptern](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="a87cc-129">[DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>