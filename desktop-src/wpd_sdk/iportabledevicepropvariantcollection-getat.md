---
description: Die GetAt-Methode ruft ein Element durch einen NULL basierten Index aus der Auflistung ab.
ms.assetid: c7119ba6-e6fc-4cb6-a8ab-3bf7b6bfe850
title: 'Iportabledevicepropvariantcollection:: GetAt-Methode (portabledevicetypes. h)'
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
ms.openlocfilehash: 0833c69b537fa230320ef69707a6f4302a8ca1ec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365977"
---
# <a name="iportabledevicepropvariantcollectiongetat-method"></a><span data-ttu-id="7466b-103">Iportabledevicepropvariantcollection:: GetAt-Methode</span><span class="sxs-lookup"><span data-stu-id="7466b-103">IPortableDevicePropVariantCollection::GetAt method</span></span>

<span data-ttu-id="7466b-104">Die **GetAt** -Methode ruft ein Element durch einen NULL basierten Index aus der Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="7466b-104">The **GetAt** method retrieves an item from the collection by a zero-based index.</span></span>

## <a name="syntax"></a><span data-ttu-id="7466b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7466b-105">Syntax</span></span>


```C++
HRESULT GetAt(
  [in]  const DWORD       dwIndex,
  [out]       PROPVARIANT *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="7466b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7466b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7466b-107">*dwIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7466b-107">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7466b-108">**DWORD** , das den NULL basierten Index des abzurufenden Elements enthält.</span><span class="sxs-lookup"><span data-stu-id="7466b-108">**DWORD** that contains the zero-based index of the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="7466b-109">*pValue* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="7466b-109">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7466b-110">Zeiger auf eine **PROPVARIANT** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="7466b-110">Pointer to a **PROPVARIANT** structure.</span></span> <span data-ttu-id="7466b-111">Der Aufrufer ist dafür verantwortlich, diesen Speicher durch Aufrufen von **propvariantclear frei** zugeben.</span><span class="sxs-lookup"><span data-stu-id="7466b-111">The caller is responsible for freeing this memory by calling **PropVariantClear**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7466b-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7466b-112">Return value</span></span>

<span data-ttu-id="7466b-113">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="7466b-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="7466b-114">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="7466b-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="7466b-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="7466b-115">Return code</span></span>                                                                                  | <span data-ttu-id="7466b-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7466b-116">Description</span></span>                                               |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <span data-ttu-id="7466b-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7466b-117"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="7466b-118">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7466b-118">The method succeeded.</span></span><br/>                          |
| <dl> <span data-ttu-id="7466b-119"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="7466b-119"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="7466b-120">Ein erforderliches Zeigerargument war **null**.</span><span class="sxs-lookup"><span data-stu-id="7466b-120">A required pointer argument was **NULL**.</span></span><br/>      |
| <dl> <span data-ttu-id="7466b-121"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="7466b-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="7466b-122">Der von ihm über gegebene Index lag außerhalb des zulässigen Bereichs.</span><span class="sxs-lookup"><span data-stu-id="7466b-122">The index that was passed in was out of range.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="7466b-123">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7466b-123">Examples</span></span>

<span data-ttu-id="7466b-124">Ein Beispiel für die Verwendung dieser Methode finden Sie [unter Abrufen der von einem Gerät unterstützten funktionalen Kategorien](retrieving-the-functional-categories-supported-by-a-device.md).</span><span class="sxs-lookup"><span data-stu-id="7466b-124">For an example of how to use this method see [Retrieving the Functional Categories Supported by a Device](retrieving-the-functional-categories-supported-by-a-device.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7466b-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7466b-125">Requirements</span></span>



| <span data-ttu-id="7466b-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7466b-126">Requirement</span></span> | <span data-ttu-id="7466b-127">Wert</span><span class="sxs-lookup"><span data-stu-id="7466b-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7466b-128">Header</span><span class="sxs-lookup"><span data-stu-id="7466b-128">Header</span></span><br/>  | <dl> <span data-ttu-id="7466b-129"><dt>Portablede vicetypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="7466b-129"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="7466b-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7466b-130">Library</span></span><br/> | <dl> <span data-ttu-id="7466b-131"><dt>Portabledeviceguids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7466b-131"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7466b-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7466b-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7466b-133">**Iportabledevicepropvariantcollection-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="7466b-133">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="7466b-134">Abrufen eines Objekt Bezeichners aus einem persistenten eindeutigen Bezeichner</span><span class="sxs-lookup"><span data-stu-id="7466b-134">Retrieving an Object Identifier from a Persistent Unique Identifier</span></span>](retrieving-an-object-identifier-from-a-persistent-unique-identifier.md)
</dt> <dt>

[<span data-ttu-id="7466b-135">Abrufen unterstützter Dienst Ereignisse</span><span class="sxs-lookup"><span data-stu-id="7466b-135">Retrieving Supported Service Events</span></span>](retrieving-supported-events.md)
</dt> <dt>

[<span data-ttu-id="7466b-136">Abrufen unterstützter Dienst Formate</span><span class="sxs-lookup"><span data-stu-id="7466b-136">Retrieving Supported Service Formats</span></span>](retrieving-supported-formats.md)
</dt> <dt>

[<span data-ttu-id="7466b-137">Abrufen unterstützter Dienst Methoden</span><span class="sxs-lookup"><span data-stu-id="7466b-137">Retrieving Supported Service Methods</span></span>](retrieving-supported-methods.md)
</dt> <dt>

[<span data-ttu-id="7466b-138">Abrufen der von einem Gerät unterstützten Inhaltstypen</span><span class="sxs-lookup"><span data-stu-id="7466b-138">Retrieving the Content Types Supported by a Device</span></span>](retrieving-the-content-types-supported-by-a-device.md)
</dt> <dt>

[<span data-ttu-id="7466b-139">Abrufen der von einem Gerät unterstützten funktionalen Kategorien</span><span class="sxs-lookup"><span data-stu-id="7466b-139">Retrieving the Functional Categories Supported by a Device</span></span>](retrieving-the-functional-categories-supported-by-a-device.md)
</dt> <dt>

[<span data-ttu-id="7466b-140">Abrufen der funktionalen Objekt Bezeichner für ein Gerät</span><span class="sxs-lookup"><span data-stu-id="7466b-140">Retrieving the Functional Object Identifiers for a Device</span></span>](retrieving-the-functional-object-identifiers-for-a-device.md)
</dt> <dt>

[<span data-ttu-id="7466b-141">Abrufen der von einem Gerät unterstützten Renderingfunktionen</span><span class="sxs-lookup"><span data-stu-id="7466b-141">Retrieving the Rendering Capabilities Supported by a Device</span></span>](retrieving-the-rendering-capabilities-supported-by-a-device.md)
</dt> <dt>

[<span data-ttu-id="7466b-142">Festlegen von Eigenschaften für mehrere Objekte</span><span class="sxs-lookup"><span data-stu-id="7466b-142">Setting Properties for Multiple Objects</span></span>](setting-properties-for-multiple-objects.md)
</dt> </dl>

 

 




