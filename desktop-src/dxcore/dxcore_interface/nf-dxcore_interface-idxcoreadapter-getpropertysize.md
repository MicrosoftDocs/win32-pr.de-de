---
title: IDXCoreAdapter::GetPropertySize
description: Ruft für eine angegebene Adapter Eigenschaft die Größe des Puffers in Bytes ab, der für den Abruf von [GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md)erforderlich ist.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: ff077d3c4c827a55f7fd9b10dfe93f1271649f72
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106340916"
---
# <a name="idxcoreadaptergetpropertysize-method"></a><span data-ttu-id="475fc-103">Idxcoreadapter:: getpropertysize-Methode</span><span class="sxs-lookup"><span data-stu-id="475fc-103">IDXCoreAdapter::GetPropertySize method</span></span>

<span data-ttu-id="475fc-104">Ruft für eine angegebene Adapter Eigenschaft die Größe des Puffers in Bytes ab, der für den Abruf von [GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md)erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="475fc-104">For a specified adapter property, retrieves the size of buffer, in bytes, that is required for a call to [GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md).</span></span> <span data-ttu-id="475fc-105">Bevor Sie **getpropertysize** für einen Eigenschaftentyp aufrufen, rufen Sie [ispropertysupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) auf, um zu bestätigen, dass der Eigenschaftentyp für diesen Adapter und dieses Betriebssystem verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="475fc-105">Before calling **GetPropertySize** for a property type, call [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) to confirm that the property type is available for this adapter and operating system (OS).</span></span>

## <a name="syntax"></a><span data-ttu-id="475fc-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="475fc-106">Syntax</span></span>

```cpp
virtual HRESULT STDMETHODCALLTYPE GetPropertySize(
  DXCoreAdapterProperty property,
  _Out_ size_t *bufferSize) = 0;
```

## <a name="parameters"></a><span data-ttu-id="475fc-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="475fc-107">Parameters</span></span>

### <a name="property"></a><span data-ttu-id="475fc-108">property</span><span class="sxs-lookup"><span data-stu-id="475fc-108">property</span></span>

<span data-ttu-id="475fc-109">Type: **[dxcoreadapterproperty](./ne-dxcore_interface-dxcoreadapterproperty.md)**</span><span class="sxs-lookup"><span data-stu-id="475fc-109">Type: **[DXCoreAdapterProperty](./ne-dxcore_interface-dxcoreadapterproperty.md)**</span></span>

<span data-ttu-id="475fc-110">Der Typ der Eigenschaft, deren Größe (in Bytes) abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="475fc-110">The type of the property whose size, in bytes, you wish to retrieve.</span></span>

### <a name="buffersize-out"></a><span data-ttu-id="475fc-111">bufferSize [out]</span><span class="sxs-lookup"><span data-stu-id="475fc-111">bufferSize [out]</span></span>

<span data-ttu-id="475fc-112">Typ: **size_t \***</span><span class="sxs-lookup"><span data-stu-id="475fc-112">Type: **size_t\***</span></span>

<span data-ttu-id="475fc-113">Ein Zeiger auf einen **size_t** Wert.</span><span class="sxs-lookup"><span data-stu-id="475fc-113">A pointer to a **size_t** value.</span></span> <span data-ttu-id="475fc-114">Die Funktion dereferenziert den Zeiger und legt den Wert auf die Größe (in Bytes) des Ausgabepuffers fest, den Sie zuordnen und als *PropertyData* -Argument in Ihrem Aufrufen von [GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md)übergeben.</span><span class="sxs-lookup"><span data-stu-id="475fc-114">The function dereferences the pointer and sets the value to the size, in bytes, of the output buffer that you should allocate and pass as the *propertyData* argument in your call to [GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md).</span></span>

## <a name="returns"></a><span data-ttu-id="475fc-115">Gibt zurück</span><span class="sxs-lookup"><span data-stu-id="475fc-115">Returns</span></span>

<span data-ttu-id="475fc-116">Typ: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="475fc-116">Type: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="475fc-117">Wenn die Funktion erfolgreich ausgeführt wird, wird **S_OK** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="475fc-117">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="475fc-118">Andernfalls wird ein [**HRESULT**](../../com/structure-of-com-error-codes.md) - [Fehlercode](../../com/com-error-codes-10.md)zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="475fc-118">Otherwise, it returns an [**HRESULT**](../../com/structure-of-com-error-codes.md) [error code](../../com/com-error-codes-10.md).</span></span>

|<span data-ttu-id="475fc-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="475fc-119">Return value</span></span>|<span data-ttu-id="475fc-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="475fc-120">Description</span></span>|
|-|-|
|<span data-ttu-id="475fc-121">DXGI_ERROR_INVALID_CALL</span><span class="sxs-lookup"><span data-stu-id="475fc-121">DXGI_ERROR_INVALID_CALL</span></span>|<span data-ttu-id="475fc-122">Der in der- *Eigenschaft* angegebene Eigenschaftentyp wird von diesem Betriebssystem (OS) nicht erkannt.</span><span class="sxs-lookup"><span data-stu-id="475fc-122">The property type specified in *property* is not recognized by this operating system (OS).</span></span> <span data-ttu-id="475fc-123">Wenden Sie [ispropertysupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) an, um zu bestätigen, dass der Eigenschaftentyp für diesen Adapter und dieses Betriebssystem verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="475fc-123">Call [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) to confirm that the property type is available for this adapter and operating system (OS).</span></span>|
|<span data-ttu-id="475fc-124">DXGI_ERROR_UNSUPPORTED</span><span class="sxs-lookup"><span data-stu-id="475fc-124">DXGI_ERROR_UNSUPPORTED</span></span>|<span data-ttu-id="475fc-125">Der in der- *Eigenschaft* angegebene Eigenschaftentyp wird vom Adapter nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="475fc-125">The property type specified in *property* is not supported by the adapter.</span></span> <span data-ttu-id="475fc-126">Wenden Sie [ispropertysupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) an, um zu bestätigen, dass der Eigenschaftentyp für diesen Adapter und dieses Betriebssystem verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="475fc-126">Call [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) to confirm that the property type is available for this adapter and operating system (OS).</span></span>|
|<span data-ttu-id="475fc-127">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="475fc-127">E_POINTER</span></span>|<span data-ttu-id="475fc-128">`nullptr` wurde für *bufferSize* bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="475fc-128">`nullptr` was provided for *bufferSize*.</span></span>|

## <a name="remarks"></a><span data-ttu-id="475fc-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="475fc-129">Remarks</span></span>

<span data-ttu-id="475fc-130">Sie können **getpropertysize** für einen Adapter aufrufen, der nicht mehr gültig ist, da &mdash; die Funktion nicht fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="475fc-130">You can call **GetPropertySize** on an adapter that's no longer valid&mdash;the function won't fail.</span></span>

## <a name="see-also"></a><span data-ttu-id="475fc-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="475fc-131">See also</span></span>

<span data-ttu-id="475fc-132">[Idxcoreadapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore-Referenz](../dxcore-reference.md), [Verwenden von DXCore zum Auflisten von Adaptern](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="475fc-132">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>