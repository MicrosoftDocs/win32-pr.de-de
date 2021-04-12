---
title: IDXCoreAdapter::GetFactory
description: 'Ruft einen [idxcoreadapterfactory](./nn-dxcore_interface-idxcoreadapterfactory.md) -Schnittstellen Zeiger auf das DXCore-adapterfactoryobjekt ab. | Idxcoreadapter:: GetFactory'
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 1ac3e7fccd39b9b03ecb7016494a610519d26afa
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104219272"
---
# <a name="idxcoreadaptergetfactory-method"></a><span data-ttu-id="81080-104">Idxcoreadapter:: GetFactory-Methode</span><span class="sxs-lookup"><span data-stu-id="81080-104">IDXCoreAdapter::GetFactory method</span></span>

<span data-ttu-id="81080-105">Ruft einen [idxcoreadapterfactory](./nn-dxcore_interface-idxcoreadapterfactory.md) -Schnittstellen Zeiger auf das DXCore-adapterfactoryobjekt ab.</span><span class="sxs-lookup"><span data-stu-id="81080-105">Retrieves an [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md) interface pointer to the DXCore adapter factory object.</span></span> <span data-ttu-id="81080-106">Programmieranleitungen und Codebeispiele finden [Sie unter Verwenden von DXCore zum Aufzählen von Adaptern](../dxcore-enum-adapters.md).</span><span class="sxs-lookup"><span data-stu-id="81080-106">For programming guidance, and code examples, see [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="81080-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="81080-107">Syntax</span></span>

```cpp
virtual HRESULT STDMETHODCALLTYPE GetFactory(
  REFIID riid,
  _COM_Outptr_ void** ppvFactory
) = 0;

template <class T>
HRESULT GetFactory(_COM_Outptr_ T** ppvFactory);
```

## <a name="parameters"></a><span data-ttu-id="81080-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="81080-108">Parameters</span></span>

### <a name="riid"></a><span data-ttu-id="81080-109">riid</span><span class="sxs-lookup"><span data-stu-id="81080-109">riid</span></span>

<span data-ttu-id="81080-110">Typ: **refID**</span><span class="sxs-lookup"><span data-stu-id="81080-110">Type: **REFIID**</span></span>

<span data-ttu-id="81080-111">Ein Verweis auf die Globally Unique Identifier (GUID) der Schnittstelle, die in *ppvfactory* zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="81080-111">A reference to the globally unique identifier (GUID) of the interface that you wish to be returned in *ppvFactory*.</span></span> <span data-ttu-id="81080-112">Dies wird als Schnittstellen Bezeichner (IID) von [idxcoreadapterfactory](./nn-dxcore_interface-idxcoreadapterfactory.md)erwartet.</span><span class="sxs-lookup"><span data-stu-id="81080-112">This is expected to be the interface identifier (IID) of [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md).</span></span>

### <a name="ppvfactory-out"></a><span data-ttu-id="81080-113">ppvfactory [out]</span><span class="sxs-lookup"><span data-stu-id="81080-113">ppvFactory [out]</span></span>

<span data-ttu-id="81080-114">Typ: **void \* \***</span><span class="sxs-lookup"><span data-stu-id="81080-114">Type: **void\*\***</span></span>

<span data-ttu-id="81080-115">Die Adresse eines Zeigers auf eine Schnittstelle mit der im *riid* -Parameter angegebenen IID.</span><span class="sxs-lookup"><span data-stu-id="81080-115">The address of a pointer to an interface with the IID specified in the *riid* parameter.</span></span> <span data-ttu-id="81080-116">Bei erfolgreicher Rückgabe enthält *\* ppvfactory* (die Dereferenzierte Adresse) einen Zeiger auf das vorhandene DXCore-adapterfactoryobjekt.</span><span class="sxs-lookup"><span data-stu-id="81080-116">Upon successful return, *\*ppvFactory* (the dereferenced address) contains a pointer to the existing DXCore adapter factory object.</span></span> <span data-ttu-id="81080-117">Vor der Rückgabe erhöht die Funktion den Verweis Zähler für die [idxcoreadapterfactory](./nn-dxcore_interface-idxcoreadapterfactory.md) -Schnittstelle des Factory-Objekts.</span><span class="sxs-lookup"><span data-stu-id="81080-117">Before returning, the function increments the reference count on the factory object's [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md) interface.</span></span>

## <a name="returns"></a><span data-ttu-id="81080-118">Gibt zurück</span><span class="sxs-lookup"><span data-stu-id="81080-118">Returns</span></span>

<span data-ttu-id="81080-119">Typ: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="81080-119">Type: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="81080-120">Wenn die Funktion erfolgreich ausgeführt wird, wird **S_OK** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="81080-120">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="81080-121">Andernfalls wird ein [**HRESULT**](../../com/structure-of-com-error-codes.md) - [Fehlercode](../../com/com-error-codes-10.md)zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="81080-121">Otherwise, it returns an [**HRESULT**](../../com/structure-of-com-error-codes.md) [error code](../../com/com-error-codes-10.md).</span></span>

|<span data-ttu-id="81080-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="81080-122">Return value</span></span>|<span data-ttu-id="81080-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="81080-123">Description</span></span>|
|-|-|
|<span data-ttu-id="81080-124">E_NOINTERFACE</span><span class="sxs-lookup"><span data-stu-id="81080-124">E_NOINTERFACE</span></span>|<span data-ttu-id="81080-125">Für *riid* wurde ein ungültiger Wert angegeben.</span><span class="sxs-lookup"><span data-stu-id="81080-125">An invalid value was provided for *riid*.</span></span>|
|<span data-ttu-id="81080-126">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="81080-126">E_POINTER</span></span>|<span data-ttu-id="81080-127">`nullptr` wurde für *ppvfactory* bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="81080-127">`nullptr` was provided for *ppvFactory*.</span></span>|

## <a name="remarks"></a><span data-ttu-id="81080-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="81080-128">Remarks</span></span>

<span data-ttu-id="81080-129">Für den Zeitraum, in dem ein Verweis auf einer [idxcoreadapterfactory](./nn-dxcore_interface-idxcoreadapterfactory.md) -Schnittstelle vorhanden ist, eine [idxcoreadapterlist](./nn-dxcore_interface-idxcoreadapterlist.md) -Schnittstelle oder eine [idxcoreadapter](./nn-dxcore_interface-idxcoreadapter.md) -Schnittstelle, zusätzliche Aufrufe von [dxcorecreateadapterfactory](../dxcore/nf-dxcore-dxcorecreateadapterfactory.md), [idxcoreadapterlist:: GetFactory](./nf-dxcore_interface-idxcoreadapterlist-getfactory.md)oder [idxcoreadapter:: GetFactory]() geben Zeiger auf dasselbe Objekt zurück und erhöhen den Verweis Zähler der **idxcoreadapterfactory** -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="81080-129">For the duration of time that a reference exists on an [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md) interface, an [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md) interface, or an [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md) interface, additional calls to [DXCoreCreateAdapterFactory](../dxcore/nf-dxcore-dxcorecreateadapterfactory.md), [IDXCoreAdapterList::GetFactory](./nf-dxcore_interface-idxcoreadapterlist-getfactory.md), or [IDXCoreAdapter::GetFactory]() will return pointers to the same object, increasing the reference count of the **IDXCoreAdapterFactory** interface.</span></span>

## <a name="see-also"></a><span data-ttu-id="81080-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="81080-130">See also</span></span>

<span data-ttu-id="81080-131">[Idxcoreadapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore-Referenz](../dxcore-reference.md), [Verwenden von DXCore zum Auflisten von Adaptern](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="81080-131">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>
