---
title: IDXCoreAdapter::GetProperty
description: Ruft den Wert der angegebenen Adapter Eigenschaft ab.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: c8a7f7b36fdb0128b4047335051823da07a074c7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316262"
---
# <a name="idxcoreadaptergetproperty-method"></a><span data-ttu-id="95d2e-103">Idxcoreadapter:: GetProperty-Methode</span><span class="sxs-lookup"><span data-stu-id="95d2e-103">IDXCoreAdapter::GetProperty method</span></span>

<span data-ttu-id="95d2e-104">Ruft den Wert der angegebenen Adapter Eigenschaft ab.</span><span class="sxs-lookup"><span data-stu-id="95d2e-104">Retrieves the value of the specified adapter property.</span></span> <span data-ttu-id="95d2e-105">Bevor Sie **GetProperty** für einen Eigenschaftentyp aufrufen, rufen Sie [ispropertysupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) auf, um zu bestätigen, dass der Eigenschaftentyp für diesen Adapter und dieses Betriebssystem (OS) verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="95d2e-105">Before calling **GetProperty** for a property type, call [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) to confirm that the property type is available for this adapter and operating system (OS).</span></span> <span data-ttu-id="95d2e-106">Rufen Sie auch vor dem Aufrufen von **GetProperty** [getpropertysize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) auf, um die erforderliche Größe des Puffers zu bestimmen, in dem der Eigenschafts Wert empfangen werden soll.</span><span class="sxs-lookup"><span data-stu-id="95d2e-106">Also before calling **GetProperty**, call [GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) to determine the necessary size of the buffer in which to receive the property value.</span></span>

## <a name="syntax"></a><span data-ttu-id="95d2e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="95d2e-107">Syntax</span></span>

```cpp
virtual HRESULT STDMETHODCALLTYPE GetProperty(
  DXCoreAdapterProperty property,
  size_t bufferSize,
  _Out_writes_bytes_(bufferSize) void *propertyData) = 0;

template <class T>
HRESULT GetProperty( 
  DXCoreAdapterProperty property,
  _Out_writes_bytes_(sizeof(T)) T *propertyData);
```

## <a name="parameters"></a><span data-ttu-id="95d2e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="95d2e-108">Parameters</span></span>

### <a name="property"></a><span data-ttu-id="95d2e-109">property</span><span class="sxs-lookup"><span data-stu-id="95d2e-109">property</span></span>

<span data-ttu-id="95d2e-110">Type: **[dxcoreadapterproperty](./ne-dxcore_interface-dxcoreadapterproperty.md)**</span><span class="sxs-lookup"><span data-stu-id="95d2e-110">Type: **[DXCoreAdapterProperty](./ne-dxcore_interface-dxcoreadapterproperty.md)**</span></span>

