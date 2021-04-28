---
description: 'IPortableDevicePropVariantCollection::GetAt-Methode: Die GetAt-Methode ruft ein Element von einem nullbasierten Index aus der Auflistung ab.'
ms.assetid: c7119ba6-e6fc-4cb6-a8ab-3bf7b6bfe850
title: IPortableDevicePropVariantCollection::GetAt-Methode (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.GetAt
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: b901e8fcfa065813e4c0942632f80901800ef0a9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106798"
---
# <a name="iportabledevicepropvariantcollectiongetat-method"></a><span data-ttu-id="4c7ab-103">IPortableDevicePropVariantCollection::GetAt-Methode</span><span class="sxs-lookup"><span data-stu-id="4c7ab-103">IPortableDevicePropVariantCollection::GetAt method</span></span>

<span data-ttu-id="4c7ab-104">Die **GetAt-Methode** ruft ein Element von einem nullbasierten Index aus der Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="4c7ab-104">The **GetAt** method retrieves an item from the collection by a zero-based index.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c7ab-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4c7ab-105">Syntax</span></span>


```C++
HRESULT GetAt(
  [in]  const DWORD       dwIndex,
  [out]       PROPVARIANT *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="4c7ab-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4c7ab-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c7ab-107">*dwIndex* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="4c7ab-107">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c7ab-108">**DWORD,** das den nullbasierten Index des abzurufenden Elements enthält.</span><span class="sxs-lookup"><span data-stu-id="4c7ab-108">**DWORD** that contains the zero-based index of the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="4c7ab-109">*pValue* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="4c7ab-109">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4c7ab-110">Zeiger auf eine **PROPVARIANT-Struktur.**</span><span class="sxs-lookup"><span data-stu-id="4c7ab-110">Pointer to a **PROPVARIANT** structure.</span></span> <span data-ttu-id="4c7ab-111">Der Aufrufer ist dafür verantwortlich, diesen Arbeitsspeicher durch Aufrufen von **PropVariantClear frei zu geben.**</span><span class="sxs-lookup"><span data-stu-id="4c7ab-111">The caller is responsible for freeing this memory by calling **PropVariantClear**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c7ab-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4c7ab-112">Return value</span></span>

<span data-ttu-id="4c7ab-113">Die -Methode gibt ein **HRESULT zurück.**</span><span class="sxs-lookup"><span data-stu-id="4c7ab-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="4c7ab-114">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="4c7ab-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="4c7ab-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="4c7ab-115">Return code</span></span>                                                                                  | <span data-ttu-id="4c7ab-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4c7ab-116">Description</span></span>                                               |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <span data-ttu-id="4c7ab-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4c7ab-117"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="4c7ab-118">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4c7ab-118">The method succeeded.</span></span><br/>                          |
| <dl> <span data-ttu-id="4c7ab-119"><dt>**\_E-ZEIGER**</dt></span><span class="sxs-lookup"><span data-stu-id="4c7ab-119"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="4c7ab-120">Ein erforderliches Zeigerargument war **NULL.**</span><span class="sxs-lookup"><span data-stu-id="4c7ab-120">A required pointer argument was **NULL**.</span></span><br/>      |
| <dl> <span data-ttu-id="4c7ab-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="4c7ab-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="4c7ab-122">Der übergebene Index lag nicht im Bereich.</span><span class="sxs-lookup"><span data-stu-id="4c7ab-122">The index that was passed in was out of range.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="4c7ab-123">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4c7ab-123">Examples</span></span>

<span data-ttu-id="4c7ab-124">Ein Beispiel für die Verwendung dieser Methode finden Sie unter Abrufen der von einem Gerät [unterstützten funktionalen Kategorien.](retrieving-the-functional-categories-supported-by-a-device.md)</span><span class="sxs-lookup"><span data-stu-id="4c7ab-124">For an example of how to use this method see [Retrieving the Functional Categories Supported by a Device](retrieving-the-functional-categories-supported-by-a-device.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4c7ab-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4c7ab-125">Requirements</span></span>



| <span data-ttu-id="4c7ab-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4c7ab-126">Requirement</span></span> | <span data-ttu-id="4c7ab-127">Wert</span><span class="sxs-lookup"><span data-stu-id="4c7ab-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c7ab-128">Header</span><span class="sxs-lookup"><span data-stu-id="4c7ab-128">Header</span></span><br/>  | <dl> <span data-ttu-id="4c7ab-129"><dt>PortableDeviceTypes.h</dt></span><span class="sxs-lookup"><span data-stu-id="4c7ab-129"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="4c7ab-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4c7ab-130">Library</span></span><br/> | <dl> <span data-ttu-id="4c7ab-131"><dt>PortableDeviceGUIDs.lib</dt></span><span class="sxs-lookup"><span data-stu-id="4c7ab-131"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c7ab-132">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4c7ab-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c7ab-133">**IPortableDevicePropVariantCollection-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="4c7ab-133">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="4c7ab-134">Abrufen eines Objektbezeichners aus einem persistenten eindeutigen Bezeichner</span><span class="sxs-lookup"><span data-stu-id="4c7ab-134">Retrieving an Object Identifier from a Persistent Unique Identifier</span></span>](retrieving-an-object-identifier-from-a-persistent-unique-identifier.md)
</dt> <dt>

[<span data-ttu-id="4c7ab-135">Abrufen unterstützter Dienstereignisse</span><span class="sxs-lookup"><span data-stu-id="4c7ab-135">Retrieving Supported Service Events</span></span>](retrieving-supported-events.md)
</dt> <dt>

[<span data-ttu-id="4c7ab-136">Abrufen unterstützter Dienstformate</span><span class="sxs-lookup"><span data-stu-id="4c7ab-136">Retrieving Supported Service Formats</span></span>](retrieving-supported-formats.md)
</dt> <dt>

[<span data-ttu-id="4c7ab-137">Abrufen unterstützter Dienstmethoden</span><span class="sxs-lookup"><span data-stu-id="4c7ab-137">Retrieving Supported Service Methods</span></span>](retrieving-supported-methods.md)
</dt> <dt>

[<span data-ttu-id="4c7ab-138">Abrufen der von einem Gerät unterstützten Inhaltstypen</span><span class="sxs-lookup"><span data-stu-id="4c7ab-138">Retrieving the Content Types Supported by a Device</span></span>](retrieving-the-content-types-supported-by-a-device.md)
</dt> <dt>

[<span data-ttu-id="4c7ab-139">Abrufen der von einem Gerät unterstützten Funktionskategorien</span><span class="sxs-lookup"><span data-stu-id="4c7ab-139">Retrieving the Functional Categories Supported by a Device</span></span>](retrieving-the-functional-categories-supported-by-a-device.md)
</dt> <dt>

[<span data-ttu-id="4c7ab-140">Abrufen der funktionalen Objektbezeichner für ein Gerät</span><span class="sxs-lookup"><span data-stu-id="4c7ab-140">Retrieving the Functional Object Identifiers for a Device</span></span>](retrieving-the-functional-object-identifiers-for-a-device.md)
</dt> <dt>

[<span data-ttu-id="4c7ab-141">Abrufen der von einem Gerät unterstützten Renderingfunktionen</span><span class="sxs-lookup"><span data-stu-id="4c7ab-141">Retrieving the Rendering Capabilities Supported by a Device</span></span>](retrieving-the-rendering-capabilities-supported-by-a-device.md)
</dt> <dt>

[<span data-ttu-id="4c7ab-142">Festlegen von Eigenschaften für mehrere Objekte</span><span class="sxs-lookup"><span data-stu-id="4c7ab-142">Setting Properties for Multiple Objects</span></span>](setting-properties-for-multiple-objects.md)
</dt> </dl>

 

 




