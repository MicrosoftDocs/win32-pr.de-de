---
description: Die GetCount-Methode ruft die Anzahl der Elemente in dieser Auflistung ab.
ms.assetid: b7c8acd2-67f2-47d3-b42a-26aa701fd613
title: 'Iportabledevicepropvariantcollection:: GetCount-Methode (portabledevicetypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.GetCount
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: d3a06cb5d89bc09a35a58f9269ba19c488c11e0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370006"
---
# <a name="iportabledevicepropvariantcollectiongetcount-method"></a><span data-ttu-id="eadec-103">Iportabledevicepropvariantcollection:: GetCount-Methode</span><span class="sxs-lookup"><span data-stu-id="eadec-103">IPortableDevicePropVariantCollection::GetCount method</span></span>

<span data-ttu-id="eadec-104">Die **GetCount** -Methode ruft die Anzahl der Elemente in dieser Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="eadec-104">The **GetCount** method retrieves the number of items in this collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="eadec-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="eadec-105">Syntax</span></span>


```C++
HRESULT GetCount(
  [in] DWORD *pcElems
);
```



## <a name="parameters"></a><span data-ttu-id="eadec-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="eadec-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eadec-107">*pcelems* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eadec-107">*pcElems* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eadec-108">Zeiger auf ein **DWORD** , das die Anzahl der Elemente in der Auflistung enthält.</span><span class="sxs-lookup"><span data-stu-id="eadec-108">Pointer to a **DWORD** that contains the number of items in the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eadec-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="eadec-109">Return value</span></span>

<span data-ttu-id="eadec-110">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="eadec-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="eadec-111">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="eadec-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="eadec-112">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="eadec-112">Return code</span></span>                                                                               | <span data-ttu-id="eadec-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="eadec-113">Description</span></span>                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="eadec-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="eadec-114"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="eadec-115">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="eadec-115">The method succeeded.</span></span><br/>                     |
| <dl> <span data-ttu-id="eadec-116"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="eadec-116"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="eadec-117">Ein erforderliches Zeigerargument war **null**.</span><span class="sxs-lookup"><span data-stu-id="eadec-117">A required pointer argument was **NULL**.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="eadec-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="eadec-118">Examples</span></span>

<span data-ttu-id="eadec-119">Ein Beispiel für die Verwendung dieser Methode finden Sie [unter Abrufen der von einem Gerät unterstützten funktionalen Kategorien](retrieving-the-functional-categories-supported-by-a-device.md).</span><span class="sxs-lookup"><span data-stu-id="eadec-119">For an example of how to use this method see [Retrieving the Functional Categories Supported by a Device](retrieving-the-functional-categories-supported-by-a-device.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="eadec-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eadec-120">Requirements</span></span>



| <span data-ttu-id="eadec-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eadec-121">Requirement</span></span> | <span data-ttu-id="eadec-122">Wert</span><span class="sxs-lookup"><span data-stu-id="eadec-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eadec-123">Header</span><span class="sxs-lookup"><span data-stu-id="eadec-123">Header</span></span><br/>  | <dl> <span data-ttu-id="eadec-124"><dt>Portablede vicetypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="eadec-124"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="eadec-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="eadec-125">Library</span></span><br/> | <dl> <span data-ttu-id="eadec-126"><dt>Portabledeviceguids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="eadec-126"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eadec-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eadec-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eadec-128">**Iportabledevicepropvariantcollection-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="eadec-128">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="eadec-129">Abrufen unterstützter Dienst Ereignisse</span><span class="sxs-lookup"><span data-stu-id="eadec-129">Retrieving Supported Service Events</span></span>](retrieving-supported-events.md)
</dt> <dt>

[<span data-ttu-id="eadec-130">Abrufen unterstützter Dienst Formate</span><span class="sxs-lookup"><span data-stu-id="eadec-130">Retrieving Supported Service Formats</span></span>](retrieving-supported-formats.md)
</dt> <dt>

[<span data-ttu-id="eadec-131">Abrufen unterstützter Dienst Methoden</span><span class="sxs-lookup"><span data-stu-id="eadec-131">Retrieving Supported Service Methods</span></span>](retrieving-supported-methods.md)
</dt> <dt>

[<span data-ttu-id="eadec-132">Abrufen der von einem Gerät unterstützten funktionalen Kategorien</span><span class="sxs-lookup"><span data-stu-id="eadec-132">Retrieving the Functional Categories Supported by a Device</span></span>](retrieving-the-functional-categories-supported-by-a-device.md)
</dt> <dt>

[<span data-ttu-id="eadec-133">Festlegen von Eigenschaften für mehrere Objekte</span><span class="sxs-lookup"><span data-stu-id="eadec-133">Setting Properties for Multiple Objects</span></span>](setting-properties-for-multiple-objects.md)
</dt> </dl>

 

 