<span data-ttu-id="95d2e-111">Der Typ der Eigenschaft, deren Wert abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="95d2e-111">The type of the property whose value you wish to retrieve.</span></span> <span data-ttu-id="95d2e-112">Weitere Informationen zu den einzelnen Adapter Eigenschaften finden Sie in der Tabelle unter [dxcoreadapterproperty](./ne-dxcore_interface-dxcoreadapterproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="95d2e-112">See the table in [DXCoreAdapterProperty](./ne-dxcore_interface-dxcoreadapterproperty.md) for more info about each adapter property.</span></span>

### <a name="buffersize"></a><span data-ttu-id="95d2e-113">bufferSize</span><span class="sxs-lookup"><span data-stu-id="95d2e-113">bufferSize</span></span>

<span data-ttu-id="95d2e-114">Typ: **size_t**</span><span class="sxs-lookup"><span data-stu-id="95d2e-114">Type: **size_t**</span></span>

<span data-ttu-id="95d2e-115">Die Größe (in Bytes) des Ausgabepuffers, den Sie zuordnen und in *PropertyData* bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="95d2e-115">The size, in bytes, of the output buffer that you allocate and provide in *propertyData*.</span></span>

### <a name="propertydata-out"></a><span data-ttu-id="95d2e-116">PropertyData [out]</span><span class="sxs-lookup"><span data-stu-id="95d2e-116">propertyData [out]</span></span>

<span data-ttu-id="95d2e-117">Typ: **void \***</span><span class="sxs-lookup"><span data-stu-id="95d2e-117">Type: **void\***</span></span>

<span data-ttu-id="95d2e-118">Ein Zeiger auf einen Ausgabepuffer, den Sie in der Anwendung zuordnen, und der die Funktion ausfüllt.</span><span class="sxs-lookup"><span data-stu-id="95d2e-118">A pointer to an output buffer that you allocate in your application, and that the function fills in.</span></span> <span data-ttu-id="95d2e-119">Ruft [getpropertysize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) auf, um die Größe zu ermitteln, die der *PropertyData* -Puffer für eine bestimmte Adapter Eigenschaft aufweisen soll.</span><span class="sxs-lookup"><span data-stu-id="95d2e-119">Call [GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) to determine the size that the *propertyData* buffer should be for a given adapter property.</span></span>

## <a name="returns"></a><span data-ttu-id="95d2e-120">Gibt zurück</span><span class="sxs-lookup"><span data-stu-id="95d2e-120">Returns</span></span>

<span data-ttu-id="95d2e-121">Typ: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="95d2e-121">Type: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="95d2e-122">Wenn die Funktion erfolgreich ausgeführt wird, wird **S_OK** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="95d2e-122">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="95d2e-123">Andernfalls wird ein [**HRESULT**](../../com/structure-of-com-error-codes.md) - [Fehlercode](../../com/com-error-codes-10.md)zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="95d2e-123">Otherwise, it returns an [**HRESULT**](../../com/structure-of-com-error-codes.md) [error code](../../com/com-error-codes-10.md).</span></span>

|<span data-ttu-id="95d2e-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="95d2e-124">Return value</span></span>|<span data-ttu-id="95d2e-125">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="95d2e-125">Description</span></span>|
|-|-|
|<span data-ttu-id="95d2e-126">DXGI_ERROR_INVALID_CALL</span><span class="sxs-lookup"><span data-stu-id="95d2e-126">DXGI_ERROR_INVALID_CALL</span></span>|<span data-ttu-id="95d2e-127">Der in der- *Eigenschaft* angegebene Eigenschaftentyp wird von diesem Betriebssystem (OS) nicht erkannt.</span><span class="sxs-lookup"><span data-stu-id="95d2e-127">The property type specified in *property* is not recognized by this operating system (OS).</span></span> <span data-ttu-id="95d2e-128">Wenden Sie [ispropertysupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) an, um zu bestätigen, dass der Eigenschaftentyp für diesen Adapter und dieses Betriebssystem verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="95d2e-128">Call [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) to confirm that the property type is available for this adapter and operating system (OS).</span></span>|
|<span data-ttu-id="95d2e-129">DXGI_ERROR_UNSUPPORTED</span><span class="sxs-lookup"><span data-stu-id="95d2e-129">DXGI_ERROR_UNSUPPORTED</span></span>|<span data-ttu-id="95d2e-130">Der in der- *Eigenschaft* angegebene Eigenschaftentyp wird vom Adapter nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="95d2e-130">The property type specified in *property* is not supported by the adapter.</span></span> <span data-ttu-id="95d2e-131">Wenden Sie [ispropertysupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) an, um zu bestätigen, dass der Eigenschaftentyp für diesen Adapter und dieses Betriebssystem verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="95d2e-131">Call [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) to confirm that the property type is available for this adapter and operating system (OS).</span></span>|
|<span data-ttu-id="95d2e-132">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="95d2e-132">E_INVALIDARG</span></span>|<span data-ttu-id="95d2e-133">In *PropertyData* ist eine unzureichende Puffergröße angegeben.</span><span class="sxs-lookup"><span data-stu-id="95d2e-133">An insufficient buffer size is provided in *propertyData*.</span></span> <span data-ttu-id="95d2e-134">Ruft [getpropertysize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) auf, um die Größe zu ermitteln, die der *PropertyData* -Puffer für eine bestimmte Adapter Eigenschaft aufweisen soll.</span><span class="sxs-lookup"><span data-stu-id="95d2e-134">Call [GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) to determine the size that the *propertyData* buffer should be for a given adapter property.</span></span>|
|<span data-ttu-id="95d2e-135">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="95d2e-135">E_POINTER</span></span>|<span data-ttu-id="95d2e-136">`nullptr` wurde für *PropertyData* bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="95d2e-136">`nullptr` was provided for *propertyData*.</span></span>|

## <a name="remarks"></a><span data-ttu-id="95d2e-137">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="95d2e-137">Remarks</span></span>

<span data-ttu-id="95d2e-138">Sie können **GetProperty** für einen Adapter aufrufen, der nicht mehr gültig ist, &mdash; da die Funktion nicht mehr gültig ist.</span><span class="sxs-lookup"><span data-stu-id="95d2e-138">You can call **GetProperty** on an adapter that's no longer valid&mdash;the function won't fail as a result of that.</span></span> <span data-ttu-id="95d2e-139">Diese Funktion gibt den *PropertyData* -Puffer aus, bevor Sie aufgefüllt wird.</span><span class="sxs-lookup"><span data-stu-id="95d2e-139">This function zeros out the *propertyData* buffer prior to filling it in.</span></span>

## <a name="see-also"></a><span data-ttu-id="95d2e-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="95d2e-140">See also</span></span>

<span data-ttu-id="95d2e-141">[Idxcoreadapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore-Referenz](../dxcore-reference.md), [Verwenden von DXCore zum Auflisten von Adaptern](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="95d2e-141">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>