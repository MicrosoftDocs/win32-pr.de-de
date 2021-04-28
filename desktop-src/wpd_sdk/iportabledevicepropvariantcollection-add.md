---
description: 'IPortableDevicePropVariantCollection::Add-Methode: Die Add-Methode fügt der Auflistung ein Element hinzu.'
ms.assetid: e9e8975f-f9b8-4940-b967-020cf3812582
title: IPortableDevicePropVariantCollection::Add-Methode (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.Add
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 7aed732cb92ea7e0f2fb3c2ebdd615f643bc3107
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112458"
---
# <a name="iportabledevicepropvariantcollectionadd-method"></a><span data-ttu-id="6e084-103">IPortableDevicePropVariantCollection::Add-Methode</span><span class="sxs-lookup"><span data-stu-id="6e084-103">IPortableDevicePropVariantCollection::Add method</span></span>

<span data-ttu-id="6e084-104">Die **Add-Methode** fügt der Auflistung ein Element hinzu.</span><span class="sxs-lookup"><span data-stu-id="6e084-104">The **Add** method adds an item to the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e084-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6e084-105">Syntax</span></span>


```C++
HRESULT Add(
  [in] const PROPVARIANT *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="6e084-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6e084-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e084-107">*pValue* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="6e084-107">*pValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e084-108">Zeiger auf ein neues **PROPVARIANT-Objekt,** das der Auflistung hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="6e084-108">Pointer to a new **PROPVARIANT** object to add to the collection.</span></span> <span data-ttu-id="6e084-109">Diese Methode kopiert **die PROPVARIANT** in die Auflistung, daher sollten Sie Ihre lokale Kopie der Variablen durch Aufrufen **von PropVariantClear** nach dem Aufruf dieser Methode veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="6e084-109">This method copies the **PROPVARIANT** to the collection, so you should release your local copy of the variable by calling **PropVariantClear** after calling this method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e084-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6e084-110">Return value</span></span>

<span data-ttu-id="6e084-111">Die -Methode gibt ein **HRESULT zurück.**</span><span class="sxs-lookup"><span data-stu-id="6e084-111">The method returns an **HRESULT**.</span></span> <span data-ttu-id="6e084-112">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="6e084-112">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="6e084-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="6e084-113">Return code</span></span>                                                                          | <span data-ttu-id="6e084-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6e084-114">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="6e084-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6e084-115"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="6e084-116">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6e084-116">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6e084-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6e084-117">Remarks</span></span>

<span data-ttu-id="6e084-118">Wenn der VARTYPE für *pValue* VT VECTOR oder VT UI1 ist, wird das Festlegen und Abrufen eines Puffers mit \_ \_ **NULL-** oder Nullgröße nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6e084-118">When the VARTYPE for *pValue* is VT\_VECTOR or VT\_UI1, setting and retrieving a **NULL** or zero-sized buffer is not supported.</span></span> <span data-ttu-id="6e084-119">Beispielsweise sind weder pValue.caub.pElems = **NULL** noch pValue.caub.cElems = 0 zulässig.</span><span class="sxs-lookup"><span data-stu-id="6e084-119">For example, neither pValue.caub.pElems = **NULL** nor pValue.caub.cElems = 0 are allowed.</span></span>

<span data-ttu-id="6e084-120">Wenn ein Aufrufer versucht, ein Element eines anderen VARTYPE-Elements hinzuzufügen, das in der Auflistung enthalten ist, und der PROPVARIANT-Wert von dieser Schnittstelle nicht automatisch geändert werden kann, wird diese Methode fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="6e084-120">If a caller tries to add an item of a different VARTYPE contained in the collection and the PROPVARIANT value cannot be changed by this interface automatically, this method will fail.</span></span> <span data-ttu-id="6e084-121">Um den Auflistungstyp manuell zu ändern, rufen [**Sie IPortableDevicePropVariantCollection::ChangeType auf.**](iportabledevicepropvariantcollection-changetype.md)</span><span class="sxs-lookup"><span data-stu-id="6e084-121">To change the collection type manually, call [**IPortableDevicePropVariantCollection::ChangeType**](iportabledevicepropvariantcollection-changetype.md).</span></span>

## <a name="examples"></a><span data-ttu-id="6e084-122">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6e084-122">Examples</span></span>

<span data-ttu-id="6e084-123">Ein Beispiel für die Verwendung dieser Methode finden Sie unter Abrufen eines Objektbezeichners [aus einem persistenten eindeutigen Bezeichner.](retrieving-an-object-identifier-from-a-persistent-unique-identifier.md)</span><span class="sxs-lookup"><span data-stu-id="6e084-123">For an example of how to use this method, see [Retrieving an Object Identifier from a Persistent Unique Identifier](retrieving-an-object-identifier-from-a-persistent-unique-identifier.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="6e084-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6e084-124">Requirements</span></span>



| <span data-ttu-id="6e084-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6e084-125">Requirement</span></span> | <span data-ttu-id="6e084-126">Wert</span><span class="sxs-lookup"><span data-stu-id="6e084-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e084-127">Header</span><span class="sxs-lookup"><span data-stu-id="6e084-127">Header</span></span><br/>  | <dl> <span data-ttu-id="6e084-128"><dt>PortableDeviceTypes.h</dt></span><span class="sxs-lookup"><span data-stu-id="6e084-128"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="6e084-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6e084-129">Library</span></span><br/> | <dl> <span data-ttu-id="6e084-130"><dt>PortableDeviceGUIDs.lib</dt></span><span class="sxs-lookup"><span data-stu-id="6e084-130"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e084-131">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="6e084-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e084-132">**IPortableDevicePropVariantCollection-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="6e084-132">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="6e084-133">Verschieben von Inhalten auf dem Gerät</span><span class="sxs-lookup"><span data-stu-id="6e084-133">Moving Content on the Device</span></span>](moving-content-on-the-device.md)
</dt> <dt>

[<span data-ttu-id="6e084-134">Abrufen eines Objektbezeichners aus einem persistenten eindeutigen Bezeichner</span><span class="sxs-lookup"><span data-stu-id="6e084-134">Retrieving an Object Identifier from a Persistent Unique Identifier</span></span>](retrieving-an-object-identifier-from-a-persistent-unique-identifier.md)
</dt> </dl>

 

 




